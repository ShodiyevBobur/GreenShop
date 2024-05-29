<template>
  <div>
    <div id="products">
      <div class="flex justify-between py-4">
        <div class="flex justify-between gap-8">
          <a
            href="#products"
            :class="{ active: activeLink === 'all' }"
            @click="toggleActive('all')"
            class="border-b-2 cursor-pointer"
          >
            All Plants
          </a>
          <a
            href="#products"
            :class="{ active: activeLink === 'new' }"
            @click="toggleActive('new')"
            class="border-b-2 cursor-pointer"
          >
            New Arrivals
          </a>
          <a
            href="#products"
            :class="{ active: activeLink === 'sale' }"
            @click="toggleActive('sale')"
            class="border-b-2 cursor-pointer"
          >
            Sale
          </a>
        </div>
        <div class="hidden md:flex items-center">
          <p class="mr-2">Sort by:</p>
          <select>
            <option value="name">Name</option>
            <option value="price">Price</option>
          </select>
        </div>
      </div>
      <div class="grid grid-cols-2 md:grid-cols-3 mb-2 md:mb-8  gap-3 md:gap-10">
        <div v-for="(product, index) in products" :key="index">
          <div class="flex flex-col items-start gap-9 py-5 px-4 product_items">
            <img
              :src="product.image"
              alt="Product Image"
              class="md:w-[250px] md:h-[250px]"
            />
            <div>
              <h3>{{ product.description }}</h3>
              <div class="flex gap-5 items-start">
                <p class="text-green-600 font-bold">${{ product.price }}.00</p>
                <p
                  v-if="product.sale !== ''"
                  class="text-gray-600 line-through"
                >
                  ${{ product.sale }}.00
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="flex justify-end">
        <div v-for="num in 4">
          <button
            :class="{ active1: activeButton === num }"
            @click="toggleClass(num)"
            class="p-3 bg-white border rounded-md h-8 w-8 flex items-center justify-center hover:bg-green-300"
          >
            {{ num }}
          </button>
        </div>
        <button
          class="p-3 bg-white border rounded-md h-8 w-8 flex items-center justify-center"
        >
          >
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const activeLink = ref("");

    const toggleActive = (link) => {
      activeLink.value = link;
    };

    const activeButton = ref(null);

    const toggleClass = (num) => {
      activeButton.value = num;
    };

    return {
      toggleClass,
      activeButton,
      activeLink,
      toggleActive,
    };
  },
  data() {
    return {
      isActive: false,
      products: [
        {
          image: "./product.png",
          description: "Barberton Daisy",
          price: "120",
          sale: "",
        },
        {
          image: "/pr_gul.png",
          description: "Angel Wing Begonia",
          price: "105",
          sale: "",
        },
        {
          image: "./pr_tuvak.png",
          description: "Barberton Daisy",
          price: "134",
          sale: "229",
        },
        {
          image: "./product.png",
          description: "Jest Begonia",
          price: "112",
          sale: "",
        },
        {
          image: "./pr_gul.png",
          description: "Barberton Kels",
          price: "320",
          sale: "",
        },
        {
          image: "./pr_tuvak.png",
          description: "Superme Wing Begonia",
          price: "380",
          sale: "",
        },
        {
          image: "./product.png",
          description: "Olde Daisy",
          price: "160",
          sale: "",
        },
        {
          image: "./pr_gul.png",
          description: "Erst Polsj",
          price: "100",
          sale: "",
        },
        {
          image: "./pr_tuvak.png",
          description: "Termos Heraw",
          price: "230",
          sale: "",
        },
      ],
    };
  },
};
</script>

<style scoped>
a.active {
  border-bottom-color: rgb(45, 196, 45);
}
.product_items:hover {
  border-top: 2px solid #16a34a;
  background-color: rgb(251, 248, 248);
}
.active1 {
  background-color: #047857; /* Equivalent to bg-green-600 */
  color: white; /* Equivalent to text-white */
}
</style>

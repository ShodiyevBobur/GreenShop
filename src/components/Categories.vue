<template>
  <div>
    <div class="categories">
      <div class="py-3">
        <h3 class="text-[18px] font-bold py-3">Categories</h3>
        <div
          v-for="(cat, index) in categories"
          :key="index"
          class="flex justify-between ml-3 gap-5 py-[10px]"
        >
          <a href="#">{{ cat.name }}</a>
          <p>({{ cat.amount }})</p>
        </div>
      </div>
      <div class="py-3 price_range">
        <h3 class="text-[18px] font-bold py-3">Price Range</h3>
        <div class="flex flex-col ml-3">
          <input
            type="range"
            min="0"
            max="100"
            class="range range-xs w-full h-6 bg-transparent focus:outline-none focus:ring-0"
            style="--range-track-bg: #d1fae5; --range-thumb-bg: #10b981"
          />
          <p class="text-[15px] font-medium py-4">
            Price: <span class="text-green-600 font-bold">$38 - $1380</span>
          </p>
          <button
            class="py-3 w-[100px] bg-green-600 border rounded-md text-white"
          >
            Filter
          </button>
        </div>
      </div>
      <div class="sizes">
        <h3 class="text-[18px] font-bold py-3">Sizes</h3>
        <div
          v-for="({ name, amount }, index) in sizes"
          :key="index"
          class="flex justify-between ml-3"
        >
          <p>{{ name }}</p>
          <p>({{ amount }})</p>
        </div>
      </div>
      <div class="sale_banner flex justify-center flex-col items-center">
        <img src="../../public/Super Sale.png" alt="" />
        <h3 class="font-bold text-2xl">UP TO 75% OFF</h3>
        <img src="../../public/sale_banner.png" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      categories: [
        {
          name: "House Plants",
          amount: 34,
        },
        {
          name: "Potter Plants",
          amount: 12,
        },
        {
          name: "Seeds",
          amount: 14,
        },
        {
          name: "Small Plants",
          amount: 32,
        },
        {
          name: "Flowers",
          amount: 19,
        },
        {
          name: "Garden Plants",
          amount: 92,
        },
        {
          name: "Hellowe Plants",
          amount: 45,
        },
        {
          name: "Lollipo jerrys",
          amount: 92,
        },
        {
          name: "Superset Exos",
          amount: 45,
        },
      ],
      sizes: [
        { name: "Small", amount: 234 },
        { name: "Large", amount: 127 },
        { name: "Large", amount: 102 },
      ],
    };
  },
};
</script>

<style lang="css" scoped>
.sale_banner {
  background: linear-gradient(
    180deg,
    rgba(70, 163, 88, 0.1) 0%,
    rgba(70, 163, 88, 0.03) 100%
  );
}
</style>

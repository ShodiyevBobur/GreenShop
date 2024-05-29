<template>
  <div>
    <div class="container">
      <div class=" grid grid-cols-2 md:flex justify-between">
        <div v-for="(item, index) in newsletter" :key="index">
          <div>
            <img :src="item.image" alt="" class="w-[85px] h-[85px]" />
            <h3 class="text-[17px] font-bold">{{ item.title }}</h3>
            <p class="text-[#727272] w-[204px]">{{ item.description }}</p>
          </div>
        </div>
        <div class=" col-span-2 grid grid-cols-2 justify-between md:justify-normal  md:w-[30%] md:flex flex-col">
          <h3 class=" col-span-2 text-[12px] md:text-[18px] font-bold">
            Would you like to join newsletters?
          </h3>
          <div class=" col-span-2 flex relative py-4 items-center">
            <input
              type="text"
              class="drop-shadow-md w-[354px] h-[40px] outline-none px-2 border rounded-md pr-[80px]"
            />
            <button
              class="absolute py-2 w-[80px] bg-green-600 border rounded-md text-white ml-[280px]"
            >
              Join
            </button>
          </div>
          <p class="text-[#727272] col-span-2">
            We usually post offers and challenges in newsletter. We’re your
            online houseplant destination. We offer a wide range of houseplants
            and accessories shipped directly from our (green)house to yours!
          </p>
        </div>
      </div>
      <div class="  md:flex py-5 bg-[#46A3581A] gap-[150px] items-center ">
        <img src="../assets/Group.png" alt="" />
        <div class="flex gap-3">
          <img src="../assets/location.svg" alt="" />
          <p class="w-[200px]">70 West Buckingham Ave. Farmingdale, NY 11735</p>
        </div>
        <div class="flex gap-3">
          <img src="../assets/email.svg" alt="" />
          <p>contact@greenshop.com</p>
        </div>
        <div class="flex gap-3">
          <img src="../assets/call.svg" alt="" />
          <p>+88 01911 717 490</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newsletter: [
        {
          image: "./kaktus.png",
          title: "Garden Care",
          description:
            "We are an online plant shop offering a wide range of cheap and trendy plants.",
        },
        {
          image: "./kaktus2.png",
          title: "Plant Renovation",
          description:
            "We are an online plant shop offering a wide range of cheap and trendy plants.",
        },
        {
          image: "./kaktus3.png",
          title: "Watering Garden",
          description:
            "We are an online plant shop offering a wide range of cheap and trendy plants.",
        },
      ],
    };
  },
};
</script>

<style lang="css" scoped></style>

<template>
  <div>
    <div class="embla">
      <div class="embla__container">
        <div class="embla__slide">
          <div class="container">
            <div class="flex justify-between items-center px-5">
              <div class="w-[50%] flex flex-col gap-5 items-start">
                <h3 class="font-medium text-[#3D3D3D]">WELCOME TO GREENSHOP</h3>
                <h1 class="text-[70px] font-black leading-[70px]">
                  LET'S MAKE A BETTER <span class="text-green-600">PLANT</span>
                </h1>
                <p class="w-[587px] text-[#727272] font-normal">
                  We are an online plant shop offering a wide range of cheap and
                  trendy plants. Use our plants to create an unique Urban
                  Jungle. Order your favorite plants!
                </p>
                <button
                  class="py-3 px-8 mt-10 bg-green-600 border rounded-md text-white"
                >
                  SHOP NOW
                </button>
              </div>
              <div class="w-[50%]">
                <img src="../assets/mainGul.png" alt="" />
              </div>
            </div>
          </div>
        </div>
        <div class="embla__slide">
          <div class="container">
            <div class="flex justify-between items-center px-5">
              <div class="w-[50%] flex flex-col gap-5 items-start">
                <h3 class="font-medium text-[#3D3D3D]">WELCOME TO GREENSHOP</h3>
                <h1 class="text-[70px] font-black leading-[70px]">
                  LET'S MAKE A BETTER <span class="text-green-600">PLANT</span>
                </h1>
                <p class="w-[587px] text-[#727272] font-normal">
                  We are an online plant shop offering a wide range of cheap and
                  trendy plants. Use our plants to create an unique Urban
                  Jungle. Order your favorite plants!
                </p>
                <button
                  class="py-3 px-8 mt-10 bg-green-600 border rounded-md text-white"
                >
                  SHOP NOW
                </button>
              </div>
              <div class="w-[50%]">
                <img src="../assets/mainGul.png" alt="" />
              </div>
            </div>
          </div>
        </div>
        <div class="embla__slide">
          <div class="container">
            <div class="flex justify-between items-center px-5">
              <div class="w-[50%] flex flex-col gap-5 items-start">
                <h3 class="font-medium text-[#3D3D3D]">WELCOME TO GREENSHOP</h3>
                <h1 class="text-[70px] font-black leading-[70px]">
                  LET'S MAKE A BETTER <span class="text-green-600">PLANT</span>
                </h1>
                <p class="w-[587px] text-[#727272] font-normal">
                  We are an online plant shop offering a wide range of cheap and
                  trendy plants. Use our plants to create an unique Urban
                  Jungle. Order your favorite plants!
                </p>
                <button
                  class="py-3 px-8 mt-10 bg-green-600 border rounded-md text-white"
                >
                  SHOP NOW
                </button>
              </div>
              <div class="w-[50%]">
                <img src="../assets/mainGul.png" alt="" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div></div>
  </div>
</template>

<script>
import { onMounted } from "vue";

export default {
  name: "YourComponent",
  setup() {
    onMounted(() => {
      const emblaNode = document.querySelector(".embla");
      const options = { loop: false };
      const plugins = [EmblaCarouselAutoplay()];
      EmblaCarousel(emblaNode, options, plugins);
    });
  },
};
</script>

<style scoped>
.embla {
  overflow: hidden;
}
.embla__container {
  display: flex;
}
.embla__slide {
  flex: 0 0 100%;
  min-width: 0;
}
</style>


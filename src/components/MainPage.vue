<template>
  <div>
    <div class="md:embla">
      <div class="md:embla__container">
        <div class="md:embla__slide">
          <div class="container">
            <div class="flex justify-between items-center md:px-5">
              <div class="w-[80%] flex flex-col gap-5 items-start">
                <h3 class="text-[11px] md:font-medium text-[#3D3D3D]">
                  WELCOME TO GREENSHOP
                </h3>
                <h1
                  class="text-[24px] leading-[24px] md:text-[70px] font-black md:leading-[70px]"
                >
                  LET'S MAKE A BETTER <span class="text-green-600">PLANT</span>
                </h1>
                <p class="text-[12px] md:w-[587px] text-[#727272] font-normal">
                  We are an online plant shop offering a wide range of cheap and
                  trendy plants. Use our plants to create an unique Urban
                  Jungle. Order your favorite plants!
                </p>
                <button
                  class="text-[12px] flex items-center text-green-600 md:py-3 md:px-8 md:mt-10 md:bg-green-600 md:border md:rounded-md md:text-white"
                >
                  SHOP NOW
                  <div class="md:hidden">
                    <svg
                      width="16"
                      height="16"
                      viewBox="0 0 16 16"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M13.167 7.81712L3.16699 7.81712"
                        stroke="#46A358"
                        stroke-width="1.5"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                      />
                      <path
                        d="M9.13379 3.8008C9.13379 3.8008 13.1671 5.9748 13.1671 7.81613C13.1671 9.6588 9.13379 11.8335 9.13379 11.8335"
                        stroke="#46A358"
                        stroke-width="1.5"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                      />
                    </svg>
                  </div>
                </button>
              </div>
              <div class="w-[50%]">
                <img src="../assets/mainGul.png" alt="" />
              </div>
            </div>
          </div>
        </div>
        <div class="hidden md:embla__slide">
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
        <div class="hidden  md:embla__slide">
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

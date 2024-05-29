<template>
  <div>
    <Login v-if="isModal" @close="closeModal" />
    <div class="container">
      <div
        class="hidden md:flex justify-between border border-x-white border-b-green-700 py-8"
      >
        <div>
          <img src="../assets/Group.png" alt="Logo" />
        </div>
        <div class="flex gap-12">
          <a href="#">Home</a>
          <a href="#">Shop</a>
          <a href="#">Plant Care</a>
          <a href="#">Blogs</a>
        </div>
        <div class="flex items-center gap-4 relative">
          <img src="../assets/search.svg" alt="Search Icon" class="h-[32px]" />
          <div
            class="w-[12px] h-[12px] rounded-full bg-green-700 flex items-center justify-center absolute ml-[65px] mb-7"
          >
            <span class="text-white text-[10px]">6</span>
          </div>
          <img src="../assets/cart.svg" alt="Cart Icon" class="h-[32px]" />
          <div
            class="flex items-center gap-2 border rounded-md bg-green-600 text-white py-3 px-5 cursor-pointer"
            @click="toggleModal"
          >
            <img src="../assets/login.svg" alt="Login Icon" />
            <button class="text-sm">Login</button>
          </div>
        </div>
      </div>
      <div class="flex mt-4 md:hidden">
        <div class="bg-[#F8F8F8] h-[45px] w-[90%] flex items-center md:hidden ">
          <svg
            width="22"
            height="22"
            viewBox="0 0 22 22"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M10.5296 3.2436C6.50469 3.2436 3.24326 6.50244 3.24326 10.5207C3.24326 14.539 6.50469 17.7978 10.5296 17.7978C12.5376 17.7978 14.3546 16.9875 15.6732 15.675C16.9977 14.3566 17.8159 12.5347 17.8159 10.5207C17.8159 6.50244 14.5545 3.2436 10.5296 3.2436ZM1.83301 10.5207C1.83301 5.72204 5.72737 1.83334 10.5296 1.83334C15.3318 1.83334 19.2262 5.72204 19.2262 10.5207C19.2262 12.6706 18.4436 14.6389 17.149 16.1554L19.9595 18.9627C20.2351 19.2379 20.2353 19.6843 19.9601 19.9599C19.6849 20.2354 19.2384 20.2356 18.9629 19.9604L16.1497 17.1505C14.6343 18.4335 12.6719 19.2081 10.5296 19.2081C5.72737 19.2081 1.83301 15.3194 1.83301 10.5207Z"
              fill="#A5A5A5"
            />
          </svg>
          <input
            type="text"
            class="focus:border-none focus:outline-none bg-[#F8F8F8] w-full"
          />
        </div>
        <button @click="toggleModal" class="bg-green-500 p-3 rounded-lg">
          <svg
            width="22"
            height="22"
            viewBox="0 0 22 22"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M10.2144 16.3926H4.28125"
              stroke="white"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M13.9375 16.3934C13.9375 18.2651 14.5617 18.8884 16.4325 18.8884C18.3033 18.8884 18.9274 18.2651 18.9274 16.3934C18.9274 14.5218 18.3033 13.8984 16.4325 13.8984C14.5617 13.8984 13.9375 14.5218 13.9375 16.3934Z"
              stroke="white"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              d="M12.9951 6.77801H18.9274"
              stroke="white"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M9.27202 6.77677C9.27202 4.90595 8.64786 4.2818 6.77704 4.2818C4.9054 4.2818 4.28125 4.90595 4.28125 6.77677C4.28125 8.64841 4.9054 9.27175 6.77704 9.27175C8.64786 9.27175 9.27202 8.64841 9.27202 6.77677Z"
              stroke="white"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import Login from "../components/Login.vue";

export default {
  name: "ParentComponent",
  components: {
    Login,
  },
  data() {
    return {
      isModal: false,
    };
  },
  methods: {
    toggleModal() {
      this.isModal = !this.isModal;
    },
    closeModal() {
      this.isModal = false;
    },
  },
};
</script>

<style lang="css" scoped>
/* Add your styles here */
</style>

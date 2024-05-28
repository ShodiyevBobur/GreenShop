<template>
  <div>
    <Login v-if="isModal" @close="closeModal" />
    <div class="container">
      <div class="flex justify-between border border-x-white border-b-green-700 py-8">
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
    </div>
  </div>
</template>

<script>
import Login from '../components/Login.vue';

export default {
  name: 'ParentComponent',
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

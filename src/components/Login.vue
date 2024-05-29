<template>
  <div>
    <div
      @click="closeModal"
      class="fixed bg-black/60 top-0 left-0 w-full h-screen md:h-screen z-10"
    ></div>
    <div
      class="fixed bg-white top-1/5 md:top-1/2 left-1/2 rounded -translate-x-1/2 md:-translate-y-1/2 w-[95%] md:w-[500px] p-5 z-20"
    >
      <div class="flex justify-end">
        <button @click="closeModal">X</button>
      </div>
      <div class="flex justify-center divide-x-2 divide-green-600">
        <button
          @click="content = 'login'"
          class="py-1 px-5 font-semibold text-xl"
        >
          login
        </button>
        <button
          @click="content = 'register'"
          class="py-1 px-5 font-semibold text-[20px]"
        >
          Register
        </button>
      </div>
      <div v-if="content == 'login'" class="w-full md:w-[360px] mx-auto">
        <p class="text-[#3D3D3D] text-center p-5 text-[14px]">
          Enter your username and password to login.
        </p>
        <div class="px-5">
          <input
            class="text-[#A5A5A5] py-2 px-4 border rounded w-full"
            type="email"
            placeholder="greenshop@email.com"
          />
        </div>
        <div class="p-5">
          <input
            class="text-[#A5A5A5] py-2 px-4 border rounded pr-28"
            type="password"
            placeholder="password"
          />
        </div>
        <p class="px-5 text-end text-green-400">Forgot Password?</p>
        <button
          class="bg-[#46A358] px-[138px] py-2 m-5 my-3 text-white rounded hover:bg-[#266933]"
        >
          Login
        </button>
        <p class="text-center text-[#3D3D3D] m-">Or login with</p>
        <div class="">
          <button
            class="flex gap-2 items-center py-2 px-[73px] text-center border rounded m-5 hover:text-green-600"
          >
            <svg
              width="20"
              height="20"
              viewBox="0 0 20 20"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <g clip-path="url(#clip0_9_990)">
                <path
                  d="M16.4336 17.6055C14.6992 19.0703 12.4493 20 10 20C6.35547 20 3.15621 17.9922 1.42188 15.0625L2.07117 12.0695L4.94922 11.5352C5.61719 13.6914 7.63278 15.2734 10 15.2734C11.1484 15.2734 12.2148 14.9102 13.0938 14.2656L15.8594 14.6875L16.4336 17.6055Z"
                  fill="#59C36A"
                />
                <path
                  d="M16.4336 17.6055L15.8594 14.6875L13.0937 14.2656C12.2148 14.9102 11.1484 15.2734 10 15.2734V20C12.4493 20 14.6992 19.0703 16.4336 17.6055Z"
                  fill="#00A66C"
                />
                <path
                  d="M4.72656 10C4.72656 10.539 4.8086 11.0546 4.94922 11.5352L1.42188 15.0625C0.542969 13.5859 0 11.8515 0 10C0 8.1484 0.542969 6.41406 1.42188 4.9375L4.25285 5.42473L4.94922 8.46484C4.8086 8.94527 4.72656 9.4609 4.72656 10Z"
                  fill="#FFDA2D"
                />
                <path
                  d="M20 10C20 13.0468 18.5899 15.7773 16.4336 17.6055L13.0938 14.2656C13.7734 13.7734 14.3477 13.1171 14.7227 12.3437H10C9.67184 12.3437 9.41406 12.0859 9.41406 11.7578V8.24219C9.41406 7.91402 9.67184 7.65625 10 7.65625H19.25C19.5312 7.65625 19.7773 7.85543 19.8242 8.13668C19.9414 8.74609 20 9.37887 20 10Z"
                  fill="#4086F4"
                />
                <path
                  d="M14.7227 12.3437C14.3477 13.1171 13.7734 13.7734 13.0938 14.2656L16.4336 17.6055C18.5899 15.7773 20 13.0469 20 10C20 9.37887 19.9414 8.74609 19.8242 8.13668C19.7773 7.85543 19.5312 7.65625 19.25 7.65625H10V12.3437H14.7227Z"
                  fill="#4175DF"
                />
                <path
                  d="M16.5977 2.79293C16.6094 2.95699 16.5391 3.10937 16.4336 3.22652L13.9258 5.72262C13.7266 5.93355 13.3985 5.95699 13.1641 5.78121C12.2382 5.08984 11.1484 4.72656 10 4.72656C7.63278 4.72656 5.61719 6.30855 4.94922 8.46484L1.42188 4.9375C3.15621 2.00781 6.35547 0 10 0C12.332 0 14.6055 0.859375 16.3867 2.35934C16.5156 2.46484 16.5859 2.62887 16.5977 2.79293Z"
                  fill="#FF641A"
                />
                <path
                  d="M13.1641 5.78121C13.3984 5.95703 13.7265 5.93355 13.9257 5.72262L16.4336 3.22652C16.5391 3.10938 16.6094 2.95703 16.5976 2.79293C16.5859 2.62883 16.5156 2.46484 16.3867 2.35934C14.6055 0.859375 12.332 0 10 0V4.72656C11.1484 4.72656 12.2382 5.08984 13.1641 5.78121Z"
                  fill="#F03800"
                />
              </g>
              <defs>
                <clipPath id="clip0_9_990">
                  <rect width="20" height="20" fill="white" />
                </clipPath>
              </defs>
            </svg>
            Login with Google
          </button>
        </div>
        <button
          class="flex gap-2 py-2 px-[65px] text-center border rounded m-5 items-center hover:text-green-600"
        >
          <svg
            width="20"
            height="20"
            viewBox="0 0 20 20"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <g clip-path="url(#clip0_9_1018)">
              <path
                d="M13.3308 3.32083H15.1566V0.140826C14.8416 0.0974924 13.7583 -7.62939e-06 12.4966 -7.62939e-06C6.71993 -7.62939e-06 8.2916 6.54166 8.0616 7.49999H5.15576V11.055H8.06076V20H11.6224V11.0558H14.4099L14.8524 7.50083H11.6216C11.7783 5.14749 10.9874 3.32083 13.3308 3.32083Z"
                fill="#3B5999"
              />
            </g>
            <defs>
              <clipPath id="clip0_9_1018">
                <rect width="20" height="20" fill="white" />
              </clipPath>
            </defs>
          </svg>
          Login with Facebook
        </button>
      </div>
      <div v-if="content == 'register'" class="w-[360px] mx-auto">
        <p class="text-[#3D3D3D] text-center p-5 text-[14px]">
          Enter your username and password to login.
        </p>
        <div class="px-5 py-2">
          <input
            class="text-[#A5A5A5] py-2 px-4 border rounded pr-28"
            type="text"
            placeholder="someUsername"
          />
        </div>
        <div class="px-5 py-2">
          <input
            class="text-[#A5A5A5] py-2 px-4 border rounded pr-28"
            type="email"
            placeholder="some@email.com"
          />
        </div>
        <div class="px-5 py-2">
          <input
            class="text-[#A5A5A5] py-2 px-4 border rounded pr-28"
            type="password"
            placeholder="password"
          />
          <!-- <img src="../../public/Hide.png" alt="" /> -->
        </div>
        <div class="px-5 py-2">
          <input
            class="text-[#A5A5A5] py-2 px-4 border rounded pr-28"
            type="password"
            placeholder="Connfirm password"
          />
          <!-- <img src="../../public/Hide.png" alt="" /> -->
        </div>

        <button
          class="bg-[#46A358] px-[125px] py-2 m-5 my-2 text-white rounded hover:bg-[#266933]"
        >
          Register
        </button>
        <p class="text-center text-[#3D3D3D] m-1">Or register with</p>
        <div class="">
          <button
            class="flex gap-2 items-center py-2 px-[73px] text-center border rounded m-5 my-3 hover:text-green-500"
          >
            <svg
              width="20"
              height="20"
              viewBox="0 0 20 20"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <g clip-path="url(#clip0_9_990)">
                <path
                  d="M16.4336 17.6055C14.6992 19.0703 12.4493 20 10 20C6.35547 20 3.15621 17.9922 1.42188 15.0625L2.07117 12.0695L4.94922 11.5352C5.61719 13.6914 7.63278 15.2734 10 15.2734C11.1484 15.2734 12.2148 14.9102 13.0938 14.2656L15.8594 14.6875L16.4336 17.6055Z"
                  fill="#59C36A"
                />
                <path
                  d="M16.4336 17.6055L15.8594 14.6875L13.0937 14.2656C12.2148 14.9102 11.1484 15.2734 10 15.2734V20C12.4493 20 14.6992 19.0703 16.4336 17.6055Z"
                  fill="#00A66C"
                />
                <path
                  d="M4.72656 10C4.72656 10.539 4.8086 11.0546 4.94922 11.5352L1.42188 15.0625C0.542969 13.5859 0 11.8515 0 10C0 8.1484 0.542969 6.41406 1.42188 4.9375L4.25285 5.42473L4.94922 8.46484C4.8086 8.94527 4.72656 9.4609 4.72656 10Z"
                  fill="#FFDA2D"
                />
                <path
                  d="M20 10C20 13.0468 18.5899 15.7773 16.4336 17.6055L13.0938 14.2656C13.7734 13.7734 14.3477 13.1171 14.7227 12.3437H10C9.67184 12.3437 9.41406 12.0859 9.41406 11.7578V8.24219C9.41406 7.91402 9.67184 7.65625 10 7.65625H19.25C19.5312 7.65625 19.7773 7.85543 19.8242 8.13668C19.9414 8.74609 20 9.37887 20 10Z"
                  fill="#4086F4"
                />
                <path
                  d="M14.7227 12.3437C14.3477 13.1171 13.7734 13.7734 13.0938 14.2656L16.4336 17.6055C18.5899 15.7773 20 13.0469 20 10C20 9.37887 19.9414 8.74609 19.8242 8.13668C19.7773 7.85543 19.5312 7.65625 19.25 7.65625H10V12.3437H14.7227Z"
                  fill="#4175DF"
                />
                <path
                  d="M16.5977 2.79293C16.6094 2.95699 16.5391 3.10937 16.4336 3.22652L13.9258 5.72262C13.7266 5.93355 13.3985 5.95699 13.1641 5.78121C12.2382 5.08984 11.1484 4.72656 10 4.72656C7.63278 4.72656 5.61719 6.30855 4.94922 8.46484L1.42188 4.9375C3.15621 2.00781 6.35547 0 10 0C12.332 0 14.6055 0.859375 16.3867 2.35934C16.5156 2.46484 16.5859 2.62887 16.5977 2.79293Z"
                  fill="#FF641A"
                />
                <path
                  d="M13.1641 5.78121C13.3984 5.95703 13.7265 5.93355 13.9257 5.72262L16.4336 3.22652C16.5391 3.10938 16.6094 2.95703 16.5976 2.79293C16.5859 2.62883 16.5156 2.46484 16.3867 2.35934C14.6055 0.859375 12.332 0 10 0V4.72656C11.1484 4.72656 12.2382 5.08984 13.1641 5.78121Z"
                  fill="#F03800"
                />
              </g>
              <defs>
                <clipPath id="clip0_9_990">
                  <rect width="20" height="20" fill="white" />
                </clipPath>
              </defs>
            </svg>
            Login with Google
          </button>
        </div>
        <button
          class="flex gap-2 py-2 px-[65px] text-center border rounded mt-5 mb-1 mx-5 items-center hover:text-green-500"
        >
          <svg
            width="20"
            height="20"
            viewBox="0 0 20 20"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <g clip-path="url(#clip0_9_1018)">
              <path
                d="M13.3308 3.32083H15.1566V0.140826C14.8416 0.0974924 13.7583 -7.62939e-06 12.4966 -7.62939e-06C6.71993 -7.62939e-06 8.2916 6.54166 8.0616 7.49999H5.15576V11.055H8.06076V20H11.6224V11.0558H14.4099L14.8524 7.50083H11.6216C11.7783 5.14749 10.9874 3.32083 13.3308 3.32083Z"
                fill="#3B5999"
              />
            </g>
            <defs>
              <clipPath id="clip0_9_1018">
                <rect width="20" height="20" fill="white" />
              </clipPath>
            </defs>
          </svg>
          Login with Facebook
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      content: "login",
    };
  },
  methods: {
    closeModal() {
      this.$emit("close");
    },
  },
};
</script>

<style lang="css" scoped></style>

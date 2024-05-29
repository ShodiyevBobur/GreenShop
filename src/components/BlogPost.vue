<template>
  <div>
    <div class="container">
      <div class="flex flex-col items-center py-8">
        <h2 class="md:text-[30px] font-bold">OUR BLOG POST</h2>
        <p class="text-[#727272] text-[12px] md:text-[16px]">
          We are an online plant shop offering a wide range of cheap and trendy
          plants.
        </p>    
      </div>
      <div class=" md:flex items-center justify-between">
        <div
          v-for="(post, index) in blogs"
          :key="index"
          class="flex flex-col items-center mt-4"
        >
          <img :src="post.image" alt="" class=" w-full  md:w-[270px] md:h-[220px]" />
          <div class="flex  md:px-3 flex-col md:w-[270px] items-start gap-1">
            <p class="text-green-600">{{ post.date }}</p>
            <h3 class="text-[20px] font-bold w-[189px]">{{ post.title }}</h3>
            <p class="text-[#727272]">{{ post.description }}</p>
            <button class="text-semibold hover:text-green-600">Read More -></button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      blogs: [
        {
          image: "./01.png",
          date: "September 12  I Read in 6 minutes",
          title: "Cactus & Succulent Care Tips",
          description:
            "Cacti are succulents are easy care plants for any home or patio. ",
        },
        {
          image: "./02.png",
          date: "September 13  I Read in 2 minutes",
          title: "Top 10 Succulents for Your Home",
          description:
            "Best in hanging baskets. Prefers medium to high light. ",
        },
        {
          image: "./03.png",
          date: "September 15  I Read in 3 minutes",
          title: "Cacti & Succulent Care Tips",
          description:
            "Cacti are succulents are easy care plants for any home or patio. ",
        },
        {
          image: "./04.png",
          date: "September 12  I Read in 6 minutes",
          title: "Best Houseplants Room by Room",
          description:
            "The benefits of houseplants are endless. In addition to.. ",
        },
      ],
    };
  },
};
</script>

<style lang="css" scoped></style>

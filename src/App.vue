<script setup>
import moment from "moment";
import {photos} from "./data.ts";

var a = moment("20241117", "YYYYMMDD");
  var b = moment();
  const formattedTime = moment.duration(b.diff(a)).days()
</script>

<template>
  <div class="absolute min-h-screen w-full bg-pink-50 flex flex-col items-center justify-center">
        <h1 class="text-center font-bold text-3xl text-pretty-50">张云起和布热比耶在一起{{formattedTime}}天啦！</h1>
    <div class="container mx-auto">
      <h2 class="w-full text-left text-2xl m-5 font-bold">我们的点点滴滴:</h2>
      <div class="grid grid-cols-6 gap-8 ">
      <div v-for="image in photos" :key="image.id">
        <img :src="image.src" alt=""/>
      </div></div>
    </div>

  </div>
  <div class="absolute ">
    <div class="relative container mx-auto h-fit">
      <h1 class="font-bold text-2xl ">Love Forever</h1>

    </div>

  </div>

</template>

<style scoped>

</style>

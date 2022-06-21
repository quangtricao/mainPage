<template>
  <div>
    <img :src="source" alt="/" />
    <div class="p-4 bg-slate-100 rounded-md">
      <div class="flex justify-between">
        <span
          class=" bg-red-200 text-red-500 rounded-md py-1 px-2 inline-block font-semibold "> <nuxt-link to="/">{{ name }}</nuxt-link></span>
        <span class="text-gray-400"><i class="fa-solid fa-calendar mr-1"></i>06/05/2022</span>
      </div>
      <h4 class="mt-4 text-xl font-semibold">
        <nuxt-link to="/">{{ content }}</nuxt-link>
      </h4>
      <button @click="printLink">Print</button>
    </div>
  </div>
</template>

<script>
export default {
    props: {
      source: {

      },
      name: {
        type: String,
        required: true,
      },
      content: {
        type: String,
        required: true,
      },
    },
    methods: {
      printLink() {
        console.log(this.source);
      }
    }
};
</script>
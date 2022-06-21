<template>
  <div>
    <div class="flex">
      <img class="rounded-md w-48 object-cover" :src="source" alt="/" />
      <div class="mt-2 ml-5">
        <span class="text-gray-400 block"><i class="fa-solid fa-calendar mr-1"></i>06/05/2022</span>
        <h4 class="mt-3 text-xl font-semibold">
          {{name}}
        </h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    props: {
        name: {
            type: String,
            required: true,
        },
        source: {

        },
    }
}
</script>

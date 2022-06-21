<template>

    <div>
      <img src="" alt="/" />
      <div class="p-2 bg-slate-100 rounded-md">
        <div>
          <span class="text-gray-400"
            ><i class="fa-solid fa-calendar mr-1"></i>06/05/2022</span
          >
        </div>
        <h4 class="mt-4 text-md font-medium">
          <nuxt-link to="/"> {{ name }}</nuxt-link>
        </h4>
      </div>
    </div>

</template>
<script>
export default {
    props: {
        source: {
            type: String,
            required: false,
        },
        name: {
            type: String,
            required: true,
        }
    }
}
</script>

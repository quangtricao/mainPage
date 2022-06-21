<template>
    <div>
        <div class="grid grid-cols-2">
        <h3 class="font-semibold text-2xl border-b-4 border-red-500 w-max"> {{ text1 }}</h3>
        <nuxt-link class="text-right text-red-500 hover:text-red-300" to="/">{{ text2 }} <i class="fa-solid fa-right-long"></i
        ></nuxt-link>
      </div>
    </div>
</template>

<script>
export default {
    props: {
        text1: {
            type: String,
            required: true,
        },
        text2: {
            type: String,
            required: true,
        }
    }
}
</script>

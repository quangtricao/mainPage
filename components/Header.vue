<template>
  <header>
    <div class="bg-gray-200">
      <div class="max-w-7xl py-3 mx-auto">
        <h4 class="font-semibold">
          Bộ thông tin và truyền thông chuyển đổi số quốc gia
        </h4>
      </div>
    </div>
    <div class="max-w-7xl mx-auto py-5">
      <div class="grid grid-cols-3 items-center">
        <div class="flex items-center">
          <img class="mr-5" src="~/assets/images/logo.png" alt="logo" />
          <div class="font-bold">
            Câu chuyện chuyển đổi số của 63 tỉnh thành phố doanh nghiệp
          </div>
        </div>
        <div class="col-span-2">
          <ul class="flex gap-5 justify-end">
            <li class="hover:text-red-600" v-for="(item, index) in headName" :key="index" >
              <nuxt-link :to="item.route"> {{ item.name }} </nuxt-link>
            </li>

            <li>
              <a href="#"><i class="fa-solid fa-magnifying-glass"></i></a>
            </li>
            <button>
              <a
                class="
                  bg-red-500
                  hover:bg-red-400
                  text-white
                  py-2
                  px-3
                  rounded-md
                "
                href="#"
                >Đăng nhập</a
              >
            </button>
          </ul>
        </div>
      </div>
    </div>
    <section class="banner py-28">
      <div class="max-w-7xl mx-auto">
        <h1 class="text-white text-4xl">Success comes from sharing</h1>
      </div>
    </section>
  </header>
</template>

<script>
export default {
  data() {
    return {
      headName: [
        { name: "TRANG CHỦ", route: "/" },
        { name: "GIỚI THIỆU", route: "/GioiThieu" },
        { name: "VIDEO", route: "/Video" },
        { name: "CHUYÊN MỤC", route: "/ChuyenMuc" },
        { name: "BẢN ĐỒ", route: "/BanDo" },
        { name: "LIÊN HỆ", route: "/LienHe" },
      ],
    };
  },
};
</script>


<style scoped>
.banner {
  background-image: url("~/assets/images/bg-banner.png");
  background-size: cover;
  background-repeat: none;
}
</style>
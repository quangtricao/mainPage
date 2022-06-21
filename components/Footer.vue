<template>
  <div>
    <footer class="mt-20 border-t-2 border-red-500 py-16">
      <div class="grid grid-cols-5 max-w-7xl mx-auto">
        <div>
          <img src="~assets/images/logo.png" alt="" />
        </div>
        <div>
          <h2 class="font-semibold text-lg mb-3">Chủ đề</h2>
          <ul class="flex flex-col gap-y-2">
            <li class="hover:text-red-600" v-for="(item,index) in chuDeObject" :key="index" ><nuxt-link :to="item.route"> {{ item.name }} </nuxt-link></li>
          </ul>
        </div>
        <div>
          <h2 class="font-semibold text-lg mb-3">Chuyên mục</h2>
          <ul class="flex flex-col gap-y-2">
            <li class="hover:text-red-600" v-for="(item,index) in chuyenMucObject" :key="index" ><nuxt-link :to="item.route"> {{ item.name }} </nuxt-link></li>
          </ul>
        </div>
        <div class="col-span-2">
          <h2 class="font-semibold text-lg mb-3">
            CƠ QUAN CHỦ QUẢN: BỘ THÔNG TIN VÀ TRUYỀN THÔNG
          </h2>
          <ul class="flex flex-col gap-y-2">
            <li>
              <i class="mr-3 fa-solid fa-earth-americas"></i> Đơn vị đồng quản
              lý: Vụ Hợp tác quốc tế - Cục Tin học hóa
            </li>
            <li>
              <i class="mr-3 fa-solid fa-location-dot"></i> Địa chỉ: 18 Nguyễn
              Du, Hai Bà Trưng – Hà Nội (Tầng 3)
            </li>
            <li>
              <i class="mr-3 fa-solid fa-phone"></i> Điện thoại: +84-24-39430204
              / +84-24-37821766
            </li>
            <li>
              <i class="mr-3 fa-solid fa-envelope"></i> Email: t63@mic.gov.vn
            </li>
          </ul>
        </div>
      </div>
    </footer>
    <div class="border-t-2 border-gray-300">
      <div class="py-4 grid grid-cols-2 max-w-7xl mx-auto">
        <h4 class="text-red-500 font-medium">
          Bộ Thông tin và Truyền thông - Chương trình Chuyển đổi số Quốc gia
        </h4>
        <div class="text-right">
          <span class="inline-block mx-3"
            ><i class="fa-solid fa-wifi text-orange-500"></i
          ></span>
          <span class="inline-block mx-3"
            ><i class="fa-brands fa-youtube text-red-500"></i
          ></span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            chuDeObject: [
                {name:"Video mới" , route: "/"},
                {name:"Câu chuyện mới" , route: "/"},
                {name:"Chính phủ số" , route: "/"},
                {name:"Kinh tế số" , route: "/"},
                {name:"Xã hội số" , route: "/"},
                {name:"Công nghệ số" , route: "/"},
            ],
            chuyenMucObject: [
                {name:"Trang chủ" , route: "/"},
                {name:"Giới thiệu" , route: "/"},
                {name:"Chuyên mục" , route: "/"},
                {name:"Bản đồ" , route: "/"},
                {name:"Liên hệ" , route: "/"},
            ]
        }
    }
}
</script>

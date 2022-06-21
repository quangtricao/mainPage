<template>
  <div>
    <section class="max-w-7xl mx-auto pt-10 pb-8 border-b-2 border-gray-400">
      <component-header text1="Video mới" text2="Xem thêm các video khác"></component-header>

      <div class="grid grid-cols-2 gap-10 mt-10">
        <div class="pr-10">
          <div class="flex justify-between">
            <span class="bg-red-200 text-red-500 rounded-md py-1 px-2 inline-block font-semibold ">Chính quyền số</span>
            <span class="text-gray-400"><i class="fa-solid fa-calendar mr-1"></i>06/05/2022</span>
          </div>
          <h3 class="text-4xl my-5"> Kho dữ liệu dùng chung thành phố Đà Nẵng </h3>
          <p>
            Chuyển đổi số là sử dụng công nghệ số và dựa trên dữ liệu số. Trong
            quá trình triển khai ứng dụng CNTT, Chính phủ điện tử và chính quyền
            điện tử đã hình thành một số cơ sở dữ liệu.
          </p>
          <nuxt-link class="mt-5 inline-block bg-red-500 hover:bg-red-400 text-white py-2 px-4 rounded-md" to="/">Xem ngay</nuxt-link>
        </div>
        <div>
          <img
            class="object-cover rounded-sm"
            src="~/assets/images/blog/2.png"
            alt="blog 1"
          />
        </div>
      </div>

      <div class=" grid sm:grid-cols-1 sm:grid-rows-auto lg:grid-cols-2 lg:grid-rows-auto xl:grid-cols-3 xl:grid-rows-2 gap-8 mt-16 " >
        <video-moi v-for="(item, index) in objectVideoMoi" :key="index" :source="item.source" :name="item.name" :content="item.content" ></video-moi>
      </div>
    </section>

    <section class="max-w-7xl mx-auto pt-10 pb-10 border-b-2 border-gray-400">
      <component-header text1="Câu chuyện mới" text2="Xem thêm các câu chuyện khác"></component-header>

      <div class="grid grid-cols-2 gap-10 mt-10">
        <div>
          <img class="rounded-md" src="~/assets/images/blog/8.png" alt="/" />
          <div class="mt-2">
            <span class="text-gray-400 block"
              ><i class="fa-solid fa-calendar mr-1"></i>06/05/2022</span
            >
            <h4 class="mt-3 text-xl font-semibold">
              Triển khai áp dụng Nền tảng Sổ tay đảng viên tại Thái Nguyên
            </h4>
          </div>
        </div>
        <div class="grid grid-cols-1 grid-rows-3 gap-5">
          <cau-chuyen-moi v-for="(item,index) in objectCauChuyenMoi" :key="index" :name="item.name" :source="item.source"></cau-chuyen-moi>
        </div>
      </div>
    </section>

    <six-component header="Chính phủ số"></six-component>
    <six-component header="Kinh tế số"></six-component>
    <six-component header="Xã hội số"></six-component>
    <six-component header="Công nghệ số"></six-component>
  </div>
</template>



<script>
import ComponentHeader from "@/components/mainPage/ComponentHeader.vue";
import VideoMoi from "@/components/mainPage/VideoMoi.vue";
import CauChuyenMoi from "@/components/mainPage/CauChuyenMoi.vue";
import SixComponent from "@/components/mainPage/SixComponent.vue";
export default {
  components: { VideoMoi, CauChuyenMoi, ComponentHeader, SixComponent },
  data() {
    return {
      objectVideoMoi: [
        {
          // source: "~/assets/images/blog/2.png",
          source: "http://localhost:3000/_nuxt/assets/images/blog/2.png",
          name: "Chính quyền số",
          content:
            "Triển khai áp dụng Nền tảng Sổ tay đảng viên tại Thái Nguyên",
        },
        {
          source: "http://localhost:3000/_nuxt/assets/images/blog/3.png",
          name: "Kinh tế số",
          content:
            "Câu chuyện chuyển đổi số cho người nông dân mùa dịch - xã Yên Hòa",
        },
        {
          source: "http://localhost:3000/_nuxt/assets/images/blog/4.png",
          name: "Xã hội số",
          content: "Chuyển đổi số 100% các trường từ mầm non đến PTTH",
        },
        {
          source: "http://localhost:3000/_nuxt/assets/images/blog/5.png",
          name: "Chính quyền số",
          content:
            "Triển khai áp dụng Nền tảng Sổ tay đảng viên tại Thái Nguyên",
        },
        {
          source: "http://localhost:3000/_nuxt/assets/images/blog/6.png",
          name: "Kinh tế số",
          content:
            "Câu chuyện chuyển đổi số cho người nông dân mùa dịch - xã Yên Hòa",
        },
        {
          source: "http://localhost:3000/_nuxt/assets/images/blog/7.png",
          name: "Xã hội số",
          content: "Chuyển đổi số 100% các trường từ mầm non đến PTTH",
        },
      ],
      objectCauChuyenMoi: [
        {
          source: "http://localhost:3000/_nuxt/assets/images/blog/9.png",
          name: "Triển khai áp dụng Nền tảng Sổ tay đảng viên tại Thái Nguyên",
        },
        {
          source: "http://localhost:3000/_nuxt/assets/images/blog/10.png",
          name: "Triển khai áp dụng Nền tảng Sổ tay đảng viên tại Thái Nguyên",
        },
        {
          source: "http://localhost:3000/_nuxt/assets/images/blog/11.png",
          name: "Triển khai áp dụng Nền tảng Sổ tay đảng viên tại Thái Nguyên",
        },
      ],

    };
  },
};
</script>

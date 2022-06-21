<template>
    <section class="max-w-7xl mx-auto py-10 border-b-2 border-gray-400">
        <div class="grid grid-cols-2">
            <h3 class="font-semibold text-2xl border-b-4 border-red-500 w-max">{{ header }}</h3>
            <a class="text-right text-red-500" href="#">Xem thêm <i class="fa-solid fa-right-long"></i></a>
        </div>
            <div v-if="header === 'Chính phủ số'">
                <div class="grid grid-cols-6 gap-3 mt-10">
                <small-component v-for="(item, index) in chinhPhuSo" :key="index" :name="item.name"></small-component>
                </div>
            </div>
            <div v-if="header === 'Kinh tế số'">
                <div class="grid grid-cols-6 gap-3 mt-10">
                <small-component v-for="(item, index) in kinhTeSo" :key="index" :name="item.name"></small-component>
                </div>
            </div>
            <div v-if="header === 'Xã hội số'">
                <div class="grid grid-cols-6 gap-3 mt-10">
                <small-component v-for="(item, index) in xaHoiSo" :key="index" :name="item.name"></small-component>
                </div>
            </div>
            <div v-if="header === 'Công nghệ số'">
                <div class="grid grid-cols-6 gap-3 mt-10">
                <small-component v-for="(item, index) in congNgheSo" :key="index" :name="item.name"></small-component>
                </div>
            </div>
    </section>
</template>

<script>
import SmallComponent from "~/components/mainPage/SmallComponent.vue";
export default {
    components: { SmallComponent },
    props: {
        header: {
            type: String,
            required: true,
        }
    },
    data() {
        return {
            chinhPhuSo: [
            { name:"chinhPhuSo"} ,
            { name:"Hệ thống truyền hình trực tiếp kết nối"},
            { name:"Mô hình chuyển đổi số cấp tỉnh ở Lạng Sơn"},
            { name:"Ứng dụng trợ lý ảo cung cấp thông tin cho lãnh đạo"},
            { name:"Triển khai áp dụng Nền tàng Sổ tay đảng viên"},
            { name:"Giải pháp tổng đài AI để tư vấn, hỗ trợ chăm sóc F0"}
            ],
            kinhTeSo: [
            { name:"kinhTeSo"} ,
            { name:"Hệ thống truyền hình trực tiếp kết nối"},
            { name:"Mô hình chuyển đổi số cấp tỉnh ở Lạng Sơn"},
            { name:"Ứng dụng trợ lý ảo cung cấp thông tin cho lãnh đạo"},
            { name:"Triển khai áp dụng Nền tàng Sổ tay đảng viên"},
            { name:"Giải pháp tổng đài AI để tư vấn, hỗ trợ chăm sóc F0"}
            ],
            xaHoiSo: [
            { name:"xaHoiSo"} ,
            { name:"Hệ thống truyền hình trực tiếp kết nối"},
            { name:"Mô hình chuyển đổi số cấp tỉnh ở Lạng Sơn"},
            { name:"Ứng dụng trợ lý ảo cung cấp thông tin cho lãnh đạo"},
            { name:"Triển khai áp dụng Nền tàng Sổ tay đảng viên"},
            { name:"Giải pháp tổng đài AI để tư vấn, hỗ trợ chăm sóc F0"}
            ],
            congNgheSo: [
            { name:"congNgheSo"} ,
            { name:"Hệ thống truyền hình trực tiếp kết nối"},
            { name:"Mô hình chuyển đổi số cấp tỉnh ở Lạng Sơn"},
            { name:"Ứng dụng trợ lý ảo cung cấp thông tin cho lãnh đạo"},
            { name:"Triển khai áp dụng Nền tàng Sổ tay đảng viên"},
            { name:"Giải pháp tổng đài AI để tư vấn, hỗ trợ chăm sóc F0"}
            ],
        }
    }
}
</script>

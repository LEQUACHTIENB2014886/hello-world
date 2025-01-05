<template>
  <header>
    <div class="navbar bg-light">
      <a><img src="@/assets/logo.png" alt="logo" width="65%"></a>
      <a>
        <h3>CÔNG TY TNHH TỶ XUÂN<br>VINH LONG FOOTWEAR CO.,LTD</h3>
      </a>
      <a class="right">
        <div id="currentDateTime">{{ currentDate }}</div>
      </a>
    </div>
    <div class="d-flex bg-white">
      <div class="p-2 flex-fill"><a href="#" id="link1">Trang chủ</a></div>
      <div class="p-2 flex-fill"><a href="#" id="link1">Giới thiệu</a></div>
      <div class="p-2 flex-fill"><a href="#" id="link1">Trách nhiệm xã hội</a></div>
      <div class="p-2 flex-fill"><a href="#" id="link1">Hoạt động công đoàn</a></div>
      <div class="p-2 flex-fill"><a href="#" id="link1">Tuyển dụng</a></div>
      <div class="p-2 flex-fill"><a href="#" id="link1">Liên hệ</a></div>
    </div>
  </header>

</template>

<script>
export default {
  data() {
    return {
      currentDate: '',
    };
  },
  methods: {
    updateDateTime() {
      const now = new Date();
      const days = ['Chủ nhật', 'Thứ hai', 'Thứ ba', 'Thứ tư', 'Thứ năm', 'Thứ sáu', 'Thứ bảy'];
      const dayOfWeek = days[now.getDay()];
      const date = now.getDate();
      const month = now.getMonth() + 1;
      const year = now.getFullYear();
      this.currentDate = `${dayOfWeek}, ${('0' + date).slice(-2)}/${('0' + month).slice(-2)}/${year}`;
    },
  },
  mounted() {
    this.updateDateTime();
    setInterval(this.updateDateTime, 1000);
  },
};
</script>

<style scoped>
@import '../assets/style.css';
</style>
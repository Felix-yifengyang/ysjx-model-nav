<template>
  <header :class="{ 'scrolled': isScrolled }">
    <div class="logo-wrapper">
      <div class="logo">
        <img src="../assets/ysjx-logo-noword.png" alt="云上江西 logo">
      </div>
      <span class="platform-name">云上江西大模型展示</span>
    </div>
    <nav>
      <ul>
        <li>
          <router-link 
            to="/"
            :active-class="isActive('/') ? 'active' : ''"
          >
            首页
          </router-link>
        </li>
        <li>
          <router-link 
            to="/about"
            :active-class="isActive('/about') ? 'active' : ''"
          >
            关于我们
          </router-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted, computed } from 'vue';
import { useRoute } from 'vue-router';

const isScrolled = ref(false);
const route = useRoute();

const isActive = (path) => {
  return route.path === path;
};

const handleScroll = () => {
  isScrolled.value = window.scrollY > 0;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<style scoped>
header {
  background-color: #ffffff;
  color: rgb(0, 0, 0);
  padding: 15px;
  height: 30px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: sticky; /* 使导航栏固定在页面顶部 */
  top: 0; /* 固定在页面顶部 */
  z-index: 100; /* 确保导航栏显示在其他元素之上 */
  transition: all 0.3s ease;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.logo-wrapper {
  display: flex;
  align-items: center;
}

.logo img {
  width: auto;
  height: 40px;
  margin-right: 5px;
}

.platform-name {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-size: 20px;
  font-weight: bold;
  color: #38a5ff;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
  transition: all 0.3s ease;
  letter-spacing: 2px;
}

nav ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  display: flex;
}

nav ul li {
  margin-left: 30px;
}

nav ul li a {
  color: rgb(0, 0, 0);
  text-decoration: none;
  font-size: 20px;
}

nav ul li a:hover {
  text-decoration: underline;
}

header.scrolled {
  background-color: rgba(228, 228, 228, 0.9); /* 半透明背景 */
  padding: 15px; /* 减少内边距 */
}
header.scrolled .platform-name {
  font-size: 18px; /* 减小字体大小 */
}

/* 高亮显示的样式 */
.active {
  color: #38a5ff;
  font-weight: bold;
}
</style>
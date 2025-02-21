<template>
    <section class="hero">
        <!-- 为背景添加半透明遮罩层 -->
        <div class="hero-overlay"></div>
        <div class="hero-content">
            <div class="hero-logo-content-wrapper">
                <div class="hero-logo">
                    <img src="../assets/ysjx-logo-noword.png" alt="云上江西 logo">
                </div>
                <div class="hero-text-content">
                    <h2 class="hero-title">云上江西大模型展示</h2>
                    <p class="hero-slogan">数据赋能 创新发展</p>
                    <p class="hero-features">数据资源获取 数据资源登记 数据产品使用</p>
                </div>
            </div>
            <div class="department-info">
                <span class="department-label">隶属于</span>
                <span class="department-name">数据要素部门</span>
            </div>
            <!-- 合并 FeatureSelection 部分 -->
            <section class="features">
                <h2>平台特色</h2>
                <div class="feature-container">
                    <div class="feature" v-for="(item, index) in featureList" :key="index">
                        <div class="icon-wrapper">
                            <i :class="item.icon"></i>
                        </div>
                        <div class="text-content">
                            <h3>{{ item.title }}</h3>
                            <p>{{ item.description }}</p>
                        </div>
                    </div>
                </div>
            </section>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';

const featureList = ref([
    {
        icon: 'fas fa-sitemap',
        title: '全面模型覆盖',
        description: '整合内部各类大模型，提供一站式导航，精准满足不同业务场景需求。'
    },
    {
        icon: 'fas fa-bolt',
        title: '快速导航跳转',
        description: '简洁高效的导航设计，实现大模型间的快速切换与访问，节省时间成本。'
    },
    {
        icon: 'fas fa-eye',
        title: '直观模型展示',
        description: '多维度展示大模型信息，包括功能特性、应用案例等，助您深入了解模型。'
    },
    {
        icon: 'fas fa-lock',
        title: '安全访问保障',
        description: '严格的权限管理与安全机制，确保内部大模型数据的安全访问与使用。'
    }
]);
</script>

<style scoped>
.hero {
    background-image: url('../assets/sample.webp');
    background-size: cover;
    background-position: center;
    height: 800px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative; /* 为遮罩层定位做准备 */
    overflow: hidden; /* 防止内容溢出 */
}

/* 半透明遮罩层 */
.hero-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5); /* 半透明黑色背景 */
}

.hero-content {
    text-align: center;
    color: white;
    z-index: 1; /* 确保内容显示在遮罩层之上 */
    padding: 0 20px; /* 添加左右内边距，防止内容紧贴边缘 */
    display: flex;
    flex-direction: row; /* 修改为水平排列 */
    align-items: flex-start; /* 子元素左对齐 */
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    position: relative; /* 为 department-info 定位做参考 */
}

.hero-logo-content-wrapper {
    display: flex;
    align-items: center;
    flex: 1; /* 占据一半空间 */
}

.hero-logo {
    width: 300px; /* 根据实际情况调整 logo 的宽度 */
    height: auto;
    margin-right: 40px;
    animation: fadeIn 1s ease; /* 添加淡入动画 */
}

.hero-logo img {
    width: 100%;
    height: auto;
    filter: drop-shadow(0 0 10px rgba(0, 0, 0, 0.5)); /* 添加投影效果 */
}

.hero-text-content {
    text-align: left;
}

.hero-title {
    font-family: 'Montserrat', sans-serif; /* 使用更美观的字体 */
    font-size: 56px;
    margin-bottom: 20px;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5); /* 添加文字阴影 */
    animation: fadeInDown 1s ease; /* 添加淡入向下动画 */
}

.hero-slogan {
    font-family: 'Open Sans', sans-serif;
    font-size: 24px;
    margin-bottom: 30px;
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
    animation: fadeInUp 1s ease 0.3s; /* 添加淡入向上动画，延迟 0.3 秒 */
    opacity: 0; /* 初始透明度为 0 */
    animation-fill-mode: forwards; /* 动画结束后保持最终状态 */
}

.hero-features {
    font-family: 'Open Sans', sans-serif;
    font-size: 18px;
    margin-bottom: 20px; /* 减少底部边距，为部门信息留出空间 */
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
    animation: fadeInUp 1s ease 0.6s; /* 添加淡入向上动画，延迟 0.6 秒 */
    opacity: 0; /* 初始透明度为 0 */
    animation-fill-mode: forwards; /* 动画结束后保持最终状态 */
}

.department-info {
    display: flex;
    align-items: center;
    font-family: 'Open Sans', sans-serif;
    font-size: 18px;
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
    animation: fadeInUp 1s ease 0.9s; /* 添加淡入向上动画，延迟 0.9 秒 */
    opacity: 0; /* 初始透明度为 0 */
    animation-fill-mode: forwards; /* 动画结束后保持最终状态 */
    position: absolute; /* 绝对定位 */
    right: 250px; /* 距离右侧 20px */
    bottom: -30px; /* 距离底部 20px，可根据需要调整 */
}

.department-label {
    margin-right: 5px;
    color: #ccc; /* 标签颜色稍浅 */
}

.department-name {
    color: #fff;
    font-weight: bold;
}

/* 淡入动画 */
@keyframes fadeIn {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
    }
}

/* 淡入向下动画 */
@keyframes fadeInDown {
    from {
        opacity: 0;
        transform: translateY(-50px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* 淡入向上动画 */
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(50px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.features {
    padding: 60px 20px;
    background-color: rgba(249, 249, 249, 0.8); /* 增加透明度 */
    text-align: center;
    flex: 1; /* 占据一半空间 */
}

.features h2 {
    font-family: 'Poppins', sans-serif;
    font-size: 36px;
    color: #333;
    margin-bottom: 60px;
    text-transform: uppercase;
    letter-spacing: 2px;
    position: relative;
}

.features h2::after {
    content: '';
    position: absolute;
    bottom: -20px;
    left: 50%;
    transform: translateX(-50%);
    width: 80px;
    height: 3px;
    background-color: #007BFF;
}

.feature-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 40px;
    max-width: 1200px;
    margin: 0 auto;
}

.feature {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 250px;
    position: relative;
    transition: all 0.3s ease;
}

.feature::after {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 0;
    width: 0;
    height: 2px;
    background-color: #007BFF;
    transition: width 0.3s ease;
}

.feature:hover::after {
    width: 100%;
}

.icon-wrapper {
    font-size: 48px;
    color: #007BFF;
    margin-bottom: 20px;
}

.text-content {
    text-align: center;
}

.text-content h3 {
    font-family: 'Poppins', sans-serif;
    font-size: 22px;
    color: #333;
    margin-bottom: 10px;
}

.text-content p {
    font-family: 'Open Sans', sans-serif;
    font-size: 16px;
    color: #666;
    line-height: 1.6;
}
</style>
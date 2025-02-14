<template>
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
.features {
    padding: 60px 20px;
    background-color: #f9f9f9;
    text-align: center;
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
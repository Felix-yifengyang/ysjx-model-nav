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
            <!-- 合并进来的 ShowcaseSection 内容 -->
            <div class="showcase-section">
                <h2>大模型导航</h2>
                <div class="showcase-container">
                    <!-- 第一个矩形 -->
                    <a href="http://106.227.19.2:28088/apps" class="showcase-item item-1">
                        <p class="description">大数据编排工具</p>
                    </a>
                    <!-- 第二个矩形 -->
                    <a href="http://106.227.19.14:16105/" class="showcase-item item-2">
                        <p class="description">云西大模型API路由系统</p>
                    </a>
                    <!-- 第三个矩形 -->
                    <a href="http://10.9.55.36:12300/" class="showcase-item item-3">
                        <p class="description">赣企通知识库工具</p>
                    </a>
                    <!-- 第四个矩形 -->
                    <a href="http://106.227.19.14:16104/" class="showcase-item item-4">
                        <p class="description">大模型通用对话聊天</p>
                    </a>
                    <!-- 第五个矩形 -->
                    <a href="http://106.227.19.2:26011/" class="showcase-item item-5">
                        <p class="description">大模型党建辅助系统</p>
                    </a>
                    <!-- 第六个矩形 -->
                    <a href="http://106.227.19.14:9999/datamodel/dist/#/login" class="showcase-item item-6">
                        <p class="description">政务大模型开发底座</p>
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
</script>

<style scoped>
/* 整体背景和基础样式 */
.hero {
    background-image: url('../assets/sample.webp');
    background-size: cover;
    background-position: center;
    height: 100vh; /* 使用视口高度，适应不同屏幕 */
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    overflow: hidden;
}

/* 半透明遮罩层 */
.hero-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to bottom, rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.8)); /* 渐变遮罩 */
}

/* 主要内容区域 */
.hero-content {
    text-align: center;
    color: white;
    z-index: 1;
    padding: 0 20px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 90%; /* 调整宽度 */
    max-width: 1400px; /* 增加最大宽度 */
    margin: 0 auto;
    position: relative;
}

/*  logo 和文本内容包装器 */
.hero-logo-content-wrapper {
    display: flex;
    align-items: center;
    flex-direction: row;
    text-align: left;
}

/*  logo 样式 */
.hero-logo {
    width: 350px; /* 调整 logo 宽度 */
    height: auto;
    margin-right: 50px;
    animation: fadeIn 1s ease, scaleIn 1s ease; /* 增加缩放动画 */
}

.hero-logo img {
    width: 100%;
    height: auto;
    filter: drop-shadow(0 0 15px rgba(255, 255, 255, 0.3)); /* 调整投影效果 */
}

/* 文本内容样式 */
.hero-text-content {
    text-align: left;
}

.hero-title {
    font-family: 'Montserrat', sans-serif;
    font-size: 64px; /* 增大标题字体 */
    margin-bottom: 30px;
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.7); /* 增强文字阴影 */
    animation: fadeInDown 1s ease, slideInLeft 1s ease; /* 增加滑入动画 */
}

.hero-slogan {
    font-family: 'Open Sans', sans-serif;
    font-size: 30px; /* 增大标语字体 */
    margin-bottom: 40px;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
    animation: fadeInUp 1s ease 0.3s, slideInLeft 1s ease 0.3s; /* 增加滑入动画 */
    opacity: 0;
    animation-fill-mode: forwards;
}

.hero-features {
    font-family: 'Open Sans', sans-serif;
    font-size: 22px; /* 增大功能描述字体 */
    margin-bottom: 30px;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
    animation: fadeInUp 1s ease 0.6s, slideInLeft 1s ease 0.6s; /* 增加滑入动画 */
    opacity: 0;
    animation-fill-mode: forwards;
}

/* 部门信息样式 */
.department-info {
    display: flex;
    align-items: center;
    font-family: 'Open Sans', sans-serif;
    font-size: 20px; /* 增大部门信息字体 */
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
    animation: fadeInUp 1s ease 0.9s, slideInRight 1s ease 0.9s; /* 增加滑入动画 */
    opacity: 0;
    animation-fill-mode: forwards;
    position: absolute;
    right: 300px; /* 调整位置 */
    bottom: -40px;
}

.department-label {
    margin-right: 10px;
    color: #ccc;
}

.department-name {
    color: #fff;
    font-weight: bold;
}

/* 展示区域样式 */
.showcase-section {
    width: 50%;
    padding: 30px; /* 增加内边距 */
    background-color: rgba(255, 255, 255, 0.9); /* 增加背景透明度 */
    border-radius: 20px; /* 增大圆角 */
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.3); /* 增强阴影 */
}

.showcase-section h2 {
    font-family: 'Poppins', sans-serif;
    font-size: 42px; /* 增大标题字体 */
    color: #333;
    margin-bottom: 30px;
    text-transform: uppercase;
    letter-spacing: 3px;
    position: relative;
}

.showcase-section h2::after {
    content: '';
    position: absolute;
    bottom: -15px;
    left: 50%;
    transform: translateX(-50%);
    width: 80px; /* 增加下划线宽度 */
    height: 4px; /* 增加下划线高度 */
    background-color: #007BFF;
}

.showcase-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(3, 1fr);
    gap: 20px; /* 增大间距 */
    justify-content: center;
}

.showcase-item {
    background-color: #ffffff;
    border-radius: 20px; /* 增大圆角 */
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15); /* 增强阴影 */
    overflow: hidden;
    transition: all 0.3s ease;
    text-decoration: none;
    color: inherit;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    background-image: linear-gradient(to bottom, #f9f9f9, #ffffff);
    border: 2px solid #e0e0e0; /* 增加边框宽度 */
}

.showcase-item:hover {
    transform: translateY(-10px);
    box-shadow: 0 12px 24px rgba(0, 0, 0, 0.2);
    background-image: linear-gradient(to bottom, #ffffff, #f9f9f9);
    border-color: #a0a0a0;
}

.showcase-item::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.08);
    opacity: 0;
    transition: opacity 0.3s ease;
}

.showcase-item:hover::before {
    opacity: 1;
}

.description {
    padding: 20px; /* 增加内边距 */
    font-size: 20px; /* 增大字体 */
    color: #333333;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    position: relative;
    z-index: 1;
    text-shadow: 1px 1px 1px rgba(0, 0, 0, 0.1);
    text-align: center;
    line-height: 1.5;
}

.item-1 {
    grid-column: 1 / 2;
    grid-row: 1 / 2;
}

.item-2 {
    grid-column: 2 / 3;
    grid-row: 1 / 2;
}

.item-3 {
    grid-column: 1 / 2;
    grid-row: 2 / 3;
}

.item-4 {
    grid-column: 2 / 3;
    grid-row: 2 / 3;
}

.item-5 {
    grid-column: 1 / 2;
    grid-row: 3 / 4;
}

.item-6 {
    grid-column: 2 / 3;
    grid-row: 3 / 4;
}

/* 动画定义 */
@keyframes fadeIn {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
    }
}

@keyframes scaleIn {
    from {
        transform: scale(0.8);
    }
    to {
        transform: scale(1);
    }
}

@keyframes fadeInDown {
    from {
        opacity: 0;
        transform: translateY(-80px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(80px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes slideInLeft {
    from {
        transform: translateX(-100px);
    }
    to {
        transform: translateX(0);
    }
}

@keyframes slideInRight {
    from {
        transform: translateX(100px);
    }
    to {
        transform: translateX(0);
    }
}
</style>
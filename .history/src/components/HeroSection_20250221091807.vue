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
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
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
    justify-content: space-between; /* 子元素两端对齐 */
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    position: relative; /* 为 department-info 定位做参考 */
}

.hero-logo-content-wrapper {
    display: flex;
    align-items: center;
    flex-direction: column; /* 垂直排列 logo 和文本 */
    text-align: left;
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

/* ShowcaseSection 样式 */
.showcase-section {
    width: 50%; /* 占据一半宽度 */
    padding: 20px;
    background-color: rgba(255, 255, 255, 0.8); /* 半透明白色背景 */
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}

.showcase-section h2 {
    font-family: 'Poppins', sans-serif;
    font-size: 36px;
    color: #333;
    margin-bottom: 20px;
    text-transform: uppercase;
    letter-spacing: 2px;
    position: relative;
}

.showcase-section h2::after {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 50%;
    transform: translateX(-50%);
    width: 60px;
    height: 3px;
    background-color: #007BFF;
}

.showcase-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(3, 1fr);
    gap: 15px;
    justify-content: center;
}

.showcase-item {
    background-color: #ffffff;
    border-radius: 15px;
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
    overflow: hidden;
    transition: all 0.3s ease;
    text-decoration: none;
    color: inherit;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    background-image: linear-gradient(to bottom, #f9f9f9, #ffffff); /* 添加渐变背景 */
    border: 1px solid #e0e0e0; /* 添加边框 */
}

.showcase-item:hover {
    transform: translateY(-8px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
    background-image: linear-gradient(to bottom, #ffffff, #f9f9f9); /* 悬停时渐变背景反转 */
    border-color: #a0a0a0; /* 悬停时边框颜色变深 */
}

.showcase-item::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.05);
    opacity: 0;
    transition: opacity 0.3s ease;
}

.showcase-item:hover::before {
    opacity: 1;
}

.description {
    padding: 15px;
    font-size: 18px; /* 增大字体大小 */
    color: #333333; /* 加深文字颜色 */
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    position: relative;
    z-index: 1;
    text-shadow: 1px 1px 1px rgba(0, 0, 0, 0.1); /* 增强文字阴影 */
    text-align: center;
    line-height: 1.4; /* 调整行高 */
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
    grid-column: 1 / 3;
    grid-row: 3 / 4;
}
</style>
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
    flex-direction: column; /* 垂直排列子元素 */
    align-items: flex-start; /* 子元素左对齐 */
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    position: relative; /* 为 department-info 定位做参考 */
}

.hero-logo-content-wrapper {
    display: flex;
    align-items: center;
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
</style>
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
/* 整体背景部分 */
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
    background-color: rgba(0, 0, 0, 0.6); /* 加深遮罩层颜色 */
}

/* 主要内容区域 */
.hero-content {
    text-align: center;
    color: white;
    z-index: 1; /* 确保内容显示在遮罩层之上 */
    padding: 40px; /* 增加内边距 */
    display: flex;
    flex-direction: column; /* 垂直排列子元素 */
    align-items: flex-start; /* 子元素左对齐 */
    width: 100%;
    max-width: 1400px; /* 增大最大宽度 */
    margin: 0 auto;
    position: relative; /* 为 department-info 定位做参考 */
}

/* Logo 和文本内容的包裹器 */
.hero-logo-content-wrapper {
    display: flex;
    align-items: center;
    margin-bottom: 60px; /* 增加底部间距 */
}

/* Logo 区域 */
.hero-logo {
    width: 350px; /* 增大 logo 宽度 */
    height: auto;
    margin-right: 60px; /* 增加右边距 */
    animation: fadeIn 1.2s ease; /* 延长淡入动画时间 */
}

.hero-logo img {
    width: 100%;
    height: auto;
    filter: drop-shadow(0 0 15px rgba(0, 0, 0, 0.7)); /* 增强投影效果 */
}

/* 文本内容区域 */
.hero-text-content {
    text-align: left;
}

/* 标题样式 */
.hero-title {
    font-family: 'Montserrat', sans-serif; /* 使用更美观的字体 */
    font-size: 64px; /* 增大字体大小 */
    margin-bottom: 30px;
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.7); /* 增强文字阴影 */
    animation: fadeInDown 1.2s ease; /* 延长淡入向下动画时间 */
}

/* 标语样式 */
.hero-slogan {
    font-family: 'Open Sans', sans-serif;
    font-size: 30px; /* 增大字体大小 */
    margin-bottom: 40px;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7); /* 增强文字阴影 */
    animation: fadeInUp 1.2s ease 0.4s; /* 延长动画时间，调整延迟 */
    opacity: 0; /* 初始透明度为 0 */
    animation-fill-mode: forwards; /* 动画结束后保持最终状态 */
}

/* 特色功能样式 */
.hero-features {
    font-family: 'Open Sans', sans-serif;
    font-size: 22px; /* 增大字体大小 */
    margin-bottom: 30px; /* 增加底部边距 */
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7); /* 增强文字阴影 */
    animation: fadeInUp 1.2s ease 0.8s; /* 延长动画时间，调整延迟 */
    opacity: 0; /* 初始透明度为 0 */
    animation-fill-mode: forwards; /* 动画结束后保持最终状态 */
}

/* 部门信息样式 */
.department-info {
    display: flex;
    align-items: center;
    font-family: 'Open Sans', sans-serif;
    font-size: 20px; /* 增大字体大小 */
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7); /* 增强文字阴影 */
    animation: fadeInUp 1.2s ease 1.2s; /* 延长动画时间，调整延迟 */
    opacity: 0; /* 初始透明度为 0 */
    animation-fill-mode: forwards; /* 动画结束后保持最终状态 */
    position: absolute; /* 绝对定位 */
    right: 300px; /* 调整右侧距离 */
    bottom: -40px; /* 调整底部距离 */
}

.department-label {
    margin-right: 10px; /* 增加右边距 */
    color: #ddd; /* 调整标签颜色 */
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
        transform: translateY(-80px); /* 增大初始偏移量 */
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
        transform: translateY(80px); /* 增大初始偏移量 */
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}
</style>
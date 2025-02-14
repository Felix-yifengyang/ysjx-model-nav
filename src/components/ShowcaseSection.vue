<template>
    <section class="showcase">
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
    </section>
</template>

<script setup>
</script>

<style scoped>
.showcase {
    padding: 60px 20px;
    background-color: #f9f9f9;
    text-align: center;
}

.showcase h2 {
    font-family: 'Poppins', sans-serif;
    font-size: 36px;
    color: #333;
    margin-bottom: 60px;
    text-transform: uppercase;
    letter-spacing: 2px;
    position: relative;
}

.showcase h2::after {
    content: '';
    position: absolute;
    bottom: -20px;
    left: 50%;
    transform: translateX(-50%);
    width: 80px;
    height: 3px;
    background-color: #007BFF;
}

.showcase-container {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: repeat(2, 1fr);
    gap: 25px;
    justify-content: center;
    max-width: 1200px;
    margin: 0 auto;
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
    padding: 25px;
    font-size: 20px; /* 增大字体大小 */
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
    grid-column: 2 / 4;
    grid-row: 1 / 2;
}

.item-3 {
    grid-column: 1 / 3;
    grid-row: 2 / 3;
}

.item-4 {
    grid-column: 3 / 4;
    grid-row: 2 / 3;
}

.item-5 {
    grid-column: 4 / 5;
    grid-row: 1 / 3;
}
</style>
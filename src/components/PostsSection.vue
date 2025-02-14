<template>
    <section class="platform-data">
      <h2>平台数据展示</h2>
      <div class="data-item">
        <span class="data-number">
          100
          <small class="unit">家</small>
        </span>
        <p class="data-description">对接单位</p>
      </div>
      <div class="data-item">
        <span class="data-number">
          1,000
          <small class="unit">个</small>
        </span>
        <p class="data-description">对接系统</p>
      </div>
      <div class="data-item">
        <span class="data-number">
          10,000
          <small class="unit">条</small>
        </span>
        <p class="data-description">数据目录</p>
      </div>
    </section>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .platform-data {
    padding: 40px;
    text-align: center;
    background-color: #f9f9f9;
  }
  
  .platform-data h2 {
    font-size: 32px;
    color: #333;
    margin-bottom: 40px;
  }
  
  .data-item {
    display: inline-block;
    width: 20%;
    margin: 10px;
    padding: 20px;
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
  }
  
  .data-item:hover {
    transform: translateY(-5px);
  }
  
  .data-number {
    font-size: 48px;
    font-weight: bold;
    color: #007BFF;
    display: inline-block; /* 使数字和单位在一行显示 */
    margin-bottom: 10px;
    position: relative;
  }
  
  .unit {
    font-size: 24px;
    color: #666;
    position: relative; /* 相对定位 */
    bottom: 0; /* 底部对齐 */
    left: -0.2em; /* 向左偏移一点，使其靠在数字身上 */
    vertical-align: baseline; /* 垂直对齐方式 */
  }
  
  .data-description {
    font-size: 18px;
    color: #666;
  }
  </style>
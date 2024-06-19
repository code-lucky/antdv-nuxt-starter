<script setup lang="ts">
const activeKey1 = ref(["1"]);
</script>

<template>
  <div id="main" class="layui-main">
    <div class="breadcrumb">
      <a-breadcrumb>
        <a-breadcrumb-item><a href="/">首页</a></a-breadcrumb-item>
        <a-breadcrumb-item><a href="/study">全部课程</a></a-breadcrumb-item>
        <a-breadcrumb-item>测试数据</a-breadcrumb-item>
      </a-breadcrumb>
    </div>
    <div class="course-meta wrap">
      <div class="cover">
        <img
          src="https://course-1255691183.file.myqcloud.com/img/cover/612a249fa1301.jpeg!cover_270"
          alt=""
        />
      </div>
      <div class="info">
        <p class="name">Java可重入锁原理与源码分析</p>
        <p class="item desc">
          详细介绍了可重入锁的原理以及源码中每个字段每个方法的具体的意义，让你快速掌握可重入锁的原理
        </p>
        <p class="item author">
          <span class="key">作者</span>
          <span class="value">菜鸡网</span>
        </p>
        <p class="item">64人学习 · 5讲 · 2小时28分钟25秒</p>
      </div>
    </div>
    <div class="course-meta wrap buy-tool">
      <div style="display: flex; align-items: center">
        <h2 class="price-icon">￥</h2>
        <span class="price">30.00</span>
        <span class="line">|</span>
        <span>购买后暂不支持退款</span>
      </div>
      <div>
        <a-button type="primary" danger size="large">立即购买</a-button>
      </div>
    </div>
    <div class="layout-main">
      <div class="layout-content">
        <div class="course-tab-wrap wrap">
          <a-tabs v-model:activeKey="activeKey">
            <a-tab-pane key="1" tab="课程目录" force-render>
              <a-collapse v-model:activeKey1="activeKey1">
                <a-collapse-panel key="1" header="Java可重入锁原理与源码分析">
                  <ul class="videobox">
                    <li>
                      <p>第1节：Java AQS 重入锁独占模式属性分析</p>
                      <p>时长 14分钟44秒</p>
                    </li>
                  </ul>
                </a-collapse-panel>
              </a-collapse>
            </a-tab-pane>
            <a-tab-pane key="2" tab="课程评价"
              >Content of Tab Pane 3</a-tab-pane
            >
          </a-tabs>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
ul li {
  list-style: none;
}
#main {
  margin-top: 20px;
  margin-bottom: 30px;
  min-height: 760px;
}
.layui-main {
  position: relative;
  width: 1160px;
  margin: 0 auto;
}
.breadcrumb {
  position: relative;
  margin-bottom: 20px;
}
.course-meta {
  display: flex;
}
.wrap {
  padding: 20px;
  margin-bottom: 20px;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
}
.course-meta .cover {
  position: relative;
  width: 270px;
  height: 150px;
  margin-right: 10px;
}
.course-meta .cover img {
  width: 100%;
  height: 100%;
}
img {
  display: inline-block;
  border: none;
  vertical-align: middle;
  overflow-clip-margin: content-box;
  overflow: clip;
}
.course-meta .info {
  /* width: 580px; */
  padding-top: 5px;
}
.course-meta .info .name {
  font-weight: 600;
  font-size: 24px;
  color: #21293c;
}
.course-meta .info .desc {
  color: #4b587c;
}
.course-meta .info .item {
  margin-top: 23px;
  font-size: 13px;
}
.course-meta .info .key {
  margin-right: 5px;
}
.course-meta .info .value {
  margin-right: 5px;
  color: #666;
}
.buy-tool {
  border-radius: 6px;
  height: 80px;
  display: flex;
  align-items: center;
  padding: 0 20px;
  justify-content: space-between;
}
.buy-tool span {
  font-size: 13px;
  color: #8899a6;
}
.buy-tool .price-icon {
  margin-top: 19px;
  color: #f4212e;
  font-weight: 500;
  font-size: 24px;
}
.buy-tool .price {
  font-weight: 600;
  font-size: 36px;
  color: #f4212e;
}
.buy-tool .line {
  margin: 0 10px;
}
.layout-main {
  display: flex;
  justify-content: space-between;
}
.layout-content {
  width: 800px;
}
:deep(.ant-collapse) {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  color: rgba(0, 0, 0, 0.88);
  font-size: 14px;
  line-height: 1.5714285714285714;
  list-style: none;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple Color Emoji",
    "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";
  background-color: rgba(0, 0, 0, 0.02);
  border: none;
  border-bottom: none;
  border-radius: 8px;
}
:deep(.ant-collapse .ant-collapse-content) {
  color: rgba(0, 0, 0, 0.88);
  background-color: #ffffff;
  border-top: none;
}
:deep(.ant-collapse > .ant-collapse-item:last-child > .ant-collapse-header) {
  border-radius: 0 0 8px 8px;
  background: white;
}
:deep(.ant-collapse > .ant-collapse-item) {
  border-bottom: none;
}
.videobox li {
  width: 100%;
  height: 100%;
  background: red;
}
</style>

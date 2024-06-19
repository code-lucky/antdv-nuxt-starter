<script setup lang="ts">
import { LeftCircleOutlined, RightCircleOutlined } from "@ant-design/icons-vue";
useHead({
  title: "首页",
  meta: [
    { name: "description", content: "首页" },
    { name: "keywords", content: "首页" },
  ],
});
interface DataItem {
  title: string;
}
const IndexListData: DataItem[] = [
  {
    title: "Title 1",
  },
  {
    title: "Title 2",
  },
  {
    title: "Title 3",
  },
  {
    title: "Title 4",
  },
  {
    title: "Title 5",
  },
  {
    title: "Title 6",
  },
  {
    title: "Title 6",
  },
  {
    title: "Title 6",
  },
];
</script>

<template>
  <div class="index-carousel wrap">
    <!-- 轮播图开始 -->
    <div class="banner_box">
      <div class="banner">
        <a-carousel arrows>
          <template #prevArrow>
            <div class="custom-slick-arrow" style="left: 10px; z-index: 1">
              <LeftCircleOutlined />
            </div>
          </template>
          <template #nextArrow>
            <div class="custom-slick-arrow" style="right: 10px">
              <RightCircleOutlined />
            </div>
          </template>
          <div>
            <img
              src="https://course-1255691183.file.myqcloud.com/img/cover/20210305165849582986.jpg!slide_1100"
              width="100%"
              height="100%"
              alt
            />
          </div>
        </a-carousel>
      </div>
    </div>
    <!-- 轮播图结束 -->
  </div>
  <!-- 内容部分开始 -->
  <div class="index-wrap wrap">
    <div class="header">推荐课程</div>
    <div class="content">
      <a-tabs v-model:activeKey="activeKey">
        <a-tab-pane key="1" tab="前端开发">
          <a-list
            :grid="{ gutter: 16, xs: 1, sm: 2, md: 4, lg: 4, xl: 4, xxl: 3 }"
            :data-source="IndexListData"
          >
            <template #renderItem="{ item }">
              <a-list-item>
                <div class="index-course-content">
                  <div class="cover">
                    <img
                      src="https://course-1255691183.file.myqcloud.com/img/cover/202001242303535808.jpg!cover_270"
                      alt=""
                      style="width: 100%; height: 100%"
                    />
                  </div>
                  <div class="info">
                    <div class="title layui-elip">
                      <a href="">Vue核心技术Vue+Vue-Router+Vuex+SSR实战精讲</a>
                    </div>
                    <div class="meta">
                      <span class="price">￥366.00</span>
                      <span class="lesson">60 节课</span>
                      <span class="user">591 人购买</span>
                    </div>
                  </div>
                </div>
              </a-list-item>
            </template>
          </a-list>
        </a-tab-pane>
        <a-tab-pane key="2" tab="后端开发" force-render
          >Content of Tab Pane 2</a-tab-pane
        >
        <a-tab-pane key="3" tab="系统运维">Content of Tab Pane 3</a-tab-pane>
      </a-tabs>
    </div>
  </div>
  <!-- 内容部分结束 -->
  <!-- 内容部分开始 -->
  <div class="index-wrap wrap">
    <div class="header">推荐课程</div>
    <div class="content">
      <a-tabs v-model:activeKey="activeKey">
        <a-tab-pane key="1" tab="前端开发">
          <a-list
            :grid="{ gutter: 16, xs: 1, sm: 2, md: 4, lg: 4, xl: 4, xxl: 3 }"
            :data-source="IndexListData"
          >
            <template #renderItem="{ item }">
              <a-list-item>
                <div class="index-course-content">
                  <div class="cover">
                    <img
                      src="https://course-1255691183.file.myqcloud.com/img/cover/202001242303535808.jpg!cover_270"
                      alt=""
                      style="width: 100%; height: 100%"
                    />
                  </div>
                  <div class="info">
                    <div class="title layui-elip">
                      <a href="">Vue核心技术Vue+Vue-Router+Vuex+SSR实战精讲</a>
                    </div>
                    <div class="meta">
                      <span class="price">￥366.00</span>
                      <span class="lesson">60 节课</span>
                      <span class="user">591 人购买</span>
                    </div>
                  </div>
                </div>
              </a-list-item>
            </template>
          </a-list>
        </a-tab-pane>
        <a-tab-pane key="2" tab="后端开发" force-render
          >Content of Tab Pane 2</a-tab-pane
        >
        <a-tab-pane key="3" tab="系统运维">Content of Tab Pane 3</a-tab-pane>
      </a-tabs>
    </div>
  </div>
  <!-- 内容部分结束 -->
</template>

<style scoped>
a {
  text-decoration: none;
  color: black;
}
.index-carousel {
  width: 1160px;
  height: 376px;
  text-align: center;
  margin: 20px auto;
  display: flex;
  justify-content: center;
  align-items: center;
}
.index-wrap {
  width: 1160px;
  /* height: 641px; */
  padding-bottom: 15px;
  margin: 20px auto;
}
.index-wrap .header {
  text-align: center;
  font-size: 18px;
  padding-bottom: 15px;
  border-bottom: 1px solid #f6f6f6;
}
.wrap {
  padding: 20px;
  margin-bottom: 20px;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
}
.banner {
  width: 1120px;
  height: 336px;
  /* margin: 5px auto; */
  /* border-radius: 10px; */
}
.banner img {
  width: 100%;
  height: 100%;
  /* border-radius: 10px; */
}
.slide {
  width: 1300px;
  /* height: 460px; */
  margin: 10px auto;
  /* background: red; */
  display: flex;
  align-items: center;
  justify-content: space-around;
}
.common-msg-content {
  width: 764px;
  height: 350px;
  background: white;
  padding: 20px;
  /* border-radius: 10px; */
  display: flex;
  box-shadow: 0 1px 3px 0 rgba(28, 28, 40, 0.1);
}
.org-enter-card {
  width: 438px;
  height: 350px;
  background: blue;
}
.common-msg-itemc {
  width: 396px;
  flex: 0 0 406px;
}
.common-msg-itemr {
  width: 318px;
  height: 310px;
  margin-left: 10px;
}
.org-card-content {
  flex: 1;
}
.common-msg-itemc img {
  width: 394px;
  height: 222px;
}
.org-card-content {
  min-height: 68px;
  margin-left: 10px;
}
.org-card-title {
  color: black;
  overflow: hidden;
  font-size: 16px;
  line-height: 25px;
  margin-top: 10px;
  min-height: 48px;
  margin-bottom: 4px;
}
.org-card-author {
  overflow: hidden;
  line-height: 16px;
  font-size: 13px;
  font-weight: 400;
  display: flex;
  color: #8f90a6;
  justify-content: space-between;
}
.ivu-line-clamp {
  overflow: hidden;
}
/* 轮播图样式 */
:deep(.slick-slide) {
  text-align: center;
  /* height: 100%; */
  /* line-height: ; */
  overflow: hidden;
  /* border-radius: 10px; */
}

:deep(.slick-arrow.custom-slick-arrow) {
  width: 25px;
  height: 25px;
  font-size: 25px;
  color: #fff;
  background-color: rgba(31, 45, 61, 0.11);
  transition: ease all 0.3s;
  opacity: 0.3;
  z-index: 1;
}
:deep(.slick-arrow.custom-slick-arrow:before) {
  display: none;
}
:deep(.slick-arrow.custom-slick-arrow:hover) {
  color: #fff;
  opacity: 0.5;
}

:deep(.slick-slide h3) {
  color: #fff;
}

/* 对ant tab切换样式更改 */
:deep(.ant-tabs-top > .ant-tabs-nav::before) {
  position: absolute;
  right: 0;
  left: 0;
  border-bottom: none;
  content: "";
}

:deep(.ant-list .ant-list-item) {
  padding: 0;
  color: rgba(0, 0, 0, 0.88);
}
.index-course-content {
  width: 265px;
  /* height: 250px; */
  /* background: red; */
  box-shadow: none;
  border: 1px solid #eee;
  border-radius: 2px;
}
.index-course-content .info {
  padding-bottom: 18px;
  padding: 10px;
}
.index-course-content .info .title {
  margin-bottom: 10px;
}
.index-course-content .info .layui-elip {
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
}
.index-course-content .info .layui-elip {
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
}
.index-course-content .meta {
  color: #666;
  font-size: 12px;
}
.index-course-content span {
  margin-right: 10px;
}
.index-course-content .meta .price {
  color: red;
}
.index-course-content .meta .lesson {
  color: #666;
  font-size: 12px;
}
.index-course-content .meta .user {
}
.index-course-content .cover {
  overflow: hidden;
}
.index-course-content .cover img {
  width: 275px;
  height: 155px;
  transition: all 0.6s;
}
.index-course-content .cover img:hover {
  transform: scale(1.2);
  transition: all 0.6s;
}
</style>

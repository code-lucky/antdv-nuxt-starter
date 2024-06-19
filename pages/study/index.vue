<script setup lang="ts">
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
  <div id="main" class="layui-main">
    <div class="filter-wrap wrap">
      <div class="filter-group">
        <div class="title">方向</div>
        <div class="content">
          <a href="/">全部</a>
          <a href="/">前端开发</a>
          <a href="/">后端开发</a>
        </div>
      </div>
      <div class="filter-group">
        <div class="title">类型</div>
        <div class="content">
          <a href="/">全部</a>
          <a href="/">图文</a>
          <a href="/">视频</a>
        </div>
      </div>
      <div class="filter-group">
        <div class="title">难度</div>
        <div class="content">
          <a href="/">全部</a>
          <a href="/">初级</a>
          <a href="/">中级</a>
          <a href="/">高级</a>
          <a href="/">资深</a>
        </div>
      </div>
    </div>
    <!-- 内容部分开始 -->
    <div class="index-wrap wrap">
      <div class="content">
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
      </div>
    </div>
    <!-- 内容部分结束 -->
  </div>
</template>

<style scoped>
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
.filter-wrap {
  margin-bottom: 20px;
}
.wrap {
  padding: 20px;
  margin-bottom: 20px;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
}
.filter-group {
  display: flex;
  height: 40px;
  line-height: 40px;
  padding-bottom: 5px;
}

.filter-group .title {
  width: 50px;
  font-weight: 700;
  font-size: 14px;
}
.filter-group .content a {
  margin-right: 15px;
  font-size: 14px;
  text-decoration: none;
  color: black;
}
.index-wrap {
  width: 1160px;
  /* height: 641px; */
  padding-bottom: 15px;
  margin: 20px auto;
}
.wrap {
  padding: 20px;
  margin-bottom: 20px;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
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

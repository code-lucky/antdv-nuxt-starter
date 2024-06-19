<script setup lang="ts">
const navData = [
  {
    id: 1,
    link: "/",
    name: "首页",
  },
  {
    id: 2,
    link: "/study",
    name: "课程",
  },
  {
    id: 3,
    link: "/video",
    name: "专栏",
  },
  {
    id: 4,
    link: "/itexam",
    name: "问答",
  },
  {
    id: 5,
    link: "/about",
    name: "关于我们",
  },
];
</script>

<template>
  <!-- 头部开始 -->
  <a-affix :offset-top="top">
    <div class="nav">
      <div class="nav_one">
        <div style="display: flex; align-items: center">
          IT菜鸡论坛
          <div class="nav_list">
            <ul>
              <li v-for="(item, index) in navData" :key="index">
                <a :href="item.link">{{ item.name }}</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="login">
          <div class="login_box">
            <a href="/login">
              <img
                src="@/public/img/login.png"
                alt
                width="20px"
                height="20px"
              />
              登录
            </a>
          </div>
          <div>
            <img src="@/public/img/regis.png" alt width="20px" height="20px" />
            注册
          </div>
        </div>
      </div>
    </div>
  </a-affix>
  <!-- 头部结束 -->
  <slot />
  <!-- 底部开始 -->
  <div id="footer">
    <div class="layui-main">
      <div class="row footernav">
        <a href="/">测试数据</a>
        <a href="/">测试数据</a>
        <a href="/">测试数据</a>
        <a href="/">测试数据</a>
        <a href="/">测试数据</a>
      </div>
      <div class="row cop">
        <span>© 北京菜鸡网络科技有限公司</span>
      </div>
    </div>
  </div>
  <!-- 底部结束 -->
</template>

<style scoped>
a {
  text-decoration: none;
  color: black;
}
.nav {
  width: 100%;
  height: 60px;
  background: white;
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
  display: flex;
  align-items: center;
  justify-content: center;
}
.nav_list ul li {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100px;
  height: 50px;
  text-align: center;
  list-style: none;
  float: left;
  margin-left: 20px;
}
.nav_one {
  width: 1200px;
  height: 66px;
  /* background: red; */
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.login {
  display: flex;
}
.login_box {
  width: 100px;
  height: 100%;
}
#footer {
  width: 100%;
  padding: 30px 0;
  background: #474443;
  text-align: center;
  font-size: 12px;
}
#footer .footernav a {
  margin-right: 10px;
}
#footer .cop {
  color: #999;
}
#footer a {
  color: #999;
}
.layui-main {
  position: relative;
  width: 1160px;
  margin: 0 auto;
}
#footer .row {
  line-height: 18px;
  margin-bottom: 15px;
}
</style>

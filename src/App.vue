<script setup>
// 定义比赛数据
const matches = [
  { id: 1, name: "英雄联盟高校联赛", time: "2026-03-15 19:00", team: "川师 VS 电子科大" },
  { id: 2, name: "程序设计竞赛", time: "2026-03-20 09:00", team: "个人赛" },
  { id: 3, name: "校园足球赛", time: "2026-03-25 14:00", team: "计算机学院 VS 文学院" }
];
</script>

<template>
  <div class="container">
    <!-- 导航栏 -->
    <nav class="navbar">
      <div class="logo">我的比赛网站</div>
      <ul class="nav-links">
        <li><a href=" ">首页</a ></li>
        <li><a href="#">我的比赛</a ></li>
        <li><a href="#">历史记录</a ></li>
        <li><a href="#">关于</a ></li>
      </ul>
    </nav>

    <!-- 页面标题 -->
    <h1>🏆 热门比赛</h1>
    <p>这是我用 Vue 做的第一个完整页面！</p >

    <!-- 比赛列表 -->
    <div class="match-list">
      <div v-for="match in matches" :key="match.id" class="match-card">
        <h3>{{ match.name }}</h3>
        <p>⏰ 时间：{{ match.time }}</p >
        <p>👥 对阵：{{ match.team }}</p >
        <button class="btn">查看详情</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container {
  font-family: Arial, sans-serif;
  min-height: 100vh;
  background-color: #f5f7fa;
}

/* 导航栏样式 */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #42b883;
  padding: 1rem 5%;
  color: white;
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 2rem;
}

.nav-links a {
  color: white;
  text-decoration: none;
  font-size: 1.1rem;
}

.nav-links a:hover {
  text-decoration: underline;
}

/* 标题样式 */
h1 {
  color: #42b883;
  font-size: 3em;
  text-align: center;
  margin: 2rem 0;
}

p {
  font-size: 1.5em;
  color: #333;
  text-align: center;
  margin-bottom: 2rem;
}

/* 比赛列表样式 */
.match-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  padding: 0 5%;
}

.match-card {
  background: white;
  padding: 1.5rem;
  border-radius: 10px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  text-align: left;
}

.match-card h3 {
  color: #42b883;
  margin-bottom: 1rem;
}

.match-card p {
  font-size: 1rem;
  color: #666;
  margin: 0.5rem 0;
  text-align: left;
}

.btn {
  margin-top: 1rem;
  padding: 0.7rem 1.5rem;
  background-color: #42b883;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 1rem;
}

.btn:hover {
  background-color: #359469;
}
</style>
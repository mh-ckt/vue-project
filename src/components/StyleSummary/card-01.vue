<script></script>

<template>
  <div class="floor-box">
    <section class="floor1-container">
      <p class="floor-desc">1. 水平居中块级元素</p>
      <div class="box"></div>
    </section>
    <section class="floor2-container">
      <p class="floor-desc">2. 弹性布局中灵活分配剩余空间</p>
      <div class="box">
        <h4>我展示在上方</h4>
        <p>我展示在下方</p>
        <p>我也展示在下方</p>
      </div>
    </section>
  </div>
</template>

<style scoped lang="less">
h4 {
  margin: 0;
}

.floor-box {
  display: flex;
  gap: 20px;
}

.floor-desc {
  font-size: 10px;
  text-align: center;
}

// floor1
.floor1-container {
  width: 200px;
  height: 100px;
  background-color: #ececec;
  .box {
    width: 50px;
    height: 50px;
    background-color: #979797;
    margin: auto;
  }
}

// floor2
.floor2-container {
  width: 200px;
  height: 100px;
  background-color: #ececec;
  display: flex;
  flex-direction: column;
  // 让box中的两个p标签展示在box的底部
  .box {
    background-color: #979797;
    flex: 1;
    display: flex;
    flex-direction: column;
    p:first-of-type {
      margin-top: auto;
    }
  }
}
</style>

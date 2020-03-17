/* eslint-disable prettier/prettier */
<script>
export default {
  data() {
    return {
      linkList: [
        { label: "Github", url: "github.com/impeiran" },
        { label: "Blog", url: "github.com/impeiran/Blog" },
        {
          label: "掘金",
          url: "juejin.im/user/5b6b21cb5188251af53e0a91"
        }
      ]
    };
  }
};
</script>

<template>
  <section class="page-home">
    <main>
      <div class="block avatar-box">
        <img :src="require('../../assets//avatar.jpg')" />
      </div>

      <div class="block description">写前端的，是个工具党，爱折腾也爱造轮子。</div>

      <div class="block link-group">
        <div v-for="item in linkList" :key="item.url">
          <label>{{ item.label }}:</label>
          <a :href="'https://' + item.url" target="_blank">{{ item.url }}</a>
        </div>
      </div>
    </main>
  </section>
</template>

<style lang="scss" scoped>
.page-home {
  position: relative;
  min-height: calc(100vh - 40px);
  font-size: 14px;
  line-height: 1.2;

  .block {
    margin: 0 auto 10px;
  }

  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    position: absolute;
    top: 35%;
    left: 50%;
    transform: translate(-50%, -50%);
    min-width: 340px;
    min-height: 200px;
    animation: up-fade 0.5s linear;
  }

  .avatar-box {
    position: relative;
    margin: 0 auto 10px;
    width: 80px;
    height: 80px;
    overflow: hidden;
    box-shadow: 4px 4px 8px rgba(0, 0, 0, 0.1);

    img {
      position: absolute;
      width: 100%;
      height: 100%;
    }
  }

  .description {
    text-align: center;
  }

  .link-group {
    margin-top: 10px;

    & > div {
      line-height: 18px;
    }

    label {
      display: inline-block;
      width: 4em;
    }
  }

  a {
    color: #333;

    &:active,
    &:hover {
      color: #333;
    }
  }
}

@keyframes up-fade {
  from {
    top: 40%;
    opacity: 0;
  }

  to {
    top: 35%;
    opacity: 1;
  }
}
</style>

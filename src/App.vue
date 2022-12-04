<template>
  <div id="app" class="home">
    <div class="left">
      <img
        src="../src/assets/img/logo.png"
        alt=""
        width="62px"
        height="62px"
        class="logo"
      />
      <div v-for="(item, index) in iconList" :key="index">
        <img
          :src=item.icon
          alt=""
          width="42px"
          height="42px"
          class="icon_nav"
        />
      </div>
    </div>
    <div class="right">
      <div class="top_banner">
        <img src="../src/assets/img/TOP.png" alt="" class="top_search" />
        <img src="../src/assets/img/banner1.png" alt="" style="width: 100%" />
        <div class="top_btn">
          <img
            src="../src/assets/img/learnMore.png"
            alt=""
            style="width: 100%; height: 100%"
          />
        </div>
      </div>
      <div class="game">
        <img src="../src/assets/img/Game.png" alt="" class="game_title" />
        <div class="game_pic">
          <img
            v-for="(item, index) in gamePic"
            :key="index"
            :src="item.pic"
            alt=""
            class="game_img"
          />
        </div>
      </div>
      <div class="NFT">
        <img src="../src/assets/img/NFT.png" alt="" class="NFT_title" />
        <div class="NFT_pic">
          <img src="../src/assets/img/NFTPic1.png" alt="" class="NFT_img" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      iconList: [
        {
          icon: require("./assets/img/noClick1.png"),
        },
        {
          icon: require("../src/assets/img/noClick2.png"),
        },
        {
          icon: require("../src/assets/img/noClick3.png"),
        },
        {
          icon: require("../src/assets/img/noClick4.png"),
        },
        {
          icon: require("../src/assets/img/noClick5.png"),
        },
      ],
      gamePic: [
        {
          pic: require("../src/assets/img/bigPic1.png"),
        },
        {
          pic: require("../src/assets/img/smallPic2.png"),
        },
        {
          pic: require("../src/assets/img/smallPic3.png"),
        },
      ],
    };
  },
};
</script>

<style>
.home {
  width: 100%;
  background: #131313;
  min-height: 100%;
  display: flex;
  flex-direction: row;
}
.left {
  width: 92px;
  background: #000;
  min-height: 100%;
}
.right {
  width: calc(100% - 92px);
  color: #fff;
  font-size: 18px;
  font-family: "Lexend Exa";
}
.logo {
  width: 62px;
  height: 62px;
  margin: 32px 15px 52px 15px;
}
.icon_nav {
  width: 42px;
  height: 42px;
  margin: 0 25px 38px 25px;
}
.changColor {
  color: #fff;
  background: #fff;
}
.top_banner {
  width: 100%;
  height: 600px;
}
.top_search {
  width: 90%;
  position: fixed;
  top: 38px;
  /* left: 164px; */
}
.top_btn {
  box-sizing: border-box;
  position: absolute;
  width: 200px;
  height: 62px;
  left: 144px;
  top: 506px;
}
.game {
  margin: 0 46px;
}
.game_title {
  position: absolute;
  width: 118px;
  height: 45px;
  left: 144px;
  top: 698px;
}
.game_pic {
  /* width: 350px; */
  height: 520px;
  display: flex;
  flex-direction: row;
  position: relative;
  top: 170px;
  justify-content: center;
}
.game_img:not(:first-child) {
  width: 100%;
  margin-left: 28px;
}
.NFT {
  margin-top: 62px;
}
.NFT_title {
  margin-bottom: 33px;
}
</style>

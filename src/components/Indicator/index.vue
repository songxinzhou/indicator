<template>
  <div id="Indicator">
    <div class="ring">
      <div class="ring-out">
        <!--老有厚德-->
        <div class="ring-ball lyhd">
          <h4>老有厚德<span>（二级）</span></h4>
          <h3>99分<span>20%</span></h3>
        </div>
        <!--学有优教-->
        <div class="ring-ball xyyj">
          <h4>学有优教<span>（二级）</span></h4>
          <h3>99分<span>20%</span></h3>
        </div>
        <!--病友良医-->
        <div class="ring-ball byly">
          <h4>病友良医<span>（二级）</span></h4>
          <h3>99分<span>20%</span></h3>
        </div>
        <!--弱有众扶-->
        <div class="ring-ball ryzf">
          <h4>弱有众扶<span>（二级）</span></h4>
          <h3>99分<span>20%</span></h3>
        </div>
      </div>
      <div class="ring-inner">
        <!--住有宜居-->
        <div class="ring-ball zyyj">
          <h4>住有宜居<span>（二级）</span></h4>
          <h3>99分<span>20%</span></h3>
        </div>
        <!--优有善育-->
        <div class="ring-ball yysy">
          <h4>优有善育<span>（二级）</span></h4>
          <h3>99分<span>20%</span></h3>
        </div>
        <!--老有颐养-->
        <div class="ring-ball lyyy">
          <h4>老有颐养<span>（二级）</span></h4>
          <h3>99分<span>20%</span></h3>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import indicatorConf from "./index.json";
export default {
  name: "Indicator",
  data() {
    return {
      outerlist:[],
      innerlist:[],
    };
  },
  mounted() {
    // this.turnRing();
    this.indicatolist();
  },
  methods: {
    indicatolist(){
      this.outerlist=indicatorConf.list.slice(0,4);
      this.innerlist=indicatorConf.list.slice(4,7);
      console.log(this.outerlist);
      console.log(this.innerlist);
    },
    turnRing() {
      var i = 5;
      setInterval(() => {
        if (i < 360) {
          this._$(".ring-out").css("transform", "rotate(" + i + "deg)");
          this._$(".ring-inner").css("transform", "rotate(" + i + "deg)");
          i = i + 5;
        } else {
          i = 5;
        }
      }, 500);
    },
  },
};
</script>
<style lang="scss">
#Indicator {
  width: 1920px;
  height: 1080px;
  background-image: url(../../assets/image/Indicator/indicatorbg.png);
  background-size: 100% 100%;
  background-repeat: no-repeat;
  text-align: center;
  .ring {
    width: 1604px;
    height: 1030px;
    transform-origin: 802px 515px;
    transform: skew(129deg, 350deg);
    .ring-out {
      width: 998px;
      height: 512px;
      background-image: url(/img/ring.afa929f9.png);
      background-repeat: no-repeat;
      background-size: 100% 100%;
      position: absolute;
      top: 294px;
      left: 511px;
      .ring-ball {
        width: 326px;
        height: 113px;
        h4 {
          color: white;
          font-size: 16px !important;
          padding-top: 28px;
          padding-left: 25px;
          span {
            font-size: 14px !important;
          }
        }
      }
      //老有厚德
      .lyhd {
        background-image: url("../../assets/image/Indicator/blue/laoyouhoude.png");
        background-repeat: no-repeat;
        background-size: 100% 100%;
        position: relative;
        transform: skew(52deg, 8deg);
      }
      //学有优教
      .xyyj {
        background-image: url("../../assets/image/Indicator/blue/xueyouyoujiao.png");
        background-repeat: no-repeat;
        background-size: 100% 100%;
        position: relative;
        transform: skew(52deg, 8deg);
        top: 163px;
      }
      //病友良医
      .byly {
        background-image: url("../../assets/image/Indicator/blue/bingyouliangyi.png");
        background-repeat: no-repeat;
        background-size: 100% 100%;
        position: relative;
        transform: skew(52deg, 8deg);
        top: 136px;
        left: 725px;
      }
      //弱有众扶
      .ryzf {
        background-image: url("../../assets/image/Indicator/blue/ruoyouzhongfu.png");
        background-repeat: no-repeat;
        background-size: 100% 100%;
        position: relative;
        transform: skew(52deg, 8deg);
        top: -372px;
        left: 794px;
      }
    }
    .ring-inner {
      width: 673px;
      height: 353px;
      background-image: url(/img/ring.afa929f9.png);
      background-repeat: no-repeat;
      background-size: 100% 100%;
      position: absolute;
      top: 342px;
      left: 621px;
      .ring-ball {
        width: 326px;
        height: 113px;
        h4 {
          color: white;
          font-size: 16px !important;
          padding-top: 28px;
          padding-left: 25px;
          span {
            font-size: 14px !important;
          }
        }
      }
      //住有宜居
      .zyyj {
        background-image: url("../../assets/image/Indicator/blue/zhuyouyiju.png");
        background-repeat: no-repeat;
        background-size: 100% 100%;
        position: relative;
        transform: skew(52deg, 8deg);
        top: 208px;
      }

      //优有善育
      .yysy {
        background-image: url("../../assets/image/Indicator/blue/youyoushanyu.png");
        background-repeat: no-repeat;
        background-size: 100% 100%;
        position: relative;
        transform: skew(52deg, 8deg);
        top: -191px;
        left: 153px;
      }
      //老有颐养
      .lyyy {
        background-image: url("../../assets/image/Indicator/blue/laoyouyiyang.png");
        background-repeat: no-repeat;
        background-size: 100% 100%;
        position: relative;
        transform: skew(52deg, 8deg);
        top: -89px;
        left: 536px;
      }
    }
  }
}
</style>
<template>
    <div id="lists" class="list">
        <ul>
            <li>
                <div class="title f-cb">
                    <p class="fl">上海缘阁家电服务部</p>
                </div>
                <p class="tel">电话：
                    <a href="tel:021-63165845/63080662">021-63165845/63080662</a><br> 地址：上海市黄浦区中山南一路204号
                    <a href="tel:021-63165845/63080662" class="sign"></a>
                </p>
            </li>
        </ul>
    </div>
</template>
<script>
import servePoint from '@/static/data/servePoint.json'
export default {
  data: function(){
    return {
      servePoint: servePoint
    }
  },
  mounted:function(){
    console.log(this.servePoint[0])
  }
};
</script>
<style lang="less" scoped>
.list {
  ul {
    float: none;
    width: 100%;
  }
  li {
    position: relative;
    float: none;
    width: 90.8%;
    padding: 4.6%;
    p.tel a {
      color: #f60;
    }
    p.tel {
      position: relative;
      min-height: 72px;
    }
    .title {
      padding: 1% 0 3%;
      font-size: 16px;
      line-height: 22px;
      color: #000;
      overflow: hidden;
      p.fl {
        width: 80%;
      }
      span {
        font-size: 14px;
        line-height: 22px;
        color: #666;
      }
    }
    a {
      display: inline-block;
      font-size: 14px;
      line-height: 24px;
      color: #666;
    }
  }
  .fl {
    float: left;
  }
  .f-cb {
    zoom: 1;
  }
  p.tel {
    position: relative;
    min-height: 72px;
  }
  a.map {
    padding-left: 5%;
    background: url(https://www.supor.com.cn/Content/mcss/../img_m/network/bg_sign05.png)
      no-repeat left center/auto 120%;
    margin-top: 2%;
  }
}
</style>



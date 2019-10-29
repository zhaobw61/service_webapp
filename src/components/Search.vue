<template>
  <div class="city-wrap">
    <div class="search">
      <select class="fl" id="sel_region" name="province" v-model="provinceName">
        <option name="provinces" value="null">选择省份</option>
        <option name="provinces" value="北京市">北京市</option>
        <option name="provinces" value="天津市">天津市</option>
        <option name="provinces" value="河北省">河北省</option>
        <option name="provinces" value="山西省">山西省</option>
        <option name="provinces" value="内蒙自治区">内蒙自治区</option>
        <option name="provinces" value="辽宁省">辽宁省</option>
        <option name="provinces" value="吉林省">吉林省</option>
        <option name="provinces" value="黑龙江省">黑龙江省</option>
        <option name="provinces" value="上海市">上海市</option>
        <option name="provinces" value="江苏省">江苏省</option>
        <option name="provinces" value="浙江省">浙江省</option>
        <option name="provinces" value="安徽省">安徽省</option>
        <option name="provinces" value="福建省">福建省</option>
        <option name="provinces" value="江西省">江西省</option>
        <option name="provinces" value="山东省">山东省</option>
        <option name="provinces" value="河南省">河南省</option>
        <option name="provinces" value="湖北省">湖北省</option>
        <option name="provinces" value="湖南省">湖南省</option>
        <option name="provinces" value="广东省">广东省</option>
        <option name="provinces" value="广西自治区">广西自治区</option>
        <option name="provinces" value="海南省">海南省</option>
        <option name="provinces" value="重庆市">重庆市</option>
        <option name="provinces" value="四川省">四川省</option>
        <option name="provinces" value="贵州省">贵州省</option>
        <option name="provinces" value="云南省">云南省</option>
        <option name="provinces" value="西藏自治区">西藏自治区</option>
        <option name="provinces" value="陕西省">陕西省</option>
        <option name="provinces" value="甘肃省">甘肃省</option>
        <option name="provinces" value="青海省">青海省</option>
        <option name="provinces" value="宁夏自治区">宁夏自治区</option>
        <option name="provinces" value="新疆自治区">新疆自治区</option>

      </select>
      <select class="fr" id="sel_city" name="city" v-model="cityName">
        <option name="cityess" value="null">选择城市</option>
        <option name="cityess" value="上海市">上海市</option>
      </select>
      <input name="keyword" id="keyword" type="text" placeholder="关键词" v-model="keyword">
      <input type="submit" value="搜索" class="submit" v-on:click='search'>
    </div>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      provinceName: null,
      cityName: null,
      keyword: null
    };
  },
  watch: {
    provinceName: function() {
      console.log(this.provinceName);
    }
  },
  methods: {
    search: function() {
      this.$emit("searchKey", {
        provinceName: this.provinceName,
        cityName: this.cityName,
        keyword: this.keyword
      });
    }
  }
};
</script>
<style lang='less' scoped>
.city-wrap {
  .search {
    padding: 3%;
    border-top: 1px solid #f5f5f5;
    border-bottom: 1px solid #f5f5f5;
    font-size: 14px;
    input {
      width: 100%;
      height: 35px;
      border: 0;
      border-radius: 0;
      background: #eaeaea;
      margin-bottom: 10px;
    }
    .submit {
      background: #666;
      color: #fff;
    }
    select {
      width: 49%;
      height: 35px;
      border: 0;
      background: #eaeaea;
      margin-bottom: 10px;
      option {
        font-weight: normal;
        display: block;
        white-space: pre;
        min-height: 1.2em;
        padding: 0px 2px 1px;
      }
    }
    .fl {
      float: left;
    }
    .fr {
      float: right;
    }
  }
}
</style>


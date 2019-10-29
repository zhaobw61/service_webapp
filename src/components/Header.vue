<template>
    <div>
        <div class="header">
            <img class="logo" src="@/static/img/logo.png" alt="">
        </div>
        <div class="warn">服务网点信息可能会不定期更新，维修前建议提前致电网点，确保您的产品可以在该网点进行维修，如有疑问欢迎咨询现在服务</div>
    </div>
</template>
<script>
</script>

<style lang="less" scoped>
/* @color:red; */
.header {
  height: 47px;
  width: 100%;
  background-color: #ff6600;
  position: relative;
  .logo {
    display: block;
    width: 128px;
    margin: 0 auto;
  }
}
.warn {
    color: #ff6600;
    font-size: 12px;
    padding: 5px 11px;
    height: 30px;
  }
</style>
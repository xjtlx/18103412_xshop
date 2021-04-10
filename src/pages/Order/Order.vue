<template>
<div>
    <section class="order">
      <HeaderTop title="订单列表"></HeaderTop>
      <section class="order_no_login">
        <img src="./images/order/person.png">
        <h3>登录后查看外卖订单</h3>
        <button>立即登陆</button>
      </section>
    </section>
  </div>
</template>

<script>
import HeaderTop from '../../components/HeaderTop/HeaderTop'
export default {
  components: {
    HeaderTop
  }
}
</script>

<style>
h3{
  position: absolute;
  left: 50%;
  margin-left: -84.2px;
}
button{
  position :absolute;
  top:60%;
  left:50%;
  transform :translate(-50%,-50%);
  width : 100px;
  height : 50px;
  color : #fff;
  text-transform :uppercase;
  text-decoration : none;
  font-family : sans-serif;
  box-sizing:border-box;
  background :linear-gradient(99deg,#03a9f4,#f441a5,#ffeb3b,#03a9f4);
  background-size :400%;
  border-radius:30px;
  z-index : 1;
}
button:hover{
  animation :animate 8s linear infinite;
}
@keyframes animate {
  0%
  {
    background-position :0%;
  }
  100%
  {
    background-position :400%;
  }
}
button:before {
  content : '';
  position :absolute;
  top:-5px;
  left:-5px;
  right:-5px;
  bottom : -5px;
  z-index : -1;
  background :linear-gradient(99deg,#03a9f4,#f441a5,#ffeb3b,#03a9f4);
  background-size : 400%;
  border-radius: 40px;
  filter : blur(20px);
  opacity :0;
  transition :0.5s;
}
button:hover:before {
  filter :blur(20px);
  opacity :1;
  animation :animate 8s linear infinite;
}
</style>

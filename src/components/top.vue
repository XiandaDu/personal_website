<template>
  <div class="top">
  	<div class="container">
  		<slot></slot>
  	  <div class="banner">
  	    <div class="avator"><img src="../common/images/myself.jpg" alt=""></div>
  	    <div class="info">
  	      <h5 class="hello">Welcome!</h5>
  	      <h1>{{info.name}}</h1>
  	      <h6 class="text_hidden">{{info.job}}</h6>
  	      <ul>
  	        <li  class="text_hidden"><b>Email</b> <span>{{info.email}}</span></li>
  	        <li  class="text_hidden"><b>Phone</b> <span>{{info.phone}}</span></li>
  	        <li  class="text_hidden"><b>Birth</b> <span>{{info.birth}}</span></li>
  	        <li  class="text_hidden"><b>Address</b> <span>{{info.address}}</span></li>
  	        <li  class="text_hidden"><b>Education</b> <span>{{info.university}}</span></li>
  	      </ul>
  	    </div>
  	    <div class="clearfix"></div>
  	  </div>
  	</div>
  </div>
</template>

<script>
export default {
  name: 'top',
  data () {
    return {
      info: {
      	"name": "Hi! I am Xianda Du",
      	"job": "Java Developer and Web Engineer",
      	"birth": "December 3rd, 2003",
      	"email": "a32du@uwaterloo.ca",
      	"phone": "+1 2267524494",
      	"address": "295 Lester St. Waterloo, ON",
      	"university": "University of Waterloo, Computer Engineering"
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.top{width:100%;height:auto;background: url('../common/images/banner.jpg') no-repeat center 0px;background-size: cover;color:#fff;}
	.container{width:100%;height:auto;background: url('../common/images/dott.png') repeat;position: relative;}
	.banner{max-width: 1200px;padding: 10% 0;margin: 0 auto;}
	.avator{float:left;width: 40%;text-align: center;position: relative;z-index: 10;}
	.avator img{width: 74%;border: 5px solid rgba(255, 255, 255, 0.68);}
	.info{float:right;width: 60%;text-align: left;}
	.info .hello{position:relative;display:inline-block;padding: 4px 16px;font-size: 16px;color:#fff;background-color: #03a9f4;font-family: 'Overlock', cursive;vertical-align: top; box-shadow: 0 8px 17px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);}
	/*小三角*/
	.info .hello:after{position: absolute;width: 0;height: 0;left:6px;bottom:-4px;content: '';border-style: solid;border-width: 6px 6px 0 6px;border-color: #03a9f4 transparent;}
	h1{font-size: 34px;font-family: 'Overlock', cursive;}
	h6{margin-top: 6px;font-size:14px;font-family: 'Overlock', cursive;color: #C7C7C7;letter-spacing: 4px;}
	.info ul{margin-top: 10px;border-top: 1px solid #fff;}
	.info ul li{font-size: 20px;margin-top: 26px;}
	.info b{display:inline-block;font-family: 'Overlock', cursive;margin-right: 10px;}
	.info ul li span:hover{color: #03a9f4;}
  .info ul li span {
    -webkit-user-select: auto;
    -moz-user-select: auto;
    -ms-user-select: auto;
    user-select: auto;
  }
	#particles-js{position: absolute; top: 0; left: 0; width: 100%; height: 100%; z-index: 1;}
</style>

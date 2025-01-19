<template>
    <div class="main-content">
      <div class="container">
          <div class="main-content-title">
              <h2>Kingdom Technologies</h2>
          </div>
          <div class="main-content-desc">
              <p>The Ultimate Collaborative Community<br> For Startup Success</p>
          </div>
          <div class="main-content-video">
              <div class="how-it-worksimg">
                  <img :src="`.${publicPath}images/how-it-works.png`" alt="">
              </div>
              <div class="main-content-middle-img">
              <img :src="`.${publicPath}images/vid-img.png`" alt="">
              <span><i class="fas fa-play"></i></span>
              </div>
              
              <div class="how-it-startsimg">
                  <img :src="`.${publicPath}images/when-to-start.png`" alt="">
              </div>
          </div>
          <div class="main-content-get-started">
              <div class="get-start">
                  <a href="#" class="get-start-btn">get started now</a>
              </div>
          </div>
      </div>
    </div>    
</template>
<script>

export default{
    name:'MainContent',
    data() {
        return {
            publicPath: process.env.BASE_URL,
        }
    }
}
</script>

<style scoped>
.main-content-title h2{
    font-size: 50px;
letter-spacing: 1px;
line-height: 48px;
color: #060a25;
font-weight: 600;
text-align: center;
text-transform:capitalize;
margin: 30px 0;
}
.main-content-desc {
	width: 80%;
	margin: auto;
}
.main-content-desc p{
font-size: 32px;
letter-spacing: 1px;
line-height: 32px;
color: #060a25;
font-weight: 400;
text-align: center;
margin-top: 0;
}
.main-content-video{
    display: flex;
    width: 100%;
    position: relative;
    align-items: center;
    
}
.main-content-middle-img{
    position: relative;
    width: 60%;
    margin: auto;
}
.main-content-middle-img img{
    width: 70%;
}
.main-content-middle-img span{
    position: absolute;
    left: 47%;
    top: 45%;
    border: 2px solid #fff;
    border-radius:100% ;
    padding: 15px 15px 15px 20px;
}
.main-content-video span i{
    font-size: 24px;
    color: #fff;
}
.get-start-btn{
    display: inline-block;
}
.get-start-btn {
	background: #fc7e00;
	font-size: 32px;
	line-height: 38px;
	color: #fefefd;
	font-weight: 600;
	text-align: center;
	text-transform: uppercase;
	padding: 5px 30px;
	border-radius: 5px;
    margin: 50px 0;
    transition: 0.3s all linear;
    border: 2px solid #060a25;
}
.get-start-btn:hover{
    background: #060a25;
}
.how-it-worksimg {
    width: 15%;
    position: absolute;
    bottom: 0;
    left: 12%;
  
}
.how-it-worksimg img{
    width: 80%;
}
.how-it-startsimg {
	width: 25%;
	position: absolute;
	left: 61%;
	bottom: -23%;
}
.how-it-startsimg img{
    width: 80%;
}

@media screen and (max-width:1800px) {
    .how-it-startsimg{
	left: 63%;
}
}
@media screen and (max-width:1600px) {
    .how-it-startsimg{
	left: 65%;
    
}
.main-content-middle-img img{
	width: 80%;
}
.how-it-worksimg {
	left: 10%;
}
}
@media screen and (max-width:1440px) {
    .how-it-startsimg{
	left: 66%;
    bottom: -30%;
}
.main-content-middle-img img {
	width: 90%;
}
.how-it-worksimg {
	left: 6%;
}
}
@media screen and (max-width:1366px) {
    .how-it-startsimg{
	left: 68%;
    bottom: -20%;
}
.main-content-middle-img span {
	
	left: 45%;
	top: 40%;
}
}
@media screen and (max-width:1199px) {
    .main-content-video span i {
	font-size: 18px;
}
.main-content-middle-img img {
	width: 100%;
}
.how-it-worksimg {
	left: 3%;
}
.how-it-startsimg {
	left: 70%;
	bottom: -20%;
}
.get-start-btn {
	font-size: 20px;
	margin: 30px 0;
}
}
@media screen and (max-width:991px) {
    .main-content-title h2 {
	font-size: 45px;
}
.main-content-desc p {
	font-size: 28px;
}
.main-content-middle-img span {
	left: 43%;
	top: 35%;
}
}
@media screen and (max-width:767px) {
    .main-content {
	display: none;
}
    
}
</style>
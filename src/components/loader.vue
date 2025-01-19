<template>
<div>
    <div class="loader-main">
        <div class="container">
            <div class="loader-content-box">
                <div class="nightmode">
                    <a href="#" class="nightmodebtn"><img :src="`.${publicPath}images/brightness.png`" alt=""></a>
                </div>
                <div class="daymode">
                    <a href="#" class="daymodebtn"><img :src="`.${publicPath}images/night.png`" alt=""></a>
                </div>
                <div class="loader-logo">
                    <img :src="`.${publicPath}images/nav-left-logo.png`" alt="" id="daylogo">
                    <img :src="`.${publicPath}images/nav-left-logo-dark.png`" alt="" id="nightlogo">
                </div>
                <div class="loader-head">
                    <h2>Step-by-step Startup Strategies</h2>
                </div>
                <div class="loader-desc">
                    <p>Get one critical proven start up strategy each week to make sure you're as on track us as much as possible.</p>
                </div>
                <div class="loader-user-info">
                    <form action="#">
                        <input type="email" name="loader-mail" id="loaderMail" placeholder="Email">
                        <button class="loadermailbtn">Subscribe</button>
                    </form>
                </div>
                <div class="loader-link">
                    <a href="#">Let me explore first <span><i class="fas fa-chevron-right"></i></span></a>
                </div>
            </div>
        </div>
    </div>
    <home/>    
    </div>
</template>
<script>
import JQuery from 'jquery'
let $ = JQuery
import home from './home'

export default{
    name:'loader',
    components:{
        home
    },
    data() {
        return {
            publicPath: process.env.BASE_URL,
        }
    },
    mounted(){
       $('.loader-link>a').click(function (e) { 
           e.preventDefault();
           $('.home-main').toggleClass('active')
           $('.loader-main').toggleClass('active')
           
       });
       $('.nightmodebtn').click(function (e) { 
           e.preventDefault();
           $('.loader-main').toggleClass('day')
       });
       $('.daymodebtn').click(function (e) { 
           e.preventDefault();
           $('.loader-main').removeClass('day')
       });
    
   }
}
</script>

<style scoped>
.nightmodebtn {
	display: block;
	border: 2px solid #fff;
	padding: 2px 5px 0px;
	border-radius: 10px;
    transition: 0.3s all linear;
}
.nightmodebtn:hover{
    box-shadow: 0px 0px 14px 0px #fff;
}
.nightmodebtn img{
    width: 25px;
}
.nightmode {
	display: inline-block;
    position: absolute;
    top: 0px;
    right: 0;
}
.daymodebtn {
	display: block;
	border: 2px solid #060a25;
	padding: 2px 5px 0px;
	border-radius: 10px;
    transition: 0.3s all linear;
}
.daymodebtn:hover{
    box-shadow: 0px 0px 14px 0px #060a25;
}
.daymodebtn img{
    width: 25px;
}
.daymode {
	display: inline-block;
    position: absolute;
    top: 0px;
    right: 0;
    display: none;
}

.home-main.active{
    display: block;
}
.home-main{
    display: none;
}
.loader-main.active{
    display: none;
}
.loader-main {
	background: #060a25;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    

}
.loader-content-box {
	max-width: 640px;
    position: relative;
}
#daylogo {
	display: inline-block;
}
#nightlogo {
	display: none;
}
.loader-head h2 {
	font-size: 28px;
	font-weight: 600;
	text-transform: uppercase;
	color: #fff;
	margin: 50px 0;
    letter-spacing: 2px;
    text-align: left;
}
.loader-desc p {
	font-size: 28px;
	color: #fff;
	font-weight: 500;
	letter-spacing: 1px;
	text-align: left;
    padding: 0 0 50px;
}
.loader-user-info form {
	text-align: left;
	width: 95%;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
}
#loaderMail {
	width: 98%;
	text-align: left;
	position: relative;
	background: transparent;
	border: 2px solid #5b5b5b;
	padding: 10px;
	border-radius: 5px 0 0 5px;
    font-size: 18px;
    border-right: none;
    font-weight: 500;
    color: #fff;
}
#loaderMail::placeholder{
    color: #fff;
    opacity: 1 ;
}
#loaderMail:focus-visible{
    outline: none;
}
.loadermailbtn {
	background: #fc7e00;
    padding: 10px;
    border-radius: 0px 5px 5px 0px;
    color: #fff;
    font-size: 18px;
    font-weight: 500;
    border: 2px solid #fc7e00;
    transition: 0.3s all linear;
}
.loadermailbtn:hover{
    color: #060a25;
}

.loader-link {
	display: block;
	text-align: left;
	margin-top: 50px;
}
.loader-link a {
	font-size: 20px;
	color: #fff;
	font-weight: 500;
	letter-spacing: 1px;
    display: block;
    transition: 0.3s all linear;
}
.loader-link a:hover {
	color: #fc7e00;
}
.loader-main.day{
    background:#fff;
}
.loader-main.day .daymode{
    display: block;
}
.loader-main.day .nightmode{
    display: none;
}
.loader-main.day #daylogo {
	display: none;
}
.loader-main.day #nightlogo {
	display: inline-block;
}
.loader-main.day .loader-head h2 {
	color: #060a25;
}
.loader-main.day .loader-desc p {
	color: #060a25;
}
.loader-main.day #loaderMail{
	color: #060a25;
}
.loader-main.day #loaderMail::placeholder{
    color: #060a25;
}
.loader-main.day .loader-link a {
	color: #060a25;
}
.loader-main.day .loader-link a:hover {
	color: #fc7e00;
}
@media screen and (max-width:767px) {
    .loader-main{
        padding: 50px 0;
    }
    .loader-head h2 {
	font-size: 22px;
    text-align: center;
    margin: 30px 0;
    }
    .loader-desc p {
	font-size: 20px;
	text-align: center;
    padding: 0 0 20px;
    }
    .loader-user-info form{
        flex-direction: column;
    }
    .loader-user-info form{
        width: 100%;
    }
    #loaderMail{
        border-right: 2px solid #5b5b5b;
        border-radius:5px;
        margin-bottom: 30px;
        width: 90%;
    }
    .loadermailbtn{
        border-radius: 5px;
    }
    .loader-link{
        text-align: center;
    }
    
}
@media screen and (max-width:575px) {
    .loader-main{
        padding: 70px 0;
    }
    .nightmode {
        top: -65px;
        right: 45%;
    }
    .daymode{
        top: -65px;
        right: 45%;
    }
    .loader-link a {
        font-size: 16px;
    }
    .loader-desc p {
        font-size: 16px;
    }
}
</style>
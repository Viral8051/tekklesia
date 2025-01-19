<template>
    <div class="option-main">
        <div class="option-main-content top">
            <div class="option-main-content-box">
                <div class="option-box-extra">
                    <img :src="`.${publicPath}images/who-we-are.png`" alt="">
                </div>
            </div>
            <div class="option-main-content-box">
                <div class="option-box-extra">
                    <img :src="`.${publicPath}images/why-we-exist.png`" alt="">
                </div>
            </div>
            <div class="option-main-content-box">
                <div class="option-box-extra">
                    <img :src="`.${publicPath}images/what-we-do.png`" alt="">
                </div>
            </div>
            <div class="option-main-content-box">
                <div class="option-box-extra">
                    <img :src="`.${publicPath}images/where-we-are.png`" alt="">
                </div>
            </div>
        </div>
        <div class="option-main-content bottom">
            <div class="option-main-content-box">
                <div class="option-box-content">
                    <a href="#">
                        <img :src="`data:img/png;base64,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`" alt="">
                    </a>
                </div>
            </div>
            <div class="option-main-content-box">
                <div class="option-box-content">
                    <a href="#">
                        <img :src="`data:img/png;base64,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`" alt="">
                    </a>
                </div>
            </div>
            <div class="option-main-content-box">
                <div class="option-box-content">
                    <a href="#">
                        <img :src="`data:img/png;base64,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`" alt="">
                    </a>
                </div>
            </div>
            <div class="option-main-content-box">
                <div class="option-box-content">
                    <a href="#">
                        <img :src="`data:img/png;base64,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`" alt="">
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>
<script>

export default{
    name:'OptionMain',
    data() {
        return {
            publicPath: process.env.BASE_URL,
        }
    }
}
</script>

<style scoped>
.option-box-content a img {
	height: 100px;
}
.option-main-content {
    display: flex;
    align-items: center;
    padding: 0 50px;
    margin-top: 30px;
}
.option-main-content-box {
    width: 25%;
    text-align: left;
}
.option-main-content-box:nth-child(3){
    text-align: right;
}
.option-main-content-box:nth-child(4){
    text-align: right;
}
.option-box-extra {
    padding: 0 0 40px 0;
}
.option-box-content {
    text-align: center;
    position: relative;
}
.option-main-content.bottom {
    padding: 0;
    margin: 0;
}
.option-main-content.bottom  .option-main-content-box {
    border-top: 2px solid #060a25;
    border-left: 2px solid #060a25;
    border-bottom: 2px solid #060a25;
    padding: 15px 0;
}
.option-main-content.bottom  .option-main-content-box:first-child{
    border-left:none ;
}
@media screen and (max-width:767px) {
    .option-main-content.top {
	display: none;
}
.option-box-content a img{
        width: 60%;
        height: 80px;
    }
}


@media  screen and (max-width:479px) {
    .option-box-content a img[data-v-735a949e] {
	width: 60%;
	height: 75px;
}
}
@media  screen and (max-width:400px) {
    .option-box-content a img[data-v-735a949e] {
	width: 60%;
	height: 50px;
}
}


</style>
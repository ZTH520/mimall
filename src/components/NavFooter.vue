<template>
    <div class="footer">
        <div class="footer-logo">
            <img src="/imgs/logo-footer.png" alt="">
            <p>小米商城</p>
        </div>
        <div class="footer-link">
            <a href="#">个人主页</a><span>|</span>
            <a href="#">Vue全栈课程</a><span>|</span>
            <a href="#">React全家桶课程</a><span>|</span>
            <a href="#">微信支付专项课程（H5+小程序+Node+Mongo）</a>
        </div>
        <div class="copyright">Copyright ©2019 <span class="domain">mi.com</span> All Rights Reserved.</div>
    </div>
</template>

<script>

export default {
    name: 'nav-footer'
}

</script>
<style lang="scss" scoped>
@import '../assets/scss/config.scss';
    .footer{
        height: 234px;
        border-top: 4px solid $colorA;
        background-color: $colorB;
        color: $colorD;
        font-size: 16px;
        text-align: center;
        .footer-logo{
            margin-top: 46px;
            margin-bottom: 32px;
            img{
                width: 53px;
                height: 36px;
                margin-bottom: 13px;
            }
        }
        .footer-link{
            a{
                display: inline-block;
                color: $colorD;
            }
            span{
                margin: 0 10px;
            }
            margin-bottom: 13px;
        }
        .copyright{
            span{
                color: $colorA;
            }
        }
    }
</style>
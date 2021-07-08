<template>
    <div>
        <nav>
            <div class="brand__info">
                <img alt="Logo" src="../assets/logo.svg">
            </div>
            <div class="nav__links">
                <ul>
                    <router-link active-class="active" tag="li" to="/product" class="link__item">Products</router-link>
                    <router-link active-class="active" tag="li" to="/pricing" class="link__item">Pricing &amp; Features</router-link>
                    <router-link active-class="active" tag="li" to="/advertise" class="link__item">Advertise</router-link>
                    <router-link active-class="active" tag="li" to="/demo" class="link__item">Demo</router-link>
                    <router-link active-class="active" tag="li" to="/contact" class="link__item">Contact</router-link>
                    <router-link active-class="active" tag="li" to="/login" class="link__item">Log In</router-link>
                </ul>
                <div class="sign_up__button">
                    <app-button tag="a" to="/signup">Sign Up</app-button>
                </div>
            </div>
            <div class="mobile_nav__toggle">
                <div class="line"></div>
                <div class="line"></div>
                <div class="line"></div>
            </div>
        </nav>
    </div>
</template>

<script>
import Button from '@/components/buttons/MainButton'
export default {
    components: {
        appButton: Button
    }
}
</script>

<style scoped lang="css">
    div nav{
        display: flex;
        justify-content: space-between;
        padding: 36px 150px;
    }

    div nav .nav__links{
        display: flex;
    }

    div nav .nav__links ul{
        padding: 0;
        margin: 0;
    }

    div nav .nav__links ul li{
        display: inline-block;
        margin: 0 35px;
        font-style: normal;
        font-weight: normal;
        cursor: pointer;
        font-size: 18px;
    }

    div nav .nav__links ul li:hover,
    div nav .nav__links ul li:focus,
    div nav .nav__links ul li.active{
        color: #FD435A;
    }

    div nav .nav__links .sign_up__button{
        margin-left: 20px;
    }

    div nav .mobile_nav__toggle {
        display: none;
    }

    div nav .mobile_nav__toggle .line {
        width: 24px;
        height: 3px;
        margin: 3px;
        background: #FD435A;
    }

    @media screen and (max-width: 1450px) {
        div nav{
            padding: 36px 120px;
        }

        div nav .nav__links ul li{
            margin: 0 25px;
        }
    }

    @media screen and (max-width: 1300px) {
        div nav{
            padding: 36px 80px;
        }

        div nav .nav__links ul li{
            margin: 0 20px;
        }
    }

    @media screen and (max-width: 1150px) {
        div nav .nav__links {
            display: none;
        }

        div nav .mobile_nav__toggle {
            display: block;
        }
    }

    @media screen and (max-width: 800px) {
        div nav{
            padding: 36px 50px;
        }
    }

    @media screen and (max-width: 500px) {
        div nav{
            padding: 36px 30px;
        }
    }

    @media screen and (max-width: 400px) {
        div nav{
            padding: 30px 15px;
        }
    }
</style>
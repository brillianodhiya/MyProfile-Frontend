<template>
    <div>
        <Animation />
        <Header />
        <div class="firstcontainer">
            <div class="container">
                <div class="box">
                    <div class="imgBx">
                        <img src="image2.jpg">
                    </div>
                    <ul class="socail-icon">
                        <li><a href="#"><i class="fa fa-facebook" aria-hidden="true"></i></a></li>
                        <li><a href="#"><i class="fa fa-twitter" aria-hidden="true"></i></a></li>
                        <li><a href="#"><i class="fa fa-google-plus" aria-hidden="true"></i></a></li>
                        <li><a href="#"><i class="fa fa-linkedin" aria-hidden="true"></i></a></li>
                        <li><a href="#"><i class="fa fa-instagram" aria-hidden="true"></i></a></li>
                    </ul>
                    <div class="details">
                        <h2>Someone Famous<br><span>UX/UI Designer</span></h2>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
@import '../assets/css/partner.css';
</style>

<script>
import Animation from "~/components/animation"
import Header from "~/components/header"

export default {
    components: {
        Animation,
        Header
    }
}
</script>
<template>
    <div>
        <Animation />
        <Header />
        <div class="firstcontainer">
            <div class="container">
                <div class="row">
                    <div class="col-xl-4 col-md-6 mb-4">
                        <div class="card border-0 shadow">
                            <img src="~/assets/images/hakim2.jpeg" class="card-img-top" alt="...">
                            <div class="card-body text-center">
                            <h5 class="card-title mb-0"><a href="https://www.instagram.com/ginryu_/">Ananda Muhammad Luqmanul Hakim Nurohmat</a></h5>
                            <div class="card-text text-black-50">Animator 2D / 3D</div>
                            </div>
                        </div>
                    </div>
                    <div class="col-xl-4 col-md-6 mb-4">
                        <div class="card border-0 shadow">
                            <img src="~/assets/images/zulfa2.jpeg" class="card-img-top" alt="...">
                            <div class="card-body text-center">
                            <h5 class="card-title mb-0"><a href="https://www.instagram.com/miyounewa_zulfa/">Aulia Zulfa Istiqomah</a></h5>
                            <div class="card-text text-black-50">2D Line Art</div>
                            </div>
                        </div>
                    </div>
                    <div class="col-xl-4 col-md-6 mb-4">
                        <div class="card border-0 shadow">
                            <img src="~/assets/images/hafidh2.jpeg" class="card-img-top" alt="...">
                            <div class="card-body text-center">
                            <h5 class="card-title mb-0">Hafidh Hanan An-Nafi'</h5>
                            <div class="card-text text-black-50">Team Support</div>
                            </div>
                        </div>
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
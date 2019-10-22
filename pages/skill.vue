<template>
    <div>
        <div class="open">
			<div class="layer"></div>
			<div class="layer"></div>
		</div>
		<section>
			<div class="header">
				<h2 class="back" @click="goBack()"><a href="#"><i class="fa fa-arrow-left"></i> Back</a></h2>
				<ul>
					<li>
						<a href="#">Skills</a>
					</li>
				</ul>
			</div>
            <div class="bannerText">
                <h3>Here is My Skill</h3>
                <div class="row">
                    <div class="col-sm-2">
                        test
                    </div>
                    <div class="col-sm-2">
                        test
                    </div>
                    <div class="col-sm-2">
                        test
                    </div>
                    <div class="col-sm-2">
                        test
                    </div>
                    <div class="col-sm-2">
                        test
                    </div>
                    <div class="col-sm-2">
                        test
                    </div>
                    <div class="col-sm-2">
                        test
                    </div>
                    <div class="col-sm-2">
                        test
                    </div>
                    <div class="col-sm-2">
                        test
                    </div>
                </div>
            </div>
			<ul class="sci">
				<li><a href="https://wa.me/628819671476"><i class="fa fa-whatsapp"></i></a></li>
				<li><a href="https://github.com/brillianodhiya"><i class="fa fa-github"></i></a></li>
				<li><a href="https://www.linkedin.com/in/brilliano-dhiya-44b196194/"><i class="fa fa-linkedin"></i></a></li>
				<li><a href="https://www.instagram.com/brilliano_19/"><i class="fa fa-instagram"></i></a></li>
			</ul>
			<div class="element1"></div>
			<div class="element2"></div>
		</section>
    </div>
</template>

<script>
import axios from 'axios'

export default {
    data () {
		return {
            Skill: [],
		}
	},
	mounted () {
		axios('https://brillianoprofileapi.herokuapp.com/skill', {
			crossDomain: true
		})
		.then(({data}) => {
			this.Skill = data.data
		})
	},
	methods: {
		goBack () {
			this.$router.replace({ 'path' : '/' })
		}
	}
}
</script>

<style lang="css" scoped>
@import '../assets/css/about.css';

.bannerText
{
	position: absolute;
	top: 20%;
	left: 10%;
	transform: translateY(-50%);
}
/* .skillcontainer {
    position: absolute;
    top: 20%;
    left: 10%;
} */
</style>
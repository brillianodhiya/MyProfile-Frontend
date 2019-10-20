<template>
    <div class="this_container">
        <div class="open">
			<div class="layer"></div>
			<div class="layer"></div>
		</div>
		<section v-for="item in About" v-bind:key="item.key">
			<div class="header">
				<h2 class="back" @click="goBack()"><a href="#"><i class="fa fa-arrow-left"></i> Back</a></h2>
				<ul>
					<li>
						<a href="#">About Me</a>
					</li>
				</ul>
			</div>
			<div class="bannerText">
				<h2>{{ item.my_name }}</h2><br>
				<h3>{{ item.my_role[0] }} － {{ item.my_role[2] }}</h3>
				<p>{{ item.my_summary }}</p>
				<h4>Address</h4>
				<p>{{ item.my_address }}</p>
				<h4>Birth / Age</h4>
				<p>{{ item.my_birth }} / {{ item.my_age }}</p>
				<!-- <h4>Mariage Status</h4>
				<p>{{ item.is_marriage }}</p> -->
			</div>
			<img src="~/assets/images/me3.png" class="bulb">
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
			About: []
		}
	},
	mounted () {
		axios('https://brillianoprofileapi.herokuapp.com/detail', {
			crossDomain: true
		})
		.then(({data}) => {
			this.About = data.data
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
</style>
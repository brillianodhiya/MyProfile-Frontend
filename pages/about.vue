<template>
    <div class="this_container">
		<Animation />
		<section v-for="item in About" v-bind:key="item.key">
			<Header />
			<div class="bannerText">
				<h2>{{ item.my_name }}</h2><br>
				<h3>{{ item.my_role[0] }} － {{ item.my_role[2] }}</h3>
				<p>{{ item.my_summary }}</p>
				<h4>Address</h4>
				<p>{{ item.my_address }}</p>
				<h4>Birth / Age</h4>
				<p>{{ item.my_birth }} / {{ item.my_age }}</p>
				<h4>Skills</h4>
				<p>HTML5, CSS, C++, Java, PHP, JavaScript, Bootstrap, Materialize, MySQL, Firebase, MongoDB, Node.js, ReactJS, React Native, Redux, Mocha, Vue.js, Nuxt.js, JQuery, Krita, Paint Tool Sai</p>
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
import Animation from "~/components/animation"
import Header from "~/components/header"

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
	components: {
		Animation,
		Header
    }
}
</script>

<style lang="css" scoped>
@import '../assets/css/about.css';
</style>
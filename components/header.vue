<template>
    <div>
        <div class="header">
			<h2 class="back" @click="goBack()"><a href="#"><i class="fa fa-arrow-left"></i> Back</a></h2>
			<ul>
				<li>
					<a href="#" class="Route">{{ this.$route.name }}</a>
				</li>
			</ul>
		</div>
    </div>
</template>

<style scoped>
@import '../assets/css/about.css';
</style>

<script>
export default {
    methods: {
		goBack () {
			this.$router.replace({ 'path' : '/' })
		}
	},
}
</script>
<template>
  <div>
    <div class="the_container">
    <Quote />
    <div class="welcome">
      <h3>Welcome to Brilliano profile !</h3>
      <p># Please click menu's below</p>
    </div>
      <ul>
        <li>
          <a href="#">
            <span>About</span>
            <span @click="aboutMe()">About</span>
          </a>
        </li>
        <li>
          <a href="#">
            <span>Education</span>
            <span @click="education()">Education</span>
          </a>
        </li>
        <li>
          <a href="#">
            <span>Experience</span>
            <span @click="experience()">Experience</span>
          </a>
        </li>
        <li>
          <a href="#">
            <span>Project</span>
            <span @click="project()">Project</span>
          </a>
        </li>
        <li>
          <a href="#">
            <span>Partner</span>
            <span @click="partner()">Partner</span>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="css" scoped>
@import url('https://fonts.googleapis.com/css?family=Poppins:400,500,600,700');
.the_container
{
	margin: 0;
	padding: 0;
	display: flex;
	justify-content: center;
	align-items: center;
	min-height: 100vh;
	font-family: 'Poppins', sans-serif;
	background: #111;
  /* background: url('../assets/images/background.png'); */
  /* background-repeat: no-repeat;
  background-size: cover; */
  opacity: 0.99;
  /* background-color: rgba(51, 51, 51, 0.4); */
  font-size: 22px;
}
ul
{
	margin: 0;
	padding: 0;
	display: flex;
  /* flex-direction: column; */
}
ul li
{
	position: relative;
	list-style: none;
	margin: 0 10px;
}
ul li a
{
	position: relative;
	height: 25px;
	display: block;
	text-decoration: none;
	overflow: hidden;
	text-transform: uppercase;
	font-weight: 600;
}
ul li a span
{
	width: 100%;
	height: 100%;
	display: block;
	transition: 0.5s;
	color: #fff;
}
ul li a span:nth-child(1)
{
	color: #444;
}
ul li a span:nth-child(2)
{
	color: #fff;
}
ul li:hover a span:nth-child(1)
{
	transform: translateY(-100%);
}
ul li:hover a span:nth-child(2)
{
	transform: translateY(-100%);
}
ul li:before
{
	content: '';
	position: absolute;
	top: -90px;
	left: -65px;
	width: 265px;
	height: 265px;
	background: #0f0;
	z-index: -1;
	opacity: 0;
	transition: 0.5s;
	transform: translateY(100px);
}
ul li:hover:before
{
	opacity: 1;
	transition-delay: 0.5s;
	transform: translateY(0);
}
ul li:nth-child(1):before
{
	background: url(../assets/images/imgme.jpeg);
	background-size: cover;
  filter: opacity(0.5);
}
ul li:nth-child(2):before
{
	background: url(../assets/images/imgskill.jpg);
	background-size: cover;
  filter: opacity(0.5);
}
ul li:nth-child(3):before
{
	background: url(../assets/images/imgpendidikan.jpg);
	background-size: cover;
  filter: opacity(0.5);
}
ul li:nth-child(4):before
{
	background: url(../assets/images/imgwork.jpg);
	background-size: cover;
  filter: opacity(0.5);
}
ul li:nth-child(5):before
{
	background: url(../assets/images/imgproject.jpg);
	background-size: cover;
  filter: opacity(0.5);
}
ul li:nth-child(6):before
{
	background: url(../assets/images/imglilia.jpeg);
	background-size: cover;
  filter: opacity(0.5);
}
.welcome {
  position: absolute;
  top: 80px;
  /* width: 500px;
  /* margin: 5% auto; */
  margin: 20px;
  color: rgb(255, 255, 255);
}
@media (min-width: 200px) {
  ul {
    flex-direction: column;
  }
  h3 {
    font-size: 18px;
  }
  p {
    font-size: 15px;
  } 
}

@media (min-width: 300px) {
  ul {
    flex-direction: column;
  }
  h3 {
    font-size: 18px;
  }
  p {
    font-size: 15px;
  } 
}

@media (min-width: 411px) {
  ul {
    flex-direction: column;
  }
  h3 {
    font-size: 18px;
  }
  p {
    font-size: 15px;
  } 
}

@media (min-width: 576px) {
  ul {
    flex-direction: column;
  }
  h3 {
    font-size: 18px;
  }
  p {
    font-size: 15px;
  } 
}

@media (min-width: 768px) {
  ul {
    flex-direction: column;
  }
  h3 {
    font-size: 18px;
  }
  p {
    font-size: 15px;
  } 
}

@media (min-width: 992px) {
  ul {
    flex-direction: column;
  }
  h3 {
    font-size: 18px;
  }
  p {
    font-size: 15px;
  } 
}

@media (min-width: 1200px) {
  ul {
    flex-direction: row;
  }
  h3 {
    font-size: 27px;
  }
  p {
    font-size: 18px;
  } 
}
</style>

<script>
import Quote from "~/components/quote"

export default {
    components: {
        Quote
    },
    methods: {
      aboutMe () {
        this.$router.replace({ 'path': '/about' })
      },
      education () {
        this.$router.replace({ 'path': '/education' })
      },
      experience () {
        this.$router.replace({ 'path': '/experience' })
      },
      project () {
        this.$router.replace({ 'path': '/project' })
      },
      partner () {
        this.$router.replace({ 'path': '/partner' })
      }
    }
}
</script>
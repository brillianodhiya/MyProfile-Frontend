<template>
    <div>
        <Animation />
        <Header />
        <div class="firstcontainer">
            <div class="thecontainer">
                <div v-for="item in Project" v-bind:key="item.key">
                    <div class="box">
                        <img :src="item.project_ss">
                        <h2><a :href="item.project_repo">{{ item.project_title }}</a></h2>
                        <p>{{ item.project_description }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
@import '../assets/css/project.css';
</style>

<script>
import Animation from "~/components/animation"
import Header from "~/components/header"
import axios from 'axios'

export default {
    components: {
        Animation,
        Header
    },
    data () {
        return {
            Project: []
        }
    },
    mounted () {
        axios('https://brillianoprofileapi.herokuapp.com/project', {
            crossDomain: true
        })
        .then(({data}) => {
            this.Project = data.data
        })
    },
}
</script>
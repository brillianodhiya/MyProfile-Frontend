<template>
    <div>
        <Animation />
        <Header />
        <div class="thecontainer">
            <div class="timeline">
                <ul>
                    <li v-for="item in Education" v-bind:key="item.key">
                        <div class="content">
                            <h3>{{ item.school_name }}</h3>
                            <p>{{ item.school_description }}</p>
                        </div>
                        <div class="time">
                            <h4>{{ item.graduation_year }}</h4>
                        </div>
                    </li>
                    <div style="clear: both;"></div>
                </ul>
            </div>
        </div>
    </div>
</template>

<style scoped>
@import '../assets/css/timeline.css';

</style>

<script>
import Animation from "~/components/animation"
import Header from "~/components/header"
import axios from "axios";

export default {
    components: {
        Animation,
        Header
    },  
    data () {
        return {
            Education: []
        }
    },
    mounted () {
        axios("https://brillianoprofileapi.herokuapp.com/edu", {
            crossDomain: true
        })
        .then(({data}) => {
            this.Education = data.data
        })
    },
    
}
</script>
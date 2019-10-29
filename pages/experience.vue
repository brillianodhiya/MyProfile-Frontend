<template>
    <div>
        <Animation />
        <Header />
        <div class="thecontainer">
            <div class="timeline">
                <ul>
                    <li v-for="item in Experience" v-bind:key="item.key">
                        <div class="content">
                            <h3>{{ item.work_company }} {{ item.work_at }}</h3>
                            <p>{{ item.work_description }}</p>
                        </div>
                        <div class="time">
                            <h4>{{ item.work_interval }}</h4>
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
            Experience: []
        }
    },
    mounted () {
        axios("https://brillianoprofileapi.herokuapp.com/work", {
            crossDomain: true
        })
        .then(({data}) => {
            this.Experience = data.data
        })
    },
    
}
</script>
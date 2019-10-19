<template>
    <div class="quote">
        <div v-for="item in Quotes" v-bind:key="item.key">
            <h5>{{ item.title }}</h5>
            <p>❝ {{ item.quote }} ❞ <br>- {{ item.author }}</p>
        </div>
    </div>
</template>

<style scoped>
.quote {
    position: absolute;
    right: 10px;
    bottom: 10px;
    color: rgb(255, 255, 255);
}
p {
    text-align: right;
    font-size: 12px;
}
h5 {
    text-align: right;
    font-size: 17px;
}
</style>

<script>
import axios from 'axios'

export default {
    data () {
        return {
            Quotes: []
        }
    },
    mounted () {
        axios('https://quotes.rest/qod.json', {
            crossDomain: true
        })
        .then(({data}) => {
            this.Quotes = data.contents.quotes
        })
    }
}
</script>
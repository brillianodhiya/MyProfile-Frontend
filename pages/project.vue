<template>
    <div>
        <Animation />
        <div>
            <Header />
        </div>
    </div>
</template>

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
<template>
    <section class="row">
        <rocket 
        v-for="rocket in rockets" 
        :key="rocket.id" 
        :rocket="rocket"
        >
        </rocket>
    </section>
</template>

<script>
import {mapGetters} from 'vuex';

import Rocket from '../components/Rocket.vue'
    export default {
        computed: mapGetters(['rockets']),
        components:{
            Rocket
        }
    }
</script>

<style lang="scss" scoped>

</style>
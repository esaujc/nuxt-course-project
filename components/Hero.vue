<template>
    <div>
        <slot name="header">
            
        </slot>
        Chucos
        <!-- <p v-if="banner == 'slogan'"><Banner /></p> -->
        <p v-if="num == 1">Raaaa<Banner /></p>
        <p v-else>Roooo<Slogan /></p>
    </div>
</template>


<script>
import Slogan from '~/components/Slogan';
import Banner from '~/components/Banner' 
export default {
    components: {
        Slogan,
        Banner
    },
    data: () => ({
        banner:'slogan',
        num: 1
    })   
}
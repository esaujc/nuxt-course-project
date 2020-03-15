<template>
    <div>
        <p>{{message}}</p>
        <p v-show="true">Se muestra</p>
        <p v-if="num>10"> Muestra If</p>
        <p v-else>No muestra el if</p>
        <ul>
            <li v-for="item in items" v-bind:key="item">{{item}}</li>
        </ul>
        <ul>
            <li v-for="(item,i) in items" :key="item">{{i}}</li>
        </ul>
        <label>Name: </label>
        <input v-model="name" type="text" />
             {{name}}
        <button v-on:click="hello" class="button is-info">Hi</button>
        {{count}}
    </div>
</template>

<script>
export default {
    data: () => ({
        message: 'Mensaje',
        num: 10,
        items:[1,2,3,4],
        name: '',
        count: 0

    }),
    methods: {
        hello(){
            this.count++;
        }
    }
}
</script>
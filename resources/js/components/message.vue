<template>
<div>
    <li class="list-group-item" :class="className"><slot></slot>
    <span id="time">{{ time }}</span>
    </li>
    <small class="badge float-right" :class="badgeColor">{{ user }}</small>
</div>
</template>

<script>
    export default {
        props:[
            'color',
            'user',
            'time',
        ],

        data(){
            return{

            }
        },
        computed:{
            className(){
                return 'list-group-item-'+this.color;
            },
            badgeColor(){
                return 'badge-'+this.color;
            }
        },

        mounted() {
            console.log('Component mounted.')
        }
    }
    // 04:34
    // #7 >> 06:19
</script>
<style>
    #time{
        font-size: 10px;
        margin-top: 11px;
        margin-left: 5px;
        color: black;
    }
</style>


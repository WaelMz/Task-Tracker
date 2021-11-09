<template>
    <button :style="{background: color}" class="btn" v-on:click="$emit('btn-click')">{{ text }}</button>
</template>

<script>
export default {
    name:'Button',
    props:{
        text:String,
        color:String
    }
}
</script>
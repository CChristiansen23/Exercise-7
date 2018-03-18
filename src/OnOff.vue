<template>
    <div>
        <div id="on" @click="switched(true)" :class="{active: value}">Yes</div>

        <div id="off" @click="switched(false)" :class="{active: !value}">No</div>
    </div>
</template>

<script>
    export default {
        props: ['value'],
        methods: {
            switched(isOn){
                this.$emit('input', isOn)
            }
        }
    }
</script>

<style scoped>
    #on, #off {
        cursor: pointer;
    }

</style>
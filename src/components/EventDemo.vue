<template>
    <div>
    <h3>点击变色</h3>
    <button v-on:click="changecolor">改颜色</button>
    <p :style="{color:textcolor}">颜色改变</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            count: 0,
            textcolor: 'black'
        }
    },
    methods: {
        addcount() {
            this.count++
        },
        changecolor(){
            const colors = ['red', 'blue', 'green', 'yellow', 'purple'];
            this.textcolor = colors[Math.floor(Math.random() * colors.length)];
        }
    }
}
</script>

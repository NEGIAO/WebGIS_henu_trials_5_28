<script>
    export default{
        data(){
            return{
                flag:1,
                ok:"c",
                en:1,
                a:13
            }
        }
    }
</script>


<template>
    <h3>ifdemo</h3>
    <div v-if="flag">你好啊！</div>
    <div v-else>再见！</div>

    <div v-if="ok=='a'">条件a成立！</div>
    <div v-else-if="ok=='b'">条件b成立！</div>
    <div v-else-if="ok=='c'">条件c成立！</div>

    <div v-show="en">
        <p>这是一个v-show</p>
    </div>

    <div v-if="a%2==0">
        <p>这是一个v-if,判断a是偶数</p>
    </div>
    <div v-else="a%2!=0">
        <p>这是一个v-else,判断a是奇数</p>
    </div>
    
</template>

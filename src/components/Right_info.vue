<template>
    <div id="Title">
        这里是地环院的新闻哟！
    </div>
    <div id="text">
        你好，请你缩放到地环院，可以展示新闻
    </div>



    <br><br>
    <div d="trials">实验练习
        <h3>1、累加</h3>
        <button @click = "addcount('嗯，是的，你说的对')">累加事件的实现</button>
        <p>计数：{{ count }}</p>

        <h3>2、点击变色的事件</h3>
        <button @click = "changecolor">点击变色</button>
        <p :style="{color:textColor}">这是事件的响应者：{{ textColor }}</p>

        <h3>3、一个for迭代example</h3>
        <button @click = "addList" >  数据添加 </button>
        <p @click = "gerNameOfFruits(iten,$event)" v-for = "(iten,index) of fruits" :key = "index">这是联动的内容：{{ iten }}</p>
        <!-- v-for 指令用于遍历 fruits 数组，将每一项和索引返回到（），即iterm和index,且这两个名字可以自定义，并将每个元素显示在页面上 -->
    
    </div>



</template>

<script>


export default {
    data() {
        return {
            count: 0,
            textColor: 'black',
            colors: ['red', 'green', 'blue', 'yellow', 'purple', 'orange'],
            currentColorIndex: 0,
            fruits:["苹果","香蕉","梨子","其他水果"]
        };
    },
    methods: {
        addcount(msg) {
            this.count++;
            console.log(msg);
        },
        changecolor() {
            // 随机生成颜色
            //const color =["red", "green", "blue", "yellow", "purple", "orange"];
            //const randomColor = color[Math.floor(Math.random() * color.length)];
            //this.textColor = randomColor;
            //this.color = randomColor;
            this.currentColorIndex = (this.currentColorIndex + 1) % this.colors.length;
            this.textColor = this.colors[this.currentColorIndex];
            this.color = this.textColor;
            console.log("当前的颜色是：" + this.textColor);
        },
        gerNameOfFruits(msg,e){
            console.log("这是你单击的水果名字:" + msg);
            console.log("all right" + e)
        },
        addList(){
            this.fruits.push("这是新加入的水果");
            this.fruits = this.fruits.concat("这是新加入的水果2");
            //concat方法，连接并生成新的数组，
            // 这里赋值新的数组给原始数组内容，可以实现水果数组的更新
        }
    }
}


</script>

<style scoped>
#Title {
    position: relative;
    top: -10px;
    left: 10px;
    background-color: rgba(255, 255, 255, 0);
    padding: 1px;
    border-radius: 5px;
    font-size: 28px;
    color: #c10707;
}
#text {
    font-size: 20px;
    color: #000000;
}
#trials {
    position: relative;
    top: 10px;
    left: 10px;
    background-color: rgba(255, 255, 255, 0);
    padding: 1px;
    border-radius: 5px;
    z-index: 1000; /* 确保信息框在其他元素之上 */
    font-size: 20px;
    color: #c10707;
}
button{
    padding: 8px 16px;
    margin-bottom: 10px;
}
</style>
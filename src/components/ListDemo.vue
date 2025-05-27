<script>
export default{
    data(){
        return{
            items: [1,2,3,4,5],
            key_Value: {
                name: "小明",
                age: 18,
                gender: "男"
            },
            news: [
                { title: "新闻1", content: "内容1" ,id:1},
                { title: "新闻2", content: "内容2" ,id:2},
                { title: "新闻3", content: "内容3" ,id:3}
            ]
        }
    }
}
</script>

<template>
    <div>
        for循环中，列表和对象的使用<br>
        都用for来循环，for的语法是一样的<br>
        但是在对象中，for循环的语法是：<br>
        v-for="(value,key) in object"<br>
        括号中的顺序依次为值，键，索引值<br>
    </div>

    <p v-for="negiao in items">
        这是一个列表渲染的例子<br>{{negiao}}
    </p>

    <p v-for="(negiao,i) in items">
        这是一个列表渲染的例子<br>（当前值，索引值）名字可以自命名，索引从0开始<br>当前值：{{negiao}}<br>索引值是：{{i}}
    </p>

    <p v-for="value of key_Value">
        ok，返回键值对的所有value<br>{{ value }}
    </p>

    <ul>
        <li v-for="news in news">
            <h3>{{news.title}}</h3>
            <p>id:{{news.id}}<br>{{news.content}}</p>
        </li>
    </ul>
</template>
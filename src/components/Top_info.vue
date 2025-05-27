<template>
    <div class="top-bar">
        <h1>GIS---The science of where!</h1>
    </div>
</template>


<script>

</script>

<style scoped>
.top-bar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 60px;
    background: linear-gradient(90deg, #4ac54e, #2E7D32); /* 渐变背景 */
    color: white;
    display: flex;
    align-items: center;
    justify-content: center; /* 改为 center 而不是 space-between */
    padding: 0 20px;
    ;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2); /* 添加阴影 */
}
.top-bar h1 {
    margin: 0;
    font-size: 30px;
    font-weight: bold;
    font-family: 'Times New Roman', Times, serif;
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3); /* 添加文字阴影 */
}
</style>
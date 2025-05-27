<script setup>
import WebGIS from './components/WebGIS.vue';
import RightInfo from './components/Right_info.vue';
import Top_info from './components/Top_info.vue';
</script>

<template>
  <div class="main-container">
    <div class="top-container">
      <Top_info/>
    </div>
    <div class="content-row">
      <div class="map-container">
        <WebGIS/>
      </div>
      <div class="info-container">
        <RightInfo/>
      </div>
    </div>
  </div>
</template>

<style>
html, body {
    margin: 0;
    padding: 0;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 12px;
    color: #666666;
    background: #ffffff;
    height: 100%;
}
.main-container {
  display: flex;
  flex-direction: column;
  height: 100vh;
  width: 100vw;
  box-sizing: border-box;
  background: #368a3a9e;
}

.top-container {
  height: 56px;
  width: 100%;
  background: #f5f5f5;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 12px;
  font-size: 22px;
  font-weight: bold;
  letter-spacing: 2px;
  box-sizing: border-box;
  margin-bottom: 8px;
  position: relative;
    z-index: 10; /* 确保顶部信息栏在其他元素之上 */
}

.content-row {
  display: flex;
  flex: 1;
  width: 100%;
  gap: 10px;
}

.map-container {
  flex: 1;
  min-width: 600px;
  background: #e6f7ff;
  border-radius: 12px;
  position: relative;
  overflow: hidden;
  display: flex;
}

.info-container {
  width: 350px;
  background: #f5f5f5;
  padding: 24px 16px;
  box-sizing: border-box;
  border-radius: 12px;
  border-left: 2px solid #13af1077;
  overflow-y: auto;
  display: flex;
  flex-direction: column;
}
</style>

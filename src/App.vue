<script setup lang="ts">
import Generator from './components/Generator.vue'
</script>

<template>
  <html class="dark">
  <div class="common-layout">
    <el-container>
      <el-card shadow="always">
        <el-header>Halcyon Character Creator</el-header>
        <el-container>
          <el-aside width="400px">Character Viewer
            <el-image style="width: 400px; height: 150px" lazy
              src="https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg" fit="contain" />
          </el-aside>
          <el-main>
            <Generator msg="Halcyon Character Creator" />
          </el-main>
        </el-container>
      </el-card>
    </el-container>
  </div>

  </html>
</template>

<style scoped></style>

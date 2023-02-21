<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()
const gender = ref(0)
const bodyPath = ref(`/assets/body/bodies/${gender.value === 0 ? 'male' : 'female'}/idle/`)
const bodyString = bodyPath.value.toString()
const bodyImages = import(`${bodyString}`)
const headPath = ref(`/assets/head/human_${gender.value === 0 ? 'male' : 'female'}/idle/`)
const hairPath = ref('/assets/hair/')
const eyePath = ref(`/assets/eyes/${gender.value === 0 ? 'male' : 'female'}/`)
const bodyList = ref([]);
const headList = ref([]);
const hairList = ref([]);
const eyeList = ref([]);


console.log(await bodyImages)





</script>

<template>
  <el-col :gutter="1">
    Select a gender<br />
    <el-space size="large" spacer="|"></el-space>
    <el-radio-group v-model="gender">
      <el-radio :label="0">Male</el-radio>
      <el-radio :label="1">Female</el-radio>
    </el-radio-group>
  </el-col>
  <el-row :gutter="12">
    <el-col :span="6">

    </el-col>
  </el-row>
</template>



<style scoped>
.bottom {
  margin-top: 13px;
  line-height: 12px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>

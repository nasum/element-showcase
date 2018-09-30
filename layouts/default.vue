<template>
  <el-container>
    <el-header height="auto">
      <h1>Element Showcase</h1>
    </el-header>
    <el-container>
      <el-aside width="200px">
        <SideMenu/>
      </el-aside>
      <el-main>
        <nuxt/>
      </el-main>
    </el-container>
  </el-container>
</template>

<script>
import SideMenu from '@/components/SideMenu'

export default {
  components: {
    SideMenu
  }
}
</script>

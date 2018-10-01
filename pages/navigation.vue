<template>
  <el-container direction="vertical">
    <el-row>
      <el-col :span="24">
        <h1>Nav Menu</h1>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <h1>Tab</h1>
        <el-tabs v-model="activeTab">
          <el-tab-pane 
            label="タイムライン"
            name="first"
          >
            タイムライン
          </el-tab-pane>
          <el-tab-pane
            label="リプライ"
            name="second"
          >
            リプライ
          </el-tab-pane>
          <el-tab-pane
            label="ダイレクトメッセージ"
            name="third"
          >
            ダイレクトメッセージ
          </el-tab-pane>
        </el-tabs>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <h1>BreadCrumb</h1>
        <el-breadcrumb separator="/">
          <el-breadcrumb-item
          >
            記事
          </el-breadcrumb-item>
          <el-breadcrumb-item>
            Vue.js
          </el-breadcrumb-item>
          <el-breadcrumb-item>
            SingleFileComponent
          </el-breadcrumb-item>
        </el-breadcrumb>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <h1>Dropdown</h1>
        <el-dropdown
          trigger="click"
        >
          <span class="el-dropdown-link">
            メニュー
          </span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>Home</el-dropdown-item>
            <el-dropdown-item>設定</el-dropdown-item>
            <el-dropdown-item>ログアウト</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <h1>Step</h1>
        <el-steps
          :active="active"
          finish-status="success"
        >
          <el-step title="準備"/>
          <el-step title="待機"/>
          <el-step title="出撃"/>
        </el-steps>
      </el-col>
    </el-row>
  </el-container>
</template>

<script>
export default {
  data() {
    return {
      activeTab: '',
      active: 1
    }
  }
}
</script>

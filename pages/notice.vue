<template>
  <el-container direction="vertical">
    <el-row>
      <el-col :span="24">
        <h1>Alert</h1>
        <el-alert
          show-icon
          title="success"
          type="success"
          description="成功"
        />
        <br>
        <el-alert
          show-icon
          title="info"
          type="info"
          description="情報"
        />
        <br>
        <el-alert
          show-icon
          title="warning"
          type="warning"
          description="警告"
        />
        <br>
        <el-alert
          show-icon
          title="error"
          type="error"
          description="エラー"
        />
        <br>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <el-container
          v-loading="true"
        >
          <el-header style="background-color: #409EFF;">
            <h1>el-header</h1>
          </el-header>
          <el-container>
            <el-aside 
              width="200px" 
              style="background-color: #CEFFAE;"
            >
              el-aside
            </el-aside>
            <el-main style="background-color: #FFAEF3;">
              el-main
            </el-main>
          </el-container>
          <el-footer style="background-color: #409EFF;">
            el-footer
          </el-footer>
          <br>
        </el-container>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <el-button 
          :plain="true" 
          @click="open"
        >
          メッセージを表示
        </el-button>
        <br>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <el-button @click="openAlertMessageBox">
          アラートメッセージボックスを表示
        </el-button>
        <br>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <el-button
          @click="openNotification">
          Notificationを表示
        </el-button>
      </el-col>
    </el-row>
  </el-container>
</template>

<script>
export default {
  methods: {
    open() {
      this.$message({ message: 'メッセージの表示', duration: 0 })
    },
    openAlertMessageBox() {
      this.$alert('メッセージ本文', 'メッセージタイトル', {
        confirmButtonText: 'OK',
        callback: action => {
          this.$message({
            type: 'info',
            message: `action: ${action}`
          })
        }
      })
    },
    openNotification() {
      this.$notify({
        title: 'Notification',
        message: '本文',
        duration: 0
      })
    }
  }
}
</script>

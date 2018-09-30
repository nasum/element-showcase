<template>
  <el-container direction="vertical">
    <el-row>
      <el-col :span="24">
        <h1>レイアウト関連のコンポーネント</h1>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <h1>コンテナ</h1>
        コンテナコンポーネントはページの基本的な構造を決定します。
        <el-container>
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
        </el-container>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <h1>レイアウト</h1>
        <el-container>
          <el-main>
            <el-row style="background-color: #FFAEF3;">
              el-row
            </el-row>
            <el-row>
              <el-col 
                :span="6" 
                style="background-color: #FFDDAE;"
              >
                el-col
              </el-col>
              <el-col 
                :span="6"
                style="background-color: #8CFF40;"
              >
                el-col
              </el-col>
              <el-col 
                :span="6" 
                style="background-color: #FFDDAE;"
              >
                el-col
              </el-col>
              <el-col
                :span="6"
                style="background-color: #8CFF40;"
              >
                el-col
              </el-col>
            </el-row>
          </el-main>
        </el-container>
      </el-col>
    </el-row>
  </el-container>
</template>

<script>
export default {}
</script>

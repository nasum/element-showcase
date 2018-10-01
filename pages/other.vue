<template>
  <el-container direction="vertical">
    <el-row>
      <el-col :span="24">
        <h1>Dialog</h1>
        <el-button
          @click="dialogVisible = true"
        >
          ダイアログを開く
        </el-button>
        <el-dialog
          :visible.sync="dialogVisible"
          title="タイトル"
          width="30%"
        >
          <span>ダイアログの内容</span>
        </el-dialog>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <h1>Tooltip</h1>
        <el-tooltip
          effect="dark"
          content="ツールチップ"
          placement="top-start"
        >
          <el-button>ツールチップの表示</el-button>
        </el-tooltip>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <h1>Popover</h1>
        <el-popover
          placement="top-start"
          title="タイトル"
          width="200"
          trigger="hover"
          content="内容"
        >
          <el-button slot="reference">Popover</el-button>
        </el-popover>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <h1>Card</h1>
        <el-card class="box-card">
          <div
            slot="header"
            class="clearfix"
          >
            <span>Card Header</span>
          </div>
          <div>
            Cardの内容
          </div>
        </el-card>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <h1>Carousel</h1>
        <el-carousel height="150px">
          <el-carousel-item
            v-for="item in 4"
            :key="item"
          >
            <h3>アイテムの内容：{{ item }}</h3>
          </el-carousel-item>
        </el-carousel>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <h1>Collapse</h1>
        <el-collapse v-model="activeNames">
          <el-collapse-item
            title="Collapse1"
            name="1"
          >
            内容１
          </el-collapse-item>
          <el-collapse-item
            title="Collapse2"
            name="2"
          >
            内容２
          </el-collapse-item>
        </el-collapse>
      </el-col>
    </el-row>
  </el-container>
</template>

<script>
export default {
  data() {
    return {
      dialogVisible: false,
      activeNames: ''
    }
  }
}
</script>

<style>
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}
.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
</style>

<template>
  <el-container direction="vertical">
    <el-row>
      <el-col :span="24">
        <h1>Table</h1>
        <el-table
          :data="tableData"
          style="width: 100%"
        >
          <el-table-column
            prop="type"
            label="型"
            width="180"
          />
          <el-table-column
            prop="name"
            label="艦名"
            width="180"
          />
          <el-table-column
            prop="completion"
            label="竣工"
          />
        </el-table>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <h1>Tag</h1>
        <el-tag>吹雪</el-tag>
        <el-tag type="success">白雪</el-tag>
        <el-tag type="info">初雪</el-tag>
        <el-tag type="warning">深雪</el-tag>
        <el-tag type="danger">叢雲</el-tag>
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <h1>Progress</h1>
        <el-progress :percentage="70"/>
        <el-progress 
          :percentage="100"
          status="success"
        />
        <el-progress
          :percentage="10"
          status="exception"
        />
        <el-progress
          :percentage="50"
          type="circle"
        />
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <h1>Tree</h1>
        <el-tree 
          :data="data"
          :props="defaultProps"
        />
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <h1>Pagination</h1>
        <el-pagination
          :total="50"
          layout="prev, pager, next"
        />
        <el-pagination
          :total="100"
          background
          layout="prev, pager, next"
        />
      </el-col>
    </el-row>
    <el-row>
      <el-col>
        <h1>Badge</h1>
        <el-badge 
          :value="100"
          class="item"
        >
          <el-button>comments</el-button>
        </el-badge>
        <br>
        <br>
        <el-badge 
          value="new" 
          class="item"
        >
          <el-button>comments</el-button>
        </el-badge>
        <br>
        <br>
        <el-badge
          is-dot
          class="item"
        >
          <el-button>comments</el-button>
        </el-badge>
      </el-col>
    </el-row>
  </el-container>
</template>

<script>
export default {
  data() {
    return {
      tableData: [
        {
          type: '吹雪型',
          name: '吹雪',
          completion: '1928年8月10日'
        },
        {
          type: '暁型',
          name: '響',
          completion: '1933年3月31日'
        },
        {
          type: '暁型',
          name: '電',
          completion: '1932年11月15日'
        }
      ],
      data: [
        {
          label: '戦艦',
          children: [
            {
              label: '金剛型',
              children: [
                {
                  label: '金剛'
                },
                {
                  label: '比叡'
                },
                {
                  label: '榛名'
                },
                {
                  label: '霧島'
                }
              ]
            },
            {
              label: '長門型',
              children: [
                {
                  label: '長門'
                },
                {
                  label: '陸奥'
                }
              ]
            }
          ]
        }
      ]
    }
  }
}
</script>

<template>
  <el-container direction="vertical">
    <el-row>
      <el-col :span="24">
        <h1>ボタンコンポーネント</h1>
      </el-col>
    </el-row>
    <el-row style="margin-bottom: 10px;">
      <el-col :span="24">
        <el-button>Default</el-button>
        <el-button type="primary">Primary</el-button>
        <el-button type="success">Success</el-button>
        <el-button type="info">Info</el-button>
        <el-button type="warning">Warning</el-button>
        <el-button type="danger">Danger</el-button>
      </el-col>
    </el-row>
    <el-row style="margin-bottom: 10px;">
      <el-col :span="24">
        <el-button plain>Plain</el-button>
        <el-button 
          type="primary" 
          plain>
          Primary
        </el-button>
        <el-button 
          type="success" 
          plain
        >
          Success
        </el-button>
        <el-button 
          type="info" 
          plain
        >
          Info
        </el-button>
        <el-button 
          type="warning" 
          plain
        >
          Warning
        </el-button>
        <el-button 
          type="danger" 
          plain
        >
          Danger
        </el-button>
      </el-col>
    </el-row>
    <el-row style="margin-bottom: 10px;">
      <el-col :span="24">
        <el-button round>Round</el-button>
        <el-button 
          type="primary" 
          round
        >
          Primary
        </el-button>
        <el-button 
          type="success" 
          round
        >
          Success
        </el-button>
        <el-button 
          type="info" 
          round
        >
          Info
        </el-button>
        <el-button 
          type="warning" 
          round
        >
          Warning
        </el-button>
        <el-button 
          type="danger" 
          round
        >
          Danger
        </el-button>
      </el-col>
    </el-row>
    <el-row style="margin-bottom: 10px;">
      <el-col :span="24">
        <el-button
          icon="el-icon-search" 
          circle
        />
        <el-button
          type="primary" 
          icon="el-icon-edit" 
          circle
        />
        <el-button
          type="success" 
          icon="el-icon-check" 
          circle
        />
        <el-button
          type="info" 
          icon="el-icon-message" 
          circle
        />
        <el-button
          type="warning" 
          icon="el-icon-star-off" 
          circle
        />
        <el-button
          type="danger" 
          icon="el-icon-delete" 
          circle
        />
      </el-col>
    </el-row>
  </el-container>
</template>

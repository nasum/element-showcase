<template>
  <el-container direction="vertical">
    <el-row>
      <el-col :span="24">
        <h1>Formに関するコンポーネント</h1>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <h1>Radio</h1>
        <el-row>
          <el-col>
            <el-radio-group v-model="radio1">
              <el-radio
                label="大和">大和</el-radio>
              <el-radio
                label="武蔵">武蔵</el-radio>
            </el-radio-group>
            <br>
            <el-radio-group v-model="radio2">
              <el-radio-button label="金剛"/>
              <el-radio-button label="比叡"/>
              <el-radio-button label="榛名"/>
              <el-radio-button label="霧島"/>
            </el-radio-group>
            <br>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <h1>Checkbox</h1>
            <el-row>
              <el-col>
                <el-checkbox-group v-model="checkList1">
                  <el-checkbox label="吹雪"/>
                  <el-checkbox label="白雪"/>
                  <el-checkbox label="初雪"/>
                  <el-checkbox label="深雪"/>
                  <el-checkbox label="叢雲"/>
                </el-checkbox-group>
                <br>
                <el-checkbox-group v-model="checkList2">
                  <el-checkbox-button label="綾波"/>
                  <el-checkbox-button label="敷浪"/>
                  <el-checkbox-button label="朝霧"/>
                  <el-checkbox-button label="夕霧"/>
                  <el-checkbox-button label="天霧"/>
                  <el-checkbox-button label="狭霧"/>
                </el-checkbox-group>
              </el-col>
            </el-row>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <h1>Input</h1>
            <el-row>
              <el-col>
                <el-input
                  v-model="input1"
                  placeholder="input1"
                />
                <el-input
                  v-model="input3"
                  :rows="2"
                  type="textarea"
                  placeholder="input3"
                />
                <el-autocomplete
                  v-model="input4"
                  :fetch-suggestions="querySearchAsync"
                  placeholder="input4"
                />
              </el-col>
            </el-row>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <h1>InputNumber</h1>
            <el-row>
              <el-col>
                <el-input-number
                  v-model="num1"
                  :min="1"
                  :max="10"
                />
                <el-input-number
                  v-model="num2"
                  :min="1"
                  :max="10"
                  controls-position="right"
                />
              </el-col>
            </el-row>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <h1>Select</h1>
            <el-select
              v-model="select"
              placeholder="川内型"
            >
              <el-option
                v-for="item in options"
                :key="item.value"
                :label="item.label"
                :value="item.value"
              />
            </el-select>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <h1>cascade</h1>
            <el-cascader
              :options="cascadeOptions"
              v-model="cascade"
            />
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <h1>Switch</h1>
            <el-switch v-model="switch1"/>
            <el-switch
              v-model="switch2"
              active-color="#13ce66"
              inactive-color="#ff4949"/>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <h1>Slider</h1>
            <el-slider v-model="slider1"/>
            <el-slider
              v-model="slider2"
              vertical
              height="200px"/>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <h1>TimePicker</h1>
            <el-time-select
              v-model="time1"
              :picker-options="{
                start: '08:30',
                step: '00:15',
                end: '18:30'
              }"
              placeholder="Time"
            />
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <h1>DatePickar</h1>
            <el-date-picker
              v-model="date1"
              type="date"
              placeholder="date"
            />
            <br>
            <el-date-picker
              v-model="date2"
              type="daterange"
              range-separator="To"
              start-placeholder="Start"
              end-placeholder="End"
            />
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <h1>upload</h1>
            <el-upload
              :limit="3"
              :on-exceed="handleExceed"
              :file-list="fileList"
              class="upload-demo"
              multiple>
              <el-button
                size="small"
                type="primary"
              >
                Click to upload
              </el-button>
            </el-upload>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <h1>Rate</h1>
            <el-rate v-model="rate1"/>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <h1>Color Picker</h1>
            <el-color-picker v-model="color1"/>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <h1>Transfer</h1>
            <el-transfer
              v-model="transfer1"
              :data="data"
            />
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <h1>Form</h1>
            <el-form 
              :inline="true"
              :model="form"
            >
              <el-form-item label="姓">
                <el-input
                  v-model="form.last"
                  placeholder="鈴木"
                />
              </el-form-item>
              <el-form-item label="名">
                <el-input
                  v-model="form.first"
                  placeholder="太郎"
                />
              </el-form-item>
              <el-form-item>
                <el-button type="primary">送信</el-button>
              </el-form-item>
            </el-form>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            a　
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            a
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            a　
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            a
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            a　
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            a
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            a　
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            a
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            a　
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            a
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            a　
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            a
          </el-col>
        </el-row>
      </el-col>
    </el-row>
  </el-container>
</template>
<script>
export default {
  data() {
    return {
      radio1: '',
      radio2: '',
      checkList1: [],
      checkList2: [],
      input1: '',
      input2: '',
      input3: '',
      input4: '',
      links: [],
      num1: 0,
      num2: 0,
      options: [
        {
          value: '川内',
          label: '川内'
        },
        {
          value: '神通',
          label: '神通'
        },
        {
          value: '那珂',
          label: '那珂'
        }
      ],
      select: '',
      cascadeOptions: [
        {
          value: '重巡洋艦',
          label: '重巡洋艦',
          children: [
            {
              value: '利根型',
              label: '利根型',
              children: [
                { value: '利根', label: '利根' },
                { value: '筑摩', label: '筑摩' }
              ]
            },
            {
              value: '妙高型',
              label: '妙高型',
              children: [
                { value: '妙高', label: '妙高' },
                { value: '那智', label: '那智' },
                { value: '足柄', label: '足柄' },
                { value: '羽黒', label: '羽黒' }
              ]
            }
          ]
        }
      ],
      switch1: true,
      switch2: true,
      slider1: 0,
      slider2: 0,
      time1: '',
      date1: '',
      date2: '',
      fileList: [
        { name: 'photo01.jpeg', url: '' },
        { name: 'photo02.jpeg', url: '' }
      ],
      rate1: 0,
      color1: '',
      data: [
        { key: 0, label: '島風' },
        { key: 1, label: '天津風' },
        { key: 2, label: '時津風' },
        { key: 3, label: '雪風' }
      ],
      transfer1: [],
      form: {}
    }
  },
  mounted() {
    this.links = this.loadAll()
  },
  methods: {
    loadAll() {
      return [{ value: 'hoge' }, { value: 'huga' }]
    },
    querySearchAsync(queryString, cb) {
      var links = this.links
      var results = queryString
        ? links.filter(this.createFilter(queryString))
        : links
      cb(results)
    },
    createFilter(queryString) {
      return link => {
        return link.value.toLowerCase().indexOf(queryString.toLowerCase()) === 0
      }
    }
  }
}
</script>

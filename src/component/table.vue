<template>
  <div>
    <el-row>
      <el-col :span="18" :offset="3">
        <el-table
          :data="books"
          style="width: 100%">
          <el-table-column
            prop="id"
            label="序号">
          </el-table-column>
          <el-table-column
            prop="name"
            label="书名">
          </el-table-column>
          <el-table-column
            prop="author"
            label="作者">
          </el-table-column>
          <el-table-column
            prop="price"
            label="价格">
          </el-table-column>
        </el-table>
      </el-col>
    </el-row>
    <button @click="getme">点击获取数据</button>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        books:[]
      }
    },
    methods:{
      getme:function () {
        this.axios.get('http://www.cyydit.club/data.php').then((res)=>{
          console.log(res.data.content)
          let data = res.data.content
          this.books=data
        })
      }
    }
  }
</script>

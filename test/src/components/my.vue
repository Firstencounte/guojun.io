
<template>
<div    id="app1">
    <input type="text" v-model="inputValue">
    <button @click="xg">修改名字</button>
  <div class="one">
      <ul>
          <li class="name">
              {{item1s}}
          </li>
      </ul>
    </div>
    <div class="one">
      <ul>
          <li v-for="item in item2s">
              {{item}}
          </li>
      </ul>
    </div>
    <div class="kecheng">
        <span class="title">主修课程</span>
        <pre> 
            {{pre1}}
        </pre>
    </div>
    <div class="kecheng">
        <span class="title">获奖荣誉</span>
        <pre v-for="pre2 in pre2s">
            {{pre2}}
        </pre>
    </div>
    <div class="kecheng">
        <span class="title">在校经历</span>
        <pre v-for="pre3 in pre3s">
            {{pre3}}

        </pre>
    </div>
</div>
</template>

<script>
export default {
  name: 'app1',
  data(){
      return {
          inputValue:"",
          item1s:"郭俊",
          item2s:[
              "求职意向:web前端",
              "电话：13113981593",
              "邮箱：596278576@qq.com"
              ],
           pre1:"C语言、数据库原理、网站性能优化和安全维护、ASP.net信息系统开发、php、小程序、ps、vue、web前端、bootstrap、thinkphp5、layui",
           pre2s:[
               "2018年6月13日	广州城建技工学校第五届校园技能节网站设计与开发比赛优秀奖",
               "2017-2018年软件技术开发社团“优秀干事",
               "2017-2018学年“一等奖”奖学金",
               "2018-2019广州城建技工学校抖音大赛“优秀奖”",
               "2018年5月8日	北大青鸟2018年“平面网页设计大赛”全国一等奖",
                "2017-2018 荣获“北大青鸟专业奖学金“",
                "2019年5月荣获“第六届校园技能节创新创业大赛一等奖”"
           ],
           pre3s:[
               "担任“软件技术开发社团”副社长",
               "担任班级宣传委员",
               "担任机信学生会宣传部副部长"
           ]       
      }
    
  },
  methods:{
      xg:function(){
          this.item1s=this.inputValue
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
    li{
        list-style: none;
        float: left;
        margin-left: 150px;
        
    }
    .one{
        overflow:hidden;
        margin: 0 10%;
    }
    .kecheng{
        margin:40px 0 0 0;
        overflow: hidden;
        
    }
    .name,.title{
        font-size: 36px;
        color:cornflowerblue;
       
    }
    input{
        padding: 2px;
    }
</style>

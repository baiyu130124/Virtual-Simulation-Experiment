<template>


    <!-- <span> {{ test }}</span> -->
    <h2>一、实验目的  </h2>
    <p class="content">理解软件项目规模度量功能点法原理，通过实验操作掌握功能点法。
      学生应以小组为单位，根据本小组“软件工程管理与经济”课程设计项目架构及组件等设计成果，
      以功能点方法测量该项目的规模(功能点数量)。 建议选用某一种功能点方法度量课程设计项目的功能点，
      并采用另外一种功能点方法或其他的软件规模度量方法对前一种方法的度量结果进行验证。
      本实验为课内设计性实验项目，实验学时 1 学时，完成实验报告 1 学时。
    </p>
    <h2>二、实验原理  </h2>
    <p class="secondtitle">第一步：确定计数的视角和目的</p>
    <p class="content">确定功能点计数的视角方便了后续计数边界的确定。下面是三种常用的视角————<br />
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.项目视角：为了确定以软件开发项目形式所要交付功能的规模，计数的目的是要利用功能
      规模测量结果来评估项目开发生产率，
      或者估算开发项目工作量。在此情况下，边界通过项目用户的功能需求范围来确定；<br />
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.业务视角： 为了确定支持特定商业功能领域的应用程序的全部软件功能规模，
      这些商业功能由一个业务主管所领导的一一个组织(业务团队)来管理，计数的目的是想要跟踪每年变化的业务领域功能需求，
      或者是评估业务团队对整个领域的支撑工作生产率。在此情况下，边界通过业务团队支撑的功能范围来确定；<br />
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.企业视角：为了对企业进行资产评估而确定企业应用程序功能组合的规模。在此情况下，
      边界
      通过企业的整个应用程序功能组合来确定。
    <br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;详见实验指导书，以实验指导书为准。
   </p>

    <p class="secondtitle">第二步：确定计数的边界和接口</p>
    <p class="content">绘制FP计数申请的边界取决于计数的意图观点，目的和用途。绘制边界将确定将在计数中包含哪些功能，
      以及排除哪些功能。当绘制应用程序边界时，它定义了软件和“用户”之间的概念边界。<br />
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;来自用户的“输入数据”越过边界进入应用程序。 “输出数据”离开了应用程序，并越过边界
      到达了用户那里。
      在边界内是数据实体类型（为简单起见，以下简称“实体”） ，它们由应用程序的逻辑事务类型（以下简称“逻辑事务”或简称“ 事务”）
      处理。
      <br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;当为特定的FP计数而绘制应用程序边界时，它可能会导致识别到其他 应用程序的
      “接口”。在一般的理解中，“接口”这个词用于两个物
      理上不同的进程。两种类型的接口：
      <br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.“数据”文件（如主数据记录、“事务”、一串消息等）可以作为接口文件从一个
      应用程序与另一个应用程序共享。
      <br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.“数据”通过一个接口，一次一个或一批，从一个应用程序传输到另一个应用程序
    <br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;详见实验指导书，以实验指导书为准。
    </p>
    <p class="secondtitle">第三步：识别逻辑事务，对数据实体类型进行识别和分类，计算输入数据元素类型、所引用的数据实体类型和输出数据元素类型。</p>
    <p class="content">逻辑事务是软件应用程序支持的最低级别的业务流程。每个逻辑事务包括三个元素：跨应用程序边界的输入、
      一些相关的处理和跨应用程序边界的输出<br />
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在识别逻辑事务集时，考虑以下问题：
      <br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;“谁在使用它呢？”
      <br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; “为什么还需要它呢？”
      <br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;“它是做什么的？”
      <br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;“它是什么时候启动的？”
      <br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;“它与其他逻辑事务有何不同？”

      <br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;实体类型是业务用户在现实世界中想要保存信息的某种东西（严格地说，
      是某种类型的东西）。数据元素类型保存有关实体类型的信息。例如：·“员工”将是一个人事系统中的一个实体类型。识别并
      对数据实体类型进行分类有助于我们对每个逻辑事务的分析以及其三元素的识别分析。
      <br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 每个逻辑事务都由输入、流程和输出三个元素组成。 MkII FPA对这三个元素
      的功能大小做出了以下基本假设：
      输入元素的大小与构成事务输入侧的唯一处理数据元素类型（“DET’s”）的数量成正比；
      处理元素的大小与逻辑事务过程中引用的数据实体类型（或“实体”）的数量成正比；
      输出元素的大小与组成事务输出端的唯一处理DET的数量成正比。

      MkII FPA的一个约定是，每个逻辑事务必须至少有一个输入数据元素类型，必须对一个实体类型进行一个引用，
      并且必须有一个输出数据元素类型。
      提供这三种不同类型的信息处理所涉及的功能都是不同的。因此，在MkII FPA中，使用了三个加权因子，
      使这三种功能能够组合为一个功能大小的单个值。（权重已根据分析、设计、编程、测试、实施这些组件的行业平均相对工作量，
      以便MkII FP功能规模量表为这些活动提供工作产出的行业平均相对度量。）
      对于每个逻辑事务，计算输入数据元素类型的数量（Ni）、引用的数据实体类型的数量（Ne）以及输出数据元素类型的数量（No）。


    <br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;详见实验指导书，以实验指导书为准。
    </p>


    <p class="secondtitle">第四步：计算功能规模</p>
    <p class="content">功能大小（FPI,Function Point Index）是所有逻辑事务、输入数据元素类型（Ni）、引用的数据实体类型（Ne）
    和输出数据元素类型（No）的事务的加权和。因此，一个应用程序的FPI是：FPI = Wi * ∑Ni + We * ∑Ne + Wo * ∑No。
    其中“∑”表示所有逻辑事务的总和，每个输入数据元素类型、数据实体类型引用和输出数据元素类型的行业平均权重分别为：
    Wi = 0.58,
    We = 1.66,
    Wo = 0.26。

    <br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;详见实验指导书，以实验指导书为准。
    </p>

    <p class="secondtitle">第五步：评估每个技术复杂性调整特性的影响程度，并计算调整后的规模</p>
    <p class="content">
      除了信息处理规模之外，FPA还提供了一种考虑到应用程序 的技术复杂性和某些质量要求的方法。
      这些需求有时被称为“非功能性需求”。当FPI乘以技术复杂性调整时，结果称为调整函数点指数。
      该方法试图在0到5的范围内测量19个（或更多）技术特征对应用规模的影响。
      所有特征的和被用来计算要应用的因子。这个因素被称为技术复杂性调整（TCA）。
      如果这19个（或更多）特征中的每个特征的得分的总数被称为总影响度（TDI）
      即要求从数据流，分布式功能，性能等20个技术中挑选19个，并为其复杂度调整特性的影响程度打分，
      0~5表示影响程度由小到大。
      TCA =（TDI * C）+0.65，其中当前行业平均值C为0.005。因此，TCA可以在0.65到1.15之间变化（
      如果所有的特征分别有最小或最大的影响）。调整后的功能点计算表示为： AFPI = FPI * TCA，
      其中AFPI =调整后的功能点指数，FPI =功能点指数，TCA =技术复杂性调整。
    <br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;详见实验指导书，以实验指导书为准。
    </p>
   <h2>三. 实验步骤 </h2>
  <p class="secondtitle">第一步：计算输入数据元素类型Input Types个数，引用的数据实体类型Entity References个数，
    引用的数据实体类型Entity References个数，填写到表一。（其中FUNCTION CHANGED与FUNCTION DELETED两类的三个个数可填为0。）</p>
  <br />
  <h4 style="text-align: center;">表1：功能点分析-总体总结和汇总 </h4>
  <a-table :pagination="false" :columns="columns" :data-source="tableData" bordered size="middle" style="word-break: break-all;">
    <template #bodyCell="{ column, record, index }">
      <template v-if="column.dataIndex === 'A'">
        <a-input v-model:value="record.A" style="width:100px; " />
      </template>
      <template v-if="column.dataIndex === 'D'">
        <a-input v-model:value="record.D" style="width:100px;" />
      </template>
      <template v-if="column.dataIndex === 'G'">
        <a-input v-model:value="record.G" style="width:100px;" />
      </template>
      <template v-if="column.dataIndex === 'C'">
        {{ c(index) }}
      </template>
      <template v-if="column.dataIndex === 'F'">
        {{ f(index) }}
      </template>
      <template v-if="column.dataIndex === 'I'">
        {{ i(index) }}
      </template>
      <template v-if="column.dataIndex === 'unchanged'">
        {{ unchanged(index) }}
      </template>
    </template>
    <br /><br />
  </a-table>
  <br /><br />
  <p class="secondtitle">第二步：计算调整前的功能大小FPI</p>
  <br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;根据公式FPI = Wi * ∑Ni + We * ∑Ne + Wo * ∑No
  可得，本实验未调整功能大小FPI计算表示为
  <span style="font-size:20px">{{SUM}}</span>
  <br>
  <br /><br />

  <p class="secondtitle">第三步：技术复杂性调整，在 0到5的范围内测量19个（或更多）技术特征对应用规模的影响。
    即要求从数据流，分布式功能，性能等20个技术中挑选19个，并为其复杂度调整特性的影响程度打分，
    0~5表示影响程度由小到大，填写表二。</p>
  <br />
  <h4 style="text-align: center;">表2：功能点分析-技术复杂性调整 </h4>
  <a-table :columns="columnsadjust" :pagination="false" :data-source="dataadjust" bordered size="middle" style="word-break: break-all;">
    <template #bodyCell="{ column, record }">
      <template v-if="column.dataIndex === 'grade'">
        <a-input-group compact>
          <a-select v-model:value="record.grade">
            <a-select-option value="0">0</a-select-option>
            <a-select-option value="1">1</a-select-option>
            <a-select-option value="2">2</a-select-option>
            <a-select-option value="3">3</a-select-option>
            <a-select-option value="4">4</a-select-option>
            <a-select-option value="5">5</a-select-option>
          </a-select>

        </a-input-group>

      </template>
    </template>
  </a-table>
  <br />
  <br /><br />

  <p class="secondtitle">第四步：计算技术复杂性调整（TCA）</p>

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;19个（或更多）特征中的每个特征的得分的总数,即总影响度TDI：
  <span style="font-size:20px">{{TDL}}</span>
  <br />
  <p class="secondtitle">第五步：计算总影响度（TDI）</p>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;TCA =（TDI * C）+0.65，其中当前行业平均值C为0.005。因此，TCA可以在0.65到1.15之间变化
  。技术复杂性调整TCA为：
  <span style="font-size:20px"> {{TCA}}</span>
  <br />
  <p class="secondtitle">第六步：计算调整后的功能点指数（AFPI）</p>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;AFPI = FPI * TCA，
      AFPI =调整后的功能点指数，FPI =功能点指数，TCA =技术复杂性调整。调整后的功能点计算AFPI表示为：
  <span style="font-size:20px">{{AFPI}}  </span>

  <br /><br />

  <p class="secondtitle">第七步：根据生产率计算项目工作量</p>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;项目工作量 Project Effort = AFPI * Productivity，
  Productivity生产率默认为 10 人时/功能点。所以项目工作量 Project Effort=
  <span style="font-size:20px">{{ PE}}  人时</span>
  <br />
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;则此部分资金成本为<span style="font-size:20px">{{MONEY}}   </span>元，默认每人时的花费为50元.



  <br /><br />
  <h2>四. 实验心得 </h2>
<textarea  class="textareac"></textarea>

  <br />
  <a-button class="button3" type="primary" shape="round">
    <template #icon>
      <DownloadOutlined />
    </template>实验报告提交
  </a-button>




</template>

<script>
import { Document } from '@element-plus/icons-vue'
import { defineComponent } from 'vue'
export default {

  setup() {
    return {
      value,
      data,
      columns,
    }
  },
  name: 'Exp1_MARKII',
  data() {
    return {
      test: '21111',
      SUM: 0,
      TDL: 0,
      columns: [
        {
          title: '逻辑事务',
          dataIndex: 'component',
          key: 'component',
          align: 'center'
          // width: 30,
          // fixed: 'left',
        },

        {
          title: '逻辑事务汇总',
          children: [
            {
              title: 'FUNCTION ADDED',
              align: 'center',
              children: [{
                title: '计数',
                align: 'center',
                children: [{
                  title: 'A',
                  // width: 30,
                  dataIndex: 'A',
                  align: 'center'
                }],
              },
                {
                  title: '权重',
                  align: 'center',
                  children: [{
                    title: 'B',
                    dataIndex: 'B',
                    align: 'center',
                    // width: 30,
                  }],
                },
                {
                  title: '功能点数',
                  align: 'center',
                  children: [{
                    title: 'C=A*B',
                    align: 'center',
                    dataIndex: 'C',
                    // width: 30,
                  }],
                }
              ],
            },
            {
              title: 'FUNCTION CHANGED',
              align: 'center',
              children: [{
                title: '计数', children: [{
                  align: 'center',
                  dataIndex: 'D',
                  title: 'D',
                  // width: 30,
                }],
              },
                {
                  title: '权重',
                  align: 'center',
                  children: [{
                    dataIndex: 'E',
                    align: 'center',
                    title: 'E',
                    // width: 30,
                  }],
                },
                {
                  title: '功能点数',
                  align: 'center',
                  children: [{
                    dataIndex: 'F',
                    title: 'F=D*E',
                    align: 'center',
                    // width: 30,
                  }],
                }],
            },
            {
              title: 'FUNCTION DELETED',
              align: 'center',
              children: [{
                title: '计数',
                align: 'center',
                children: [{
                  dataIndex: 'G',
                  align: 'center',
                  title: 'G',
                  // width: 30,
                }],
              },
                {
                  title: '权重',
                  align: 'center',
                  children: [{
                    dataIndex: 'H',
                    align: 'center',
                    title: 'H',
                    // width: 30,
                  }],
                },
                {
                  title: '功能点数',
                  align: 'center',
                  children: [{
                    dataIndex: 'I',
                    title: 'I=G*H',
                    align: 'center',
                    // width: 30,
                  }],
                }],
            },

          ]
        },
        {
          title: '未调整功能点数',
          dataIndex: 'unchanged',
          key: 'unchanged',
          align: 'center',
          // width: 800,
          // fixed: 'right',
        },
      ],
      columnsadjust: [
        {
          title: '序号',
          dataIndex: 'index',
          key: 'component',
          align: 'center',
          width: 100
          // fixed: 'left',
        },
        {
          title: '技术名称',
          dataIndex: 'title',
          key: 'component',
          align: 'center',
          width: 900,
          // fixed: 'left',
        },
        {
          title: '影响程度',
          dataIndex: 'grade',
          key: 'component',
          align: 'center'
          // width: 30,
          // fixed: 'left',
        },
      ],
      tableData: [
        {
          component: 'Input Types',
          A: '',
          B: '0.58',
          C: '',
          D: '',
          E: '1.66',
          F: '',
          G: '',
          H: '0.26',
          I: '',
          unchanged: '',
        },
        {
          component: 'Entity References',
          A: '',
          B: '0.58',
          C: '',
          D: '',
          E: '1.66',
          F: '',
          G: '',
          H: '0.26',
          I: '',
          unchanged: '',
        },
        {
          component: 'Output Types',
          A: '',
          B: '0.58',
          C: '',
          D: '',
          E: '1.66',
          F: '',
          G: '',
          H: '0.26',
          I: '',
          unchanged: '',
        },

      ],
      dataadjust: [
        {
          index: '1',
          title: 'Data Communications ',
          grade: ''

        },
        {
          index: '2',
          title: 'Distributed Function',
          grade: ''

        },
        {
          index: '3',
          title: 'Performance',
          grade: ''

        },
        {
          index: '4',
          title: 'Heavily Used Configuration',
          grade: ''

        },
        {
          index: '5',
          title: 'Transaction Rates',
          grade: ''

        },
        {
          index: '6',
          title: 'On-Line Data Entry ',
          grade: ''

        },
        {
          index: '7',
          title: 'Design for End-User Efficiency ',
          grade: ''

        },
        {
          index: '8',
          title: 'On-Line Update ',
          grade: ''

        },
        {
          index: '9',
          title: 'Complexity of Processing ',
          grade: ''

        },
        {
          index: '10',
          title: 'Usable in Other Applications ',
          grade: ''

        },
        {
          index: '11',
          title: 'Installation Ease ',
          grade: ''

        },
        {
          index: '12',
          title: 'Operations Ease ',
          grade: ''

        },
        {
          index: '13',
          title: 'Multiple Sites ',
          grade: ''

        },
        {
          index: '14',
          title: 'Facilitate Changes',
          grade: ''

        },
        {
          index: '15',
          title: 'Requirements of Other Applications',
          grade: ''

        },
        {
          index: '16',
          title: 'Security, Privacy and Auditability',
          grade: ''

        },
        {
          index: '17',
          title: 'User Training Needs',
          grade: ''

        },
        {
          index: '18',
          title: 'Direct use by Third Parties',
          grade: ''

        },
        {
          index: '19',
          title: 'Documentation',
          grade: ''

        },
        {
          index: '20',
          title: 'User Defined Characteristics',
          grade: ''

        },


      ]
    }
  },
  computed: {
    c() {
      return function (index) {
        this.tableData[index].C = (parseFloat(this.tableData[index].A) ? parseFloat(this.tableData[index].A) : 0) * parseFloat(this.tableData[index].B)
        return this.tableData[index].C.toFixed(2)
      }
    },
    f() {
      return function (index) {
        this.tableData[index].F = (parseFloat(this.tableData[index].D) ? parseFloat(this.tableData[index].D) : 0) * parseFloat(this.tableData[index].E)
        return this.tableData[index].F.toFixed(2)
      }
    },
    i() {
      return function (index) {
        this.tableData[index].I = (parseFloat(this.tableData[index].G) ? parseFloat(this.tableData[index].G) : 0) * parseFloat(this.tableData[index].H)
        return this.tableData[index].I.toFixed(2)
      }
    },
    unchanged() {
      return function (index) {
        this.tableData[index].unchanged = (parseFloat(this.tableData[index].C) ? parseFloat(this.tableData[index].C) : 0) + (parseFloat(this.tableData[index].F) ? parseFloat(this.tableData[index].F) : 0) + (parseFloat(this.tableData[index].I) ? parseFloat(this.tableData[index].I) : 0)

        var sum = 0
        for (var i = 0; i < 3; i++)
          sum += (parseFloat(this.tableData[i].unchanged) ? parseFloat(this.tableData[i].unchanged) : 0)
        this.$data.SUM = sum.toFixed(2)

        return this.tableData[index].unchanged.toFixed(2)
      }
    },
    TDL() {
      var vaf = 0
      // console.log('111',this.$data.tableData)
      for (var i = 0; i < 20; i++)
        vaf += (parseFloat(this.dataadjust[i].grade) ? parseFloat(this.dataadjust[i].grade) : 0)
      this.$data.TDL = vaf.toFixed(2)
      return vaf
    },
    TCA(){
      return (this.$data.TDL*0.005+0.65).toFixed(2)
    },
    AFPI(){

      return (this.$data.SUM*(this.$data.TDL*0.005+0.65)).toFixed(2)
    },
    PE(){

      return (this.$data.SUM*(this.$data.TDL*0.005+0.65)*10).toFixed(2)
    },
    MONEY(){

      return (this.$data.SUM*(this.$data.TDL*0.005+0.65)*10*50).toFixed(2)
    }



  },
  methods: {

  }
}
</script>

<style scoped>
.title {
  text-align: center;
  font-family: sans-serif;
  font-size: 30px;
}

.secondtitle {
  text-indent: 2em;
  font-weight: bold;
  margin-left: 30px;
  margin-right: 30px;
  font-size: 15px;
}
.thirdtitle {
  text-indent: 2em;
  font-weight: normal;
  margin-left: 30px;
  margin-right: 30px;
  font-size: 10px;
}
.textareac{
  resize: none;
  text-align: left;
  background: #FFFFFF;
  width:400px;
  height:100px;
  text-align:center;
  SCROLLBAR-FACE-COLOR: #004824;
  SCROLLBAR-HIGHLIGHT-COLOR: #004824;
  SCROLLBAR-SHADOW-COLOR: #004824;
  SCROLLBAR-3DLIGHT-COLOR: #004824;
  SCROLLBAR-ARROW-COLOR: #00fc00;
  SCROLLBAR-TRACK-COLOR: #4848fc;
  SCROLLBAR-DARKSHADOW-COLOR: #004824;
  SCROLLBAR-BASE-COLOR: #004824
}
.textareacc{
  resize: none;
  background: #FFFFFF;
  /*将边框去掉*/
  border: 0;
  /*设置宽度高度*/
  height: 80px;
  width: 400px;
  /*设置字体大小*/
  font-size: 18px;
  /* placeholder位置 提示靠左靠右居中等 */
  text-align: left;
  /* 其他样式还有不少，没有用就没查，需要可自行查看 */
}


.maintable {
  text-align: center;
  font-family: sans-serif;
  font-size: 30px;
}

.button1 {
  margin-left: 25px;
}

.button2 {
  margin-left: 15px;
}

.button3 {

  float: right;
  margin-top: 10px;
  margin-right: 50px;

}

.button4 {

  margin-left: 250px;

}

.content {
  text-indent: 2em;
  margin-left: 20px;
  margin-right: 20px;
}

.guidance {
  position: absolute;
  right: 50px;
  font-weight: bold;
}

:deep(.ant-table .ant-table-thead > tr > th) {
  border-width: 1px;
}
</style>

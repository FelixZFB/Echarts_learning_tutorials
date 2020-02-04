## ECharts 4.6.0 使用教程----2020.2.04

# 1. 安装使用
- 直接从 [GitHub](https://github.com/apache/incubator-echarts/releases) 下载整个项目文件，然后从echarts-4.6.0/dist 
    文件夹中获取构建好的 echarts，这都可以直接在浏览器端项目中使用。这些构建好的 echarts 提供了下面这几种定制：
- 完全版：echarts/dist/echarts.js，体积最大，包含所有的图表和组件，所包含内容参见：echarts/echarts.all.js。
- 常用版：echarts/dist/echarts.common.js，体积适中，包含常见的图表和组件，所包含内容参见：echarts/echarts.common.js。
- 精简版：echarts/dist/echarts.simple.js，体积较小，仅包含最常用的图表和组件，所包含内容参见：echarts/echarts.simple.js。
- 也可以使用在线引入地址：http://www.bootcdn.cn/echarts/

# 2. ECharts基础概念概览
## 2.1 ECharts实例 
- 一个网页中可以创建多个 echarts 实例。
- 每个 echarts 实例 中可以创建多个图表和坐标系等等（用 option 来描述）。
- 准备一个 DOM 节点（作为 echarts 的渲染容器），就可以在上面创建一个 echarts 实例。
- 每个 echarts 实例独占一个 DOM 节点。
- 参考图片解释-001，01文件夹中003案例

## 2.2 系列（series）
- 系列（series）是很常见的名词。
- 在 echarts 里，系列（series）是指：一组数值以及他们映射成的图。
- “系列”这个词原本可能来源于“一系列的数据”，而在 echarts 中取其扩展的概念，不仅表示数据，也表示数据映射成为的图。
- 所以，一个 系列 包含的要素至少有：一组数值、图表类型（series.type）、以及其他的关于这些数据如何映射成图的参数。
- echarts 里系列类型（series.type）就是图表类型。系列类型（series.type）至少有：
    - line（折线图）、bar（柱状图）、pie（饼图）、scatter（散点图）、graph（关系图）、tree（树图）、...
    - 如下图，右侧的 option 中声明了三个 系列（series）：pie（饼图系列）、line（折线图系列）、bar（柱状图系列），
    - 每个系列中有他所需要的数据（series.data）。
    - 参考图片解释-002/003


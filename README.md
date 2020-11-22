# grid-layout

> 网格布局

## 定义网格布局

- display: grid;

## 行/列 宽

- grid-template-columns  列宽
- grid-template-rows  行宽

    - repeat(n, 33.3%)  n: 重复次数
    - repeat(auto-fill, 100px)  自动填充
    - fr 比例关系
    - minmax()  最小/大值
    - auto 自适应像素
    - [] 方括号网格线

## 行/列 间距

- grid-row-gap 行间距
- grid-column-gap 列间距
- grid-gap: `<grid-row-gap> <grid-column-gap>` (简称)

## 项目排序

- 默认：row (先左右后上下)
- grid-auto-flow: `row/column | dense`

  - row 先左右后上下
  - column 先上下后左右
  - dense (尽量填充满)

### 整个内容区域在容器的位置

- align-content （整个内容区域在容器的垂直位置）
- justify-content （整个内容区域在容器的水平位置）
- place-content: `<align-content> <justify-content>` 简写

### 单元格的位置，作用于所有项目

- justify-items (单元格的水平位置) 
- align-items（单元格的垂直位置） 注意：有足够的高度才会有效果
- place-items: `<align-items> <justify-items>` 简写

## 单元格的位置，作用于单个项目

- justify-self（单元格内容水平位置）
- align-self （单元格内容垂直位置）
- place-self `<justify-self> <align-self>` 简写

### 特殊属性

- space-evenly - 项目与项目的间隔相等，项目与容器边框之间也是同样长度的间隔。

## 指定单元格边框的所在网格线

- grid-column-start 
- grid-column-end 
- grid-row-start 
- grid-row-end 

- span n（跨域n个网格线）

#### 简写

- grid-column: <start-line> / <end-line>;
- grid-row: <start-line> / <end-line>;

- grid-column: 1 / span 3

## grid-area

- 1、属性指定项目放在哪一个区域。
- 2、grid-column-start/end grid-row-start/end (指定单元格边框的所在网格线的简写)
 
  - grid-area: <row-start> / <column-start> / <row-end> / <column-end>;

## - grid-auto-rows/column(指定多余的行/列 高)

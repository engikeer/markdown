# Markdown语法手册
[TOC]
## 一. 板式
### 1. 标题
```
# 一级标题
## 二级标题
……
###### 六级标题
```

### 2. 换行
```
空格+空格+回车
或：
<br/>
```

### 3. 缩进
```
使用添加空格符的方式实现：
半方大的空白&ensp;或&#8194;
全方大的空白&emsp;或&#8195;
不断行的空白格&nbsp;或&#160;

```

### 4. 强调
```
*斜体* 或 _斜体_
**粗体** 或 __粗体__
++下划线++
~~删除线~~
==记号==

```
*斜体* 
**粗体**
++下划线++  
~~删除线~~
==记号==

### 5. 上下标
```
上标^TM^
下标~2~
```
上标^TM^  
下标~2~

### 6. 水平线
```
---
或
***
```

### 7. 注脚
```
这里需要注脚[^note1]
[^note1]: 注脚文本
```
这里需要注脚[^note1]
[^note1]: 注脚文本note1
注：无论注脚文本写在何处，都显示在页面最下方

### 8. 缩写
```
*[缩写]: 含义
```
*[HTML]: Hyper Text Markup Language
程序员使用 HTML 开发网络应用


### 9. 无序列表
```
* 列表项1
或：
+ 列表项2
或：
- 列表项3
```
* 列表项1
+ 列表项2
- 列表项3

### 10. 有序列表
```
由数字与点表示：
1. 列表项1
2. 列表项2
3. 列表项3
```
1. 列表项1
2. 列表项2
3. 列表项3

### 11. 定义列表
```
列表项 1
~ 定义一

列表项 2
~ 定义一
~ 定义二
```
列表项 1
~ 定义一

列表项 2
~ 定义一
~ 定义二

### 12. 转义字符
```
markdown中的转义字符为“\”
当需要输入某些markdown记号时，可在前面加入“\”
```
未转义：2*2*2=8  
转义：2\*2\*2=8
## 二. 插入项
### 1. 链接
```
[链接描述](链接地址)
```
[百度一下](https://www.baidu.com)

### 2. 图片
```
![图片描述](图片链接)
```
![图片描述](图片链接)

### 3. 目录
```
[TOC] 
```
[TOC]
### 4. 文字引用
```
> 引用的文字
```
> We must know, we will know.

### 5. 代码块
```
使用Tab键表示代码块
```
    print("Life is shot, use python!")

### 6. 行内代码块
```
`some code`
```
键入`print("Life is shot, use python!")`

### 7. 表格
```
First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

| Left Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
```
First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |

### 8. 自定义区域
```
:::info
提示信息
:::
:::success
成功信息
:::
:::warning
警告信息
:::
:::danger
危险信息
:::
```
:::info
提示信息
:::
:::success
成功信息
:::
:::warning
警告信息
:::
:::danger
危险信息
:::

### 9. 待办事项
```
- [ ] a bigger project
  - [x] first subtask
  - [x] follow up subtask
  - [ ] final subtask
- [ ] a separate task
```
- [ ] a bigger project
  - [x] first subtask
  - [x] follow up subtask
  - [ ] final subtask
- [ ] a separate task


### 10. Html标签
```html
<p style="text-align:center;"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/120px-HTML5_logo_and_wordmark.svg.png"/></p>

<a href="https://github.com/tylingsoft/markdown-plus" target="_blank"><img style="position: absolute; top: 0; right: 0; border: 0;" src="http://aral.github.com/fork-me-on-github-retina-ribbons/right-green.png" alt="Fork me on GitHub"></a>
```


## 三. 内嵌图标
### 1. Emoji图标
```
:smile:
```
:smile:  
[Emoji Cheat Sheet](http://www.emoji-cheat-sheet.com/)


### 2. Fontawesome图标
```
:fa-code:
```
:fa-code:  
注：github暂不支持  
[Font Awesome icons](http://fontawesome.io/icons/)

### 3. Ionicons
```
:ion-coffee:
```
:ion-coffee:  
注：github暂不支持  
[Ionicons icons](http://ionicons.com/)

## 四. 数学公式
### 1. TeX公式
```
行内公式：`$E = mc^2$`
公式块：

“```math
```”
```
行内公式：`$E = mc^2$`  
公式块：
```math
\phi_n(\kappa) =
 \frac{1}{4\pi^2\kappa^2} \int_0^\infty
 \frac{\sin(\kappa R)}{\kappa R}
 \frac{\partial}{\partial R}
 \left[R^2\frac{\partial D_n(R)}{\partial R}\right]\,dR
```
注：编写语法为TeX标记，github默认不支持TeX语法，但可识别公式块中的简单公式。

### . AsciiMath
```
行内公式： `@(1/2[1-(1/2)^n])/(1-(1/2))=s_n@`
公式块：
“```ASCIIMath
phi_n(kappa) = 1/(4pi^2 kappa^2)
 int_0^oo (sin(kappa R))/(kappa R)
 del/(del R)
[R^2 (del D_n (R))/(del R)] del R
```”
```
[AsciiMath Documentation](http://asciimath.org/)

## 五. 加强块
```
markdown中的代码块可以通过指定语言来实现语法高亮。
```
### 1. 加强代码块
python:
```python
@requires_authorization
def somefunc(param1='', param2=0):
    '''A docstring'''
    if param1 > param2: # interesting
        print 'Greater'
    return (param2 - param1 + 1) or None

class SomeClass:
    pass

>>> message = '''interpreter
... prompt'''
```
R:
```r
EDA <- function(x) {
par(mfrow = c(2, 2)) 
hist(x)
dotchart(x)
boxplot(x, horizontal = T)
qqnorm(x); qqline(x)
par(mfrow = c(1, 1))
}
```

### 2. 流程图
```
graph TD
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C{Let me think}
    C -->|One| D[Laptop]
    C -->|Two| E[iPhone]
    C -->|Three| F[Car]
```
```
graph LR
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C{Let me think}
    C -->|One| D[Laptop]
    C -->|Two| E[iPhone]
    C -->|Three| F[Car]
```
[流程图语法](http://knsv.github.io/mermaid/#flowcharts-basic-syntax)

### 4. 序列图
```
sequenceDiagram
    loop every day
        Alice->>John: Hello John, how are you?
        John-->>Alice: Great!
    end
```
[序列图语法](http://knsv.github.io/mermaid/#sequence-diagrams)

### 5. 甘特图
```
gantt
    title 项目开发流程
    section 项目确定
        需求分析       :a1, 2016-06-22, 3d
        可行性报告     :after a1, 5d
        概念验证       : 5d
    section 项目实施
        概要设计      :2016-07-05  , 5d
        详细设计      :2016-07-08, 10d
        编码          :2016-07-15, 10d
        测试          :2016-07-22, 5d
    section 发布验收
        发布: 2d
        验收: 3d
```
[甘特图语法](http://knsv.github.io/mermaid/#gant-diagrams)


## 六. 图表
[图表参考](tuhttp://www.chartjs.org/docs/)
### 1. 折线图
```chart
{
  "type": "line",
  "data": {
    "labels": [
      "January",
      "February",
      "March",
      "April",
      "May",
      "June",
      "July"
    ],
    "datasets": [
      {
        "label": "# of bugs",
        "fill": false,
        "lineTension": 0.1,
        "backgroundColor": "rgba(75,192,192,0.4)",
        "borderColor": "rgba(75,192,192,1)",
        "borderCapStyle": "butt",
        "borderDash": [],
        "borderDashOffset": 0,
        "borderJoinStyle": "miter",
        "pointBorderColor": "rgba(75,192,192,1)",
        "pointBackgroundColor": "#fff",
        "pointBorderWidth": 1,
        "pointHoverRadius": 5,
        "pointHoverBackgroundColor": "rgba(75,192,192,1)",
        "pointHoverBorderColor": "rgba(220,220,220,1)",
        "pointHoverBorderWidth": 2,
        "pointRadius": 1,
        "pointHitRadius": 10,
        "data": [
          65,
          59,
          80,
          81,
          56,
          55,
          40
        ],
        "spanGaps": false
      }
    ]
  },
  "options": {}
}
```
[折线图参考](http://www.chartjs.org/docs/#line-chart)

### 2. 条形图
```chart
{
  "type": "bar",
  "data": {
  "labels": [
    "Red",
    "Blue",
    "Yellow",
    "Green",
    "Purple",
    "Orange"
  ],
  "datasets": [
    {
    "label": "# of Votes",
    "data": [
      12,
      19,
      3,
      5,
      2,
      3
    ],
    "backgroundColor": [
      "rgba(255, 99, 132, 0.2)",
      "rgba(54, 162, 235, 0.2)",
      "rgba(255, 206, 86, 0.2)",
      "rgba(75, 192, 192, 0.2)",
      "rgba(153, 102, 255, 0.2)",
      "rgba(255, 159, 64, 0.2)"
    ],
    "borderColor": [
      "rgba(255,99,132,1)",
      "rgba(54, 162, 235, 1)",
      "rgba(255, 206, 86, 1)",
      "rgba(75, 192, 192, 1)",
      "rgba(153, 102, 255, 1)",
      "rgba(255, 159, 64, 1)"
    ],
    "borderWidth": 1
    }
  ]
  },
  "options": {}
}
```
[条形图参考](http://www.chartjs.org/docs/#bar-chart)

### 3. 雷达图
```chart
{
  "type": "radar",
  "data": {
    "labels": [
      "Eating",
      "Drinking",
      "Sleeping",
      "Designing",
      "Coding",
      "Cycling",
      "Running"
    ],
    "datasets": [
      {
        "label": "My First dataset",
        "backgroundColor": "rgba(179,181,198,0.2)",
        "borderColor": "rgba(179,181,198,1)",
        "pointBackgroundColor": "rgba(179,181,198,1)",
        "pointBorderColor": "#fff",
        "pointHoverBackgroundColor": "#fff",
        "pointHoverBorderColor": "rgba(179,181,198,1)",
        "data": [
          65,
          59,
          90,
          81,
          56,
          55,
          40
        ]
      },
      {
        "label": "My Second dataset",
        "backgroundColor": "rgba(255,99,132,0.2)",
        "borderColor": "rgba(255,99,132,1)",
        "pointBackgroundColor": "rgba(255,99,132,1)",
        "pointBorderColor": "#fff",
        "pointHoverBackgroundColor": "#fff",
        "pointHoverBorderColor": "rgba(255,99,132,1)",
        "data": [
          28,
          48,
          40,
          19,
          96,
          27,
          100
        ]
      }
    ]
  },
  "options": {}
}
```
[雷达图参考](http://www.chartjs.org/docs/#radar-chart)

### 4. 极面积图
```chart
{
  "type": "polarArea",
  "data": {
    "datasets": [
      {
        "data": [
          11,
          16,
          7,
          3,
          14
        ],
        "backgroundColor": [
          "#FF6384",
          "#4BC0C0",
          "#FFCE56",
          "#E7E9ED",
          "#36A2EB"
        ],
        "label": "My dataset"
      }
    ],
    "labels": [
      "Red",
      "Green",
      "Yellow",
      "Grey",
      "Blue"
    ]
  },
  "options": {}
}
```
[极面积图参考](http://www.chartjs.org/docs/#polar-area-chart)

### 5. 饼图
```chart
{
  "type": "pie",
  "data": {
    "labels": [
      "Red",
      "Blue",
      "Yellow"
    ],
    "datasets": [
      {
        "data": [
          300,
          50,
          100
        ],
        "backgroundColor": [
          "#FF6384",
          "#36A2EB",
          "#FFCE56"
        ],
        "hoverBackgroundColor": [
          "#FF6384",
          "#36A2EB",
          "#FFCE56"
        ]
      }
    ]
  },
  "options": {}
}
```
[饼图参考](http://www.chartjs.org/docs/#doughnut-pie-chart)

### 6. 圆环图
```chart
{
  "type": "doughnut",
  "data": {
    "labels": [
      "Red",
      "Blue",
      "Yellow"
    ],
    "datasets": [
      {
        "data": [
          300,
          50,
          100
        ],
        "backgroundColor": [
          "#FF6384",
          "#36A2EB",
          "#FFCE56"
        ],
        "hoverBackgroundColor": [
          "#FF6384",
          "#36A2EB",
          "#FFCE56"
        ]
      }
    ]
  },
  "options": {}
}
```
[圆环图参考](http://www.chartjs.org/docs/#doughnut-pie-chart)

8. 气泡图
```chart
{
  "type": "bubble",
  "data": {
    "datasets": [
      {
        "label": "First Dataset",
        "data": [
          {
            "x": 20,
            "y": 30,
            "r": 15
          },
          {
            "x": 40,
            "y": 10,
            "r": 10
          }
        ],
        "backgroundColor": "#FF6384",
        "hoverBackgroundColor": "#FF6384"
      }
    ]
  },
  "options": {}
}
```
[气泡图参考](http://www.chartjs.org/docs/#bubble-chart)
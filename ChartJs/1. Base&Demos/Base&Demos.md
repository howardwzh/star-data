#Base&Demos

## Base Usage
```html
...
<!-- Step1: canvas -->
<canvas id="myChart" width="400" height="400"></canvas>
...
<!-- Step2: 引入ChartJs库 -->
<script src="path/to/chartjs/dist/Chart.js"></script>
<!-- Step3: 获取canvas元素，配置图表并渲染 -->
<script>
  var ctx = document.getElementById("myChart"); // 获取canvas元素
  var myChart = new Chart(ctx, { // 配置图表并渲染
    type: 'line', // Part1: 图表类型 = line|bar|radar|pie|doughnut|polarArea|bubble|scatter
    data: { // Part2: 图表数据
      labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'], // 水平labels
      datasets: [{ // 数据datasets(数组类型，可多组数据，且可有自己的“图表类型”)
        label: 'Hello ChartJs-Line', // 数据标题
        data: [12, 19, 3, 5, 2, 3], // 数据值
        ... // 其它配置请参考文档，“可配置参数” 根据 “图表类型” 不同而不同
      }]
    },
    options: { // Part3: 图表选项
      ... // 配置请参考文档，“可配置选项” 根据 “图表类型” 不同而不同
    }
  });
</script>
```
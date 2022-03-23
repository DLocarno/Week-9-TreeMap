## Make e-charts tree map
using the data here:

```
    let data=[
        {"parentColumn": "",  "childColumn":"A"},
        {"parentColumn": "A", "childColumn":"B"},
        {"parentColumn": "A", "childColumn":"C"},
        {"parentColumn": "B", "childColumn":"D","val":30},
        {"parentColumn": "B", "childColumn":"E","val":50},
        {"parentColumn": "C", "childColumn":"F","val":20},
        {"parentColumn": "C", "childColumn":"G","val":40},
        {"parentColumn": "C", "childColumn":"H","val":60}
    ]
```

<b>Note</b><p>you need to stratify data manually, or using an algorithm such that echarts can convert it into visualization. In case you go with a code, it should be a recursive code to cover all the children</p><p>The top parent in echart requires a parent node.</p>

1. You can transform data manually or use a recursive algorithm to convert parents and all the children into readable data for echarts. (30 Points + 10 bonus points for the recursive function)
2. echarts Visualization (should contain all the parents including A --  Modify the dataset to add it as root!) (30 points)
3. Manually Color-code each one of the parents (20 points)
4. Upload the final result on GitHub, make a Web Page, share it along with the zip file of the application.

Node for manual color code use the following option in series:
levels: [{
                itemStyle: {
                    borderColor: '#555',
                    borderWidth: 0,
                    gapWidth: 10
                },
                upperLabel: {
                    show: false
                }
            }, {
                itemStyle: {
                    borderColor: '#52AB80',
                    borderWidth: 5,
                    gapWidth: 5
                },
                emphasis: {
                    itemStyle: {
                        borderColor: '#ccc'
                    }
                }
            }, {
                itemStyle: {
                    borderColor: '#e8aa63',
                    borderWidth: 5,
                    gapWidth: 1
                },
                emphasis: {
                    itemStyle: {
                        borderColor: '#ccc'
                    }
                }
            }, {
                itemStyle: {
                    borderColor: '#F0F4F3',
                    borderWidth: 5,
                    gapWidth: 1
                },
                emphasis: {
                    itemStyle: {
                        borderColor: '#ccc'
                    }
                }
            }, {
                colorSaturation: [0.3, 0.55],
                itemStyle: {
                    borderWidth: 5,
                    gapWidth: 1,
                    borderColorSaturation: 0.7
                }
            }],
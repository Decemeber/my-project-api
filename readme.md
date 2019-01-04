
## 简介

用来记录项目中的API接口

## 客流分析
获取Echarts表格的数据
```bash
# GET
    /api/passengeranalysis/:type

# 进站客流（终端设备）
    /api/passengeranalysis/entrypassenger

# 出站客流（终端设备）
    /api/passengeranalysis/outpassenger

# 进站客流（票卡类型）
    /api/passengeranalysis/entrypassengercard

# 出站客流（票卡类型）
    /api/passengeranalysis/outpassengercard

# Response Example
{
    "timexAxis": ["06:15", "06:30", "06:45", "07:00", "07:15", "07:30", "07:45", "08:00", "08:15", "08:30", "08:45", "09:00", "09:15"],
    "equipNode": [
        { "CardName": "一日票", "MainType": 95, "SubType": 0 },
        {"CardName": "单程票", "MainType": 98, "SubType": 0 }, 
        { "CardName": "普通卡(一卡通)", "MainType": 66, "SubType": 1 }],
    "detailData": {
        "一日票": [10, 20, 10, 30, 40, 80, 20, 30, 0, 120, 0, 0, 110],
        "三日票": [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
        "单程票": [0, 0, 0, 10, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
        "爱心票": [0, 0, 0, 0, 0, 0, 20, 0, 0, 0, 0, 0, 0, 0],
        "学生票": [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 2, 0, 0],
        "出站票": [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
        "储值卡": [0, 0, 10, 0, 0, 0, 0, 0, 0, 10, 0, 20, 0]
}
```

## 统计报表
获取report表格的相关数据
```bash
# GET
    /api/statisticalreport
#query params
    id,equip,datestart,dateend
#Response Example
{
    title:“”,
    main：[],
    res:[]
}
```
获取report发送的id
```bash    
# GET
    /api/reportid
#query params
    无
#Response Example
    [id1,id2,di3,...]
```
获取当前可选择设备
```bash
# GET
    /api/equipmentonline
#query params
    无
#Response Example
[
    {
        NodeID,
        NodeNo,
        NodeType
    },
    ...
]
```
浏览器访问 http://localhost:8080





## 其它
```bash
# --report to build with bundle size analytics

```

## License

[MIT](https://github.com/Decemeber/my-project-api/LICENSE)

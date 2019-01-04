
## 简介

用来记录项目中的API接口

## 客流分析
获取Echarts表格的数据
```
#GET
    /api/passengeranalysis/:type
#进站客流（终端设备）
    /api/passengeranalysis/entrypassenger
#出站客流（终端设备）
    /api/passengeranalysis/outpassenger
#进站客流（票卡类型）
    /api/passengeranalysis/entrypassengercard
#出站客流（票卡类型）
    /api/passengeranalysis/outpassengercard

Response Example

{
    "timexAxis": ["06:15", "06:30", "06:45", "07:00", "07:15", "07:30", "07:45", "08:00", "08:15", "08:30", "08:45", "09:00", "09:15"],
    "equipNode": [{ "CardName": "一日票", "MainType": 95, "SubType": 0 }, { "CardName": "三日票", "MainType": 95, "SubType": 1 }, {"CardName": "单程票", "MainType": 98, "SubType": 0 }, { "CardName": "普通卡(一卡通)", "MainType": 66, "SubType": 1 }],
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

## 开发
```bash
# 克隆项目


# 安装依赖
npm install
   
# 建议不要用cnpm安装 会有各种诡异的bug 可以通过如下操作解决 npm 下载速度慢的问题

# 启动服务

```
浏览器访问 http://localhost:9527

## 发布
```bash
# 构建测试环境
{
    timeLine:[6:00,6:15],
    equipNode:[],
    detailData:{
        '单程票':[1,2,3,4,5,1,2,1],
        '出站票':[2,3,4,5,6,7,8,9]
    }
}

# 构建生成环境
npm run build:prod
```

## 其它
```bash
# --report to build with bundle size analytics
npm run build:prod --report

# --preview to start a server in local to preview
npm run build:prod --preview

# lint code
npm run lint

# auto fix
npm run lint -- --fix
```


## Changelog

## Online Demo

## Donate
如果你觉得这个项目帮助到了你，你可以帮作者买一杯果汁表示鼓励 :tropical_drink:

## License

[MIT](https://github.com/PanJiaChen/vue-element-admin/blob/master/LICENSE)


## 简介

## 功能
```
- 登录/注销
- 权限验证
- Markdown2html
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

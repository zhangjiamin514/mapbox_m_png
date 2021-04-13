# mapbox_m_png
mapbox转png图片

## Build Setup

``` bash
# 安装依赖
npm install

# 启动页面，访问 localhost:6688
npm run dev

```

## 修改自己的地图样式
在static/config.json文件中修改，accessToken为自己的mapbox中的密钥，name为点击下载之后的图片名称，mapOp中的对象为mapbox的配置。
其他的不需要改，如果需要改文件，修改src\components\mapbox下的Map.vue文件

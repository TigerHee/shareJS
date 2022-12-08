
- [安装前先npm初始化](#%E5%AE%89%E8%A3%85%E5%89%8D%E5%85%88npm%E5%88%9D%E5%A7%8B%E5%8C%96)
- [本地服务](#%E6%9C%AC%E5%9C%B0%E6%9C%8D%E5%8A%A1)
- [复制html](#%E5%A4%8D%E5%88%B6html)
- [处理css](#%E5%A4%84%E7%90%86css)
- [处理less](#%E5%A4%84%E7%90%86less)
- [抽离css文件，通过link引入](#%E6%8A%BD%E7%A6%BBcss%E6%96%87%E4%BB%B6%E9%80%9A%E8%BF%87link%E5%BC%95%E5%85%A5)
- [压缩css和js](#%E5%8E%8B%E7%BC%A9css%E5%92%8Cjs)
- [给css加上兼容浏览器的前缀](#%E7%BB%99css%E5%8A%A0%E4%B8%8A%E5%85%BC%E5%AE%B9%E6%B5%8F%E8%A7%88%E5%99%A8%E7%9A%84%E5%89%8D%E7%BC%80)
- [es6 转 es5](#es6-%E8%BD%AC-es5)
- [es 7的语法](#es-7%E7%9A%84%E8%AF%AD%E6%B3%95)
- [全局变量引入](#%E5%85%A8%E5%B1%80%E5%8F%98%E9%87%8F%E5%BC%95%E5%85%A5)
- [webpack图片打包](#webpack%E5%9B%BE%E7%89%87%E6%89%93%E5%8C%85)
- [当图片小于多少，用base64](#%E5%BD%93%E5%9B%BE%E7%89%87%E5%B0%8F%E4%BA%8E%E5%A4%9A%E5%B0%91%E7%94%A8base64)
- [打包文件分类](#%E6%89%93%E5%8C%85%E6%96%87%E4%BB%B6%E5%88%86%E7%B1%BB)
- [希望输出的时候，给这些`css\img`加上前缀，传到服务器也能访问](#%E5%B8%8C%E6%9C%9B%E8%BE%93%E5%87%BA%E7%9A%84%E6%97%B6%E5%80%99%E7%Bimg%E5%8A%A0%E4%B8%8A%E5%89%8D%E7%BC%80%E4%BC%A0%E5%88%B0%E6%9C%8D%E5%8A%A1%E5%99%A8%E4%B9%9F%E8%83%BD%E8%AE%BF%E9%97%AE)
- [如果只希望处理图片](#%E5%A6%82%E6%9E%9C%E5%8F%AA%E5%B8%8C%E6%9C%9B%E5%A4%84%E7%90%86%E5%9B%BE%E7%89%87)
- [打包多页应用](#%E6%89%93%E5%8C%85%E5%A4%9A%E9%A1%B5%E5%BA%94%E7%94%A8)
- [配置`source-map`](#%E9%85%8D%E7%BD%AEsource-map)
- [`watch` 改完代表重新打包实体](#watch-%E6%94%B9%E5%AE%8C%E4%BB%A3%E8%A1%A8%E9%87%8D%E6%96%B0%E6%89%93%E5%8C%85%E5%AE%9E%E4%BD%93)
- [`webpack`的其他三个小插件](#webpack%E7%9A%84%E5%85%B6%E4%BB%96%E4%B8%89%E4%B8%AA%E5%B0%8F%E6%8F%92%E4%BB%B6)
- [`webpack` 跨域](#webpack-%E8%B7%A8%E5%9F%9F)
- [如果后端给的请求没有API 「跨域」](#%E5%A6%82%E6%9E%9C%E5%90%8E%E7%AB%AF%E7%BB%99%E7%9A%84%E8%AF%B7%E6%B1%82%E6%B2%A1%E6%9C%89api-%E8%B7%A8%E5%9F%9F)
- [前端只想单纯mock数据 「跨域」](#%E5%89%8D%E7%AB%AF%E5%8F%AA%E6%83%B3%E5%8D%95%E7%BA%AFmock%E6%95%B0%E6%8D%AE-%E8%B7%A8%E5%9F%9F)
- [有服务端，不用代理, 服务端启动webpack 「跨域」](#%E6%9C%89%E6%9C%8D%E5%8A%A1%E7%AB%AF%E4%B8%8D%E7%94%A8%E4%BB%A3%E7%90%86-%E6%9C%8F%E5%90%AF%E5%8A%A8webpack-%E8%B7%A8%E5%9F%9F)
- [webpack解析resolve](#webpack%E8%A7%A3%E6%9E%90resolve)
- [但是每次引入都很长，如何优雅引入](#%E4%BD%86%E6%98%AF%E6%AF%8F%E6%AC%A1%E5%BC%95%E5%85%A5%E9%83%BD%E5%BE%88%E9%95%BF%E5%A6%82%E4%B%9B%85%E5%BC%95%E5%85%A5)
- [省略扩展名](#%E7%9C%81%E7%95%A5%E6%89%A9%E5%B1%95%E5%90%8D)
- [定义环境变量](#%E5%AE%9A%E4%B9%89%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F)
- [区分两个不同的环境](#%E5%8C%BA%E5%88%86%E4%B8%A4%E4%B8%AA%E4%B8%8D%E5%90%8C%E7%9A%84%E7%8E%AF%E5%A2%83)
- [webpack 优化](#webpack-%E4%BC%98%E5%8C%96)
- [优化：当某些包是独立的个体没有依赖](#%E4%BC%98%E5%8C%96%E5%BD%93%E6%9F%90%E4%BA%9B%E5%8C%85%E6%98%AF%E7%8B%AC%E7%AB%8B%E7%9A%84%E4%B8%AA%E4%BD%93%E6%B2%A1%E6%9C%89%E4%BE%9D%E8%B5%96)
- [优化：规则匹配设置范围](#%E4%BC%98%E5%8C%96%E8%A7%84%E5%88%99%E5%8C%B9%E9%85%8D%E8%AE%BE%E7%BD%AE%E8%8C%83%E5%9B%B4)
- [优化：忽略依赖中不必要的语言包](#%E4%BC%98%E5%8C%96%E5%BF%BD%E7%95%A5%E4%BE%9D%E8%B5%96%E4%B8%AD%E4%B8%8D%E5%BF%85%E8%A6%81%E7%9A%A8%80%E5%8C%85)
- [动态链接库](#%E5%8A%A8%E6%80%81%E9%93%BE%E6%8E%A5%E5%BA%93)
- [多线程打包happypack](#%E5%A4%9A%E7%BA%BF%E7%A8%8B%E6%89%93%E5%8C%85happypack)
- [webpack 自带的优化](#webpack-%E8%87%AA%E5%B8%A6%E7%9A%84%E4%BC%98%E5%8C%96)
- [抽取公共代码](#%E6%8A%BD%E5%8F%96%E5%85%AC%E5%85%B1%E4%BB%A3%E7%A0%81)
- [懒加载(延迟加载)](#%E6%87%92%E5%8A%A0%E8%BD%BD%E5%BB%B6%E8%BF%9F%E5%8A%A0%E8%BD%BD)
- [热更新(当页面改变只更新改变的部分，不重新打包)](#%E7%83%AD%E6%9B%B4%E6%96%B0%E5%BD%93%E9%A1%B5%E9%9D%A2%E6%94%B9%E5%8F%98%E5%8F%AA%E6%9B%B4%E6%96%B0%E6%94%B9%E5%8F%98%E7%9A%84%E9%83%A8%E5%88%86%E4%B8%8D%E9%87%8D%E6%96%B0%E6%89%93%E5%8C%85)
- [tapable介绍 - SyncHook](#tapable%E4%BB%8B%E7%BB%8D---synchook)
- [tapable介绍 - SyncBailHook](#tapable%E4%BB%8B%E7%BB%8D---syncbailhook)
- [tapable介绍 - SyncWaterfallHook](#tapable%E4%BB%8B%E7%BB%8D---syncwaterfallhook)
- [tapable介绍 - SyncLoopHook](#tapable%E4%BB%8B%E7%BB%8D---syncloophook)
- [`AsyncParallelHook` 与 `AsyncParallelBailHook`](#asyncparallelhook-%E4%B8%8E-asyncparallelbailhook)
    + [AsyncParallelHook](#asyncparallelhook)
    + [AsyncParallelBailHook](#asyncparallelbailhook)
- [异步串行 —— AsyncSeriesHook](#%E5%BC%82%E6%AD%A5%E4%B8%B2%E8%A1%8C--asyncserieshook)
- [异步串行 —— AsyncSeriesWaterfallHook](#%E5%BC%82%E6%AD%A5%E4%B8%B2%E8%A1%8C--asyncserieswaterfallhook)
- [手写webpack](#%E6%89%8B%E5%86%99webpack)
- [webpack分析及处理](#webpack%E5%88%86%E6%9E%90%E5%8F%8A%E5%A4%84%E7%90%86)
- [创建依赖关系](#%E5%88%9B%E5%BB%BA%E4%BE%9D%E8%B5%96%E5%85%B3%E7%B3%BB)
- [ast递归解析](#ast%E9%80%92%E5%BD%92%E8%A7%A3%E6%9E%90)
- [生成打包工具](#%E7%94%9F%E6%88%90%E6%89%93%E5%8C%85%E5%B7%A5%E5%85%B7)
- [增加loader](#%E5%A2%9E%E5%8A%A0loader)
- [增加plugins](#%E5%A2%9E%E5%8A%A0plugins)
- [loader](#loader)
- [配置多个loader](#%E9%85%8D%E7%BD%AE%E5%A4%9A%E4%B8%AAloader)
- [`babel-loader`实现](#babel-loader%E5%AE%9E%E7%8E%B0)
- [`banner-loader`实现(自创)](#banner-loader%E5%AE%9E%E7%8E%B0%E8%87%AA%E5%88%9B)
- [实现`file-loader`和`url-loader`](#%E5%AE%9E%E7%8E%B0file-loader%E5%92%8Curl-loader)
- [`less-loader`和`css-loader`](#less-loader%E5%92%8Ccss-loader)
- [`css-loader`](#css-loader)
- [webpack 中的插件](#webpack-%E4%B8%AD%E7%9A%84%E6%8F%92%E4%BB%B6)
- [文件列表插件](#%E6%96%87%E4%BB%B6%E5%88%97%E8%A1%A8%E6%8F%92%E4%BB%B6)
- [内联的`webpack`插件](#%E5%86%85%E8%81%94%E7%9A%84webpack%E6%8F%92%E4%BB%B6)
- [打包后自动发布](#%E6%89%93%E5%8C%85%E5%90%8E%E8%87%AA%E5%8A%A8%E5%8F%91%E5%B8%83)

## 安装前先npm初始化

```
npm init -y
npm i webpack webpack-cli -D
```


```js
let path = require('path')   // 相对路径变绝对路径

module.exports = {
  mode: 'production', // 模式 默认 production development
  entry: './src/index',    // 入口
  output: {
    filename: 'bundle.[hash:8].js',   // hash: 8只显示8位
    path: path.resolve(__dirname, 'dist'),
    publicPath: ''  // // 给所有打包文件引入时加前缀，包括css，js，img，如果只想处理图片可以单独在url-loader配置中加publicPath
  }
}
```
## 本地服务

`npm i webpack-dev-server -D`

```
devServer: {
  port: 3000,
  progress: true          // 滚动条
  contentBase: './build'  // 起服务的地址
  open: true              // 自动打开浏览器
  compress： true         // gzip压缩
}
```


## 复制html

`npm i html-webpack-plugin -D`

```
let HtmlWebpackPlugin = require('html-webpack-plugin')
plugins: [ // 放着所有webpack插件
  new HtmlWebpackPlugin({ // 用于使用模板打包时生成index.html文件，并且在run dev时会将模板文件也打包到内存中
    template: './index.html', // 模板文件
    filename: 'index.html', // 打包后生成文件
    hash: true, // 添加hash值解决缓存问题
    minify: { // 对打包的html模板进行压缩
      removeAttributeQuotes: true, // 删除属性双引号
      collapseWhitespace: true // 折叠空行变成一行
    }
  })
]

```

[html-webpack-plugin#options](https://github.com/jantimon/html-webpack-plugin#options)


## 处理css

`npm i css-loader style-loader -D`

```
// css-loader   作用：用来解析@import这种语法
// style-loader 作用：把 css 插入到head标签中
// loader的执行顺序： 默认是从右向左（从下向上）
module: {    // 模块
  rules: [   // 规则
    // style-loader 把css插入head标签中
    // loader 功能单一
    // 多个loader 需要 []
    // 顺便默认从右到左
    // 也可以写成对象方式
    {
      test: /\.css$/,   // css 处理
      // use: 'css-loader'
      // use: ['style-loader', 'css-loader'],
      use: [
        // {
        //     loader: 'style-loader',
        //     options: {
        //         insertAt: 'top' // 将css标签插入最顶头  这样可以自定义style不被覆盖
        //     }
        // },
        MiniCssExtractPlugin.loader,
        'css-loader', // css-loader 用来解析@import这种语法,
        'postcss-loader'
      ]
    }
  ]
}
```


## 处理less

`npm i less-loader`

```
{
  test: /\.less$/,   // less 处理
  // use: 'css-loader'
  // use: ['style-loader', 'css-loader'],
  use: [
    // {
    //     loader: 'style-loader',
    //     options: {
    //         insertAt: 'top' // 将css标签插入最顶头  这样可以自定义style不被覆盖
    //     }
    // },
    MiniCssExtractPlugin.loader,   // 这样相当于抽离成一个css文件， 如果希望抽离成分别不同的css, 需要再引入MiniCssExtractPlugin，再配置
    'css-loader', // css-loader 用来解析@import这种语法
    'postcss-loader',
    'less-loader' // less-loader less -> css
    // sass node-sass sass-loader
    // stylus stylus-loader
  ]
}
```

[less-loader](https://webpack.js.org/loaders/less-loader/#src/components/Sidebar/Sidbar.jsx)

## 抽离css文件，通过link引入

`yarn add mini-css-extract-plugin -D`

[mini-css-extract-plugin](https://github.com/webpack-contrib/mini-css-extract-plugin)

```
let MiniCssExtractPlugin = require('mini-css-extract-plugin')

// 压缩css

plugins: [
  new MiniCssExtractPlugin({
      filename: 'css/main.css'
  })
]

{
  test: /\.css$/,   // css 处理
  // use: 'css-loader'
  // use: ['style-loader', 'css-loader'],
  use: [
    // {
    //     loader: 'style-loader',
    //     options: {
    //         insertAt: 'top' // 将css标签插入最顶头  这样可以自定义style不被覆盖
    //     }
    // },
    // 此时不需要style-loader
    MiniCssExtractPlugin.loader,   // 抽离
    'css-loader', // css-loader 用来解析@import这种语法,
    'postcss-loader'
  ]
}

```

抽离css插件文件时可使用`optimize-css-assets-webpack-plugin`优化压缩css以及js文件

## 压缩css和js

```
// 用了`mini-css-extract-plugin`抽离css为link需使用`optimize-css-assets-webpack-plugin`进行压缩css,使用此方法压缩了css需要`uglifyjs-webpack-plugin`压缩js
const OptimizeCSSAssetsPlugin = require("optimize-css-assets-webpack-plugin")
const UglifyJsPlugin = require("uglifyjs-webpack-plugin")

module.exports = {
  optimization: {              // 优化项
    minimizer: [
      new UglifyJsPlugin({     // 优化js
        cache: true,           // 是否缓存
        parallel: true,        // 是否并发打包
        // sourceMap: true     // 源码映射 set to true if you want JS source maps
      }),
      new OptimizeCSSAssetsPlugin({})    // css 的优化
    ]
  },
  mode: 'production',
  entry: '',
  output: {},
}

```

## 给css加上兼容浏览器的前缀

`yarn add postcss-loader autoprefixer -D`

```
// css
{
  test: /\.css$/,   // css 处理
  // use: 'css-loader'
  // use: ['style-loader', 'css-loader'],
  use: [
    // {
    //     loader: 'style-loader',
    //     options: {
    //         insertAt: 'top' // 将css标签插入最顶头  这样可以自定义style不被覆盖
    //     }
    // },
    MiniCssExtractPlugin.loader,
    'css-loader', // css-loader 用来解析@import这种语法,
    'postcss-loader'
  ]
}
// less
{
  test: /\.less$/,   // less 处理
  // use: 'css-loader'
  // use: ['style-loader', 'css-loader'],
  use: [
    // {
    //     loader: 'style-loader',
    //     options: {
    //         insertAt: 'top' // 将css标签插入最顶头  这样可以自定义style不被覆盖
    //     }
    // },
    MiniCssExtractPlugin.loader,   // 这样相当于抽离成一个css文件， 如果希望抽离成分别不同的css, 需要再引入MiniCssExtractPlugin，再配置
    'css-loader', // css-loader 用来解析@import这种语法
    'postcss-loader',
    'less-loader' // less-loader less -> css
    // sass node-sass sass-loader
    // stylus stylus-loader
  ]
},
```

postcss 需要配置文档   `postcss.config1.js`

[postcss-loader](https://github.com/postcss/postcss-loader)

```
module.exports = {
  plugins: [
    require('autoprefixer')
  ]
}
```

## es6 转 es5

`npm i babel-loader @babel/core  @babel/preset-env -D`

```
module.exports = {
  module: {
    rules: [
      {
        test: /\.js$/,
        use: {
          loader: 'babel-loader',
          options: {
            presets: [ //预设
              '@babel/preset-env' 
            ],
            plugins:[
              // 转es7的语法
              ["@babel/plugin-proposal-decorators", { "legacy": true }],
              ["@babel/plugin-proposal-class-properties", { "loose" : true }]
            ]
          }
        },
        exclude: /node_modules/
      }
    ]
  }
}

```


## 转es7的语法

```
// 转class
npm i @babel/plugin-proposal-class-properties -D

// 转装饰器
npm i @babel/plugin-proposal-decorators -D
```

配置如上

### 其他不兼容的高级语法

```
使用 @babel/polyfill
```

## 语法检查 eslint

`npm i eslint eslint-loader -S`

根目录添加 `.eslintrc.json` 配置文件

```
module.exports = {
  module: {
    rules: [
      {
        test: /\.js$/,
        use: {
          loader: 'eslint-loader',
          options: {
            enforce: 'pre'  // previous优先执行  post-普通loader之后执行
          }
        }
      },
      {
        test: /\.js$/,      // mormal 普通的loader
        use: {
          loader: 'babel-loader',
          options: {
            presets: [ //预设
              '@babel/preset-env' 
            ]
          }
        },
        exclude: /node_modules/
      }
    ]
  }
}

```

## 全局变量引入

jquery的引入

```
npm i jquery -S
```

```
let webpack = require('webpack')

new webpack.ProvidePlugin({
  $: 'jquery'
})
```

其他情况

1. 暴露全局

`npm i expose-loader -D` 暴露全局的`loader`

#### 法1：

可以在js中 `import $ from 'expose-loader?$!jquery'`   // 全局暴露jquery为$符号

可以调用`window.$`

#### 法2：

也可在`webpack.config.js` 中配置 `rules`

```
module.exports = {
  module: {
    rules: [
      {
        test: require.resolve('jquery'),
        use: 'expose-loader?$'
      }
    ]
  }
}

```
以后在`.js`文件中引入

```
import $ from 'jquery'
```

#### 法3. 如何在每个模块中注入：

```
let webpack = require('webpack')

module.exports = {
  plugins: [
    new webpack.ProvidePlugin({
      $: 'jquery'
    })
  ]
}

之后代码内直接使用 $
```
#### 法4：

在`index.html`中通过`script`标签引入`jquery`, 但是在`js`中，用`import`会重新打包`jquery`,如何避免

从输出的bundle 中排除依赖

```
module.exports = {
  externals: { // 告知webpack是外部引入的，不需要打包
    jquery: 'jQuery'
  }
}

```

此时在index.js上

```
import $ from 'jquery'

console.log($)
```

## webpack图片打包

1. js中创建
2. css中引入
3. `<img src="">`

`yarn add file-loader -D`

适合一二情况

```
module.export={
  module: {
    rules: [
      {
        test: /\.(png|jpg|gif)$/,
        use: 'file-loader'
      }
    ]
  }
}

```

默认会内部生成一张图片到build,生成图片的路径返回回来

第一种情况: 图片地址要`import`引入，直接写图片的地址，会默认为字符串

```
import logo from './logo.png'

let image = new Image()
image.src = logo
document.body.appendChild(image)
```

第二种情况: `css-loader`会将`css`里面的图片转为`require`的格式

```
div {
  background: url("./logo.png");
}
```

第三种情况: 解析`html`中的`image`

`yarn add html-withimg-loader -D`

```
{
  test: /\.html$/,
  use: 'html-withimg-loader'
}
```

## 当图片小于多少，用base64

`yarn add url-loader -D`

如果过大，才用`file-loader`

```
{
  test: /\.(png|jpg|gif)$/,
  // 当图片小于多少，用base64,否则用file-loader产生真实的图片
  use: {
    loader: 'url-loader',
    options: {
      limit: 200 * 1024,          // 小于200k变成base64
      // outputPath: '/img/',     // 打包后输出地址
      // publicPath: ''           // 给资源加上域名路径
    }
  }
}
```

## 打包文件分类

1.图片:

```
{
  test: /\.(png|jpg|gif)$/,
  // 当图片小于多少，用base64,否则用file-loader产生真实的图片
  use: {
    loader: 'url-loader',
    options: {
      limit: 1,  // 200k 200 * 1024
      outputPath: 'img/'   // 打包后输出地址 在dist/img
    }
  }
},
```

2.css:

```
plugins: [
  new MiniCssExtractPlugin({
    filename: 'css/main.css'
  }),
]
```

## 希望输出的时候，给这些`css\img`加上前缀，传到服务器也能访问

```
output: {
  filename: 'bundle.[hash:8].js',   // hash: 8只显示8位
  path: path.resolve(__dirname, 'dist'),
  publicPath: 'http://www.mayufo.cn'  // 给静态资源统一加
},
```


## 如果只希望处理图片

```
{
  test: /\.(png|jpg|gif)$/,
  // 当图片小于多少，用base64,否则用file-loader产生真实的图片
  use: {
    loader: 'url-loader',
    options: {
      limit: 1,  // 200k 200 * 1024
      outputPath: '/img/',   // 打包后输出地址
      publicPath: 'http://www.mayufo.cn'
    }
  }
}
```

## 打包多页应用

```
// 多入口
let path = require('path')
let HtmlWebpackPlugin = require('html-webpack-plugin')

module.exports = {
  mode: 'development',
  entry: {
    home: './src/index.js',
    other: './src/other.js'
  },
  output: {
    filename: "[name].js",
    path: path.resolve(__dirname, 'dist2')
  },
  plugins: [
    new HtmlWebpackPlugin({
      template: './index.html',
      filename: 'home.html',
      chunks: ['home']
    }),
    new HtmlWebpackPlugin({
      template: './index.html',
      filename: 'other.html',
      chunks: ['other', 'home']   // other.html 里面有 other.js & home.js
    }),
  ]
}

```

## 配置`source-map`

`yarn add @babel/core  @babel/preset-env babel-loader  webpack-dev-server -D`

```
module.exports = {
  devtool: 'source-map' // 增加映射文件调试源代码
}
```
1. 源码映射 会标识错误的代码 打包后生成独立的文件 大而全 「source-map」
2. 不会陈胜单独的文件 但是可以显示行和列  「eval-source-map」
3. 不会产生列有行，产生单独的映射文件  「cheap-module-source-map」
4. 不会产生文件 集成在打包后的文件中 不会产生列有行 「cheap-module-eval-source-map」


## `watch` 改完代表重新打包实体

```
module.exports = {
  watch: true,
  watchOptions: {
    poll: 1000,              // 每秒监听1000次
    aggregateTimeout: 300,   // 防抖，当第一个文件更改，会在重新构建前增加延迟
    ignored: /node_modules/  // 对于某些系统，监听大量文件系统会导致大量的 CPU 或内存占用。这个选项可以排除一些巨大的文件夹，
  },
}
```


## `webpack`的其他三个小插件

1. `cleanWebpackPlugin`

每次打包之前删掉dist目录
`yarn add clean-webpack-plugin -D`

[clean-webpack-plugin](https://github.com/johnagan/clean-webpack-plugin)

```
const CleanWebpackPlugin = require('clean-webpack-plugin');

module.exports = {
  output: {
    path: path.resolve(process.cwd(), 'dist'),
  },
  plugins: [
    new CleanWebpackPlugin('./dist')
  ]
}
```

2. `copyWebpackPlugin`

一些静态资源也希望拷贝的dist中

`yarn add copy-webpack-plugin -D`

```
const CopyWebpackPlugin = require('copy-webpack-plugin')

module.exports = {
  plugins: [
    new CopyWebpackPlugin([
      {from: 'doc', to: './dist'}
    ])
  ]
}
```

3. `bannerPlugin`内置模块

版权声明

```
const webpack = require('webpack');

new webpack.BannerPlugin('hello world')
// or
new webpack.BannerPlugin({ banner: 'hello world'})

```

## `webpack` 跨域

设置一个服务,由于`webpack-dev-server`内含`express`

[express](https://expressjs.com/zh-cn/starter/hello-world.html)

`server.js`

```
// express

let express = require('express')

let app = express();

app.get('/api/user', (res) => {
  res.json({name: 'mayufo'})
})

app.listen(3000)   // 服务端口在3000
```

写完后记得`node server.js`

访问 `http://localhost:3000/api/user` 可见内容


`index.js`

```
// 发送一个请求
let xhr = new XMLHttpRequest();

// 默认访问 http://localhost:8080  webpack-dev-server 的服务 再转发给3000
xhr.open('GET', '/api/user', true);

xhr.onload = function () {
  console.log(xhr.response)
}

xhr.send();

```


`webpack.config.js`

```
module.exports = {
  devServer: {
    proxy: {
      '/api': 'http://localhost:3000'
    }
  },
}
```

## 1.如果后端给的请求没有API 「跨域」

```
// express

let express = require('express')

let app = express();


app.get('/user', (res) => {
  res.json({name: 'mayufo'})
})

app.listen(3000)   // 服务端口在3000
```


请求已api开头, 转发的时候再删掉api

```
devServer: {
  proxy: {
    '/api': {
      target: 'http://localhost:3000',
      pathRewrite: {'^/api': ''}
    }
  }
}
```

## 2.前端只想单纯mock数据 「跨域」

```
devServer: {
  // proxy: {
  //     '/api': 'http://localhost:3000' // 配置一个代理
  // }
  //   proxy: {   // 重写方式 把请求代理到express 上
  //       '/api': {
  //           target: 'http://localhost:3000',
  //           pathRewrite: {'^/api': ''}
  //       }
  //   }
  before: function (app) {  // 勾子
    app.get('/api/user', (req, res) => {
      res.json({name: 'tigerHee'})
    })
  }
},
```

## 3.有服务端，不用代理, 服务端启动webpack 「跨域」

`server.js`中启动`webpack`

`yarn add webpack-dev-middleware -D`

`server.js`

```
// express

let express = require('express')
let webpack = require('webpack')
let app = express();


// 中间件
let middle = require('webpack-dev-middleware')

let config = require('./webpack.config')


let compiler = webpack(config)


app.use(middle(compiler))

app.get('/user', (req, res) => {
  res.json({name: 'mayufo'})
})


app.listen(3000)

```

## webpack解析resolve

以`bootstrap`为例

```
npm install bootstrap  -D
```

`index.js`

```
import 'bootstrap/dist/css/bootstrap.css'
```

报错
```
ERROR in ./node_modules/bootstrap/dist/css/bootstrap.css 7:0
Module parse failed: Unexpected token (7:0)
You may need an appropriate loader to handle this file type.
|  * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
|  */
> :root {
|   --blue: #007bff;
|   --indigo: #6610f2;
 @ ./src/index.js 22:0-42
 @ multi (webpack)-dev-server/client?http://localhost:8081 ./src/index.js

```

这是因为`bootstrap` 4.0的css引入了新的特性，CSS Variables

安装
`npm install postcss-custom-properties --save-dev`


配置`webpack.config.js`
```
{
  test: /\.css$/,
  use: ['style-loader', 'css-loader', {
    loader: 'postcss-loader',
    options: {
      plugins: (loader) => [
        require("postcss-custom-properties")
      ]
    }
  }]
}
```

## 但是每次引入都很长，如何优雅引入

```
resolve: {
  // 在当前目录查找
  modules: [path.resolve('node_modules')],
  alias: {
      'bootstrapCss': 'bootstrap/dist/css/bootstrap.css'
  }
},
```

```
import 'bootstrapCss'  // 在node_modules查找
```

## 省略扩展名

extensions:

```
resolve: {
  // 在当前目录查找
  modules: [path.resolve('node_modules')],
  // alias: {
  //   'bootstrapCss': 'bootstrap/dist/css/bootstrap.css'
  // },
  mainFields: ['style', 'main'],   // 先用bootstrap中在package中的style,没有在用main
  // mainFiles: []  // 入口文件的名字 默认index
  extensions: ['.js', '.css', '.json']  // 当没有拓展命的时候，先默认js、次之css、再次之json
},
```

## 定义环境变量

`DefinePlugin` 允许创建一个在编译时可以配置的全局常量。这可能会对开发模式和生产模式的构建允许不同的行为非常有用。

```
let url = ''
if (DEV === 'dev') {
  // 开发环境
  url = 'http://localhost:3000'
} else {
  // 生成环境
  url = 'http://www.mayufo.cn'
}
```

`webpack.config.js`

```
new webpack.DefinePlugin({
  // DEV: '"production"',
  DEV: JSON.stringify('production'),
  FLAG: 'true',   // 布尔
  EXPRESSION: '1 + 1'   // 字符串 如果希望是字符串 JSON.stringify('1 + 1')
})
```

## 区分两个不同的环境

分别配置不同的环境

- `webpack.base4.js`   基础配置
- `webpack.dev4.js`    开发环境
- `webpack.prod4.js`   生产环境

`yarn add webpack-merge -D`


`npm run build -- -- config webpack.dev4.js`
`npm run build -- -- config webpack.build.js`

[官方文档](https://webpack.docschina.org/guides/production/)


`webpack.base4.js`

```
let path = require('path')
let HtmlWebpackPlugin = require('html-webpack-plugin')
let CleanWebpackPlugin = require('clean-webpack-plugin')

module.exports = {
  entry: {
    home: './src/index.js'
  },
  output: {
    filename: "[name].js",
    path: path.resolve(process.cwd(), 'dist3')
  },
  module: {
    rules: [
      {
        test: /\.js$/,
        use: {
          loader: 'babel-loader',
          options: {
            presets: [
              '@babel/preset-env'
            ]
          }
        }
      },
      {
        test: /\.css$/,
        use: ['style-loader', 'css-loader', {
          loader: 'postcss-loader',
          options: {
            plugins: (loader) => [
              require("postcss-custom-properties")
            ]
          }
        }]
      }
    ]
  },
  plugins: [
    new HtmlWebpackPlugin({
      template: './src/index.html',
      filename: 'index.html'
    })
  ]
}

```

`webpack.dev4.js`

```
let merge = require('webpack-merge')
let base = require('./webpack.base4.js')

module.exports = merge(base, {
  mode: 'development',
  devServer: {},
  devtool: 'source-map'
})

```

`webpack.prod4.js`

```
let merge = require('webpack-merge')
let base = require('./webpack.base4.js')

module.exports = merge(base, {
  mode: 'production'
})

```

`package.json`

```
"scripts": {
  "build": "webpack  --config webpack.prod4.js",
  "dev": "webpack-dev-server --config webpack.dev4.js"
},
```


## webpack 优化

`yarn add webpack webpack-cli html-webpack-plugin @babel/core babel-loader @babel/preset-env @babel/preset-react -D`

`webpack.config.js`

```
let path = require('path')
let HtmlWebpackPlugin = require('html-webpack-plugin')


module.exports = {
  mode: 'development',
  entry: './src/index.js',
  output: {
    filename: 'main.js',
    path: path.resolve(__dirname, 'dist')
  },
  module: {
    rules: [
      {
        test: /\.js$/,
        use: {
          loader: 'babel-loader',
          options: {
            presets: [
              '@babel/preset-env',
              '@babel/preset-react'
            ]
          }
        }
      },
    ]
  },
  plugins: [
    new HtmlWebpackPlugin({
      template: './src/index.html',
      filename: 'index.html'
    }),
  ]
}

```
##  优化：当某些包是独立的个体没有依赖

以jquery为例，`yarn add jquery -D`,它是一个独立的包没有依赖，可以在webpack配置中，配置它不再查找依赖

```
module: {
    noParse: /jquery/, // 不用解析某些包的依赖
    rules: [
      {
        test: /\.js$/,
        use: {
          loader: 'babel-loader',
          options: {
            presets: [
              '@babel/preset-env',
              '@babel/preset-react'
            ]
          }
        }
      },
  ]
}

```
运行`npx webpack`

从2057ms  -> 1946 ms

## 优化：规则匹配设置范围

```
rules: [
  {
    test: /\.js$/,
    exclude: '/node_modules/',   // 排除
    include: path.resolve('src'),  // 在这个范围内
    use: {
      loader: 'babel-loader',
      options: {
        presets: [
          '@babel/preset-env',
          '@babel/preset-react'
        ]
      }
    }
  }
```

尽量实用`include`,不使用`exclude`,使用绝对路径

## 优化：忽略依赖中不必要的语言包
`yarn add moment webpack-dev-server -D`

忽略掉`moment`的其他语言包

```
let webpack = require('webpack')

plugins: [
    new webpack.IgnorePlugin(/\.\/locale/, /moment/)
]

```

`index.js`

```
import moment from 'moment'

let r = moment().endOf('day').fromNow()  // 距离现在多少天
console.log(r);
```


从 1.2MB 到  800kb

## 动态链接库

`yarn add react react-dom`

正常使用

`webpack.config.js`

```
{
  test: /\.js$/,
  exclude: '/node_modules/',
  include: path.resolve('src'),
  use: {
    loader: 'babel-loader',
    options: {
      presets: [
        '@babel/preset-env',
        '@babel/preset-react'
      ]
    }
  }
}
```

`index.js`
```
import React from 'react'

import {render} from 'react-dom'


render(<h1>111111</h1>, window.root)
```

`index.html`

```
<div id="root"></div>
```

独立的将`react react-dom` 打包好, 打包好再引用，从而减少`webpack`每次都要打包`react`

创建`webpack.config.react.js`


```
let path = require('path')
let webpack = require('webpack')
module.exports = {
  mode: 'development',
  entry: {
    // test: './src/test.js'
    react: ['react', 'react-dom']
  },
  output: {
    filename: '_dll_[name].js',  // 产生的文件名
    path: path.resolve(__dirname, 'dist'),
    library: '_dll_[name]',     // 给输出的结果加个名字
    // libraryTarget: 'var'   // 配置如何暴露 library
    // commonjs 结果放在export属性上， umd统一资源模块, 默认是var
  },
  plugins: [
    new webpack.DllPlugin({
      name: '_dll_[name]',   // name === library
      path: path.resolve(__dirname, 'dist', 'manifest.json')  // manifest.json 定义了各个模块的路径
    })
  ]
}
```

[libraryTarget](https://webpack.docschina.org/configuration/output/#%E6%9A%B4%E9%9C%B2%E4%B8%BA%E4%B8%80%E4%B8%AA%E5%8F%98%E9%87%8F)

`manifest.json`就是一个任务清单or动态链接库，在这个清单里面查找react

`npx webpack --config webpack.config.react.js`

在`index.html`增加引用

```
<body>
<div id="root"></div>
<script src="/_dll_react.js"></script>
</body>
```

在webpack.config.js 中配置，现在动态链接库`manifest.json`中查找,如果没有再打包react
```
plugins: [
  new webpack.DllReferencePlugin({
    manifest: path.resolve(__dirname, 'dist', 'manifest.json')
  })
]

```

[DLLPlugin 和 DLLReferencePlugin](https://webpack.docschina.org/plugins/dll-plugin/#src/components/Sidebar/Sidebar.jsx)

`npm run build`

打包后的`bunle.js`文件变小

`npm run dev`

可以理解为先把react打包，后面每次都直接使用react打包后的结果

## 多线程打包`happypack`

`yarn add happypack`

`webpack.config.js`

```
let Happypack = require('happypack')


rules: [
  {
    test: /\.js$/,
    exclude: '/node_modules/',
    include: path.resolve('src'),
    use: 'happypack/loader?id=js'
  },
]

plugins: [
  new Happypack({
    id: 'js',
    use: [{
      loader: 'babel-loader',
      options: {
        presets: [
          '@babel/preset-env',
          '@babel/preset-react'
        ]
      }
    }]
  })
]
```

js启用多线程，由于启用多线程也会浪费时间，因此当项目比较大的时候启用效果更好

css启用多线程
```

{
  test: /\.css$/,
  use: 'happypack/loader?id=css'
}

new Happypack({
  id: 'css',
  use: ['style-loader', 'css-loader']
}),
```

## webpack 自带的优化

`test.js`

```
let sum = (a, b) => {
  return a + b + 'sum'
}

let minus = (a, b) => {
  return a - b + 'minus';
}

export default {
  sum, minus
}
```

1. 使用import 

`index.js`

```
import calc from './test'

console.log(calc.sum(1, 2));
```


import在生产环境下会自动去除没有用的代码`minus`，这叫`tree-shaking`，将没有用的代码自动删除掉


`index.js`

```
let calc = require('./test')
console.log(calc);   // es 6导出，是一个default的对象
console.log(calc.default.sum(1, 2));
```

require引入es6 模块会把结果放在default上,打包build后并不会把多余`minus`代码删除掉，不支持`tree-shaking`


2. 作用域的提升

`index.js`

```
let a = 1
let b = 2
let c = 3
let d = a + b + c

console.log(d, '---------');
```
打包出来的文件

```
console.log(r.default.sum(1,2));console.log(6,"---------")
```

在webpack中可以省略一些可以简化的代码

## 抽取公共代码

1. 抽离自有模块

`webpack.config.js`

```
module.exports = {
  optimization: {
    splitChunks: {             // 分割代码块，针对多入口
      cacheGroups: {           // 缓存组
        common: {              // 公共模块
          minSize: 0,          // 大于多少抽离
          minChunks: 2,        // 使用多少次以上抽离抽离
          chunks: 'initial'    // 从什么地方开始, 从入口开始
        }
      }
    }
  },
}
```
[SplitChunksPlugin](https://webpack.docschina.org/plugins/split-chunks-plugin/)


分别有a.js和b.js, index.js和other.js分别引入a和b两个js

`index.js`

```
import './a'
import './b'

console.log('index.js');
```

`other.js`

```
import './a'
import './b'

console.log('other.js');
```

`webpack.config.js`

```
module.exports = {
  optimization: {
    splitChunks: {             // 分割代码块，针对多入口
      cacheGroups: {           // 缓存组
        common: {              // 公共模块
          minSize: 0,          // 大于多少抽离
          minChunks: 2,        // 使用多少次以上抽离抽离
          chunks: 'initial'    // 从什么地方开始, 从入口开始
        }
      }
    }
  },
}
```

2. 抽离第三方模块

比如jquery

`index.js` 和 `other.js`分别引入

```
import $ from 'jquery'

console.log($);
```

修改`webpack.config.js`配置：

```
optimization: {
  splitChunks: {              // 分割代码块，针对多入口
    cacheGroups: {            // 缓存组
      common: {               // 公共模块
        minSize: 0,           // 大于多少抽离
        minChunks: 2,         // 使用多少次以上抽离抽离
        chunks: 'initial'     // 从什么地方开始,刚开始
      },
      vendor: {
        priority: 1,          // 增加权重, (先抽离第三方)
        test: /node_modules/, // 把此目录下的抽离
        minSize: 0,           // 大于多少抽离
        minChunks: 2,         // 使用多少次以上抽离抽离
        chunks: 'initial'     // 从什么地方开始,刚开始
      }
    }
  },
},
```

## 懒加载(延迟加载)

`yarn add @babel/plugin-syntax-dynamic-import  -D`

`source.js`

```
export default 'mayufo'
```

`index.js`

```
let button = document.createElement('button')
button.innerHTML = 'hello'
button.addEventListener('click', function () {
  console.log('click')
  // es6草案中的语法，jsonp实现动态加载文件
  import('./source.js').then(data => {
    console.log(data.default)
  })
})
document.body.appendChild(button)

```

`webpack.config.js`

```
{
  test: /\.js$/,
  exclude: '/node_modules/',
  include: path.resolve('src'),
  use: [{
    loader: 'babel-loader',
    options: {
      presets: [
        '@babel/preset-env',
        '@babel/preset-react'
      ],
      plugins: [
        '@babel/plugin-syntax-dynamic-import'
      ]
    }
  }]
}
```

## 热更新(当页面改变只更新改变的部分，不重新打包)

`webpack.config.js`

```
plugins: [
  new HtmlWebpackPlugin({
    template: './src/index.html',
    filename: 'index.html'
  }),
  new webpack.NameModulesPlugin(),          // 打印更新的模块路径
  new webpack.HotModuleReplacementPlugin()  // 热更新插件
]
```

`index.js`

```

import str from './source'

console.log(str);

if (module.hot) {
  module.hot.accept('./source', () => {
    console.log('文件更新了');
    require('./source')
    console.log(str);
  })
}

```

## tapable介绍 - SyncHook

[tapable](https://juejin.im/post/5abf33f16fb9a028e46ec352)

`webpack`本质上是一种事件流的机制，它的工作流程就是将各个插件串联起来，而实现这一切的核心就是`Tapable`，`webpack`中最核心的负责编译的`Compiler`和负责创建`bundles`的`Compilation`都是`Tapable`的实例。

`SyncHook` 不关心监听函数的返回值

`yarn add tabable`

`1.use.js`

```
let {SyncHook} = require('tapable')   // 结构同步勾子


class Lesson {
  constructor () {
    this.hooks = {
      // 订阅勾子
      arch: new SyncHook(['name']),
    }
  }
  start () {
    this.hooks.arch.call('may')
  }
  tap () {   //  注册监听函数
    this.hooks.arch.tap('node', function (name) {
      console.log('node', name)
    })
    this.hooks.arch.tap('react', function (name) {
      console.log('react', name)
    })
  }
}


let l = new Lesson()

l.tap();  //注册两个函数
l.start() // 启动勾子

```

`1.theory.js`

```
class SyncHook {  // 勾子是同步的
  constructor(args) {  // args => ['name']
    this.tasks = []
  }
  tap (name, task) {
    this.tasks.push(task)
  }
  call (...args) {
    this.tasks.forEach((task) => task(...args))
  }
}

let hook = new SyncHook(['name'])

hook.tap('react', function (name) {
  console.log('react', name);
})


hook.tap('node', function (name) {
  console.log('node', name);
})


hook.call('jw')
```


## tapable介绍 - SyncBailHook

`SyncBailHook`为勾子加了个保险，当`return`返回不是`undefine`就会停止

`2.use.js`

```
let {SyncBailHook} = require('tapable')   // 解构同步勾子

class Lesson {
  constructor () {
    this.hooks = {
      // 订阅勾子
      arch: new SyncBailHook(['name']),

    }
  }
  start () {
    // 发布
    this.hooks.arch.call('may')
  }
  tap () {   //  注册监听函数,订阅
    this.hooks.arch.tap('node', function (name) {
      console.log('node', name)
      return '停止学习'  // 会停止
      // return undefined
    })
    this.hooks.arch.tap('react', function (name) {
      console.log('react', name)
    })
  }
}


let l = new Lesson()

l.tap();  //注册两个函数
l.start() // 启动勾子

```

`2.theory.js`

```
class SyncBailHook {  // 勾子是同步的
    constructor(args) {  // args => ['name']
        this.tasks = []
    }
    tap (name, task) {
        this.tasks.push(task)
    }
    call (...args) {
        let ret;   // 当前函数的返回值
        let index = 0; // 当前要执行的第一个
        do {
            ret = this.tasks[index](...args)
        } while (ret === undefined  && index < this.tasks.length)
    }
}

let hook = new SyncBailHook(['name'])

hook.tap('react', function (name) {
    console.log('react', name);
    return '停止学习'
    // return undefined
})


hook.tap('node', function (name) {
    console.log('node', name);
})


hook.call('jw')

```

## tapable介绍 - SyncWaterfallHook

`SyncWaterfallHook`上一个监听函数的返回值可以传给下一个监听函数
 
`3.use.js`
 
```
let {SyncWaterfallHook} = require('tapable')   // 解构同步勾子

// waterfall 瀑布

class Lesson {
    constructor () {
        this.hooks = {
            // 订阅勾子
            arch: new SyncWaterfallHook(['name']),

        }
    }
    start () {
        // 发布
        this.hooks.arch.call('may')
    }
    tap () {   //  注册监听函数,订阅
        this.hooks.arch.tap('node', function (name) {
            console.log('node', name)
            return '学的不错'
        })
        this.hooks.arch.tap('react', function (name) {
            console.log('react', name)
        })
    }
}


let l = new Lesson()

l.tap();  //注册两个函数
l.start() // 启动勾子

```

`3.theory.js`

```
class SyncWaterfallHook {  // 勾子是同步的 - 瀑布
    constructor(args) {  // args => ['name']
        this.tasks = []
    }
    tap (name, task) {
        this.tasks.push(task)
    }
    call (...args) {
        let [first, ...others] = this.tasks;
        let ret = first(...args)
        others.reduce((a, b) => {
            return b(a);
        }, ret);

    }
}

let hook = new SyncWaterfallHook(['name'])

hook.tap('react', function (name) {
    console.log('react', name);
    return 'react Ok'
    // return undefined
})


hook.tap('node', function (name) {
    console.log('node', name);
    return 'node Ok'
})

hook.tap('webpack', function (data) {
    console.log('webpack', data);
})



hook.call('jw')


```

## tapable介绍 - SyncLoopHook

`SyncLoopHook`当监听函数被触发的时候，如果该监听函数返回`true`时则这个监听函数会反复执行，如果返回 `undefined` 则表示退出循环

`4.use.js`

```
let {SyncLoopHook} = require('tapable')   // 解构同步勾子

// 不返回undefined 会多次执行

class Lesson {
    constructor () {
        this.index = 0
        this.hooks = {
            // 订阅勾子
            arch: new SyncLoopHook(['name']),

        }
    }
    start () {
        // 发布
        this.hooks.arch.call('may')
    }
    tap () {   //  注册监听函数,订阅
        this.hooks.arch.tap('node',  (name) => {
            console.log('node', name)
            return ++this.index === 3 ? undefined : '继续学'
        })
        this.hooks.arch.tap('react',  (name) => {
            console.log('react', name)
        })
    }
}


let l = new Lesson()

l.tap();  //注册两个函数
l.start() // 启动勾子

```

`4.theory.js`

```
class SyncLoopHook {  // 勾子是同步的 - 瀑布
    constructor(args) {  // args => ['name']
        this.tasks = []
    }
    tap (name, task) {
        this.tasks.push(task)
    }
    call (...args) {
        this.tasks.forEach(task => {
            let ret
            do {
                ret = task(...args);
            } while(ret !== undefined)
        })
    }
}

let hook = new SyncLoopHook(['name'])
let total = 0
hook.tap('react', function (name) {
    console.log('react', name);
    return ++total === 3 ? undefined: '继续学'
})


hook.tap('node', function (name) {
    console.log('node', name);
})

hook.tap('webpack', function (data) {
    console.log('webpack', data);
})



hook.call('jw')

```


## `AsyncParallelHook` 与 `AsyncParallelBailHook`

异步的勾子分两种`串行`和`并行`

`并行`等待所有并发的异步事件执行后执行回调

注册的三种方法

1. 异步的注册方法`tap`
2. 异步的注册方法`tapAsync`， 还有个回调参数
3. `topPromise`,注册`promise`

调用的三种

1. call (同步)
2. callAsync （异步）
3. promise （异步）

这里介绍的是异步并行的

#### AsyncParallelHook 

不关心监听函数的返回值。

`5.use.js`

```
let {AsyncParallelHook} = require('tapable')   // 解构同步勾子

// 不返回undefined 会多次执行

class Lesson {
    constructor() {
        this.index = 0
        this.hooks = {
            // 订阅勾子
            arch: new AsyncParallelHook(['name']),

        }
    }

    start() {
        // 发布callAsync
        // this.hooks.arch.callAsync('may', function () {
        //     console.log('end');
        // })
        // 另一种发布promise
        this.hooks.arch.promise('may').then(function () {
                console.log('end');
            }
        )
    }

    tap() {   //  注册监听函数,订阅
        // 注册tapAsync
        // this.hooks.arch.tapAsync('node',  (name, callback) => {
        //     setTimeout(() => {
        //         console.log('node', name)
        //         callback()
        //     }, 1000)
        // })
        // this.hooks.arch.tapAsync('react',  (name, callback) => {
        //     setTimeout(() => {
        //         console.log('react', name)
        //         callback()
        //     }, 1000)
        // })
        // 另一种订阅 tapPromise
        this.hooks.arch.tapPromise('node', (name) => {
            return new Promise((resolve, reject) => {
                setTimeout(() => {
                    console.log('node', name)
                    resolve()
                }, 1000)
            })
        })
        this.hooks.arch.tapPromise('react', (name) => {
            return new Promise((resolve, reject) => {
                setTimeout(() => {
                    console.log('react', name)
                    resolve()
                }, 1000)
            })
        })
    }
}


let l = new Lesson()

l.tap();  //注册两个函数
l.start() // 启动勾子


```


`5.theory.js`

```
class AsyncParallelHook {  // 勾子是同步的 - 瀑布
    constructor(args) {  // args => ['name']
        this.tasks = []
    }

    tapAsync(name, task) {
        this.tasks.push(task)
    }

    tapPromise(name, task) {
        this.tasks.push(task)
    }
    callAsync(...args) {
        let finalCallback = args.pop()   // 拿出最终的函数
        let index = 0
        let done = () => {   // 类似promise.all的实现
            index++;
            if (index === this.tasks.length) {
                finalCallback();
            }
        }
        this.tasks.forEach(task => {
            task(...args, done) // 这里的args 已经把最后一个参数删掉
        })
    }

    promise(...args) {
        let tasks = this.tasks.map(task => task(...args))
        return Promise.all(tasks)
    }
}

let hook = new AsyncParallelHook(['name'])


// hook.tapAsync('react', function (name, callback) {
//     setTimeout(() => {
//         console.log('react', name);
//         callback()
//     }, 1000)
// })
//
// hook.tapAsync('node', function (name, callback) {
//     setTimeout(() => {
//         console.log('node', name);
//         callback()
//     }, 1000)
// })

// hook.tapAsync('webpack', function (name, callback) {
//     setTimeout(() => {
//         console.log('webpack', name);
//         callback()
//     }, 1000)
// })

hook.tapPromise('react', function (name, callback) {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            console.log('react', name);
            resolve()
        }, 1000)
    })
})

hook.tapPromise('node', function (name, callback) {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            console.log('node', name);
            resolve()
        }, 1000)
    })
})



//
// hook.callAsync('jw', function () {
//     console.log('end');
// })


hook.promise('jw').then(function () {
    console.log('end');
})


```


#### AsyncParallelBailHook

只要监听函数的返回值不为 `null`，就会忽略后面的监听函数执行，直接跳跃到`callAsync`等触发函数绑定的回调函数，然后执行这个被绑定的回调函数。

使用和原理与`SyncBailHook`相似


## 异步串行 —— AsyncSeriesHook

`串行 `one by one

`6.use.js`

```
let {AsyncSeriesHook} = require('tapable')   // 解构同步勾子


class Lesson {
    constructor() {
        this.index = 0
        this.hooks = {
            // 订阅勾子
            arch: new AsyncSeriesHook(['name']),

        }
    }

    start() {
        // 发布
        // this.hooks.arch.callAsync('may', function () {
        //     console.log('end');
        // })
        // 另一种发布
        this.hooks.arch.promise('may').then(function () {
                console.log('end');
            }
        )
    }

    tap() {   //  注册监听函数,订阅
        // this.hooks.arch.tapAsync('node',  (name, callback) => {
        //     setTimeout(() => {
        //         console.log('node', name)
        //         callback()
        //     }, 1000)
        // })
        // this.hooks.arch.tapAsync('react',  (name, callback) => {
        //     setTimeout(() => {
        //         console.log('react', name)
        //         callback()
        //     }, 1000)
        // })
        // 另一种订阅
        this.hooks.arch.tapPromise('node', (name) => {
            return new Promise((resolve, reject) => {
                setTimeout(() => {
                    console.log('node', name)
                    resolve()
                }, 1000)
            })
        })
        this.hooks.arch.tapPromise('react', (name) => {
            return new Promise((resolve, reject) => {
                setTimeout(() => {
                    console.log('react', name)
                    resolve()
                }, 1000)
            })
        })
    }
}


let l = new Lesson()

l.tap();  //注册两个函数
l.start(); // 启动勾子

```

`6.theory.js`

```
class AsyncSeriesHook {  //
    constructor(args) {  // args => ['name']
        this.tasks = []
    }

    tapAsync(name, task) {
        this.tasks.push(task)
    }

    tapPromise(name, task) {
        this.tasks.push(task)
    }

    callAsync(...args) {
        let finalCallback = args.pop()
        let index = 0;
        let next = () => {
            if (this.tasks.length === index) return finalCallback();
            let task = this.tasks[index++];
            task(...args, next);
        }
        next();
    }

    promise(...args) {
        // 将promise串联起来
        let [first, ...other] = this.tasks
        return other.reduce((p, n) => {
             return p.then(() => n (...args))
        }, first(...args))
    }
}

let hook = new AsyncSeriesHook(['name'])


// hook.tapAsync('react', function (name, callback) {
//     setTimeout(() => {
//         console.log('react', name);
//         callback()
//     }, 1000)
// })
//
// hook.tapAsync('node', function (name, callback) {
//     setTimeout(() => {
//         console.log('node', name);
//         callback()
//     }, 1000)
// })
//
// hook.tapAsync('webpack', function (name, callback) {
//     setTimeout(() => {
//         console.log('webpack', name);
//         callback()
//     }, 1000)
// })


hook.tapPromise('react', function (name, callback) {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            console.log('react', name);
            resolve()
        }, 1000)
    })
})

hook.tapPromise('node', function (name, callback) {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            console.log('node', name);
            resolve()
        }, 1000)
    })
})




// hook.callAsync('jw', function () {
//     console.log('end');
// })


hook.promise('jw').then(function () {
    console.log('end');
})

```

## 异步串行 —— AsyncSeriesWaterfallHook

上一个监听函数的中的`callback(err, data)`的第二个参数,可以作为下一个监听函数的参数


`7.use.js`

```
let {AsyncSeriesWaterfallHook} = require('tapable')   // 解构同步勾子


class Lesson {
    constructor() {
        this.index = 0
        this.hooks = {
            // 订阅勾子
            arch: new AsyncSeriesWaterfallHook(['name']),

        }
    }

    start() {
        // 发布
        this.hooks.arch.callAsync('may', function () {
            console.log('end');
        })
        // 另一种发布
        // this.hooks.arch.promise('may').then(function () {
        //         console.log('end');
        //     }
        // )
    }

    tap() {   //  注册监听函数,订阅
        this.hooks.arch.tapAsync('node',  (name, callback) => {
            setTimeout(() => {
                console.log('node', name)
                // callback(null, 'result')
                callback('error', 'result')   // 如果放error, 会跳过直接后面的勾子，直接走到最终的

            }, 1000)
        })
        this.hooks.arch.tapAsync('react',  (name, callback) => {
            setTimeout(() => {
                console.log('react', name)
                callback()
            }, 1000)
        })
        // 另一种订阅
        // this.hooks.arch.tapPromise('node', (name) => {
        //     return new Promise((resolve, reject) => {
        //         setTimeout(() => {
        //             console.log('node', name)
        //             resolve()
        //         }, 1000)
        //     })
        // })
        // this.hooks.arch.tapPromise('react', (name) => {
        //     return new Promise((resolve, reject) => {
        //         setTimeout(() => {
        //             console.log('react', name)
        //             resolve()
        //         }, 1000)
        //     })
        // })
    }
}


let l = new Lesson()

l.tap();  //注册两个函数
l.start(); // 启动勾子

```

`7.theory.js`

```
class AsyncSeriesWaterfallHook {  //
    constructor(args) {  // args => ['name']
        this.tasks = []
    }

    tapAsync(name, task) {
        this.tasks.push(task)
    }

    tapPromise(name, task) {
        this.tasks.push(task)
    }
    callAsync(...args) {
        let finalCallback = args.pop()
        let index = 0;
        let next = (err, data) => {
            let task = this.tasks[index]
            if(!task) return finalCallback();
            if (index === 0) {
                // 执行的第一个
                task(...args, next)
            } else {
                task(data, next)
            }
            index ++
        }
        next();
    }

    promise(...args) {
        // 将promise串联起来
        let [first, ...other] = this.tasks
        return other.reduce((p, n) => {
             return p.then((data) => n(data))
        }, first(...args))
    }
}

let hook = new AsyncSeriesWaterfallHook(['name'])


// hook.tapAsync('react', function (name, callback) {
//     setTimeout(() => {
//         console.log('react', name);
//         callback(null, '结果1')
//     }, 1000)
// })
//
// hook.tapAsync('node', function (name, callback) {
//     setTimeout(() => {
//         console.log('node', name);
//         callback(null, '结果2')
//     }, 1000)
// })
//
// hook.tapAsync('webpack', function (name, callback) {
//     setTimeout(() => {
//         console.log('webpack', name);
//         callback()
//     }, 1000)
// })

//
hook.tapPromise('react', function (name, callback) {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            console.log('react', name);
            resolve('result')
        }, 1000)
    })
})

hook.tapPromise('node', function (name, callback) {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            console.log('node', name);
            resolve()
        }, 1000)
    })
})


//
//
// hook.callAsync('jw', function () {
//     console.log('end');
// })


hook.promise('jw').then(function () {
    console.log('end');
})

```


## 手写webpack

[对应的may-pack项目](https://github.com/mayufo/webpack-training)


`yarn add webpack webpack-cli -D`


`webpack.config.js`

```
let path = require('path')

module.exports = {
    mode: 'development',
    entry: './src/index.js',
    output: {
        filename: 'bundle.js',
        path: path.resolve(__dirname, 'dist')
    }
}
```

`npx webpack`

生成文件`bundle.js`

```
(function (modules) {
    var installedModules = {};

    function __webpack_require__(moduleId) {

        if (installedModules[moduleId]) {
            return installedModules[moduleId].exports;
        }
        var module = installedModules[moduleId] = {
            i: moduleId,
            l: false,
            exports: {}
        };

        modules[moduleId].call(module.exports, module, module.exports, __webpack_require__);

        module.l = true;

        return module.exports;
    }


    // Load entry module and return exports
    return __webpack_require__(__webpack_require__.s = "./src/index.js");
})
({
    "./src/a.js":
        (function (module, exports, __webpack_require__) {
            eval("let b = __webpack_require__(/*! ./base/b */ \"./src/base/b.js\")\n\nmodule.exports = 'a'+ b\n\n\n\n//# sourceURL=webpack:///./src/a.js?");
        }),
    "./src/base/b.js":
        (function (module, exports) {
            eval("module.exports = 'b'\n\n\n//# sourceURL=webpack:///./src/base/b.js?");
        }),
    "./src/index.js":
        (function (module, exports, __webpack_require__) {
            eval(" let str = __webpack_require__(/*! ./a.js */ \"./src/a.js\")\n\n console.log(str);\n\n\n//# sourceURL=webpack:///./src/index.js?");
        })

});

```

新建项目用于自己的`webpack`,这里叫`may-pack`

`yarn init`

如果在node里想执行命令，创建`bin`文件,再创建`may-pack.js`

配置`package.json`

```
{
  "name": "may-pack",
  "version": "1.0.0",
  "main": "index.js",
  "license": "MIT",
  "bin": {
    "may-pack": "./bin/may-pack.js"
  }
}
```

`may-pack.js`

```
#!  /usr/bin/env node 

// node环境

console.log('start');

```
运行`npm link`将npm 模块链接到对应的运行项目中去，方便地对模块进行调试和测试

在想运行`may-pack`的项目中运行，`npm link may-pack` 得到 `start`

## webpack分析及处理

`may-pack.js`

```
#!  /usr/bin/env node

// node环境

console.log('start');

let path = require('path')

// 拿到配置文件webpack.config.js
let config = require(path.resolve('webpack.config.js'));


let Compiler = require('../lib/Compiler.js');

let compiler = new Compiler(config);

// 标识运行编译
compiler.run()

```

创建`lib`文件`Compiler.js`

```
let path = require('path')
let fs = require('fs')

class Compiler {
    constructor(config) {
        // entry  output
        this.config = config
        // 需要保存入口文件的路径
        this.entryId = '';   // './src/index.js'
        // 需要保存所有的模块依赖
        this.modules = {};
        this.entry = config.entry  // 入口文件
        // 工作目录
        this.root = process.cwd(); // 当前运行npx的路径
    }
    
    // 构建模块
    buildModule(modulePath, isEntry) {
       
    }

    // 发射文件
    emitFile() {
        // 用数据 渲染想要的
    }

    run() {
        // 执行 创建模块的依赖关系
        this.buildModule(path.resolve(this.root, this.entry), true)  // path.resolve(this.root, this.entry) 得到入口文件的绝对路径
        // 发射打包后的文件
        this.emitFile()
    }
}

module.exports = Compiler

```
主要两个任务
1. 拿到入口Id
2. 解析模块，也就是实现`buildModule`方法

## 创建依赖关系

`may-pack`中`Compiler.js`

```

let path = require('path')
let fs = require('fs')
// babylon  主要把源码转成ast Babylon 是 Babel 中使用的 JavaScript 解析器。
// @babel/traverse 对ast解析遍历语法树 负责替换，删除和添加节点
// @babel/types 用于AST节点的Lodash-esque实用程序库
// @babel/generator 结果生成

let babylon = require('babylon')
let traverse = require('@babel/traverse').default;
let type = require('@babel/types');
let generator = require('@babel/generator').default
class Compiler {
    constructor(config) {
        // entry  output
        this.config = config
        // 需要保存入口文件的路径
        this.entryId = '';   // './src/index.js'
        // 需要保存所有的模块依赖
        this.modules = {};
        this.entry = config.entry  // 入口文件
        // 工作目录
        this.root = process.cwd(); // 当前运行npx的路径


    }
    // 拿到模块内容
    getSource (modulePath) {
        let content = fs.readFileSync(modulePath, 'utf8')
        return content
    }
    parse (source, parentPath) {
        console.log(source, parentPath)
    }
    // 构建模块
    buildModule(modulePath, isEntry) {
        // 拿到模块内容
        let source = this.getSource(modulePath)  // 得到入口文件的内容
        // 模块id modulePath(需要相对路径) = modulePath(模块路径) - this.root(项目工作路径)   src/index.js
        let moduleName = './' + path.relative(this.root, modulePath)
        console.log(source, moduleName);  // 拿到代码 和相对路径 ./src/index.js
        if (isEntry) {
            this.entryId = moduleName
        }
        let {sourceCode, dependencies} = this.parse(source, path.dirname(moduleName))   // ./src
        // 把相对路径和模块中的内容对应起来
        this.modules[moduleName] = sourceCode
    }

    // 发射文件
    emitFile() {
        // 用数据 渲染想要的
    }

    run() {
        // 执行 创建模块的依赖关系
        this.buildModule(path.resolve(this.root, this.entry), true)  // path.resolve(this.root, this.entry) 得到入口文件的绝对路径
        console.log(this.modules, this.entryId);
        // 发射打包后的文件
        this.emitFile()
    }


}

module.exports = Compiler


```

## ast递归解析

`parse`方法主要靠解析语法树来进行转义
`babylon`  主要把源码转成ast Babylon 是 Babel 中使用的 JavaScript 解析器。
`@babel/traverse` 对ast解析遍历语法树 负责替换，删除和添加节点
`@babel/types` 用于AST节点的Lodash-esque实用程序库
`@babel/generator` 结果生成


`yarn add babylon @babel/traverse @babel/types @babel/generator`

`may-pack`中`Compiler.js`

```
let path = require('path')
let fs = require('fs')
// babylon  主要把源码转成ast Babylon 是 Babel 中使用的 JavaScript 解析器。
// @babel/traverse 对ast解析遍历语法树 负责替换，删除和添加节点
// @babel/types 用于AST节点的Lodash-esque实用程序库
// @babel/generator 结果生成

let babylon = require('babylon')
let traverse = require('@babel/traverse').default;
let type = require('@babel/types');
let generator = require('@babel/generator').default
class Compiler {
    constructor(config) {
        // entry  output
        this.config = config
        // 需要保存入口文件的路径
        this.entryId = '';   // './src/index.js'
        // 需要保存所有的模块依赖
        this.modules = {};
        this.entry = config.entry  // 入口文件
        // 工作目录
        this.root = process.cwd(); // 当前运行npx的路径


    }
    // 拿到模块内容
    getSource (modulePath) {
        let content = fs.readFileSync(modulePath, 'utf8')
        return content
    }
    parse (source, parentPath) {
        // AST解析语法树
        let ast = babylon.parse(source)
        let dependencies = []; // 依赖的数组
        // https://astexplorer.net/
        traverse(ast, {
            // 调用表达式
            CallExpression(p) {
                let node = p.node; //对应的节点
                if(node.callee.name === 'require') {
                   node.callee.name = '__webpack_require__'
                    let moduledName = node.arguments[0].value   // 取到模块的引用名字
                    moduledName = moduledName + (path.extname(moduledName) ? '': '.js');  // ./a.js
                    moduledName = './' + path.join(parentPath, moduledName)  // './src/a.js'
                    dependencies.push(moduledName)
                    node.arguments = [type.stringLiteral(moduledName)] // 改掉源码
                }
            }
        })
        let sourceCode = generator(ast).code
        return { sourceCode, dependencies }
    }
    // 构建模块
    buildModule(modulePath, isEntry) {
        // 拿到模块内容
        let source = this.getSource(modulePath)  // 得到入口文件的内容
        // 模块id modulePath(需要相对路径) = modulePath(模块路径) - this.root(项目工作路径)   src/index.js
        let moduleName = './' + path.relative(this.root, modulePath)
        // console.log(source, moduleName);  // 拿到代码 和相对路径 ./src/index.js
        if (isEntry) {
            this.entryId = moduleName
        }
        // 解析把source源码进行改造， 返回一个依赖列表
        let {sourceCode, dependencies} = this.parse(source, path.dirname(moduleName))   // ./src
        // 把相对路径和模块中的内容对应起来
        this.modules[moduleName] = sourceCode
        dependencies.forEach(dep => {  // 附模块的加载 递归加载
            this.buildModule(path.join(this.root, dep), false)
        })
    }

    // 发射文件
    emitFile() {
        // 用数据 渲染想要的
    }

    run() {
        // 执行 创建模块的依赖关系
        this.buildModule(path.resolve(this.root, this.entry), true)  // path.resolve(this.root, this.entry) 得到入口文件的绝对路径
        console.log(this.modules, this.entryId);
        // 发射打包后的文件
        this.emitFile()
    }


}

module.exports = Compiler

```

## 生成打包工具

使用ejs模板

`may-pack`中`main.ejs`
```
(function (modules) {
var installedModules = {};

function __webpack_require__(moduleId) {

if (installedModules[moduleId]) {
return installedModules[moduleId].exports;
}
var module = installedModules[moduleId] = {
i: moduleId,
l: false,
exports: {}
};

modules[moduleId].call(module.exports, module, module.exports, __webpack_require__);

module.l = true;

return module.exports;
}


// Load entry module and return exports
return __webpack_require__(__webpack_require__.s = "<%-entryId %>");
})({
<% for(let key in modules){ %>
    "<%- key %>":
    (function (module, exports,__webpack_require__) {
eval(`<%-modules[key] %>`);
}),
<% } %>
});

```

[ejs入门](https://ejs.bootcss.com/)

`yarn add ejs`


`may-pack`中`Compiler.js`

```
let ejs = require('ejs')
```

```
// 发射文件
    emitFile() {
        // 用数据 渲染想要的
        // 输出到那个目录下
        let main = path.join(this.config.output.path, this.config.output.filename)
        let templateStr = this.getSource(path.join(__dirname, 'main.ejs'))
        let code = ejs.render(templateStr, { entryId: this.entryId, modules: this.modules})
        this.assets = {}
        // 路径对应的代码
        this.assets[main] = code
        fs.writeFileSync(main, this.assets[main])
    }
```

在`webpack-training`项目中运行`npx may-pack`, 得到`bundle.js`,运行得到结果

## 增加loader

创建`loader`文件夹，创建`less-loader1.js`和`style-loader1.js`

`yarn add less`

[less使用](http://lesscss.cn/#using-less)

`less-loader1.js`

```
// 将less转为css
let less = require('less')

function loader(source) {
    let css = ''
    less.render(source, function (err, output) {
        css = output.css
    })
    css = css.replace(/\n/g, '\\n');
    return css
}

module.exports = loader

```

`style-loader1.js`

```
// 将css插入到html头部
function loader(source) {
    console.log(111);
    let style = `
    let style = document.createElement('style')
    style.innerHTML = ${JSON.stringify(source)}
    document.head.appendChild(style)
   `
    return style
}
module.exports = loader


// JSON.stringify(source) 可以将代码转为一行

```

`webpack.config.js`

```
let path = require('path')

module.exports = {
    mode: 'development',
    entry: './src/index.js',
    output: {
        filename: 'bundle.js',
        path: path.resolve(__dirname, 'dist')
    },
    module: {
        rules: [
            {
                test: /\.less$/,
                use: [
                    path.resolve(__dirname, 'loader', 'style-loader1'),
                    path.resolve(__dirname, 'loader', 'less-loader1')
                ]
            }
        ]
    }
}

```

创建`index.less`

```
body {
  background: red
}
```

`index.js`

```
 let str = require('./a.js')

 require('./index.less')

 console.log(str);

```

`may-pack`中`Compiler.js`

```
// 拿到模块内容
    getSource (modulePath) {
        // 匹配各种文件的规则
        let rules= this.config.module.rules;   // webpack.config.js 中rules的数组
        let content = fs.readFileSync(modulePath, 'utf8')

        for (let i = 0; i < rules.length; i++) {
            let rule = rules[i]
            let {test, use} = rule
            let len = use.length - 1

            if (test.test(modulePath)) {
                // console.log(use[len]);
                function normalLoader () {
                    // console.log(use[len--]);
                    let loader = require(use[len--])
                    content = loader(content)
                    // 递归调用loader 实现转化
                    if (len >= 0) {
                        normalLoader()
                    }
                }
                normalLoader()
            }

        }
        return content
    }
```

运行`npx may-pack`

## 增加plugins

`yarn add tapable`

`may-pack`中`Compiler.js`

```
constructor(config) {
        // entry  output
        this.config = config
        // 需要保存入口文件的路径
        this.entryId = '';   // './src/index.js'
        // 需要保存所有的模块依赖
        this.modules = {};
        this.entry = config.entry  // 入口文件
        // 工作目录
        this.root = process.cwd(); // 当前运行npx的路径

        this.hooks = {
            entryOption: new SyncHook(),  // 入口选项
            compile: new SyncHook(),      // 编译
            afterCompile: new SyncHook(),  // 编译完成
            afterPlugins: new SyncHook(),   // 编译完插件
            run: new SyncHook(),         // 运行
            emit: new SyncHook(),        // 发射
            done: new SyncHook()         // 完成
        }
        // 如果传递了plugins参数
        let plugins = this.config.plugins
        if (Array.isArray(plugins)) {
            plugins.forEach(plugin => {
                plugin.apply(this); // 这里只是appLy方法不是改变this指向
            })
        }
        this.hooks.afterPlugins.call()
    }
```

在`webpack.config.js`中写插件方法

```
class P {
    apply(compiler) {   // 这里只是appLy方法不是改变this指向
        // 绑定
        compiler.hooks.emit.tap('emit', function () {
            console.log('emit');
        })
    }
}

class P1 {
    apply(compiler) {   // 这里只是appLy方法不是改变this指向
        // 绑定
        compiler.hooks.afterPlugins.tap('emit', function () {
            console.log('afterPlugins');
        })
    }
}



module.exports = {
    mode: 'development',
    entry: './src/index.js',
    output: {
        filename: 'bundle.js',
        path: path.resolve(__dirname, 'dist')
    },
    module: {
        rules: [
            {
                test: /\.less$/,
                use: [
                    path.resolve(__dirname, 'loader', 'style-loader'),
                    path.resolve(__dirname, 'loader', 'less-loader')
                ]
            }
        ]
    },
    plugins: [
        new P(),
        new P1()
    ]
}
```

然后在各个地方调用

`may-pack`中`may-pack.js`


```
.....
// 调用
compiler.hooks.entryOption.call()
// 标识运行编译
compiler.run()
```

`may-pack`中`Compiler.js`
```
run() {
        this.hooks.run.call()

        this.hooks.compile.call()
        // 执行 创建模块的依赖关系
        this.buildModule(path.resolve(this.root, this.entry), true)  // path.resolve(this.root, this.entry) 得到入口文件的绝对路径
        // console.log(this.modules, this.entryId);
        this.hooks.afterCompile.call()
        // 发射打包后的文件
        this.emitFile()
        this.hooks.emit.call()
        this.hooks.done.call()
    }
```

运行`npx may-pack`


## loader


[手写loader](https://juejin.im/post/59e6a5de518825469c7461da)

`webapck.config.js`

```
let path = require('path')

module.exports = {
    mode: 'development',
    entry: './src/index',
    output: {
        filename: 'build.js',
        path: path.resolve(__dirname, 'dist')
    },
    module: {
        rules: [
            {
                test: /\.js/,
                use: 'loader1' // 如何找到这个loader1
            }
        ]
    },
}

```

创建`loader`文件`loader1.js`

```
console.log(22);

function loader(source) {  // loader的参数就是源代码
    return source
}
module.exports = loader

```


`webpack.config.js`

```
let path = require('path')

module.exports = {
    mode: 'development',
    entry: './src/index.js',
    output: {
        filename: 'build.js',
        path: path.resolve(__dirname, 'dist')
    },
    resolveLoader: {
      // 别名
      // alias: {
      //     loader1: path.resolve(__dirname, 'loader', 'loader1')
      // }
        modules: ['node_modules', path.resolve(__dirname, 'loader')]  // 先找node_modules, 再去loader中去找
    },
    module: {
        rules: [
            {
                test: /\.js$/,
                // use: [path.resolve(__dirname, 'loader', 'loader1')]
                use: 'loader1' // 如何找到这个loader1

            },
            // {
            //     test: /\.less$/,
            //     use: [
            //         path.resolve(__dirname, 'loader', 'style-loader'),
            //         path.resolve(__dirname, 'loader', 'less-loader')
            //     ]
            // }
        ]
    },
}

```
如何找到这个`loader1`

1. 通过配别名`alias`
2. 通过`modules`

`npx webpack`

## 配置多个loader

1. 数组方式

先分别在`loader`文件下创建，`loader2.js`和`loader3.js`

```

function loader(source) {  // loader的参数就是源代码
    console.log('loader2');  // loader3.js 类似
    return source
}
module.exports = loader

```

`webpack.config.js`

```
rules: [
    {
        test: /\.js$/,
        use: ['loader3', 'loader2', 'loader1']
    },
]
```

运行`npx webpack`,分别打出
```
loader1
loader2
loader3
```

2. 对象方式

```
rules: [
    {
        test: /\.js$/,
        use: ['loader3']
    },
    {
        test: /\.js$/,
        use: ['loader2']
    },
    {
        test: /\.js$/,
        use: ['loader1']
    }
]
```

运行`npx webpack`,分别打出

```
loader1
loader2
loader3
```


> `loader`的顺序: 从右到左, 从下到上


也可以通过配置不同的参数改变`loader`的执行顺序，`pre` 前面的， `post`在后面的， `normal`正常


```
{
    test: /\.js$/,
    use: ['loader1'],
    enforce: "pre"
},
{
    test: /\.js$/,
    use: ['loader2']
},
{
    test: /\.js$/,
    use: ['loader3'],
    enforce: "post"
},
```

`loader` 带参数执行的顺序: `pre  -> normal -> inline -> post`

`inline`为行内`loader`

在`loader`文件中新建`inlin-loader`

```

function loader(source) {  // loader的参数就是源代码
    console.log('inline');
    return source
}
module.exports = loader

```

`src/a.js`

```
module.exports = 'may'
```

`src/index`

```
console.log('hello')
let srt = require('-!inline-loader!./a')
```

1. `-!`禁用`pre-loader`和 `normal-loader`来处理了

```
loader1
loader2
loader3
inline
loader3
```



2. `!`禁用`normal-loader`

```
loader1
loader2
loader3
loader1
inline
loader3
```



3. `!!` 禁用`pre-loader`、`normal-loader`、`post-loader`,只能行内处理

```
loader1
loader2
loader3
inline
```

loader 默认由两部分组成`pitch`和`normal`

`user: [loader3, loader2, loader1]`


无返回值: 先执行pitch方法,从左到右，再获取资源


```

    pitch loader - 无返回值
    
pitch   loader3 → loader2 → loader1  
                                    ↘
                                      资源
                                    ↙
normal   loader3 ← loader2 ← loader1 
```

有返回值: 直接跳过后续所有的`loader`包括自己的,跳到之前的`loader`, 可用于阻断

[loader](https://webpack.docschina.org/api/loaders/)

```
user: [loader3, loader2, loader1]

    pitch loader - 有返回值
    
pitch   loader3 → loader2  loader1  
                     ↙               
               有返回值               资源
               ↙                      
normal  loader3  loader2  loader1 
```

`loadeer2.js`

```

function loader(source) {  // loader的参数就是源代码
    console.log('loader2');
    return source
}

loader.pitch = function () {
    return '111'
}
module.exports = loader

```

结果

```
loader3
```

## `babel-loader`实现

`yarn add @babel/core @babel/preset-env`

`webpack.config.js`

```
{
    test: '\.js$/',
    use: {
        loader: 'babel-loader2',
        options: {
            presets: [
                '@babel/preset-env'
            ]
        }
    }
}
```

在`loader`文件创建`babel-loader2.js`(如果你已经装过`babel-loader`)

拿到`babel`的参数

`yarn add loader-utils`


```
// 需要在webpack.config.js拿到babel的预设, 通过预设转换模块, 先引入babel
let babel = require('@babel/core')

// 拿到babel的参数 需要工具 loaderUtils
let loaderUtils =require('loader-utils')


function loader(source) {  // loader的参数就是源代码  这里的this就是loader的上下文
    let options = loaderUtils.getOptions(this)
    console.log(this.resourcePath, 444);   // [./src/index.js]
    let callback = this.async(); // babel的转换是异步的,同步的返回是不行的， 不能用return  同步就是直接掉用 异步会在async中
    babel.transform(source, {
        ...options,
        sourceMap: true,         // 是否设置sourceMap 还需要再webpack.config.js 中配置  devtool: 'source-map'
        filename: this.resourcePath.split('/').pop()   //  给生成的`source-map`指定名字
    }, function (err, result) {
        callback(err, result.code, result.map)   // 异步 参数分别是「错误 转化后的代码 和 sourceMap」
    })
    console.log(options);
    // return source  失效
}

module.exports = loader


```


`index.js`

```
class May {
    constructor () {
        this.name = 'may'
    }
    getName () {
        return this.name
    }
}


let may = new May()

console.log(may.getName());
```

`npx webpack`

## `banner-loader`实现(自创)

给所有匹配的`js`加一个注释

`webpack.config.js`

```
{    // 给所有匹配的`js`加一个注释
    test: /\.js$/,
    use: {
        loader: 'banner-loader',
        options: {
           text: 'may',
           filename: path.resolve(__dirname, 'banner.js')
        }
    }
}
```

`banner.js`

```
二次星球中毒
```


在`loader`文件创建`banner-loader.js`

`yarn add schema-utils` 校验自己写的`loader`格式是否正确

[schema-utils](https://github.com/webpack-contrib/schema-utils)

`banner-loader.js`

```
// 拿到loader的配置
let loaderUtils = require('loader-utils')
// 校验loader
let validateOptions = require('schema-utils')
// 读取文件
let fs = require('fs')  // 异步

function loader(source) {  // loader的参数就是源代码
    let options = loaderUtils.getOptions(this)
    let callback = this.async()  // 读取文件是异步
    let schema = {
        type: 'object',
        properties: {
            text: {
                type: 'string'
            },
            filename: {
                type: 'string'
            }
        }
    }
    validateOptions(schema, options, 'banner-loader')  // 自己的校验格式， 自己的写的配置， 对应的loader名字
    if (options.filename) {
        this.cacheable(false)  // 不要缓存  如果有大量计算 推荐缓存
        // this.cacheable && this.cacheable()
        this.addDependency(options.filename) // 自动增加依赖
        fs.readFile(options.filename, 'utf8', function (err, data) {
            callback(err, `/**${data}**/${source}`)
        })
    } else {
        callback(null, `/**${options.text}**/${source}`)
    }
    return source
}
module.exports = loader

```

优化:

1. 修改`banner.js`的内容后, `webpack`进行监控，打包`webapck.config.js`配置`watch: true`
2. `loader`缓存

## 实现`file-loader`和`url-loader`

`yarn add mime`

其主要用途是设置某种扩展名的文件的响应程序类型

[mime](https://github.com/broofa/node-mime#readme)

创建`file-loader.js1`

```
// 拿到babel的参数 需要工具 loaderUtils
let loaderUtils = require('loader-utils')

function loader(source) {  // loader的参数就是源代码
    // file-loader需要返回路径
    let filename = loaderUtils.interpolateName(this, '[hash].[ext]', {content: source })
    this.emitFile(filename, source) // 发射文件
    console.log('loader1');
    return `module.exports="${filename}"`
}
loader.raw = true // 二进制
module.exports = loader

```

创建`url-loader1.js`

```
// 拿到babel的参数 需要工具 loaderUtils
let loaderUtils = require('loader-utils')
let mime = require('mime')  // 途是设置某种扩展名的文件的响应程序类型

function loader(source) {  // loader的参数就是源代码
    let {limit} = loaderUtils.getOptions(this)
    console.log(this.resourcePath);
    if (limit && limit > source.length) {
        return `module.exports="data:${mime.getType(this.resourcePath)};base64,${source.toString('base64')}"`
    } else {
        return require('./file-loader1').call(this, source)
    }
}
loader.raw = true // 二进制
module.exports = loader

```

`webpack.config.js`

```
{
    test: /\.png$/,
    // 目的是根据图片生成md5 发射到dist目录下，file-loader 返回当前图片路径
    // use: 'file-loader'
    // 处理路径
    use: {
        loader: 'url-loader1',
        options: {
            limit: 200 * 1024
        }
    }
}
```

`index.js`引入图片

```
import p from './photo.png'

let img = document.createElement('img')
img.src = p
document.body.appendChild(img);

```


## `less-loader`和`css-loader`


先安装`less`

分别创建`style-loader2` `css-loader2` `less-loader2`

`style-loader1` 与 `less-loader1` 同之前的


## `css-loader`

主要用来处理`css`中的图片链接，需要把`url`转换成`require`


`webpack.config.js`

```
{
    test: /\.png$/,
    // 目的是根据图片生成md5 发射到dist目录下，file-loader 返回当前图片路径
    // use: 'file-loader'
    // 处理路径
    use: {
        loader: 'url-loader1',
        options: {
            limit: 200 * 1024
        }
    }
},
{
    test: /\.less$/,
    use: ['style-loader2', 'css-loader2', 'less-loader2']
}
```

创建`index.less`

```
@base: #f938ab;
body {
  background: @base;
  background: url("./photo.png");
}
```

`less-loader2.js`

```
// 将less转为css
let less = require('less')

function loader(source) {
    let css = ''
    // console.log(source, 2222);
    less.render(source, function (err, output) {
        // console.log(output);
        css = output.css
    })
    // css = css.replace(/\n/g, '\\n');
    return css
}

module.exports = loader
```


`css-loader2.js`

```
// css-loader 用来解析@import这种语法,包括css中引入的图片
function loader(source) {
    let reg = /url\((.+?)\)/g   // 匹配括号

    let pos = 0;
    let current;

    let arr = ['let list = []']

    while (current = reg.exec(source)) {
        let [matchUrl, g] = current   // matchUrl -> 'url("./photo.png")', g  -> '"./photo.png"'
        // console.log(matchUrl, g, 88);
        let lastIndex = reg.lastIndex - matchUrl.length    // 拿到css从开通到地址链接之前的index
        arr.push(`list.push(${JSON.stringify(source.slice(pos, lastIndex))})`)  // 拼入开始和地址之前的代码
        pos = reg.lastIndex
        arr.push(`list.push('url('+ require(${g}) +')')`)    // 拼入图片地址
    }
    arr.push(`list.push(${JSON.stringify(source.slice(pos))})`)  // 拼入地址到结尾的代码
    arr.push(`module.exports = list.join('')`)
    console.log(arr.join('\r\n'));
    // let list = []
    // list.push("body {\\n  background: #f938ab;\\n  background: ")
    // list.push('url('+ require("./photo.png") +')')
    // list.push(";\\n}\\n")
    // module.exports = list.join('')

    return arr.join('\r\n')
}
module.exports = loader

```

`style-loader2.js`

```
let loaderUtils = require('loader-utils')

// 将css插入到html头部
function loader(source) {
    let str = `
    let style = document.createElement('style')
    style.innerHTML = ${JSON.stringify(source)}
    document.head.appendChild(style)
   `
    return str
}


// style-loader写了pitch,有返回后面的跳过，自己的写不会走
loader.pitch = function (remainingRequest) {  // 剩余的请求
    console.log(loaderUtils.stringifyRequest(this, '!!' + remainingRequest, 99999999))
    // 让style-loader 处理 less-loader 和css-loader拼接的结果
    // 得到 /Users/liuhuimin/work/webpack/loader/css-loader2.js!/Users/liuhuimin/work/webpack/loader/less-loader2.js!/Users/liuhuimin/work/webpack/src/index.less
    // 剩余的请求 less-loader!css-loader!./index.less
    // console.log(remainingRequest, 1223);
    // require返回的就是css-loader处理好的结果require('!!css-loader!less-loader!./index.less')
    let str = `
    let style = document.createElement('style')
    style.innerHTML = require(${loaderUtils.stringifyRequest(this, '!!' + remainingRequest)})
    document.head.appendChild(style)
   `
    // stringifyRequest 绝对路径转相对路径
    return str
}
module.exports = loader

```


```
user: ['style-loader2', 'css-loader2', 'less-loader2']

    pitch loader - 有返回值
    
pitch   style-loader2 → css-loader2  less-loader2  
                     ↙               
               有返回值               资源
               ↙                      
normal  style-loader2  css-loader2  less-loader2
```

在`style-loader2`中 引用了`less-loader` `css-loader` 和`less`文件


## webpack 中的插件

`yarn add webpack webpack-cil -D`

`webpack.config.js`

```
let path = require('path')
let DonePlugin = require('./plugins/DonePlugins')
let AsyncPlugins = require('./plugins/AsyncPlugins')

module.exports = {
    mode: 'development',
    entry: './src/index.js',
    output: {
        filename: 'build.js',
        path: path.resolve(__dirname, 'dist')
    },
    plugins: [
        new DonePlugin(),    // 同步
        new AsyncPlugins()   // 异步
    ]
}

```

`node_modules/webpack/lib`中查看`Compiler.js`

1. 同步`plugins/DonePlugins`

打包完成

```
class DonePlugins {
    apply (compiler) {
        console.log(1);
        compiler.hooks.done.tap('DonePlugin', (stats) => {
            console.log('编译完成');
        })
    }
}


module.exports = DonePlugins

```


2. 异步`plugins/AsyncPlugins`

```
class AsyncPlugins {
    apply (compiler) {
        console.log(2);
        compiler.hooks.emit.tapAsync('AsyncPlugin', (complete, callback) => {
            setTimeout(() => {
                console.log('文件发射出来');
                callback()
            }, 1000)
        })
        compiler.hooks.emit.tapPromise('AsyncPlugin', (complete, callback) => {
            return new Promise((resolve, reject) => {
                setTimeout(() => {
                    console.log('文件发射出来 222');
                    resolve()
                }, 1000)
            })
        })
    }
}


module.exports = AsyncPlugins

```

## 文件列表插件

希望生成一个文件描述打包出来的文件

在`plugins`中新建`FileListPlugin`

```
class FileListPlugin {
    constructor ({filename}) {
        this.filename = filename
    }
    apply (compiler) {
        // 文件已经准备好了 要进行发射
        // emit
        compiler.hooks.emit.tap('FileListPlugin', (compilation) => {
            let assets = compilation.assets;
            console.log(assets, 55);
            let content = `## 文件名  资源大小\r\n`
            // [ [bundls.js, {}], [index.html, {}]]
            Object.entries(assets).forEach(([filename, stateObj]) => {
                content += `- ${filename}    ${stateObj.size()}\r\n`
            })
            // 资源对象
            assets[this.filename] = {
                source () {
                    return content;
                },
                size () {
                    return content.length
                }
            }
        })
    }
}

module.exports = FileListPlugin

```

```
let path = require('path')
let DonePlugin = require('./plugins/DonePlugins')
let AsyncPlugins = require('./plugins/AsyncPlugins')
let HtmlWebpackPlugin = require('html-webpack-plugin')
let FileListPlugin = require('./plugins/FileListPlugin')

module.exports = {
    mode: 'development',
    entry: './src/index.js',
    output: {
        filename: 'build.js',
        path: path.resolve(__dirname, 'dist')
    },
    plugins: [
        new DonePlugin(),
        new AsyncPlugins(),
        new HtmlWebpackPlugin({
            template: './src/index.html',
            filename: 'index.html'
        }),
        new FileListPlugin({
            filename: 'list.md'
        })
    ]
}

```

生成`list.md`


## 内联的`webpack`插件

新建`index.css`引入`index.js`

`yarn add css-loader mini-css-extract-plugin -D`

希望打包后`css、js`内联在`index.html`文件中

创建`plugins`中`InlineSourcePlugins.js`

`yarn add --dev html-webpack-plugin@next`

[HTML Webpack Plugin](https://github.com/jantimon/html-webpack-plugin)

`webpack.config.js`

```
let path = require('path')
let DonePlugin = require('./plugins/DonePlugins')
let AsyncPlugins = require('./plugins/AsyncPlugins')
let HtmlWebpackPlugin = require('html-webpack-plugin')
let FileListPlugin = require('./plugins/FileListPlugin')

let InlineSourcePlugins = require('./plugins/InlineSourcePlugins')

let MiniCssExtractPlugin = require('mini-css-extract-plugin')

module.exports = {
    mode: 'production',
    entry: './src/index.js',
    output: {
        filename: 'bundle.js',
        path: path.resolve(__dirname, 'dist')
    },
    module: {
        rules: [
            {
                test: /\.css$/,
                use: [MiniCssExtractPlugin.loader, 'css-loader']
            }
        ]
    },
    plugins: [
        // new DonePlugin(),
        // new AsyncPlugins(),
        new HtmlWebpackPlugin({
            template: './src/index.html',
            filename: 'index.html'
        }),
        new MiniCssExtractPlugin({
            filename: 'index.css'
        }),
        new InlineSourcePlugins({
            match: /\.(js|css)/
        }),
        // new FileListPlugin({
        //     filename: 'list.md'
        // })
    ]
}

```

`InlineSourcePlugins.js`

```
const HtmlWebpackPlugin = require('html-webpack-plugin')

// 把外链的标签编程内联的标签
class InlineSourcePlugins {
    constructor({match}) {
        this.reg = match  // 正则
    }

    // 处理某一个标签
    processTag(tag, compilation) {
        let newTag = {}
        let url = ''
        if (tag.tagName === 'link' && this.reg.test(tag.attributes.href)) {
            newTag = {
                tagName: 'style',
                attributes: {type: 'text/css'}
            }
            url = tag.attributes.href
        } else if (tag.tagName === 'script' && this.reg.test(tag.attributes.src)) {
            newTag = {
                tagName: 'script',
                attributes: {type: 'application/javascript'}
            }
            url = tag.attributes.src
        }
        if (url) {
            newTag.innerHTML = compilation.assets[url].source(); // 文件内容放到innerHTML属性中
            delete compilation.assets[url]   // 删除原有的资源
            return newTag
            // console.log(compilation.assets[url].source());
        }
        return tag
    }

    // 处理引入标签的数据
    processTags(data, compilation) {
        let headTags = []
        let bodyTags = []
        data.headTags.forEach(headTag => {
            headTags.push(this.processTag(headTag, compilation))
        })
        data.bodyTags.forEach(bodyTag => {
            bodyTags.push(this.processTag(bodyTag, compilation))
        })
        console.log({...data, headTags, bodyTags})
        return {...data, headTags, bodyTags}
    }



    apply(compiler) {
        // 通过webpackPlugin来实现  npm搜索  html-webpack-plugin
        compiler.hooks.compilation.tap('InlineSourcePlugins', (compilation) => {
            HtmlWebpackPlugin.getHooks(compilation).alterAssetTagGroups.tapAsync(
                'alertPlugin',
                (data, callback) => {
                    // console.log('======');
                    // console.log(data) // 插入html标签的数据
                    // console.log('======');
                    data = this.processTags(data, compilation)   // compilation.assets 资源的链接
                    callback(null, data)
                })
        })

    }
}

module.exports = InlineSourcePlugins

```


## 打包后自动发布

打包好的文件自动上传致七牛

需要这几个参数

```
bucket: ''  // 七牛的存储空间
domain: '',
accessKey: '', // 七牛云的两对密匙
secretKey: '' // 七牛云的两对密匙
```

注册七牛，并在对象存储里面,新建存储空间列表`test`,`bucket: 'test'`

内容管理外链接默认域名 `domain: 'xxxxxxxx'`

右上角个人面板里面个人中心,密钥管理分别对应`accessKey`和`secretKey`

[进入开发者中心](https://developer.qiniu.com/) -> SDK&工具 -> 官方SDK -> Node服务端文档 —> 文件上传


[node文件上传](https://developer.qiniu.com/kodo/sdk/1289/nodejs)



`npm install qiniu`

[compiler-hooks](https://webpack.docschina.org/api/compiler-hooks)


`webpack.config.js`

```
plugins: [
        new HtmlWebpackPlugin({
            template: './src/index.html',
            filename: 'index.html'
        }),
        new MiniCssExtractPlugin({
            filename: 'index.css'
        }),
        new UploadPlugin({
            bucket: 'test',  // 七牛的存储空间
            domain: 'poyrjyh1b.bkt.clouddn.com',
            accessKey: 'xxxxxx', // 七牛云的两对密匙
            secretKey: 'yyyyyy' // 七牛云的两对密匙
        })
    ]
```

`UploadPlugin.js`

```
let qiniu = require('qiniu')
let path = require('path')

class UploadPlugin {
    constructor (options = {}) {
        // 参考 https://developer.qiniu.com/kodo/sdk/1289/nodejs
        let { bucket = '', domain = '', accessKey = '', secretKey = ''} = options
        let mac = new qiniu.auth.digest.Mac(accessKey, secretKey)
        let putPolicy = new qiniu.rs.PutPolicy({
            scope: bucket
        });
        this.uploadToken = putPolicy.uploadToken(mac)
        let config = new qiniu.conf.Config();
        this.formUploader = new qiniu.form_up.FormUploader(config)
        this.putExtra = new qiniu.form_up.PutExtra()
    }
    apply (compiler) {
        compiler.hooks.afterEmit.tapPromise('UploadPlugin', (complication) => {
            let assets = complication.assets
            let promise = []
            Object.keys(assets).forEach(filename => {
                promise.push(this.upload(filename))
            })
            return Promise.all(promise)
        })
    }

    upload (filename) {
        return new Promise((resolve, reject) => {
            let localFile = path.resolve(__dirname, '../dist', filename)
            this.formUploader.putFile(this.uploadToken, filename, localFile, this.putExtra, function(respErr,
                                                                                 respBody, respInfo) {
                if (respErr) {
                    reject(respErr)
                }
                if (respInfo.statusCode == 200) {
                    resolve(respBody)
                } else {
                    console.log(respInfo.statusCode)
                    console.log(respBody)
                }
            });
        })
    }
}

module.exports = UploadPlugin

```

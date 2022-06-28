## less函数实现媒体查询

- 公用的less函数文件

如：mix.less

```less
@mq-width-md:768px;
@mq-width-lg:1024px;

// < 768px
.mediaQuerySm(@style) {
  @media screen and (max-width:@mq-width-md) {
    @style()
  }
}

// < 1024px
.mediaQueryMd(@style) {
  @media screen and (max-width:@mq-width-lg) {
    @style()
  }
}
```

- 实际组件引入并使用函数

```less
@import '~xxx/mix.less'; // 路径自定

.cls {
  padding: 20px;
  .mediaQueryMd({
    padding: 12px;
  });
  .mediaQuerySm({
    padding: 8px;
  });
}
```
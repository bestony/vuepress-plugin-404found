# Vuepress-Plugin-cleanmylink
![](https://github.com/bestony/vuepress-plugin-cleanmylink/workflows/Node%20CI/badge.svg) ![](https://github.com/bestony/vuepress-plugin-cleanmylink/workflows/Node.js%20Package/badge.svg)
一个用于检查 Vuepress 下所有的 Hyperlink ，返回所有的非 200 的链接

## 用法

1. 使用 `npm install --save vuepress-plugin-cleanmylink` 安装插件
2. 在 `.vuepress/config.js` 的 plugins 配置项目中加入插件配置，具体如下

```javascript
module.exports = {
  plugins: [
    ['vuepress-plugin-404found',{
    	allowState: [200,201,301,302,405],
    	fileName: 'link-with-error.txt',
    }]
  ]
}
```

- `allowState` 为允许通过的状态码，一般建议设置为 200,201,301,302。
- `fileName` 为导出链接时的对应文件。根据你自己的需求自定义。如果不需要导出，则设置此项目为 null

## LINCESE

[GPLV3](LICENSE)
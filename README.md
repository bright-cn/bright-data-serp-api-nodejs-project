# Bright Data 搜索引擎 API Node.js 项目
Bright Data 搜索引擎 API Node.js 样板代码

[![Bright Data 推广](https://github.com/bright-cn/Awesome-Web-Scraping/raw/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner%20CN.png)](https://www.bright.cn/)


[在 StackBlitz 编辑器中编辑 ⚡️](https://stackblitz.com/~/github.com/bright-cn/bright-data-serp-api-nodejs-project?file=index.js)

## Bright Data 搜索引擎 API 示例

本项目演示了如何使用 [Bright Data 的搜索引擎 API](https://www.bright.cn/products/serp-api)，通过 [Bright Data 搜索引擎 API](https://www.bright.cn/products/serp-api) 访问搜索引擎查询结果且不被屏蔽。


### 在 StackBlitz 中使用环境变量

1. 选择 `.env` 文件
2. 添加以下变量：
   - `BRIGHT_DATA_API_TOKEN`：你的 Bright Data [API 令牌](https://docs.brightdata.com/general/account/api-token)
   - `BRIGHT_DATA_ZONE`：你的 Bright Data 搜索引擎 API [区域](https://www.bright.cn/cp/zones)名称（例如 `serp_api1`）

### 直接配置

或者，直接在脚本中编辑 CONFIG 对象：

```javascript
const CONFIG = {
  apiToken: process.env.BRIGHT_DATA_API_TOKEN || 'YOUR_API_TOKEN', // Replace with your actual token
  zone: process.env.BRIGHT_DATA_ZONE || 'serp_api1',           // Replace with your SERP APIzone
  searchEngineQueryUrl: 'https://geo.brdtest.com/welcome.txt'                 // Replace with your search engine query URL
};
```

## 运行示例

1. 确保已配置 `API token` 和 `zone`
2. 在终端中运行 `node index.js`
3. 查看控制台输出中的结果

## 工作原理

1. 该脚本向 Bright Data 搜索引擎 API 端点发送 POST 请求
2. 请求中包含你的身份验证令牌和搜索引擎查询 URL
3. Bright Data 的搜索引擎 API 会访问该搜索引擎查询 URL
4. 响应将返回到你的脚本并显示在控制台中

## 故障排除

如果遇到错误：

- 验证你的 API 令牌是否正确
- 检查你的区域名称是否有效
- 确保搜索引擎查询 URL 的格式正确

## 修改示例

如需请求其他 URL：
1. 更新 CONFIG 对象中的 `searchEngineQueryUrl`
2. 再次运行脚本

## 其他资源

- [Bright Data 搜索引擎 API](https://docs.brightdata.com/scraping-automation/serp-api/introduction)
- [获取 API 令牌](https://docs.brightdata.com/general/account/api-token)
- [管理区域](https://www.bright.cn/cp/zones)

**注意：** 这是一个用于教学目的的实现示例。用于生产环境时，请考虑添加额外的错误处理、日志记录和安全措施。

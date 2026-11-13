# Hello World 静态页面

最小化静态 HTML 页面，用于验证 loopforge1 仓库的前端交付链路（代码仓库 → 测试沙箱 welcome-test-sandbox → 构建/测试）是否跑通。

## 本地验证

### 方式一：直接用浏览器打开

双击或用浏览器打开 `index.html`（`file://` 方式），页面会显示 "Hello World"。

### 方式二：启动本地静态文件服务器

```bash
python3 -m http.server 8000
# 或
npx serve .
```

然后在浏览器访问 `http://127.0.0.1:8000/`，或执行：

```bash
curl -s http://127.0.0.1:8000/
```

响应体应包含字符串 `Hello World`，且 HTTP 状态码为 200。

## 说明

- 页面不依赖任何外部网络资源（无 CDN 字体/样式/脚本），断网环境下也可正常打开。
- `package.json` 中 `build` 脚本仅为空操作（`echo no-build-needed`），不引入任何真实构建工具链或依赖；仅用于兼容可能对 `npm run build` 进行探测的测试沙箱流程。

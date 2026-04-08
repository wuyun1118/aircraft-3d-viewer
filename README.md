# 3D Aircraft CAD Viewer

专业的飞机维修3D可视化工具，采用CAD线框风格。

## 部署方式

### 方式一：Vercel部署（推荐）

1. 访问 https://vercel.com 并登录（可用GitHub账号）
2. 点击 "New Project"
3. 将 `aircraft-3d-viewer` 文件夹拖拽到页面上
4. 点击 "Deploy" 部署
5. 部署完成后获得类似 `https://aircraft-3d-viewer.vercel.app` 的URL

### 方式二：GitHub Pages部署

1. 在GitHub创建新仓库
2. 上传 `index.html` 文件
3. 进入仓库 Settings → Pages
4. Source选择 "Deploy from a branch"
5. Branch选择 "main"，文件夹选择 "/ (root)"
6. 点击Save，等待部署完成
7. 访问 `https://你的用户名.github.io/仓库名`

### 方式三：Gitee Pages部署（国内访问快）

1. 访问 https://gitee.com 并登录
2. 创建新仓库
3. 上传 `index.html` 文件
4. 进入仓库 "服务" → "Gitee Pages"
5. 选择分支和目录，点击 "启动"
6. 访问 `https://你的用户名.gitee.io/仓库名`

## 使用方式

### URL参数

支持通过URL参数传递飞机信息：

```
https://your-domain.com/index.html?no=B-4680&model=Airbus%20A320neo&inDate=2025-04-06
```

参数说明：
- `no`: 飞机编号
- `model`: 机型
- `inDate`: 进厂日期

### iframe嵌入

```html
<iframe 
  src="https://your-domain.com/index.html?no=B-4680&model=Airbus%20A320neo" 
  width="100%" 
  height="600px" 
  frameborder="0"
  allowfullscreen
></iframe>
```

### JS API

父页面可以通过JavaScript调用：

```javascript
// 获取iframe
var iframe = document.getElementById('aircraft-viewer');

// 设置飞机数据
iframe.contentWindow.setAircraftData({
  no: 'B-8024',
  model: 'Boeing 737 MAX 8',
  inDate: '2025-03-31'
});
```

## 功能特性

- ✅ Three.js 3D渲染
- ✅ CAD线框风格
- ✅ 维修部位标记（红点闪烁/绿点）
- ✅ 点击标记查看详情
- ✅ 鼠标拖拽旋转、滚轮缩放
- ✅ 响应式设计
- ✅ URL参数传递
- ✅ iframe嵌入支持

## 技术栈

- Three.js 0.160.0
- 纯HTML/CSS/JavaScript
- 无需构建工具
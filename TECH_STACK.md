# 智能健康管家APP - 技术栈说明

## 前端技术

### 核心技术
- **HTML5**：语义化标签、新特性支持
- **CSS3**：Flexbox/Grid布局、动画、渐变、媒体查询
- **JavaScript (ES6+)**：现代JavaScript语法、箭头函数、模板字符串等

### UI设计
- **渐变配色**：蓝紫渐变主色调，符合健康科技感
- **毛玻璃效果**：backdrop-filter实现现代感
- **平滑动画**：CSS transitions和animations
- **响应式设计**：适配桌面端和移动端

### 浏览器API
- **Web Speech API**：语音合成(speechSynthesis)和语音识别(SpeechRecognition)
- **LocalStorage/SessionStorage**：本地数据持久化
- **DOM API**：动态元素创建和操作
- **Canvas/SVG**：数据可视化图表

## 数据处理

### 存储方案
```javascript
// 用户数据存储
localStorage.setItem('users', JSON.stringify(users));
localStorage.setItem('currentUser', username);

// 会话状态管理
sessionStorage.setItem('isLoggedIn', 'true');
```

### 疾病数据库
- 内置症状-疾病匹配系统
- 关键词识别与智能分析
- 多维度症状评估算法

### 食物数据库
- 常见食物营养成分数据
- 热量、蛋白质、脂肪、碳水化合物等
- 支持自定义添加食物

## AI功能实现

### AI智能问诊
- 关键词识别与提取
- 症状严重程度评估
- 智能建议生成
- 疾病风险预警

### AI健康分析
- 睡眠质量评分算法
- 活动能量消耗计算
- 健康状况综合评估
- 个性化建议生成

### AI语音陪伴
- 文本转语音（TTS）
- 语音转文本（STT）
- 多语言支持
- 语音交互流程控制

## 动画与交互

### CSS动画
```css
/* 缓动函数 */
cubic-bezier(0.175, 0.885, 0.32, 1.275)

/* 关键帧动画 */
@keyframes float { ... }
@keyframes fadeInUp { ... }
@keyframes heartbeat { ... }
```

### JavaScript交互
- 事件监听与处理
- 防抖与节流优化
- 滚动检测与视差效果
- 动态样式切换

## 响应式设计

### 断点设置
- **移动端**：< 768px
- **平板**：768px - 1024px
- **桌面端**：> 1024px

### 适配策略
- 流式布局
- 弹性图片
- 相对单位（rem、em、vw、vh）
- 媒体查询

## 性能优化

### 加载优化
- 内联关键CSS
- 延迟加载非关键资源
- 图片懒加载

### 渲染优化
- 使用CSS transform代替top/left
- 避免频繁的DOM操作
- 使用requestAnimationFrame

### 代码优化
- 事件委托
- 防抖与节流
- 内存泄漏预防

## 代码规范

### 命名规范
- 类名：BEM命名法（block__element--modifier）
- 变量：camelCase
- 常量：UPPER_SNAKE_CASE

### 文件结构
```
/
├── index.html              # 主页
├── login.html              # 登录页
├── demo.html               # AI问诊
├── food-diary.html         # 饮食管理
├── health-analysis.html    # 健康分析
├── voice-companion.html    # 语音陪伴
└── [各页面内嵌CSS/JS]
```

## 浏览器兼容性

### 支持的浏览器
- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

### 特性检测
```javascript
// Web Speech API检测
if ('speechSynthesis' in window) { ... }

// LocalStorage检测
if (typeof Storage !== 'undefined') { ... }
```

## 未来技术规划

### 框架升级
- React/Vue框架重构
- TypeScript类型支持
- 组件化开发

### AI增强
- 大语言模型API集成
- 计算机视觉（食物识别）
- 机器学习模型部署

### 后端支持
- Node.js/Express后端
- 数据库（MongoDB/PostgreSQL）
- 用户认证与授权

---

*文档版本：v1.0*
*最后更新：2026-05-17*

# 重定向页面
# "不良研究所" - 404 页面介绍

## 项目概述
本页面是一个充满创意的 404 错误页面，旨在为用户提供视觉吸引力和沉浸式的体验，同时引导用户自动跳转到最新发布的页面。这不仅提升了用户的体验，还确保了导航的顺畅性。

---

### 页面特色

#### 1. **动态背景与动画粒子效果**
页面以黑色背景为主，添加了动态浮动的粒子效果，粒子内容为“**不良研究所**”的字符，创造了一种科技感与神秘感交织的氛围。

- **动画实现**：通过 `@keyframes` 实现粒子的浮动效果，粒子大小及模糊效果均有所变化，赋予页面灵动的视觉效果。
- **多样粒子**：共生成了 80 个粒子，各自的动画时长、模糊程度和位置均有所不同，增加了随机性和丰富性。

#### 2. **内容区的渐现动画**
页面的主要内容通过 `animation` 实现渐现效果，内容框在加载时从透明状态逐渐显现，同时从下方向上移动，过渡流畅自然。

- **动画细节**：
  - 使用 `cubic-bezier` 进行缓动设计，确保动画更加柔和且真实。
  - 动画时长为 0.8 秒，延迟 1.2 秒后触发。

#### 3. **重定向逻辑**
该页面设计了一个自动跳转功能，用户在页面停留 5 秒后会被自动重定向到最新的发布页面。用户也可以通过按钮实现手动跳转。

- **倒计时显示**：页面动态显示剩余秒数，倒计时为 5 秒，清晰提示用户重定向状态。
- **用户控制权**：提供“点此重定向”按钮，用户可自主跳转到目标页面。

#### 4. **精简风格与自适应设计**
内容区采用黑底白字的极简设计，结合现代字体和居中布局，确保页面风格一致且能适配不同的设备屏幕。

- **自适应布局**：使用 `flexbox` 实现居中布局，同时保证页面在各类屏幕上的表现一致。
- **移动优先设计**：通过 `max-width` 和 `viewport` 元信息确保内容在移动设备上的清晰呈现。

---

### 代码亮点

#### 样式
```css
body {
    margin: 0;
    font-size: 20px;
    background: black;
    color: white;
    font-family: Arial, sans-serif;
}

.container {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    overflow: hidden;
}
```

#### 粒子动画
```css
@keyframes float {
    0%, 100% {
        transform: translateY(0);
    }
    50% {
        transform: translateY(180px);
    }
}
```

#### 倒计时逻辑
```javascript
let timeLeft = 4;
const countdown = setInterval(() => {
    if (timeLeft == 0) {
        clearInterval(countdown);
    }
    document.getElementById("countdown").innerHTML = timeLeft;
    timeLeft--;
}, 1000);
```

---

### 项目部署
此页面可直接部署于静态网站，或作为 404 错误页面配置于服务器（如 Apache、Nginx 或 Cloudflare）。其结构简单，所有动画和逻辑均通过 HTML、CSS 和原生 JavaScript 实现，具有极高的兼容性。

---

### 访问方式
- **项目名称**：不良研究所 - 404 页面
- **项目地址**：[https://dizhi66.top](https://dizhi66.top)

此页面欢迎改进与二次开发！

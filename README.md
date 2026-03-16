# 色彩选择器

这是一个使用Next.js和React开发的色彩选择器应用，具有以下功能：

## 功能特性

- **色轮选择**：使用直观的色轮界面选择颜色
- **两种选择模式**：
  - 自由选择模式：用户可以独立选择两种颜色
  - 推荐选择模式：用户选择一种颜色后，系统自动推荐最佳搭配颜色
- **渐变预览**：实时预览两种颜色的渐变效果
- **色彩推荐算法**：基于互补色原理生成推荐颜色

## 技术栈

- Next.js 14
- React 18
- TypeScript
- react-color（颜色选择器库）

## 安装和运行

### 安装依赖

```bash
npm install
```

### 开发模式运行

```bash
npm run dev
```

应用将在 http://localhost:3000 启动

### 构建生产版本

```bash
npm run build
npm start
```

## 项目结构

```
selectColor/
├── src/
│   └── pages/
│       ├── index.tsx   # 主应用页面
│       └── test.tsx    # 测试页面
├── package.json
├── tsconfig.json
└── README.md
```

## 色彩推荐算法

色彩推荐算法基于互补色原理：

1. 将用户选择的颜色从HEX格式转换为RGB格式
2. 将RGB转换为HSL（色相、饱和度、亮度）格式
3. 计算互补色相（色相值+180度）
4. 使用相同的饱和度和亮度生成互补色
5. 将互补色转换回HEX格式

## 测试

访问 http://localhost:3000/test 查看色彩推荐算法的测试结果

## 使用说明

1. 在主页面选择「自由选择模式」或「推荐选择模式」
2. 在自由模式下，分别调整两种颜色
3. 在推荐模式下，调整第一种颜色，第二种颜色会自动生成
4. 查看渐变预览效果
5. 复制生成的颜色代码使用

## 示例

### 自由选择模式

![自由选择模式](https://trae-api-cn.mchost.guru/api/ide/v1/text_to_image?prompt=color%20picker%20interface%20with%20two%20color%20wheels%20and%20gradient%20preview&image_size=landscape_16_9)

### 推荐选择模式

![推荐选择模式](https://trae-api-cn.mchost.guru/api/ide/v1/text_to_image?prompt=color%20picker%20interface%20with%20one%20active%20color%20wheel%20and%20one%20disabled%20color%20wheel%20with%20gradient%20preview&image_size=landscape_16_9)
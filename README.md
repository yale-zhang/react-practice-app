This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Target 
    - [x] 常用组件 
    - [x] react.js 练习

## 开发  

1. 隔离开发组件 
    通常，在应用程序中，你有许多 UI 组件，并且每个组件都有许多不同的 states(状态) 例如，一个简单的按钮组件可以具有以下 states(状态)：
    在常规状态下，带有文本标签。    
       * 在禁用模式下。
       * 处于加载状态。
       * 通常，如果没有运行示例应用程序或一些示例，很难看到这些状态。 
    Storybook 是 React UI 组件的开发环境。 它允许你浏览组件库，查看每个组件的不同状态，以及交互式开发和测试组件。  
    在应用程序的目录中运行以下命令:  
       `npx -p @storybook/cli sb init`  
2. 分析 Bundle (包) 大小  
    Source map explorer 使用 source maps 分析 JavaScript 包。 这有助于了解代码膨胀的来源。
        `npm install --save source-map-explorer`  
    然后在 package.json 中，将以下行添加到 scripts 中：
   "scripts": {
      "analyze": "source-map-explorer build/static/js/main.*",
   }
   然后分析 bundle(包) 运行生产构建然后运行分析脚本。

## 组件
- 评论功能  
    1. 页面加载完成自动聚焦到评论输入框。 
    2. 把用户名持久化，存放到浏览器的LocalStorage中。(页面加载时会把用户名加载出来显示到输入框，用户就不需要重新输入用户名了。)
    3. 把已发布的评论持久化，存放到浏览器的LocalStorage中。(页面加载时会把已保存的评论加载出来，显示到页面的评论列表上。)
    4. 评论显示发布日期，如“1秒前”，“30分钟前”，并且会每隔5秒更新发布日期。
    5. 评论可以被删除。
    6. 类似Markdown的行内代码块显示功能，用户输入的用‘’包含起来的内容都会被处理成用<code>元素包含。



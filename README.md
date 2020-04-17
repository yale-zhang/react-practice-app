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

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.


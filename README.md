## 利用robot-gallery创建项目
创建ts项目
npm create-react-app robot-gallery --template typescript
### 引入样式小结
1. 直接引入整个css文件
import './index.css'
<div className="app"/>
2. JSS模块化引入组件
import styles from './index.css'
<div className={styles.app}>
 
### 实现方式
 
 1) 首先声明 在根目录创建custom.d.ts 
 
 declare module "*.css"{
    const css:{[key:string]:string}
    export default css
 } 
 
 2) 对css的文件设置文件名为xxx.module.css 
 
 3) 在需要使用样式的文件中导入 
 
  import styles from './xxx.module.css'
 
 4) 在需要的组件中使用 
 
  <div className={styles.yyy}>
安装插件
   npm install typescript-plugin-css-modules --save-dev
配置插件
   在根目录创建一个.vscode文件/settings
   
   在settings下
   {
    "typescript.tsdk": "node_modules/typescript/lib",
    "typescript.enablePromptUseWorkspaceTsdk": true
}
   解析css文件并且生成typescript所对应的引用类型
   


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
#### 1) 首先声明 在根目录创建custom.d.ts 
 declare module "*.css"{
    const css:{[key:string]:string}
    export default css
} 
#### 2) 对css的文件设置文件名为xxx.module.css 
#### 3) 在需要使用样式的文件中导入 
  import styles from './xxx.module.css' 
#### 4) 在需要的组件中使用 
  <div className={styles.yyy}>
```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/kennis-wang/giterror/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

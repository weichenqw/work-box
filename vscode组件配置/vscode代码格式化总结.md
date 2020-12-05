

### 								vscode代码格式化设置参考

#### 目的：

​		统一团队代码风格和格式，保证项目顺利进行，方便组员阅读和修改代码

#### 格式化概念：

​		代码检查：依据一种指定代码格式，提示出不符合格式的代码（EsLint）

​		代码格式化：依据一种指定代码格式，修正不符合格式的代码（Prettier，Beutiful）

#### vscode代码格式化组件：

​	单一组件不足以满足开发需要，目前个人vscode安装的格式化组件有：

- 设定 JavaScript 代码格式 ，安装插件 [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)   ，添加配置文件`.editorconfig`即可， 可以设置部分的基本格式，然后使用编辑器默认的格式化 

  `.editorconfig`示例：

  ```
  root = true
  
  [*]                             # [] 内是正则表达式，匹配文件
  charset = utf-8                 # 文本格式
  end_of_line = lf                # 配置结尾符号
  insert_final_newline = true     # 文件末尾空行
  indent_style = space            # 缩进使用空格
  indent_size = 2                 # 缩进长度
  trim_trailing_whitespace = true # 去掉行尾多余的空格
  。
  ```

-  安装Prettier()，beutiful（），两个同为代码美化工具

-  Prettier插件配置：

  ```
   "prettier": {
        //设置分号
        "semi": true,
        //双引号变成单引号
        "singleQuote": true,
        //禁止随时添加逗号
        "trailingComma": "none"
      }
  ```
  
- beutiful（）插件配置：
```
   默认美化的文件类型，扩展名或特定文件名
   "beautify.language": {
    "js": {
      "type": ["javascript", "json", "jsonc"],
      "filename": [".jshintrc", ".jsbeautifyrc"]
    },
    "css": ["css", "less", "scss"],
    "html": ["htm", "html"]
  },
  定义默认的格式化程序
  "[css]": {
      "editor.defaultFormatter": "HookyQR.beautify"
    },
    "[json]": {
      "editor.defaultFormatter": "HookyQR.beautify"
    },
    "[scss]": {
      "editor.defaultFormatter": "HookyQR.beautify"
    },
    "[javascript]": {
      "editor.defaultFormatter": "HookyQR.beautify"
    },
    "[html]": {
      "editor.defaultFormatter": "HookyQR.beautify"
    },
    "[jsonc]": {
      "editor.defaultFormatter": "HookyQR.beautify"
    },

```
- Vetur：vue代码高亮，除了支持template模板以外，还支持大多数主流的前端开发脚本和插件，比如Sass和TypeScript ：

  ```
"[vue]": {
      "editor.defaultFormatter": "octref.vetur" //vue代码格式采用vetur
   },
  ```
  
-   eslint：运行项目时，检查代码是否符合ESlint规范

  eslint和prettier关系时相互依存，eslint检错（质量检测），prettier纠错（风格检测），两者的校验规则同样依据.eslintrc.js文件配置
  
  ```
  "eslint.codeAction.showDocumentation": {
      "enable": true
    },//在“快速修复”菜单中显示“打开lint规则文档”网页。默认情况下为true
  ```
  
- .eslintrc.js 文件配置：

  ```
  module.exports = {
    root: true,
    parserOptions: {
      parser: 'babel-eslint'
    },
    env: {
      browser: true,
    },
    extends: [
    error-prevention
    `plugin:vue/recommended` for stricter rules.
      'plugin:vue/essential',
      'standard'
    ],
    plugins: [
      'vue'
    ],
    rules: {
      'generator-star-spacing': 'off',
      'no-debugger': process.env.NODE_ENV === 'production' ? 'error' : 'off',
    }
  }
  
  ```

  

- settings.json文件全部配置

  ```
  {
    //editor默认配置
    "editor.formatOnType": true,
    "editor.formatOnSave": true, // 保存时自动格式化
    "editor.suggestSelection": "first", //默认选择建议列表的第一项
  
    "workbench.tree.indent": 20, //文件树缩进为20像素
  
    "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
    "[css]": {
      "editor.defaultFormatter": "HookyQR.beautify"
    },
    "[json]": {
      "editor.defaultFormatter": "HookyQR.beautify"
    },
    "[scss]": {
      "editor.defaultFormatter": "HookyQR.beautify"
    },
    "[javascript]": {
      "editor.defaultFormatter": "HookyQR.beautify"
    },
    "[html]": {
      "editor.defaultFormatter": "HookyQR.beautify"
    },
    "[vue]": {
      "editor.defaultFormatter": "octref.vetur" //vue代码格式采用vetur
    },
    "[jsonc]": {
      "editor.defaultFormatter": "HookyQR.beautify"
    },
  
    "eslint.codeAction.showDocumentation": {
      "enable": true
    },
    "beautify.config": "",
    "beautify.language": {
      "js": {
        "type": ["javascript", "json", "jsonc"],
        "filename": [".jshintrc", ".jsbeautifyrc"]
      },
      "css": ["css", "less", "scss"],
      "html": ["htm", "html"]
    },
    // 设置vetur风格工具，可扩展至css,js,scss等文件保持同一风格
    "vetur.format.defaultFormatter.html": "js-beautify-html",
    // 所有默认格式化程序的选项
    "vetur.format.defaultFormatterOptions": {
      // beautiful组件
      "js-beautify-html": {
        // #vue组件中html代码格式化样式
        "wrap_attributes": "force-aligned", //也可以设置为“auto”，效果会不一样
        "wrap_line_length": 200,
        "end_with_newline": false,
        "semi": true,
        "singleQuote": true
      },
      //prettier组件
      "prettier": {
        //设置分号
        "semi": true,
        //双引号变成单引号
        "singleQuote": true,
        //禁止随时添加逗号
        "trailingComma": "none"
      }
    }
  }
  
  ```

- 为不影响其他项目开发

    在项目下新建一个.vscode 目录和settings.json 文件, 这个文件就是**工作区设置,**相对于设置中的settings.json 文件优先级更高， 可以上传到项目配置库, 整个团队共享 

目前主要参考网络，完成了较基础项目的项目格式化配置，满足目前的项目开发，后续有新的需要可以随时提出并新增配置

推荐较为好用的vscode插件：

Auto Close Tag 自动闭合标签
Auto Rename Tag 自动重命名标签

Bracket Pair Colorizer 结对的括号颜色高亮

HTML CSS Support  html标签智能提示当前项目所支持的样式

Visual Studio IntelliCode 辅助预测开发者使用最可能正确的api

npm 包管理
npm intellisense // npm 自动补全

stylelint //格式化css代码
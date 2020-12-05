vscode插件：

Eslint: 代码检查工具;

Prettier - Code formatter :Visual Studio代码格式化程序;

Vetur 支持.vue文件语法高亮显示;



`setting.json文件配置`

```
    "window.zoomLevel": 0, //设置窗口缩放级别
    "files.autoSave": "afterDelay", //自动保存代码
    "breadcrumbs.enabled": true, // 开启 vscode 文件路径导航
    "search.exclude": { //用来忽略搜索的文件夹
        "**/bower_components": true,
        "**/node_modules": false
    },
    "diffEditor.ignoreTrimWhitespace": false, // 控制差异编辑器是否将对前导空格或尾随空格的更改显示为差异
    "terminal.integrated.fontSize": 16, // 控制终端的字号(以像素为单位)。
    // "terminal.integrated.shell.windows": "C:\\Windows\\System32\\cmd.exe", //设置访问终端的路径
    "git.path": "D:/Git/bin/git.exe", /*此路径为自己电脑git的安装路径  如果终端（terminal 使用git bash需要配置此项*/
    "git.confirmSync": false, //同步 Git 存储库前请先进行确认
    //eeditor部分-------------
    "editor.formatOnSave": true, //每次保存自动格式化
    "editor.formatOnPaste": true, // 编辑粘贴自动格式化
    "editor.wordWrapColumn": 400, // 400 列后换行
    "editor.mouseWheelZoom": true, // 通过使用鼠标滚轮同时按住 Ctrl 可缩放编辑器的字体
    "editor.lineHeight": 22, //设置文字行高
    // 控制是否在打开文件时，基于文件内容自动检测 Editor: Tab Size 和 Editor: Insert Spaces。如果设置为true则.editorconfi文件中的indent_size会失效
    "editor.detectIndentation": false,
    "editor.fontSize": 16, //设置字体大小
    "editor.tabSize": 4, // 因为设置了 "editor.detectIndentation": false 所以该设置仅对settings.json文件缩进起作用
    // 显示 markdown 中英文切换时产生的特殊字符
    "editor.renderControlCharacters": true,
    // 设置 eslint 保存时自动修复 【可修复function关键字后不带空格】
    "editor.codeActionsOnSave": {
        "source.fixAll.eslint": true
    },
    // ----------------eslint部分---------
    "eslint.alwaysShowStatus": true,
    // "eslint.provideLintTask": true,
    "eslint.quiet": true,
    "eslint.validate": [ //开启对.vue文件中错误的检查
        "javascript",
        "javascriptreact",
        "vue",
        "html"
    ],
    // prettier部分----------------------
    // "prettier.eslintIntegration": true, //让prettier使用eslint的代码格式进行校验   // 注释后面加空格
    "prettier.semi": false, //去掉代码结尾的分号
    "prettier.tabWidth": 4, // tab 大小为4个空格
    "prettier.singleQuote": true, //  #使用单引号替代双引号
    // vetur部分------------------------
    // vetur处理单文件组件格式化    支持格式化嵌入的html/css/scss/less/postcss/stylus/js/ts
    // 如果不设置这些项目格式化时会先进行vetur格式化 然后在进行eslint格式化
    // 关闭vetur格式化template标签,由prettier最终执行
    "vetur.format.defaultFormatter.html": "none",
    "vetur.format.defaultFormatter.js": "prettier",
    // "vetur.format.defaultFormatter.js": "vscode-typescript", // #让vue中的js按编辑器自带的ts格式进行格式化
    "vetur.format.defaultFormatter.less": "prettier",
    "vetur.validation.template": false, //因为使用了eslint-plugin-vue插件 避免vetur验证模板文件
    // "vetur.format.defaultFormatter.postcss": "prettier",
    "vetur.format.defaultFormatter.scss": "prettier",
    // "vetur.format.defaultFormatter.stylus": "stylus-supremacy",
    "vetur.format.defaultFormatter.ts": "prettier",
    "vetur.format.options.tabSize": 4, // tab 大小为4个空格
    "vetur.format.defaultFormatterOptions": {
        //项目中如果有prettierrc、.prettierrc.js等配置文件，否则会覆盖掉vscode上面的配置
        // 处理单文件中的js文件 继承自 prettier
        "prettier": {
            "semi": false, //是否使用分号
            "singleQuote": true
        },
        //取消vue强制换行【官方不推荐使用】
        // "js-beautify-html": {
        // "wrap_line_length": 160,
        //   "wrap_attributes": "auto",
        //   "end_with_newline": false
        // }
        // 处理单文件组件中的模板
        // 继承自prettyhtml格式化===> https://prettyhtml.netlify.com/     https://vuejs.github.io/vetur/formatting.html#settings
        "prettyhtml": {
            // 模板单行超过n个长度的时候开始换行显示各种参数和事件
            "printWidth": 200,
            //单文件组件html中是否使用单引号
            "singleQuote": true
            // "HTMLWhitespaceSensitivity": "ignore"
            // "bracketSpacing": true
            // "htmlWhitespaceSensitivity": "ignore",
        }
    },
    "vetur.experimental.templateInterpolationService": false, //防止单文件组件首行template报错
    "vetur.format.enable": true, // 是否启用vetur格式化程序 【需要重启vscode】
    // "[vue]": { //针对某种语言，配置替代编辑器设置。
    //     "editor.defaultFormatter": "octref.vetur"
    // },
    // 其他部分--------------
    "javascript.preferences.quoteStyle": "single",
    "javascript.format.insertSpaceBeforeFunctionParenthesis": true, //让函数(名)和后面的括号之间加个空格
    "quokka.compactMessageOutput": true, //vscode插件 实时观看 javascript 的变量的变化  //压缩消息输出
    "quokka.suppressExpirationNotifications": true, //禁止过期通知
    "liveServer.settings.donotShowInfoMsg": true, //关闭liveserver提示
    "search.quickOpen.includeSymbols": true, //  配置为在 Quick Open 文件结果中包括全局符号搜索的结果。
    "[javascript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    // "prettier.stylelintIntegration": true,
    "[jsonc]": {
        "editor.defaultFormatter": "vscode.json-language-features"
    },
    "[json]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[vue]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "files.associations": { //文件后缀类型的支持
        "*.cjson": "jsonc",
        "*.wxss": "css",
        "*.wxs": "javascript"
    },
    "files.exclude": { //用来忽略工程打开的文件夹
        "**/.git": true,
        "**/.svn": true,
        "**/.DS_Store": true,
        "**/node_modules": true,
        "**/iOS": true
    },
    //emmet能识别缩写语法的场景
    "emmet.includeLanguages": {
        "wxml": "html"
    },
    "minapp-vscode.disableAutoConfig": true //禁用自动配置 //微信小程序标签、属性的智能补全（同时支持原生小程序、mpvue 和 wepy 框架，并提供 snippets）
}

```

 *项目中如果有prettierrc、.prettierrc.js等配置文件，否则会覆盖掉vscode上面的配置* 


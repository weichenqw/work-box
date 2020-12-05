1.  **vetur-设置风格工具** 

```
"vetur.format.defaultFormatter.html": "prettyhtml",
"vetur.format.defaultFormatter.css": "prettier",
"vetur.format.defaultFormatter.postcss": "prettier",
"vetur.format.defaultFormatter.scss": "prettier",
"vetur.format.defaultFormatter.less": "prettier",
"vetur.format.defaultFormatter.stylus": "stylus-supremacy",
"vetur.format.defaultFormatter.js": "prettier",
"vetur.format.defaultFormatter.ts": "prettier",
"vetur.format.defaultFormatter.sass": "sass-formatter"
```

```
  "vetur.format.options.tabSize": 2,
  "vetur.format.options.useTabs": false
  当.prettierrc和.eslintrc.js存在时,他会被覆盖. 
```

2. **vetur-设置prettier风格** 

```
"vetur.format.defaultFormatterOptions": {
"prettier": {
// Prettier option here
"trailingComma": "es5", // 多行时，尽可能打印尾随的逗号
"tabWidth": 4, // 会忽略vetur的tabSize配置
"useTabs": false, // 是否利用tab替代空格
"semi": true, // 句尾是否加;
"singleQuote": true, // 使用单引号而不是双引号
"arrowParens": "avoid", // allow paren-less arrow functions 箭头函数的参数使用圆括号
}
}
```

3. **vetur-设置风格工具prettyhtml到js-beautify-html** 

   ```
   "vetur.format.defaultFormatterOptions": {
       "js-beautify-html": {
           // js-beautify-html settings here
       }
   }
   ```

   
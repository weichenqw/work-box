1. “svn.autorefresh”:true, //是否启用自动刷新
2. “svn.commit.changes.selectedAll”:true, //在提交更改时选择所有文件
3. “svn.commit.checkEmptyMessage”:true,// 提交前检查空消息
4. “svn.conflicts.autoResolve”:none, //将文件设置为在修复冲突后已解决的状态
5. “svn.default.encoding”:空, //如果输出不是utf-8，则对svn输出进行编码。当此参数为空时，将自动检测编码。例如:“windows - 1252”。
6. “svn.defaultCheckoutDirectory”:空, //检出svn存储库的默认位置。
7. “svn.delete.actionForDeletedFiles”: “prompt” //值:[“none”，“prompt”，“remove”]，//当一个文件被删除时，SVN应该做什么?“none”—什么也不做，“prompt”—请求操作，“remove”—从SVN中自动删除
8. “svn.delete.ignoredRulesForDeletedFiles”: [], //忽略“svn.delete.actionForDeletedFiles”的文件/规则(例如:file.txt或**/*.txt)
9. “svn.detectExternals”:true, //控制是否自动检测svn外部。
10. “svn.detectIgnored”:没错, //控制是否在忽略的文件夹上自动检测svn。
11. “svn.diff.withHead”:true, //使用存储库中的最新修订显示差异更改。将false设置为在本地文件夹中使用最新修订
12. “svn.启用”:true, //是否启用svn
13. “svn.experimental.detect_encoding”:空, //试试实验性的编码检测
14. “svn.experimental.encoding_priority”: [], //编码的优先级
15. “svn.gravatar.icon_url”:“https://www.gravatar.com/avatar/ < AUTHOR_MD5 > . jpg ? s = <大小>研发= robohash ", //使用， <AUTHOR_MD5>和占位符的庄严图标的Url
16. “svn.gravatars.启用”:true, //在日志查看器中使用garavatar图标
17. “svn.ignoreMissingSvnWarning”:空, 忽略SVN缺失时的警告
18. “svn.ignoreRepositories”:空, //要忽略的SVN存储库列表。
19. “svn.ignoreWorkingCopyIsTooOld”:空, 当工作副本太旧时忽略警告
20. “svn.layout.branchesRegex”:“分支/ ([^ /]+)(/ . *)?” // Regex检测SVN URL中“分支”的路径，禁用“null”。子路径使用“分支/ [^ /]+ / ([^ /]+)(/ . *)?”(例:“分支/……”、“版本/……)
21. “svn.layout.branchesRegexName”: 1、 // Regex group的分支名称位置
22. “svn.layout.showFullName”:没错, //将true设置为显示“branch /”，将false设置为只显示“”
23. “svn.layout。tagRegexName”: 1、 //标签名称的正则组位置
24. “svn.layout.tagsRegex”:“标签/ ([^ /]+)(/ . *)?” // Regex检测SVN URL中“标记”的路径，禁用“null”。子路径使用的标签/ [^]+ / ([^ /]+)(/ . *)?”。(例:‘标签/…’,'邮票/……)
25. “svn.layout.trunkRegex”:“(树干)(/ . *)?” // Regex检测SVN URL中“trunk”的路径，禁用“null”。(例:“(树干)”、“(主要)”)
26. “svn.layout.trunkRegexName”: 1、 // 中继名称的正则表达式组位置
27. “svn.log.长度”:50, 提交到日志的消息的数量
28. “svn.multipleFolders.depth”: 4 //使用SVN查找子文件夹的最大深度
29. “svn.multipleFolders。启用”:空, //允许使用SVN查找子文件夹
30. “svn.multipleFolders。忽略”:“* * / .”,“* * / .hg”、“* * /供应商”、“* * / node_modules”), //文件夹来忽略使用SVN
31. “svn.path”:空, //指向svn可执行文件的路径
32. “svn.refresh.remoteChanges”:空, //刷新远程更改刷新命令
33. “svn.remoteChanges.checkFrequency”: 300年, //设置间隔(以秒为单位)，检查远程存储库中更改的文件，并在statusbar中显示。0禁用
34. “svn.showOutput”:空, //在扩展开始时显示输出窗口
35. “svn.showUpdateMessage”:true, //在运行更新时显示更新消息
36. “svn.sourceControl.vaule:[“open”，“open diff”]，//设置更改资源状态时的左键单击功能
37. “svn.sourceControl.combineExternalIfSameServer”:空, //将主if中的外部svn与来自同一台服务器的svn合并。
38. “svn.sourceControl.countUnversioned”:true, //允许在状态计数中计算未版本化的文件
39. “svn.sourceControl.hideUnversioned”:空, //将未版本控制的文件隐藏在源代码控制UI中
40. “svn.sourceControl.ignoreOnCommit”:“ignore-on-commit”, //提交时忽略更改列表
41. “svn.sourceControl.ignoreOnStatusCount”:“ignore-on-commit”, //在状态计数时忽略更改列表
42. “svn.update.ignoreExternals”:true //设置为在更新时忽略外部定义(添加——ignore-externals)
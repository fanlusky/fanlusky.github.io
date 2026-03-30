---
title: 我的 VSCode 基本设置
date: 2023-02-06 22:48:57
updated: 2023-05-04 11:37:16
tags:
- VSCode
categories:
index_img: https://i.imgur.com/QtvTvxN.png
banner_img: https://i.imgur.com/QtvTvxN.png
description: '我的个人的目前的 VSCode 加 Vim 插件的配置'
---

2023.05.04 更新：

放一下 GitHub Gist 的地址，配置可能会新一点，

- settings.json

<https://gist.github.com/fanlusky/62bbfab7ed9cd7db93b439f64f01bbeb>

- keybindings.json

<https://gist.github.com/fanlusky/3b58a7a8de255ca8eab77c9551467574>

应 B 站小伙伴的请求，我给我目前的 VSCode 的整体设置和快捷键设置的 json 文件的每一行都加上了注释，如下，

settings.json，

```json
{
  // 是否要确认是否信任新打开的文件
  "security.workspace.trust.untrustedFiles": "open",
  // redhat 遥测设置
  "redhat.telemetry.enabled": true,
  // xml 设置，这是自动生成的
  "xml.server.binary.trustedHashes": [
    "75545f1685acea66aed67cb886c59e49cbbf0f51c25c89baad76cf0a3ee962a7"
  ],
  // 编辑器设置在保存时自动格式化
  "editor.formatOnSave": true,
  // 图标主题
  "workbench.iconTheme": "material-icon-theme",
  // 不要弹出确认拖放
  "explorer.confirmDragAndDrop": false,
  // 不要弹出确认删除
  "explorer.confirmDelete": false,
  // 设置编辑器的字体
  "editor.fontFamily": "'CaskaydiaCove NF Mono', 'Cascadia Mono', 'Source Han Sans CN', Consolas, 'Courier New', monospace",
  // 开启编辑器的连字符设置
  "editor.fontLigatures": true,
  // 开始的编辑器
  "workbench.startupEditor": "none",
  // 智能提交
  "git.enableSmartCommit": true,
  // git 不要弹窗确认是否同意 sync
  "git.confirmSync": false,
  // python 对 formatter 的设置
  "python.formatting.autopep8Args": [
    "--ignore",
    "E402"
  ],
  // python 对某些语法分析的设置
  "python.analysis.diagnosticSeverityOverrides": {
    "reportUnsupportedDunderAll": "none"
  },
  // 设置 html 的 formatter
  "[html]": {
    "editor.defaultFormatter": "vscode.html-language-features"
  },
  // unicode 高亮设置
  "editor.unicodeHighlight.allowedLocales": {
    "zh-hans": true,
    "zh-hant": true
  },
  // 光标的动画效果
  "editor.cursorBlinking": "smooth",
  "editor.cursorSmoothCaretAnimation": "on",
  // 指定默认的 termimal
  "terminal.integrated.defaultProfile.windows": "PowerShell",
  // 设置 terminal 的字体
  "terminal.integrated.fontFamily": "CaskaydiaCove NF Mono",
  // 设置 markdown 预览的字体
  "markdown.preview.fontFamily": "CaskaydiaCove NF Mono, -apple-system, BlinkMacSystemFont, 'Segoe WPC', 'Segoe UI', system-ui, 'Ubuntu', 'Droid Sans', sans-serif",
  // 关闭编辑器的自动检测缩进设置
  "editor.detectIndentation": false,
  // 设置不同语言的 tab 大小
  "[javascript]": {
    "editor.tabSize": 2,
  },
  "[css]": {
    "editor.tabSize": 2,
  },
  "[jsonc]": {
    "editor.tabSize": 2,
  },
  "[json]": {
    "editor.tabSize": 2,
  },
  "[lua]": {
    "editor.tabSize": 2,
  },
  "[javascriptreact]": {
    "editor.tabSize": 2,
  },
  "[scss]": {
    "editor.tabSize": 2,
  },
  "[java]": {
    "editor.tabSize": 2,
  },
  // 行包裹设置
  "editor.wordWrap": "on",
  // python 设置在文件所在目录进行执行
  "python.terminal.executeInFileDir": true,
  // 终端的限制
  "terminal.integrated.bellDuration": 100000,
  // 不要高亮一些看不见的 unicode 字符
  "editor.unicodeHighlight.invisibleCharacters": false,
  "workbench.colorCustomizations": {
    // 光标的颜色设置
    "editorCursor.foreground": "#16C60C",
    // 当前行的背景颜色设置
    "editor.lineHighlightBackground": "#292e42",
    // 状态栏颜色设置
    "statusBar.background": "#1e1e1e",
    "statusBar.foreground": "#9b9b8f",
    "statusBar.border": "#333a48",
  },
  // 隐藏 minimap
  "editor.minimap.autohide": true,
  "editor.minimap.enabled": false,
  // 在某些情况下隐藏光标
  "editor.hideCursorInOverviewRuler": true,
  // 以下三行是为了隐藏滚动栏
  "editor.scrollbar.horizontal": "hidden",
  "editor.scrollbar.vertical": "hidden",
  "editor.scrollbar.verticalScrollbarSize": 0,
  // 布局控制
  "workbench.layoutControl.enabled": false,
  // 渲染行高的风格
  "editor.renderLineHighlight": "line",
  // 取消 occurrence 和 selection 的高亮
  "editor.occurrencesHighlight": false,
  "editor.selectionHighlight": false,
  // 以下是 vim 的设置
  // vim 使用系统剪贴板
  "vim.useSystemClipboard": true,
  // 开启 vim 的 easymotion
  "vim.easymotion": true,
  // 当输入一个搜索字符时，显示下一个匹配的结果
  "vim.incsearch": true,
  // vim 来接管 ctrl 键
  "vim.useCtrlKeys": true,
  // 高亮搜索结果
  "vim.hlsearch": true,
  // 设置 vim 的 leader 键为空格键
  "vim.leader": "<space>",
  // 设置 vim 不接管某些快捷键
  "vim.handleKeys": {
    "<C-a>": false,
    "<C-f>": false
  },
  // vim normal 模式下的键位设置
  "vim.normalModeKeyBindings": [
    // 侧边栏的显示和隐藏的快捷键，我映射成了 leader + e
    {
      "before": [
        "leader",
        "e"
      ],
      "commands": [
        {
          "command": "workbench.action.toggleSidebarVisibility"
        }
      ]
    },
    // cmake 快速编译和运行文件，我映射成了 leader + l，这个和直接点击底部状态栏的运行按钮效果是一样的
    {
      "before": [
        "leader",
        "l"
      ],
      "commands": [
        {
          "command": "workbench.action.terminal.sendSequence",
          "args": {
            "text": "clear \u000D"
          }
        },
        {
          "command": "cmake.launchTarget"
        }
      ]
    },
    // 在左侧的文件管理器中打开当前文件
    {
      "before": [
        "leader",
        "f"
      ],
      "commands": [
        {
          "command": "revealInExplorer"
        }
      ]
    },
    // 取消高亮，比如我们在当前文件中搜索之后可以使用这个快捷键
    {
      "before": [
        "leader",
        "h"
      ],
      "commands": [
        ":noh"
      ]
    },
    // 关闭当前的 tab
    {
      "before": [
        "leader",
        "c"
      ],
      "commands": [
        ":q"
      ]
    },
    // 保存当前的文件
    {
      "before": [
        "leader",
        "w"
      ],
      "commands": [
        ":w"
      ]
    },
    // 显示和隐藏左侧的活动栏
    {
      "before": [
        "leader",
        "a"
      ],
      "commands": [
        {
          "command": "workbench.action.toggleActivityBarVisibility"
        }
      ]
    },
    // 显示和隐藏底部的状态栏
    {
      "before": [
        "leader",
        "b"
      ],
      "commands": [
        {
          "command": "workbench.action.toggleStatusbarVisibility"
        }
      ]
    },
    // 快速在底部的 terminal 中运行 python 文件
    {
      "before": [
        "leader",
        "p",
        "y"
      ],
      "commands": [
        "workbench.action.files.saveAll",
        {
          "command": "workbench.action.terminal.sendSequence",
          "args": {
            "text": "clear \u000D"
          }
        },
        "workbench.action.terminal.focus",
        {
          "command": "workbench.action.terminal.sendSequence",
          "args": {
            "text": "python '${file}'\u000D"
          }
        },
        "workbench.action.focusActiveEditorGroup"
      ]
    },
    // 快速在底部的 terminal 中运行 autohotkey
    {
      "before": [
        "leader",
        "k",
        "k"
      ],
      "commands": [
        "workbench.action.files.saveAll",
        {
          "command": "workbench.action.terminal.sendSequence",
          "args": {
            "text": "clear \u000D"
          }
        },
        "workbench.action.terminal.focus",
        {
          "command": "workbench.action.terminal.sendSequence",
          "args": {
            "text": "${file} \u000D"
          }
        },
        "workbench.action.focusActiveEditorGroup"
      ]
    },
    // 这个和 Ctrl + P 效果是等同的，即，快速搜索打开文件
    {
      "before": [
        "leader",
        "g",
        "g"
      ],
      "commands": [
        {
          "command": "workbench.action.quickOpen"
        }
      ]
    },
    // 在当前打开的项目中搜索文本
    {
      "before": [
        "leader",
        "g",
        "f"
      ],
      "commands": [
        {
          "command": "workbench.view.search"
        }
      ]
    },
    // 快速运行 java 代码
    {
      "before": [
        "leader",
        "j",
        "a"
      ],
      "commands": [
        {
          "command": "java.debug.runJavaFile"
        }
      ]
    },
    // 快速执行 VSCode 的 debug 命令
    {
      "before": [
        "leader",
        "r",
      ],
      "commands": [
        {
          "command": "workbench.action.debug.start"
        }
      ]
    },
  ],
  // vim 的 visual 模式下的键位绑定
  "vim.visualModeKeyBindings": [
    // 向右缩进，可以重复使用
    {
      "before": [
        ">"
      ],
      "commands": [
        "editor.action.indentLines"
      ]
    },
    // 向左缩进，可以重复使用
    {
      "before": [
        "<"
      ],
      "commands": [
        "editor.action.outdentLines"
      ]
    },
  ],
  // vim 在 normal 模式下非递归的键位绑定
  "vim.normalModeKeyBindingsNonRecursive": [
    // 将 u 和 VSCode 自身的撤销动作绑定
    {
      "before": [
        "u"
      ],
      "commands": [
        "undo"
      ]
    },
    // 将 Ctrl + r 和 VSCode 自身的重做动作绑定
    {
      "before": [
        "C-r"
      ],
      "commands": [
        "redo"
      ]
    }
  ],
  // vim 的 easymotion 插件的高亮字符的前景色
  "vim.easymotionMarkerForegroundColorOneChar": "#DF5452",
  // 关闭 snippet 的阻止快速建议的行为
  "editor.suggest.snippetsPreventQuickSuggestions": false,
  // 禁止一些括号设置
  "editor.guides.bracketPairs": false,
  "editor.guides.bracketPairsHorizontal": false,
  // 开启 vim-surround
  "vim.surround": true,
  // 扩展忽视建议
  "extensions.ignoreRecommendations": true,
  // cmake 配置
  "cmake.configureOnOpen": true,
  // 编辑器内联的建议
  "editor.inlineSuggest.enabled": true,
  // 关闭 terminal 中的多行粘贴的警告
  "terminal.integrated.enableMultiLinePasteWarning": false,
  // 窗口的缩放程度
  "window.zoomLevel": 1,
  // 关闭不明 unicode 字符的高亮
  "editor.unicodeHighlight.ambiguousCharacters": false,
  // 修改窗口的风格为 windows 原生风格
  "window.titleBarStyle": "native",
  // 标签栏和面包屑的显示和隐藏
  "workbench.editor.showTabs": true,
  "breadcrumbs.enabled": false,
  // 修改窗口标题的显示文字
  "window.title": "💖${folderName}-FanyFull",
  // 我们在文件管理器中使用 vscode 打开文件时，确保其会在新的 vscode 窗口中打开
  "window.openFilesInNewWindow": "on",
  // 将 manifest 文件关联到 xml 文件，这样，manifest 文件就可以使用 xml 的语法高亮了
  "files.associations": {
    "*.manifest": "xml"
  },
  // 大文件的最大可使用内存
  "files.maxMemoryForLargeFilesMB": 8192,
  // 关闭 tab 标签的 X 按钮
  "workbench.editor.tabCloseButton": "off",
  // 隐藏 tab 标签的 X 按钮，当然，如果 CloseButton 被隐藏了，那么这个设置其实是无所谓
  "workbench.editor.tabSizing": "shrink",
  // accessibility
  "editor.accessibilitySupport": "off",
  "git.openRepositoryInParentFolders": "never",
  // 设置 python 在输入的时候进行格式化，也就是说，自动缩进
  "[python]": {
    "editor.formatOnType": true
  },
  // 隐藏菜单栏
  "window.menuBarVisibility": "hidden",
  "workbench.statusBar.visible": false,
  "workbench.activityBar.visible": false,
}
```

keybindings.json，

```json
// Place your key bindings in this file to override the defaultsauto[]
[
  // new file in explorer
  {
    "key": "ctrl+n",
    "command": "explorer.newFile",
    "when": "explorerViewletFocus"
  },
  // 以下是 vim 绑定的键位
  // 当光标在编辑器中聚焦时，显示和隐藏底部的 panel
  {
    "key": "ctrl+j",
    "command": "workbench.action.togglePanel",
    "when": "editorTextFocus"
  },
  // 编写代码时的智能提示框的上下选择
  {
    "key": "ctrl+j",
    "command": "selectNextSuggestion",
    "when": "vim.active && suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
  },
  {
    "key": "ctrl+k",
    "command": "selectPrevSuggestion",
    "when": "vim.active && suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
  },
  // 在 quickOpen 的对话框中上下跳转
  {
    "key": "ctrl+j",
    "command": "workbench.action.quickOpenSelectNext",
    "when": "vim.active && inQuickOpen"
  },
  {
    "key": "ctrl+k",
    "command": "workbench.action.quickOpenSelectPrevious",
    "when": "vim.active && inQuickOpen"
  },
  // 当光标聚焦在编辑器中且 vim 处于 normal 模式时，进行 tab 栏目的左右跳转
  {
    "key": "shift+h",
    "command": "workbench.action.previousEditor",
    "when": "editorTextFocus && vim.mode == 'Normal'"
  },
  {
    "key": "shift+l",
    "command": "workbench.action.nextEditor",
    "when": "editorTextFocus && vim.mode == 'Normal'"
  },
  // 在不同的组件之间进行跳转
  {
    "key": "ctrl+h",
    "command": "workbench.action.navigateLeft"
  },
  {
    "key": "ctrl+l",
    "command": "workbench.action.navigateRight"
  },
  {
    "key": "ctrl+k",
    "command": "workbench.action.navigateUp",
    "when": "terminal.active && terminalFocus"
  },
  // 跳转到 terminal 中
  {
    "key": "ctrl+\\",
    "command": "workbench.action.terminal.toggleTerminal"
  },
  // vim 模式下的左侧的文件管理器的操作
  // 在文件管理器中搜索
  {
    "key": "/",
    "command": "list.find",
    "when": "listFocus && listSupportsFind && !inputFocus"
  },
  // 新建一个文件
  {
    "key": "a",
    "command": "explorer.newFile",
    "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
  },
  // 新建一个文件夹
  {
    "key": "shift+a",
    "command": "explorer.newFolder",
    "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
  },
  // 给文件重命名
  {
    "key": "r",
    "command": "renameFile",
    "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
  },
  // 删除文件
  {
    "key": "d",
    "command": "deleteFile",
    "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
  },
  // 在不同的 terminal 之间进行跳转
  {
    "key": "ctrl+shift+alt+j",
    "command": "workbench.action.terminal.focusNext",
    "when": "terminalFocus && terminalHasBeenCreated && !terminalEditorFocus || terminalFocus && terminalProcessSupported && !terminalEditorFocus"
  },
  {
    "key": "ctrl+shift+alt+k",
    "command": "workbench.action.terminal.focusPrevious",
    "when": "terminalFocus && terminalHasBeenCreated && !terminalEditorFocus || terminalFocus && terminalProcessSupported && !terminalEditorFocus"
  },
  // codeAction 上下选择
  {
    "key": "j",
    "command": "selectNextCodeAction",
    "when": "codeActionMenuVisible"
  },
  {
    "key": "k",
    "command": "selectPrevCodeAction",
    "when": "codeActionMenuVisible"
  },
  // terminal 中上下滚动
  {
    "key": "alt+j",
    "command": "workbench.action.terminal.scrollDown",
    "when": "terminalFocus"
  },
  {
    "key": "alt+k",
    "command": "workbench.action.terminal.scrollUp",
    "when": "terminalFocus"
  },
  // 关闭 terminal
  {
    "key": "ctrl+w",
    "command": "workbench.action.terminal.kill",
    "when": "terminalFocus"
  },
  // 调整底部的 panel 的大小
  {
    "key": "ctrl+shift+k",
    "command": "workbench.action.terminal.resizePaneUp",
    "when": "terminalFocus"
  },
  {
    "key": "ctrl+shift+j",
    "command": "workbench.action.terminal.resizePaneDown",
    "when": "terminalFocus"
  },
  // 最大化 terminal
  {
    "key": "ctrl+win+`",
    "command": "workbench.action.toggleMaximizedPanel",
    "when": "terminalFocus"
  },
]
```
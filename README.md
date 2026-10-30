# 文游小集

手机上就能玩的文字小游戏，用 GitHub Pages 发布。

- 目录页：https://tonkmy.github.io/bin/
- 《半本胭脂谱》：https://tonkmy.github.io/bin/banben-yanzhipu/

## 结构

```
index.html              目录页
.nojekyll               让 Pages 原样发布文件，不经过 Jekyll 处理
<游戏 slug>/index.html  一部游戏一个文件夹，单文件独立版
```

## 加一部新游戏

1. 新建文件夹 `<slug>/`（拼音 kebab-case），把游戏的独立版 HTML 放进去，命名为 `index.html`。
2. 在 `index.html` 的目录里，复制一整个 `<li class="entry">`，放到最上面，改这几处：
   - `href`
   - `--c`：题签颜色，挑一个代表这部游戏的颜色
   - `--c2`：深色模式下的标语颜色，比 `--c` 亮一些
   - 卷号、标题、标语、简介、标签、时长
3. 改右上角的「共 N 部」，提交并推送。Pages 一两分钟后就会更新。

## 注意

- **存档键名要加游戏前缀**：同一个 `tonkmy.github.io` 下的所有页面共用一份浏览器存储，键名重复会互相覆盖存档。例如《半本胭脂谱》用的是 `banben_yanzhi_*`。
- **外部字体用脚本异步加载**：Google Fonts 在国内可能连不上，阻塞式加载会让页面白屏很久。
- 每部游戏的设计档案在 skill 仓库 `Tonkmy/-skill` 的 `wenyou-dangan/games/<slug>/`。

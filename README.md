git commit emoji 使用指南
============================

执行 `git commit` 时使用 emoji 为本次提交打上一个 "标签", 使得此次 commit 的主要工作得以凸现，也能够使得其在整个提交历史中易于区分与查找。

### commit 格式

`git commit` 时，提交信息遵循以下格式：

```sh
:emoji1: :emoji2: 不超过 50 个字的摘要，首字母大写，使用祈使语气，句末不要加句号

提交信息主体

引用相关 issue 或 PR 编号 <#110>
```

初次提交示例：

```sh
git commit -m ":tada: Initialize Repo"
```

### emoji 指南

| emoji                                   | emoji 代码                    | commit 说明           |
| :-------------------------------------- | :---------------------------- | :-------------------- |
| :tada: (庆祝)                           | `:tada:`                      | 初次提交              |
| :new: (全新)                            | `:new:`                       | 引入新功能            |
| :bookmark: (书签)                       | `:bookmark:`                  | 发行/版本标签         |
| :bug: (bug)                             | `:bug:`                       | 修复 bug              |
| :ambulance: (急救车)                    | `:ambulance:`                 | 重要补丁              |
| :globe_with_meridians: (地球)           | `:globe_with_meridians:`      | 国际化与本地化        |
| :lipstick: (口红)                       | `:lipstick:`                  | 更新 UI 和样式文件    |
| :clapper: (场记板)                      | `:clapper:`                   | 更新演示/示例         |
| :rotating_light: (警车灯)               | `:rotating_light:`            | 移除 linter 警告      |
| :wrench: (扳手)                         | `:wrench:`                    | 修改配置文件          |
| :heavy_plus_sign: (加号)                | `:heavy_plus_sign:`           | 增加一个依赖          |
| :heavy_minus_sign: (减号)               | `:heavy_minus_sign:`          | 减少一个依赖          |
| :arrow_up: (上升箭头)                   | `:arrow_up:`                  | 升级依赖              |
| :arrow_down: (下降箭头)                 | `:arrow_down:`                | 降级依赖              |
| :zap: (闪电)<br>:racehorse: (赛马)      | `:zap:`<br>`:racehorse:`      | 提升性能              |
| :chart_with_upwards_trend: (上升趋势图) | `:chart_with_upwards_trend:`  | 添加分析或跟踪代码    |
| :rocket: (火箭)                         | `:rocket:`                    | 部署功能              |
| :white_check_mark: (白色复选框)         | `:white_check_mark:`          | 增加测试              |
| :memo: (备忘录)<br>:book: (书)          | `:memo:`<br>`:book:`          | 撰写文档              |
| :hammer: (锤子)                         | `:hammer:`                    | 重大重构              |
| :art: (调色板)                          | `:art:`                       | 改进代码结构/代码格式 |
| :fire: (火焰)                           | `:fire:`                      | 移除代码或文件        |
| :pencil2: (铅笔)                        | `:pencil2:`                   | 修复 typo             |
| :construction: (施工)                   | `:construction:`              | 工作进行中            |
| :wastebasket: (垃圾桶)                  | `:wastebasket:`               | 废弃或删除            |
| :wheelchair: (轮椅)                     | `:wheelchair:`                | 可访问性              |
| :construction_worker: (工人)            | `:construction_worker:`       | 添加 CI 构建系统      |
| :green_heart: (绿心)                    | `:green_heart:`               | 修复 CI 构建问题      |
| :lock: (锁)                             | `:lock:`                      | 修复安全问题          |
| :whale: (鲸鱼)                          | `:whale:`                     | Docker 相关工作       |
| :apple: (苹果)                          | `:apple:`                     | 修复 macOS 下的问题   |
| :penguin: (企鹅)                        | `:penguin:`                   | 修复 Linux 下的问题   |
| :checkered_flag: (旗帜)                 | `:checkered_flag:`            | 修复 Windows 下的问题 |
| :twisted_rightwards_arrows: (交叉箭头)  | `:twisted_rightwards_arrows:` | 分支合并              |

### 参考

#### git commit emoji

-   [gitmoji](https://github.com/carloscuesta/gitmoji/)
-   [emoji-cheat-sheet](http://www.webpagefx.com/tools/emoji-cheat-sheet/)
-   [styleguide-git-commit-message](https://github.com/slashsBin/styleguide-git-commit-message)
-   [atom git commit messages guide](https://github.com/atom/atom/blob/master/CONTRIBUTING.md#git-commit-messages)
-   [An emoji guide for your commit messages](https://gitmoji.carloscuesta.me/)
-   [程序员提交代码的 emoji 指南——原来表情文字不能乱用](https://www.h5jun.com/post/gitmoji.html)
-   [Ant Design 更新日志 emoji 规范](https://github.com/ant-design/ant-design/wiki/轮值规则和版本发布流程#emoji-for-changelog)

#### write a good commit message

-   [A Note About Git Commit Messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
-   [How to write a Git Commit Message (2014)](https://news.ycombinator.com/item?id=13889155)
-   [how to write a good git commit message](https://github.com/joelparkerhenderson/git_commit_message)
-   [5 Useful Tips For A Better Commit Message](https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message)
-   [Udacity Git Commit Message Style Guide](http://udacity.github.io/git-styleguide/)
-   [How to commit a change with both “message” and “description” from the command line?](https://stackoverflow.com/questions/16122234/how-to-commit-a-change-with-both-message-and-description-from-the-command-li)

### Message Subject(first line)

-   Capitalize the .`<subject>`

-   Do not end the first line with a period.

-   Total characters of the first line **MUST** be *Less* than or *Equal* to **50** characters Long.

-   Use the **present tense** ("Add feature" not "Added feature").

-   Use the **imperative mood** ("Move cursor to..." not "Moves cursor to...").

-   Use to identify what type of changes introduced in this commit; Allowed keywords: 

    ```
    <type>
    ```

    ```
    <type>
    ```

    -   An Emoji(see below for [list of Suggested Emojis](https://github.com/slashsBin/styleguide-git-commit-message#suggested-emojis))
    -   Or a Text:
        -   feat: 用户的新功能(或 something 表情符号)
        -   fix: bug fix for the user (or emoji)
        -   docs: 更改文档(或表情符号)
        -   style: 格式，缺少分号等; 没有生产代码更改(或表情符号)
        -   refactor: 重构生产代码，例如重命名变量(或表情符号)
        -   test: 添加缺少的测试，重构测试; 没有生产代码更改(或表情符号)
        -   chore: 更新粗活等; 没有生产代码更改

### Message Footer

-   Reference issues this commit is related to with the status of that Issue; Ex. , or or .`Issue #27``Ref T27``Ref T27, T56``Fixes T8`
-   Supported issue tracker status keywords:
    -   Fixes
    -   Fixed
    -   Closes
    -   Closed
    -   Resolves
    -   Resolved
    -   Ref
    -   Issue
    -   Issues

## Suggested Emojis

| Emoji | Raw Emoji Code           | Description                                                  |
| ----- | ------------------------ | ------------------------------------------------------------ |
| 🎨     | `:art:`                  | when improving the **format**/structure of the code 在改进代码的格式/结构时 |
| 📰     | `:newspaper:`            | when creating a **new file** 当创建一个新文件时              |
| 📝     | `:pencil:`               | when **performing minor changes/fixing** the code or language 当对代码或语言进行小的修改时 |
| 🐎     | `:racehorse:`            | when improving **performance** 在提高性能的时候              |
| 📚     | `:books:`                | when writing **docs** 写作的时候                             |
| 🐛     | `:bug:`                  | when reporting a **bug**, with Comment Tag 当报告一个错误的时候，用评论标签 |
| 🚑     | `:ambulance:`            | when fixing a **bug** 在修理一个漏洞的时候                   |
| 🐧     | `:penguin:`              | when fixing something on **Linux** 在 Linux 上修东西的时候   |
| 🍎     | `:apple:`                | when fixing something on **Mac OS **在Mac OS上修东西的时候   |
| 🏁     | `:checkered_flag:`       | when fixing something on **Windows **在Windows上修东西的时候 |
| 🔥     | `:fire:`                 | when **removing code** or files, *maybe* with `@CHANGED` Comment Tag  当删除代码或文件时，可能使用“@Changed”注释标签 |
| 🚜     | `:tractor:`              | when **change file structure**. Usually together with 🎨 当改变文件结构时 |
| 🔨     | `:hammer:`               | when **refactoring** code 重构代码                           |
| ☔     | `:umbrella:`             | when adding **tests** 当加入测试的时候                       |
| 🔬     | `:microscope:`           | when adding **code coverage** 当添加代码覆盖时               |
| 💚     | `:green_heart:`          | when fixing the **CI** build 在修理ci的时候                  |
| 🔒     | `:lock:`                 | when dealing with **security** 在处理安全问题的时候          |
| ⬆️     | `:arrow_up:`             | when upgrading **dependencies**  当升级依赖关系时            |
| ⬇️     | `:arrow_down:`           | when downgrading **dependencies** 当降低依赖度时             |
| ⏩     | `:fast_forward:`         | when **forward-porting features** from an older version/branch 当从旧版本/分支转移特性时 |
| ⏪     | `:rewind:`               | when **backporting features** from a newer version/branch 当从较新的版本/分支向后移植特性时 |
| 👕     | `:shirt:`                | when removing **linter**/strict/deprecation warnings 当删除 linter/严格/弃用警告时 |
| 💄     | `:lipstick:`             | when improving **UI**/Cosmetic 在改进 UI                     |
| ♿     | `:wheelchair:`           | when improving **accessibility** 在改善无障碍环境的同时      |
| 🌐     | `:globe_with_meridians:` | when dealing with **globalization**/internationalization/i18n/g11n 处理全球化/国际化/i18n/g11n |
| 🚧     | `:construction:`         | **WIP**(Work In Progress) Commits, *maybe* with `@REVIEW` Comment Tag “ WIP”提交，“可能”加上“@Review”注释标签 |
| 💎     | `:gem:`                  | New **Release** 新版本                                       |
| 🥚     | `:egg:`                  | New **Release** with Python egg 最新发布的                   |
| 🎡     | `:ferris_wheel:`         | New **Release** with Python wheel package 新发布的 Python 车轮包 |
| 🔖     | `:bookmark:`             | Version **Tags **新tag                                       |
| 🎉     | `:tada:`                 | **Initial** Commit 初次提交                                  |
| 🔈     | `:speaker:`              | when Adding **Logging**  当添加日志                          |
| 🔇     | `:mute:`                 | when Reducing **Logging**  减少日志记录时                    |
| ✨     | `:sparkles:`             | when introducing **New** Features 在介绍新功能的时候         |
| ⚡     | `:zap:`                  | when introducing **Backward-InCompatible** Features, *maybe* with `@CHANGED` Comment Tag 当引入向后不兼容的功能时，可以使用“@Changed”评论标签 |
| 💡     | `:bulb:`                 | New **Idea**, with `@IDEA` Comment Tag 新的创意，带有“@创意”评论标签 |
| ❄️     | `:snowflake:`            | changing **Configuration**, Usually together with 🐧 or 🎀 or 🚀 |
| 🎀     | `:ribbon:`               | Customer requested application **Customization**, with `@HACK` Comment Tag 客户要求应用程序定制，带有“@HACK”评论标签 |
| 🚀     | `:rocket:`               | Anything related to Deployments/**DevOps** 任何与部署/DevOps 相关的东西 |
| 🐘     | `:elephant:`             | **PostgreSQL** Database specific (Migrations, Scripts, Extensions, ...)  特定于 PostgreSQL 数据库(迁移、脚本、扩展、 ...) |
| 🐬     | `:dolphin:`              | **MySQL** Database specific (Migrations, Scripts, Extensions, ...) 特定于 MySQL数据库(迁移、脚本、扩展、 ...) |
| 🍃     | `:leaves:`               | **MongoDB** Database specific (Migrations, Scripts, Extensions, ...) 特定于 MongoDB数据库(迁移、脚本、扩展、 ...) |
| 🏦     | `:bank:`                 | **Generic Database** specific (Migrations, Scripts, Extensions, ...) 特定于 Generic Database数据库(迁移、脚本、扩展、 ...) |
| 🐳     | `:whale:`                | **Docker** Configuration docker配置                          |
| 🤝     | `:handshake:`            | when **Merge files** 当合并文件时                            |
| 🍒     | `:cherries:`             | when Commit Arise from one or more **Cherry-Pick**Commit(s) 当提交由一个或多个初选提交引起时 |

## 工具

\- [提交]( https://github.com/jakeasmith/Commit )(CLI) : 这是一个漂亮的 CLI 工具，可以帮助标准化基于此文档的提交消息，感谢@jakeasmith。

\- [ gitMoji ]( https://gitlab.com/louisgrasset/git-moji )(Firefox & Chrome 扩展) : 使用 emoji 增强提交功能，感谢[@louisgrasset ]( https://twitter.com/louisgrasset )

## 有趣的表情符号用法

\- [代码表情符号]( https://Codemoji.org/) : Mozilla 的代码表情符号用表情符号加密你的信息，以获取乐趣和利润

\- [基于表情符号的图表]( https://blog.mozilla.org/services/2016/08/23/sending-VAPID-identified-WebPush-notifications-via-mozillas-push-service/#send_data ) : 基于表情符号的数据轴承订阅更新图表(WebPush VAPID)

### Git Commit Messages

-   Use the present tense ("Add feature" not "Added feature")
-   Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
-   Limit the first line to 72 characters or less
-   Reference issues and pull requests liberally after the first line
-   When only changing documentation, include in the commit title`[ci skip]`
-   Consider starting the commit message with an applicable emoji:
    -   🎨 `:art:` when improving the format/structure of the code
    -   🐎 `:racehorse:` when improving performance
    -   🚱 `:non-potable_water:` when plugging memory leaks
    -   📝 `:memo:` when writing docs
    -   🐧 `:penguin:` when fixing something on Linux
    -   🍎 `:apple:` when fixing something on macOS
    -   🏁 `:checkered_flag:` when fixing something on Windows
    -   🐛 `:bug:` when fixing a bug
    -   🔥 `:fire:` when removing code or files
    -   💚 `:green_heart:` when fixing the CI build
    -   ✅ `:white_check_mark:` when adding tests
    -   🔒 `:lock:` when dealing with security
    -   ⬆️ `:arrow_up:` when upgrading dependencies
    -   ⬇️ `:arrow_down:` when downgrading dependencies
    -   👕 `:shirt:` when removing linter warnings

## Emoji for changelog

-   🐞 Bug 修复
-   💄 样式更新/less 变量更新
-   🆕 新增特性
-   🔥 极其值得关注的新增特性
-   🇺🇸🇨🇳🇬🇧 国际化改动，注意这里直接用对应国家/地区的旗帜。
-   📖 📝 文档或网站改进
-   ✅ 新增或更新测试用例
-   🛎 更新警告/提示信息
-   ⌨️ ♿ 可访问性增强
-   🗑 废弃或移除
-   🛠 重构或工具链优化
-   ⚡️ 性能提升

## Continue with a longer description

Continue with a longer description a.k.a. message body:

-   Add a blank line after the summary line, then write as much as you want.
-   Use up to 72 characters per line for typical text for word wrap.
-   Use as many characters as needed for atypical text, such as URLs, terminal output, formatted messages, etc.
-   Include any kind of notes, links, examples, etc. as you want.

## Summary examples

Summary examples of good commit messages:

-   Add foo
-   Drop foo
-   Fix foo
-   Refactor foo
-   Optimize foo

## Summary keywords

We recommend these summary keywords because they use imperative mood, present tense, active voice, and are verbs:

-   **Add**: Create a capability e.g. feature, test, dependency. 创建一个功能，例如特性，测试，依赖。
-   **Drop**: Delete a capability e.g. feature, test, dependency. 删除功能，例如功能，测试，依赖。
-   **Fix**: Fix an issue e.g. bug, typo, accident, misstatement. 修复一个问题，例如 bug，输入错误，事故，错误陈述。
-   **Bump**: Increase the version of something e.g. a dependency. 增加某事物的版本，例如依赖关系
-   **Make**: Change the build process, or tools, or infrastructure. 改变构建过程，或工具，或基础设施。
-   **Start**: Begin doing something; e.g. enable a toggle, feature flag, etc. 开始做一些事情; 例如，启用一个切换，功能标志等。
-   **Stop**: End doing something; e.g. disable a toggle, feature flag, etc. 结束做某事，例如禁用切换，功能标志等。
-   **Optimize**: A change that MUST be just about performance, e.g. speed up code.一个改变，必须只是性能，例如加速代码。
-   **Document**: A change that MUST be only in the documentation, e.g. help files.只能在文档中进行的更改，例如帮助文件。
-   **Refactor**: A change that MUST be just a refactoring patch一个改变，必须只是一个重构补丁
-   **Reformat**: A change that MUST be just a formatting path, e.g. change spaces.一个必须只是格式化路径的更改，例如，更改空格。
-   **Rearrange**: A change that MUST be just an arranging patch, e.g. change layout. 一个必须只是安排补丁的更改，例如更改布局。
-   **Redraw**: A change that MUST be just a drawing patch, e.g. change a graphic, image, icon, etc. 一个改变，必须只是一个绘图补丁，例如改变图形，图像，图标等。
-   **Reword**: A change that MUST be just a wording patch, e.g. change a comment, label, doc, etc. 一个修改，必须只是一个措辞补丁，例如改变一个评论，标签，文档等。
-   **Revise**: A change that MUST be just a revising patch e.g. a change, an alteration, a correction, etc. 一个修改，必须是一个修改补丁，例如一个变化，一个修改，一个更正等。
-   **Refit/Refresh/Renew/Reload**: A change that MUST be just a patch e.g. update test data, API keys, etc. 一个必须是补丁的更改，例如更新测试数据、 API 密钥等。


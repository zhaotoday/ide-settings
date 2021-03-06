## 介绍
WebStorm（前端）和 PhpStorm（后端 PHP）IDE 的统一设置。

## 目的
为了多人开发时，提高代码风格的一致性和代码的可读性，减少合并时由代码格式化产生的冲突。
> 可考虑导出 IDE 配置文件，团队统一使用。

## 相关
- [standard](https://github.com/feross/standard)
- [stylelint-config-standard](https://github.com/stylelint/stylelint-config-standard)
- [EditorConfig 官网](http://editorconfig.org/)
- [EditorConfig 使用介绍](https://segmentfault.com/a/1190000007599845)
- [遵循 ESDoc 规范编写 JS 代码注释](https://github.com/zhaotoday/esdoc)
- [遵循 PHPDoc 规范编写 PHP 代码注释](https://www.phpdoc.org/)

## 配置文件
部分配置文件拷贝自`vue-cli`，见`/configs`文件夹，仅供参考。

## 注意
请定期升级 IDE，目前最新版本为：WebStorm（2017.1.4）、PhpStorm（2017.1.3）。

## 激活服务器
在激活框，选择`License server`，输入`激活服务器地址`。
- WebStorm：`http://idea.iteblog.com/key.php`；
- PhpStorm：`http://www.0-php.com:1017`。

## 代码注释规范
- 前端 JS：ESDoc；
- 后端 PHP：PHPDoc。

## 统一设置
#### 取消文件自动保存
File -> Settings -> Appearance & Behavior -> system settings -> 去掉勾选 Save files on frame deactivation。

#### 给已修改文件加 * 号（便于区分文件是否已修改）
File -> Settings -> Editor -> General -> Editor Tabs -> [Tab Appearance] 勾选 Mark modified tabs with asterisk。

#### 重置 Redo 快捷键（可选）
File -> Settings -> Keymap -> [Main menu -> Edit] 搜索 Redo -> 删除已有快捷键，并设置为 Ctrl+Y。

#### 配置 EditorConfig
EditorConfig 可以帮助开发者在不同的编辑器和 IDE 之间定义和维护一致的代码风格。
> 比如，在项目开发过程中，有的人喜欢用 tab 来缩进，有的人喜欢用空格。为了保持代码风格的一致，可以使用 EditorConfig 来规范缩进风格，缩进大小，tab 长度以及字符集等。

#### 启用 ESLint
File -> Settings -> Languages & Frameworks -> JavaScript -> Code Quality Tools -> ESLint -> 勾选 Enable。

#### 启用 Stylelint
File -> Settings -> Languages & Frameworks -> Stylesheets - > Stylelint -> 勾选 Enable。

## WebStorm 设置
#### 使用 Standard 规范格式化代码
File -> Settings -> Editor -> Code Style -> JavaScript -> Scheme 选择 Default -> [右上角] Set From... -> Predefined Style -> JavaScript Standard Style。

#### 格式化 html、css 等其他格式文件
... -> Set from... -> JavaScript。

#### 修复修改文件时，webpack-dev-server 不会自动编译刷新的 bug
File -> Settings -> Appearance & Behavior -> System Settings -> 去掉勾选 Use "safe write" (save changes to a temporary file first)

## PhpStorm 设置
#### 使用 Drupal 规范格式化代码（按团队习惯统一选择一种规范）
File -> Settings -> Editor -> Code Style -> PHP -> Scheme 选择 Default -> [右上角] Set From... -> Predefined Style -> Drupal。

#### 修改 PHPDoc 规则（可选）
在上面的配置页面，切到 PHPDoc，以下这两项去掉勾选即可：
- Blank lines around parameters
- Blank line before the fist tag

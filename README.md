# Felint - 无痛的前端 JS 和 SCSS/CSS 代码检查工具


Felint = Eslint + Git Hook + Statistics 

## 安装 felint
安装前请确保你的电脑已经安装好了 npm 和 gem 

```c
npm install -g felint
```

## 初始化

进入到你项目的根目录，运行
```c
felint init
```
felint 会从 https://github.com/youzan/felint-config 下载所需的默认的配置文件，包括Git Hook脚本、eslint 和 css lint 的配置文件等，然后放到当前项目合适的位置。

## 升级配置文件

```c
felint update
```

## 使用自己的 felint 配置

如果你不想使用我们默认的[felint-config](https://github.com/youzan/felint-config)校验，你可以fork出来修改为自己的felint-config（修改方法参考 [felint-config 的 readme](https://github.com/youzan/felint-config/blob/master/README.md) ），然后在项目中手动配置你自己的 felint-config 仓库地址，在你的项目根目录添加一个`.felintrc`文件，其文件内容格式为：

```js
{
	"gitHookUrl": "your url"
}
```
然后执行一次 `felint init` 即可

## 可以配合使用的 Sublime 插件

### html-css-js prettify

`Sublime`插件：`html-css-js prettify`，按`shift+command+h`能自动规范大部分代码。

### SublimeLinter

`Sublime`插件：`SublimeLinter`、`SublimeLinter-contrib-eslint`和`SublimeLinter-contrib-scss-lint`插件，在文件保存时就可以验证是否符合规范，红的提示为error必须修改为规范的代码，黄的为warning可以忽略，减少commit代码时不符合规范又要重新改的时间。

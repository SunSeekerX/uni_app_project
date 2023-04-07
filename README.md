# uni-app-project 技术中台

**不建议使用非 cli 创建的版本，它并不是通用的前端项目结构，仅仅只能用在 hbuilderx 内，同时也无法集成 ci&cd**

vue2 + vuex + eslint + prettier + stylelint + lint-staged + husky

- 项目地址: [Github](https://github.com/SunSeekerX/uni-app-project-cli)
- 博客地址: [https://yoouu.cn/](https://yoouu.cn/)
- 当我们日复一日年复一年的搬砖的时候，你是否曾想过提升一下开发效率，如果一个通用的架构摆在你的面前，你还会选择自己搭架构么，但是搭建出一个好的架构并非易事，有多少人愿意选择去做，还有多少人选择努力去做好，可能寥寥无几，但是你今天看到的，正是你所想要的，一个真正能解决你开发新项目时最大痛点的架构工程，你不需要再麻木 Copy 原有旧项目的代码，只需改动少量代码就能得到想要的效果，你会发现开发新项目其实是一件很快乐的事。

## 快速上手

克隆项目

```shell
git clone https://github.com/SunSeekerX/uni-app-project.git
```

安装依赖

```shell
yarn
```

运行

把项目拖到 HbuilderX 运行就行了。

## 其他命令

scripts 里面包含了一些额外的命令

### 提交代码

我提交代码喜欢用这个，但是用到了 commitizen 这个插件（用来规范提交信息的），你想用可以看 [规范提交代码](https://doc.yoouu.cn/front-end/npm/#%F0%9F%93%8C-%E8%A7%84%E8%8C%83%E6%8F%90%E4%BA%A4%E4%BB%A3%E7%A0%81) 说明

```shell
yarn gc
```

### eslint

检查 `src` 目录下 `vue` 和 `js` 后缀结尾的文件是否有错误

```shell
yarn lint:eslint
```

### prettier

使用 `prettier` 格式化 `src` 目录下的 `js,json,tsx,css,less,scss,vue,html,md` 后缀结尾的文件

```shell
yarn lint:prettier
```

### stylelint

使用 `stylelint` 校验和格式化 `src` 目录下的 `vue,less,postcss,css,scss` 后缀结尾的文件内的样式代码

```shell
yarn lint:stylelint
```

### 排序 package.json

强迫症专用的，对 `package.json` 内的 `key` 值进行排序

```shell
yarn pkg:sort
```

## 项目亮点

- 常用集成：[uView UI](https://www.uviewui.com/)、[limm-windi-css-uniapp](https://ext.dcloud.net.cn/plugin?id=8575)、[limm-utools](https://ext.dcloud.net.cn/plugin?id=8574)
- 代码注释：项目内有非常完善的代码注释，对每个模块的作用做了仔细的说明
- 代码统一：对项目中常见的代码进行了封装，或是封装到工具类中、或者封装到框架中，不追求过度封装，根据实际场景和代码维护性考虑，尽量保证同一个功能的代码在项目中不重复。
- 敏捷开发：一个 App 大概率会出现的功能已经写好，对项目的敏捷开发起到了至关重要的作用，可用于新项目开发或者旧项目重构，可将开发周期缩短近一半的时间，并且后续不会因为前期的快速开发而留下成堆的技术遗留问题，万丈高楼平地起，uni-app-project-cli 属于基建工程，而在软件行业我们称之为技术中台。
- 开发约束：集成 eslint + prettier + stylelint + lint-staged + husky 对从开发到提交至仓库过程进行代码质量把控，保持团队整体风格统一。

## 食用指南

### 项目结构

```
├── apis
│   ├── express.js
│   └── index.js
├── config
│   ├── cdev.config.js
│   ├── default.js
│   ├── index.js
│   ├── online.config.js
│   ├── prod.config.js
│   └── stage.config.js
├── constant
│   └── index.js
├── pages
│   ├── find
│   ├── home
│   ├── index
│   ├── message
│   └── mine
├── static
│   ├── images
│   └── js
├── store
│   └── index.js
├── styles
│   └── index.scss
├── uni_modules
│   ├── limm-utools
│   ├── limm-windi-css-uniapp
│   └── uview-ui
├── utils
│   ├── libs
│   ├── request
│   └── index.js
├── App.vue
├── CHANGELOG.md
├── README.md
├── index.html
├── jsconfig.json
├── main.js
├── manifest.json
├── package.json
├── pages.json
├── stylelint.config.js
├── uni.scss
└── yarn.lock
```

**生成命令**

```shell
tree -L 2 -I "node_modules" --dirsfirst
```

### 你需要修改的信息

- `package.json`
  - `name`
  - `version`
  - `repository`
  - `license`
  - `author`
- `src/manifest.json` 到 `HbuilderX` 内的可视化界面去修改吧，如果没出现可视化界面，把项目从 `HbuilderX` 移除重新添加，或者右键`重新构建项目索引`、`重新识别项目类型`，关闭 `manifest.json` 再打开就会出现可视化配置界面了
  - `uni-app 应用标识`
  - `应用名称`
  - `应用描述`
  - `版本名`
  - `版本号`
  - `App 图标配置`
- 删除本项目说明

## 注意

项目使用 yarnv3 版本管理依赖，禁用 npm,pnpm 等其他的包管理工具，会出现各种问题！

## 更新日志

[更新日志](./CHANGELOG.md)

## 关于和联系

如果对项目使用有问题可以提交 issue 或者直接联系 `QQ: 1647800606`。解决了问题记得请我喝咖啡 🥹。

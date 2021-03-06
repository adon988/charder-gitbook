# Bower

* 是 Twitter 團隊開發的一套前端套件管理工具
* 預設目錄在 bower_components

<!-- bowerbrid -->

**使用情境**

* 管理專案中使用的錯綜複雜的外部套件，主要以前端用的 HTML、JS、CSS 為主。

**npm vs bower**

| 名稱   | 主要支援  | 結構 |
| ----- | -------- | ------ |
| bower | 前端 JS | 扁平化 |
| npm   | 後端 JS | 樹狀   |

**安裝 bower**

```
npm install bower -g
```

### 常用指令

* [Bower - Commands](https://bower.io/docs/api/)

```
bower init
bower install
bower install bootstrap
// 離線安裝
bower install bootstrap --offline

bower uninstall bootstrap
bower update bootstrap
bower search bootstrap
bower lookup bootstrap
bower list
bower -help
bower -v
bower cache list
bower cache clean
```

### bower.json

專案有關的配置

```json
{
  name: 'demo',
  authors: [
    'alincode <alincode@gmail.com>'
  ],
  description: '',
  main: '',
  license: 'MIT',
  homepage: '',
  ignore: [
    '**/.*',
    'node_modules',
    'bower_components',
    'test',
    'tests'
  ]
}
```

### .bowerrc

環境有關的配置

* directory
* scripts
* [resolvers](https://bower.io/docs/pluggable-resolvers/)

```json
{
  "cwd": "~/.my-project",
  "directory": "bower_components",
  "registry": "https://bower.herokuapp.com",
  "shorthand-resolver": "git://github.com//.git",
  "proxy": "http://proxy.local",
  "https-proxy": "http://proxy.local",
  "ca": "/var/certificate.pem",
  "color": true,
  "timeout": 60000,
  "save": true,
  "save-exact": true,
  "strict-ssl": true,
  "storage": {
    "packages" : "~/.bower/packages",
    "registry" : "~/.bower/registry",
    "links" : "~/.bower/links"
  },
  "interactive": true,
  "resolvers": [
    "mercurial-bower-resolver"
  ],
  "shallowCloneHosts": [
    "myGitHost.example.com"
  ],
  "scripts": {
    "preinstall": "",
    "postinstall": "",
    "preuninstall": ""
  },
  "ignoredDependencies": [
    "jquery"
  ]
}
```

### 前端使用方式

```html
<script src="bower_components/jquery/dist/jquery.min.js"></script>
```

### 練習題

* 建立 bower 專案檔

```
cd your-project-folder
bower init
```

* 將安裝路徑從 bower_components 更改路徑為 lib。

```
rm -rf bower_components
touch .bowerrc
vi .bowerrc
```

```json
{
  "directory": "lib"
}
```

```
bower install
```

### Bower "Git not in the PATH" error

![](https://cloud.githubusercontent.com/assets/10702007/10532690/d2e8991a-7386-11e5-9a57-613c7f92e84e.png)

* 安裝 [Git for Windows](https://git-for-windows.github.io/)
* [GitHub - bower/bower: A package manager for the web](https://github.com/bower/bower#windows-users)
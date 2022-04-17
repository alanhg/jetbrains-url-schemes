# jetbrains-url-schemes
链接跳转到JB IDE且自动执行某个动作

## Requirement
- 安装JetBrains Toolbox
- 安装需要打开的JB家IDE，比如WebStorm

## JB各IDE-toolTag说明

scheme链接中使用tag

```js
{
  idea: {
    name: 'IntelliJ IDEA',
    tag: 'idea',
  },
  appcode: {
    name: 'AppCode',
    tag: 'appcode',
  },
  clion: {
    name: 'CLion',
    tag: 'clion',
  },
  pycharm: {
    name: 'PyCharm',
    tag: 'pycharm'
  },
  phpstorm: {
    name: 'PhpStorm',
    tag: 'php-storm'
  },
  rubymine: {
    name: 'RubyMine',
    tag: 'rubymine'
  },
  webstorm: {
    name: 'WebStorm',
    tag: 'web-storm'
  },
  rider: {
    name: 'Rider',
    tag: 'rd'
  },
  goland: {
    name: 'GoLand',
    tag: 'goland'
  }
}
```

## checkout某个仓库，使用对应对应IDE打开

```
jetbrains://${toolTag}/checkout/git?checkout.repo=${cloneUrl}&idea.required.plugins.id=Git4Idea
```

例子
```
jetbrains://webstorm/checkout/git?checkout.repo=https://github.com/alanhg/alfred-workflows&idea.required.plugins.id=Git4Idea
```


## 打开某仓库，某文件及移动到对应行列位置

```
jetbrains://${toolTag}/navigate/reference?project=${project}&path=${filePath}:${lineIndex}:${columnIndex}
```

例子
```
jetbrains://webstorm/navigate/reference?project=alfred-workflows&path=${filePath}:${lineIndex}:${columnIndex}
```

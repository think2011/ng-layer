## 概述
对[layer](http://layer.layui.com/)的angular封装，同时增加异步载入content的功能

## 下载
1. 推荐使用 bower install ng-layer

## 使用
1. 引入layer自身，再引入ng-layer

2. 注册模块

```js
angular.module('app', ['ng-layer']);
```

3. 使用

```js
var layerId = layer.open({
    contentUrl: 'modules/home/index.html',  // 额外增加的方法，正如其名，当然也还可以用content
    scope     : $scope  // 当前content环境中的$scope
});

// layer.close(layerId); 
```


## 兼容
理论上支持任何版本的layer，除非layer更改了核心功能
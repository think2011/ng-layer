## 概述
对[layer](http://layer.layui.com/)的angular封装，同时增加异步载入content的功能

## 下载
1. 推荐使用 `bower install ng-layer`
2. 当然也可以直接复制 `ng-layer.js` 文件

## 使用
①. 引入layer自身，再引入ng-layer

②. 注册模块

```js
angular.module('app', ['ng-layer']);
```

③. 使用

支持标准方式 和 controller as方式(感谢@wandergis)

标准方式
```js
var layerId = layer.open({
    contentUrl: 'modules/home/index.html',  // 额外增加的方法，正如其名
    scope: $scope
});

// layer.close(layerId); 
```

controller as方式
```js
var layerId = layer.open({
    // contentUrl: 'modules/home/index.html'，当然也还可以用原来的content
    content: '<div controller="appCtrl as vm">{{vm.name}}</div>'
});

// layer.close(layerId);
```

[具体可以查看demo文件](http://think2011.net/ng-layer)

## 兼容
理论上支持任何版本的layer，除非layer更改了核心功能

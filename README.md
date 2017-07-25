# angular-notes
1.3.1.14



### viwe 路由

```js
var bookStoreApp = angular.module('bookStoreApp', [
    'ngRoute', 'ngAnimate', 'bookStoreCtrls', 'bookStoreFilters',
    'bookStoreServices', 'bookStoreDirectives'
]);

bookStoreApp.config(function($routeProvider) {
    $routeProvider.when('/hello', {   //发现地址栏为 hello 的时候  就执行以下
        templateUrl: 'tpls/hello.html',// 调用该目录下的模板
        controller: 'HelloCtrl' //  引用该控制器来处理
    }).when('/list', {
        templateUrl: 'tpls/bookList.html',
        controller: 'BookListCtrl'
    }).otherwise({ //其他情况就跳到 该下面
        redirectTo: '/hello'
    })
});

```

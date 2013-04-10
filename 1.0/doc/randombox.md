## 综述

RandomBox是一个随机选择的组件，可作为前端随机摇奖效果的实现。

* 版本：1.0
* 基于：kissy1.20或者更高版本
* 作者：胡潇琪


## demo

[点击访问](http://docs.kissyui.com/kissy-gallery/gallery/randombox/1.0/demo/default.html)

## 组件使用

kissy1.2下需要gallery的包配置：

```javascript
KISSY.config({
    packages:[
        {
            name:"gallery",
            path:"http://a.tbcdn.cn/s/kissy/",
            charset:"utf-8"
        }
    ]
});
```


### 1.加载RandomBox模块,初始化RandomBox

```javascript
    KISSY.use('gallery/randombox/1.0/index', function (S, RandomBox) {
       var  box = new RandomBox({
            //配置id数组   "#"号勿忘
            list:["#b1","#b2","#b3","#b4","#b5",    
                  "#b10","#b15","#b20","#b25","#b24",
                  "#b23","#b22","#b21","#b16","#b11",
                  "#b6","#b7","#b8","#b9","#b14",
                  "#b19","#b18","#b17","#b12","#b13"],
            //配置旋转圈数
            rollTimes:2,
            //配置CSS类名  （选中时效果）
            cls:"sel-item", 
            //配置动画周期 (ms)
            duration:40
            //配置最终选中的id "#"号勿忘 不填为随机 
            //finalId:"#b6"     
        },function(targetId){
            //执行选中后的回调函数
            setTimeout(function(){alert("你选中了"+$(targetId).html());},400);
        });
    })
```
**提醒**：use()的回调，第一个参数是KISSY，第二个参数才是组件。


### 2. 方法
start 开始,stop 停止,reset 复位



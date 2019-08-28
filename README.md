# vue-依赖注入特性

## 首先下载clone代码到本地，然后安装依赖
```
npm install
```

### 运行项目
```
npm run serve
```

项目一个创建了四个组件
* root组件
* father组件
* son组件
* grandson组件
并且在App组件中完成嵌套关系。
``` html
<Root>
    <Father>
        <Son>
        	<Grandson></Grandson>
        </Son>
    </Father>
</Root>
```
root根组件中设置provide属性
``` js
 provide(){
      return{
        rootA:this.rootA,
        rootNum: this.rootNum,
        rootFun:this.rootFun
    }
  }
```

> 在后边的三个组件中都可以调用到这个provide依赖提供的数据

在Fathter、Son、Grandson中，设置inject注入属性
``` js
inject:["rootA","rootNum","rootFun"],
```





# Object-character 面向对象三特性-多态、继承、封装性
> 只讲多态和继承
## 继承
> 字面意思,继承上一辈的东西.

> 需要拥有父级的基础,又拥有自己的个性。否则就叫做copy。
- 为什么要使用继承?
> 把相同的东西放到基类/父类

> 本质是为了避免重复,统一管理对象集

> 实现继承的代码

    /*父子类*/
    var Father = function(){
        this.type = 'person';
        this.age = 45;
    }
    Father.prototype = {
        takeMoney:function(){
            console.log(20000);
        }
    }
    var Son = function(){
        //固定用法
        Father.call(this.arguments);
    }
    Son.prototype = new Father();
    Son.prototype.stuy = function(){
        console.log('study');
    }
    var xiaoMing = new Son();
    console.log(xiaoMing.type);//person
## 多态
> 比如淘宝上买东西
大家都有buy这个方法,但是买的过程肯定不一样.
你买实物,要下单,等物流,收货
买电影票,只要下单,扫码就可以了.
- 对象的多态,方法的多态

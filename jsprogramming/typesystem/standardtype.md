# 标准类型（原始类型、引用类型）
1、 [简介]()<br />
2、 [堆栈、复制说明]()<br />
3、
```
/*
BEGIN   FOR EACH
    类型说明
    出现场景
    类型转换
END
*/
```
4、 [类型转换总结]()<br />
　　　　o [案例]()
### 简介
![](241.PNG)<br />
### 堆栈、复制说明
![](2411.PNG)<br />
![](2412.PNG)<br />
<br />
```
/*
BEGIN   FOR EACH
    类型说明
    出现场景
    类型转换
END
*/
```
![](2413.PNG)<br /><br />
Note: <br />
**出现场景:**<br />
* 已声明未赋值的变量：a显示声明后未赋值   b隐式声明后未赋值<br />
![](24131.PNG)<br />
* 获取对象不存在的属性<br />
![](24132.PNG)
* 无返回值的函数的执行结果<br />
![](24133.PNG)
* 函数未传入的参数<br />
![](24134.PNG)<br />
**案例：**<br />
![](24135.PNG)![](24136.PNG)<br />
![](24137.PNG)![](24138.PNG)<br />
![](24139.PNG)![](241310.PNG)<br />
<br />
![](2414.PNG)<br />
![](2415.PNG)<br />
![](2416.PNG)<br />
![](2417.PNG)<br />
![](2418.PNG)<br />
<br />
### 类型转换总结<br />

| type | Value | Boolean | Number | String |
| -- | -- | -- | -- | -- |
| **Undefined** | undefined | false | **NaN** | "undefined" |
| **Null** | null | false | 0 | "null" |
| **Boolean** | true |  | 1 | **"null"** |
|  | true |  | 0 | "false" |
| **String** | "" | false | 0 |  |
|  | "123" | true | 123 |  |
|  | "1a" | true | **NaN** |  |
| **Number** | 0 | false |  | "0" |
|  | 1 | true |  | "1" |
|  | -1 | true |  | "-1" |
|  | Infinity | true |  | "Infinity" |
|  | NaN | **false** |  | **"NaN"** |
| **Object** | {} | **true** | **NaN** | **"[object Object]"** |

![](2419.png)<br />
* 左边Object转String：toString后如果是原始值就直接到String，如果是引用值就valueOf()然后到String
* 右边Object转Number：优先级不同流程同上
* Object转String或Number：若没有明确Object具体转的类型，那么走的是右边的路，除了Date对象之外？ demo如下结果为面积之和
加号两边若有一个为String类型则进行的是连接

* 每个JavaScript固有对象的 valueOf，toString 方法定义不同。 》http://www.jb51.net/article/32327.htm
<br />
    * **案例**
![](24191.png)<br />
![](24193.png)<br />
结果：首先类型转换，然后值相加
![](24194.PNG)

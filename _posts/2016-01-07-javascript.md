---
layout: post
category : javascript
tagline: "Supporting tagline"
tags : ['javascript']
---
{% include JB/setup %}

# Javascript类
1. 使用new调用构造函数会自动创建一个新对象，因此构造函数
本身只需要初始化这个新对象的状态即可。  调用构造函数的一个重要特征
是，！！构造函数的prototype属性被用作新对象的原型！！ 这意味着通过同一
个构造函数创建的所有对象都继承自一个相同的对象，因此他们都是同一个类的
成员

2. 每个javascript函数（ECMAScript 5中的Function.bind()方法返回的函数除
外）都自动拥有一个prototype属性。这个属性的值是一个对象，这个对象包含
唯一一个不可枚举属性constructor。constructor属性的值是一个函数对象
(ablian认为，这个函数对象，就是相应的那个javascript函数)。例
如,`A.prototype.constructor === A(其中A是一个javascript函数)`

3. javascript的类，其中实现的话，一个关键点就是构造函数反向引用。即，
A.prototype.constructor一定要===A。如果你使用一个新的对象来覆盖
A.prototype，那么，这个对象，你一定要显示写一个constructor字段，并且等
于A。即，如果`A.prototype ={}`这样的写法，你要`A.prototype
={constructor:A, ...}`

4. Javascript中定义类的步骤:
   1. 先定义一个构造函数，并设置初始化新对象的实例属性
   2. 给构造函数的prototype对象定义实例的方法
   3. 给构造函数定义类字段和类属性

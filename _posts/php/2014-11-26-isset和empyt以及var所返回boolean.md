---
title: isset和empyt以及$var所返回的boolean
layout: post
tags:
categories:
    - php
---

### isset($var)
```
return false
$var未设置，或者是NULL

return true
$var已设置，并且不是NULL
```



### empty($var)
```
return false
// 如果 var 是非空或非零的值，则 empty() 返回 FALSE。
// ‘0.0’

return true
// 换句话说，""、0、"0"、NULL、FALSE、array()、var $var; 以及没有任何属性的对象都将被认为是空的，如果 var 为空，则返回 TRUE。
```



### if ($var)
```
return false
// 布尔值 FALSE 本身
// 整型值 0（零）
// 浮点型值 0.0（零）
// 空字符串，以及字符串 "0"
// 不包括任何元素的数组
// 不包括任何成员变量的对象（仅 PHP 4.0 适用）
// 特殊类型 NULL（包括尚未赋值的变量）
// 从空标记生成的 SimpleXML 对象

return true
// 所有其它值都被认为是 TRUE（包括任何资源)
```

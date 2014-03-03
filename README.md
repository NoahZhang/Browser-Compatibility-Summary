浏览器兼容性汇总
=============================
1. IE6-8不支持defaultView(返回当前 document 对象所关联的 window 对象)
2. IE6-7取得class属性时，必须通过getAttribute('className'),并且readonly返回布尔类型，该函数还可以指定整形类型的参数，1代表执行case-sensitive的查找，2代表以字符串形式返回attribute的值
3. IE9 matchesSelector当node为disconnected nodes时,返回false
4. IE < 9 getAttribute("value")时，使用defaultValue替代
5. IE < 9 getAttribute取不到form的name属性，使用getAttributeNode替代
6. IE6-7的circular references导致内存泄露
7. IE自动删除.innerHTML值的前置空白字符
8. IE自动为空table补上tbody
9. IE < 9 取得事件源通过event.srcElement，其他通过event.target
10. IE < 9 阻止浏览器的默认行为returnValue = false，其他通过调用preventDefault，停止事件冒泡IE cancelBubble = true, 其他通过调用stopPropagation 
11. IE6-8 can't serialize link, script, style, or any html5 (NoScope) tags,unless wrapped in a div with non-breaking characters in front of it.
12. IE < 8 操作table时，必须添加tbody
13. IE 禁止删除expando properties,必须通过removeAttribute
14. IE < 9确保select显示空白，options.length = 0
15. 定义css浮动，IE使用el.style.styleFloat，其他使用cssFloat
16. IE取得样式信息使用el.cssText,其他通过.getAttribute("style") 
17. IE创建ajax请求window.ActiveXObject( "Microsoft.XMLHTTP" )，非IE window.XMLHttpRequest()
18. IE 绑定事件elem.attachEvent( "on" + type, eventHandle )，非IE elem.addEventListener( type, eventHandle, false )
19. IE < 9 不支持Array的如下方法：map,forEach,filter,every,some,reduce,lastIndexOf,indexOf,reduceRight

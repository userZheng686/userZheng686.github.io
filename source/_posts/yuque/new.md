---
title: new
urlname: nkdh0y
date: '2021-04-14 00:25:34 +0800'
tags: []
categories: []
---

```javascript
function news(obj, ...args) {
  var obj2 = {};
  obj2.__proto__ = obj.prototype;
  obj.call(obj2);

  for (var i = 0; i < args.length; i++) {
    var key = Object.keys(obj2)[i];
    obj2[key] = args[i];
  }
  // let obj3 = Array.apply(obj2,obj.prototype.constructor)
  return obj2;
}
```

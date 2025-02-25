---
title: CustomEvent()
slug: Web/API/CustomEvent/CustomEvent
---

{{APIRef("DOM")}}

The **`CustomEvent()`** constructor creates a new {{domxref("CustomEvent")}}.

构造方法 CustomerEvent() 创建一个新的 {{domxref("CustomEvent")}} 对象。

## 语法

```js-nolint
new CustomEvent(type)
new CustomEvent(type, options)
```

### 参数

- _typeArg_
  - : 一个表示 event 名字的字符串
- _customEventInit_

  - : Is a `CustomEventInit` dictionary, having the following fields: 一个字典类型参数，有如下字段

    - `"detail"`, optional and defaulting to `null`, of type any, that is a event-dependant value associated with the event. 可选的默认值是 null 的任意类型数据，是一个与 event 相关的值
    - bubbles 一个布尔值，表示该事件能否冒泡。来自 {{domxref("Event.Event", "EventInit")}}。注意：测试 chrome 默认为不冒泡。
    - cancelable 一个布尔值，表示该事件是否可以取消。来自 {{domxref("Event.Event", "EventInit")}}

    <div class="note"><p><em>The <code>CustomEventInit</code></em><em> dictionary also accepts fields from the {{domxref("Event.Event", "EventInit")}} dictionary.</em></p><p>CustomerEventInit 字典参数同样接受来自于 Event 类构造函数的 eventInit 字典参数，如下</p><p>bubbles 一个布尔值，表示该事件能否冒泡</p><p>cancelable 一个布尔值，表示该事件是否可以取消</p></div>

## 示例

```js
// add an appropriate event listener
obj.addEventListener("cat", function (e) {
  process(e.detail);
});

// create and dispatch the event
var event = new CustomEvent("cat", {
  detail: {
    hazcheeseburger: true,
  },
});
obj.dispatchEvent(event);
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{domxref("CustomEvent")}}

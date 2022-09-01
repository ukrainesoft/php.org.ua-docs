---
navigation:
  - yaf-route-supervar.construct.html: '« YafRouteSupervar::construct'
  - class.yaf-session.html: YafSession »
  - index.md: PHP Manual
  - class.yaf-route-supervar.html: YafRouteSupervar
title: 'YafRouteSupervar::route'
---
# YafRouteSupervar::route

(Yaf >=1.0.0)

YafRouteSupervar::route — Призначення route

### Опис

```methodsynopsis
public Yaf_Route_Supervar::route(Yaf_Request_Abstract $request): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`request`

### Значення, що повертаються

Якщо у $GET є ключ (який був визначений у [YafRouteSupervar::construct()](yaf-route-supervar.construct.html)), поверне **`true`**, інакше поверне **`false`**

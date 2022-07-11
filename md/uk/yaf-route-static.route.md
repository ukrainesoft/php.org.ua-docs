- [« Yaf_Route_Static::match](yaf-route-static.match.md)
- [Yaf_Route_Supervar »](class.yaf-route-supervar.md)

- [PHP Manual](index.md)
- [Yaf_Route_Static](class.yaf-route-static.md)
- Надсилає запит

# Yaf_Route_Static::route

(Yaf \>=1.0.0)

Yaf_Route_Static::route — Надсилає запит

### Опис

public
**Yaf_Route_Static::route**([Yaf_Request_Abstract](class.yaf-request-abstract.md)
`$request`): bool

**Увага**

На цей час ця функція ще була документована; для
ознайомлення доступний лише список аргументів.

### Список параметрів

`request`

### Значення, що повертаються

Завжди повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Yaf_Route_Static::route()****

`` shellcode
// за умови, що визначено лише один модуль:Index
Запит: http://yourdomain.com/a/b
=> module = index, controller=a, action=b

//за умови, що ap.action_prefer = On
Запит: http://yourdomain.com/b
=> module = default(index), controller = default(index), action = b

//за умови, що ap.action_prefer = Off
Запит: http://yourdomain.com/b
=> module = default(index), controller = b, action = default(index)


Запит: http://yourdomain.com/a/b/foo/bar/test/a/id/4
=> module = default(index), controller = a, action = b, параметри запиту: foo = bar, test = a, id = 4
````

### Дивіться також

- [Yaf_Route_Supervar::route()](yaf-route-supervar.route.md) -
Призначення route
- [Yaf_Route_Simple::route()](yaf-route-simple.route.md) -
Надсилає запит
- [Yaf_Route_Regex::route()](yaf-route-regex.route.md) - Ціль
маршруту
- [Yaf_Route_Rewrite::route()](yaf-route-rewrite.route.md) -
Призначення route
- [Yaf_Route_Map::route()](yaf-route-map.route.md) - Призначення
route

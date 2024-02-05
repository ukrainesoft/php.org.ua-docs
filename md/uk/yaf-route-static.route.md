---
navigation:
  - yaf-route-static.match.md: '« Yaf\_Route\_Static::match'
  - class.yaf-route-supervar.md: Yaf\_Route\_Supervar »
  - index.md: PHP Manual
  - class.yaf-route-static.md: Yaf\_Route\_Static
title: 'Yaf\_Route\_Static::route'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Route\_Static::route

(Yaf >=1.0.0)

Yaf\_Route\_Static::route — Надсилає запит

### Опис

```methodsynopsis
public Yaf_Route_Static::route(Yaf_Request_Abstract $request): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`request`

### Значення, що повертаються

Завжди повертає **`true`**

### Приклади

**Приклад #1 Приклад використання** Yaf\_Route\_Static::route()\*\*\*\*

// за умови, що визначено лише один модуль: Index Запит: [http://yourdomain.com/a/b](http://yourdomain.com/a/b) => module = index, controller=a, action=b

//за умови, що ap.action\_prefer = On Запрос:[http://yourdomain.com/b](http://yourdomain.com/b) => module = default(index), controller = default(index), action = b

//за умови, що ap.action\_prefer = Off Запрос:[http://yourdomain.com/b](http://yourdomain.com/b) => module = default(index), controller = b, action = default(index)

Запит: [http://yourdomain.com/a/b/foo/bar/test/a/id/4](http://yourdomain.com/a/b/foo/bar/test/a/id/4)\=> module = default(index), controller = a, action = b, параметри запиту: foo = bar, test = a, id = 4

### Дивіться також

-   [Yaf\_Route\_Supervar::route()](yaf-route-supervar.route.md) \- Призначення route
-   [Yaf\_Route\_Simple::route()](yaf-route-simple.route.md) \- Надсилає запит
-   [Yaf\_Route\_Regex::route()](yaf-route-regex.route.md) \- Мета маршруту
-   [Yaf\_Route\_Rewrite::route()](yaf-route-rewrite.route.md) \- Призначення route
-   [Yaf\_Route\_Map::route()](yaf-route-map.route.md) \- Призначення route

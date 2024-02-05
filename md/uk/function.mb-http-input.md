---
navigation:
  - function.mb-get-info.md: « mb\_get\_info
  - function.mb-http-output.md: mb\_http\_output »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_http\_input
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_http\_input

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_http\_input — Визначає кодування символів вхідних даних HTTP-запиту

### Опис

```methodsynopsis
mb_http_input(?string $type = null): array|string|false
```

Визначає кодування символів вхідних даних запиту HTTP.

### Список параметрів

`type`

Рядок запиту визначає тип вхідних даних. Значення `«G»`для GET запроса,`«P»`для POST запроса,`«C»`для COOKIE,`«S»` для рядків, `«L»`для списка и`«I»` для всього разом (вернеться масив (array)). Якщо аргумент опущений, функція поверне останній тип вхідних даних.

### Значення, що повертаються

Повертає назву кодування символів для заданого типу (`type`) або масив імен символьних кодувань, якщо параметр `type`задан как`«I»`. Якщо функція **mb\_http\_input()** не може обробити HTTP-запит, вона поверне **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`type` тепер може набувати значення **`null`** |

### Дивіться також

-   [mb\_internal\_encoding()](function.mb-internal-encoding.md) \- Встановлює/отримує внутрішнє кодування скрипту
-   [mb\_http\_output()](function.mb-http-output.md) \- Встановлює/отримує кодування символів виводу HTTP
-   [mb\_detect\_order()](function.mb-detect-order.md) \- Встановлює/отримує порядок визначення кодування символів

---
navigation:
  - function.mb-http-input.md: « mb\_http\_input
  - function.mb-internal-encoding.md: mb\_internal\_encoding »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_http\_output
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_http\_output

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_http\_output — Встановлює/отримує кодування символів виводу HTTP

### Опис

```methodsynopsis
mb_http_output(?string $encoding = null): string|bool
```

Встановлює/отримує кодування символів виводу HTTP. Вихідні дані після роботи цієї функції будуть перетворені з внутрішнього кодування до значення параметра `encoding`

### Список параметрів

`encoding`

Если задан параметр`encoding`, функция**mb\_http\_output()** встановлює кодування вихідних символів HTTP значення параметра `encoding`

Якщо аргумент `encoding`опущен, функция**mb\_http\_output()** повертає поточне кодування символів виводу HTTP.

### Значення, що повертаються

Якщо аргумент `encoding`опущен, функция**mb\_http\_output()** повертає поточне кодування символів виводу HTTP. В іншому випадку Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |

### Дивіться також

-   [mb\_internal\_encoding()](function.mb-internal-encoding.md) \- Встановлює/отримує внутрішнє кодування скрипту
-   [mb\_http\_input()](function.mb-http-input.md) \- Визначає кодування символів вхідних даних HTTP-запиту
-   [mb\_detect\_order()](function.mb-detect-order.md) \- Встановлює/отримує порядок визначення кодування символів

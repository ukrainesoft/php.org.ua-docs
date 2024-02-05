---
navigation:
  - function.mb-send-mail.md: « mb\_send\_mail
  - function.mb-str-pad.md: mb\_str\_pad »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_split
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_split

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

mb\_split — Розділяє рядки в багатобайтних кодуваннях через регулярний вираз.

### Опис

```methodsynopsis
mb_split(string $pattern, string $string, int $limit = -1): array|false
```

Розділяє багатобайтний рядок `string`, зіставляючи її з регулярним виразом `pattern`і повертає масив (array).

### Список параметрів

`pattern`

Шаблон регулярного виразу.

`string`

Рядок, що розбивається (string).

`limit`

Якщо необов'язковий параметр `limit` заданий, функція розіб'є рядок не більше, ніж на `limit`частей.

### Значення, що повертаються

Повертає результат розбиття у вигляді масиву (array) або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Кодування символів, вказане функцією [mb\_regex\_encoding()](function.mb-regex-encoding.md), буде за промовчанням використана для цієї функції.

### Дивіться також

-   [mb\_regex\_encoding()](function.mb-regex-encoding.md) \- Встановлює/отримує кодування символів для однобайтового регулярного виразу
-   [mb\_ereg()](function.mb-ereg.md) \- Знаходить збіг регулярного виразу за допомогою багатобайтових кодувань

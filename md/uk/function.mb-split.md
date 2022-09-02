---
navigation:
  - function.mb-send-mail.md: « mbsendmail
  - function.mb-str-split.md: мбstrsplit »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбsplit
---
# мбsplit

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

мбsplit — Поділ рядків у багатобайтних кодуваннях, використовуючи регулярний вираз.

### Опис

```methodsynopsis
mb_split(string $pattern, string $string, int $limit = -1): array|false
```

Розділяє багатобайтний рядок `string`, використовуючи регулярний вираз `pattern`і повертає масив (array).

### Список параметрів

`pattern`

Шаблон регулярного виразу.

`string`

Рядок, що розбивається (string).

`limit`

Якщо необов'язковий аргумент `limit` заданий, функція розіб'є рядок не більше, ніж на `limit` частин.

### Значення, що повертаються

Результат розбиття у вигляді масиву (array) або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Кодування символів, вказане функцією [мбregexencoding()](function.mb-regex-encoding.md), буде за замовчуванням використана для цієї функції.

### Дивіться також

-   [мбregexencoding()](function.mb-regex-encoding.md) - Встановлює/отримує поточне кодування для багатобайтового регулярного виразу
-   [мбereg()](function.mb-ereg.md) - Збіг з регулярним виразом з підтримкою багатобайтових кодувань

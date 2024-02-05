---
navigation:
  - function.bzerrstr.md: « bzerrstr
  - function.bzopen.md: bzopen »
  - index.md: PHP Manual
  - ref.bzip2.md: Функції Bzip2
title: bzflush
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# bzflush

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

bzflush - Нічого не робить

### Опис

```methodsynopsis
bzflush(resource $bz): bool
```

Функція повинна примусово записувати всі буферизовані дані bzip2 у файл, який посилається покажчик `bz`але в libbz2 реалізована як нульова функція і тому нічого не робить.

### Список параметрів

`bz`

Вказівник на файл. Має бути коректним і вказувати на файл, успішно відкритий [bzopen()](function.bzopen.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [bzread()](function.bzread.md) \- Бінарно-безпечне читання файлу bzip2
-   [bzwrite()](function.bzwrite.md) \- Бінарно-безпечний запис bzip2 файлу

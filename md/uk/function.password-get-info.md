---
navigation:
  - function.password-algos.md: « password\_algos
  - function.password-hash.md: password\_hash »
  - index.md: PHP Manual
  - ref.password.md: Функції хешування паролів
title: password\_get\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# password\_get\_info

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

password\_get\_info — Повертає інформацію про заданий хеш

### Опис

```methodsynopsis
password_get_info(string $hash): array
```

Якщо передано коректний хеш, створений підтримуваним [password\_hash()](function.password-hash.md) алгоритмом, то ця функція поверне інформацію про це хеш.

### Список параметрів

`hash`

Хеш, створений функцією [password\_hash()](function.password-hash.md)

### Значення, що повертаються

Повертає асоціативний масив із трьома елементами:

-   `algo`, що містить одну з[констант алгоритмів паролів](password.constants.md)
-   `algoName`, Що містить ім'я алгоритму в людиночитаному вигляді
-   `options`, що включає опції, передані під час виклику[password\_hash()](function.password-hash.md)

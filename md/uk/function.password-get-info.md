---
navigation:
  - function.password-algos.md: « passwordalgos
  - function.password-hash.md: passwordhash »
  - index.md: PHP Manual
  - ref.password.md: Функції хешування паролів
title: passwordgetinfo
---
# passwordgetinfo

(PHP 5> = 5.5.0, PHP 7, PHP 8)

passwordgetinfo — Повертає інформацію про заданий хеш

### Опис

```methodsynopsis
password_get_info(string $hash): array
```

Якщо передано коректний хеш, створений підтримуваним [passwordhash()](function.password-hash.md) алгоритмом, то ця функція поверне інформацію про це хеш.

### Список параметрів

`hash`

Хеш, створений функцією [passwordhash()](function.password-hash.md)

### Значення, що повертаються

Повертає асоціативний масив із трьома елементами:

-   `algo`, що містить одну з [констант алгоритмов паролей](password.constants.md)
-   `algoName`, Що містить ім'я алгоритму в людиночитаному вигляді
-   `options`, що включає опції, передані під час виклику [passwordhash()](function.password-hash.md)

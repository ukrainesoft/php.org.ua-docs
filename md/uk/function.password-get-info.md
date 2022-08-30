Повертає інформацію про заданий хеш

-   [« passwordalgos](function.password-algos.html)
    
-   [passwordhash »](function.password-hash.html)
    
-   [PHP Manual](index.html)
    
-   [Функції хешування паролів](ref.password.html)
    
-   Повертає інформацію про заданий хеш
    

# passwordgetinfo

(PHP 5> = 5.5.0, PHP 7, PHP 8)

passwordgetinfo — Повертає інформацію про заданий хеш

### Опис

```methodsynopsis
password_get_info(string $hash): array
```

Якщо передано коректний хеш, створений підтримуваним [passwordhash()](function.password-hash.html) алгоритмом, то ця функція поверне інформацію про це хеш.

### Список параметрів

`hash`

Хеш, створений функцією [passwordhash()](function.password-hash.html)

### Значення, що повертаються

Повертає асоціативний масив із трьома елементами:

-   `algo`, що містить одну з [констант алгоритмов паролей](password.constants.html)
-   `algoName`, Що містить ім'я алгоритму в людиночитаному вигляді
-   `options`, що включає опції, передані під час виклику [passwordhash()](function.password-hash.html)
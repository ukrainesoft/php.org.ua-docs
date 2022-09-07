---
navigation:
  - function.posix-setpgid.md: « posixsetpgid
  - function.posix-setsid.md: posixsetsid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixsetrlimit
---
# posixsetrlimit

(PHP 7, PHP 8)

posixsetrlimit - Встановлює межі системних ресурсів

### Опис

```methodsynopsis
posix_setrlimit(int $resource, int $soft_limit, int $hard_limit): bool
```

**posixsetrlimit()** встановлює жорсткі та м'які межі заданих системних ресурсів.

З кожним ресурсом асоційовані свої м'які та жорсткі обмеження. М'які обмеження - величина, яку ядро ​​обіцяє забезпечити ресурсу. Жорсткі обмеження – це величина, що характеризує стелю м'яких ресурсів. Непривілейований процес може управляти лише своїми м'якими обмеженнями, виставляючи їх від 0 до величини жорсткого обмеження.

### Список параметрів

`resource`

[Константа предела ресурса](posix.constants.setrlimit.md) що відповідає за межу, яка має бути встановлена.

`soft_limit`

М'яка межа, будь-яка необхідна межа, або **`POSIX_RLIMIT_INFINITY`**

`hard_limit`

Жорстка межа, будь-яка необхідна межа, або **`POSIX_RLIMIT_INFINITY`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   man page SETRLIMIT(2)
-   [posixgetrlimit()](function.posix-getrlimit.md) - Повертає інформацію про обмеження системних ресурсів

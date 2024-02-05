---
navigation:
  - function.posix-setpgid.md: « posix\_setpgid
  - function.posix-setsid.md: posix\_setsid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_setrlimit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_setrlimit

(PHP 7, PHP 8)

posix\_setrlimit - Встановлює межі системних ресурсів

### Опис

```methodsynopsis
posix_setrlimit(int $resource, int $soft_limit, int $hard_limit): bool
```

**posix\_setrlimit()** встановлює жорсткі та м'які межі заданих системних ресурсів.

З кожним ресурсом асоційовані свої м'які та жорсткі обмеження. М'які обмеження це величина, яку ядро ​​обіцяє забезпечити ресурсу. Жорсткі обмеження - це величина, що характеризує стелю м'яких ресурсів. Непривілейований процес може керувати лише своїми м'якими обмеженнями, виставляючи їх від 0 до величини жорсткого обмеження.

### Список параметрів

`resource`

[Константа межі ресурсу](posix.constants.setrlimit.md) що відповідає за межу, яка має бути встановлена.

`soft_limit`

М'яка межа, будь-яка необхідна межа, або **`POSIX_RLIMIT_INFINITY`**

`hard_limit`

Жорстка межа, будь-яка необхідна межа, або **`POSIX_RLIMIT_INFINITY`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   man page SETRLIMIT(2)
-   [posix\_getrlimit()](function.posix-getrlimit.md) \- Повертає інформацію про обмеження системних ресурсів

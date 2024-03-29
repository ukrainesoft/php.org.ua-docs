---
navigation:
  - function.posix-getpwuid.md: « posix\_getpwuid
  - function.posix-getsid.md: posix\_getsid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_getrlimit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_getrlimit

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_getrlimit — Повертає інформацію про обмеження системних ресурсів

### Опис

```methodsynopsis
posix_getrlimit(?int $resource = null): array|false
```

**posix\_getrlimit()** повертає array з інформацією про поточні м'які та жорсткі обмеження системних ресурсів.

З кожним ресурсом асоційовані свої м'які та жорсткі обмеження. М'які обмеження це величина, яку ядро ​​обіцяє забезпечити ресурсу. Жорсткі обмеження - це величина, що характеризує стелю м'яких ресурсів. Непривілейований процес може керувати лише своїми м'якими обмеженнями, виставляючи їх від 0 до величини жорсткого обмеження.

### Список параметрів

`resource`

Если указано значение\*\*`null`\*\*, то буде знайдено всі обмеження ресурсів. Інакше буде повернено лише обмеження наданого типу ресурсу.

### Значення, що повертаються

Повертає асоціативний array, кожен елемент якого відповідає певному обмеженню. Кожен ліміт має м'яке та жорстке обмеження.

**Список можливих обмежень**

| Ограничение | Опис ограничения |
| --- | --- |
| core | Максимальний розмір файлу. У разі некоректного завершення програми операційна система завершує цей процес і створює системний файл з дампом стану програми, щоб програмісти могли розібратися в причинах того, що сталося. Якщо це обмеження встановлено на 0, то системні файли не створюються. Якщо розмір системного файлу перевищує цю межу, він обрізається до вказаного розміру. |
| totalmem | Максимальний розмір пам'яті, доступний процесу, в байтах. |
| virtualmem | Максимальний розмір віртуальної пам'яті, доступної процесу, у байтах. |
| data | Максимальний розмір сегмента даних для процесу в байтах. |
| stack | Максимальний розмір стека процесу у байтах. |
| rss | Максимальна кількість віртуальних сторінок в оперативній пам'яті |
| maxproc | Максимальна кількість процесів, яка може бути створена для окремого дійсного ID користувача, що викликав процес. |
| memlock | Максимальний обсяг пам'яті в байтах, який може бути заблокований у RAM |
| cpu | Кількість процесорного часу доступного для використання в CPU. |
| filesize | Максимальний розмір сегмента даних для процесу в байтах. |
| openfiles | На один більше, ніж доступна максимальна кількість відкритих файлових дескрипторів. |

Функція повертає \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Додано необов'язковий параметр `resource` |

### Приклади

**Приклад #1 Приклад використання** posix\_getrlimit()\*\*\*\*

```php
<?php

$limits = posix_getrlimit();

print_r($limits);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [soft core] => 0
    [hard core] => unlimited
    [soft data] => unlimited
    [hard data] => unlimited
    [soft stack] => 8388608
    [hard stack] => unlimited
    [soft totalmem] => unlimited
    [hard totalmem] => unlimited
    [soft rss] => unlimited
    [hard rss] => unlimited
    [soft maxproc] => unlimited
    [hard maxproc] => unlimited
    [soft memlock] => unlimited
    [hard memlock] => unlimited
    [soft cpu] => unlimited
    [hard cpu] => unlimited
    [soft filesize] => unlimited
    [hard filesize] => unlimited
    [soft openfiles] => 1024
    [hard openfiles] => 1024
)
```

### Дивіться також

-   керівництво GETRLIMIT(2)
-   [posix\_setrlimit()](function.posix-setrlimit.md) \- встановлює межі системних ресурсів

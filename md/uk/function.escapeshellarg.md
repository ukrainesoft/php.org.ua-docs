---
navigation:
  - ref.exec.md: « Функції запуску програм
  - function.escapeshellcmd.md: escapeshellcmd »
  - index.md: PHP Manual
  - ref.exec.md: Функції запуску програм
title: escapeshellarg
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# escapeshellarg

(PHP 4 >= 4.0.3, PHP 5, PHP 7, PHP 8)

escapeshellarg — Екранувати рядок для того, щоб він міг бути використаний як аргумент командного рядка

### Опис

```methodsynopsis
escapeshellarg(string $arg): string
```

Функция**escapeshellarg()** додає одинарні лапки навколо рядка та лапок і екранує будь-які існуючі одинарні лапки, дозволяючи вам передати рядок безпосередньо у функцію оболонки та розглядати її як один безпечний аргумент. Ця функція повинна використовуватися для того, щоб екранувати окремі аргументи для функцій оболонки, отримані з введення користувача. Екранування аргументу необхідне у таких функціях оболонки як [exec()](function.exec.md) [system()](function.system.md)и оператор["зворотний апостроф"](language.operators.execution.md)

В Windows**escapeshellarg()** замінює знак оклику, знак відсотка (пізнє зв'язування змінних) і подвійні лапки на пробіли і додає подвійні лапки навколо рядка. Крім того, кожна серія послідовних зворотних слішів (`\`) екранується одним додатковим зворотним слішем.

### Список параметрів

`arg`

Аргумент, який буде екрановано.

### Значення, що повертаються

Екранований рядок.

### Приклади

**Приклад #1 Приклад використання** escapeshellarg()\*\*\*\*

```php
<?php
system('ls '.escapeshellarg($dir));
?>
```

### Дивіться також

-   [escapeshellcmd()](function.escapeshellcmd.md) \- Екранувати метасимволи командного рядка
-   [exec()](function.exec.md) \- Виконати зовнішню програму
-   [popen()](function.popen.md) \- Відкриває файловий покажчик процесу
-   [system()](function.system.md) \- Виконати зовнішню програму та відобразити висновок
-   [Оператор виконання](language.operators.execution.md)

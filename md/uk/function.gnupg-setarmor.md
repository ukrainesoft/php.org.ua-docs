---
navigation:
  - function.gnupg-listsignatures.md: « gnupg\_listsignatures
  - function.gnupg-seterrormode.md: gnupg\_seterrormode »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_setarmor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_setarmor

(PECL gnupg >= 0.1)

gnupg\_setarmor — Перемикає вивод у текстовому або бінарному режимі

### Опис

```methodsynopsis
gnupg_setarmor(resource $identifier, int $armor): bool
```

Перемикає висновок у текстовому або бінарному режимі.

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`armor`

У разі ненульового цілого числа, функція включає текстовий режим виводу (за умовчанням). У разі 0 виведення в бінарному режимі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** gnupg\_setarmor()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
gnupg_setarmor($res,1); // текстовый режим вывода;
gnupg_setarmor($res,0); // бинарный режим вывода;
?>
```

**Приклад #2 Приклад використання** gnupg\_setarmor()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg();
$gpg->setarmor(1); // текстовый режим вывода;
$gpg->setarmor(0); // бинарный режим вывода;
?>
```

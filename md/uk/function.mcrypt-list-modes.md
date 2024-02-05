---
navigation:
  - function.mcrypt-list-algorithms.md: « mcrypt\_list\_algorithms
  - function.mcrypt-module-close.md: mcrypt\_module\_close »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_list\_modes
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_list\_modes

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_list\_modes — Отримати список усіх підтримуваних режимів шифрування

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_list_modes(string $lib_dir = ini_get("mcrypt.modes_dir")): array
```

Отримати список усіх режимів шифрування з директорії `lib_dir`

### Список параметрів

`lib_dir`

Вказує директорію, де розташовані режими. Якщо не встановлено, то буде використано значення директиви `mcrypt.modes_dir`из php.ini.

### Значення, що повертаються

Повертає масив підтримуваних режимів.

### Приклади

**Приклад #1 Приклад використання** mcrypt\_list\_modes()\*\*\*\*

```php
<?php
    $modes = mcrypt_list_modes();

    foreach ($modes as $mode) {
        echo "$mode <br />\n";
    }
?>
```

Приклад вище демонструє отримання списку всіх алгоритмів директорії за замовчуванням. Якщо директива php.ini `mcrypt.modes_dir`не задана, то будет использована директория mcrypt по умолчанию (/usr/local/lib/libmcrypt).

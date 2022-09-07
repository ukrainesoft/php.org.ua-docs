---
navigation:
  - class.rarentry.md: « RarEntry
  - rarentry.getattr.md: 'RarEntry::getAttr »'
  - index.md: PHP Manual
  - class.rarentry.md: RarEntry
title: 'RarEntry::extract'
---
# RarEntry::extract

(PECL rar >= 0.1)

RarEntry::extract — Витягує елемент з архіву

### Опис

```methodsynopsis
public RarEntry::extract(    string $dir,    string $filepath = "",    string $password = NULL,    bool $extended_data = false): bool
```

**RarEntry::extract()** витягує вміст елемента. При цьому створюється новий файл у зазначеній директорії `dir` з ім'ям, що збігається з ім'ям елемента, якщо тільки не заданий другий аргумент. Дивіться нижче.

### Список параметрів

`dir`

Шлях до директорії, куди потрібно витягти файли. Цей параметр враховується лише якщо не вказано `filepath`. Якщо обидва параметри не вказані, файли витягуються в поточну директорію.

`filepath`

Шлях (повний або відносний) містить директорію та ім'я файлу, що видобувається. Цей параметр перевизначає параметр `dir` та оригінальне ім'я файлу.

`password`

Пароль використовується для шифрування поточного елемента. Якщо елемент не зашифрований, цей параметр не буде використаний і його можна не вказувати. Якщо цей параметр не вказано, а елемент зашифрований, то буде використаний пароль, переданий функції [raropen()](rararchive.open.md), Якщо її викликали. Якщо передано невірний пароль, явно чи неявно через [raropen()](rararchive.open.md), то перевірка CRC буде невдалою і буде повернуто **`false`**. Ви можете перевірити, чи є елемент зашифрованим за допомогою [RarEntry::isEncrypted()](rarentry.isencrypted.md)

`extended_data`

Якщо **`true`**, то до файлу буде додано додаткову інформацію, таку як NTFS ACL і власник у системі Unix, якщо вони були присутні в архіві.

**Увага**

До версії 2.0.0 не обробляла відносні шляхи коректно. Використовуйте для цієї ситуації [realpath()](function.realpath.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| PECL rar 3.0.0 | Було додано параметр `extended_data` |
| PECL rar 3.0.0 | Виправлена ​​підтримка RAR архівів з іменами елементів, що повторюються. |

### Приклади

**Приклад #1 Приклад використання **RarEntry::extract()****

```php
<?php

$rar_file = rar_open('example.rar') or die("Не удалось открыть Rar архив");

$entry = rar_entry_get($rar_file, 'Dir/file.txt') or die("Не удалось найти такую запись");

$entry->extract('/dir/to'); // создание /dir/to/Dir/file.txt
$entry->extract(false, '/dir/to/new_name.txt'); // создание /dir/to/new_name.txt

?>
```

**Приклад #2 Як отримати всі файли з архіву:**

```php
<?php

/* Пример от Erik Jenssen aka erix */

$filename = "foobar.rar";
$filepath = "/home/foo/bar/";

$rar_file = rar_open($filepath.$filename);
$list = rar_list($rar_file);
foreach($list as $file) {
    $entry = rar_entry_get($rar_file, $file);
    $entry->extract("."); // извлечь в текущий каталог
}
rar_close($rar_file);

?>
```

### Дивіться також

-   [RarEntry::getStream()](rarentry.getstream.md) - Отримати обробник для запису
-   [`rar://`wrapper](wrappers.rar.md)

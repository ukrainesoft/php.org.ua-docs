---
navigation:
  - function.xattr-set.md: « xattr\_set
  - book.xdiff.md: xdiff »
  - index.md: PHP Manual
  - ref.xattr.md: xattr Функції
title: xattr\_supported
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xattr\_supported

(PECL xattr >= 1.0.0)

xattr\_supported — Перевірка підтримки розширених атрибутів

### Опис

```methodsynopsis
xattr_supported(string $filename, int $flags = 0): bool
```

Ця функція перевіряє чи підтримує файлова система, що містить файл, розширені атрибути. Потрібне право читати файл.

### Список параметрів

`filename`

Шлях до файлу, що перевіряється.

`flags`

<table class="doctable table"><caption><strong>Підтримувані xattr-прапори</strong></caption><tbody class="tbody"><tr><td><strong><code>XATTR_DONTFOLLOW</code></strong></td><td>Не розіменовувати символічні посилання, працювати з самим посиланням.</td></tr></tbody></table>

### Значення, що повертаються

Функція повертає **`true`**, якщо файлова система підтримує розширені атрибути, \*\*`false`\*\*якщо це не так і **`null`**, якщо неможливо визначити (наприклад неправильний шлях до файлу, або немає дозволу на читання файлу).

### Приклади

**Пример #1**xattr\_supported()**example**

Перевірте, чи можна використовувати розширені атрибути.

```php
<?php
$file = 'some_file';

if (xattr_supported($file)) {
    /* ... make use of some xattr_* functions ... */
}

?>
```

### Дивіться також

-   [xattr\_get()](function.xattr-get.md) \- Отримання розширених атрибутів файлу
-   [xattr\_list()](function.xattr-list.md) \- Перегляд списку розширених атрибутів файлу

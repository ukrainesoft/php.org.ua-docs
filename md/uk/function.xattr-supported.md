Перевірка підтримки розширених атрибутів

-   [« xattr\_set](function.xattr-set.html)
    
-   [xdiff »](book.xdiff.html)
    
-   [PHP Manual](index.html)
    
-   [xattr Функции](ref.xattr.html)
    
-   Перевірка підтримки розширених атрибутів
    

# xattrsupported

(PECL xattr >= 1.0.0)

xattrsupported — Перевірка підтримки розширених атрибутів

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

Функція повертає **`true`**, якщо файлова система підтримує розширені атрибути, **`false`**якщо це не так і **`null`**, якщо неможливо визначити (наприклад неправильний шлях до файлу, чи немає дозволу на читання файлу).

### Приклади

**Приклад #1 **xattrsupported()** example**

Перевірте, чи можна використовувати розширені атрибути.

```php
<?php
$file = 'some_file';

if (xattr_supported($file)) {
    /* ... make use of some xattr_* functions ... */
}

?>
```

### Дивіться також

-   [xattr\_get()](function.xattr-get.html) - Отримання розширених атрибутів файлу
-   [xattr\_list()](function.xattr-list.html) - Перегляд списку розширених атрибутів файлу
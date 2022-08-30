Видалення розширених атрибутів файлу

-   [« xattrlist](function.xattr-list.html)
    
-   [xattrset »](function.xattr-set.html)
    
-   [PHP Manual](index.html)
    
-   [xattr Функции](ref.xattr.html)
    
-   Видалення розширених атрибутів файлу
    

# xattrremove

(PECL xattr >= 0.9.0)

xattrremove — Видалення розширених атрибутів файлу

### Опис

```methodsynopsis
xattr_remove(string $filename, string $name, int $flags = 0): bool
```

Ця функція видаляє розширений атрибут файлу.

Розширені атрибути мають два різних простори імен: користувальницьке та кореневе (root). Користувальницький простір імен доступний для всіх користувачів, в той час як кореневе - тільки для користувачів з root-привілеями. За умовчанням xattr оперує в просторі імен, але ви можете змінити цю поведінку за допомогою аргументу `flags`

### Список параметрів

`filename`

Файл, атрибут якого потрібно видалити.

`name`

Ім'я атрибута, що видаляється.

`flags`

<table class="doctable table"><caption><strong>Підтримувані xattr-прапори</strong></caption><tbody class="tbody"><tr><td><strong><code>XATTR_DONTFOLLOW</code></strong></td><td>Не розіменовувати символічні посилання, працювати з самим посиланням.</td></tr><tr><td><strong><code>XATTR_ROOT</code></strong></td><td>Встановити атрибут у кореневому просторі імен. Потрібні права суперкористувача.</td></tr></tbody></table>

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Видалити всі розширені атрибути файлу**

```php
<?php
$file = 'some_file';
$attributes = xattr_list($file);

foreach ($attributes as $attr_name) {
    xattr_remove($file, $attr_name);
}
?>
```

### Дивіться також

-   [xattrlist()](function.xattr-list.html) - Перегляд списку розширених атрибутів файлу
-   [xattrset()](function.xattr-set.html) - Встановлення розширених атрибутів файлу
-   [xattrget()](function.xattr-get.html) - Отримання розширених атрибутів файлу
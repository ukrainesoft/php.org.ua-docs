Перегляд списку розширених атрибутів файлу

-   [« xattrget](function.xattr-get.html)
    
-   [xattrremove »](function.xattr-remove.html)
    
-   [PHP Manual](index.md)
    
-   [xattr Функции](ref.xattr.md)
    
-   Перегляд списку розширених атрибутів файлу
    

# xattrlist

(PECL xattr >= 0.9.0)

xattrlist — Перегляд списку розширених атрибутів файлу

### Опис

```methodsynopsis
xattr_list(string $filename, int $flags = 0): array
```

Ця функція повертає список імен розширених атрибутів файлу.

Розширені атрибути мають два різні простори імен: користувальницьке та кореневе (root). Користувальницький простір імен доступний для всіх користувачів, в той час як кореневе - тільки для користувачів з root-привілеями. За умовчанням xattr оперує в просторі імен, але ви можете змінити цю поведінку за допомогою аргументу `flags`

### Список параметрів

`filename`

Файл, список атрибутів якого потрібно прочитати.

`flags`

<table class="doctable table"><caption><strong>Підтримувані xattr-прапори</strong></caption><tbody class="tbody"><tr><td><strong><code>XATTR_DONTFOLLOW</code></strong></td><td>Не розіменовувати символічні посилання, працювати з самим посиланням.</td></tr><tr><td><strong><code>XATTR_ROOT</code></strong></td><td>Встановити атрибут у кореневому просторі імен. Потрібні права суперкористувача.</td></tr></tbody></table>

### Значення, що повертаються

Функція повертає масив, що містить імена розширених атрибутів.

### Приклади

**Приклад #1 Вивести імена всіх розширених атрибутів файлу**

```php
<?php
$file = 'some_file';
$root_attributes = xattr_list($file, XATTR_ROOT);
$user_attributes = xattr_list($file);

echo "Root-атрибуты: \n";
foreach ($root_attributes as $attr_name) {
    printf("%s\n", $attr_name);
}

echo "\n Пользовательские атрибуты: \n";
foreach ($attributes as $attr_name) {
    printf("%s\n", $attr_name);
}

?>
```

### Дивіться також

-   [xattrget()](function.xattr-get.html) - Отримання розширених атрибутів файлу
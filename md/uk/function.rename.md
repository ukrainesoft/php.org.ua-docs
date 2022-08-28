Перейменовує файл або директорію

-   [« realpath](function.realpath.html)
    
-   [rewind »](function.rewind.html)
    
-   [PHP Manual](index.html)
    
-   [Функции файловой системы](ref.filesystem.html)
    
-   Перейменовує файл або директорію
    

# rename

(PHP 4, PHP 5, PHP 7, PHP 8)

rename — Перейменує файл або директорію

### Опис

```methodsynopsis
rename(string $from, string $to, ?resource $context = null): bool
```

Намагається перейменувати `from` в `to`, переносячи файл між директоріями, якщо потрібно. Якщо `to` існує, він буде перезаписаний. При перейменуванні директорії з існуючим `to` буде виведено попередження.

### Список параметрів

`from`

Старе ім'я.

> **Зауваження**
> 
> Обгортка, що використовується в `from` *повинна* збігатися з обгорткою, що використовується в `to`

`to`

Нове ім'я

> **Зауваження**: У Windows, якщо `to` вже існує, він має бути доступним для запису. В іншому випадку **rename()** завершиться помилкою та видасть **`E_WARNING`**

`context`

Ресурс (resource) з [контекстом потока](stream.contexts.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання функції **rename()****

```php
<?php
rename("/tmp/tmp_file.txt", "/home/user/login/docs/my_file.txt");
?>
```

### Дивіться також

-   [copy()](function.copy.html) - Копіює файл
-   [unlink()](function.unlink.html) - Видаляє файл
-   [move\_uploaded\_file()](function.move-uploaded-file.html) - Переміщує завантажений файл у нове місце
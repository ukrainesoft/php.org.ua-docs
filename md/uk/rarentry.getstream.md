Отримати обробник для запису

-   [« RarEntry::getPackedSize](rarentry.getpackedsize.html)
    
-   [RarEntry::getUnpackedSize »](rarentry.getunpackedsize.html)
    
-   [PHP Manual](index.html)
    
-   [RarEntry](class.rarentry.html)
    
-   Отримати обробник для запису
    

# RarEntry::getStream

(PECL rar >= 2.0.0)

RarEntry::getStream — Отримати обробник для запису

### Опис

```methodsynopsis
public RarEntry::getStream(string $password = ?): resource|false
```

Повертає оброблювач, який підтримує операцію читання. Цей оброблювач вміє розпаковувати запис на льоту.

Обробник не знищується під час виклику [rar\_close()](rararchive.close.html)

**Увага**

Результуючий потік не перевіряється цілісність. Отже, ніяк не визначається псування файлу або розшифровка з невірним ключем. Перевірка контрольної суми розтисненого та розшифрованого файлу повністю на совісті розробника.

### Список параметрів

`password`

Пароль, який використовується для шифрування запису. Якщо запис не шифрований, цей параметр ігнорується і може бути опущений. Якщо ж параметр опущений, а запис шифрований, буде використано пароль заданий у функції [rar\_open()](rararchive.open.html)якщо звичайно він був заданий. Якщо було встановлено неправильний пароль, явно чи неявно через [rar\_open()](rararchive.open.html), цей метод поверне потік із невірними даними. Якщо пароль не заданий взагалі, а він потрібен, то метод поверне **`false`**. Зашифрований запис чи ні можна перевірити за допомогою [RarEntry::isEncrypted()](rarentry.isencrypted.html)

### Значення, що повертаються

Обробник або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| PECL rar 3.0.0 | Підтримка RAR-архівів з іменами записів, що дублюються, тепер працює нормально. |

### Приклади

**Приклад #1 Приклад використання **RarEntry::getStream()****

```php
<?php

$rar_file = rar_open('example.rar');
if ($rar_file === false)
    die("Не удалось открыть Rar архив");

$entry = rar_entry_get($rar_file, 'Dir/file.txt');
if ($entry === false)
    die("Не удалось найти такую запись");

$stream = $entry->getStream();
if ($stream === false)
    die("Не удалось получить поток.");

rar_close($rar_file); //поток не зависит от файла

while (!feof($stream)) {
    $buff = fread($stream, 8192);
    if ($buff !== false)
        echo $buff;
    else
        break; //ошибка fread
}

fclose($stream);

?>
```

### Дивіться також

-   [RarEntry::extract()](rarentry.extract.html) - Витягує елемент із архіву
-   [обёртка `rar://`](wrappers.rar.html)
---
navigation:
  - function.finfo-file.md: « finfo\_file
  - function.finfo-set-flags.md: finfo\_set\_flags »
  - index.md: PHP Manual
  - ref.fileinfo.md: Функції модуля Fileinfo
title: finfo\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# finfo\_open

# finfo::\_\_construct

(PHP >= 5.3.0, PHP 7, PHP 8, PECL fileinfo >= 0.1.0)

finfo\_open -- finfo::\_\_construct - Створює екземпляр finfo

### Опис

Процедурний стиль

```methodsynopsis
finfo_open(int $flags = FILEINFO_NONE, ?string $magic_database = null): finfo|false
```

Об'єктно-орієнтований стиль (конструктор):

public[finfo::\_\_construct](finfo.construct.md)(int`$flags` **`FILEINFO_NONE`**, ?string`$magic_database` **`null`**) .

Ця функція відкриває магічну базу даних та повертає екземпляр.

### Список параметрів

`flags`

Одна або кілька об'єднаних через бінарне АБО [констант Fileinfo](fileinfo.constants.md)

`magic_database`

Ім'я файлу магічної бази даних, зазвичай щось на кшталт цього: /path/to/magic.mime. Якщо не вказано повний шлях, буде використано змінне оточення `MAGIC`. Якщо змінна оточення не вказана, то використовуватиметься вбудована в PHP магічна база даних.

Передача\*\*`null`\*\* або порожній рядок еквівалентно значенням за промовчанням.

### Значення, що повертаються

(Тільки процедурний стиль) Повертає екземпляр [finfo](class.finfo.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Повертає екземпляр [finfo](class.finfo.md); раніше повертався ресурс ([resource](language.types.resource.md) |
| 8.0.3 | `magic_database` тепер допускає значення null. |

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$finfo = new finfo(FILEINFO_MIME, "/usr/share/misc/magic"); // возвращает mime-тип а-ля mimetype расширения

/* получить mime-type для указанного файла */
$filename = "/usr/local/something.txt";
echo $finfo->file($filename);

?>
```

**Приклад #2 Процедурний стиль**

```php
<?php
$finfo = finfo_open(FILEINFO_MIME, "/usr/share/misc/magic"); // возвращает mime-тип а-ля mimetype расширения

if (!$finfo) {
    echo "Открытие базы данных fileinfo не удалось";
    exit();
}

/* получить mime-type для указанного файла */
$filename = "/usr/local/something.txt";
echo finfo_file($finfo, $filename);

/* закрыть соединение */
finfo_close($finfo);
?>
```

Результат виконання наведеного прикладу:

```
text/plain; charset=us-ascii
```

### Примітки

> **Зауваження** :
> 
> Зазвичай використання вбудованої магічної бази даних (при невстановлених `magic_database`и`MAGIC`) найкращий вибір, якщо вам не потрібна певна версія магічної бази даних.

### Дивіться також

-   [finfo\_close()](function.finfo-close.md) \- Закриває екземпляр finfo

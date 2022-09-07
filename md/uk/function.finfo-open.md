---
navigation:
  - function.finfo-file.md: « finfofile
  - function.finfo-set-flags.md: finfosetflags »
  - index.md: PHP Manual
  - ref.fileinfo.md: Функции модуля Fileinfo
title: finfoopen
---
# finfoopen

# finfo::construct

(PHP >= 5.3.0, PHP 7, PHP 8, PECL fileinfo >= 0.1.0)

finfoopen -- finfo::construct - Створює екземпляр finfo

### Опис

Процедурний стиль

```methodsynopsis
finfo_open(int $flags = FILEINFO_NONE, ?string $magic_database = null): finfo|false
```

Об'єктно-орієнтований стиль (конструктор):

public [finfo::construct](finfo.construct.md)(int `$flags` **`FILEINFO_NONE`**, ?string `$magic_database` **`null`**

Ця функція відкриває магічну базу даних та повертає екземпляр.

### Список параметрів

`flags`

Одна або кілька об'єднаних через бінарне АБО [констант Fileinfo](fileinfo.constants.md)

`magic_database`

Ім'я файлу магічної бази даних, зазвичай щось на кшталт цього: /path/to/magic.mime. Якщо не вказано повний шлях, буде використано змінне оточення `MAGIC`. Якщо змінна оточення не вказана, використовуватиметься вбудована в PHP магічна база даних.

Передача **`null`** або порожній рядок еквівалентно значенням за промовчанням.

### Значення, що повертаються

(Тільки процедурний стиль) Повертає екземпляр [finfo](class.finfo.md) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Повертає екземпляр [finfo](class.finfo.md); раніше повертався ресурс ([resource](language.types.resource.md) |
|  | `magic_database` тепер допускає значення null. |

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

Результат виконання цього прикладу:

```
text/plain; charset=us-ascii
```

### Примітки

> **Зауваження**
> 
> Зазвичай використання вбудованої магічної бази даних (при невстановлених `magic_database` і `MAGIC`) найкращий вибір, якщо вам не потрібна певна версія магічної бази даних.

### Дивіться також

-   [finfoclose()](function.finfo-close.md) - Закриває екземпляр finfo

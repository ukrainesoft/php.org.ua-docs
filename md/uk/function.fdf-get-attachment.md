Виймає завантажений файл, вбудований у FDF

-   [« fdfgetап](function.fdf-get-ap.html)
    
-   [fdfgetencoding »](function.fdf-get-encoding.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Виймає завантажений файл, вбудований у FDF
    

# fdfgetattachment

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdfgetattachment — Витягує завантажений файл, вбудований у FDF

### Опис

```methodsynopsis
fdf_get_attachment(resource $fdf_document, string $fieldname, string $savepath): array
```

Виймає файл, завантажений за допомогою поля "Вибір файлу" `fieldname`, і зберігає його в `savepath`

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) або [fdfopenstring()](function.fdf-open-string.html)

`fieldname`

`savepath`

Можливо, це ім'я простого файлу або існуючого каталогу, в якому файл має бути створений під його вихідним ім'ям. Будь-який існуючий файл з таким самим ім'ям буде перезаписано.

> **Зауваження**
> 
> Здається, немає іншого способу дізнатися вихідне ім'я файлу, крім як зберегти файл, використовуючи каталог як `savepath` та перевірити базове ім'я, під яким його було збережено.

### Значення, що повертаються

Повернутий масив містить такі поля:

-   `path` - шлях, де зберігається файл
-   `size` - розмір файлу, що зберігається в байтах
-   `type` - mimetype, якщо він вказаний у FDF

### Приклади

**Приклад #1 Збереження завантаженого файлу**

```php
<?php
  $fdf = fdf_open_string($HTTP_FDF_DATA);
  $data = fdf_get_attachment($fdf, "filename", "/tmpdir");
  echo "Загруженный файл хранится в $data[path]";
?>
```
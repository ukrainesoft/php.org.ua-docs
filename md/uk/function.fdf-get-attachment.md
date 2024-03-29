---
navigation:
  - function.fdf-get-ap.md: « fdf\_get\_ap
  - function.fdf-get-encoding.md: fdf\_get\_encoding »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_get\_attachment
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_get\_attachment

(PHP 4 >= 4.3.0, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_get\_attachment — Витягує завантажений файл, вбудований у FDF

### Опис

```methodsynopsis
fdf_get_attachment(resource $fdf_document, string $fieldname, string $savepath): array
```

Виймає файл, завантажений за допомогою поля "Вибір файлу" `fieldname`, і зберігає його в `savepath`

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md) або [fdf\_open\_string()](function.fdf-open-string.md)

`fieldname`

`savepath`

Можливо, це ім'я простого файлу або існуючого каталогу, в якому файл має бути створений під його вихідним ім'ям. Будь-який існуючий файл з таким самим ім'ям буде перезаписано.

> **Зауваження** :
> 
> Здається, немає іншого способу дізнатися вихідне ім'я файлу, крім як зберегти файл, використовуючи каталог як `savepath` та перевірити базове ім'я, під яким його було збережено.

### Значення, що повертаються

Повернутий масив містить такі поля:

-   `path`\- шлях, де зберігається файл
-   `size`\- розмір файлу, що зберігається в байтах
-   `type`\- mimetype, якщо він вказаний у FDF

### Приклади

**Приклад #1 Збереження завантаженого файлу**

```php
<?php
  $fdf = fdf_open_string($HTTP_FDF_DATA);
  $data = fdf_get_attachment($fdf, "filename", "/tmpdir");
  echo "Загруженный файл хранится в $data[path]";
?>
```

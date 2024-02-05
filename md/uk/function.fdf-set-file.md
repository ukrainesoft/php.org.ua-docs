---
navigation:
  - function.fdf-set-encoding.md: « fdf\_set\_encoding
  - function.fdf-set-flags.md: fdf\_set\_flags »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_set\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_set\_file

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_set\_file — Встановлює PDF-документ для відображення даних FDF

### Опис

```methodsynopsis
fdf_set_file(resource $fdf_document, string $url, string $target_frame = ?): bool
```

Вибирає інший PDF-файл для відображення результатів форми у формі, з якої він був створений.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md)or[fdf\_open\_string()](function.fdf-open-string.md)

`url`

Повинна бути вказана абсолютна URL-адреса.

`target_frame`

Використовуйте цей параметр, щоб вказати кадр, у якому буде відображено документ. Ви також можете встановити значення за промовчанням для цього параметра за допомогою [fdf\_set\_target\_frame()](function.fdf-set-target-frame.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Передача даних FDF у другу форму**

```php
<?php
  /* Установка типа содержимого для Adobe FDF */
  fdf_header();

  /* Создание нового fdf */
  $fdf = fdf_create();

  /* Установка значения "bar" в поле "foo" */
  fdf_set_value($fdf, "foo", "bar");

  /* сообщение клиенту, что нужно отображать данные FDF, используя "fdf_form.pdf" */
  fdf_set_file($fdf, "http://www.example.com/fdf_form.pdf");

  /* вывод fdf */
  fdf_save($fdf);

  /* закрытие */
  fdf_close($fdf);
?>
```

### Дивіться також

-   [fdf\_get\_file()](function.fdf-get-file.md) \- Отримує значення ключа /F
-   [fdf\_set\_target\_frame()](function.fdf-set-target-frame.md) \- Встановлює цільовий кадр для відображення форми

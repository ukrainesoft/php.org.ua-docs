---
navigation:
  - function.fdf-set-encoding.md: « fdfsetencoding
  - function.fdf-set-flags.md: fdfsetflags »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfsetfile
---
# fdfsetfile

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfsetfile — Встановлює PDF-документ для відображення даних FDF

### Опис

```methodsynopsis
fdf_set_file(resource $fdf_document, string $url, string $target_frame = ?): bool
```

Вибирає інший PDF-файл для відображення результатів форми в тій формі, з якої він був створений.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.md) [fdfopen()](function.fdf-open.md) ор [fdfopenstring()](function.fdf-open-string.md)

`url`

Повинна бути вказана абсолютна URL-адреса.

`target_frame`

Використовуйте цей параметр, щоб вказати кадр, у якому буде відображено документ. Ви також можете встановити значення за промовчанням для цього параметра за допомогою [fdfsettargetframe()](function.fdf-set-target-frame.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

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

-   [fdfgetfile()](function.fdf-get-file.md) - Отримує значення ключа /F
-   [fdfsettargetframe()](function.fdf-set-target-frame.md) - Встановлює цільовий кадр для відображення форми

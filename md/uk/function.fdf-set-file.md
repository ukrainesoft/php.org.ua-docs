Встановлює PDF-документ для відображення даних FDF

-   [« fdf\_set\_encoding](function.fdf-set-encoding.html)
    
-   [fdf\_set\_flags »](function.fdf-set-flags.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Встановлює PDF-документ для відображення даних FDF
    

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

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.html) [fdf\_open()](function.fdf-open.html) ор [fdf\_open\_string()](function.fdf-open-string.html)

`url`

Повинна бути вказана абсолютна URL-адреса.

`target_frame`

Використовуйте цей параметр, щоб вказати кадр, у якому буде відображено документ. Ви також можете встановити значення за промовчанням для цього параметра за допомогою [fdf\_set\_target\_frame()](function.fdf-set-target-frame.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Передача даних FDF у другу форму**

```php
<?php
  /* Установка типа содержимого для Adobe FDF */
  fdf_header();

  /* Создание нового fdf */
  $fdf = fdf_create();

  /* Установка значения "bar" в поле "foo" */
  fdf_set_value($fdf, "foo", "bar");

  /* сообщение клиенту, что нужно отображать данные FDF, используя "fdf_form.pdf" */
  fdf_set_file($fdf, "http://www.example.com/fdf_form.pdf");

  /* вывод fdf */
  fdf_save($fdf);

  /* закрытие */
  fdf_close($fdf);
?>
```

### Дивіться також

-   [fdf\_get\_file()](function.fdf-get-file.html) - Отримує значення ключа /F
-   [fdf\_set\_target\_frame()](function.fdf-set-target-frame.html) - Встановлює цільовий кадр для відображення форми
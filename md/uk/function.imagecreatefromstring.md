---
navigation:
  - function.imagecreatefrompng.html: « imagecreatefrompng
  - function.imagecreatefromtga.html: imagecreatefromtga »
  - index.html: PHP Manual
  - ref.image.html: Функції GD та функції для роботи із зображеннями
title: imagecreatefromstring
---
# imagecreatefromstring

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

imagecreatefromstring — Створення нового зображення з потоку, представленого рядком

### Опис

```methodsynopsis
imagecreatefromstring(string $data): GdImage|false
```

**imagecreatefromstring()** повертає ідентифікатор зображення, що представляє зображення, отримане з потоку `data`. Ці типи будуть автоматично визначатися, якщо збірка PHP їх підтримує: JPEG, PNG, GIF, BMP, WBMP, GD2 та WEBP.

### Список параметрів

`data`

Рядок містить дані зображення.

### Значення, що повертаються

У разі успішного виконання буде повернуто об'єкт ресурсу, **`false`**, якщо тип зображення не підтримується, дані не розпізнаються або дані порушені та не можуть бути завантажені.

### Помилки

**imagecreatefromstring()** викликає помилку рівня EWARNING, якщо дані не підтримуються.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.html); раніше повертався ресурс (resource). |
|  | Додана підтримка WEBP (якщо підтримується libgd). |

### Приклади

**Приклад #1 Приклад використання **imagecreatefromstring()****

```php
<?php
$data = 'iVBORw0KGgoAAAANSUhEUgAAABwAAAASCAMAAAB/2U7WAAAABl'
       . 'BMVEUAAAD///+l2Z/dAAAASUlEQVR4XqWQUQoAIAxC2/0vXZDr'
       . 'EX4IJTRkb7lobNUStXsB0jIXIAMSsQnWlsV+wULF4Avk9fLq2r'
       . '8a5HSE35Q3eO2XP1A1wQkZSgETvDtKdQAAAABJRU5ErkJggg==';
$data = base64_decode($data);

$im = imagecreatefromstring($data);
if ($im !== false) {
    header('Content-Type: image/png');
    imagepng($im);
    imagedestroy($im);
}
else {
    echo 'Произошла ошибка.';
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagecreatefromstring()](images/21009b70229598c6a80eef8b45bf282b-imagecreatefromstring.png)

### Дивіться також

-   [imagecreatefromjpeg()](function.imagecreatefromjpeg.html) - Створює нове зображення з файлу чи URL
-   [imagecreatefrompng()](function.imagecreatefrompng.html) - Створює нове зображення з файлу чи URL
-   [imagecreatefromgif()](function.imagecreatefromgif.html) - Створює нове зображення з файлу чи URL
-   [imagecreatetruecolor()](function.imagecreatetruecolor.html) - Створення нового повнокольорового зображення

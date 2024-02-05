---
navigation:
  - function.imagecreatefrompng.md: « imagecreatefrompng
  - function.imagecreatefromtga.md: imagecreatefromtga »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromstring
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecreatefromstring

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

imagecreatefromstring — Створення нового зображення з потоку, представленого рядком

### Опис

```methodsynopsis
imagecreatefromstring(string $data): GdImage|false
```

\*\*imagecreatefromstring()\*\*возвращает идентификатор изображения, представляющего изображение полученное из потока`data`. Ці типи будуть автоматично визначатися, якщо збірка PHP їх підтримує: JPEG, PNG, GIF, BMP, WBMP, GD2 та WEBP.

### Список параметрів

`data`

Рядок містить дані зображення.

### Значення, що повертаються

У разі успішного виконання буде повернуто об'єкт ресурсу, **`false`**, якщо тип зображення не підтримується, дані не розпізнаються або дані порушені та не можуть бути завантажені.

### Помилки

**imagecreatefromstring()** викликає помилку рівня E\_WARNING, якщо дані не підтримуються.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |
| 7.3.0 | Додана підтримка WEBP (якщо підтримується libgd). |

### Приклади

**Пример #1 Пример использования**imagecreatefromstring()\*\*\*\*

```php
<?php
$data = 'iVBORw0KGgoAAAANSUhEUgAAABwAAAASCAMAAAB/2U7WAAAABl'
       . 'BMVEUAAAD///+l2Z/dAAAASUlEQVR4XqWQUQoAIAxC2/0vXZDr'
       . 'EX4IJTRkb7lobNUStXsB0jIXIAMSsQnWlsV+wULF4Avk9fLq2r'
       . '8a5HSE35Q3eO2XP1A1wQkZSgETvDtKdQAAAABJRU5ErkJggg==';
$data = base64_decode($data);

$im = imagecreatefromstring($data);
if ($im !== false) {
    header('Content-Type: image/png');
    imagepng($im);
    imagedestroy($im);
}
else {
    echo 'Произошла ошибка.';
}
?>
```

Висновок наведеного прикладу буде схожим на:

![Висновок прикладу: imagecreatefromstring()](images/21009b70229598c6a80eef8b45bf282b-imagecreatefromstring.png)

### Дивіться також

-   [imagecreatefromjpeg()](function.imagecreatefromjpeg.md) \- Створює нове зображення з файлу чи URL
-   [imagecreatefrompng()](function.imagecreatefrompng.md) \- Створює нове зображення з файлу чи URL
-   [imagecreatefromgif()](function.imagecreatefromgif.md) \- Створює нове зображення з файлу чи URL
-   [imagecreatetruecolor()](function.imagecreatetruecolor.md) \- Створення нового повнокольорового зображення

---
navigation:
  - imagick.adaptiveblurimage.md: '« Imagick::adaptiveBlurImage'
  - imagick.adaptivesharpenimage.md: 'Imagick::adaptiveSharpenImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::adaptiveResizeImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::adaptiveResizeImage

(PECL imagick 2, PECL imagick 3)

Imagick::adaptiveResizeImage — Адаптивна зміна розміру зображення з даними тріангуляції

### Опис

```methodsynopsis
public Imagick::adaptiveResizeImage(    int $columns,    int $rows,    bool $bestfit = false,    bool $legacy = false): bool
```

Адаптивна зміна розміру зображення з даними тріангуляції. Дозволяє уникнути розмиття через різку зміну кольору. Найчастіше використовується зменшення зображень трохи менше " розміру для web " ; виходить погано, коли повнорозмірне зображення адаптивно змінюється мініатюру. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

> **Зауваження**: Поведение параметра`bestfit` було змінено у Imagick 3.0.0. До цієї версії при зміні зображення розміром 200 x 150 до 400 x 300 жодних операцій не відбувалося. В Imagick 3.0.0 і пізніших версіях зображення буде масштабовано до розміру 400 x 300, тому що найбільше відповідає ("best fit") даним розмірам. Якщо вказано параметр `bestfit`, то ширина та висота також повинні бути визначені.

### Список параметрів

`columns`

Кількість стовпців у масштабі зображення.

`rows`

Кількість рядків у масштабі зображення.

`bestfit`

Чи підганятиметься зображення всередині обмежувальної рамки.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL imagick 2.1.0 | Додано необов'язковий параметр припасування. |
| PECL imagick 2.1.0 | Метод тепер підтримує пропорційне масштабування. Для цього потрібно передати 0 одному з параметрів. |

### Приклади

**Пример #1 Пример использования**Imagick::adaptiveResizeImage()\*\*\*\*

Зміна розмірів зображення, що зазвичай використовуються в web. Цей метод найкраще працює при невеликій зміні розміру.

```php
<?php
header('Content-type: image/jpeg');

$image = new Imagick('image.jpg');
$image->adaptiveResizeImage(1024,768);

echo $image;
?>
```

### Дивіться також

-   [Imagick::chopImage()](imagick.chopimage.md) \- Видаляє область зображення та обрізає його
-   [Imagick::cropImage()](imagick.cropimage.md) \- Витягує область зображення
-   [Imagick::magnifyImage()](imagick.magnifyimage.md) \- Пропорційно масштабує зображення вдвічі
-   [Imagick::minifyImage()](imagick.minifyimage.md) \- Масштабує зображення пропорційно до половини його розміру
-   [Imagick::resizeImage()](imagick.resizeimage.md) \- Масштабує зображення
-   [Imagick::scaleImage()](imagick.scaleimage.md) \- Масштабує розмір зображення
-   [Imagick::shaveImage()](imagick.shaveimage.md) \- Видаляє пікселі по краях зображення
-   [Imagick::thumbnailImage()](imagick.thumbnailimage.md) \- Змінює розмір зображення
-   [Imagick::trimImage()](imagick.trimimage.md) \- Видаляє краї із зображення

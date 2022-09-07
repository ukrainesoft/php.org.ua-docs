---
navigation:
  - function.imagecopymergegray.md: « imagecopymergegray
  - function.imagecopyresized.md: imagecopyresized »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecopyresampled
---
# imagecopyresampled

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

imagecopyresampled — Копіювання та зміна розміру зображення з ресемплюванням

### Опис

```methodsynopsis
imagecopyresampled(    GdImage $dst_image,    GdImage $src_image,    int $dst_x,    int $dst_y,    int $src_x,    int $src_y,    int $dst_width,    int $dst_height,    int $src_width,    int $src_height): bool
```

**imagecopyresampled()** копіює прямокутну частину одного зображення на інше зображення, інтерпрелюючи значення пікселів таким чином, щоб зменшення розміру зображення не зменшувало його чіткості.

Іншими словами, **imagecopyresampled()** бере прямокутну ділянку з `src_image` із шириною `src_width` та заввишки `src_height` на координатах `src_x``src_y` і поміщає його у прямокутну ділянку зображення `dst_image` шириною `dst_width` та заввишки `dst_height` на координатах `dst_x``dst_y`

Якщо координати, ширина або висота вихідного та кінцевого зображень є різними, фрагмент, що копіюється, буде розтягнутий або стиснутий. Координати відраховуються від верхнього лівого кута зображення. Функцію можна використовувати для накладання ділянок на те саме зображення, з якого вони скопійовані (якщо `dst_image` має те саме значення, що і `src_image`), але якщо ділянки перетинатимуться, результат непередбачуваний.

### Список параметрів

`dst_image`

Ресурс цільового зображення.

`src_image`

Ресурс вихідного зображення.

`dst_x`

x-координата результуючого зображення.

`dst_y`

y-координата результуючого зображення.

`src_x`

x-координата вихідного зображення.

`src_y`

y-координата вихідного зображення.

`dst_width`

результуюча ширина.

`dst_height`

Результатова висота.

`src_width`

Ширина вихідного зображення.

`src_height`

Висота вихідного зображення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `dst_image` і `src_image` тепер чекають на екземпляр [GdImage](class.gdimage.md); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Простий приклад**

У цьому прикладі зображення буде стисло до половини вихідного розміру.

```php
<?php
// файл
$filename = 'test.jpg';
$percent = 0.5;

// тип содержимого
header('Content-Type: image/jpeg');

// получение новых размеров
list($width, $height) = getimagesize($filename);
$new_width = $width * $percent;
$new_height = $height * $percent;

// ресэмплирование
$image_p = imagecreatetruecolor($new_width, $new_height);
$image = imagecreatefromjpeg($filename);
imagecopyresampled($image_p, $image, 0, 0, 0, 0, $new_width, $new_height, $width, $height);

// вывод
imagejpeg($image_p, null, 100);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: Простий приклад](images/21009b70229598c6a80eef8b45bf282b-imagecopyresampled.jpg)

**Приклад #2 Ресемплювання зображення із збереженням пропорцій**

У цьому прикладі зображення буде стиснуто до 200 пікселів шириною або висотою, дивлячись що більше.

```php
<?php
// файл
$filename = 'test.jpg';

// задание максимальной ширины и высоты
$width = 200;
$height = 200;

// тип содержимого
header('Content-Type: image/jpeg');

// получение новых размеров
list($width_orig, $height_orig) = getimagesize($filename);

$ratio_orig = $width_orig/$height_orig;

if ($width/$height > $ratio_orig) {
   $width = $height*$ratio_orig;
} else {
   $height = $width/$ratio_orig;
}

// ресэмплирование
$image_p = imagecreatetruecolor($width, $height);
$image = imagecreatefromjpeg($filename);
imagecopyresampled($image_p, $image, 0, 0, 0, 0, $width, $height, $width_orig, $height_orig);

// вывод
imagejpeg($image_p, null, 100);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: Ресемплювання зображення із збереженням пропорцій](images/21009b70229598c6a80eef8b45bf282b-imagecopyresampled_2.jpg)

### Примітки

> **Зауваження**
> 
> Існує проблема, пов'язана з обмеженнями палітрових зображень (255+1 колір). Ресемплювання або фільтрація зображення потребує більше кольорів, ніж 255. Для розрахунку нового пікселя та його кольору використовується деяке наближення. У разі палітрових зображень ми намагаємося створити новий колір, а якщо це не вдається, ми вибираємо найближчий (теоретично) обчислений колір. Це не завжди візуально найближчий колір. Такий підхід може давати в результаті порожні (або візуально порожні) зображення. Для усунення цієї проблеми, будь ласка, використовуйте truecolor-зображення як результуючі, що створюються функцією [imagecreatetruecolor()](function.imagecreatetruecolor.md)

### Дивіться також

-   [imagecopyresized()](function.imagecopyresized.md) - Копіювання та зміна розміру частини зображення
-   [imagescale()](function.imagescale.md) - Масштабувати зображення за заданою шириною та висотою
-   [imagecrop()](function.imagecrop.md) - Обрізати зображення до заданого прямокутника

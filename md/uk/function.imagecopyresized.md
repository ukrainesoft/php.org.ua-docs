- [«imagecopyresampled](function.imagecopyresampled.md)
- [imagecreate »](function.imagecreate.md)

- [PHP Manual](index.md)
- [Функції GD та функції для роботи із зображеннями](ref.image.md)
- Копіювання та зміна розміру частини зображення

# imagecopyresized

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecopyresized — Копіювання та зміна розміру частини зображення

### Опис

**imagecopyresized**(
[GdImage](class.gdimage.md) `$dst_image`,
[GdImage](class.gdimage.md) `$src_image`,
int `$dst_x`,
int `$dst_y`,
int `$src_x`,
int `$src_y`,
int `$dst_width`,
int `$dst_height`,
int `$src_width`,
int `$src_height`
): bool

**imagecopyresized()** копіює прямокутну ділянку одного зображення
інше зображення. `dst_image` - результуюче зображення,
`src_image` – ідентифікатор вихідного зображення.

Іншими словами, **imagecopyresized()** бере прямокутну ділянку з
`src_image` з шириною `src_width` та висотою `src_height` на координатах
`src_x`, `src_y` і поміщає його у прямокутну область зображення
`dst_image` з шириною `dst_width` та висотою `dst_height` на координатах
`dst_x`, `dst_y`.

Якщо координати, ширина або висота вихідного та кінцевого зображень
різні, копіюваний фрагмент буде розтягнутий або стиснутий. Координати
відраховуються від верхнього лівого кута зображення. Функцію можна
використовувати для накладання ділянок на те саме зображення, з якого вони
скопійовані (якщо `dst_image` має те саме значення, що і `src_image`),
але якщо ділянки перетинатимуться, результат непередбачуваний.

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
Результатова ширина.

`dst_height`
Результатова висота.

`src_width`
Ширина вихідного зображення.

`src_height`
Висота вихідного зображення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                                              |
| ------ | ----------------------------------------------------------------------------------------------------------------- |
| 8.0.0  | dst_image і src_image тепер чекають на екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Зміна розміру зображення**

У цьому прикладі розмір зображення буде зменшено вдвічі.

` <?php//файл і новий розмір$filename = 'test.jpg';$percent = 0.5;// тип вмістheader('Content-Type: image/jpeg'); height) = getimagesize($filename);$newwidth = $width * $percent;$newheight = $height * $percent;// завантаження$thumb = imagecreatetruecolor($newwidth, $$ ;// зміна розміруimagecopyresized($thumb, $source, 0, 0, 0, 0, $newwidth, $newheight, $width, $height);// виведенняimagejpeg($thumb);?> `

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: Зміна розміру зображення](images/21009b70229598c6a80eef8b45bf282b-imagecopyresized.jpg)

Зображення буде відображено зі зменшеним розміром. Якщо необхідно
отримати зображення у найкращій якості, використовуйте функцію
[imagecopyresampled()](function.imagecopyresampled.md).

### Примітки

> **Примітка**:
>
> Існує проблема, пов'язана з обмеженнями палітрових зображень
> (255+1 колір). Ресемплювання або фільтрація зображення вимагає
> більше кольорів, ніж 255. Для розрахунку нового пікселя та його кольору
> застосовується деяке наближення. У разі палітрових зображень ми
> намагаємося створити новий колір, а якщо це не вдається, ми вибираємо
> найближчий (теоретично) обчислений колір. Це не завжди візуально
> найближчий колір. Такий підхід може давати в результаті порожні (або
> візуально порожні) зображення. Для усунення цієї проблеми,
> будь ласка, використовуйте truecolor-зображення як
> результуючих, що створюються функцією
> [imagecreatetruecolor()](function.imagecreatetruecolor.md).

### Дивіться також

- [imagecopyresampled()](function.imagecopyresampled.md) -
Копіювання та зміна розміру зображення з ресемплюванням
- [imagescale()](function.imagescale.md) - Масштабувати
зображення по заданій ширині та висоті
- [imagecrop()](function.imagecrop.md) - Обрізати зображення до
заданого прямокутника

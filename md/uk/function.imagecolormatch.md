- [«imagecolorexactalpha](function.imagecolorexactalpha.md)
- [imagecolorresolve »](function.imagecolorresolve.md)

- [PHP Manual](index.md)
- [Функції GD та функції для роботи із зображеннями](ref.image.md)
- Робить кольори палітрової версії зображення більш відповідними
truecolor версії

#imagecolormatch

(PHP 4 \>= 4.3.0, PHP 5, PHP 7, PHP 8)

imagecolormatch — Робить кольори палітрової версії зображення.
відповідними truecolor версії

### Опис

**imagecolormatch**([GdImage](class.gdimage.md) `$image1`,
[GdImage](class.gdimage.md) `$image2`): bool

Робить кольори палітрової версії зображення більш відповідними
truecolor версії.

### Список параметрів

`image1`
Об'єкт truecolor-зображення.

`image2`
Об'єкт палітрового зображення, що має той самий розмір, що і `image1`.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                                       |
| ------ | ---------------------------------------------------------------------------------------------------------- |
| 8.0.0  | image1 та image2 тепер очікують екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagecolormatch()****

` <?php// створення зображень$im1 = imagecreatefrompng('./gdlogo.png');$im2 = imagecreate(imagesx($im1), imagesy($im1));// Додамо кілька квітів в$ = Array();$colors[] = imagecolorallocate($im2, 255, 36, 74);$colors[] = imagecolorallocate($im2, 40, 0, 240);$colors[] = imagecololoca , 100, 255);$colors[] = imagecolorallocate($im2,84,63,44); ($im2);?> `

### Дивіться також

- [imagecreatetruecolor()](function.imagecreatetruecolor.md) -
Створення нового повнокольорового зображення

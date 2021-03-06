- [«imagegd2](function.imagegd2.md)
- [imagegetclip »](function.imagegetclip.md)

- [PHP Manual](index.md)
- [Функції GD та функції для роботи із зображеннями](ref.image.md)
- Виведення GD-зображення у браузер або файл

#imagegd

(PHP 4 \>= 4.0.7, PHP 5, PHP 7, PHP 8)

imagegd — Вивод GD-зображення у браузер або файл

### Опис

**imagegd**([GdImage](class.gdimage.md) `$image`, ?string `$file` =
**`null`**): bool

Висновок GD-зображення в `file`.

### Список параметрів

`image`
Об'єкт [GdImage](class.gdimage.md), який повертається однією з функцій
створення зображень, наприклад, такий як
[imagecreatetruecolor()](function.imagecreatetruecolor.md).

`file`
Шлях, або відкритий потоковий ресурс (який автоматично закривається
після завершення функції), щоб зберегти файл. Якщо не встановлено або
дорівнює **`null`**, зображення буде виведено в потік виведення у бінарному
вигляді.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

**Застереження**

Однак, якщо libgd не може вивести зображення, ця функція поверне
**`true`**.

### Список змін

| Версія | Опис                                                                                                          |
|--------|---------------------------------------------------------------------------------------------------------------|
| 8.0.3  | file тепер допускає значення null.                                                                            |
| 8.0.0  | image тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource).                  |
| 7.2.0  | Тепер **imagegd()** дозволяє зберігати зображення "truecolor". Раніше вони неявно перетворювалися на палітру. |

### Приклади

**Приклад #1 Висновок GD-зображення**

`<?php// Створюємо пусте зображення і додаємо текст$im = imagecreatetruecolor(120, 20);$text_color = imagecolorallocate($im, 233, 14, 91)   Simple Text String", $text_color);// Виводимо зображенняimagegd($im);// Звільняємо пам'ятьimagedestroy($im);?> `

**Приклад #2 Збереження GD-зображення**

`<?php// Створюємо пусте зображення і додаємо текст$im = imagecreatetruecolor(120, 20);$text_color = imagecolorallocate($im, 233, 14, 91)   Simple Text String", $text_color);// Зберігаємо GD-зображення// Розширенням GD-зображень є .gd, детальніше на http://www.libgd.org/GdFileFormatsimagegd($im, '; / Звільняємо пам'ятьimagedestroy($im);?> `

### Примітки

> **Примітка**:
>
> Формат GD зазвичай використовується для швидкого завантаження деталей
> Зображення. Зауважимо, що формат GD використовується тільки в
> GD-сумісні програми.

**Увага**

Формати зображень GD та GD2 є пропрієтарними форматами
зображень libgd. Вони повинні розглядатися як застарілі і повинні
використовуватися тільки з метою розробки та тестування.

### Дивіться також

- [imagegd2()](function.imagegd2.md) - Висновок GD2 зображення в
браузер або файл

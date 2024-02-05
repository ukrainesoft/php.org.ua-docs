---
navigation:
  - function.exif-imagetype.md: « exif\_imagetype
  - function.exif-tagname.md: exif\_tagname »
  - index.md: PHP Manual
  - ref.exif.md: Exif Функції
title: exif\_read\_data
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# exif\_read\_data

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

exif\_read\_data — Читає заголовки EXIF ​​із файлів зображень

### Опис

```methodsynopsis
exif_read_data(    resource|string $file,    ?string $required_sections = null,    bool $as_arrays = false,    bool $read_thumbnail = false): array|false
```

**exif\_read\_data()** читає заголовки EXIF ​​із файлів зображень. Таким чином, можна читати метадані, що генеруються цифровими фотоапаратами.

За ідеєю, EXIF-заголовки повинні йти першими в файлах JPEG/TIFF, що генеруються фотоапаратами. Але, на жаль, кожен виробник має своє уявлення про те, як компонувати метадані зображення. Тому будьте готові до ситуації, коли перед Exif-заголовком ще є щось.

`Height`и`Width` обчислюються аналогічно до обчислень [getimagesize()](function.getimagesize.md)так що ці параметри не повинні бути присутніми в заголовку . `html` - текстовий рядок, що задає висоту/ширину, яку можна використовувати у звичайному HTML.

Якщо Exif-заголовок містить повідомлення про авторські права (Copyright), саме повідомлення може містити два значення. Ця ситуація не описана у стандарті Exif 2.10, тому розділ `COMPUTED` міститиме обидва ці значення в полях `Copyright.Photographer`и`Copyright.Editor`. Водночас розділи `IFD0` будуть містити масив байт з NULL-символом як роздільник цих двох значень або тільки перше значення, якщо тип файлу визначено неправильно (нормальна ситуація для Exif). Розділ `COMPUTED` буде також містити `Copyright`, це може бути або вихідний рядок, або список із власника фотографії та редактора через кому.

Тег`UserComment` має ті ж проблеми, що й Copyright. Він може зберігати 2 значення. Перше - використане кодування, друге - саме значення. У цьому випадку розділ `IFD` містить або кодування, або масив байт. Розділ `COMPUTED` буде зберігати обидва ці значення в полях `UserCommentEncoding`и`UserComment`Содержимое`UserComment` буде доступно в будь-якому випадку, тому краще використовувати його замість розділу `IFD0`

Также**exif\_read\_data()** перевіряє EXIF ​​теги на відповідність специфікації EXIF ​​([» http://exif.org/Exif2-2.PDF](http://exif.org/Exif2-2.PDF), Стор. 20).

### Список параметрів

`file`

Розташування файлу із зображенням. Можливо як шляхом до файлу, і потоковим ресурсом (можна використовувати обгортки).

`required_sections`

Список розділених комів розділів, які мають бути представлені в результуючому масиві (array). Якщо жоден із розділів знайти не вдасться, функція поверне **`false`**

< td>COMPUTED

<table class="doctable informaltable"><tbody class="tbody"><tr><td>FILE</td><td>FileName, FileSize, FileDateTime, SectionsFound</td></tr><tr><td>html, Width, Height, IsColor та інші. Height та Width обчислюються аналогічно <span class="function"><a href="function.getimagesize.md" class="function">getimagesize()</a></span>, тому їх не обов'язково включати в заголовок. <code class="literal">html</code> - текстовий рядок, що задає висоту/ширину, яку можна використовувати у звичайному <abbr title="Hyper Text Markup Language">HTML</abbr>.</td></tr><tr><td>ANY_TAG</td><td>Будь-яка інформація укладена в тег, наприклад, <code class="literal">IFD0</code>, <code class="literal">EXIF</code>, ...</td></tr><tr><td>IFD0</td><td>Всі дані тега IFD0. У звичайних зображеннях у ньому зберігається розмір зображення.</td></tr><tr><td>THUMBNAIL</td><td>Якщо файл містить другий розділ <code class="literal">IFD</code>, то вважається, що зображення є ескіз. Вся інформація про ескіз зберігається в цьому розділі.</td></tr><tr><td>COMMENT</td><td>Заголовки коментарів JPEG зображень.</td></tr><tr><td>EXIF</td><td>Розділ EXIF ​​є підрозділом <code class="literal">IFD0</code>. Він містить більш детальну інформацію про зображення. Більшість його записів залежить від фотоапарата.</td></tr></tbody></table>

`as_arrays`

Визначає, чи формувати розділи як масивів. Розділи `required_sections` `COMPUTED` `THUMBNAIL`и`COMMENT` завжди робляться масивами, оскільки можуть містити значення, імена яких конфліктуватимуть з іменами інших розділах.

`read_thumbnail`

Якщо **`true`**, буде прочитано сам ескіз. Інакше буде прочитана лише інформація у тегах.

### Значення, що повертаються

Повертає асоціативний масив (array), у якому ключами будуть імена заголовків, а значеннями – значення, що відповідають цим заголовкам. Якщо жодних даних повернути не можна, **exif\_read\_data()** поверне **`false`**

### Помилки

Помилки рівня **`E_WARNING`**и/или**`E_NOTICE`** можуть виникати для тегів, що не підтримуються, або інших потенційних умов помилки, але функція все одно намагається прочитати всю зрозумілу інформацію.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `required_sections` тепер допускає значення null. |
| 7.2.0 | Параметр`file`перейменований на`stream` і може приймати як локальний шлях до файлу, і потоковий ресурс. |
| 7.2.0 | Додано підтримку наступних форматів EXIF: |

-   Samsung
-   DJI
-   Panasonic
-   Sony
-   Pentax
-   Minolta
-   Sigma/Foveon
-   AGFA
-   Kyocera
-   Ricoh
-   Epson

### Приклади

**Пример #1 Пример использования**exif\_read\_data()\*\*\*\*

```php
<?php
echo "test1.jpg:<br />\n";
$exif = exif_read_data('tests/test1.jpg', 'IFD0');
echo $exif===false ? "Не найдено данных заголовка.<br />\n" : "Изображение содержит заголовки<br />\n";

$exif = exif_read_data('tests/test2.jpg', 0, true);
echo "test2.jpg:<br />\n";
foreach ($exif as $key => $section) {
    foreach ($section as $name => $val) {
        echo "$key.$name: $val<br />\n";
    }
}
?>
```

Перший дзвінок завершується невдачею, оскільки в заголовках зображення немає інформації.

Висновок наведеного прикладу буде схожим на:

```
test1.jpg:
No header data found.
test2.jpg:
FILE.FileName: test2.jpg
FILE.FileDateTime: 1017666176
FILE.FileSize: 1240
FILE.FileType: 2
FILE.SectionsFound: ANY_TAG, IFD0, THUMBNAIL, COMMENT
COMPUTED.md: width="1" height="1"
COMPUTED.Height: 1
COMPUTED.Width: 1
COMPUTED.IsColor: 1
COMPUTED.ByteOrderMotorola: 1
COMPUTED.UserComment: Exif test image.
COMPUTED.UserCommentEncoding: ASCII
COMPUTED.Copyright: Photo (c) M.Boerger, Edited by M.Boerger.
COMPUTED.Copyright.Photographer: Photo (c) M.Boerger
COMPUTED.Copyright.Editor: Edited by M.Boerger.
IFD0.Copyright: Photo (c) M.Boerger
IFD0.UserComment: ASCII
THUMBNAIL.JPEGInterchangeFormat: 134
THUMBNAIL.JPEGInterchangeFormatLength: 523
COMMENT.0: Comment #1.
COMMENT.1: Comment #2.
COMMENT.2: Comment #3end
THUMBNAIL.JPEGInterchangeFormat: 134
THUMBNAIL.Thumbnail.Height: 1
THUMBNAIL.Thumbnail.Height: 1
```

**Пример #2 Использование**exif\_read\_data()\*\* з потоковим ресурсом (доступно з PHP 7.2.0)\*\*

```php
<?php
// Открываем файл в бинарном режиме
$fp = fopen('/path/to/image.jpg', 'rb');

if (!$fp) {
    echo 'Ошибка: Невозможно открыть файл для чтения';
    exit;
}

// Попытка прочитать заголовки exif
$headers = exif_read_data($fp);

if (!$headers) {
    echo 'Ошибка: невозможно прочитать заголовки exif';
    exit;
}

// Напечатать заголовки 'COMPUTED'
echo 'Заголовки EXIF:' . PHP_EOL;

foreach ($headers['COMPUTED'] as $header => $value) {
    printf(' %s => %s%s', $header, $value, PHP_EOL);
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
EXIF Headers:
 Height => 576
 Width => 1024
 IsColor => 1
 ByteOrderMotorola => 0
 ApertureFNumber => f/5.6
 UserComment =>
 UserCommentEncoding => UNDEFINED
 Copyright => Denis
 Thumbnail.FileType => 2
 Thumbnail.MimeType => image/jpeg
```

### Примітки

> **Зауваження** :
> 
> Якщо дозволено [mbstring](ref.mbstring.md), то exif буде намагатися обробляти юнікод і брати кодування як зазначено в [exif.decode\_unicode\_motorola](exif.configuration.md#ini.exif.decode-unicode-motorola) і [exif.decode\_unicode\_intel](exif.configuration.md#ini.exif.decode-unicode-intel). Модуль exif не намагатиметься самостійно визначити кодування та вказівка ​​правильного кодування залишається на совісті користувача шляхом встановлення однієї з двох INI-директив перед викликом **exif\_read\_data()**

> **Зауваження** :
> 
> Якщо параметр `file` використаний для передачі в функцію потоку, цей потік повинен бути перемотується. Зверніть увагу, що файловий позиційний покажчик не буде змінено після завершення роботи цієї функції.

### Дивіться також

-   [exif\_thumbnail()](function.exif-thumbnail.md) \- Отримує вбудоване прев'ю зображення
-   [getimagesize()](function.getimagesize.md) \- Отримання розміру зображення
-   [Підтримувані протоколи та обгортки](wrappers.md)

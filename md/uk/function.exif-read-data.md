- [«exif_imagetype](function.exif-imagetype.md)
- [exif_tagname »](function.exif-tagname.md)

- [PHP Manual](index.md)
- [Exif Функції](ref.exif.md)
- Читає заголовки EXIF із файлів зображень

# exif_read_data

(PHP 4 \>= 4.2.0, PHP 5, PHP 7, PHP 8)

exif_read_data — Читає заголовки EXIF із файлів зображень

### Опис

**exif_read_data**(
resource\|string `$file`,
?string `$required_sections` = **`null`**,
bool `$as_arrays` = **`false`**,
bool `$read_thumbnail` = **`false`**
): array\|false

**exif_read_data()** читає заголовки EXIF із файлів зображень. Таким
можна читати метадані, генеровані цифровими фотоапаратами.

За ідеєю, EXIF-заголовки повинні йти першими в JPEG/TIFF файлах,
генеруються фотоапаратами. Але, на жаль, кожен виробник має
своє уявлення про те, як компонувати метадані
зображення. Тому будьте готові до ситуації, коли перед
Exif-заголовком є ще щось.

`Height` та `Width` обчислюються аналогічно до обчислень
[getimagesize()](function.getimagesize.md), тому ці параметри не
повинні бути у заголовку. `html` - текстовий рядок, що задає
висоту/ширину, яку можна використовувати у звичайному HTML.

Якщо Exif-заголовок містить повідомлення про авторські права (Copyright),
саме повідомлення може містити 2 значення. Ця ситуація не описана в
стандарті Exif 2.10, тому розділ `COMPUTED` буде містити обидва ці
значення в полях `Copyright.Photographer` та `Copyright.Editor`. В теж
час розділи `IFD0` будуть містити масив байт з NULL-символом
як роздільник цих двох значень або тільки перше значення,
якщо тип файлу визначено неправильно (звичайна ситуація для Exif). Розділ
`COMPUTED` буде також містити `Copyright`, це може бути або
вихідний рядок, або список із власника фотографії та редактора через
кому.

Тег UserComment має ті ж проблеми, що і Copyright. Він може
зберігати 2 значення. Перше - використане кодування, друге - саме
значення. У цьому випадку розділ `IFD` містить або кодування, або
масив байт. Розділ `COMPUTED` буде зберігати обидва ці значення в полях
`UserCommentEncoding` та `UserComment`. Вміст `UserComment` буде
доступно в будь-якому випадку, тому краще використовувати його
замість розділу `IFD0`.

Також **exif_read_data()** перевіряє EXIF теги на відповідність
специфікації EXIF
([»http://exif.org/Exif2-2.PDF](http://exif.org/Exif2-2.PDF), стор 20).

### Список параметрів

`file`
Розташування файлу із зображенням. Можливо як шляхом до файлу, і
потоковим ресурсом (можна використовувати обгортки).

`required_sections`
Список розділених ком розділів, які повинні бути представлені в
результуючий масив (array). Якщо жоден із розділів знайти не
вдасться, функція поверне **`false`**.

|           |                                                                                                                                                                                                                                                                  |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FILE      | FileName, FileSize, FileDateTime, SectionsFound                                                                                                                                                                                                                  |
| COMPUTED  | html, Width, Height, IsColor, та інші. Height і Width обчислюються аналогічно [getimagesize()](function.getimagesize.md), тому їх обов'язково включати в заголовок. html - текстовий рядок, що задає висоту/ширину, яку можна використовувати у звичайному HTML. |
| ANY_TAG   | Будь-яка інформація міститься в тег, наприклад, IFD0, EXIF, ...                                                                                                                                                                                                  |
| IFD0      | Всі дані тега IFD0. У звичайних зображеннях зберігається розмір зображення.                                                                                                                                                                                      |
| THUMBNAIL | Якщо файл містить другий розділ IFD, то вважається, що зображення є ескіз. Вся інформація про ескіз зберігається у цьому розділі.                                                                                                                                |
| COMMENT   | Заголовки коментарів JPEG-зображень.                                                                                                                                                                                                                             |
| EXIF      | Розділ EXIF є підрозділом IFD0. Він містить більш детальну інформацію про зображення. Більшість його записів залежить від фотоапарата.                                                                                                                           |

`as_arrays`
Визначає, чи формувати розділи як масивів. Розділи
`required_sections`, `COMPUTED`, `THUMBNAIL` і `COMMENT` завжди робляться
масивами, тому що вони можуть містити значення, імена яких будуть
конфліктувати з іменами інших розділах.

`read_thumbnail`
Якщо **`true`**, буде прочитано сам ескіз. Інакше буде
прочитана лише інформація у тегах.

### Значення, що повертаються

Повертає асоціативний масив (array), у якому ключами будуть імена
заголовків, а значеннями - значення, що відповідають цим заголовкам.
Якщо жодних даних повернути не можна, **exif_read_data()** поверне
**`false`**.

### Помилки

Помилки рівня **`E_WARNING`** та/або **`E_NOTICE`** можуть виникати для
непідтримуваних тегів або інших потенційних умов помилки, але
функція все одно намагається прочитати всю зрозумілу інформацію.

### Список змін

[TABLE]

### Приклади

**Приклад #1 Приклад використання **exif_read_data()****

`<?phpecho "test1.jpg:<br />
";$exif = exif_read_data('tests/test1.jpg', 'IFD0');echo $exif===false ? "Не найдено даних заголовка.<br />
" : "Зображення містить заголовки<br />
";$exif = exif_read_data('tests/test2.jpg', 0, true);echo "test2.jpg:<br />
";foreach ($exif as $key => $section) {    foreach ($section as $name => $val) {        echo "$key.$name: >
";    }}?> `

Перший виклик завершується невдачею, тому що в заголовках зображення немає
інформації.

Результатом виконання цього прикладу буде щось подібне:

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
COMPUTED.Copyright: Фотографії (c) M.Boerger, Edited by M.Boerger.
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

**Приклад #2 Використання **exif_read_data()** з потоковим ресурсом
(доступно з PHP 7.2.0)**

` <?php//Відкриваємо файл в бінарному режимі$fp = fopen('/path/to/image.jpg', 'rb');if (!$fp) {    echo 'Помилка: Неможливий  Неможливий| exit;}// Спроба прочитати заголовки exif$headers = exif_read_data($fp);if (!$headers) {   echo 'Помилка: неможливо прочитати заголовки exif'; exit;}// Надрукувати заголовки 'COMPUTED'echo 'Заголовки EXIF:' . PHP_EOL;foreach ($headers['COMPUTED'] as $header => $value) {    printf(' %s => %s%s', $header, $value, PHP_EOL);}>?

Результатом виконання цього прикладу буде щось подібне:

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

### Примітки

> **Примітка**:
>
> Якщо дозволено [mbstring](ref.mbstring.md), exif буде намагатися
> обробляти юнікод і брати кодування як зазначено в
> [exif.decode_unicode_motorola](exif.configuration.md#ini.exif.decode-unicode-motorola)
> і
> [exif.decode_unicode_intel](exif.configuration.md#ini.exif.decode-unicode-intel).
> Модуль exif не намагатиметься самостійно визначити кодування та
> Вказівка правильного кодування залишається на совісті користувача шляхом
> встановлення однієї з двох INI-директив перед викликом
> **exif_read_data()**.

> **Примітка**:
>
> Якщо параметр `file` використаний передачі у функцію потоку, то
> цей потік повинен бути перемотувати. Зверніть увагу, що файловий
> Позиційний покажчик не буде змінено після завершення цієї роботи
> Функції.

### Дивіться також

- [exif_thumbnail()](function.exif-thumbnail.md) - Отримує
вбудоване прев'ю зображення
- [getimagesize()](function.getimagesize.md) - Отримання розміру
зображення
- [Підтримувані протоколи та обгортки](wrappers.md)

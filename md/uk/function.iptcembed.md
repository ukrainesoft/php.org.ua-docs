- [«imagexbm](function.imagexbm.md)
- [iptcparse »](function.iptcparse.md)

- [PHP Manual](index.md)
- [Функції GD та функції для роботи із зображеннями](ref.image.md)
- Вбудовування двійкових IPTC даних у JPEG зображення

# iptcembed

(PHP 4, PHP 5, PHP 7, PHP 8)

iptcembed — Вбудовування двійкових IPTC даних у JPEG зображення

### Опис

**iptcembed**(string `$iptc_data`, string `$filename`, int `$spool` =
0): string\|bool

Включає двійкові IPTC дані у зображення JPEG.

### Список параметрів

`iptc_data`
Дані.

`filename`
Шлях до зображення JPEG.

`spool`
Якщо значення цього прапора більше 2, то JPEG буде повернено як
рядки. Інакше JPEG буде надруковано в STDOUT.

### Значення, що повертаються

Якщо `spool` менше 2, буде повернено JPEG або **`false`** у разі
виникнення помилки. В іншому випадку **`true`** у разі успішного
виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Вбудовування даних IPTC у JPEG**

` <?php// iptc_make_tag() функція від Thies C. Arntzenfunction iptc_make_tag($rec, $data, $value){    $length = strlen($value); $retval==chr(0x1C) . chr($rec) . chr ($ data); if($length < 0x8000)    {        $retval .= chr($length >> 8) . chr($length & 0xFF); }   else    {        $retval .= chr(0x80) . chr(0x04) . chr(($length >> 24) & 0xFF) . chr(($length >> 16) & 0xFF) . chr(($length >> 8) & 0xFF) . chr($length & 0xFF); }   return $retval . $value;}//Шлях к jpeg файлу$path = './phplogo.jpg';// установка IPTC тегів$iptc = array(    '2#120' => 'Тестове 'Copyright 2008-2009, The PHP Group');// Перетворення IPTC тегів в двійковий код$data = '';foreach($iptc as $tag => $string $data .= iptc_make_tag(2, $tag, $string);}// Вбудовування IPTC даних$content = iptcembed($data, $path);// запис нового зображення в файл$f ");fwrite($fp, $content);fclose($fp);?> `

### Примітки

> **Примітка**:
>
> Ця функція не потребує бібліотеки GD.

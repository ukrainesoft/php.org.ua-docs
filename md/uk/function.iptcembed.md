Вбудовування двійкових IPTC даних у JPEG зображення

-   [« imagexbm](function.imagexbm.html)
    
-   [iptcparse »](function.iptcparse.html)
    
-   [PHP Manual](index.html)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.html)
    
-   Вбудовування двійкових IPTC даних у JPEG зображення
    

# iptcembed

(PHP 4, PHP 5, PHP 7, PHP 8)

iptcembed — Вбудовування двійкових IPTC даних у JPEG зображення

### Опис

```methodsynopsis
iptcembed(string $iptc_data, string $filename, int $spool = 0): string|bool
```

Включає двійкові IPTC дані у зображення JPEG.

### Список параметрів

`iptc_data`

Дані.

`filename`

Шлях до зображення JPEG.

`spool`

Якщо значення цього прапора більше 2, то JPEG буде повернуто у вигляді рядка. В іншому випадку, JPEG буде надруковано в STDOUT.

### Значення, що повертаються

Якщо `spool` менше 2, буде повернено JPEG або **`false`** у разі виникнення помилки. В іншому випадку **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Вбудовування даних IPTC у JPEG**

```php
<?php

// iptc_make_tag() функция от Thies C. Arntzen
function iptc_make_tag($rec, $data, $value)
{
    $length = strlen($value);
    $retval = chr(0x1C) . chr($rec) . chr($data);

    if($length < 0x8000)
    {
        $retval .= chr($length >> 8) .  chr($length & 0xFF);
    }
    else
    {
        $retval .= chr(0x80) .
                   chr(0x04) .
                   chr(($length >> 24) & 0xFF) .
                   chr(($length >> 16) & 0xFF) .
                   chr(($length >> 8) & 0xFF) .
                   chr($length & 0xFF);
    }

    return $retval . $value;
}

// Путь к jpeg файлу
$path = './phplogo.jpg';

// установка IPTC тэгов
$iptc = array(
    '2#120' => 'Тестовое изображение',
    '2#116' => 'Copyright 2008-2009, The PHP Group'
);

// Преобразование IPTC тэгов в двоичный код
$data = '';

foreach($iptc as $tag => $string)
{
    $tag = substr($tag, 2);
    $data .= iptc_make_tag(2, $tag, $string);
}

// Встраивание IPTC данных
$content = iptcembed($data, $path);

// запись нового изображения в файл
$fp = fopen($path, "wb");
fwrite($fp, $content);
fclose($fp);
?>
```

### Примітки

> **Зауваження**
> 
> Ця функція не потребує бібліотеки GD.
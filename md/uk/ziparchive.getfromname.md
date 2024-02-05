---
navigation:
  - ziparchive.getfromindex.md: '« ZipArchive::getFromIndex'
  - ziparchive.getnameindex.md: 'ZipArchive::getNameIndex »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::getFromName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::getFromName

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

ZipArchive::getFromName — Повертає вміст елемента на його ім'я

### Опис

```methodsynopsis
public ZipArchive::getFromName(string $name, int $len = 0, int $flags = 0): string|false
```

Повертає вміст елемента на його ім'я.

### Список параметрів

`name`

Ім'я елемент.

`len`

Розмір даних з елемента. Якщо , вміст читається повністю.

`flags`

Прапори, які використовуються для пошуку запису. Наступні значення можуть бути приєднані (побітове АБО).

-   **`ZipArchive::FL_UNCHANGED`**
    
-   **`ZipArchive::FL_COMPRESSED`**
    
-   **`ZipArchive::FL_NOCASE`**
    

### Значення, що повертаються

Повертає вміст елемента при успіху або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Отримати вміст файлу**

```php
<?php
$zip = new ZipArchive;
if ($zip->open('test1.zip') === TRUE) {
    echo $zip->getFromName('testfromfile.php');
    $zip->close();
} else {
    echo 'ошибка';
}
?>
```

**Приклад #2 Перетворити зображення із ZIP-елемента**

```php
<?php
$z = new ZipArchive();
if ($z->open(dirname(__FILE__) . '/test_im.zip')) {
    $im_string = $z->getFromName("pear_item.gif");
    $im = imagecreatefromstring($im_string);
    imagepng($im, 'b.png');
}
?>
```

### Дивіться також

-   [ZipArchive::getFromIndex()](ziparchive.getfromindex.md) \- Повертає вміст елемента за його індексом

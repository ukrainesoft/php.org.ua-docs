---
navigation:
  - ziparchive.getcommentname.md: '« ZipArchive::getCommentName'
  - ziparchive.getexternalattributesname.md: 'ZipArchive::getExternalAttributesName »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::getExternalAttributesIndex'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::getExternalAttributesIndex

(PHP 5 >= 5.6.0, PHP 7, PHP 8, PECL zip >= 1.12.4)

ZipArchive::getExternalAttributesIndex — Витягує зовнішні атрибути запису за її індексом

### Опис

```methodsynopsis
public ZipArchive::getExternalAttributesIndex(    int $index,    int &$opsys,    int &$attr,    int $flags = 0): bool
```

Витягує зовнішні атрибути запису за її індексом.

### Список параметрів

`index`

Індекс запису.

`opsys`

У разі успішного виконання сюди записується код операційної системи, заданий однією із констант ZipArchive::OPSYS\_

`attr`

У разі успішного виконання записуються сюди зовнішні атрибути. Значення залежить від операційної системи.

`flags`

Якщо поставлено як **`ZipArchive::FL_UNCHANGED`**, буде повернено оригінальні незмінені атрибути.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

У цьому прикладі метод отримує всі файли з ZIP-архіву test.zip і встановлює їм права Unix, отримані із зовнішніх атрибутів.

**Приклад #1 Витягуємо всі записи з їхніми правами Unix**

```php
<?php
$zip = new ZipArchive();
if ($zip->open('test.zip') === TRUE) {
    for ($idx=0 ; $s = $zip->statIndex($idx) ; $idx++) {
        if ($zip->extractTo('.', $s['name'])) {
            if ($zip->getExternalAttributesIndex($idx, $opsys, $attr)
                && $opsys==ZipArchive::OPSYS_UNIX) {
               chmod($s['name'], ($attr >> 16) & 0777);
            }
        }
    }
    $zip->close();
    echo "готово\n";
} else {
    echo "ошибка\n";
}
?>
```

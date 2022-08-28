Витягти зовнішні атрибути запису на її ім'я

-   [« ZipArchive::getExternalAttributesIndex](ziparchive.getexternalattributesindex.html)
    
-   [ZipArchive::getFromIndex »](ziparchive.getfromindex.html)
    
-   [PHP Manual](index.html)
    
-   [ZipArchive](class.ziparchive.html)
    
-   Витягти зовнішні атрибути запису на її ім'я
    

# ZipArchive::getExternalAttributesName

(PHP 5 >= 5.6.0, PHP 7, PHP 8, PECL zip >= 1.12.4)

ZipArchive::getExternalAttributesName — Вийняти зовнішні атрибути запису на ім'я

### Опис

```methodsynopsis
public ZipArchive::getExternalAttributesName(    string $name,    int &$opsys,    int &$attr,    int $flags = 0): bool
```

Витягує зовнішні атрибути запису на її ім'я.

### Список параметрів

`name`

Назва запису.

`opsys`

У разі успішного виконання сюди записується код операційної системи, заданий однією із констант ZipArchive::OPSYS

`attr`

У разі успішного виконання записуються сюди зовнішні атрибути. Значення залежить від операційної системи.

`flags`

Якщо поставлено як **`ZipArchive::FL_UNCHANGED`**, буде повернено оригінальні незмінені атрибути.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
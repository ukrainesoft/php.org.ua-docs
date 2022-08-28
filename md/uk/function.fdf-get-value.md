Отримує значення поля

-   [« fdf\_get\_status](function.fdf-get-status.html)
    
-   [fdf\_get\_version »](function.fdf-get-version.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Отримує значення поля
    

# fdfgetvalue

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfgetvalue — Отримує значення поля

### Опис

```methodsynopsis
fdf_get_value(resource $fdf_document, string $fieldname, int $which = -1): mixed
```

Отримує значення запрошеного поля.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.html) [fdf\_open()](function.fdf-open.html) або [fdf\_open\_string()](function.fdf-open-string.html)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`which`

Елементи поля масиву можна отримати, передавши цей параметр, починаючи з нуля. Для полів без масиву цей параметр буде проігноровано.

### Значення, що повертаються

Повертає значення поля.

### список змін

| Версия | Описание |
| --- | --- |
|  | Додана підтримка масивів та параметра `which` |

### Дивіться також

-   [fdf\_set\_value()](function.fdf-set-value.html) - Встановлює значення поля
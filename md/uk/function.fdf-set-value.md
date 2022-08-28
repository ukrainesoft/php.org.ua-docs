Встановлює значення поля

-   [« fdf\_set\_target\_frame](function.fdf-set-target-frame.html)
    
-   [fdf\_set\_version »](function.fdf-set-version.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Встановлює значення поля
    

# fdfsetvalue

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfsetvalue — Встановлює значення поля

### Опис

```methodsynopsis
fdf_set_value(    resource $fdf_document,    string $fieldname,    mixed $value,    int $isName = ?): bool
```

Встановлює `value` для заданого поля.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.html) [fdf\_open()](function.fdf-open.html) ор [fdf\_open\_string()](function.fdf-open-string.html)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`value`

Цей параметр зберігатиметься у вигляді рядка, якщо він не є масивом. І тут всі елементи масиву будуть збережені як масив значень.

`isName`

> **Зауваження**
> 
> У старіших версіях набору інструментів FDF останній параметр визначав, чи має значення поля бути перетворено на PDF Name (= 1) чи встановлено PDF String (= 0).
> 
> Це значення більше не використовується у поточній версії 5.0. Для сумісності воно, як і раніше, підтримується як необов'язковий параметр, але внутрішньо ігнорується.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdf\_get\_value()](function.fdf-get-value.html) - Отримує значення поля
-   [fdf\_remove\_item()](function.fdf-remove-item.html) - Встановлює цільовий кадр для форми
Розбирає рядок файлу відповідно до заданого формату

-   [« SplFileObject::fread](splfileobject.fread.html)
    
-   [SplFileObject::fseek »](splfileobject.fseek.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Розбирає рядок файлу відповідно до заданого формату
    

# SplFileObject::fscanf

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::fscanf — Розбирає рядок файлу відповідно до заданого формату

### Опис

```methodsynopsis
public SplFileObject::fscanf(string $format, mixed &...$vars): array|int|null
```

Читає рядок із файлу та розбирає його відповідно до заданого формату `format`

Будь-які прогалини в рядку `format` відповідає будь-якому пробілу у рядку з файлу. Це означає, що символ табуляції (`\t`) у рядку формату може відповідати одному пробілу у рядку файлу.

### Список параметрів

`format`

Інтерпретований формат для параметра `string`, який описаний у документації функції [sprintf()](function.sprintf.html) з наступними відмінностями:

-   Функція не орієнтована на локалізацію.
-   Не підтримуються значення `F` `g` `G` і `b`
-   `D` позначає десяткове число.
-   `i` позначає ціле число із визначенням системи числення.
-   `n` означає кількість символів, оброблених на даний момент.
-   `s` зупиняє читання на будь-якому символі пробілу.
-   `*` замість `argnum$` пригнічує присвоєння цієї специфікації перетворення.

`vars`

Додаткові рядки форматування.

### Значення, що повертаються

Якщо передано лише один параметр, розпізнані у рядку значення будуть поміщені до масиву. Якщо передані додаткові рядки форматування, функція поверне кількість шаблонів, з якими збігся рядок. Необов'язкові параметри повинні надсилатися за посиланням.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::fscanf()****

```php
<?php
$file = new SplFileObject("misc.txt");
while ($userinfo = $file->fscanf("%s %s %s")) {
    list ($name, $profession, $countrycode) = $userinfo;
    // Работаем с $name $profession $countrycode
}
?>
```

Зміст файлу users.txt

javier argonaut pe hiroshi sculptor jp robert slacker us luigi florist it

### Дивіться також

-   [fscanf()](function.fscanf.html) - Обробляє дані з файлу відповідно до формату
-   [sscanf()](function.sscanf.html) - Розбирає рядок відповідно до заданого формату
-   [printf()](function.printf.html) - Виводить відформатований рядок
-   [sprintf()](function.sprintf.html) - Повертає відформатований рядок
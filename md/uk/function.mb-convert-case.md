Здійснює зміну регістру символів у рядку

-   [« mb\_chr](function.mb-chr.html)
    
-   [mb\_convert\_encoding »](function.mb-convert-encoding.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с многобайтовыми строками](ref.mbstring.html)
    
-   Здійснює зміну регістру символів у рядку
    

# мбconvertcase

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

мбconvertcase — Здійснює зміну регістру символів у рядку

### Опис

```methodsynopsis
mb_convert_case(string $string, int $mode, ?string $encoding = null): string
```

Здійснює зміну регістру символів у рядку (string) відповідно до режиму `mode`

### Список параметрів

`string`

Рядок (string) для перетворення.

`mode`

Режим зміни регістру. Це може бути одна з констант **`MB_CASE_UPPER`** **`MB_CASE_LOWER`** **`MB_CASE_TITLE`** **`MB_CASE_FOLD`** **`MB_CASE_UPPER_SIMPLE`** **`MB_CASE_LOWER_SIMPLE`** **`MB_CASE_TITLE_SIMPLE`** або **`MB_CASE_FOLD_SIMPLE`**

`encoding`

Параметр `encoding` є символьним кодуванням. Якщо він опущений або дорівнює **`null`**, замість нього буде використано значення внутрішнього кодування.

### Значення, що повертаються

Рядок `string`, перетворена відповідно до режиму `mode`

### список змін

| Версия | Описание |
| --- | --- |
|  | Додана підтримка **`MB_CASE_FOLD`** **`MB_CASE_UPPER_SIMPLE`** **`MB_CASE_LOWER_SIMPLE`** **`MB_CASE_TITLE_SIMPLE`** і **`MB_CASE_FOLD_SIMPLE`** у параметрі `mode` |

### Приклади

**Приклад #1 Приклад використання **мбconvertcase()****

```php
<?php
$str = "у мэри был маленький ягнёнок и она его очень любила";
$str = mb_convert_case($str, MB_CASE_UPPER, "UTF-8");
echo $str; // Выведет У МЭРИ БЫЛ МАЛЕНЬКИЙ ЯГНЕНОК И ОНА ЕГО ОЧЕНЬ ЛЮБИЛА
$str = mb_convert_case($str, MB_CASE_TITLE, "UTF-8");
echo $str; // Выведет У Мэри Был Маленький Ягнёнок И Она Его Очень Любила
?>
```

**Приклад #2 Приклад використання **мбconvertcase()** з нелатинським UTF-8 текстом**

```php
<?php
$str = "Τάχιστη αλώπηξ βαφής ψημένη γη, δρασκελίζει υπέρ νωθρού κυνός";
$str = mb_convert_case($str, MB_CASE_UPPER, "UTF-8");
echo $str; // Выведет ΤΆΧΙΣΤΗ ΑΛΏΠΗΞ ΒΑΦΉΣ ΨΗΜΈΝΗ ΓΗ, ΔΡΑΣΚΕΛΊΖΕΙ ΥΠΈΡ ΝΩΘΡΟΎ ΚΥΝΌΣ
$str = mb_convert_case($str, MB_CASE_TITLE, "UTF-8");
echo $str; // Выведет Τάχιστη Αλώπηξ Βαφήσ Ψημένη Γη, Δρασκελίζει Υπέρ Νωθρού Κυνόσ
?>
```

### Примітки

На відміну від стандартних функцій зміни регістру, як [strtolower()](function.strtolower.html) і [strtoupper()](function.strtoupper.html), зміна регістру складає основі властивостей символу Юнікоду. Таким чином, на поведінку функції не впливають регіональні налаштування системи, і вона може конвертувати будь-які символи, що мають 'алфавітну' властивість, наприклад а-умляут (ä).

Додаткову інформацію про властивості Юнікод дивіться за посиланням[» http://www.unicode.org/reports/tr21/](http://www.unicode.org/reports/tr21/)

### Дивіться також

-   [mb\_strtolower()](function.mb-strtolower.html) - Приведення рядка до нижнього регістру
-   [mb\_strtoupper()](function.mb-strtoupper.html) - Приведення рядка до верхнього регістру
-   [strtolower()](function.strtolower.html) - Перетворює рядок на нижній регістр
-   [strtoupper()](function.strtoupper.html) - Перетворює рядок у верхній регістр
-   [ucfirst()](function.ucfirst.html) - Перетворює перший символ рядка у верхній регістр
-   [ucwords()](function.ucwords.html) - Перетворює на верхній регістр перший символ кожного слова в рядку
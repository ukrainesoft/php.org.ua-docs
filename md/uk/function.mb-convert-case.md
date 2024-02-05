---
navigation:
  - function.mb-chr.md: « mb\_chr
  - function.mb-convert-encoding.md: mb\_convert\_encoding »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_convert\_case
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_convert\_case

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

mb\_convert\_case — Змінює регістр символів у рядку

### Опис

```methodsynopsis
mb_convert_case(string $string, int $mode, ?string $encoding = null): string
```

Змінює регістр символів у рядку, перетворюючи його заданим у параметрі `mode`способом.

### Список параметрів

`string`

Рядок (string) для перетворення.

`mode`

Режим зміни регістру. Він може набувати значення однієї з констант: **`MB_CASE_UPPER`** **`MB_CASE_LOWER`** **`MB_CASE_TITLE`** **`MB_CASE_FOLD`** **`MB_CASE_UPPER_SIMPLE`** **`MB_CASE_LOWER_SIMPLE`** **`MB_CASE_TITLE_SIMPLE`** або **`MB_CASE_FOLD_SIMPLE`**

`encoding`

Параметр`encoding` - Це кодування символів. Якщо він опущений або дорівнює **`null`**, для нього буде встановлено внутрішнє кодування символів.

### Значення, що повертаються

Повертає версію, передану в параметр `string` рядки із зміненим регістром, перетвореним заданим у параметрі `mode`способом.

### список змін

| Версия | Опис |
| --- | --- |
| 7.3.0 | Додано підтримку режимів, які можна передавати до параметра `mode` **`MB_CASE_FOLD`** **`MB_CASE_UPPER_SIMPLE`** **`MB_CASE_LOWER_SIMPLE`** **`MB_CASE_TITLE_SIMPLE`** і **`MB_CASE_FOLD_SIMPLE`** |

### Приклади

**Приклад #1 Приклад использования функции**mb\_convert\_case()\*\*\*\*

```php
<?php

$str = "у мэри был маленький ягнёнок и она его очень любила";
$str = mb_convert_case($str, MB_CASE_UPPER, "UTF-8");
echo $str; // Выведет У МЭРИ БЫЛ МАЛЕНЬКИЙ ЯГНЁНОК И ОНА ЕГО ОЧЕНЬ ЛЮБИЛА
$str = mb_convert_case($str, MB_CASE_TITLE, "UTF-8");
echo $str; // Выведет У Мэри Был Маленький Ягнёнок И Она Его Очень Любила
?>
```

**Приклад #2 Приклад использования функции**mb\_convert\_case()\*\* з нелатинський текстом у кодуванні UTF-8\*\*

```php
<?php

$str = "Τάχιστη αλώπηξ βαφής ψημένη γη, δρασκελίζει υπέρ νωθρού κυνός";
$str = mb_convert_case($str, MB_CASE_UPPER, "UTF-8");
echo $str; // Выведет ΤΆΧΙΣΤΗ ΑΛΏΠΗΞ ΒΑΦΉΣ ΨΗΜΈΝΗ ΓΗ, ΔΡΑΣΚΕΛΊΖΕΙ ΥΠΈΡ ΝΩΘΡΟΎ ΚΥΝΌΣ
$str = mb_convert_case($str, MB_CASE_TITLE, "UTF-8");
echo $str; // Выведет Τάχιστη Αλώπηξ Βαφήσ Ψημένη Γη, Δρασκελίζει Υπέρ Νωθρού Κυνόσ
?>
```

### Примітки

На відміну від стандартних функцій зміни регістру, як [strtolower()](function.strtolower.md) і [strtoupper()](function.strtoupper.md), регістр змінюється з урахуванням властивостей символу Юнікоду. Тому на поведінку цієї функції не впливають регіональні налаштування системи, і вона може конвертувати будь-які символи, що мають «алфавітну» властивість, наприклад, як а-умляут (ä).

Докладніше про властивості Юнікоду розказано за посиланням [» http://www.unicode.org/reports/tr21/](http://www.unicode.org/reports/tr21/)

### Дивіться також

-   [mb\_strtolower()](function.mb-strtolower.md) \- Наводить рядок до нижнього регістру
-   [mb\_strtoupper()](function.mb-strtoupper.md) \- Приведе рядок до верхнього регістру
-   [strtolower()](function.strtolower.md) \- Перетворює рядок на нижній регістр
-   [strtoupper()](function.strtoupper.md) \- Перетворює рядок у верхній регістр
-   [ucfirst()](function.ucfirst.md) \- Перетворює перший символ рядка у верхній регістр
-   [ucwords()](function.ucwords.md) \- Перетворює у верхній регістр перший символ кожного слова у рядку

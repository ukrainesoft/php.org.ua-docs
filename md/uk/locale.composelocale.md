---
navigation:
  - locale.canonicalize.md: '« Locale::canonicalize'
  - locale.filtermatches.md: 'Locale::filterMatches »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::composeLocale'
---
# Locale::composeLocale

# localecompose

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::composeLocale -- localecompose — Повертає коректно відсортовані та розділені ідентифікатори локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::composeLocale(array $subtags): string|false
```

Процедурний стиль

```methodsynopsis
locale_compose(array $subtags): string|false
```

Повертає рядок, що складається з коректно відсортованих і розділених ідентифікаторів локалі, зібрану з масиву, ключі якого позначають підтеги ідентифікатора, а відповідні значення цих підтегів.

### Список параметрів

`subtags`

Масив (array), що містить список пар ключ-значення, де ключі є іменами підтегів ідентифікатора локалі, а значення відповідно значеннями цих підтегів.

> **Зауваження**
> 
> Підтегів `'variant'` і `'private'` може бути не більше 15, підтегів `'extlang'` трохи більше 3 і т.д. Варіанти допустимі із суфіксами від 0 до 14. Ключі для цього підтегу мають називатися так: `variant0` `variant1``variant14`. У ідентифікаторі локалі вкладений тег упорядкований по суфіксу, в результаті чого слід `variant0`, за яким слідує `variant1`, за яким слідує `variant2` і так далі.
> 
> Як альтернатива, множинні підтеги `'variant'` `'private'` і `'extlang'` можна задати у вигляді масиву під відповідним ключем (наприклад `'variant'`). У цьому випадку обмеження на кількість розпізнаних вкладених тегів не застосовуються.

### Значення, що повертаються

Відповідний ідентифікатор локалі або **`false`**, якщо параметр `subtags` не заданий.

### Приклади

**Приклад #1 Приклад використання **localecompose()****

```php
<?php
$arr = array(
    'language'=>'en',
    'script'  =>'Hans',
    'region'  =>'CN',
    'variant2'=>'rozaj',
    'variant1'=>'nedis',
    'private1'=>'prv1',
    'private2'=>'prv2',
);
echo locale_compose($arr);
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$arr = array(
    'language'=>'en' ,
    'script'  =>'Hans',
    'region'  =>'CN',
    'variant2'=>'rozaj',
    'variant1'=>'nedis',
    'private1'=>'prv1',
    'private2'=>'prv2',
);
echo Locale::composeLocale($arr);
?>
```

Результат виконання цього прикладу:

```
Locale: en_Hans_CN_nedis_rozaj_x_prv1_prv2
```

**Приклад #3 Межі підтегів**

Якщо `subtags` задані як окремі ключі з числовим суфіксом, ключі, що не підтримуються, ігноруються (в даному випадку `'extlang3'`) і впорядковуються в результаті за числовим суфіксом. Немає обмежень, якщо вкладені теги задані як масив (array); упорядковані як зазначені.

```php
<?php
$arr = array(
    'language' => 'en',
    'script'   => 'Hans',
    'region'   => 'CN',
    'extlang3' => 'd',
    'extlang2' => 'c',
    'extlang1' => 'b',
    'extlang0' => 'a',
);
echo locale_compose($arr), PHP_EOL;

$arr = array(
    'language' => 'en',
    'script'   => 'Hans',
    'region'   => 'CN',
    'extlang'  => ['a', 'b', 'c', 'd'],
);
echo locale_compose($arr), PHP_EOL;
?>
```

Результат виконання цього прикладу:

```
en_a_b_c_Hans_CN
en_a_b_c_d_Hans_CN
```

### Дивіться також

-   [localeparse()](locale.parselocale.md) - Отримати асоціативний масив усіх підтегів локалі

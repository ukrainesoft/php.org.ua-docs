Отримати ключові слова для локалі

-   [« Locale::getDisplayVariant](locale.getdisplayvariant.html)
    
-   [Locale::getPrimaryLanguage »](locale.getprimarylanguage.html)
    
-   [PHP Manual](index.html)
    
-   [Locale](class.locale.html)
    
-   Отримати ключові слова для локалі
    

# Locale::getKeywords

# localegetkeywords

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getKeywords -- localegetkeywords — Отримати ключові слова для локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::getKeywords(string $locale): array|false|null
```

Процедурний стиль

```methodsynopsis
locale_get_keywords(string $locale): array|false|null
```

Отримує ключові слова для локалі.

### Список параметрів

`locale`

Локаль для отримання ключових слів

### Значення, що повертаються

Асоціативний масив (array) з парами ключ-значення для заданої локалі

Повертає \*\*`null`\*\*якщо довжина `locale` перевищує **`INTL_MAX_LOCALE_LEN`**

### Приклади

**Приклад #1 Приклад використання **localegetkeywords()****

```php
<?php
$keywords_arr = locale_get_keywords('de_DE@currency=EUR;collation=PHONEBOOK');
if ($keywords_arr) {
    foreach ($keywords_arr as $key => $value) {
        echo "$key = $value\n";
    }
}
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$keywords_arr = Locale::getKeywords('de_DE@currency=EUR;collation=PHONEBOOK');
if ($keywords_arr) {
    foreach ($keywords_arr as $key => $value) {
        echo "$key = $value\n";
    }
}
?>
```

Результат виконання цього прикладу:

```
collation = PHONEBOOK
currency = EUR
```

### Дивіться також

-   [localegetallvariants()](locale.getallvariants.html) - Отримання варіантів із переданої локалі
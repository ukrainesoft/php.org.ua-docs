Встановити локаль за умовчанням під час виконання

-   [« Locale::parseLocale](locale.parselocale.html)
    
-   [Normalizer »](class.normalizer.html)
    
-   [PHP Manual](index.html)
    
-   [Locale](class.locale.html)
    
-   Встановити локаль за умовчанням під час виконання
    

# Locale::setDefault

# localesetdefault

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::setDefault -- localesetdefault — Встановити стандартний локаль під час виконання

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::setDefault(string $locale): bool
```

Процедурний стиль

```methodsynopsis
locale_set_default(string $locale): bool
```

Встановлює локаль за умовчанням під час виконання згідно з аргументом `locale`. Ця функція змінює значення глобальної опції 'defaultlocale'. Допускаються розширення UAX #35.

### Список параметрів

`locale`

Сумісна з BCP 47 мітка мови.

### Значення, що повертаються

Повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **localesetdefault()****

```php
<?php
locale_set_default('de-DE');
echo locale_get_default();
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
Locale::setDefault('de-DE');
echo Locale::getDefault();
?>
```

Результат виконання цього прикладу:

```
de-DE
```

### Дивіться також

-   [locale\_get\_default()](locale.getdefault.html) - Отримання значення локалі INTL за замовчуванням з опції 'defaultlocale'
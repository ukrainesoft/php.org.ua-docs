---
navigation:
  - locale.getallvariants.md: '« Locale::getAllVariants'
  - locale.getdisplaylanguage.md: 'Locale::getDisplayLanguage »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::getDefault'
---
# Locale::getDefault

# localegetdefault

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::getDefault -- localegetdefault — Отримання значення локалі INTL за замовчуванням з опції 'defaultlocale'

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::getDefault(): string
```

Процедурний стиль

```methodsynopsis
locale_get_default(): string
```

Отримання значення локалі за замовчуванням. при ініціалізації PHP, це значення встановлюється в 'intl.defaultlocale' з php.ini, якщо воно там є, або значення функції ICU ulocgetDefault().

### Список параметрів

### Значення, що повертаються

Поточна локаль часу виконання

### Приклади

**Приклад #1 Приклад використання **localegetdefault()****

```php
<?php
ini_set('intl.default_locale', 'de-DE');
echo locale_get_default();
echo '; ';
locale_set_default('fr');
echo locale_get_default();
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
ini_set('intl.default_locale', 'de-DE');
echo Locale::getDefault();
echo '; ';
Locale::setDefault('fr');
echo Locale::getDefault();
?>
```

Результат виконання цього прикладу:

```
de-DE; fr
```

### Дивіться також

-   [localesetdefault()](locale.setdefault.md) - Встановити локаль за умовчанням під час виконання

---
navigation:
  - locale.parselocale.md: '« Locale::parseLocale'
  - class.normalizer.md: Normalizer »
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::setDefault'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Locale::setDefault

# locale\_set\_default

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::setDefault -- locale\_set\_default — Встановити стандартний локаль під час виконання

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::setDefault(string $locale): bool
```

Процедурний стиль

```methodsynopsis
locale_set_default(string $locale): bool
```

Устанавливает локаль по умолчанию во время исполнения согласно аргументу`locale`. . Ця функція змінює значення глобальної опції 'default\_locale'. Допускається розширення UAX #35.

### Список параметрів

`locale`

Сумісна з BCP 47 мітка мови.

### Значення, що повертаються

Повертає **`true`**

### Приклади

**Пример #1 Пример использования**locale\_set\_default()\*\*\*\*

```php
<?php
locale_set_default('de-DE');
echo locale_get_default();
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
Locale::setDefault('de-DE');
echo Locale::getDefault();
?>
```

Результат виконання наведеного прикладу:

```
de-DE
```

### Дивіться також

-   [locale\_get\_default()](locale.getdefault.md) - Отримання значення локалі INTL за замовчуванням з опції 'default\_locale'

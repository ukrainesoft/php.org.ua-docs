---
navigation:
  - collator.geterrormessage.html: '« Collator::getErrorMessage'
  - collator.getsortkey.html: 'Collator::getSortKey »'
  - index.html: PHP Manual
  - class.collator.html: Collator
title: 'Collator::getLocale'
---
# Collator::getLocale

# collatorgetlocale

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Collator::getLocale -- collatorgetlocale — Отримує назву локалі для Collator

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Collator::getLocale(int $type): string|false
```

Процедурний стиль

```methodsynopsis
collator_get_locale(Collator $object, int $type): string|false
```

Отримує назву локалі Collator.

### Список параметрів

`object`

Об'єкт [Collator](class.collator.html)

`type`

Ви можете вибирати між коректним та фактичним мовним стандартом ( **`Locale::VALID_LOCALE`** і \*\*`Locale::ACTUAL_LOCALE`\*\*відповідно).

### Значення, що повертаються

Справжнє ім'я локалі, з якого беруться дані зіставлення. Якщо Collator був створений з правил або помилка, повертає **`false`**

### Приклади

**Приклад #1 **collatorgetlocale()** example**

```php
<?php
$coll    = collator_create( 'en_US_California' );
$res_val = collator_get_locale( $coll, Locale::VALID_LOCALE );
$res_act = collator_get_locale( $coll, Locale::ACTUAL_LOCALE );
printf( "Название корректной локали: %s\nНазвание фактической локали: %s\n",
         $res_val, $res_act );
?>
```

Результат виконання цього прикладу:

```
Запрошенное название локали: en_US_California
Название корректной локали: en_US
Название фактической локали: en
```

### Дивіться також

-   [collatorcreate()](collator.create.html) - Створює новий екземпляр Collator

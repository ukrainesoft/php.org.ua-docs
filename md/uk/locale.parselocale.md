---
navigation:
  - locale.lookup.md: '« Locale::lookup'
  - locale.setdefault.md: 'Locale::setDefault »'
  - index.md: PHP Manual
  - class.locale.md: Locale
title: 'Locale::parseLocale'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Locale::parseLocale

# locale\_parse

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

Locale::parseLocale -- locale\_parse - Отримати асоціативний масив усіх підтегів локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Locale::parseLocale(string $locale): ?array
```

Процедурний стиль

```methodsynopsis
locale_parse(string $locale): ?array
```

Повертає асоціативний масив, що містить усі підтеги заданої локалі.

### Список параметрів

`locale`

Локаль з якої витягуватиметься підтеги. Зверніть увагу: підтегів 'variant' та 'private' може бути не більше 15, а підтегів 'extlang' не більше 3.

### Значення, що повертаються

Повертає асоціативний масив, у якому ключами виступають імена підтегів, а значеннями відповідно їх значення. Підтеги відсортовані як підтеги ідентифікатора локалі, тобто. якщо ідентифікатор містить кілька варіантів '-varX-varY-varZ', то в масиві вони розташовуватимуться так: variant0=>varX, variant1=>varY, variant2=>varZ

Повертає \*\*`null`\*\*если длина параметра`locale` перевищує **`INTL_MAX_LOCALE_LEN`**

### Приклади

**Приклад #1 Приклад використання** locale\_parse()\*\*\*\*

```php
<?php
$arr = locale_parse('sl-Latn-IT-nedis');
if ($arr) {
    foreach ($arr as $key => $value) {
        echo "$key : $value , ";
    }
}
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$arr = Locale::parseLocale('sl-Latn-IT-nedis');
if ($arr) {
    foreach ($arr as $key => $value) {
        echo "$key : $value , ";
    }
}
?>
```

Результат виконання наведеного прикладу:

```
language : sl , script : Latn , region : IT , variant0 : NEDIS ,
```

### Дивіться також

-   [locale\_compose()](locale.composelocale.md) \- Повертає коректно відсортовані та розділені ідентифікатори локалі

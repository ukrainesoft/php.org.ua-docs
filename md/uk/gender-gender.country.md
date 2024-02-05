---
navigation:
  - gender-gender.construct.md: '« Gender\\Gender::\_\_construct'
  - gender-gender.get.md: 'Gender\\Gender::get »'
  - index.md: PHP Manual
  - class.gender.md: Gender\\Gender
title: 'Gender\\Gender::country'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gender\\Gender::country

(PECL gender >= 0.8.0)

Gender\\Gender::country — Отримати текстове подання країни

### Опис

```methodsynopsis
public Gender\Gender::country(int $country): array|false
```

Повертає текстову виставу країни із констант класу Gender.

### Список параметрів

`country`

Ідентифікатор країни, заданий константою класу [Gender\\Gender](class.gender.md)

### Значення, що повертаються

Повертає масив з коротким та повним ім'ям країни у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**Gender\\Gender::country()\*\*\*\*

```php
$gender = new Gender\Gender;
var_dump($gender->country(Gender\Gender::BRITAIN));
```

Результат виконання наведеного прикладу:

```
array(2) {
  'country_short' =>
  string(2) "UK"
  'country' =>
  string(13) "Great Britain"
}
```

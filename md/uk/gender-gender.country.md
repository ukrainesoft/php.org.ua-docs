---
navigation:
  - gender-gender.construct.md: '« GenderGender::construct'
  - gender-gender.get.md: 'GenderGender::get »'
  - index.md: PHP Manual
  - class.gender.md: GenderGender
title: 'GenderGender::country'
---
# GenderGender::country

(PECL gender >= 0.8.0)

GenderGender::country — Отримати текстове подання країни

### Опис

```methodsynopsis
public Gender\Gender::country(int $country): array|false
```

Повертає текстову виставу країни із констант класу Gender.

### Список параметрів

`country`

Ідентифікатор країни, заданий константою класу [GenderGender](class.gender.md)

### Значення, що повертаються

Повертає масив з коротким та повним ім'ям країни у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **GenderGender::country()****

```php
$gender = new Gender\Gender;
var_dump($gender->country(Gender\Gender::BRITAIN));
```

Результат виконання цього прикладу:

```
array(2) {
  'country_short' =>
  string(2) "UK"
  'country' =>
  string(13) "Great Britain"
}
```

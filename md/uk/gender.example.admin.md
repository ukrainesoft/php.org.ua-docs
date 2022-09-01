---
navigation:
  - gender.examples.md: « Приклади
  - class.gender.md: GenderGender »
  - index.md: PHP Manual
  - gender.examples.md: Приклади
title: Приклад використання
---
## Приклад використання

Приклад використання класу Gender.

**Приклад #1 Приклад використання.**

```php
<?php

namespace Gender;

$gender = new Gender;


$name = "Milene";
$country = Gender::FRANCE;

$result = $gender->get($name, $country);

$data = $gender->country($country);

switch($result) {
    case Gender::IS_FEMALE:
        printf("%s - это женское имя в стране %s\n", $name, $data['country']);
    break;


    case Gender::IS_MOSTLY_FEMALE:
        printf("%s  - это скорее всего женское имя в стране %s\n", $name, $data['country']);
    break;


    case Gender::IS_MALE:
        printf("%s - это мужское имя в стране %s\n", $name, $data['country']);
    break;


    case Gender::IS_MOSTLY_MALE:
        printf("%s  - это скорее всего женское имя в стране %s\n", $name, $data['country']);
    break;


    case Gender::IS_UNISEX_NAME:
        printf("Имя %s годится и для женщин, и для мужчин в стране %s\n", $name, $data['country']);
    break;


    case Gender::IS_A_COUPLE:
        printf("Имя %s может быть и женским, и мужским в стране %s\n", $name, $data['country']);
    break;


    case Gender::NAME_NOT_FOUND:
        printf("Имя %s не найдено для страны %s\n", $name, $data['country']);
    break;


    case Gender::ERROR_IN_NAME:
        echo "В заданном имени ошибка!\n";
    break;

    default:
        echo "Произошла ошибка!\n";
    break;

}
```

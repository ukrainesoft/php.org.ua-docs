---
navigation:
  - function.filter-input-array.md: « filter\_input\_array
  - function.filter-list.md: filter\_list »
  - index.md: PHP Manual
  - ref.filter.md: Функції фільтрації даних
title: filter\_input
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# filter\_input

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

filter\_input - Приймає змінну ззовні PHP і, при необхідності, фільтрує її

### Опис

```methodsynopsis
filter_input(    int $type,    string $var_name,    int $filter = FILTER_DEFAULT,    array|int $options = 0): mixed
```

### Список параметрів

`type`

Одна из констант\*\*`INPUT_GET`\*\* **`INPUT_POST`** **`INPUT_COOKIE`** **`INPUT_SERVER`** або **`INPUT_ENV`**

`var_name`

Ім'я змінної, що отримується.

`filter`

Ідентифікатор (ID) фільтра. На сторінці [Типи фільтрів](filter.filters.md) наведено список доступних фільтрів.

Если не указан, то принимает значение по умолчанию —\*\*`FILTER_DEFAULT`\*\*, який рівнозначний значенню константи [**`FILTER_UNSAFE_RAW`**](filter.filters.sanitize.md)То есть по умолчанию значение не фильтруется.

`options`

Асоціативний масив параметрів чи логічне АБО прапорів. Якщо фільтр приймає настройки, прапори можуть бути вказані в елементі масиву "flags".

### Значення, що повертаються

Значення запитуваної змінної у разі успішного виконання, **`false`**, якщо фільтрація завершилася невдачею, або **`null`**, если переменная`var_name`не определена. Если установлен флаг\*\*`FILTER_NULL_ON_FAILURE`\*\*, функція повертає **`false`**, якщо змінна не визначена та \*\*`null`\*\*якщо фільтрація завершилася невдачею.

### Приклади

**Приклад #1 Приклад використання** filter\_input()\*\*\*\*

```php
<?php
$search_html = filter_input(INPUT_GET, 'search', FILTER_SANITIZE_SPECIAL_CHARS);
$search_url = filter_input(INPUT_GET, 'search', FILTER_SANITIZE_ENCODED);
echo "Вы искали $search_html.\n";
echo "<a href='?search=$search_url'>Искать снова.</a>";
?>
```

Висновок наведеного прикладу буде схожим на:

```
Вы искали Me &#38; son.
<a href='?search=Me%20%26%20son'>Искать снова.</a>
```

### Дивіться також

-   [filter\_var()](function.filter-var.md) \- Фільтрує змінну за допомогою певного фільтра
-   [filter\_input\_array()](function.filter-input-array.md) \- Отримує кілька змінних ззовні PHP і, при необхідності, фільтрує їх
-   [filter\_var\_array()](function.filter-var-array.md) \- приймає кілька змінних і, при необхідності, фільтрує їх
-   [Типи фільтрів](filter.filters.md)

---
navigation:
  - function.mdspecialchars.md: « htmlspecialchars
  - function.join.md: join »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: implode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# implode

(PHP 4, PHP 5, PHP 7, PHP 8)

implode — Об'єднує елементи масиву в рядок

### Опис

```methodsynopsis
implode(string $separator, array $array): string
```

Альтернативна сигнатура (не підтримується з іменованими аргументами):

```methodsynopsis
implode(array $array): string
```

Застаріла сигнатура (застаріла з PHP 7.4.0, видалена в PHP 8.0.0):

```methodsynopsis
implode(array $array, string $separator): string
```

Об'єднує елементи масиву за допомогою рядка `separator`

### Список параметрів

`separator`

Необов'язковий. За замовчуванням дорівнює порожньому рядку.

`array`

Масив рядків, що об'єднуються.

### Значення, що повертаються

Повертає рядок, що містить рядкове представлення всіх елементів масиву у вказаному порядку з роздільником між кожним елементом.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Передача`separator`после`array`більше не підтримується. |
| 7.4.0 | Передача`separator`после`array` (тобто використання недокументованого порядку параметрів) застаріла. |

### Приклади

**Приклад #1 Приклад використання** implode()\*\*\*\*

```php
<?php

$array = ['имя', 'почта', 'телефон'];
var_dump(implode(",", $array)); // string(32) "имя,почта,телефон"

// Пустая строка при использовании пустого массива:
var_dump(implode('привет', [])); // string(0) ""

// Параметр separator не обязателен:
var_dump(implode(['a', 'b', 'c'])); // string(3) "abc"

?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [explode()](function.explode.md) \- Розбиває рядок за допомогою роздільника
-   [preg\_split()](function.preg-split.md) \- Розбиває рядок за регулярним виразом
-   [http\_build\_query()](function.http-build-query.md) \- Генерує URL-кодований рядок запиту

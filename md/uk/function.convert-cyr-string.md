---
navigation:
  - function.chunk-split.md: « chunk\_split
  - function.convert-uudecode.md: convert\_uudecode »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: convert\_cyr\_string
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# convert\_cyr\_string

(PHP 4, PHP 5, PHP 7)

convert\_cyr\_string — Перетворює рядок з одного кириличного кодування на інше

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.3.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
convert_cyr_string(string $str, string $from, string $to): string
```

Перетворює рядок з одного кириличного кодування на інше.

### Список параметрів

`str`

Конвертований рядок.

`from`

Вихідне кириличне кодування, один символ.

`to`

Цільове кириличне кодування, один символ.

Підтримуються такі символи:

-   k - koi8-r
-   w - windows-1251
-   i - iso8859-5
-   a - x-cp866
-   d - x-cp866
-   m - x-mac-cyrillic

### Значення, що повертаються

Повертає перетворений рядок.

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [mb\_convert\_encoding()](function.mb-convert-encoding.md) \- Перетворює рядок з одного кодування символів на інший
-   [iconv()](function.iconv.md) \- Перетворює рядок з одного кодування символів на інший

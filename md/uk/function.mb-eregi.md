---
navigation:
  - function.mb-eregi-replace.md: « mb\_eregi\_replace
  - function.mb-get-info.md: mb\_get\_info »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_eregi
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_eregi

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

mb\_eregi — Знаходить відповідність регулярному виразу за допомогою багатобайтових символів без урахування регістру

### Опис

```methodsynopsis
mb_eregi(string $pattern, string $string, array &$matches = null): bool
```

Виконує нечутливий до регістру пошук відповідності регулярному виразу за допомогою багатобайтних символів.

### Список параметрів

`pattern`

Шаблон пошуку.

`string`

Рядок (string) пошуку.

`matches`

Якщо знайдені збіги для підрядки `pattern`, укладеної в дужки, та функція викликана із заданим третім параметром `matches`, збіги будуть збережені в масиві `matches`Если совпадений не найдено, параметр`matches` стане порожнім масивом.

Елемент $matches\[ \] міститиме перший (ліворуч) підрядок, укладений у дужки; елемент $regs\[ \] - другу і так далі. Елемент $matches\[ \] міститиме копію всього знайденого рядка.

### Значення, що повертаються

Повертає **`true`**, якщо шаблон `pattern` відповідає рядку `string`, иначе\*\*`false`\*\*

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер ця функція повертає **`true`** у разі успішного виконання. Раніше, якщо було встановлено параметр `matches` та у рядку `string` було знайдено входження шаблону `pattern`, поверталася довжина знайденого підрядка в байтах Якщо параметр `matches` не задавався або довжина знайденого підрядка дорівнювала , функція повертала |
| 7.1.0 | Функция**mb\_eregi()** встановлює значення параметра `matches` рівним порожньому масиву, якщо нічого не знайдено. Раніше за відсутності збігів параметр `matches` не змінювався. |

### Примітки

> **Зауваження** :
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [mb\_regex\_encoding()](function.mb-regex-encoding.md)

### Дивіться також

-   [mb\_regex\_encoding()](function.mb-regex-encoding.md) \- Встановлює/отримує кодування символів для однобайтового регулярного виразу
-   [mb\_ereg()](function.mb-ereg.md) \- Знаходить збіг регулярного виразу за допомогою багатобайтових кодувань

---
navigation:
  - function.mb-strcut.md: « mb\_strcut
  - function.mb-stripos.md: mb\_stripos »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_strimwidth
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_strimwidth

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_strimwidth — Отримує рядок, обрізаний до заданої ширини

### Опис

```methodsynopsis
mb_strimwidth(    string $string,    int $start,    int $width,    string $trim_marker = "",    ?string $encoding = null): string
```

Обрізає рядок (string), переданий у параметр `string`, до заданой в параметре`width` ширини символів, де символи половинної ширини розраховуються як , а символи повної ширини - як . Докладніше про ширину східноазіатських символів розказано у додатку [» http://www.unicode.org/reports/tr11/](http://www.unicode.org/reports/tr11/)

### Список параметрів

`string`

Вихідний рядок.

`start`

Зміщення з початку рядка. Кількість символів від початку рядка (перший символ стоїть у позиції 0). Якщо вказано від'ємне число, то відлік буде з кінця рядка.

`width`

Ширина, до якої потрібно обрізати рядок. Якщо задано від'ємне значення ширини, відлік буде з кінця рядка.

> **Зауваження** :
> 
> Передача від'ємного значення ширини застаріла з PHP 8.3.0.

`trim_marker`

Рядок, який замістить кінець рядка, що обрізає.

`encoding`

Параметр`encoding` - Це кодування символів. Якщо він опущений або дорівнює **`null`**, для нього буде встановлено внутрішнє кодування символів.

### Значення, що повертаються

Повертає рядок, що обрізає. Якщо встановлено четвертий параметр `trim_marker`, то його значенням заміщаються символи в кінці рядка, так, щоб сумарний розмір був не більше ширини `width`

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Передача негативного значення параметр `width` функції \*\*mb\_strimwidth()\*\*устарела. |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |
| 7.1.0 | Додано підтримку негативних значень для параметрів `start`и`width` |

### Приклади

**Приклад #1 Приклад використання функції** mb\_strimwidth()\*\*\*\*

```php
<?php
echo mb_strimwidth("Hello World", 0, 10, "...");
// Выведет "Hello W..."
?>
```

### Дивіться також

-   [mb\_strwidth()](function.mb-strwidth.md) \- Повертає ширину рядка
-   [mb\_internal\_encoding()](function.mb-internal-encoding.md) \- Встановлює/отримує внутрішнє кодування скрипту

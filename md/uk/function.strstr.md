---
navigation:
  - function.strspn.md: « strspn
  - function.strtok.md: strtok »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strstr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# strstr

(PHP 4, PHP 5, PHP 7, PHP 8)

strstr — Знаходить перше входження підрядка

### Опис

```methodsynopsis
strstr(string $haystack, string $needle, bool $before_needle = false): string|false
```

Повертає рядок рядка `haystack`, починаючи з першого входження `needle` (і включаючи його) і до кінця рядка `haystack`

> **Зауваження** :
> 
> Ця функція враховує регістр символів. Для пошуку без урахування регістру використовуйте [stristr()](function.stristr.md)

> **Зауваження** :
> 
> Якщо потрібно лише визначити, чи зустрічається підрядок `needle`в`haystack`, використовуйте більш швидку та менш ресурсоємну функцію [strpos()](function.strpos.md)

### Список параметрів

`haystack`

Вхідний рядок.

`needle`

Рядок для пошуку.

До PHP 8.0.0, если параметр`needle` - не рядок, він перетворюється на ціле число і трактується як код символу. Ця поведінка застаріла з PHP 7.3.0 і покладатися на неї не рекомендується. Залежно від передбачуваної поведінки, параметр `needle` повинен бути або явно приведений до рядка, або повинен бути виконаний явний виклик функції [chr()](function.chr.md)

`before_needle`

Если установлен в\*\*`true`\*\* **strstr()** повертає частину рядка `haystack`до первого вхождения`needle`(исключая needle).

### Значення, що повертаються

Повертає частину рядка або **`false`**, якщо `needle`не найдена.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`needle` тепер допускає порожній рядок. |
| 8.0.0 | Передача цілого числа (int) `needle`більше не підтримується. |
| 7.3.0 | Передача цілого числа (int) `needle` оголошено застарілою. |

### Приклади

**Приклад #1 Приклад використання** strstr()\*\*\*\*

```php
<?php
$email  = 'name@example.com';
$domain = strstr($email, '@');
echo $domain; // выводит @example.com

$user = strstr($email, '@', true);
echo $user; // выводит name
?>
```

### Дивіться також

-   [stristr()](function.stristr.md) \- Реєстронезалежний варіант функції strstr
-   [strrchr()](function.strrchr.md) \- Знаходить останнє входження символу у рядку
-   [strpos()](function.strpos.md) \- Повертає позицію першого входження підрядка
-   [strpbrk()](function.strpbrk.md) \- Шукає у рядку будь-який символ із заданого набору
-   [preg\_match()](function.preg-match.md) \- Виконує перевірку на відповідність регулярному виразу

---
navigation:
  - function.mb-strtoupper.md: « mb\_strtoupper
  - function.mb-substitute-character.md: mb\_substitute\_character »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_strwidth
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_strwidth

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_strwidth — Повертає ширину рядка

### Опис

```methodsynopsis
mb_strwidth(string $string, ?string $encoding = null): int
```

Повертає ширину рядка (string) `string`де символи половинної ширини вважаються , а символи повної ширини вважаються Смотрите[» http://www.unicode.org/reports/tr11/](http://www.unicode.org/reports/tr11/) для отримання детальної інформації про широту символів Східної Азії.

Символи повної ширини: `U+1100`\-`U+115F` `U+11A3`\-`U+11A7` `U+11FA`\-`U+11FF` `U+2329`\-`U+232A` `U+2E80`\-`U+2E99` `U+2E9B`\-`U+2EF3` `U+2F00`\-`U+2FD5` `U+2FF0`\-`U+2FFB` `U+3000`\-`U+303E` `U+3041`\-`U+3096` `U+3099`\-`U+30FF` `U+3105`\-`U+312D` `U+3131`\-`U+318E` `U+3190`\-`U+31BA` `U+31C0`\-`U+31E3` `U+31F0`\-`U+321E` `U+3220`\-`U+3247` `U+3250`\-`U+32FE` `U+3300`\-`U+4DBF` `U+4E00`\-`U+A48C` `U+A490`\-`U+A4C6` `U+A960`\-`U+A97C` `U+AC00`\-`U+D7A3` `U+D7B0`\-`U+D7C6` `U+D7CB`\-`U+D7FB` `U+F900`\-`U+FAFF` `U+FE10`\-`U+FE19` `U+FE30`\-`U+FE52` `U+FE54`\-`U+FE66` `U+FE68`\-`U+FE6B` `U+FF01`\-`U+FF60` `U+FFE0`\-`U+FFE6` `U+1B000`\-`U+1B001` `U+1F200`\-`U+1F202` `U+1F210`\-`U+1F23A` `U+1F240`\-`U+1F248` `U+1F250`\-`U+1F251` `U+20000`\-`U+2FFFD` `U+30000`\-`U+3FFFD`. Всі інші символи належать до символів напівширини.

### Список параметрів

`string`

Початковий рядок (string).

`encoding`

Параметр`encoding` - Це кодування символів. Якщо він опущений або дорівнює **`null`**, для нього буде встановлено внутрішнє кодування символів.

### Значення, що повертаються

Повертає ширину рядка (string) `string`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |

### Приклади

**Приклад #1 Приклад использования функции**mb\_strwidth()\*\*\*\*

```php
<?php

var_dump(
    mb_strwidth('a'),       // латинская строчная буква а
    mb_strwidth("\u{ff41}") // латинская строчная буква а полной ширины
);
?>
```

Результат виконання наведеного прикладу:

```
int(1)
int(2)
```

### Дивіться також

-   [mb\_strimwidth()](function.mb-strimwidth.md) \- Отримує рядок, обрізаний до заданої ширини
-   [mb\_internal\_encoding()](function.mb-internal-encoding.md) \- Встановлює/отримує внутрішнє кодування скрипту

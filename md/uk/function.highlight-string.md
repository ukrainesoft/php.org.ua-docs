---
navigation:
  - function.highlight-file.html: « highlightfile
  - function.hrtime.html: hrtime »
  - index.html: PHP Manual
  - ref.misc.html: Різні функції
title: highlightstring
---
# highlightstring

(PHP 4, PHP 5, PHP 7, PHP 8)

highlightstring — Підсвічування синтаксису рядка

### Опис

```methodsynopsis
highlight_string(string $string, bool $return = false): string|bool
```

Виводить або повертає код PHP з розміткою HTML з підсвіченим синтаксисом, використовуючи кольори, визначені у вбудованому обробнику підсвічування синтаксису PHP.

### Список параметрів

`string`

PHP-код, що підсвічується. Повинен включати тег, що відкриває.

`return`

При встановленні цього параметра рівним **`true`**, функція повертає код із підсвічуванням синтаксису.

### Значення, що повертаються

Якщо параметр `return` дорівнює **`true`**, замість виведення у вигляді рядка повертається код з підсвічуванням синтаксису. В іншому випадку повертає **`true`** або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **highlightstring()****

```php
<?php
highlight_string('<?php phpinfo(); ?>');
?>
```

Результат виконання цього прикладу:

```
<code><span style="color: #000000">
<span style="color: #0000BB">&lt;?php phpinfo</span><span style="color: #007700">(); </span><span style="color: #0000BB">?&gt;</span>
</span>
</code>
```

### Примітки

> **Зауваження**
> 
> При використанні параметра `return` дана функція використовує внутрішню буферизацію виводу, тому вона не може бути використана всередині callback-функції [проstart()](function.ob-start.md)

Згенерована розмітка HTML може бути змінена.

### Дивіться також

-   [highlightfile()](function.highlight-file.md) - Підсвічування синтаксису файлу
-   [Подсветка директив INI](misc.configuration.html#ini.syntax-highlighting)

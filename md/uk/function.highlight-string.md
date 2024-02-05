---
navigation:
  - function.highlight-file.md: « highlight\_file
  - function.hrtime.md: hrtime »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: highlight\_string
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# highlight\_string

(PHP 4, PHP 5, PHP 7, PHP 8)

highlight\_string — Підсвічує синтаксис рядка

### Опис

```methodsynopsis
highlight_string(string $string, bool $return = false): string|bool
```

Виводить або повертає HTML-розмітку для версії з підсвічуванням синтаксису PHP-коду, застосовуючи кольори, визначені у вбудованому обробнику підсвічування синтаксису PHP.

### Список параметрів

`string`

PHP-код, який потрібно підсвітити. Код повинен включати тег, що відкриває.

`return`

Параметру устанавливают значение\*\*`true`\*\*, щоб функція повертала підсвічений код.

### Значення, що повертаються

Якщо параметр `return`равен\*\*`true`\*\*, замість виведення у вигляді рядка повертається код з підсвічуванням синтаксису. В іншому випадку повертає \*\*`true`** або **`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Змінився результуючий HTML. |

### Приклади

**Приклад #1 Приклад використання функції** highlight\_string()\*\*\*\*

```php
<?php

highlight_string('<?php phpinfo(); ?>');

?>
```

Результат виконання наведеного прикладу:

```
<code><span style="color: #000000">
<span style="color: #0000BB">&lt;?php phpinfo</span><span style="color: #007700">(); </span><span style="color: #0000BB">?&gt;</span>
</span>
</code>
```

Результат виконання наведеного прикладу в PHP 8.3:

```
<pre><code style="color: #000000"><span style="color: #0000BB">&lt;?php phpinfo</span><span style="color: #007700">(); </span><span style="color: #0000BB">?&gt;</span></code></pre>
```

### Примітки

> **Зауваження** :
> 
> Оскільки в сигнатурі функції є параметр `return`, вона буде використовувати внутрішню буферизацію виводу, тому цю функцію не можна вказувати як callback-функції при виклику функції [ob\_start()](function.ob-start.md)

У майбутньому можлива зміна згенерованої HTML-розмітки.

### Дивіться також

-   [highlight\_file()](function.highlight-file.md) \- Підсвічує синтаксис файлу
-   [Підсвічування директив INI](misc.configuration.md#ini.syntax-highlighting)

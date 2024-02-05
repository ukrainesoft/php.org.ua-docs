---
navigation:
  - function.ob-list-handlers.md: « ob\_list\_handlers
  - function.output-add-rewrite-var.md: output\_add\_rewrite\_var »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: ob\_start
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ob\_start

(PHP 4, PHP 5, PHP 7, PHP 8)

ob\_start — Вмикає буферизацію виводу

### Опис

```methodsynopsis
ob_start(callable $callback = null, int $chunk_size = 0, int $flags = PHP_OUTPUT_HANDLER_STDFLAGS): bool
```

Функція включає буферизацію виведення. Поки буферизація виводу активна, виведення зі скрипту не відправляється, натомість висновок зберігається у внутрішньому буфері. В розділі " [Який висновок буферизується?](outcontrol.what-output-is-buffered.md) » розказано, який саме висновок це впливає.

Буфери виведення поміщаються у стек, тому функцію **ob\_start()** можна викликати, поки активний інший буфер. Якщо активовано кілька буферів виведення, висновок фільтрується послідовно через кожен із них у порядку вкладеності. Докладніше про це розказано у розділі «[Вкладені буфери виводу](outcontrol.nesting-output-buffers.md)».

Детальний опис буферів виводу наведено в розділі [Буфери виводу користувача](outcontrol.user-level-output-buffers.md)

### Список параметрів

`callback`

Можна вказати необов'язковий параметр `callback` [callable](language.types.callable.md)). Щоб обійти його, передають значення **`null`**

Параметр`callback` викликається, коли буфер виведення скидається (відправляється), очищається або коли буфер виведення скидається наприкінці скрипта.

Сигнатура`callback`\-функції:

```methodsynopsis
handler(string $buffer, int $phase = ?): string
```

`buffer`

Вміст буфера виводу.

`phase`

Битовая маска из семейства констант[**`PHP_OUTPUT_HANDLER_*`**](outcontrol.constants.md#constant.php-output-handler-start) . Докладніше про прапори розказано у розділі «[Прапори, що передаються обробникам виводу](outcontrol.flags-passed-to-output-handlers.md)».

Якщо параметр `callback` поверне \*\*`false`\*\*повертається вміст буфера. Докладніше про це розказано у розділі «[Значення оброблювача виводу, що повертаються](outcontrol.output-handler-return-values.md)».

**Увага**

Виклик будь-якої з наведених нижче функцій з обробника висновку видасть фатальну помилку: [ob\_clean()](function.ob-clean.md) [ob\_end\_clean()](function.ob-end-clean.md) [ob\_end\_flush()](function.ob-end-flush.md) [ob\_flush()](function.ob-flush.md) [ob\_get\_clean()](function.ob-get-clean.md) [ob\_get\_flush()](function.ob-get-flush.md) **ob\_start()**

Подробнее о`callback`\-функціях (обробників висновку) розказано в розділах « [Обробники виводу](outcontrol.output-handlers.md) » та «[Робота з оброблювачами виводу](outcontrol.working-with-output-handlers.md)».

`chunk_size`

Якщо передано необов'язковий параметр `chunk_size`, буфер буде скинутий після кожного блоку коду, розмір буфера якого досяг або перевищив значення параметра `chunk_size`Значение по умолчанию означає, що висновок буферизується до тих пір, поки буфер не буде вимкнений. Докладніше про це розказано у розділі «[Розмір буфера](outcontrol.buffer-size.md)».

`flags`

Параметр`flags` - Це бітова маска, яка управляє операціями, що виконуються з буфером виведення. За замовчуванням дозволено очищення, скидання та видалення буферів виводу, що дозволено встановлювати явно через [прапори керування буфером](outcontrol.constants.md#outcontrol.constants.buffer-control-flags) . Докладніше про це розказано у розділі « [Операції, дозволені для буферів](outcontrol.operations-on-buffers.md) ».

Кожен прапор управляє доступом до набору функцій, як описано нижче:

| Константа | Функции |
| --- | --- |
| **`PHP_OUTPUT_HANDLER_CLEANABLE`** | [ob\_clean()](function.ob-clean.md) |
| **`PHP_OUTPUT_HANDLER_FLUSHABLE`** | [ob\_end\_flush()](function.ob-end-flush.md) |
| **`PHP_OUTPUT_HANDLER_REMOVABLE`** | [ob\_end\_clean()](function.ob-end-clean.md) [ob\_end\_flush()](function.ob-end-flush.md) [ob\_get\_clean()](function.ob-get-clean.md) [ob\_get\_flush()](function.ob-get-flush.md) |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад callback-функції, визначеної користувачем**

```php
<?php

function callback($buffer)
{
  // заменить все яблоки апельсинами
  return (str_replace("яблоки", "апельсины", $buffer));
}

ob_start("callback");

?>
<html>
<body>
<p>Это всё равно что сравнить яблоки и апельсины.</p>
</body>
</html>
<?php

ob_end_flush();

?>
```

Результат виконання наведеного прикладу:

```
<html>
<body>
<p>Это всё равно что сравнить апельсины и апельсины.</p>
</body>
</html>
```

**Приклад #2 Створення буфера виводу, що не стирається.**

```php
<?php

ob_start(null, 0, PHP_OUTPUT_HANDLER_STDFLAGS ^ PHP_OUTPUT_HANDLER_REMOVABLE);

?>
```

### Дивіться також

-   [ob\_get\_contents()](function.ob-get-contents.md) \- Повертає вміст буфера виводу
-   [ob\_end\_clean()](function.ob-end-clean.md) \- Очищає (стирає) вміст активного буфера виведення та відключає його
-   [ob\_end\_flush()](function.ob-end-flush.md) \- Скидає (відправляє) значення активного оброблювача виводу, що повертається, і відключає активний буфер виводу
-   [ob\_implicit\_flush()](function.ob-implicit-flush.md) \- Вмикає/вимикає неявне скидання
-   [ob\_gzhandler()](function.ob-gzhandler.md) \- Стискає буфер виведення в gzip, діючи як callback-функція - параметр функції ob\_start
-   [ob\_iconv\_handler()](function.ob-iconv-handler.md) \- Перетворює символи з поточного кодування на кодування вихідного буфера
-   [mb\_output\_handler()](function.mb-output-handler.md) \- Перетворює кодування символів у буфері виведення, виступаючи в ролі callback-функції
-   [ob\_tidyhandler()](function.ob-tidyhandler.md) \- Функція зворотного виклику ob\_start для відновлення буфера

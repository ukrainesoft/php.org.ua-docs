---
navigation:
  - function.ob-get-contents.md: « obgetcontents
  - function.ob-get-length.md: проgetlength »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: проgetflush
---
# проgetflush

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

проgetflush — Скинути буфер виводу, повернути його у вигляді рядка та вимкнути буферизацію виводу

### Опис

```methodsynopsis
ob_get_flush(): string|false
```

**проgetflush()** скидає буфер виведення, повертаючи його вміст у вигляді рядка та відключає буферизацію виведення.

Буфер виводу має запускатися функцією [проstart()](function.ob-start.md) з прапором [PHPOUTPUTHANDLERFLUSHABLE](outcontrol.constants.md#constant.php-output-handler-flushable). Інакше не спрацює **проgetflush()**

> **Зауваження**: Ця функція аналогічна [проendflush()](function.ob-end-flush.md) крім того, що ця функція також повертає буфер у вигляді рядка.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає буфер виводу або \*\*`false`\*\*якщо буферизація не активна.

### Приклади

**Приклад #1 Приклад використання функції **проgetflush()****

```php
<?php
//Используется output_buffering=On
print_r(ob_list_handlers());

//сохранить буфер в файл
$buffer = ob_get_flush();
file_put_contents('buffer.txt', $buffer);

print_r(ob_list_handlers());
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => default output handler
)
Array
(
)
```

### Дивіться також

-   [проendclean()](function.ob-end-clean.md) - Очистити (стерти) буфер виводу та вимкнути буферизацію виводу
-   [проendflush()](function.ob-end-flush.md) - Скинути (відправити) буфер виведення та вимкнути буферизацію виводу
-   [проlisthandlers()](function.ob-list-handlers.md) - Список всіх використовуваних обробників виводу

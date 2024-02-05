---
navigation:
  - function.ob-get-level.md: « ob\_get\_level
  - function.ob-implicit-flush.md: ob\_implicit\_flush »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: ob\_get\_status
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ob\_get\_status

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

ob\_get\_status — Отримує статус буфера виводу

### Опис

```methodsynopsis
ob_get_status(bool $full_status = false): array
```

Функция**ob\_get\_status()** повертає інформацію про стан буфера верхнього рівня або на всіх рівнях активних буферів, якщо параметр `full_status`установлен в\*\*`true`\*\*

### Список параметрів

`full_status`

Якщо \*\*`true`\*\*то поверне всі рівні активних буферів. Якщо **`false`** або не встановлений, то поверне статус лише найвищого рівня.

### Значення, що повертаються

Якщо параметр `full_status` опущений або дорівнює **`false`**, Повертає простий масив з інформацією про статус активного рівня виведення.

Якщо параметр `full_status`равен\*\*`true`\*\*, повертає масив з одним елементом кожного активного рівня буфера виведення. Рівень виведення буде вказано як ключ верхнього рівня масиву, і кожен елемент масиву сам буде іншим масивом з інформацією про статус активного рівня виведення.

Повертає порожній масив, якщо буферизація виводу була включена.

**Елементи масиву, які повертає функція **ob\_get\_status()****

| Key | Value |
| --- | --- |
| name | Ім'я активного обробника висновку (докладніше про це розказано в описі значень функції, що повертаються) [ob\_list\_handlers()](function.ob-list-handlers.md) |
| type | (внутрішній обробник) або (наданий користувачем обробник) |
| flags | Бітова маска прапорів, заданих у функції [ob\_start()](function.ob-start.md), тип обробника виведення (див. вище) та статус процесу буферизації (константи [**`PHP_OUTPUT_HANDLER_*`**](outcontrol.constants.md#outcontrol.constants.flags-returned-by-handler) ). Якщо обробник успішно обробив буфер і не повернув **`false`**, будуть встановлені значення констант **`PHP_OUTPUT_HANDLER_STARTED`**и**`PHP_OUTPUT_HANDLER_PROCESSED`**. . Якщо обробник не зміг обробити буфер або повернув **`false`**, будуть встановлені значення констант **`PHP_OUTPUT_HANDLER_STARTED`**и**`PHP_OUTPUT_HANDLER_DISABLED`** |
| level | Рівень вкладеності виводу (починається з нуля). Зауважте, що значення, яке повертається функцією [ob\_get\_level()](function.ob-get-level.md) для того ж рівня більше на одиницю. Перший рівень для функції **ob\_get\_status()** - це , а для функції [ob\_get\_level()](function.ob-get-level.md) - це |
| chunk\_size | Розмір частини у байтах. Значення, встановлене у функції [ob\_start()](function.ob-start.md), або значення налаштування [output\_buffering](outcontrol.configuration.md#ini.output-buffering)якщо вона включена і її значення встановлено як ціле позитивне число. |
| buffer\_size | Розмір буфера виведення у байтах. |
| buffer\_used | Розмір даних буфера виведення в байтах (те ж, що і функцією, що повертається [ob\_get\_length()](function.ob-get-length.md) ціле значення). |

### Приклади

**Приклад #1 Масив, який буде повернутий, якщо значення параметра `full_status` одно **`false`****

Array (\[name\] => URL-Rewriter \[type\] => 0 \[flags\] => 112 \[level\] => 2 \[chunk\_size\] => 0 \[buffer\_size\] => 16384 \[buffer\_used\] => 1024 )

**Приклад #2 Масив, який буде повернутий, якщо значення параметра `full_status` одно **`true`****

Array (\[ \] => Array ( \[name\] => default output handler \[type\] => 0 \[flags\] => 112 \[level\] => 1 \[chunk\_size\] => 0 \[buffer\_size\] => 16384 \[buffer\_used\] => 2048 )

```
\[1\] => Array
    (
        \[name\] => URL-Rewriter
        \[type\] => 0
        \[flags\] => 112
        \[level\] => 2
        \[chunk\_size\] => 0
        \[buffer\_size\] => 16384
        \[buffer\_used\] => 1024
    )
```

) .

### Дивіться також

-   [ob\_get\_level()](function.ob-get-level.md) \- Повертає рівень вкладеності механізму буферизації виводу
-   [ob\_list\_handlers()](function.ob-list-handlers.md) \- Повертає список активних обробників виводу
-   [ob\_get\_length()](function.ob-get-length.md) \- Повертає розмір буфера виводу
-   [ob\_start()](function.ob-start.md) \- Включає буферизацію виводу

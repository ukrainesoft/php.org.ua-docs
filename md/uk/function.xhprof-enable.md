---
navigation:
  - function.xhprof-disable.md: « xhprof\_disable
  - function.xhprof-sample-disable.md: xhprof\_sample\_disable »
  - index.md: PHP Manual
  - ref.xhprof.md: Функції Xhprof
title: xhprof\_enable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xhprof\_enable

(PECL xhprof >= 0.9.0)

xhprof\_enable — Запуск профілювання xhprof

### Опис

```methodsynopsis
xhprof_enable(int $flags = 0, array $options = ?): void
```

Запускає профіль.

### Список параметрів

`flags`

Необов'язкові прапори для отримання додаткової інформації для профілювання. Подробиці можна знайти у розділі [Константи XHprof](xhprof.constants.md)Например,\*\*`XHPROF_FLAGS_MEMORY`\*\*включает профилирование памяти.

`options`

Масив (array) необов'язкових опцій, саме опція 'ignored\_functions' зі списком функцій, які не потрібно профілювати.

### Значення, що повертаються

**`null`**

### список змін

| Версия | Опис |
| --- | --- |
| PECL xhprof 0.9.2 | Додано необов'язковий параметр `options` |

### Приклади

**Пример #1 Пример использования**xhprof\_enable()\*\*\*\*

```php
<?php
// 1. время исполнения + память + CPU; также игнорируем функции стандартной библиотеки
xhprof_enable(XHPROF_FLAGS_NO_BUILTINS | XHPROF_FLAGS_CPU | XHPROF_FLAGS_MEMORY);

// 2. время исполнения; игнорируем при профилировании call_user_func*
xhprof_enable(
    0,
    array('ignored_functions' =>  array('call_user_func',
                                        'call_user_func_array')));

// 3. время исполнения + память; игнорируем при профилировании call_user_func*
xhprof_enable(
    XHPROF_FLAGS_MEMORY,
    array('ignored_functions' =>  array('call_user_func',
                                        'call_user_func_array')));
?>
```

### Дивіться також

-   [xhprof\_disable()](function.xhprof-disable.md) \- Зупиняє профіль xhprof
-   [xhprof\_sample\_enable()](function.xhprof-sample-enable.md) \- Запуск семплюючого режиму профілювання XHProf
-   [memory\_get\_usage()](function.memory-get-usage.md) \- Повертає кількість пам'яті, виділеної для PHP
-   [getrusage()](function.getrusage.md) \- Отримує інформацію про використання поточного ресурсу

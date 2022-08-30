Запуск профілювання xhprof

-   [« xhprofdisable](function.xhprof-disable.html)
    
-   [xhprofsampledisable »](function.xhprof-sample-disable.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Xhprof](ref.xhprof.html)
    
-   Запуск профілювання xhprof
    

# xhprofenable

(PECL xhprof >= 0.9.0)

xhprofenable — Запуск профілювання xhprof

### Опис

```methodsynopsis
xhprof_enable(int $flags = 0, array $options = ?): void
```

Запускає профіль.

### Список параметрів

`flags`

Необов'язкові прапори для отримання додаткової інформації для профілювання. Подробиці можна знайти у розділі [Константы XHprof](xhprof.constants.html). Наприклад, **`XHPROF_FLAGS_MEMORY`** включає профіль пам'яті.

`options`

Масив (array) необов'язкових опцій, саме опція 'ignoredfunctions' зі списком функцій, які не потрібно профілювати.

### Значення, що повертаються

**`null`**

### список змін

| Версия            | Описание                                 |
|-------------------|------------------------------------------|
| PECL xhprof 0.9.2 | Додано необов'язковий параметр `options` |

### Приклади

**Приклад #1 Приклад використання **xhprofenable()****

```php
<?php
// 1. время исполнения + память + CPU; также игнорируем функции стандартной библиотеки
xhprof_enable(XHPROF_FLAGS_NO_BUILTINS | XHPROF_FLAGS_CPU | XHPROF_FLAGS_MEMORY);

// 2. время исполнения; игнорируем при профилировании call_user_func*
xhprof_enable(
    0,
    array('ignored_functions' =>  array('call_user_func',
                                        'call_user_func_array')));

// 3. время исполнения + память; игнорируем при профилировании call_user_func*
xhprof_enable(
    XHPROF_FLAGS_MEMORY,
    array('ignored_functions' =>  array('call_user_func',
                                        'call_user_func_array')));
?>
```

### Дивіться також

-   [xhprofdisable()](function.xhprof-disable.html) - Зупиняє профіль xhprof
-   [xhprofsampleenable()](function.xhprof-sample-enable.html) - Запуск семплюючого режиму профілювання XHProf
-   [memorygetusage()](function.memory-get-usage.html) - Повертає кількість пам'яті, виділену для PHP
-   [getrusage()](function.getrusage.html) - Отримує інформацію про використання поточного ресурсу
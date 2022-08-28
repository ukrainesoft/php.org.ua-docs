Повертає логічне значення змінної

-   [« Функции для работы с переменными](ref.var.html)
    
-   [debug\_zval\_dump »](function.debug-zval-dump.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с переменными](ref.var.html)
    
-   Повертає логічне значення змінної
    

# boolval

(PHP 5> = 5.5.0, PHP 7, PHP 8)

boolval - Повертає логічне значення змінної

### Опис

```methodsynopsis
boolval(mixed $value): bool
```

Повертає значення типу bool, релевантне переданому значенню `value`

### Список параметрів

`value`

Скалярне значення, яке слід привести до типу bool.

### Значення, що повертаються

Приведене до типу bool значення `value`

### Приклади

**Приклад #1 Приклад використання **boolval()****

```php
<?php
echo '0:        '.(boolval(0) ? 'true' : 'false')."\n";
echo '42:       '.(boolval(42) ? 'true' : 'false')."\n";
echo '0.0:      '.(boolval(0.0) ? 'true' : 'false')."\n";
echo '4.2:      '.(boolval(4.2) ? 'true' : 'false')."\n";
echo '"":       '.(boolval("") ? 'true' : 'false')."\n";
echo '"string": '.(boolval("string") ? 'true' : 'false')."\n";
echo '"0":      '.(boolval("0") ? 'true' : 'false')."\n";
echo '"1":      '.(boolval("1") ? 'true' : 'false')."\n";
echo '[1, 2]:   '.(boolval([1, 2]) ? 'true' : 'false')."\n";
echo '[]:       '.(boolval([]) ? 'true' : 'false')."\n";
echo 'stdClass: '.(boolval(new stdClass) ? 'true' : 'false')."\n";
?>
```

Результат виконання цього прикладу:

```
0:        false
42:       true
0.0:      false
4.2:      true
"":       false
"string": true
"0":      false
"1":      true
[1, 2]:   true
[]:       false
stdClass: true
```

### Дивіться також

-   [floatval()](function.floatval.html) - Повертає значення змінної у вигляді числа з плаваючою точкою
-   [intval()](function.intval.html) - Повертає ціле значення змінної
-   [strval()](function.strval.html) - Повертає строкове значення змінної
-   [settype()](function.settype.html) - Задає тип змінної
-   [is\_bool()](function.is-bool.html) - Перевіряє, чи є змінна булевою
-   [Преобразование типов](language.types.type-juggling.html)
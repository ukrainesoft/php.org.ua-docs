---
navigation:
  - ffi.examples.md: « Приклади
  - ffi.examples-callback.md: Callback-функции PHP »
  - index.md: PHP Manual
  - ffi.examples.md: Приклади
title: Прості приклади використання FFI
---
## Прості приклади використання FFI

Перед зануренням у деталі FFI API, розгляньмо кілька прикладів спрощеного використання FFI API у стандартних завданнях.

> **Зауваження**
> 
> Для деяких прикладів знадобиться бібліотека libc.so.6. Вони не працюватимуть у системах, де її немає.

**Приклад #1 Виклик функції загальної бібліотеки**

```php
<?php
// создаём объект FFI, загружаем libc и экспортируем функцию printf()
$ffi = FFI::cdef(
    "int printf(const char *format, ...);", // это стандартная декларация C
    "libc.so.6");
// вызываем printf()
$ffi->printf("Привет, %s!\n", "мир");
?>
```

Результат виконання цього прикладу:

```
Привет, мир!
```

> **Зауваження**
> 
> Зверніть увагу, що деякі функції C потребують певних угод про виклики, наприклад: `__fastcall` `__stdcall` або `,__vectorcall`

**Приклад #2 Виклик функції та повернення структури через аргумент**

```php
<?php
// создаём привязку gettimeofday()
$ffi = FFI::cdef("
    typedef unsigned int time_t;
    typedef unsigned int suseconds_t;

    struct timeval {
        time_t      tv_sec;
        suseconds_t tv_usec;
    };

    struct timezone {
        int tz_minuteswest;
        int tz_dsttime;
    };

    int gettimeofday(struct timeval *tv, struct timezone *tz);
", "libc.so.6");
// создаём структуры данных C
$tv = $ffi->new("struct timeval");
$tz = $ffi->new("struct timezone");
// вызываем gettimeofday()
var_dump($ffi->gettimeofday(FFI::addr($tv), FFI::addr($tz)));
// получаем доступ к полю структуры данных C
var_dump($tv->tv_sec);
// печатаем всю структуру данных
var_dump($tz);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(0)
int(1555946835)
object(FFI\CData:struct timezone)#3 (2) {
  ["tz_minuteswest"]=>
  int(0)
  ["tz_dsttime"]=>
  int(0)
}
```

**Приклад #3 Доступ до існуючих змінних C**

```php
<?php
// создаём объект FFI, загружаем libc и экспортируем переменную errno
$ffi = FFI::cdef(
    "int errno;", // это стандартная декларация C
    "libc.so.6");
// печатаем errno
var_dump($ffi->errno);
?>
```

Результат виконання цього прикладу:

```
int(0)
```

**Приклад #4 Створення та модифікація змінної C**

```php
<?php
// создаём переменную C типа int
$x = FFI::new("int");
var_dump($x->cdata);

// простое присваивание
$x->cdata = 5;
var_dump($x->cdata);

// не простое присвоение
$x->cdata += 2;
var_dump($x->cdata);
?>
```

Результат виконання цього прикладу:

```
int(0)
int(5)
int(7)
```

**Приклад #5 Робота з масивами C**

```php
<?php
// создаём структуру данных
$a = FFI::new("long[1024]");
// работаем с ней как с обычным Масивом PHP
for ($i = 0; $i < count($a); $i++) {
    $a[$i] = $i;
}
var_dump($a[25]);
$sum = 0;
foreach ($a as $n) {
    $sum += $n;
}
var_dump($sum);
var_dump(count($a));
var_dump(FFI::sizeof($a));
?>
```

Результат виконання цього прикладу:

```
int(25)
int(523776)
int(1024)
int(8192)
```

**Приклад #6 Робота з переліками C**

```php
<?php
$a = FFI::cdef('typedef enum _zend_ffi_symbol_kind {
    ZEND_FFI_SYM_TYPE,
    ZEND_FFI_SYM_CONST = 2,
    ZEND_FFI_SYM_VAR,
    ZEND_FFI_SYM_FUNC
} zend_ffi_symbol_kind;
');
var_dump($a->ZEND_FFI_SYM_TYPE);
var_dump($a->ZEND_FFI_SYM_CONST);
var_dump($a->ZEND_FFI_SYM_VAR);
?>
```

Результат виконання цього прикладу:

```
int(0)
int(2)
int(3)
```

---
navigation:
  - function.ob-implicit-flush.md: « ob\_implicit\_flush
  - function.ob-start.md: ob\_start »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: ob\_list\_handlers
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ob\_list\_handlers

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

ob\_list\_handlers — Повертає список активних обробників виводу

### Опис

```methodsynopsis
ob_list_handlers(): array
```

Виводить список активних обробників виводу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив зі списком активних обробників виводу, якщо є.

Повертає рядок `"default output handler"`, якщо налаштування [output\_buffering](outcontrol.configuration.md#ini.output-buffering) увімкнено та налаштування [output\_handler](outcontrol.configuration.md#ini.output-handler) не встановлено, або у функцію [ob\_start()](function.ob-start.md) не передана callback-функція або замість неї передано значення \*\*`null`\*\*Включение настройки[output\_buffering](outcontrol.configuration.md#ini.output-buffering)и установка значения для настройки[output\_handler](outcontrol.configuration.md#ini.output-handler) еквівалентно передачі у функцію [ob\_start()](function.ob-start.md) [внутрішньої (вбудованої) функції](functions.internal.md)

Повертає [абсолютне ім'я](language.namespaces.basics.md)переданной в параметр[callable](language.types.callable.md) функції, якщо параметр [callable](language.types.callable.md) функції [ob\_start()](function.ob-start.md) була передана callback-функція. Повертає [абсолютне ім'я](language.namespaces.basics.md) об'єкта з методом [\_\_invoke()](language.oop5.magic.md#language.oop5.magic.invoke), якщо параметр [callable](language.types.callable.md) - це об'єкт, який реалізує метод [\_\_invoke()](language.oop5.magic.md#language.oop5.magic.invoke). Повертає рядок `"Closure::__invoke"`, якщо параметр [callable](language.types.callable.md) - це об'єкт класу [Closure](class.closure.md)

### Приклади

**Пример #1 Пример использования функции**ob\_list\_handlers()\*\*\*\*

```php
<?php
// настройка включена output_buffering=On, значение для настройки output_handler не установлено
var_dump(ob_list_handlers());
ob_end_flush();

// callback-функция не передана или null
ob_start();
var_dump(ob_list_handlers());
ob_end_flush();

// анонимная функция
ob_start(function($string) { return $string; });
var_dump(ob_list_handlers());
ob_end_flush();

// стрелочная функция
ob_start(fn($string) => $string);
var_dump(ob_list_handlers());
ob_end_flush();

// callback-функция как объект первого класса
$firstClassCallable = userDefinedFunction(...);

ob_start([$firstClassCallable, '__invoke']);
var_dump(ob_list_handlers());
ob_end_flush();

// внутренняя (встроенная функция)
ob_start('print_r');
var_dump(ob_list_handlers());
ob_end_flush();

// пользовательская функция
function userDefinedFunction($string, $flags) { return $string; };

ob_start('userDefinedFunction');
var_dump(ob_list_handlers());
ob_end_flush();

class MyClass {
    public static function staticHandle($string) {
        return $string;
    }

    public static function handle($string) {
        return $string;
    }

    public function __invoke($string) {
        return $string;
    }
}

// класс и статический метод
ob_start(['MyClass','staticHandle']);
var_dump(ob_list_handlers());
ob_end_flush();

// объект и нестатический метод
ob_start([new MyClass,'handle']);
var_dump(ob_list_handlers());
ob_end_flush();

// объект вызываемого класса
ob_start(new MyClass);
var_dump(ob_list_handlers());
ob_end_flush();
?>
```

Результат виконання наведеного прикладу:

```
array(1) {
  [0]=>
  string(22) "default output handler"
}
array(1) {
  [0]=>
  string(22) "default output handler"
}
array(1) {
  [0]=>
  string(7) "print_r"
}
array(1) {
  [0]=>
  string(19) "userDefinedFunction"
}
array(1) {
  [0]=>
  string(17) "Closure::__invoke"
}
array(1) {
  [0]=>
  string(17) "Closure::__invoke"
}
array(1) {
  [0]=>
  string(17) "Closure::__invoke"
}
array(1) {
  [0]=>
  string(21) "MyClass::staticHandle"
}
array(1) {
  [0]=>
  string(15) "MyClass::handle"
}
array(1) {
  [0]=>
  string(17) "MyClass::__invoke"
}
```

### Дивіться також

-   [ob\_end\_clean()](function.ob-end-clean.md) \- Очищає (стирає) вміст активного буфера виведення та відключає його
-   [ob\_end\_flush()](function.ob-end-flush.md) \- Скидає (відправляє) значення активного оброблювача виводу, що повертається, і відключає активний буфер виводу
-   [ob\_get\_flush()](function.ob-get-flush.md) \- Скидає (відправляє) повернене активним обробником виводу значення, повертає вміст активного буфера виводу та відключає його
-   [ob\_start()](function.ob-start.md) \- Включає буферизацію виводу

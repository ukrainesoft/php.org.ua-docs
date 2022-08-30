Повертає масив усіх певних змінних

-   [« getdebugtype](function.get-debug-type.html)
    
-   [getresourceid »](function.get-resource-id.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи зі змінними](ref.var.html)
    
-   Повертає масив усіх певних змінних
    

# getdefinedvars

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

getdefinedvars - Повертає масив усіх певних змінних

### Опис

```methodsynopsis
get_defined_vars(): array
```

Ця функція повертає багатовимірний масив, що містить список всіх певних змінних, будь то змінні оточення, серверні змінні або змінні, визначені користувачем, в області видимості, в якій була викликана **getdefinedvars()**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Багатовимірний масив з усіма змінними.

### Приклади

**Приклад #1 Приклад використання **getdefinedvars()****

```php
<?php
$b = array(1, 1, 2, 3, 5, 8);

$arr = get_defined_vars();

// печатает $b
print_r($arr["b"]);

/* печатает путь до интерпретатора PHP (при использовании режима CGI)
 * например, /usr/local/bin/php */
echo $arr["_"];

// печатает параметры командной строки, если они есть
print_r($arr["argv"]);

// печатает все серверные переменные
print_r($arr["_SERVER"]);

// печатает все доступные ключи для массивов переменных
print_r(array_keys(get_defined_vars()));
?>
```

### Дивіться також

-   [isset()](function.isset.html) - Визначає, чи була встановлена ​​змінна значенням, відмінним від null
-   [getdefinedfunctions()](function.get-defined-functions.html) - Повертає масив усіх певних функцій
-   [getdefinedconstants()](function.get-defined-constants.html) - Повертає асоціативний масив з іменами всіх констант та їх значень
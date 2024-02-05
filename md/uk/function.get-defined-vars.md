---
navigation:
  - function.get-debug-type.md: « get\_debug\_type
  - function.get-resource-id.md: get\_resource\_id »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: get\_defined\_vars
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_defined\_vars

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

get\_defined\_vars - Повертає масив усіх певних змінних

### Опис

```methodsynopsis
get_defined_vars(): array
```

Ця функція повертає багатовимірний масив, що містить список всіх певних змінних, будь то змінні оточення, серверні змінні або змінні, визначені користувачем, в області видимості, в якій була викликана **get\_defined\_vars()**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Багатовимірний масив з усіма змінними.

### Приклади

**Пример #1 Пример использования**get\_defined\_vars()\*\*\*\*

```php
<?php
$b = array(1, 1, 2, 3, 5, 8);

$arr = get_defined_vars();

// печатает $b
print_r($arr["b"]);

/* печатает путь до интерпретатора PHP (при использовании режима CGI)
 * например, /usr/local/bin/php */
echo $arr["_"];

// печатает параметры командной строки, если они есть
print_r($arr["argv"]);

// печатает все серверные переменные
print_r($arr["_SERVER"]);

// печатает все доступные ключи для массивов переменных
print_r(array_keys(get_defined_vars()));
?>
```

### Дивіться також

-   [isset()](function.isset.md) \- Визначає, чи була встановлена ​​змінна значенням, відмінним від null
-   [get\_defined\_functions()](function.get-defined-functions.md) \- Повертає масив усіх певних функцій
-   [get\_defined\_constants()](function.get-defined-constants.md) \- Повертає асоціативний масив з іменами всіх констант та їх значень

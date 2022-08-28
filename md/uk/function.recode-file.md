Перекодує з одного файла до іншого відповідно до заданих параметрів

-   [« Функции Recode](ref.recode.html)
    
-   [recode\_string »](function.recode-string.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Recode](ref.recode.html)
    
-   Перекодує з одного файла до іншого відповідно до заданих параметрів
    

# recodefile

(PHP 4, PHP 5, PHP 7 < 7.4.0)

recodefile — Перекодування з одного файлу до іншого відповідно до заданих параметрів

### Опис

```methodsynopsis
recode_file(string $request, resource $input, resource $output): bool
```

Перекодує файл, заданий дескриптором `input` у файл, заданий дескриптором `output` відповідно до `request`

### Список параметрів

`request`

Вибраний тип запиту на перекодування

`input`

Локальний файловий ресурс (Resource) `input`

`output`

Локальний файловий ресурс (Resource) `output`

### Значення, що повертаються

Повертає **`false`**, якщо виникли якісь труднощі або **`true`** у разі успішного виконання.

### Приклади

**Приклад #1 Приклад використання **recodefile()****

```php
<?php
$input = fopen('input.txt', 'r');
$output = fopen('output.txt', 'w');
recode_file("us..flat", $input, $output);
?>
```

### Примітки

На даний момент ця функція не працює з дескрипторами, що посилаються на віддалені файли (URL). Обидва файлові дескриптори повинні вказувати на локальні файли.

### Дивіться також

-   [fopen()](function.fopen.html) - Відкриває файл або URL
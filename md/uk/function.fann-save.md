Зберігає всю мережу файл конфігурації

-   [« fann\_save\_train](function.fann-save-train.html)
    
-   [fann\_scale\_input\_train\_data »](function.fann-scale-input-train-data.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Зберігає всю мережу файл конфігурації
    

# fannsave

(PECL fann> = 1.0.0)

fannsave — Зберігає всю мережу у конфігураційному файлі

### Опис

```methodsynopsis
fann_save(resource $ann, string $configuration_file): bool
```

Зберігає всю мережу файл конфігурації.

Файл конфігурації містить всю інформацію про нейронну мережу і дозволяє функції [fann\_create\_from\_file()](function.fann-create-from-file.html) створювати точну копію нейронної мережі та всіх параметрів, пов'язаних з нейронною мережею.

Три параметри ([fann\_set\_callback()](function.fann-set-callback.html) [fann\_set\_error\_log()](function.fann-set-error-log.html) **fannsetuserdata()**) НЕ зберігаються у файл, тому що їх не можна безпечно перенести в інше місце. Також не зберігаються часові параметри, згенеровані під час навчання, такі як [fann\_get\_MSE()](function.fann-get-mse.html)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`configuration_file`

Шлях до конфігураційного файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_create\_from\_file()](function.fann-create-from-file.html) - Створює нейронну мережу зі зворотним поширенням помилки з конфігураційного файлу
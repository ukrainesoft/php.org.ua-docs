Створює нейронну мережу зі зворотним поширенням помилки конфігураційного файлу

-   [« fann\_copy](function.fann-copy.html)
    
-   [fann\_create\_shortcut\_array »](function.fann-create-shortcut-array.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Створює нейронну мережу зі зворотним поширенням помилки конфігураційного файлу
    

# fanncreatefromfile

(PECL fann> = 1.0.0)

fanncreatefromfile — Створює нейронну мережу із зворотним розповсюдженням помилки з конфігураційного файлу

### Опис

```methodsynopsis
fann_create_from_file(string $configuration_file): resource
```

Створює нейронну мережу зі зворотним поширенням помилки з конфігураційного файлу, створеного раніше за допомогою [fann\_save()](function.fann-save.html)

### Список параметрів

`configuration_file`

Конфігураційний файл.

### Значення, що повертаються

Повертає ресурс (resource) нейронної мережі у разі успішного виконання, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_save()](function.fann-save.html) - Зберігає всю мережу файл конфігурації
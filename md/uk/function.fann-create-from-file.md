Створює нейронну мережу зі зворотним поширенням помилки конфігураційного файлу

-   [« fanncopy](function.fann-copy.html)
    
-   [fanncreateshortcutarray »](function.fann-create-shortcut-array.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
-   Створює нейронну мережу зі зворотним поширенням помилки конфігураційного файлу
    

# fanncreatefromfile

(PECL fann> = 1.0.0)

fanncreatefromfile — Створює нейронну мережу із зворотним розповсюдженням помилки з конфігураційного файлу

### Опис

```methodsynopsis
fann_create_from_file(string $configuration_file): resource
```

Створює нейронну мережу зі зворотним поширенням помилки з конфігураційного файлу, створеного раніше за допомогою [fannsave()](function.fann-save.html)

### Список параметрів

`configuration_file`

Конфігураційний файл.

### Значення, що повертаються

Повертає ресурс (resource) нейронної мережі у разі успішного виконання, або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsave()](function.fann-save.html) - Зберігає всю мережу файл конфігурації
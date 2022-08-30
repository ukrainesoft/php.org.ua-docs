Читає файл, у якому зберігаються дані навчання

-   [« fannrandomizeweights](function.fann-randomize-weights.html)
    
-   [fannreseterrno »](function.fann-reset-errno.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Читає файл, у якому зберігаються дані навчання
    

# fannreadtrainfromfile

(PECL fann> = 1.0.0)

fannreadtrainfromfile — Читає файл, у якому зберігаються дані навчання

### Опис

```methodsynopsis
fann_read_train_from_file(string $filename): resource
```

Читає файл, де зберігаються дані навчання.

### Список параметрів

`filename`

Вхідний файл у наступному форматі:

numtraindata numinput numoutput вхідні дані, розділені пропуском вихідні дані, розділені пропуском

вхідні дані, розділені пропуском вихідні дані, розділені пропуском

### Значення, що повертаються

Повертає ресурс (resource) навчальних даних, або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **fannreadtrainfromfile()****

```php
<?php
$train_data = fann_read_train_from_file("xor.data");
if ($train_data) {
    // Сделайте что-нибудь с $train_data для функции XOR
}
?>
```

Вміст xor.data

### Дивіться також

-   [fanntrainвінdata()](function.fann-train-on-data.html) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fanndestroytrain()](function.fann-destroy-train.html) - Знищує тренувальні дані
-   [fannsavetrain()](function.fann-save-train.html) - Зберігає структуру навчання у файл
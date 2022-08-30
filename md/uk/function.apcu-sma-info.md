Витягує інформацію про виділення пам'яті, що розділяється APCu

-   [« apcukeyinfo](function.apcu-key-info.html)
    
-   [apcustore »](function.apcu-store.html)
    
-   [PHP Manual](index.md)
    
-   [Функции APCu](ref.apcu.md)
    
-   Витягує інформацію про виділення пам'яті, що розділяється APCu
    

# apcusmainfo

(PECL apcu >= 4.0.0)

apcusmainfo — Витягує інформацію про виділення пам'яті APCu, що розділяється.

### Опис

```methodsynopsis
apcu_sma_info(bool $limited = false): array|false
```

Витягує інформацію про виділення пам'яті APCu.

### Список параметрів

`limited`

Якщо встановлений у **`false`** (за замовчуванням), **apcusmainfo()** поверне детальну інформацію про кожен сегмент.

### Значення, що повертаються

Масив даних про виділену пам'ять, що розділяється; **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **apcusmainfo()****

```php
<?php
print_r(apcu_sma_info());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [num_seg] => 1
    [seg_size] => 31457280
    [avail_mem] => 31448408
    [block_lists] => Array
        (
            [0] => Array
                (
                    [0] => Array
                        (
                            [size] => 31448408
                            [offset] => 8864
                        )

                )

        )

)
```

### Дивіться також

-   [Директиви конфігурації APCu](apcu.configuration.md)
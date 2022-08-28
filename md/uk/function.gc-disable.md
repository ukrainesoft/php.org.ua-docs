Вимикає збирач циклічних посилань

-   [« gc\_collect\_cycles](function.gc-collect-cycles.html)
    
-   [gc\_enable »](function.gc-enable.html)
    
-   [PHP Manual](index.html)
    
-   [Опции PHP/информационные функции](ref.info.html)
    
-   Вимикає збирач циклічних посилань
    

# гкdisable

(PHP 5> = 5.3.0, PHP 7, PHP 8)

гкdisable — Вимикає збирач циклічних посилань

### Опис

```methodsynopsis
gc_disable(): void
```

Відключає збирач циклічних посилань шляхом встановлення значення [zend.enable\_gc](info.configuration.html#ini.zend.enable-gc) в `0`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [Сборка мусора](features.gc.html)
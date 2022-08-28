Створення нечіткого хешу з файлу

-   [« ssdeep\_fuzzy\_compare](function.ssdeep-fuzzy-compare.html)
    
-   [ssdeep\_fuzzy\_hash »](function.ssdeep-fuzzy-hash.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ssdeep](ref.ssdeep.html)
    
-   Створення нечіткого хешу з файлу
    

# ssdeepfuzzyhashfilename

(PECL ssdeep >= 1.0.0)

ssdeepfuzzyhashfilename — Створення нечіткого хешу з файлу

### Опис

```methodsynopsis
ssdeep_fuzzy_hash_filename(string $file_name): string
```

**ssdeepfuzzyhashfilename()** обчислює хеш вказаного файлу `file_name`, використовуючи [» контекстно-переключаемое частичное хеширование](http://dfrws.org/2006/proceedings/12-Kornblum.pdf) та повертає його значення.

### Список параметрів

`file_name`

Ім'я файлу для хешування.

### Значення, що повертаються

Повертає рядок у разі успішного виконання, **`false`** в іншому випадку.
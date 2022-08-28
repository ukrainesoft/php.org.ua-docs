Створює нечіткий хеш із рядка

-   [« ssdeep\_fuzzy\_hash\_filename](function.ssdeep-fuzzy-hash-filename.html)
    
-   [Строки »](book.strings.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ssdeep](ref.ssdeep.html)
    
-   Створює нечіткий хеш із рядка
    

# ssdeepfuzzyhash

(PECL ssdeep >= 1.0.0)

ssdeepfuzzyhash — Створює нечіткий хеш із рядка

### Опис

```methodsynopsis
ssdeep_fuzzy_hash(string $to_hash): string
```

**ssdeepfuzzyhash()** обчислює хеш рядки `to_hash`, використовуючи [»  контекстно-переключаемое частичное хеширование](http://dfrws.org/2006/proceedings/12-Kornblum.pdf) і повертає його.

### Список параметрів

`to_hash`

Рядок для хешування.

### Значення, що повертаються

Повертає рядок у разі успішного виконання, **`false`** в іншому випадку.
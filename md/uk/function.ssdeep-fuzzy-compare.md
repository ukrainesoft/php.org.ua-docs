Обчислює схожість двох сигнатур нечітких хешів

-   [« Функції ssdeep](ref.ssdeep.html)
    
-   [ssdeepfuzzyhashfilename »](function.ssdeep-fuzzy-hash-filename.html)
    
-   [PHP Manual](index.html)
    
-   [Функції ssdeep](ref.ssdeep.html)
    
-   Обчислює схожість двох сигнатур нечітких хешів
    

# ssdeepfuzzycompare

(PECL ssdeep >= 1.0.0)

ssdeepfuzzycompare — Обчислює схожість двох сигнатур нечітких хешів

### Опис

```methodsynopsis
ssdeep_fuzzy_compare(string $signature1, string $signature2): int
```

Обчислює величину збігу між `signature1` і `signature2`, використовуючи [»  контекстно-переключається часткове хешування](http://dfrws.org/2006/proceedings/12-Kornblum.pdf) та повертає її.

### Список параметрів

`signature1`

Перший рядок із сигнатурою нечіткого хешування.

`signature2`

Другий рядок із сигнатурою нечіткого хешування.

### Значення, що повертаються

Повертає ціле число в діапазоні від 0 до 100 у разі успішного виконання або **`false`** в іншому випадку.
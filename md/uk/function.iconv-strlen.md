Повертає кількість символів у рядку

-   [« iconvsetencoding](function.iconv-set-encoding.html)
    
-   [iconvstrpos »](function.iconv-strpos.html)
    
-   [PHP Manual](index.html)
    
-   [Функции iconv](ref.iconv.html)
    
-   Повертає кількість символів у рядку
    

# iconvstrlen

(PHP 5, PHP 7, PHP 8)

iconvstrlen — Повертає кількість символів у рядку

### Опис

```methodsynopsis
iconv_strlen(string $string, ?string $encoding = null): int|false
```

На відміну від [strlen()](function.strlen.html) **iconvstrlen()** враховує кодування рядка. Довжина `string` не обов'язково буде відповідати кількості байт у ній, так як у різних кодуваннях різні символи кодуються різною кількістю байт, наприклад, юнікод може бути і дво-, і чотирибайтним.

### Список параметрів

`string`

Рядок.

`encoding`

Якщо параметр `encoding` опущено, передбачається, що кодування рядка `string` еквівалентна значенню [iconv.internalencoding](iconv.configuration.html)

### Значення, що повертаються

Повертає кількість символів у `string` як ціле число або **`false`** у разі виникнення помилки під час кодування.

### список змін

| Версия | Описание |
| --- | --- |
|  | `encoding` тепер допускає значення null. |

### Дивіться також

-   [graphemestrlen()](function.grapheme-strlen.html) - отримує довжину рядка в одиницях графеми
-   [мбstrlen()](function.mb-strlen.html) - Отримує довжину рядка
-   [strlen()](function.strlen.html) - Повертає довжину рядка
Встановлення/отримання кодування символів виводу HTTP

-   [« mbhttpinput](function.mb-http-input.html)
    
-   [мбinternalencoding »](function.mb-internal-encoding.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з багатобайтовими рядками](ref.mbstring.html)
    
-   Встановлення/отримання кодування символів виводу HTTP
    

# мбhttpoutput

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

мбhttpoutput — Встановлення/отримання кодування символів виводу HTTP

### Опис

```methodsynopsis
mb_http_output(?string $encoding = null): string|bool
```

Встановлення/отримання кодування символів виводу HTTP. Вихідні дані після роботи цієї функції будуть перетворені з внутрішнього кодування до `encoding`

### Список параметрів

`encoding`

Якщо заданий аргумент `encoding` **мбhttpoutput()** встановлює кодування вихідних символів HTTP `encoding`

Якщо аргумент `encoding` опущений, **мбhttpoutput()** повертає поточне кодування символів виводу HTTP.

### Значення, що повертаються

Якщо аргумент `encoding` опущений, **мбhttpoutput()** повертає поточне кодування символів виводу HTTP. В іншому випадку, Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер параметр `encoding` може набувати значення **`null`** |

### Дивіться також

-   [мбinternalencoding()](function.mb-internal-encoding.html) - Встановлення/отримання внутрішнього кодування скрипту
-   [мбhttpinput()](function.mb-http-input.html) - Визначення кодування символів вхідних даних HTTP-запиту
-   [мбdetectorder()](function.mb-detect-order.html) - Встановлення/отримання списку кодувань для механізмів визначення кодування
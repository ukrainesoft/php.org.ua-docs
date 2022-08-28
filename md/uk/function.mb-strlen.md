Отримує довжину рядка

-   [« mb\_stristr](function.mb-stristr.html)
    
-   [mb\_strpos »](function.mb-strpos.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с многобайтовыми строками](ref.mbstring.html)
    
-   Отримує довжину рядка
    

# мбstrlen

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

мбstrlen — Отримує довжину рядка

### Опис

```methodsynopsis
mb_strlen(string $string, ?string $encoding = null): int
```

Отримує довжину рядка (string).

### Список параметрів

`string`

Рядок (string), на яку вимірюється довжина.

`encoding`

Параметр `encoding` є символьним кодуванням. Якщо він опущений або дорівнює **`null`**, замість нього буде використано значення внутрішнього кодування.

### Значення, що повертаються

Повертає кількість символів у рядку (string) `string`, що мають кодування символів `encoding`. Багатобайтовий символ обчислюється як один.

### Помилки

Якщо кодування невідоме, генерується помилка рівня **`E_WARNING`**

### список змін

| Версия | Описание                                                    |
|--------|-------------------------------------------------------------|
|        | Тепер параметр `encoding` може набувати значення **`null`** |

### Дивіться також

-   [mb\_internal\_encoding()](function.mb-internal-encoding.html) - Встановлення/отримання внутрішнього кодування скрипту
-   [grapheme\_strlen()](function.grapheme-strlen.html) - отримує довжину рядка в одиницях графеми
-   [iconv\_strlen()](function.iconv-strlen.html) - Повертає кількість символів у рядку
-   [strlen()](function.strlen.html) - Повертає довжину рядка
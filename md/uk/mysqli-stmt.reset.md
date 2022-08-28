Скидає результати виконання підготовленого запиту

-   [« mysqli\_stmt::prepare](mysqli-stmt.prepare.html)
    
-   [mysqli\_stmt::result\_metadata »](mysqli-stmt.result-metadata.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli\_stmt](class.mysqli-stmt.html)
    
-   Скидає результати виконання підготовленого запиту
    

# mysqlistmt::reset

# mysqlistmtreset

(PHP 5, PHP 7, PHP 8)

mysqlistmt::reset -- mysqlistmtreset — Скидає результати підготовленого запиту.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::reset(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_reset(mysqli_stmt $statement): bool
```

Скидає результати виконання підготовленого запиту на клієнта та на сервері та переводить запит у стан, як після підготовки.

Скидає запит на сервері, а також дані, передані на сервер функцією [mysqli\_stmt\_send\_long\_data()](mysqli-stmt.send-long-data.html), очищає буфер результатів запиту та поточні помилки. Функція не видаляє прив'язки параметрів запиту, а також надані на клієнта результуючі набори. Результуючі набори, що містяться на клієнті, будуть очищені при наступному виконанні запиту (або його закритті).

Для підготовки запиту з іншим текстом SQL, використовуйте функцію [mysqli\_stmt\_prepare()](mysqli-stmt.prepare.html)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.html), отриманий за допомогою [mysqli\_stmt\_init()](mysqli.stmt-init.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mysqli\_prepare()](mysqli.prepare.html) - готує SQL вираз до виконання
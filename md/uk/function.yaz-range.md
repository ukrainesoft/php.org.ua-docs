Визначає діапазон записів для отримання

-   [« yaz\_present](function.yaz-present.html)
    
-   [yaz\_record »](function.yaz-record.html)
    
-   [PHP Manual](index.html)
    
-   [Функции YAZ](ref.yaz.html)
    
-   Визначає діапазон записів для отримання
    

# yazrange

(PHP 4> = 4.0.1, PECL yaz> = 0.9.0)

yazrange — Визначає діапазон записів для отримання

### Опис

```methodsynopsis
yaz_range(resource $id, int $start, int $number): void
```

Визначає діапазон записів для отримання.

Функція має бути викликана перед [yaz\_search()](function.yaz-search.html) або [yaz\_present()](function.yaz-present.html)

### Список параметрів

`id`

Ресурс з'єднання, повернутий [yaz\_connect()](function.yaz-connect.html)

`start`

Визначає позицію першого запису, який потрібно отримати. Номери записів йдуть від 1 до [yaz\_hits()](function.yaz-hits.html)

`number`

Визначає діапазон записів для отримання.

### Значення, що повертаються

Функція не повертає значення після виконання.
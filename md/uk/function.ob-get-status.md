Отримати статус буфера виводу

-   [« ob\_get\_level](function.ob-get-level.html)
    
-   [ob\_gzhandler »](function.ob-gzhandler.html)
    
-   [PHP Manual](index.html)
    
-   [Функции контроля вывода](ref.outcontrol.html)
    
-   Отримати статус буфера виводу
    

# проgetstatus

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

проgetstatus — Отримати статус буфера виводу

### Опис

```methodsynopsis
ob_get_status(bool $full_status = false): array
```

**проgetstatus()** повертає інформацію про стан буфера верхнього рівня або на всіх рівнях активних буферів, якщо `full_status` встановлений в **`true`**

### Список параметрів

`full_status`

Якщо **`true`**то поверне всі рівні активних буферів. Якщо **`false`** або не встановлений, то поверне статус лише найвищого рівня.

### Значення, що повертаються

Якщо функція викликана без параметра `full_status` або `full_status` **`false`**, то повертається простий масив з наступних елементів:

Array ( level => 2 type => 0 status => 0 name => URL-Rewriter del => 1 )

**Результати простого виклику **проgetstatus()****

| Ключ  | Значение                                                                     |
|-------|------------------------------------------------------------------------------|
| level | Рівень вкладеності висновку                                                  |
| type  | `PHP_OUTPUT_HANDLER_INTERNAL (0)` або `PHP_OUTPUT_HANDLER_USER (1)`          |
| type  | `0` (внутрішній обробник) або `1` (наданий користувачем обробник)            |
| name  | Назва діючого обробника виводу або 'default output handler', якщо не заданий |
| del   | Прапор очищення, встановлений [ob\_start()](function.ob-start.html)          |

Якщо функція викликана з `full_status` **`true`**, Повертається масив з елементів рівнів активних буферів. Як ключ використовується рівень виведення, і кожен елемент масиву містить масив інформації про статус одного з активних елементів виведення.

```
Array
(
    [0] => Array
        (
            [chunk_size] => 0
            [size] => 40960
            [block_size] => 10240
            [type] => 1
            [status] => 0
            [name] => default output handler
            [del] => 1
        )

    [1] => Array
        (
            [chunk_size] => 0
            [size] => 40960
            [block_size] => 10240
            [type] => 0
            [buffer_size] => 0
            [status] => 0
            [name] => URL-Rewriter
            [del] => 1
        )

)
```

Повний висновок містить такі додаткові елементи:

**Повні результати **проgetstatus()****

| Ключ      | Значение                                                          |
|-----------|-------------------------------------------------------------------|
| chunksize | Розмір порції, встановлений [ob\_start()](function.ob-start.html) |
| size      |                                                                   |
| blocksize |                                                                   |

### Дивіться також

-   [ob\_get\_level()](function.ob-get-level.html) - Повертає рівень вкладеності механізму буферизації виводу
-   [ob\_list\_handlers()](function.ob-list-handlers.html) - Список всіх використовуваних обробників виводу
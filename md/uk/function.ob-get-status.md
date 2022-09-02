---
navigation:
  - function.ob-get-level.md: « obgetlevel
  - function.ob-gzhandler.md: проgzhandler »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: проgetstatus
---
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

Якщо \*\*`true`\*\*то поверне всі рівні активних буферів. Якщо **`false`** або не встановлений, то поверне статус лише найвищого рівня.

### Значення, що повертаються

Якщо функція викликана без параметра `full_status` або `full_status` **`false`**, то повертається простий масив з наступних елементів:

Array ( level => 2 type => 0 status => 0 name => URL-Rewriter del => 1 )

**Результати простого виклику **проgetstatus()****

| Ключ | Значение |
| --- | --- |
| level | Рівень вкладеності висновку |
| type | `PHP_OUTPUT_HANDLER_INTERNAL (0)` або `PHP_OUTPUT_HANDLER_USER (1)` |
| type | `0` (внутрішній обробник) або `1` (наданий користувачем обробник) |
| name | Назва діючого обробника виводу або 'default output handler', якщо не заданий |
| del | Прапор очищення, встановлений [проstart()](function.ob-start.md) |

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

| Ключ | Значение |
| --- | --- |
| chunksize | Розмір порції, встановлений [проstart()](function.ob-start.md) |
| size |  |
| blocksize |  |

### Дивіться також

-   [проgetlevel()](function.ob-get-level.md) - Повертає рівень вкладеності механізму буферизації виводу
-   [проlisthandlers()](function.ob-list-handlers.md) - Список всіх використовуваних обробників виводу

Додає дані до активного контексту хешування

-   [« hashupdatestream](function.hash-update-stream.html)
    
-   [hash »](function.hash.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Hash](ref.hash.html)
    
-   Додає дані до активного контексту хешування
    

# hashupdate

(PHP 5> = 5.1.2, PHP 7, PHP 8, PECL hash> = 1.1)

hashupdate — Додає дані до активного контексту хешування

### Опис

```methodsynopsis
hash_update(HashContext $context, string $data): bool
```

### Список параметрів

`context`

Контекст хешування, що повертається [hashinit()](function.hash-init.html)

`data`

Повідомлення, яке має бути включене до хеша.

### Значення, що повертаються

Повертає **`true`**

### список змін

| Версия | Описание                                                       |
|--------|----------------------------------------------------------------|
|        | Приймає [HashContext](class.hashcontext.html), а чи не ресурс. |

### Дивіться також

-   [hashinit()](function.hash-init.html) - Ініціалізація інкрементального контексту хешування
-   [hashupdatefile()](function.hash-update-file.html) - Додає дані з файлу до активного контексту хешування
-   [hashupdatestream()](function.hash-update-stream.html) - Додає дані з відкритого потоку до активного контексту хешування
-   [hashfinal()](function.hash-final.html) - Завершує інкрементальне хешування та повертає результат у вигляді хеш-коду
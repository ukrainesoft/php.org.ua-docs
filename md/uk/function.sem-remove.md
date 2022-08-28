Видалення семафору

-   [« sem\_release](function.sem-release.html)
    
-   [shm\_attach »](function.shm-attach.html)
    
-   [PHP Manual](index.html)
    
-   [Функции семафоров](ref.sem.html)
    
-   Видалення семафору
    

# semremove

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

semremove — Видалення семафору

### Опис

```methodsynopsis
sem_remove(SysvSemaphore $semaphore): bool
```

**semremove()** видаляє вказаний семафор.

Після видалення семафору він стає недоступним.

### Список параметрів

`semaphore`

Семафор, повернутий [sem\_get()](function.sem-get.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `semaphore` тепер чекає екземпляр [SysvSemaphore](class.sysvsemaphore.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [sem\_get()](function.sem-get.html) - Отримання ідентифікатора семафору
-   [sem\_release()](function.sem-release.html) - Звільнення семафору
-   [sem\_acquire()](function.sem-acquire.html) - Захоплення семафору
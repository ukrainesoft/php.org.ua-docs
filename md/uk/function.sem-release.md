Звільнення семафору

-   [« semget](function.sem-get.html)
    
-   [semremove »](function.sem-remove.html)
    
-   [PHP Manual](index.html)
    
-   [Функції семафорів](ref.sem.html)
    
-   Звільнення семафору
    

# semrelease

(PHP 4, PHP 5, PHP 7, PHP 8)

semrelease - Звільнення семафору

### Опис

```methodsynopsis
sem_release(SysvSemaphore $semaphore): bool
```

**semrelease()** звільняє семафор, якщо він був захоплений зухвалим процесом, інакше генерується попередження.

Після звільнення семафор може бути захоплений повторно через виклик [semacquire()](function.sem-acquire.html)

### Список параметрів

`semaphore`

Семафор, повернутий [semget()](function.sem-get.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                   |
|--------|----------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `semaphore` тепер чекає екземпляр [SysvSemaphore](class.sysvsemaphore.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [semget()](function.sem-get.html) - Отримання ідентифікатора семафору
-   [semacquire()](function.sem-acquire.html) - Захоплення семафору
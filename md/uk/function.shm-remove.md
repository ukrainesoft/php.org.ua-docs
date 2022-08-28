Видаляє пам'ять, що розділяється, з систем Unix

-   [« shm\_remove\_var](function.shm-remove-var.html)
    
-   [SysvMessageQueue »](class.sysvmessagequeue.html)
    
-   [PHP Manual](index.html)
    
-   [Функции семафоров](ref.sem.html)
    
-   Видаляє пам'ять, що розділяється, з систем Unix
    

# shmremove

(PHP 4, PHP 5, PHP 7, PHP 8)

shmremove — Видалення пам'яті, що розділяється, з систем Unix

### Опис

```methodsynopsis
shm_remove(SysvSharedMemory $shm): bool
```

**shmremove()** видаляє пам'ять, що розділяється `shm`. Усі дані будуть знищені.

### Список параметрів

`shm`

Сегмент пам'яті, що розділяється, отриманий з [shm\_attach()](function.shm-attach.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------|
|        | `shm` тепер чекає екземпляр [SysvSharedMemory](class.sysvsharedmemory.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [shm\_remove\_var()](function.shm-remove-var.html) - Видаляє змінну з пам'яті, що розділяється
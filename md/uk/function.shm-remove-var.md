Видаляє змінну з пам'яті, що розділяється

-   [« shmputvar](function.shm-put-var.html)
    
-   [shmremove »](function.shm-remove.html)
    
-   [PHP Manual](index.html)
    
-   [Функції семафорів](ref.sem.html)
    
-   Видаляє змінну з пам'яті, що розділяється
    

# shmremovevar

(PHP 4, PHP 5, PHP 7, PHP 8)

shmremovevar — Видалення змінної з пам'яті, що розділяється.

### Опис

```methodsynopsis
shm_remove_var(SysvSharedMemory $shm, int $key): bool
```

Видаляє змінну із заданим ключем `key` та звільняє зайняту пам'ять.

### Список параметрів

`shm`

Сегмент пам'яті, що розділяється, отриманий з [shmattach()](function.shm-attach.html)

`key`

Ключ змінної.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------|
|        | `shm` тепер чекає екземпляр [SysvSharedMemory](class.sysvsharedmemory.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [shmremove()](function.shm-remove.html) - Видаляє пам'ять, що розділяється, з систем Unix
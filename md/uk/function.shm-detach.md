Відключається від сегмента пам'яті, що розділяється

-   [« shmattach](function.shm-attach.html)
    
-   [shmgetvar »](function.shm-get-var.html)
    
-   [PHP Manual](index.html)
    
-   [Функції семафорів](ref.sem.html)
    
-   Відключається від сегмента пам'яті, що розділяється
    

# shmdetach

(PHP 4, PHP 5, PHP 7, PHP 8)

shmdetach — Вимикається від сегмента пам'яті, що розділяється.

### Опис

```methodsynopsis
shm_detach(SysvSharedMemory $shm): bool
```

**shmdetach()** відключається від сегмента пам'яті, зазначеного в `shm`, створеного [shmattach()](function.shm-attach.html). Пам'ятайте, що пам'ять, що розділяється, все ще існує в системі Unix і дані все ще присутні.

### Список параметрів

`shm`

Сегмент пам'яті, що розділяється, отриманий з [shmattach()](function.shm-attach.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                       |
|--------|----------------------------------------------------------------------------------------------------------------|
|        | `shm` чекає на екземпляр [SysvSharedMemory](class.sysvsharedmemory.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [shmattach()](function.shm-attach.html) - Створює або відкриває сегмент пам'яті, що розділяється
-   [shmremove()](function.shm-remove.html) - Видаляє пам'ять, що розділяється, з систем Unix
-   [shmremovevar()](function.shm-remove-var.html) - Видаляє змінну з пам'яті, що розділяється.
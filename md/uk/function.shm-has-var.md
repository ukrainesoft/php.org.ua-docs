Перевіряє, чи існує конкретний запис

-   [« shmgetvar](function.shm-get-var.html)
    
-   [shmputvar »](function.shm-put-var.html)
    
-   [PHP Manual](index.html)
    
-   [Функції семафорів](ref.sem.html)
    
-   Перевіряє, чи існує конкретний запис
    

# shmhasvar

(PHP 5> = 5.3.0, PHP 7, PHP 8)

shmhasvar — Перевіряє, чи існує конкретний запис

### Опис

```methodsynopsis
shm_has_var(SysvSharedMemory $shm, int $key): bool
```

Перевіряє, чи існує конкретний ключ у сегменті пам'яті, що розділяється.

### Список параметрів

`shm`

Сегмент пам'яті, що розділяється, отриманий з [shmattach()](function.shm-attach.html)

`key`

Ключ змінної.

### Значення, що повертаються

Повертає **`true`**, якщо запис існує, інакше повертає **`false`**

### список змін

| Версия | Описание                                                                                                          |
|--------|-------------------------------------------------------------------------------------------------------------------|
|        | `shm` тепер чекає екземпляр [SysvSharedMemory](class.sysvsharedmemory.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [shmgetvar()](function.shm-get-var.html) - Повертає змінну з пам'яті, що розділяється
-   [shmputvar()](function.shm-put-var.html) - Вставляє або оновлює змінну в пам'яті, що розділяється.
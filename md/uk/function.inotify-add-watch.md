Додати спостерігача для екземпляра inotify

-   [« Функции Inotify](ref.inotify.html)
    
-   [inotify\_init »](function.inotify-init.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Inotify](ref.inotify.html)
    
-   Додати спостерігача для екземпляра inotify
    

# inotifyaddwatch

(PECL inotify >= 0.1.2)

inotifyaddwatch — Додати спостерігача для екземпляра inotify

### Опис

```methodsynopsis
inotify_add_watch(resource $inotify_instance, string $pathname, int $mask): int
```

**inotifyaddwatch()** додає нового спостерігача або змінює існуючий для файлу або директорії, заданих у `pathname`

Використання **inotifyaddwatch()** на обстеженні, що вже відстежується, замінить поточного спостерігача. використання константи **`IN_MASK_ADD`** додати (OR) події існуючому спостерігачеві.

### Список параметрів

`inotify_instance`

Ресурс, що повертається [inotify\_init()](function.inotify-init.html)

`pathname`

Файл або директорія для відстеження

`mask`

Події, які слід відстежувати. Дивіться [Предопределённые константы](inotify.constants.html)

### Значення, що повертаються

Повертає унікальний (в контексті екземпляра inotify) дескриптор спостерігача.

### Дивіться також

-   [inotify\_init()](function.inotify-init.html) - Ініціалізує екземпляр inotify
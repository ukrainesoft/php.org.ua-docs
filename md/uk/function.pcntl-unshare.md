Поділяє частини контексту виконання процесу

-   [« pcntl\_strerror](function.pcntl-strerror.html)
    
-   [pcntl\_wait »](function.pcntl-wait.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PCNTL](ref.pcntl.html)
    
-   Поділяє частини контексту виконання процесу
    

# pcntlunshare

(PHP 7> = 7.4.0, PHP 8)

pcntlunshare — розділяє частини контексту виконання процесу

### Опис

```methodsynopsis
pcntl_unshare(int $flags): bool
```

Функція **pcntlunshare()** дозволяє процесу від'єднати частини свого контексту виконання, які зараз використовуються спільно з іншими процесами. Основне використання **pcntlunshare()** полягає в тому, щоб дозволити процесу керувати своїм загальним контекстом виконання без створення нового процесу.

### Список параметрів

`flags`

Параметр `flags` - це бітова маска, що визначає, які частини контексту виконання мають бути нерозділеними. Параметр задається шляхом використання оператора OR разом з нулем або більше констант `CLONE_*`

-   **`CLONE_NEWNS`**
-   **`CLONE_NEWIPC`**
-   **`CLONE_NEWUTS`**
-   **`CLONE_NEWNET`**
-   **`CLONE_NEWPID`**
-   **`CLONE_NEWUSER`**
-   **`CLONE_NEWCGROUP`**

### Значення, що повертаються

Повертає `0` у разі успішного виконання, `-1` в іншому випадку. У разі виникнення помилки встановлюється код помилки, який можна отримати за допомогою функції [pcntl\_get\_last\_error()](function.pcntl-get-last-error.html)

### Дивіться також

-   [Константы PCNTL](pcntl.constants.html#pcntl.constants.clone)
-   [pcntl\_get\_last\_error()](function.pcntl-get-last-error.html) - Отримати код останньої помилки, що виникла в pcntl-функції
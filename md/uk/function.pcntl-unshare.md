---
navigation:
  - function.pcntl-strerror.md: « pcntl\_strerror
  - function.pcntl-wait.md: pcntl\_wait »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_unshare
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_unshare

(PHP 7 >= 7.4.0, PHP 8)

pcntl\_unshare — розділяє частини контексту виконання процесу

### Опис

```methodsynopsis
pcntl_unshare(int $flags): bool
```

Функция**pcntl\_unshare()** дозволяє процесу від'єднати частини свого контексту виконання, які зараз використовуються спільно з іншими процесами. Основне використання **pcntl\_unshare()** полягає в тому, щоб дозволити процесу керувати своїм загальним контекстом виконання без створення нового процесу.

### Список параметрів

`flags`

Параметр`flags` - це бітова маска, що визначає, які частини контексту виконання мають бути нерозділеними. Параметр задається шляхом використання оператора OR разом з нулем або більше констант `CLONE_*` :

-   **`CLONE_NEWNS`**
-   **`CLONE_NEWIPC`**
-   **`CLONE_NEWUTS`**
-   **`CLONE_NEWNET`**
-   **`CLONE_NEWPID`**
-   **`CLONE_NEWUSER`**
-   **`CLONE_NEWCGROUP`**

### Значення, що повертаються

Повертає у разі успішного виконання, `-1` в іншому випадку. У разі виникнення помилки встановлюється код помилки, який можна отримати за допомогою функції [pcntl\_get\_last\_error()](function.pcntl-get-last-error.md)

### Дивіться також

-   [Константи PCNTL](pcntl.constants.md#pcntl.constants.clone)
-   [pcntl\_get\_last\_error()](function.pcntl-get-last-error.md) \- Отримати код останньої помилки, що виникла в pcntl-функції

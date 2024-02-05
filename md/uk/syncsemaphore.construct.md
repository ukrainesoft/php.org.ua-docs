---
navigation:
  - class.syncsemaphore.md: « SyncSemaphore
  - syncsemaphore.lock.md: 'SyncSemaphore::lock »'
  - index.md: PHP Manual
  - class.syncsemaphore.md: SyncSemaphore
title: 'SyncSemaphore::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SyncSemaphore::\_\_construct

(PECL sync >= 1.0.0)

SyncSemaphore::\_\_construct — Створення нового об'єкту SyncSemaphore

### Опис

```methodsynopsis
public SyncSemaphore::__construct(string $name = ?, int $initialval = 1, bool $autounlock = true)
```

Створює іменований чи безіменний семафор.

### Список параметрів

`name`

Ім'я семафора, якщо це названий об'єкт семафора.

> **Зауваження** :
> 
> Якщо ім'я вже існує, воно має бути доступним для відкриття поточним користувачем, від імені якого запущено процес, інакше буде викинуто виняток із безглуздим повідомленням про помилку.

`initialval`

Початкове значення семафору. Це кількість блокувань, яку можна отримати.

`autounlock`

Вказує, чи слід автоматично розблокувати семафор після завершення скрипта PHP.

**Увага**

Якщо об'єкт - це: іменований семафор з autounlock зі значенням **`false`**, об'єкт заблокований і скрипт PHP завершується до того, як об'єкт розблокується, базовий семафор опиниться в неузгодженому стані.

### Значення, що повертаються

Новий об'єкт [SyncSemaphore](class.syncsemaphore.md)

### Помилки

Якщо семафор не може бути створений або відкритий, викидається виняток.

### Приклади

**Пример #1 Пример использования**SyncSemaphore::\_\_construct()\*\*\*\*

```php
<?php
$semaphore = new SyncSemaphore("LimitedResource_2clients", 2);

if (!$semaphore->lock(3000))
{
    echo "Невозможно заблокировать семафор.";

    exit();
}

/* ... */

$semaphore->unlock();
?>
```

### Дивіться також

-   [SyncSemaphore::lock()](syncsemaphore.lock.md) \- Зменшує рахунок семафора або чекає
-   [SyncSemaphore::unlock()](syncsemaphore.unlock.md) \- Збільшує рахунок семафору

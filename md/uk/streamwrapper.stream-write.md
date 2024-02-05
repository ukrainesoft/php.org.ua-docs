---
navigation:
  - streamwrapper.stream-truncate.md: '« streamWrapper::stream\_truncate'
  - streamwrapper.unlink.md: 'streamWrapper::unlink »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::stream\_write'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::stream\_write

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::stream\_write - Запис у потік

### Опис

```methodsynopsis
public streamWrapper::stream_write(string $data): int
```

Цей метод викликається внаслідок запуску функції [fwrite()](function.fwrite.md)

> **Зауваження** :
> 
> Не забувайте змінювати поточну позицію потоку кількість успішно записаних байт.

### Список параметрів

`data`

Ці дані мають передаватися потоку рівнем нижче.

> **Зауваження** :
> 
> Якщо потік нижче здатний прийняти всі дані, передавайте скільки можливо.

### Значення, що повертаються

Повинен повертати кількість успішно записаних байт або 0, якщо нічого не вдалося записати.

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

> **Зауваження** :
> 
> Якщо значення, що повертається, виявиться більше розміру даних `data`, буде викликана помилка рівня **`E_WARNING`**, а значення, що повертається, буде усічено до цього розміру.

### Дивіться також

-   [fwrite()](function.fwrite.md) \- Бінарно-безпечний запис у файл

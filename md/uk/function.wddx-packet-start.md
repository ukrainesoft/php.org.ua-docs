---
navigation:
  - function.wddx-packet-end.md: « wddxpacketend
  - function.wddx-serialize-value.md: wddxserializevalue »
  - index.md: PHP Manual
  - ref.wddx.md: Функції WDDX
title: wddxpacketstart
---
# wddxpacketstart

(PHP 4, PHP 5, PHP 7)

wddxpacketstart — Запуск нового пакета WDDX зі структурою всередині нього

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 7.4.0.

### Опис

```methodsynopsis
wddx_packet_start(string $comment = ?): resource
```

Запустити новий пакет WDDX для інкрементного додавання змінних. Це автоматично створить визначення структури всередині пакета для зберігання змінних.

### Список параметрів

`comment`

Необов'язковий рядок із коментарем

### Значення, що повертаються

Повертає ідентифікатор пакета для використання у наступних функціях або **`false`** у разі виникнення помилки.

---
navigation:
  - function.wddx-packet-end.md: « wddx\_packet\_end
  - function.wddx-serialize-value.md: wddx\_serialize\_value »
  - index.md: PHP Manual
  - ref.wddx.md: Функції WDDX
title: wddx\_packet\_start
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wddx\_packet\_start

(PHP 4, PHP 5, PHP 7)

wddx\_packet\_start — Запуск нового пакета WDDX зі структурою всередині нього

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

Возвращает идентификатор пакета для использования в последующих функциях или\*\*`false`\*\*в случае возникновения ошибки.

---
navigation:
  - stomp.getsessionid.md: '« Stomp::getSessionId'
  - stomp.readframe.md: 'Stomp::readFrame »'
  - index.md: PHP Manual
  - class.stomp.md: Stomp
title: 'Stomp::hasFrame'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Stomp::hasFrame

# stomp\_has\_frame

(PECL stomp >= 0.1.0)

Stomp::hasFrame -- stomp\_has\_frame — Перевіряє, чи можливо читати кадр

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Stomp::hasFrame(): bool
```

Процедурний стиль:

```methodsynopsis
stomp_has_frame(resource $link): bool
```

Перевіряє, чи можливе читання кадру.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stomp\_connect()](stomp.construct.md)

### Значення, що повертаються

Повертає **`true`** якщо кадр можна прочитати, інакше **`false`**

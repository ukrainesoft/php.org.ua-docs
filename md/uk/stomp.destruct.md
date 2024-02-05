---
navigation:
  - stomp.construct.md: '« Stomp::\_\_construct'
  - stomp.error.md: 'Stomp::error »'
  - index.md: PHP Manual
  - class.stomp.md: Stomp
title: 'Stomp::\_\_destruct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Stomp::\_\_destruct

# stomp\_close

(PECL stomp >= 0.1.0)

Stomp::\_\_destruct -- stomp\_close - Закриває Stomp-з'єднання

### Опис

Об'єктно-орієнтований стиль (деструктор):

public **Stomp::\_\_destruct**()

Процедурний стиль:

```methodsynopsis
stomp_close(resource $link): bool
```

Закриває відкриті раніше з'єднання.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stomp\_connect()](stomp.construct.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

Смотрите[stomp\_connect()](stomp.construct.md)

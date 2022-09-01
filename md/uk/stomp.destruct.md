---
navigation:
  - stomp.construct.md: '« Stomp::construct'
  - stomp.error.md: 'Stomp::error »'
  - index.md: PHP Manual
  - class.stomp.md: Stomp
title: 'Stomp::destruct'
---
# Stomp::destruct

# stompclose

(PECL stomp >= 0.1.0)

Stomp::destruct - stompclose - Закриває Stomp-з'єднання

### Опис

Об'єктно-орієнтований стиль (деструктор):

public **Stomp::destruct**

Процедурний стиль:

```methodsynopsis
stomp_close(resource $link): bool
```

Закриває відкриті раніше з'єднання.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stompconnect()](stomp.construct.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

Дивіться [stompconnect()](stomp.construct.md)

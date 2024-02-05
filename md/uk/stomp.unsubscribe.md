---
navigation:
  - stomp.subscribe.md: '« Stomp::subscribe'
  - class.stompframe.md: StompFrame »
  - index.md: PHP Manual
  - class.stomp.md: Stomp
title: 'Stomp::unsubscribe'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Stomp::unsubscribe

# stomp\_unsubscribe

(PECL stomp >= 0.1.0)

Stomp::unsubscribe -- stomp\_unsubscribe — Видаляє існуючу передплату

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Stomp::unsubscribe(string $destination, array $headers = ?): bool
```

Процедурний стиль:

```methodsynopsis
stomp_unsubscribe(resource $link, string $destination, array $headers = ?): bool
```

Видаляє існуючу передплату.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stomp\_connect()](stomp.construct.md)

`destination`

Передплата видалення.

`headers`

Асоціативний масив, який містить додаткові заголовки (приклад: receipt).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

Смотрите[stomp\_ack()](stomp.ack.md)

### Примітки

**Підказка**

Stomp асинхронний за своєю суттю. Синхронний зв'язок може бути реалізований додаванням receipt-заголовка. Це змусить методи нічого не повертати, доки сервер не підтвердить отримання повідомлення або буде перевищено час очікування повідомлення.

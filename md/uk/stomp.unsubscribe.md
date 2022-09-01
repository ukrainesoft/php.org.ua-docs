---
navigation:
  - stomp.subscribe.html: '« Stomp::subscribe'
  - class.stompframe.html: StompFrame »
  - index.html: PHP Manual
  - class.stomp.html: Stomp
title: 'Stomp::unsubscribe'
---
# Stomp::unsubscribe

# stompunsubscribe

(PECL stomp >= 0.1.0)

Stomp::unsubscribe -- stompunsubscribe — Видаляє існуючу передплату

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

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stompconnect()](stomp.construct.html)

`destination`

Передплата для видалення.

`headers`

Асоціативний масив, який містить додаткові заголовки (приклад: receipt).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

Дивіться [stompack()](stomp.ack.html)

### Примітки

**Підказка**

Stomp асинхронний за своєю суттю. Синхронний зв'язок може бути реалізований додаванням receipt-заголовка. Це змусить методи нічого не повертати, поки сервер не підтвердить отримання повідомлення або буде перевищено час очікування повідомлення.

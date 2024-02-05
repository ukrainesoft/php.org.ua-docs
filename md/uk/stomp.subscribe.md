---
navigation:
  - stomp.setreadtimeout.md: '« Stomp::setReadTimeout'
  - stomp.unsubscribe.md: 'Stomp::unsubscribe »'
  - index.md: PHP Manual
  - class.stomp.md: Stomp
title: 'Stomp::subscribe'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Stomp::subscribe

# stomp\_subscribe

(PECL stomp >= 0.1.0)

Stomp::subscribe -- stomp\_subscribe — Зареєструє передплату на вказану розсилку

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Stomp::subscribe(string $destination, array $headers = ?): bool
```

Процедурний стиль:

```methodsynopsis
stomp_subscribe(resource $link, string $destination, array $headers = ?): bool
```

Реєструє передплату на вказану розсилку.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stomp\_connect()](stomp.construct.md)

`destination`

Розсилання, на яке необхідно зареєструвати передплату.

`headers`

Асоціативний масив, який містить додаткові заголовки (приклад: receipt).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

Смотрите[stomp\_ack()](stomp.ack.md)

### Примітки

**Підказка**

Stomp асинхронний за своєю суттю. Синхронний зв'язок може бути реалізований додаванням receipt-заголовка. Це змусить методи нічого не повертати, доки сервер не підтвердить отримання повідомлення або буде перевищено час очікування повідомлення.

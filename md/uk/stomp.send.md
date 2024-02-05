---
navigation:
  - stomp.readframe.md: '« Stomp::readFrame'
  - stomp.setreadtimeout.md: 'Stomp::setReadTimeout »'
  - index.md: PHP Manual
  - class.stomp.md: Stomp
title: 'Stomp::send'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Stomp::send

# stomp\_send

(PECL stomp >= 0.1.0)

Stomp::send -- stomp\_send — Надсилає повідомлення

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Stomp::send(string $destination, mixed $msg, array $headers = ?): bool
```

Процедурний стиль:

```methodsynopsis
stomp_send(    resource $link,    string $destination,    mixed $msg,    array $headers = ?): bool
```

Надсилає повідомлення брокеру повідомлень (Message Broker).

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stomp\_connect()](stomp.construct.md)

`destination`

Призначення для надсилання повідомлення.

`msg`

Повідомлення для надсилання.

`headers`

Асоціативний масив, який містить додаткові заголовки (приклад: receipt).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

Смотрите[stomp\_ack()](stomp.ack.md)

### Примітки

> **Зауваження** :
> 
> Також може бути зазначений заголовок транзакції, що означає, що прийом повідомлення повинен бути частиною іменованої транзакції.

**Підказка**

Stomp асинхронний за своєю суттю. Синхронний зв'язок може бути реалізований додаванням receipt-заголовка. Це змусить методи нічого не повертати, доки сервер не підтвердить отримання повідомлення або буде перевищено час очікування повідомлення.

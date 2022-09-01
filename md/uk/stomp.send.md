---
navigation:
  - stomp.readframe.html: '« Stomp::readFrame'
  - stomp.setreadtimeout.html: 'Stomp::setReadTimeout »'
  - index.html: PHP Manual
  - class.stomp.html: Stomp
title: 'Stomp::send'
---
# Stomp::send

# stompsend

(PECL stomp >= 0.1.0)

Stomp::send -- stompsend — Надсилає повідомлення

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

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stompconnect()](stomp.construct.html)

`destination`

Призначення для надсилання повідомлення.

`msg`

Повідомлення для надсилання.

`headers`

Асоціативний масив, який містить додаткові заголовки (приклад: receipt).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

Дивіться [stompack()](stomp.ack.html)

### Примітки

> **Зауваження**
> 
> Також може бути зазначений заголовок транзакції, що означає, що прийом повідомлення повинен бути частиною іменованої транзакції.

**Підказка**

Stomp асинхронний за своєю суттю. Синхронний зв'язок може бути реалізований додаванням receipt-заголовка. Це змусить методи нічого не повертати, поки сервер не підтвердить отримання повідомлення або буде перевищено час очікування повідомлення.

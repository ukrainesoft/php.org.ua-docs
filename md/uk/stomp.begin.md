---
navigation:
  - stomp.ack.md: '« Stomp::ack'
  - stomp.commit.md: 'Stomp::commit »'
  - index.md: PHP Manual
  - class.stomp.md: Stomp
title: 'Stomp::begin'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Stomp::begin

# stomp\_begin

(PECL stomp >= 0.1.0)

Stomp::begin -- stomp\_begin - Створює транзакцію

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Stomp::begin(string $transaction_id, array $headers = ?): bool
```

Процедурний стиль:

```methodsynopsis
stomp_begin(resource $link, string $transaction_id, array $headers = ?): bool
```

Створює транзакцію.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stomp\_connect()](stomp.construct.md)

`transaction_id`

Ідентифікатор транзакції.

`headers`

Асоціативний масив, який містить додаткові заголовки (приклад: receipt).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

Смотрите[stomp\_commit()](stomp.commit.md) або [stomp\_abort()](stomp.abort.md)

### Примітки

**Підказка**

Stomp асинхронний за своєю суттю. Синхронний зв'язок може бути реалізований додаванням receipt-заголовка. Це змусить методи нічого не повертати, доки сервер не підтвердить отримання повідомлення або буде перевищено час очікування повідомлення.

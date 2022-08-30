Створює транзакцію

-   [« Stomp::ack](stomp.ack.html)
    
-   [Stomp::commit »](stomp.commit.html)
    
-   [PHP Manual](index.html)
    
-   [Stomp](class.stomp.html)
    
-   Створює транзакцію
    

# Stomp::begin

# stompbegin

(PECL stomp >= 0.1.0)

Stomp::begin -- stompbegin - Створює транзакцію

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

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stompconnect()](stomp.construct.html)

`transaction_id`

Ідентифікатор транзакції.

`headers`

Асоціативний масив, який містить додаткові заголовки (приклад: receipt).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

Дивіться [stompcommit()](stomp.commit.html) або [stompabort()](stomp.abort.html)

### Примітки

**Підказка**

Stomp асинхронний за своєю суттю. Синхронний зв'язок може бути реалізований додаванням receipt-заголовка. Це змусить методи нічого не повертати, поки сервер не підтвердить отримання повідомлення або буде перевищено час очікування повідомлення.
Реєструє передплату на вказану розсилку

-   [« Stomp::setReadTimeout](stomp.setreadtimeout.md)
    
-   [Stomp::unsubscribe »](stomp.unsubscribe.md)
    
-   [PHP Manual](index.md)
    
-   [Stomp](class.stomp.md)
    
-   Реєструє передплату на вказану розсилку
    

# Stomp::subscribe

# stompsubscribe

(PECL stomp >= 0.1.0)

Stomp :: subscribe -- stompsubscribe — Зареєструє передплату на вказану розсилку

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

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stompconnect()](stomp.construct.md)

`destination`

Розсилання, на яке необхідно зареєструвати передплату.

`headers`

Асоціативний масив, який містить додаткові заголовки (приклад: receipt).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

Дивіться [stompack()](stomp.ack.md)

### Примітки

**Підказка**

Stomp асинхронний за своєю суттю. Синхронний зв'язок може бути реалізований додаванням receipt-заголовка. Це змусить методи нічого не повертати, поки сервер не підтвердить отримання повідомлення або буде перевищено час очікування повідомлення.
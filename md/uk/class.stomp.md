Клас Stomp

-   [« stompversion](function.stomp-version.html)
    
-   [Stomp::abort »](stomp.abort.md)
    
-   [PHP Manual](index.md)
    
-   [Stomp](book.stomp.md)
    
-   Клас Stomp
    

# Клас Stomp

(PECL stomp >= 0.1.0)

## Вступ

Представляє зв'язок між PHP та Stomp сумісним брокером повідомлень (Message Broker).

## Огляд класів

```classsynopsis



    
     
      class Stomp
     
     {


    /* Методы */
    
    public __construct(    string $broker = ini_get("stomp.default_broker_uri"),    string $username = ?,    string $password = ?,    array $headers = ?)

    public abort(string $transaction_id, array $headers = ?): bool
stomp_abort(resource $link, string $transaction_id, array $headers = ?): bool
public ack(mixed $msg, array $headers = ?): bool
stomp_ack(resource $link, mixed $msg, array $headers = ?): bool
public begin(string $transaction_id, array $headers = ?): bool
stomp_begin(resource $link, string $transaction_id, array $headers = ?): bool
public commit(string $transaction_id, array $headers = ?): bool
stomp_commit(resource $link, string $transaction_id, array $headers = ?): bool
stomp_connect(    string $broker = ini_get("stomp.default_broker_uri"),    string $username = ?,    string $password = ?,    array $headers = ?): resource
stomp_close(resource $link): bool
public error(): string
stomp_error(resource $link): string
public getReadTimeout(): array
stomp_get_read_timeout(resource $link): array
public getSessionId(): string|false
stomp_get_session_id(resource $link): string|false
public hasFrame(): bool
stomp_has_frame(resource $link): bool
public readFrame(string $class_name = "stompFrame"): stompframe
stomp_read_frame(resource $link): array
public send(string $destination, mixed $msg, array $headers = ?): bool
stomp_send(    resource $link,    string $destination,    mixed $msg,    array $headers = ?): bool
public setReadTimeout(int $seconds, int $microseconds = ?): void
stomp_set_read_timeout(resource $link, int $seconds, int $microseconds = ?): void
public subscribe(string $destination, array $headers = ?): bool
stomp_subscribe(resource $link, string $destination, array $headers = ?): bool
public unsubscribe(string $destination, array $headers = ?): bool
stomp_unsubscribe(resource $link, string $destination, array $headers = ?): bool

    public __destruct()

   }
```

## Зміст

-   [Stomp::abort](stomp.abort.md) — Скасує виконання поточної транзакції
-   [Stomp::ack](stomp.ack.md) — Підтверджує отримання повідомлення
-   [Stomp::begin](stomp.begin.md) - Створює транзакцію
-   [Stomp::commit](stomp.commit.md) - Виконує поточну транзакцію
-   [Stomp::construct](stomp.construct.md) - Відкриває з'єднання
-   [Stomp::destruct](stomp.destruct.md) - Закриває Stomp-з'єднання
-   [Stomp::error](stomp.error.md) - Повертає останню помилку Stomp
-   [Stomp::getReadTimeout](stomp.getreadtimeout.md) — Повертає час максимального очікування на операцію читання
-   [Stomp::getSessionId](stomp.getsessionid.md) - Повертає ідентифікатор поточної сесії Stomp
-   [Stomp::hasFrame](stomp.hasframe.md) — Перевіряє, чи можливе читання кадру
-   [Stomp::readFrame](stomp.readframe.md) — Виконує операцію для читання наступного кадру
-   [Stomp::send](stomp.send.md) — Надсилає повідомлення
-   [Stomp::setReadTimeout](stomp.setreadtimeout.md) - Встановлює граничний час очікування операції читання
-   [Stomp::subscribe](stomp.subscribe.md) — Реєструє передплату на вказану розсилку
-   [Stomp::unsubscribe](stomp.unsubscribe.md) — Видаляє існуючу передплату
Повертає, чи мітка помилки пов'язана з винятком

-   [« MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.html)
    
-   [MongoDB\\Driver\\Exception\\ServerException »](class.mongodb-driver-exception-serverexception.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.html)
    
-   Повертає, чи мітка помилки пов'язана з винятком
    

# MongoDBDriverExceptionRuntimeException::hasErrorLabel

(mongodb >= 1.6.0)

MongoDBDriverExceptionRuntimeException::hasErrorLabel — Повертає, чи мітка помилки пов'язана з винятком

### Опис

```methodsynopsis
final public MongoDB\Driver\Exception\RuntimeException::hasErrorLabel(string $errorLabel): bool
```

Повертає, чи було встановлено `errorLabel` для цього виняток. Мітки помилок встановлюються або сервером, або драйвером, щоб вказати конкретні ситуації, в яких може знадобитися прийняти рішення щодо способу обробки конкретного виключення. Такою ситуацією може бути перевірка, чи можна безпечно повторити транзакцію, яка не вдалася через тимчасову помилку (наприклад, проблеми з мережею або конфлікт транзакцій). Прикладами міток помилок є `TransientTransactionError` і `UnknownTransactionCommitResult`

### Список параметрів

`errorLabel`

Назва `errorLabel` для перевірки.

### Значення, що повертаються

Чи пов'язане передане значення параметра `errorLabel` з відповідним винятком.

### Дивіться також

-   [MongoDB\\Driver\\Session::commitTransaction()](mongodb-driver-session.committransaction.html) - Фіксує транзакцію
-   [» Документация MongoDB по транзакциям](https://www.mongodb.com/docs/manual/core/transactions/)
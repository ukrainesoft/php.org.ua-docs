---
navigation:
  - class.mongodb-driver-exception-runtimeexception.md: « MongoDB\\Driver\\Exception\\RuntimeException
  - class.mongodb-driver-exception-serverexception.md: MongoDB\\Driver\\Exception\\ServerException »
  - index.md: PHP Manual
  - class.mongodb-driver-exception-runtimeexception.md: MongoDB\\Driver\\Exception\\RuntimeException
title: 'MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel

(mongodb >= 1.6.0)

MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel — Повертає, чи мітка помилки пов'язана з винятком

### Опис

```methodsynopsis
final public MongoDB\Driver\Exception\RuntimeException::hasErrorLabel(string $errorLabel): bool
```

Повертає, чи було встановлено `errorLabel` для цього виняток. Мітки помилок встановлюються або сервером, або драйвером, щоб вказати конкретні ситуації, в яких може знадобитися прийняти рішення щодо способу обробки конкретного виключення. Такою ситуацією може бути перевірка, чи можна безпечно повторити транзакцію, яка не вдалася через тимчасову помилку (наприклад, проблеми з мережею або конфлікт транзакцій). Прикладами міток помилок є `TransientTransactionError`и`UnknownTransactionCommitResult`

### Список параметрів

`errorLabel`

Название`errorLabel` для перевірки.

### Значення, що повертаються

Связана ли переданное значение параметра`errorLabel` з відповідним винятком.

### Дивіться також

-   [MongoDB\\Driver\\Session::commitTransaction()](mongodb-driver-session.committransaction.md) \- Фіксує транзакцію
-   [» Документація MongoDB щодо транзакцій](https://www.mongodb.com/docs/manual/core/transactions/)

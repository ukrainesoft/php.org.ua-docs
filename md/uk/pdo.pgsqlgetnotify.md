---
navigation:
  - pdo.pgsqlcopytofile.md: '« PDO::pgsqlCopyToFile'
  - pdo.pgsqlgetpid.md: 'PDO::pgsqlGetPid »'
  - index.md: PHP Manual
  - ref.pdo-pgsql.md: PostgreSQL (PDO)
title: 'PDO::pgsqlGetNotify'
---
# PDO::pgsqlGetNotify

(PHP 5> = 5.6.0, PHP 7, PHP 8)

PDO::pgsqlGetNotify — Отримати асинхронне повідомлення

### Опис

```methodsynopsis
public PDO::pgsqlGetNotify(int $result_type = PDO::FETCH_USE_DEFAULT, int $ms_timeout = 0): array|false
```

Повертає результуючий набір, який представляє очікування асинхронного повідомлення.

### Список параметрів

`result_type`

Формат, в якому має повернутися результуючий набір, представлений як одна з констант [**`PDO::FETCH_*`**](pdostatement.fetch.md)

`ms_timeout`

Час очікування відповіді у мілісекундах.

### Значення, що повертаються

Якщо одне або більше повідомлень знаходяться в режимі очікування, повертає один рядок з полями `message` і `pid`, інакше повертає **`false`**

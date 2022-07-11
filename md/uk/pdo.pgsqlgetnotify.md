- [« PDO::pgsqlCopyToFile](pdo.pgsqlcopytofile.md)
- [PDO::pgsqlGetPid »](pdo.pgsqlgetpid.md)

- [PHP Manual](index.md)
- [PostgreSQL (PDO)](ref.pdo-pgsql.md)
- Отримати асинхронне повідомлення

# PDO::pgsqlGetNotify

(PHP 5 \>= 5.6.0, PHP 7, PHP 8)

PDO::pgsqlGetNotify — Отримати асинхронне повідомлення

### Опис

public **PDO::pgsqlGetNotify**(int `$result_type` =
**`PDO::FETCH_USE_DEFAULT`**, int `$ms_timeout` = 0): array\|false

Повертає результуючий набір, що представляє очікування асинхронного
повідомлення.

### Список параметрів

`result_type`
Формат, у якому має повернутися результуючий набір, представлений
як одна з констант [**`PDO::FETCH_*`**](pdostatement.fetch.md).

`ms_timeout`
Час очікування відповіді у мілісекундах.

### Значення, що повертаються

Якщо одне або більше повідомлень знаходяться в режимі очікування, повертається
один рядок з полями `message` та `pid`, інакше повертає **`false`**.

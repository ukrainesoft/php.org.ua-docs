Отримати асинхронне повідомлення

-   [« PDO::pgsqlCopyToFile](pdo.pgsqlcopytofile.html)
    
-   [PDO::pgsqlGetPid »](pdo.pgsqlgetpid.html)
    
-   [PHP Manual](index.html)
    
-   [PostgreSQL (PDO)](ref.pdo-pgsql.html)
    
-   Отримати асинхронне повідомлення
    

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

Формат, в якому має повернутися результуючий набір, представлений як одна з констант [**`PDO::FETCH_*`**](pdostatement.fetch.html)

`ms_timeout`

Час очікування відповіді у мілісекундах.

### Значення, що повертаються

Якщо одне або більше повідомлень знаходяться в режимі очікування, повертає один рядок з полями `message` і `pid`, інакше повертає **`false`**
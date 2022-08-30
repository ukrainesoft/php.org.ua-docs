Створює новий об'єкт колекції

-   [« ocilobісequal](function.oci-lob-is-equal.html)
    
-   [ocinewconnect »](function.oci-new-connect.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Створює новий об'єкт колекції
    

# ocinewcollection

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocinewcollection — Створює новий об'єкт колекції

### Опис

```methodsynopsis
oci_new_collection(resource $connection, string $type_name, ?string $schema = null): OCICollection|false
```

Створює новий об'єкт колекції.

### Список параметрів

`connection`

Ідентифікатор з'єднання з сервером Oracle, який повертається функцією [ociconnect()](function.oci-connect.html) або [ocipconnect()](function.oci-pconnect.html)

`type_name`

Має бути коректним ім'ям типу (у верхньому регістрі).

`schema`

Має бути зазначена схема даних, де створено іменований тип. Якщо передано значення **`null`**, вказується ім'я користувача як ім'я схеми.

### Значення, що повертаються

Повертає новий об'єкт [OCICollection](class.ocicollection.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | `schema` тепер допускає значення null. |

### Примітки

> **Зауваження**
> 
> Клас [OCICollection](class.ocicollection.html) називався **OCI-Collection** до PHP 8 та OCI8 3.0.0.

> **Зауваження**
> 
> У версіях PHP нижче 5.0.0 ця функція називалася [ocinewcollection()](function.ocinewcollection.html). У PHP 5.0.0 і вище [ocinewcollection()](function.ocinewcollection.html) є аліасом \*\*ocinewcollection()\*\*Тому ви можете продовжувати використовувати це ім'я, однак це не рекомендується.
---
navigation:
  - ref.ibm-db2.md: « Функції IBM DB2
  - function.db2-bind-param.md: db2bindparam »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2autocommit
---
# db2autocommit

(PECL ibmdb2> = 1.0.0)

db2autocommit — Повертає або встановлює режим підтвердження транзакцій для з'єднання.

### Опис

```methodsynopsis
db2_autocommit(resource $connection, bool $value = ?): mixed
```

Повертає або встановлює режим підтвердження транзакцій для зазначеного з'єднання.

### Список параметрів

`connection`

Змінна, що містить активний ресурс підключення, отриманий за допомогою [db2connect()](function.db2-connect.md) або [db2pconnect()](function.db2-pconnect.md)

`value`

Одна з наступних констант:

`DB2_AUTOCOMMIT_OFF`

Вимикає автопідтвердження.

`DB2_AUTOCOMMIT_ON`

Включає підтвердження авто.

### Значення, що повертаються

Якщо в **db2autocommit()** передати лише параметр `connection`, вона поверне значення поточного режиму для цього з'єднання у вигляді цілого числа, що приймає значення **`DB2_AUTOCOMMIT_OFF`**, якщо автопідтвердження вимкнено та **`DB2_AUTOCOMMIT_ON`**, якщо увімкнено.

Якщо в **db2autocommit()** передані обидва параметри, `connection` і `autocommit`, вона спробує встановити для заданого з'єднання вказаний режим автопідтвердження. Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Отримання поточного режиму автопідтвердження транзакцій**

У наступному прикладі ми створимо з'єднання з відключеним автопідтвердженням та перевіримо його за допомогою **db2autocommit()**

```php
<?php
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF);
$conn = db2_connect($database, $user, $password, $options);
$ac = db2_autocommit($conn);
if ($ac == DB2_AUTOCOMMIT_OFF) {
    print "$ac -- автоподтверждение включено.";
} else {
    print "$ac -- автоподтверждение отключено.";
}
?>
```

Результат виконання цього прикладу:

```
0 -- автоподтверждение отключено.
```

**Приклад #2 Встановлення режиму автопідтвердження транзакції**

У наступному прикладі ми створимо з'єднання з відключеним підтвердженням авто, після чого його включимо і перевіримо.

```php
<?php
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF);
$conn = db2_connect($database, $user, $password, $options);

// Включаем автоподтверждение
$rc = db2_autocommit($conn, DB2_AUTOCOMMIT_ON);
if ($rc) {
    print "Автоподтверждение успешно включено.\n";
}

// ппроверяет текущий режим
$ac = db2_autocommit($conn);
if ($ac == DB2_AUTOCOMMIT_OFF) {
    print "$ac -- автоподтверждение включено.";
} else {
    print "$ac -- автоподтверждение отключено.";
}
?>
```

Результат виконання цього прикладу:

```
Автоподтверждение успешно включено.
1 -- автоподтверждение включено.
```

### Дивіться також

-   [db2connect()](function.db2-connect.md) - Повертає з'єднання з базою даних
-   [db2pconnect()](function.db2-pconnect.md) - Повертає постійне з'єднання з базою даних

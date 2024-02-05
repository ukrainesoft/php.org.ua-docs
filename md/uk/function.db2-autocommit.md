---
navigation:
  - ref.ibm-db2.md: « Функції IBM DB2
  - function.db2-bind-param.md: db2\_bind\_param »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_autocommit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_autocommit

(PECL ibm\_db2 >= 1.0.0)

db2\_autocommit — Повертає або встановлює режим підтвердження транзакцій для з'єднання.

### Опис

```methodsynopsis
db2_autocommit(resource $connection, int $value = ?): int|bool
```

Повертає або встановлює режим підтвердження транзакцій для зазначеного з'єднання.

### Список параметрів

`connection`

Змінна, що містить активний ресурс підключення, отриманий за допомогою [db2\_connect()](function.db2-connect.md) або [db2\_pconnect()](function.db2-pconnect.md)

`value`

Одна з наступних констант:

`DB2_AUTOCOMMIT_OFF`

Вимикає автопідтвердження.

`DB2_AUTOCOMMIT_ON`

Включає підтвердження авто.

### Значення, що повертаються

Якщо в **db2\_autocommit()** передати лише параметр `connection`, вона поверне значення поточного режиму для цього з'єднання у вигляді цілого числа, що приймає значення **`DB2_AUTOCOMMIT_OFF`**, если автоподтверждение отключено и\*\*`DB2_AUTOCOMMIT_ON`\*\*, якщо увімкнено.

Якщо в **db2\_autocommit()** передані обидва параметри, `connection`и`autocommit`, вона спробує встановити для заданого з'єднання вказаний режим автопідтвердження. Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Отримання поточного режиму автопідтвердження транзакцій**

У наступному прикладі ми створимо з'єднання з відключеним автопідтвердженням та перевіримо його за допомогою **db2\_autocommit()**

```php
<?php
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF);
$conn = db2_connect($database, $user, $password, $options);
$ac = db2_autocommit($conn);
if ($ac == DB2_AUTOCOMMIT_OFF) {
    print "$ac -- автоподтверждение включено.";
} else {
    print "$ac -- автоподтверждение отключено.";
}
?>
```

Результат виконання наведеного прикладу:

```
0 -- автоподтверждение отключено.
```

**Приклад #2 Встановлення режиму автопідтвердження транзакції**

У наступному прикладі ми створимо з'єднання з відключеним підтвердженням авто, після чого його включимо і перевіримо.

```php
<?php
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF);
$conn = db2_connect($database, $user, $password, $options);

// Включаем автоподтверждение
$rc = db2_autocommit($conn, DB2_AUTOCOMMIT_ON);
if ($rc) {
    print "Автоподтверждение успешно включено.\n";
}

// ппроверяет текущий режим
$ac = db2_autocommit($conn);
if ($ac == DB2_AUTOCOMMIT_OFF) {
    print "$ac -- автоподтверждение включено.";
} else {
    print "$ac -- автоподтверждение отключено.";
}
?>
```

Результат виконання наведеного прикладу:

```
Автоподтверждение успешно включено.
1 -- автоподтверждение включено.
```

### Дивіться також

-   [db2\_connect()](function.db2-connect.md) \- Повертає з'єднання з базою даних
-   [db2\_pconnect()](function.db2-pconnect.md) \- Повертає постійне з'єднання з базою даних

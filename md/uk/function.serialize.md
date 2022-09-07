---
navigation:
  - function.print-r.md: « printр
  - function.settype.md: settype »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: serialize
---
# serialize

(PHP 4, PHP 5, PHP 7, PHP 8)

serialize - Генерує придатне для зберігання уявлення змінної

### Опис

```methodsynopsis
serialize(mixed $value): string
```

Генерує придатне для зберігання уявлення змінної.

Це корисно для зберігання або передачі значень PHP між скриптами без втрати їх типу та структури.

Для перетворення серіалізованого рядка назад на PHP-значення, використовуйте функцію [unserialize()](function.unserialize.md)

### Список параметрів

`value`

Значення, яке потрібно серіалізувати . **serialize()** обробляє всі типи, крім resource та деяких типів об'єкта (див. примітку нижче). Можна також серіалізувати масиви, які містять посилання на себе. Циклічні посилання всередині масиву/об'єкта, що серіалізується, також зберігаються. Будь-які інші посилання будуть втрачені.

При серіалізації об'єкта PHP намагається викликати магічні методи [serialize()](language.oop5.magic.md#object.serialize) або [sleep()](language.oop5.magic.md#object.sleep) перед серіалізацією. Це робиться для того, щоб дозволити об'єкту в останній момент провести очищення тощо перед серіалізацією. Аналогічно, коли об'єкт відновлюється функцією [unserialize()](function.unserialize.md), викликається магічний метод [unserialize()](language.oop5.magic.md#object.unserialize) або [wakeup()](language.oop5.magic.md#object.wakeup)

> **Зауваження**
> 
> Початок імен закритих членів об'єкта доповнюються іменем класу, а початок імен захищених членів символом ''. Ці доповнені значення оточуються нульовим байтом (0x00) з обох боків.

### Значення, що повертаються

Повертає рядок, що містить потокове подання змінної `value`, яка може бути збережена будь-де.

Зверніть увагу, що це бінарний рядок, який може включати нульові байти, і його потрібно зберігати та обробляти відповідним чином. Наприклад, виведення функції **serialize()** краще зберігати у BLOB-поле бази даних, а чи не в полях типу CHAR чи TEXT.

### Приклади

**Приклад #1 Приклад використання **serialize()****

```php
<?php
// $session_data содержит многомерный Масив с сессионной
// информацией о текущем пользователе. Мы используем serialize() для сохранения
// этой информации в базе данных в конце запроса.

$conn = odbc_connect("webdb", "php", "chicken");
$stmt = odbc_prepare($conn,
      "UPDATE sessions SET data = ? WHERE id = ?");
$sqldata = array (serialize($session_data), $_SERVER['PHP_AUTH_USER']);
if (!odbc_execute($stmt, $sqldata)) {
    $stmt = odbc_prepare($conn,
     "INSERT INTO sessions (id, data) VALUES(?, ?)");
    if (!odbc_execute($stmt, array_reverse($sqldata))) {
        /* Код, выполняемый в случае возникновения ошибки.. */
    }
}
?>
```

### Примітки

> **Зауваження**
> 
> Зверніть увагу, що багато вбудованих PHP об'єктів не може бути серіалізовано. Однак, ті з них, які підтримують цю можливість, реалізують або інтерфейс [Serializable](class.serializable.md), або магічні методи [serialize()](language.oop5.magic.md#object.serialize)[unserialize()](language.oop5.magic.md#object.unserialize) або [sleep()](language.oop5.magic.md#object.sleep)[wakeup()](language.oop5.magic.md#object.wakeup). Якщо вбудований клас не відповідає цим вимогам, він не може бути надійно серіалізований.
> 
> Історично є деякі винятки з вищезгаданого правила, коли деякі внутрішні об'єкти можуть бути серіалізовані без реалізації інтерфейсу або магічних методів.

**Увага**

При серіалізації об'єктів функцією **serialize()**, провідний зворотний сліш не буде включений в ім'я класу із зазначеним простором імен для кращої зворотної сумісності.

### Дивіться також

-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [varexport()](function.var-export.md) - Виводить або повертає інтерпретоване рядкове подання змінної
-   [jsonencode()](function.json-encode.md) - Повертає JSON-подання даних
-   [Серіалізація об'єктів](language.oop5.serialization.md)
-   [sleep()](language.oop5.magic.md#object.sleep)
-   [wakeup()](language.oop5.magic.md#object.wakeup)
-   [serialize()](language.oop5.magic.md#object.serialize)
-   [unserialize()](language.oop5.magic.md#object.unserialize)

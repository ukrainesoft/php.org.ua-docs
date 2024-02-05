---
navigation:
  - ldap.examples.md: « Приклади
  - ldap.examples-controls.md: LDAP Controls »
  - index.md: PHP Manual
  - ldap.examples.md: Приклади
title: Базове використання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Базове використання

Отримати інформацію для всіх записів, де прізвище починається з "S" із сервера каталогів, показуючи в результаті ім'я та адресу електронної пошти.

**Приклад #1 Приклад пошуку LDAP**

```php
<?php
// базовая последовательность работы с LDAP:
// подключение, привязка, поиск, интерпретация результата, закрытие подключения

echo "<h3>Проверочный запрос к LDAP</h3>";
echo "Подключение ...";
$ds=ldap_connect("localhost");  // Необходимо указать корректный LDAP сервер
echo "Результат подключения: " . $ds . "<br />";

if ($ds) {
    echo "Привязка ...";
    $r=ldap_bind($ds);     // "анонимная" привязка,
                           // доступ только для чтения
    echo "Результат привязки: " . $r . "<br />";

    echo "Поиск (sn=S*) ...";
    // Поиск по фамилиям записей
    $sr=ldap_search($ds, "o=My Company, c=US", "sn=S*");
    echo "Результат поиска: " . $sr . "<br />";

    echo "Получено количество записей " . ldap_count_entries($ds, $sr) . "<br />";

    echo "Получение элементов ...<p>";
    $info = ldap_get_entries($ds, $sr);
    echo "Элемент: " . $info["count"] . " Данные:<p>";

    for ($i=0; $i<$info["count"]; $i++) {
        echo "dn: " . $info[$i]["dn"] . "<br />";
        echo "первый cn: " . $info[$i]["cn"][0] . "<br />";
        echo "первый email: " . $info[$i]["mail"][0] . "<br /><hr />";
    }

    echo "Закрытие соединения";
    ldap_close($ds);

} else {
    echo "<h4>Невозможно подключиться к серверу LDAP</h4>";
}
?>
```

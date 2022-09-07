---
navigation:
  - expect.examples.md: « Приклади
  - ref.expect.md: Функции Expect »
  - index.md: PHP Manual
  - expect.examples.md: Приклади
title: Приклади використання Expect
---
## Приклади використання Expect

**Приклад #1 Приклад використання Expect**

У цьому прикладі ми з'єднаємося з віддаленим хостом SSH, і надрукуємо час безперервної роботи сервера.

```php
<?php
ini_set("expect.loguser", "Off");

$stream = fopen("expect://ssh root@remotehost uptime", "r");

$cases = array (
    array (0 => "password:", 1 => PASSWORD)
);

switch (expect_expectl ($stream, $cases)) {
    case PASSWORD:
        fwrite ($stream, "password\n");
        break;

    default:
        die ("Ошибка соединения с удалённым сервером!\n");
}

while ($line = fgets($stream)) {
      print $line;
}
fclose ($stream);
?>
```

У наступному прикладі ми з'єднаємося з віддаленим сервером, дізнаємося про розрядність його операційної системи і запустимо оновлення зазначеного пакета.

**Приклад #2 Ще один приклад використання Expect**

```php
<?php
ini_set("expect.timeout", -1);
ini_set("expect.loguser", "Off");

$stream = expect_popen("ssh root@remotehost");

while (true) {
    switch (expect_expectl ($stream, array (
            array ("password:", PASSWORD), // SSH запрашивает пароль
            array ("yes/no)?", YESNO), // SSH спрашивает, сохранять ли запись хоста
            array ("~$ ", SHELL, EXP_EXACT), // Мы получили доступ к коммандной оболочке!
    ))) {
        case PASSWORD:
            fwrite ($stream, "secret\n");
            break;

        case YESNO:
            fwrite ($stream, "yes\n");
            break;

        case SHELL:
            fwrite ($stream, "uname -a\n");
            while (true) {
                    switch (expect_expectl ($stream, array (
                            array ("~$ ", SHELL, EXP_EXACT), // Мы получили доступ к коммандной оболочке!
                            array ("^Linux.*$", UNAME, EXP_REGEXP), // вывод uname -a
                    ), $match)) {
                        case UNAME:
                            $uname .= $match[0];
                            break;

                        case SHELL:
                            // Run update:
                            if (strstr ($uname, "x86_64")) {
                                    fwrite ($stream, "rpm -Uhv http://mirrorsite/somepath/some_64bit.rpm\n");
                            } else {
                                    fwrite ($stream, "rpm -Uhv http://mirrorsite/somepath/some_32bit.rpm\n");
                            }
                            fwrite ($stream, "exit\n");
                            break 2;

                        case EXP_TIMEOUT:
                        case EXP_EOF:
                            break 2;

                        default:
                            die ("Случилась ошибка!\n");
                    }
            }
            break 2;

        case EXP_TIMEOUT:
        case EXP_EOF:
            break 2;

        default:
            die ("Случилась ошибка!\n");
    }
}

fclose ($stream);
?>
```

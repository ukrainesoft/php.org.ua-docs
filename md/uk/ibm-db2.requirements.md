---
navigation:
  - ibm-db2.setup.html: « Встановлення та налаштування
  - ibm-db2.installation.html: Установка »
  - index.md: PHP Manual
  - ibm-db2.setup.html: Встановлення та налаштування
title: Вимоги
---
## Вимоги

Для з'єднання з IBM DB2 Universal Database під Linux, UNIX і Windows, IBM Cloudscape або Apache Derby, ви повинні встановити клієнта IBM DB2 Universal Database на тій же машині, де працюватиме PHP. Модуль розроблявся та тестувався з DB2 версії 8.2.

Для з'єднання з IBM DB2 Universal Database під z/OS або iSeries вам потрібен IBM DB2 Connect або еквівалентне програмне забезпечення, здатне бути шлюзом DRDA.

## Вимоги під Linux чи Unix

Для доступу до функцій модуля з PHP, вам необхідно спочатку встановити екземпляр DB2 з яким ви будете працювати. Його можна задати у php.ini за допомогою опції `ibm_db2.instance_name` або можна створити профіль екземпляра DB2.

Якщо ви, наприклад, створите екземпляр DB2 з ім'ям `db2inst1` в /home/db2inst1/, ви можете додати наступний запис до php.ini:

```
ibm_db2.instance_name=db2inst1
```

Якщо ви не задали ім'я екземпляра php.ini, ви повинні виконати наступну команду, яка змінює змінні оточення, для доступу до DB2:

```
bash$ source /home/db2inst1/sqllib/db2profile
```

Для дозволу доступу вашому веб-серверу до функцій модуля, ви повинні або встановити опцію `ibm_db2.instance_name` у php.ini або забезпечити виставлення відповідних змінних оточення DB2 у вашому скрипті запуску веб-сервера (зазвичай це /etc/init.d/httpd або /etc/init.d/apache).

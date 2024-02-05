---
navigation:
  - mysqlnd.incompatibilities.md: « Несумісності
  - mysqlnd.stats.md: Статистика »
  - index.md: PHP Manual
  - book.mysqlnd.md: Mysqlnd
title: Постійне з'єднання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Постійне з'єднання

**Використання постійних з'єднань**

Якщо `mysqli` використовується з `mysqlnd`,\\ під час створення постійного з'єднання воно генерує на сервері запит `COM_CHANGE_USER` `mysql_change_user()`). Це гарантує, що при підключенні буде повторно зроблено авторизацію.

Оскільки через дзвінки `COM_CHANGE_USER` збільшуються накладні витрати, можна відключити таку поведінку під час компіляції. У такому разі повторне використання постійного з'єднання генеруватиме виклик `COM_PING` `mysql_ping`), для перевірки можливості повторного використання з'єднання.

Генерація виклику `COM_CHANGE_USER` може бути вимкнена прапором компіляції `MYSQLI_NO_CHANGE_USER_ON_PCONNECT`НаПриклад:

```
shell# CFLAGS="-DMYSQLI_NO_CHANGE_USER_ON_PCONNECT" ./configure --with-mysql=/usr/local/mysql/ --with-mysqli=/usr/local/mysql/bin/mysql_config --with-pdo-mysql=/usr/local/mysql/bin/mysql_config --enable-debug && make clean && make -j6
```

Або альтернативний варіант:

```
shell# export CFLAGS="-DMYSQLI_NO_CHANGE_USER_ON_PCONNECT"
shell# configure --whatever-option
shell# make clean
shell# make
```

Зверніть увагу, що тільки `mysqli` спільно з `mysqlnd` використовують `COM_CHANGE_USER`. Інші комбінації модуль-драйвер використовують `COM_PING` при первісному використанні постійного з'єднання.

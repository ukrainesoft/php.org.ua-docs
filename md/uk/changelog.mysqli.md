---
navigation:
  - function.mysqli-set-opt.md: '« mysqli::setopt'
  - book.mysql-xdevapi.md: Mysqlxdevapi »
  - index.md: PHP Manual
  - book.mysqli.md: MySQLi
title: список змін
---
# список змін

Наступні зміни були здійснені з класами/функціями/методами даного модуля.

| Version | Function | Description |
| --- | --- | --- |
|  | [mysqlidriver::$reportmode](mysqli-driver.report-mode.md) | Тепер за замовчуванням встановлено значення MYSQLIREPORTERROR |
|  | [mysqliresult::fetchall](mysqli-result.fetch-all.md) | Тепер також доступно при збиранні з libmysqlclient. |
|  | [mysqlistmt::execute](mysqli-stmt.execute.md) | Додано необов'язковий параметр params. |
|  | [mysqlistmt::nextresult](mysqli-stmt.next-result.md) | Тепер також доступно при збиранні з libmysqlclient. |
|  | [mysqli::$clientinfo](mysqli.get-client-info.md) | Виклик функції mysqligetclientinfo з аргументом mysql застарів. Функція ніколи не вимагала параметра, але неправильно дозволяла його як необов'язковий параметр. |
|  | [mysqli::$clientinfo](mysqli.get-client-info.md) | Об'єктно-орієнтований стиль виклику методу mysqli::getclientinfo застарів. |
|  | [mysqli::init](mysqli.init.md) | Об'єктно-орієнтований стиль виклику методу mysqli::init застарів. Замініть виклик методу parent::init за допомогою parent::construct. |
|  | [mysqliresult::fetchobject](mysqli-result.fetch-object.md) | constructorargs тепер приймає для конструкторів без параметрів; раніше викидався виняток. |
|  | [mysqlistmt::construct](mysqli-stmt.construct.md) | query тепер припускає значення null. |
|  | [mysqli::begintransaction](mysqli.begin-transaction.md) | name тепер припускає значення null. |
|  | [mysqli::commit](mysqli.commit.md) | name тепер припускає значення null. |
|  | [mysqli::rollback](mysqli.rollback.md) | name тепер припускає значення null. |

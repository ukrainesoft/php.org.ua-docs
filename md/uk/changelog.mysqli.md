список змін

-   [« mysqli::setopt](function.mysqli-set-opt.html)
    
-   [Mysqlxdevapi »](book.mysql-xdevapi.html)
    
-   [PHP Manual](index.html)
    
-   [MySQLi](book.mysqli.html)
    
-   список змін
    

# список змін

Наступні зміни були здійснені з класами/функціями/методами даного модуля.

| Version | Function                                                     | Description                                                                                                                                                      |
|---------|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|         | [mysqlidriver::$reportmode](mysqli-driver.report-mode.html)  | Тепер за замовчуванням встановлено значення MYSQLIREPORTERROR                                                                                                    |
|         | [mysqliresult::fetchall](mysqli-result.fetch-all.html)       | Тепер також доступно при збиранні з libmysqlclient.                                                                                                              |
|         | [mysqlistmt::execute](mysqli-stmt.execute.html)              | Додано необов'язковий параметр params.                                                                                                                           |
|         | [mysqlistmt::nextresult](mysqli-stmt.next-result.html)       | Тепер також доступно при збиранні з libmysqlclient.                                                                                                              |
|         | [mysqli::$clientinfo](mysqli.get-client-info.html)           | Виклик функції mysqligetclientinfo з аргументом mysql застарів. Функція ніколи не вимагала параметра, але неправильно дозволяла його як необов'язковий параметр. |
|         | [mysqli::$clientinfo](mysqli.get-client-info.html)           | Об'єктно-орієнтований стиль виклику методу mysqli::getclientinfo застарів.                                                                                       |
|         | [mysqli::init](mysqli.init.html)                             | Об'єктно-орієнтований стиль виклику методу mysqli::init застарів. Замініть виклик методу parent::init за допомогою parent::construct.                            |
|         | [mysqliresult::fetchobject](mysqli-result.fetch-object.html) | constructorargs тепер приймає для конструкторів без параметрів; раніше викидався виняток.                                                                        |
|         | [mysqlistmt::construct](mysqli-stmt.construct.html)          | query тепер припускає значення null.                                                                                                                             |
|         | [mysqli::begintransaction](mysqli.begin-transaction.html)    | name тепер припускає значення null.                                                                                                                              |
|         | [mysqli::commit](mysqli.commit.html)                         | name тепер припускає значення null.                                                                                                                              |
|         | [mysqli::rollback](mysqli.rollback.html)                     | name тепер припускає значення null.                                                                                                                              |
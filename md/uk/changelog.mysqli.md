список змін

-   [« mysqli::set\_opt](function.mysqli-set-opt.html)
    
-   [Mysql\_xdevapi »](book.mysql-xdevapi.html)
    
-   [PHP Manual](index.html)
    
-   [MySQLi](book.mysqli.html)
    
-   список змін
    

# список змін

Наступні зміни були здійснені з класами/функціями/методами даного модуля.

| Version | Function                                                         | Description                                                                                                                                                      |
|---------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|         | [mysqli\_driver::$report\_mode](mysqli-driver.report-mode.html)  | Тепер за замовчуванням встановлено значення MYSQLIREPORTERROR                                                                                                    |
|         | [mysqli\_result::fetch\_all](mysqli-result.fetch-all.html)       | Тепер також доступно при збиранні з libmysqlclient.                                                                                                              |
|         | [mysqli\_stmt::execute](mysqli-stmt.execute.html)                | Додано необов'язковий параметр params.                                                                                                                           |
|         | [mysqli\_stmt::next\_result](mysqli-stmt.next-result.html)       | Тепер також доступно при збиранні з libmysqlclient.                                                                                                              |
|         | [mysqli::$client\_info](mysqli.get-client-info.html)             | Виклик функції mysqligetclientinfo з аргументом mysql застарів. Функція ніколи не вимагала параметра, але неправильно дозволяла його як необов'язковий параметр. |
|         | [mysqli::$client\_info](mysqli.get-client-info.html)             | Об'єктно-орієнтований стиль виклику методу mysqli::getclientinfo застарів.                                                                                       |
|         | [mysqli::init](mysqli.init.html)                                 | Об'єктно-орієнтований стиль виклику методу mysqli::init застарів. Замініть виклик методу parent::init за допомогою parent::construct.                            |
|         | [mysqli\_result::fetch\_object](mysqli-result.fetch-object.html) | constructorargs тепер приймає для конструкторів без параметрів; раніше викидався виняток.                                                                        |
|         | [mysqli\_stmt::\_\_construct](mysqli-stmt.construct.html)        | query тепер припускає значення null.                                                                                                                             |
|         | [mysqli::begin\_transaction](mysqli.begin-transaction.html)      | name тепер припускає значення null.                                                                                                                              |
|         | [mysqli::commit](mysqli.commit.html)                             | name тепер припускає значення null.                                                                                                                              |
|         | [mysqli::rollback](mysqli.rollback.html)                         | name тепер припускає значення null.                                                                                                                              |
- [« Yaf_Application::getLastErrorMsg](yaf-application.getlasterrormsg.md)
- [Yaf_Application::getModules »](yaf-application.getmodules.md)

- [PHP Manual](index.md)
- [Yaf_Application](class.yaf-application.md)
- Отримати код останньої помилки

# Yaf_Application::getLastErrorNo

(Yaf \> = 2.1.2)

Yaf_Application::getLastErrorNo — Отримати код останньої помилки

### Опис

public **Yaf_Application::getLastErrorNo**(): int

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **Yaf_Application::getLastErrorNo()****

` <?phpfunction error_handler($errno, $errstr, $errfile, $errline) {   var_dump(Yaf_Application::app()->getLastErrorNo()); var_dump(Yaf_Application::app()->getLastErrorNo() ==YAF_ERR_NOTFOUND_CONTROLLER);}$config = array( "application" => array(   "directory" => "/t "throwException" => 0, //викликати помилку замість виключення      ),  ),);$app = new Yaf_Application($config);$app->getDispatcher()->setErrorHandler$" >run();?> `

Результатом виконання цього прикладу буде щось подібне:

int(516)
bool(true)

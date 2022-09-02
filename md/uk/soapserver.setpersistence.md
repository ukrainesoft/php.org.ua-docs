---
navigation:
  - soapserver.setobject.md: '« SoapServer::setObject'
  - class.soapfault.md: SoapFault »
  - index.md: PHP Manual
  - class.soapserver.md: SoapServer
title: 'SoapServer::setPersistence'
---
# SoapServer::setPersistence

(PHP 5, PHP 7, PHP 8)

SoapServer::setPersistence — Встановлює режим збереження SoapServer

### Опис

```methodsynopsis
public SoapServer::setPersistence(int $mode): void
```

Ця функція дозволяє змінювати режим збереження об'єкта SoapServer між запитами. Ця функція дозволяє зберігати дані між запитами, використовуючи механізм сесій PHP. Цей метод впливає лише на SoapServer після експорту функцій, використовуючи [SoapServer::setClass()](soapserver.setclass.md)

> **Зауваження**
> 
> Збереження **`SOAP_PERSISTENCE_SESSION`** гарантує збереження лише об'єктів заданого класу, але з статичні дані класу. У цьому випадку використовуйте $this->bar замість self::$bar.

> **Зауваження**
> 
> **`SOAP_PERSISTENCE_SESSION`** серіалізує дані об'єкта класу та зберігає їх між запитами. Для коректної роботи з ресурсами (наприклад, [PDO](class.pdo.md)), слід використовувати магічні методи [wakeup()](language.oop5.magic.md#object.wakeup) і [sleep()](language.oop5.magic.md#object.sleep)

### Список параметрів

`mode`

Одна з констант `SOAP_PERSISTENCE_XXX`

**`SOAP_PERSISTENCE_REQUEST`** - дані SoapServer не зберігаються між запитами. Ця поведінка *за замовчуванням* будь-якого об'єкта SoapServer після виклику setClass.

**`SOAP_PERSISTENCE_SESSION`** - Дані SoapServer зберігаються між запитами. Це досягається шляхом серіалізації об'єкта SoapServer в [SESSION\['bogussessionname'\]](reserved.variables.session.md), отже необхідно викликати [sessionstart()](function.session-start.md) перед увімкненням цього режиму.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **SoapServer::setPersistence()****

```php
<?php
 class MyFirstPersistentSoapServer {
     private $resource; // (Такие как PDO, mysqli и т.д.)
     public $myvar1;
     public $myvar2;

     public function __construct() {
         $this->__wakeup(); // Вызываем __wakeup для пересоздания $resource
     }

     public function __wakeup() {
         $this->resource = CodeToStartOurResourceUp();
     }

     public function __sleep() {
         // Не сохраняем $resource здесь.
         // Ошибка в этом методе приведёт к тому, что при последующей десериализации
         // мы не сможем восстановить состояние объекта.
         return array('myvar1','myvar2');
     }
 }

 try {
     session_start();
     $server = new SoapServer(null, array('uri' => $_SERVER['REQUEST_URI']));
     $server->setClass('MyFirstPersistentSoapServer');
     // setPersistence НЕОБХОДИМО вызвать после setClass, поскольку setClass
     // принудительно устанавливает SESSION_PERSISTENCE_REQUEST.
     $server->setPersistence(SOAP_PERSISTENCE_SESSION);
     $server->handle();
 } catch(SoapFault $e) {
     error_log("ОШИБКА SOAP: ". $e->getMessage());
 }
?>
```

### Дивіться також

-   [SoapServer::setClass()](soapserver.setclass.md) - Встановлює клас, який обробляє SOAP-запити

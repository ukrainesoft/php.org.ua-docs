---
navigation:
  - arrayaccess.offsetunset.md: '« ArrayAccess::offsetUnset'
  - serializable.serialize.md: 'Serializable::serialize »'
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Інтерфейс Serializable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс Serializable

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

Інтерфейс для персональної серіалізації.

Класи, які реалізують цей інтерфейс, більше не підтримують [\_\_sleep()](language.oop5.magic.md#object.sleep) і [\_\_wakeup()](language.oop5.magic.md#object.wakeup). Метод serialize викликається щоразу, коли необхідна серіалізація екземпляру класу. Цей метод не викликає \_\_destruct() і немає ніяких побічних дій крім тих, які запрограмовані всередині нього. Коли дані десеріалізуються, клас відомий і відповідний метод unserialize() викликається як конструктор замість виклику \_\_construct(). Якщо вам необхідно викликати стандартний конструктор, ви можете зробити це в цьому методі.

**Увага**

Починаючи з PHP 8.1.0 клас, який реалізує **Serializable**без реализации[\_\_serialize()](language.oop5.magic.md#object.serialize) і [\_\_unserialize()](language.oop5.magic.md#object.unserialize) видасть попередження про старіння

## Огляд інтерфейсів

```classsynopsis

    
     interface Serializable {

    /* Методы */
    
   public serialize(): ?string
public unserialize(string $data): void

   }
```

**Приклад #1 Основи використання**

```php
<?php
class obj implements Serializable {
    private $data;
    public function __construct() {
        $this->data = "Мои закрытые данные";
    }
    public function serialize() {
        return serialize($this->data);
    }
    public function unserialize($data) {
        $this->data = unserialize($data);
    }
    public function getData() {
        return $this->data;
    }
}

$obj = new obj;
$ser = serialize($obj);

var_dump($ser);

$newobj = unserialize($ser);

var_dump($newobj->getData());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(59) "C:3:"obj":44:{s:36:"Мои закрытые данные";}"
string(36) "Мои закрытые данные"
```

## Зміст

-   [Serializable::serialize](serializable.serialize.md)— Представляє об'єкт у вигляді рядка
-   [Serializable::unserialize](serializable.unserialize.md) \- Створює об'єкт

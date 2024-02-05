---
navigation:
  - yaf-config-abstract.toarray.md: '« Yaf\_Config\_Abstract::toArray'
  - yaf-config-ini.construct.md: 'Yaf\_Config\_Ini::\_\_construct »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Config\_Ini
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Config\_Ini

(Yaf >=1.0.0)

## Вступ

Yaf\_Config\_Ini дозволяє розробникам зберігати конфігураційні дані у відомому форматі INI і читати їх у додатку з використанням синтаксису вкладених властивостей об'єкта. INI формат спеціалізується на забезпеченні можливості мати ієрархію ключів конфігураційних даних та успадкування між розділами конфігураційних даних. Ієрархія конфігураційних даних підтримується шляхом поділу ключів із точкою ("."). Розділи можна розширювати або успадковувати від інших розділів шляхом проставлення після імені розділу двокрапки (":") та назви розділу від якого дані успадковані.

> **Зауваження** :
> 
> Yaf\_Config\_Ini використовує функцію parse\_ini\_file(). Будь ласка, вивчіть документацію для розуміння її поведінки, яка успадковує Yaf\_Config\_Ini, такого як обробка спеціальних значень "**`true`**", "**`false`**", "yes", "no", і "**`null`**".

## Огляд класів

```classsynopsis



    
     
      class Yaf_Config_Ini
     

     
      extends
       Yaf_Config_Abstract
     

     implements 
       Iterator,  ArrayAccess,  Countable {

    /* Свойства */


    /* Методы */
    
   public __construct(string $config_file, string $section = ?)

    public count(): void
public current(): void
public __get(string $name = ?): void
public __isset(string $name): void
public key(): void
public next(): void
public offsetExists(string $name): void
public offsetGet(string $name): void
public offsetSet(string $name, string $value): void
public offsetUnset(string $name): void
public readonly(): void
public rewind(): void
public __set(string $name, mixed $value): void
public toArray(): array
public valid(): void


    /* Наследуемые методы */
    abstract public Yaf_Config_Abstract::get(string $name, mixed $value): mixed
abstract public Yaf_Config_Abstract::readonly(): bool
abstract public Yaf_Config_Abstract::set(): Yaf_Config_Abstract
abstract public Yaf_Config_Abstract::toArray(): array


   }
```

## Властивості

\_config

\_readonly

## Приклади

\*\*Приклад #1 \*\*Yaf\_Config\_Ini()**example**

Цей приклад розкриває базові особливості використання Yaf\_Config\_Ini під час завантаження даних з INI-файлу. У цьому прикладі задається конфігурація для промислового та демонстраційного середовища. Так як конфігурація демо-середовища дуже схожа на конфігурацію промислової, то вона успадковує від неї. Але ви у своїх додатках вільні чинити як хочете. Загалом, така конфігурація задана в /path/to/config.ini:

; Промислове середовище\[production\]webhost =[www.example.com](http://www.example.com)database.adapter = pdo\_mysql database.params.host = db.example.com database.params.username = dbuser database.params.password = secret database.params.dbname = dbname

; Демо-середовище. Наслідує конфігурацію промислової з деякими поправками\[staging : production\]database.params.host = dev.example.com database.params.username = devuser database.params.password = devsecret

```php
<?php
$config = new Yaf_Config_Ini('/path/to/config.ini', 'staging');

var_dump($config->database->params->host);
var_dump($config->database->params->dbname);
var_dump($config->get("database.params.username"));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(15) "dev.example.com"
string(6) "dbname"
string(7) "devuser
```

## Зміст

-   [Yaf\_Config\_Ini::\_\_construct](yaf-config-ini.construct.md) \- Конструктор класу Yaf\_Config\_Ini
-   [Yaf\_Config\_Ini::count](yaf-config-ini.count.md)— Підраховує всі елементи в Yaf\_Config.ini
-   [Yaf\_Config\_Ini::current](yaf-config-ini.current.md)— Отримує поточне значення
-   [Yaf\_Config\_Ini::\_\_get](yaf-config-ini.get.md)— Отримує елемент
-   [Yaf\_Config\_Ini::\_\_isset](yaf-config-ini.isset.md) \- Визначає, чи існує ключ
-   [Yaf\_Config\_Ini::key](yaf-config-ini.key.md)— Отримує ключ поточного елемента
-   [Yaf\_Config\_Ini::next](yaf-config-ini.next.md) \- Просуває внутрішній покажчик
-   [Yaf\_Config\_Ini::offsetExists](yaf-config-ini.offsetexists.md)— Призначення offsetExists
-   [Yaf\_Config\_Ini::offsetGet](yaf-config-ini.offsetget.md) \- Призначення offsetGet
-   [Yaf\_Config\_Ini::offsetSet](yaf-config-ini.offsetset.md) \- Призначення offsetSet
-   [Yaf\_Config\_Ini::offsetUnset](yaf-config-ini.offsetunset.md) \- Призначення offsetUnset
-   [Yaf\_Config\_Ini::readonly](yaf-config-ini.readonly.md) \- Призначення readonly
-   [Yaf\_Config\_Ini::rewind](yaf-config-ini.rewind.md) \- Призначення rewind
-   [Yaf\_Config\_Ini::\_\_set](yaf-config-ini.set.md) \- Призначення\_\_set
-   [Yaf\_Config\_Ini::toArray](yaf-config-ini.toarray.md)— Повертає конфігурацію як масив PHP
-   [Yaf\_Config\_Ini::valid](yaf-config-ini.valid.md) \- Призначення valid

---
navigation:
  - yaf-config-abstract.toarray.md: '« YafConfigAbstract::toArray'
  - yaf-config-ini.construct.md: 'YafConfigIni::construct »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас YafConfigIni
---
# Клас YafConfigIni

(Yaf >=1.0.0)

## Вступ

YafConfigIni дозволяє розробникам зберігати конфігураційні дані у відомому форматі INI і читати їх у додатку з використанням синтаксису вкладених властивостей об'єкта. INI формат спеціалізується на забезпеченні можливості мати ієрархію ключів конфігураційних даних та успадкування між розділами конфігураційних даних. Ієрархія конфігураційних даних підтримується шляхом поділу ключів із точкою ("."). Розділи можна розширювати або успадковувати від інших розділів шляхом проставлення після імені розділу двокрапки (":") та назви розділу від якого дані успадковані.

> **Зауваження**
> 
> YafConfigIni використовує функцію parseinifile(). Будь ласка, вивчіть документацію для розуміння її поведінки, яка успадковує YafConfigIni, такого як обробка спеціальних значень "**`true`**","**`false`**", "yes", "no", і "**`null`**".

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

config

readonly

## Приклади

\*\*Приклад #1 \*\*YafConfigIni()**example**

Цей приклад розкриває базові особливості використання YafConfigIni під час завантаження даних з INI-файлу. У цьому прикладі задається конфігурація для промислового та демонстраційного середовища. Так як конфігурація демо-середовища дуже схожа на конфігурацію промислової, то вона успадковує від неї. Але ви у своїх додатках вільні чинити як хочете. Загалом, така конфігурація задана в /path/to/config.ini:

; Промислове середовищеproductionwebhost = [www.example.com](http://www.example.com)database.adapter = pdomysql database.params.host = db.example.com database.params.username = dbuser database.params.password = secret database.params.dbname = dbname

; Демо-середовище. Наслідує конфігурацію промислової з деякими поправкамиstaging: productiondatabase.params.host = dev.example.com database.params.username=devuser database.params.password = devsecret

```php
<?php
$config = new Yaf_Config_Ini('/path/to/config.ini', 'staging');

var_dump($config->database->params->host);
var_dump($config->database->params->dbname);
var_dump($config->get("database.params.username"));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(15) "dev.example.com"
string(6) "dbname"
string(7) "devuser
```

## Зміст

-   [YafConfigIni::construct](yaf-config-ini.construct.md) - Конструктор класу YafConfigIni
-   [YafConfigIni::count](yaf-config-ini.count.md) — Підраховує всі елементи в YafConfig.ini
-   [YafConfigIni::current](yaf-config-ini.current.md) — Отримує поточне значення
-   [YafConfigIni::get](yaf-config-ini.get.md) — Отримує елемент
-   [YafConfigIni::isset](yaf-config-ini.isset.md) - Визначає, чи існує ключ
-   [YafConfigIni::key](yaf-config-ini.key.md) — Отримує ключ поточного елемента
-   [YafConfigIni::next](yaf-config-ini.next.md) - Просуває внутрішній покажчик
-   [YafConfigIni::offsetExists](yaf-config-ini.offsetexists.md) — Призначення offsetExists
-   [YafConfigIni::offsetGet](yaf-config-ini.offsetget.md) - Призначення offsetGet
-   [YafConfigIni::offsetSet](yaf-config-ini.offsetset.md) - Призначення offsetSet
-   [YafConfigIni::offsetUnset](yaf-config-ini.offsetunset.md) - Призначення offsetUnset
-   [YafConfigIni::readonly](yaf-config-ini.readonly.md) - Призначення readonly
-   [YafConfigIni::rewind](yaf-config-ini.rewind.md) - Призначення rewind
-   [YafConfigIni::set](yaf-config-ini.set.md) - Призначення set
-   [YafConfigIni::toArray](yaf-config-ini.toarray.md) — Повертає конфігурацію як масив PHP
-   [YafConfigIni::valid](yaf-config-ini.valid.md) - Призначення valid

---
navigation:
  - yaf-view-simple.clear.md: '« Yaf\_View\_Simple::clear'
  - yaf-view-simple.display.md: 'Yaf\_View\_Simple::display »'
  - index.md: PHP Manual
  - class.yaf-view-simple.md: Yaf\_View\_Simple
title: 'Yaf\_View\_Simple::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_View\_Simple::\_\_construct

(Yaf >=1.0.0)

Yaf\_View\_Simple::\_\_construct - Конструктор класу Yaf\_View\_Simple

### Опис

final public**Yaf\_View\_Simple::\_\_construct**(string`$template_dir`, array`$options`

### Список параметрів

`template_dir`

Базовий каталог шаблонів за замовчуванням це APPLICATOIN . "/views" для Yaf.

`options`

Опції для двигуна, починаючи з Yaf 2.1.13, ви можете використовувати short\_tag "" у своєму шаблоні (незалежно від " short\_open\_tag"), щоб запобігти використанню short\_tag у шаблоні, є опція з ім'ям "short\_tag", яку ви можете вимкнути.

### Приклади

**Пример #1 Пример использования**Yaf\_View\_Simple::\_\_constructor()\*\*\*\*

```php
<?php
   define ("TEMPLATE_DIRECTORY", APPLICATOIN_PATH . '/views');
   $view = new Yaf_View_Simple(TEMPLATE_DIRECTORY, array(
                           'short_tag' => false //не позволяет использовать короткие теги в шаблоне
   ));
?>
```

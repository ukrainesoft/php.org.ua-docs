---
navigation:
  - yaf-view-simple.clear.md: '« YafViewSimple::clear'
  - yaf-view-simple.display.md: 'YafViewSimple::display »'
  - index.md: PHP Manual
  - class.yaf-view-simple.md: YafViewSimple
title: 'YafViewSimple::construct'
---
# YafViewSimple::construct

(Yaf >=1.0.0)

YafViewSimple::construct - Конструктор класу YafViewSimple

### Опис

final public **YafViewSimple::construct**(string `$template_dir`, array `$options`

### Список параметрів

`template_dir`

Базовий каталог шаблонів за замовчуванням це APPLICATOIN . "/views" для Yaf.

`options`

Опції для двигуна, починаючи з Yaf 2.1.13, ви можете використовувати shorttag "" у своєму шаблоні (незалежно від " shortopentag"), щоб запобігти використанню shorttag у шаблоні, є опція з ім'ям "shorttag", яку ви можете вимкнути.

### Приклади

**Приклад #1 Приклад використання **YafViewSimple::constructor()****

```php
<?php
   define ("TEMPLATE_DIRECTORY", APPLICATOIN_PATH . '/views');
   $view = new Yaf_View_Simple(TEMPLATE_DIRECTORY, array(
                           'short_tag' => false //не позволяет использовать короткие теги в шаблоне
   ));
?>
```

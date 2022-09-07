---
navigation:
  - class.v8js.md: « V8Js
  - v8js.executestring.md: 'V8Js::executeString »'
  - index.md: PHP Manual
  - class.v8js.md: V8Js
title: 'V8Js::construct'
---
# V8Js::construct

(PECL v8js >= 0.1.0)

V8Js::construct — Створює новий об'єкт [V8Js](class.v8js.md)

### Опис

public **V8Js::construct**  
string `$object_name` = "PHP",  
array `$variables` = array(),  
array `$extensions` = array(),  
bool `$report_uncaught_exceptions` **`true`**

Створює новий об'єкт [V8Js](class.v8js.md)

### Список параметрів

`object_name`

Ім'я об'єкта, що передається Javascript.

`variables`

Список змінних PHP, які мають бути доступні Javascript. Асоціативний масив формату `array("name-for-js" => "name-of-php-variable")`. За промовчанням порожній масив.

`extensions`

Список зареєстрованих через [V8Js::registerExtension()](v8js.registerextension.md) модулів, які мають бути доступні у контексті створеного об'єкта [V8Js](class.v8js.md)

> **Зауваження**
> 
> Модулі, зареєстровані як доступні автоматично, не потрібно перераховувати у цьому масиві. Також, якщо модуль має якісь залежності, їх теж не потрібно перераховувати. За промовчанням порожній масив.

`report_uncaught_exceptions`

Визначає, чи повідомлятимуться про непоймані винятки JavaScript відразу чи ні. За замовчуванням **`true`**. Якщо встановити в **`false`**, то ці винятки будуть доступні за допомогою [V8Js::getPendingException()](v8js.getpendingexception.md)

---
navigation:
  - function.igbinary-serialize.md: « igbinary\_serialize
  - book.json.md: JSON »
  - index.md: PHP Manual
  - ref.igbinary.md: Функції Igbinary
title: igbinary\_unserialize
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# igbinary\_unserialize

(PECL igbinary >= 1.1.1)

igbinary\_unserialize — Створює значення PHP із збереженого представлення функцією [igbinary\_serialize()](function.igbinary-serialize.md)

### Опис

```methodsynopsis
igbinary_unserialize(string $str): mixed
```

Функция**igbinary\_unserialize()** бере одну серіалізовану змінну з функції [igbinary\_serialize()](function.igbinary-serialize.md) і перетворить її назад на значення PHP.

**Увага**

Ненадійні вхідні дані користувача не повинні передаватися в **igbinary\_unserialize()**. Десеріалізація може призвести до завантаження та виконання коду через створення екземпляра об'єкта та автозавантаження, тоді зловмисник може цим скористатися. Натомість слід використовувати безпечний стандартний формат обміну даними, такий як JSON (за допомогою функцій [json\_decode()](function.json-decode.md) і [json\_encode()](function.json-encode.md)), якщо серіалізовані дані потрібно передати клієнту.

Якщо необхідно десеріалізувати збережені ззовні серіалізовані дані, для перевірки даних можна використовувати функцію [hash\_hmac()](function.hash-hmac.md). Важливо переконатись, що дані ніхто не підробив.

**Увага**

Формат серіалізації igbinary не дозволяє розрізняти різні групи посилань для одного і того ж значення. Всі посилання PHP на задане значення при десеріалізації обробляються як частина однієї групи посилань, навіть якщо при серіалізації вони були частинами різних груп посилань.

### Список параметрів

`str`

Серіалізована функцією [igbinary\_serialize()](function.igbinary-serialize.md) рядок.

Якщо десеріалізоване значення є об'єктом (object), після успішного відновлення об'єкта, igbinary автоматично спробує викликати метод [\_\_unserialize()](language.oop5.magic.md#object.unserialize) або [\_\_wakeup()](language.oop5.magic.md#object.wakeup) (якщо такий існує).

> **Зауваження** **unserialize\_callback\_func directive**
> 
> Можна встановити callback-функцію, яка буде викликатися, якщо під час десеріалізації повинен бути створений екземпляр невизначеного класу (щоб запобігти отриманню неповного об'єкта (object) `__PHP_Incomplete_Class`). Для определения[unserialize\_callback\_func](var.configuration.md#ini.unserialize-callback-func) можуть використовуватись файли php.ini, [ini\_set()](function.ini-set.md) або .htaccess. Щоразу, коли необхідно створити екземпляр невизначеного класу, callback-функція буде викликатися. Щоб вимкнути цю функцію, потрібно очистити параметр.

### Значення, що повертаються

Повертає перетворене значення, яке може бути bool, int, float, string, array, object чи null.

Якщо переданий рядок не може бути десеріалізованим, повертається **`false`** і видається помилка рівня **`E_NOTICE`**или**`E_WARNING`**

### Помилки

Об'єкти можуть викидати виняток [Throwable](class.throwable.md) у своїх оброблювачах десеріалізації.

### Примітки

**Увага**

**`null`**или**`false`** повертається як у разі виникнення помилки, так і при десеріалізації серіалізованого значення **`null`**или**`false`**. Цей особливий випадок можна визначити, порівнявши`str`с`igbinary_serialize(null)`или`igbinary_serialize(false)` або обробивши видану помилку рівня **`E_NOTICE`**

### Дивіться також

-   [unserialize()](function.unserialize.md) \- Створює PHP-значення зі збереженого уявлення
-   [json\_encode()](function.json-encode.md) \- Повертає JSON-подання даних
-   [json\_decode()](function.json-decode.md) \- Декодує рядок JSON
-   [hash\_hmac()](function.hash-hmac.md) \- Генерація хеш-коду на основі ключа, використовуючи метод HMAC
-   [igbinary\_serialize()](function.igbinary-serialize.md) \- Створює компактне, двійкове подання значення, що зберігається
-   [Автоматичне завантаження класів](language.oop5.autoload.md)
-   [unserialize\_callback\_func](var.configuration.md#ini.unserialize-callback-func)
-   [\_\_wakeup()](language.oop5.magic.md#object.wakeup)
-   [\_\_serialize()](language.oop5.magic.md#object.serialize)
-   [\_\_unserialize()](language.oop5.magic.md#object.unserialize)

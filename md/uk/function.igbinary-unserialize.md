---
navigation:
  - function.igbinary-serialize.html: « igbinaryserialize
  - book.json.md: JSON »
  - index.md: PHP Manual
  - ref.igbinary.md: Функции Igbinary
title: igbinaryunserialize
---
# igbinaryunserialize

(PECL igbinary >= 1.1.1)

igbinaryunserialize — Створює значення PHP із збереженого представлення функцією [igbinaryserialize()](function.igbinary-serialize.html)

### Опис

```methodsynopsis
igbinary_unserialize(string $str): mixed
```

**igbinaryunserialize()** бере одну серіалізовану змінну з [igbinaryserialize()](function.igbinary-serialize.html) і перетворює її назад на значення PHP.

**Увага**

Ненадійні вхідні дані користувача не повинні передаватися в **igbinaryunserialize()**. Десеріалізація може призвести до завантаження та виконання коду через створення екземпляра об'єкта та автозавантаження, тоді зловмисник може цим скористатися. Натомість слід використовувати безпечний стандартний формат обміну даними, такий як JSON (за допомогою функцій [jsondecode()](function.json-decode.html) і [jsonencode()](function.json-encode.html)), якщо серіалізовані дані потрібно передати клієнту.

Якщо необхідно десеріалізувати збережені ззовні серіалізовані дані, для перевірки даних можна використовувати функцію [hashhmac()](function.hash-hmac.html). Важливо переконатись, що дані ніхто не підробив.

**Увага**

Формат серіалізації igbinary не дозволяє розрізняти різні групи посилань для одного і того ж значення. Всі посилання PHP на задане значення при десеріалізації обробляються як частина однієї групи посилань, навіть якщо при серіалізації вони були частинами різних груп посилань.

### Список параметрів

`str`

Серіалізована функцією [igbinaryserialize()](function.igbinary-serialize.html) рядок.

Якщо десеріалізоване значення є об'єктом (object), після успішного відновлення об'єкта, igbinary автоматично спробує викликати метод [unserialize()](language.oop5.magic.html#object.unserialize) або [wakeup()](language.oop5.magic.html#object.wakeup) (якщо такий існує).

> **Зауваження** **unserializecallbackfunc directive**
> 
> Можна встановити callback-функцію, яка буде викликатися, якщо під час десеріалізації повинен бути створений екземпляр невизначеного класу (щоб запобігти отриманню неповного об'єкта (object) `__PHP_Incomplete_Class`). Для визначення [unserializecallbackfunc](var.configuration.html#ini.unserialize-callback-func) можуть використовуватись файли php.ini, [iniset()](function.ini-set.html) або .htaccess. Щоразу, коли необхідно створити екземпляр невизначеного класу, callback-функція буде викликатися. Щоб вимкнути цю функцію, потрібно очистити параметр.

### Значення, що повертаються

Повертається перетворене значення, яке може бути bool, int, float, string, array, object чи null.

Якщо переданий рядок не може бути десеріалізованим, повертається **`false`** і видається помилка рівня **`E_NOTICE`** або **`E_WARNING`**

### Помилки

Об'єкти можуть викидати виняток [Throwable](class.throwable.md) у своїх оброблювачах десеріалізації.

### Примітки

**Увага**

**`null`** або **`false`** повертається як у разі виникнення помилки, так і при десеріалізації серіалізованого значення **`null`** або **`false`**. Цей особливий випадок можна визначити, порівнявши`str` з `igbinary_serialize(null)` або `igbinary_serialize(false)` або обробивши видану помилку рівня **`E_NOTICE`**

### Дивіться також

-   [unserialize()](function.unserialize.md) - Створює PHP-значення зі збереженого уявлення
-   [jsonencode()](function.json-encode.html) - Повертає JSON-подання даних
-   [jsondecode()](function.json-decode.html) - Декодує рядок JSON
-   [hashhmac()](function.hash-hmac.html) - Генерація хеш-коду на основі ключа, використовуючи метод HMAC
-   [igbinaryserialize()](function.igbinary-serialize.html) - Створює компактне, двійкове уявлення значення, що зберігається
-   [Автоматичне завантаження класів](language.oop5.autoload.md)
-   [unserializecallbackfunc](var.configuration.html#ini.unserialize-callback-func)
-   [wakeup()](language.oop5.magic.html#object.wakeup)
-   [serialize()](language.oop5.magic.html#object.serialize)
-   [unserialize()](language.oop5.magic.html#object.unserialize)

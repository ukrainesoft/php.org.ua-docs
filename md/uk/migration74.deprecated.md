---
navigation:
  - migration74.incompatible.md: '« Зміни, що ламають зворотну сумісність'
  - migration74.removed-extensions.md: Видалені модулі »
  - index.md: PHP Manual
  - migration74.md: Міграція з PHP 7.3.x на PHP 7.4.x
title: Застаріла функціональність
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Застаріла функціональність

### Ядро PHP

#### Вкладені тернарні оператори без явної вказівки дужок

У вкладених тернарних операціях повинні використовуватися круглі дужки, щоб визначити порядок операцій. Раніше, якщо дужки явно не задані, здебільшого ліва асоціативність не призводила до очікуваної поведінки.

```php
<?php
1 ? 2 : 3 ? 4 : 5;   // устарело
(1 ? 2 : 3) ? 4 : 5; // хорошо
1 ? 2 : (3 ? 4 : 5); // хорошо
?>
```

Дужки *не* потрібні при вкладенні в середній операнд, оскільки це завжди однозначно і не залежить від асоціативності:

```php
1 ? 2 ? 3 : 4 : 5 // хорошо
```

#### Звернення до індексу масиву та рядки через фігурні дужки

Синтаксис доступу до масиву та рядка з використанням фігурних дужок оголошено застарілим. Використовуйте `$var[$idx]` замість `$var{$idx}`

#### Приведення типу (real) та функція [is\_real()](function.is-real.md)

Приведение типа`(real)` оголошено застарілим, натомість використовуйте `(float)`

Функция[is\_real()](function.is-real.md) також оголошено застарілою, замість неї використовуйте [is\_float()](function.is-float.md)

#### Отмена привязки`$this`при использовании`$this`

Отмена привязки`$this` у нестатичному замиканні, яке використовує `$this`, оголошено застарілою.

#### Ключевое слово`parent` поза батьківським класом

Использование`parent` усередині класу, який не має батька, оголошено застарілим, а в майбутньому відбудеться помилка компіляції. А поки що помилка буде тільки при зверненні до батька під час виконання.

#### INI-опція allow\_url\_include

Конфігураційна директива [allow\_url\_include](filesystem.configuration.md#ini.allow-url-include) оголошено застарілою. При ввімкненій опції буде викликано повідомлення про застарілі можливості під час завантаження.

#### Неприпустимі символи в основних функціях перетворення

Передача неприпустимих символів [base\_convert()](function.base-convert.md) [bindec()](function.bindec.md) [octdec()](function.octdec.md) тепер викликає повідомлення про застарілі можливості. Результат все одно буде обчислений так, якби неприпустимих символів не було. Провідні та завершальні прогалини, а також префікси типу 0x (залежно від системи числення), як і раніше, дозволені.

#### Использование[array\_key\_exists()](function.array-key-exists.md) з об'єктом

Использование[array\_key\_exists()](function.array-key-exists.md) з об'єктом оголошено застарілим. Натомість слід використовувати або [isset()](function.isset.md), либо[property\_exists()](function.property-exists.md)

#### Функції, пов'язані з чарівними лапками

Функції [get\_magic\_quotes\_gpc()](function.get-magic-quotes-gpc.md) і [get\_magic\_quotes\_runtime()](function.get-magic-quotes-runtime.md) оголошено застарілими. Вони завжди повертають **`false`**

#### Функция[hebrevc()](function.hebrevc.md)

Функция[hebrevc()](function.hebrevc.md) оголошено застарілою. Її можна замінити на вираз `nl2br(hebrev($str))`, або краще використовувати підтримку Unicode RTL.

#### Функция[convert\_cyr\_string()](function.convert-cyr-string.md)

Функция[convert\_cyr\_string()](function.convert-cyr-string.md) оголошено застарілою. Її можна замінити або на **mb\_convert\_string()**, либо[iconv()](function.iconv.md)или на класс[UConverter](class.uconverter.md)

#### Функция[money\_format()](function.money-format.md)

Функция[money\_format()](function.money-format.md) оголошено застарілою. Вона може бути замінена функціональністю інтернаціоналізації – класом [NumberFormatter](class.numberformatter.md)

#### Функция[ezmlm\_hash()](function.ezmlm-hash.md)

Функция[ezmlm\_hash()](function.ezmlm-hash.md) оголошено застарілою.

#### Функция[restore\_include\_path()](function.restore-include-path.md)

Функция[restore\_include\_path()](function.restore-include-path.md) оголошено застарілою. Її можна замінити на `ini_restore('include_path')`

#### Використання implode з нерекомендованим порядком параметрів

Передача параметров в[implode()](function.implode.md) у зворотному порядку оголошено застарілою - використовуйте `implode($glue, $parts)` замість `implode($parts, $glue)`

### COM

Імпорт бібліотек типів із реєстрацією констант без урахування регістру оголошено застарілим.

### Фільтрування

Фильтр\*\*`FILTER_SANITIZE_MAGIC_QUOTES`\*\* оголошено застарілим, замість нього використовуйте **`FILTER_SANITIZE_ADD_SLASHES`**

### Багатобайтові рядки

Передача нестрокового шаблона в[mb\_ereg\_replace()](function.mb-ereg-replace.md) оголошено застарілою. На даний момент нерядкові значення інтерпретуються як кодові точки ASCII. У PHP 8 шаблон буде оброблятися як рядок.

Передача кодування як 3-й параметр в [mb\_strrpos()](function.mb-strrpos.md) оголошено застарілою. Натомість передавайте позицію як 0, а кодування у 4-му параметрі.

### Полегшений протокол доступу до каталогів (LDAP)

Функції [ldap\_control\_paged\_result\_response()](function.ldap-control-paged-result-response.md) і [ldap\_control\_paged\_result()](function.ldap-control-paged-result.md) оголошено застарілими. Для керування посторінковим режимом використовуйте функцію [ldap\_search()](function.ldap-search.md)

### Reflection

Виклики [ReflectionType::\_\_toString()](reflectiontype.tostring.md) тепер створюють повідомлення про застарілі можливості. Цей метод оголошено застарілим на користь використання [ReflectionNamedType::getName()](reflectionnamedtype.getname.md) у документації з PHP 7.1, але не видавав відповідного повідомлення з технічних причин.

Методи `export()`у всех классов[Reflection](class.reflection.md) оголошено застарілими. Тепер створюйте об'єкт [Reflection](class.reflection.md)и преобразуйте его в строку:

```php
<?php
// Вместо ReflectionClass::export(Foo::class, false) используйте:
echo new ReflectionClass(Foo::class), "\n";

// Вместо $str = ReflectionClass::export(Foo::class, true) используйте:
$str = (string) new ReflectionClass(Foo::class);
?>
```

### Сокети

Флаги\*\*`AI_IDN_ALLOW_UNASSIGNED`** і **`AI_IDN_USE_STD3_ASCII_RULES`\*\* для функції [socket\_addrinfo\_lookup()](function.socket-addrinfo-lookup.md) оголошено застарілими через оновлення glibc.

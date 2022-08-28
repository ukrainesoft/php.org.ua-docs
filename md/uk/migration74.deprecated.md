Застаріла функціональність

-   [« Изменения, ломающие обратную совместимость](migration74.incompatible.html)
    
-   [Удалённые модули »](migration74.removed-extensions.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 7.3.x на PHP 7.4.x](migration74.html)
    
-   Застаріла функціональність
    

## Застаріла функціональність

### Ядро PHP

#### Вкладені тернарні оператори без явної вказівки дужок

У вкладених тернарних операціях повинні використовуватися круглі дужки, щоб визначити порядок операцій. Раніше, якщо дужки явно не задані, здебільшого ліва асоціативність не призводила до очікуваної поведінки.

```php
<?php
1 ? 2 : 3 ? 4 : 5;   // устарело
(1 ? 2 : 3) ? 4 : 5; // хорошо
1 ? 2 : (3 ? 4 : 5); // хорошо
?>
```

Дужки *not* потрібні при вкладенні в середній операнд, оскільки це завжди однозначно і не залежить від асоціативності:

```php
1 ? 2 ? 3 : 4 : 5 // хорошо
```

#### Звернення до індексу масиву та рядки через фігурні дужки

Синтаксис доступу до масиву та рядка з використанням фігурних дужок оголошено застарілим. Використовуйте `$var[$idx]` замість `$var{$idx}`

#### Приведення типу (real) та функція [is\_real()](function.is-real.html)

Приведення типу `(real)` оголошено застарілим, натомість використовуйте `(float)`

Функція [is\_real()](function.is-real.html) також оголошено застарілою, замість неї використовуйте [is\_float()](function.is-float.html)

#### Скасування прив'язки `$this` при використанні `$this`

Скасування прив'язки `$this` у нестатичному замиканні, яке використовує `$this`, оголошено застарілою.

#### Ключове слово `parent` поза батьківським класом

Використання `parent` усередині класу, який не має батька, оголошено застарілим, а в майбутньому відбудеться помилка компіляції. А поки що помилка буде тільки при зверненні до батька під час виконання.

#### INI-опція allowurlinclude

Конфігураційна директива [allow\_url\_include](filesystem.configuration.html#ini.allow-url-include) оголошено застарілою. При включеній опції буде викликано повідомлення про застарілі можливості під час завантаження.

#### Неприпустимі символи в основних функціях перетворення

Передача неприпустимих символів [base\_convert()](function.base-convert.html) [bindec()](function.bindec.html) [octdec()](function.octdec.html) тепер викликає повідомлення про застарілі можливості. Результат все одно буде обчислений так, якби неприпустимих символів не було. Провідні та завершальні прогалини, а також префікси типу 0x (залежно від системи числення), як і раніше, дозволені.

#### Використання [array\_key\_exists()](function.array-key-exists.html) з об'єктом

Використання [array\_key\_exists()](function.array-key-exists.html) з об'єктом оголошено застарілим. Натомість слід використовувати або [isset()](function.isset.html), або [property\_exists()](function.property-exists.html)

#### Функції, пов'язані з чарівними лапками

Функції [get\_magic\_quotes\_gpc()](function.get-magic-quotes-gpc.html) і [get\_magic\_quotes\_runtime()](function.get-magic-quotes-runtime.html) оголошено застарілими. Вони завжди повертають **`false`**

#### Функція [hebrevc()](function.hebrevc.html)

Функція [hebrevc()](function.hebrevc.html) оголошено застарілою. Її можна замінити на вираз `nl2br(hebrev($str))`, або краще використовувати підтримку Unicode RTL.

#### Функція [convert\_cyr\_string()](function.convert-cyr-string.html)

Функція [convert\_cyr\_string()](function.convert-cyr-string.html) оголошено застарілою. Її можна замінити або на **мбconvertstring()**, або [iconv()](function.iconv.html) або на клас [UConverter](class.uconverter.html)

#### Функція [money\_format()](function.money-format.html)

Функція [money\_format()](function.money-format.html) оголошено застарілою. Вона може бути замінена функціональністю інтернаціоналізації – класом [NumberFormatter](class.numberformatter.html)

#### Функція [ezmlm\_hash()](function.ezmlm-hash.html)

Функція [ezmlm\_hash()](function.ezmlm-hash.html) оголошено застарілою.

#### Функція [restore\_include\_path()](function.restore-include-path.html)

Функція [restore\_include\_path()](function.restore-include-path.html) оголошено застарілою. Її можна замінити на `ini_restore('include_path')`

#### Використання implode з нерекомендованим порядком параметрів

Передача параметрів у [implode()](function.implode.html) у зворотному порядку оголошено застарілою - використовуйте `implode($glue, $parts)` замість `implode($parts, $glue)`

### COM

Імпорт бібліотек типів із реєстрацією констант без урахування регістру оголошено застарілим.

### Фільтрування

Фільтр **`FILTER_SANITIZE_MAGIC_QUOTES`** оголошено застарілим, замість нього використовуйте **`FILTER_SANITIZE_ADD_SLASHES`**

### Багатобайтові рядки

Передача нерядкового шаблону в [mb\_ereg\_replace()](function.mb-ereg-replace.html) оголошено застарілою. На даний момент нерядкові значення інтерпретуються як кодові точки ASCII. У PHP 8 шаблон буде оброблятися як рядок.

Передача кодування як 3-й параметр в [mb\_strrpos()](function.mb-strrpos.html) оголошено застарілою. Натомість передавайте позицію як 0, а кодування у 4-му параметрі.

### Полегшений протокол доступу до каталогів (LDAP)

Функції [ldap\_control\_paged\_result\_response()](function.ldap-control-paged-result-response.html) і [ldap\_control\_paged\_result()](function.ldap-control-paged-result.html) оголошено застарілими. Для керування посторінковим режимом використовуйте функцію [ldap\_search()](function.ldap-search.html)

### Reflection

Виклики [ReflectionType::\_\_toString()](reflectiontype.tostring.html) тепер створюють повідомлення про застарілі можливості. Цей метод оголошено застарілим на користь використання [ReflectionNamedType::getName()](reflectionnamedtype.getname.html) у документації з PHP 7.1, але не видавав відповідного повідомлення з технічних причин.

Методи `export()` у всіх класів [Reflection](class.reflection.html) оголошено застарілими. Тепер створюйте об'єкт [Reflection](class.reflection.html) і перетворіть його на рядок:

```php
<?php
// Вместо ReflectionClass::export(Foo::class, false) используйте:
echo new ReflectionClass(Foo::class), "\n";

// Вместо $str = ReflectionClass::export(Foo::class, true) используйте:
$str = (string) new ReflectionClass(Foo::class);
?>
```

### Сокети

Прапори **`AI_IDN_ALLOW_UNASSIGNED`** і **`AI_IDN_USE_STD3_ASCII_RULES`** для функції [socket\_addrinfo\_lookup()](function.socket-addrinfo-lookup.html) оголошено застарілими через оновлення glibc.
---
navigation:
  - yaf.installation.md: « Встановлення
  - yaf.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - yaf.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Yaf**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [yaf.library](yaf.configuration.md#ini.yaf.library) |  | **`INI_ALL`** |  |
| [yaf.action\_prefer](yaf.configuration.md#ini.yaf.action-prefer) |  | **`INI_ALL`** |  |
| [yaf.lowcase\_path](yaf.configuration.md#ini.yaf.lowcase-path) |  | **`INI_ALL`** |  |
| [yaf.use\_spl\_autoload](yaf.configuration.md#ini.yaf.use-spl-autoload) |  | **`INI_ALL`** |  |
| [yaf.forward\_limit](yaf.configuration.md#ini.yaf.forward-limit) | 5 | **`INI_ALL`** |  |
| [yaf.name\_suffix](yaf.configuration.md#ini.yaf.name-suffix) |  | **`INI_ALL`** |  |
| [yaf.name\_separator](yaf.configuration.md#ini.yaf.name-separator) |  | **`INI_ALL`** |  |
| [yaf.cache\_config](yaf.configuration.md#ini.yaf.cache-config) |  | **`INI_SYSTEM`** |  |
| [yaf.environ](yaf.configuration.md#ini.yaf.environ) | product | **`INI_SYSTEM`** |  |
| [yaf.use\_namespace](yaf.configuration.md#ini.yaf.use-namespace) |  | **`INI_SYSTEM`** |  |

Коротке пояснення конфігураційних директив.

`yaf.library`string

Шлях до глобальних бібліотек, Yaf\_loader шукатиме глобальні бібліотеки тут.

`yaf.action_prefer`int

Якщо у PATH\_INFO тільки одна частина, її слід розглянути як контролер або дію.

Якщо задана як On, вона розглядатиметься як ім'я дії (Action).

`yaf.lowcase_path`int

Чи розглядати всі шляхи в нижньому регістрі під час автозавантаження класів.

`yaf.use_spl_autoload`int

Якщо поставлено як On, то якщо [Yaf\_Loader](class.yaf-loader.md) не може знайти клас, він поверне **`false`**, тим самим надаючи можливість виклику іншої функції автозавантаження.

Якщо поставлено як Off, то якщо [Yaf\_Loader](class.yaf-loader.md) не знайде клас, він поверне **`true`** і перерве подальші дії з автозавантаження.

> **Зауваження** :
> 
> Yaf реєструє завантажувач класів під час створення екземпляра класу [Yaf\_Application](class.yaf-application.md), так що будь-які інші автозавантажувачі, зареєстровані до інстанціації цього класу, будуть запущені до [Yaf\_Loader::autoload()](yaf-loader.autoload.md)

Если задано как Off(по умолчанию),[Yaf\_Loader::autoload()](yaf-loader.autoload.md) завжди повертатиме **`true`**

`yaf.forward_limit`int

Максимальна кількість перенаправлень, за замовчуванням 5. Це означає, що стек перенаправлень не може бути глибшим за 5.

Це зроблено для запобігання рекурсії у [Yaf\_Controller\_Abstract::forward()](yaf-controller-abstract.forward.md)

`yaf.name_suffix`int

Якщо поставлено як On, Yaf\_Loader ідентифікуватиме за його суфіксом, для визначення, чи є він класом MVC.

Якщо встановлено як Off, Yaf\_Loader дивитиметься на префікс.

`yaf.name_separator`string

Якщо не порожньо, Yaf\_Loader, при ідентифікації класу, шукатиме суфікс з огляду на заданий символ як роздільник.

Наприклад, якщо поставити рівним "\_", Yaf\_Loader ідентифікує Index\_Controller як клас контролер, а IndexController як клас.

`yaf.cache_config`int

Якщо встановлено як On, і в той же час ви використовуєте конфігураційний ini-файл як параметр **Yaf\_Application()**, то результат компіляції цього файлу ini буде закеширован в процесі PHP.

> **Зауваження** :
> 
> Yaf перевіряє mtime ini-файлу і якщо значення змінилося з моменту останньої компіляції, перекомпілює його.

**Увага**

Yaf використовує шлях до ini-файлу як ключ закешованого запису, тому рекомендується використовувати повні, абсолютні шляхи, щоб не сталося конфлікту між двома додатками, що використовують ini-файли з однаковими іменами, але різним вмістом.

`yaf.environ`string

За замовчуванням одно "product" і використовується Yaf для отримання потрібної секції з ini-файлу.

Отже, якщо параметр дорівнює "product", Yaf використовуватиме секцію "product" в ini-файлі (перший параметр [Yaf\_Application](class.yaf-application.md)) як конфігурація [Yaf\_Application](class.yaf-application.md)

`yaf.use_namespace`int

Якщо встановлено як On, всі класи Yaf іменуються з використанням просторів імен.

Например:

```
Yaf_Route_Rewrite => \Yaf\Route\Rewrite
Yaf_Request_Http  => \Yaf\Request\Http
```

Є винятки для класів типу [Yaf\_Controller\_Abstract](class.yaf-controller-abstract.md). Останній компонент імені є ключовим словом PHP і не може використовуватися як ім'я класу, так що він буде виглядати так:

```
Yaf_Controller_Abstract => \Yaf\Controller_Abstract
Yaf_Route_Static => \Yaf\Route_Static
```

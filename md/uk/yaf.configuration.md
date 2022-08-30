Налаштування під час виконання

-   [« Установка](yaf.installation.md)
    
-   [Типи ресурсів »](yaf.resources.md)
    
-   [PHP Manual](index.md)
    
-   [Встановлення та налаштування](yaf.setup.md)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Yaf**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [yaf.library](yaf.configuration.html#ini.yaf.library) |  | PHPINIALL |  |
| [yaf.actionprefer](yaf.configuration.html#ini.yaf.action-prefer) |  | PHPINIALL |  |
| [yaf.lowcasepath](yaf.configuration.html#ini.yaf.lowcase-path) |  | PHPINIALL |  |
| [yaf.usesplautoload](yaf.configuration.html#ini.yaf.use-spl-autoload) |  | PHPINIALL |  |
| [yaf.forwardlimit](yaf.configuration.html#ini.yaf.forward-limit) |  | PHPINIALL |  |
| [yaf.namesuffix](yaf.configuration.html#ini.yaf.name-suffix) |  | PHPINIALL |  |
| [yaf.nameseparator](yaf.configuration.html#ini.yaf.name-separator) |  | PHPINIALL |  |
| [yaf.cacheconfig](yaf.configuration.html#ini.yaf.cache-config) |  | PHPINISYSTEM |  |
| [yaf.environ](yaf.configuration.html#ini.yaf.environ) | product | PHPINISYSTEM |  |
| [yaf.usenamespace](yaf.configuration.html#ini.yaf.use-namespace) |  | PHPINISYSTEM |  |

Коротке пояснення конфігураційних директив.

`yaf.library` string

Шлях до глобальних бібліотек, Yafloader шукатиме глобальні бібліотеки тут.

`yaf.action_prefer` int

Якщо у PATHINFO тільки одна частина, її слід розглянути як контролер або дію.

Якщо задана як On, вона розглядатиметься як ім'я дії (Action).

`yaf.lowcase_path` int

Чи розглядати всі шляхи в нижньому регістрі під час автозавантаження класів.

`yaf.use_spl_autoload` int

Якщо поставлено як On, то якщо [YafLoader](class.yaf-loader.html) не може знайти клас, він поверне **`false`**, тим самим надаючи можливість виклику іншої функції автозавантаження.

Якщо поставлено як Off, то якщо [YafLoader](class.yaf-loader.html) не знайде клас, він поверне **`true`** і перерве подальші дії з автозавантаження.

> **Зауваження**
> 
> Yaf реєструє завантажувач класів під час створення екземпляра класу [YafApplication](class.yaf-application.html), так що будь-які інші автозавантажувачі, зареєстровані до інстанціації цього класу, будуть запущені до [YafLoader::autoload()](yaf-loader.autoload.html)

Якщо встановлено як Off(за замовчуванням), [YafLoader::autoload()](yaf-loader.autoload.html) завжди повертатиме **`true`**

`yaf.forward_limit` int

Максимальна кількість перенаправлень, за замовчуванням 5. Це означає, що стек перенаправлень не може бути глибшим за 5.

Це зроблено для запобігання рекурсії у [YafControllerAbstract::forward()](yaf-controller-abstract.forward.html)

`yaf.name_suffix` int

Якщо поставлено як On, YafLoader ідентифікуватиме за його суфіксом, для визначення, чи є він класом MVC.

Якщо встановлено як Off, YafLoader дивитиметься на префікс.

`yaf.name_separator` string

Якщо не порожньо, YafLoader, при ідентифікації класу, шукатиме суфікс з огляду на заданий символ як роздільник.

Наприклад, якщо поставити рівним "", YafLoader ідентифікує IndexController як клас контролер, а IndexController як клас.

`yaf.cache_config` int

Якщо встановлено як On, і в той же час ви використовуєте конфігураційний ini-файл як параметр **YafApplication()**, то результат компіляції цього файлу ini буде закеширован в процесі PHP.

> **Зауваження**
> 
> Yaf перевіряє mtime ini-файлу і якщо значення змінилося з моменту останньої компіляції, перекомпілює його.

**Увага**

Yaf використовує шлях до ini-файлу як ключ закешованого запису, тому рекомендується використовувати повні, абсолютні шляхи, щоб не сталося конфлікту між двома додатками, що використовують ini-файли з однаковими іменами, але різним вмістом.

`yaf.environ` string

За замовчуванням одно "product" і використовується Yaf для отримання потрібної секції з ini-файлу.

Отже, якщо параметр дорівнює "product", Yaf використовуватиме секцію "product" в ini-файлі (перший параметр [YafApplication](class.yaf-application.html)) як конфігурація [YafApplication](class.yaf-application.html)

`yaf.use_namespace` int

Якщо встановлено як On, всі класи Yaf іменуються з використанням просторів імен.

Наприклад:

```
Yaf_Route_Rewrite => \Yaf\Route\Rewrite
Yaf_Request_Http  => \Yaf\Request\Http
```

Є винятки для класів типу [YafControllerAbstract](class.yaf-controller-abstract.html). Останній компонент імені є ключовим словом PHP і не може використовуватися як ім'я класу, так що він виглядатиме так:

```
Yaf_Controller_Abstract => \Yaf\Controller_Abstract
Yaf_Route_Static => \Yaf\Route_Static
```
Клас YafRouter

-   [« Yaf\_Route\_Rewrite::route](yaf-route-rewrite.route.html)
    
-   [Yaf\_Router::addConfig »](yaf-router.addconfig.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafRouter
    

# Клас YafRouter

(Yaf >=1.0.0)

## Вступ

**YafRouter** – це стандартний каркасний маршрутизатор. Маршрутизація - це процес отримання кінцевої точки URI (тої частини URI, яка йде після базового URI: дивіться [Yaf\_Request\_Abstract::setBaseUri()](yaf-request-abstract.setbaseuri.html)) та розкладання її на параметри, щоб визначити, який модуль, контролер та дія повинні отримати запит. Ці значення модуля, контролера, дії та інших параметрів упаковані в об'єкт [Yaf\_Request\_Abstract](class.yaf-request-abstract.html), який потім обробляється [Yaf\_Dispatcher](class.yaf-dispatcher.html). Маршрутизація відбувається лише один раз: при початковому отриманні запиту та до відправлення першого контролера . **YafRouter** призначений для забезпечення функціональності, подібної до modrewrite, з використанням чистих структур PHP. Він базується на маршрутизації Ruby on Rails і не вимагає будь-яких попередніх знань про перезапис URL веб-сервера. Він призначений для роботи з одним правилом Apache modrewrite (одним з):

**Приклад #1 Правило перезапису Apache**

RewriteEngine on RewriteRule!.(js|ico|gif|jpg|png|css|html)$ index.php

або (переважно):

**Приклад #2 Правило перезапису Apache**

RewriteEngine On RewriteCond %{REQUESTFILENAME} -s ВРRewriteCond %{REQUESTFILENAME} -l ВРRewriteCond %{REQUESTFILENAME} -d RewriteRule ^. NC,LRewriteRule ^.$index.php NC,L

У разі використання Lighttpd використовуйте таке правило перезапису:

**Приклад #3 Правило перезапису для Lighttpd**

url.rewrite-once = ( ".)$" => "/індекс.пхп?$1", "..(js|ico|gif|jpg|png|css|html)$" => "$0", "" => "/index.php" )

Під час використання Nginx використовуйте таке правило перезапису:

**Приклад #4 Правило перезапису Nginx**

server { listen ; servername yourdomain.com; root documentroot; index index.php index.html;

if (!-e $requestfilename) { rewrite ^/(.) /index.php/$1 last; } }

## Маршрут за замовчуванням

**YafRouter** поставляється з попередньо налаштованим маршрутом за умовчанням [Yaf\_Route\_Static](class.yaf-route-static.html), який буде відповідати URI у формі контролера/дії. Крім того, ім'я модуля може бути зазначено як перший елемент шляху, що дозволяє використовувати URI форми модуля/контролера/дії. Нарешті, він також буде відповідати будь-яким додатковим параметрам, які додаються до URI за замовчуванням - controller /action/var1/value1/var2/value2.

> **Зауваження**
> 
> Ім'я модуля має бути визначено у конфігурації з урахуванням application.module="Index,Foo,Bar", у цьому випадку тільки index, foo та bar можуть розглядатися як ім'я модуля. Якщо не налаштовано, є лише один модуль під назвою "Index".

Деякі приклади відповідності таких маршрутів:

**Приклад #5 Приклад використання [Yaf\_Route\_Static](class.yaf-route-static.html)(маршрут за замовчуванням)**

// Припускаючи наступне налаштування: $conf = array( "application" => array( "modules" => "Index,Blog", ), );

Тільки контролер:[http://example/news](http://example/news)controller == news Тільки дія (якщо визначено yaf.actionprefer=1 в php.ini) action == news

Невірний модуль відображається на ім'я контролера:[http://example/foo](http://example/foo)controller == foo

Модуль + контролер:[http://example/blog/archive](http://example/blog/archive)module == blog controller == archive

Модуль + контролер + дія:[http://example/blog/archive/list](http://example/blog/archive/list)module == blog controller == archive action == list

Модуль + контролер + дія + параметри:[http://example/blog/archive/list/sort/alpha/date/desc](http://example/blog/archive/list/sort/alpha/date/desc)module == blog controller == archive action == list sort == alpha date == desc

## Огляд класів

```classsynopsis



    
     
      class Yaf_Router
     
     {

    /* Свойства */
    
     protected
      $_routes;

    protected
      $_current;



    /* Методы */
    
   public __construct()

    public addConfig(Yaf_Config_Abstract $config): bool
public addRoute(string $name, Yaf_Route_Abstract $route): bool
public getCurrentRoute(): string
public getRoute(string $name): Yaf_Route_Interface
public getRoutes(): mixed
public route(Yaf_Request_Abstract $request): bool

   }
```

## Властивості

routes

стек зареєстрованих маршрутів

current

після фази маршрутизації вказується назва, який маршрут використовується для маршрутизації поточного запиту. Ви можете отримати його ім'я за допомогою [Yaf\_Router::getCurrentRoute()](yaf-router.getcurrentroute.html)

## Зміст

-   [Yaf\_Router::addConfig](yaf-router.addconfig.html) — Додає настроєні маршрути до маршрутизатора
-   [Yaf\_Router::addRoute](yaf-router.addroute.html) — Додає новий маршрут до маршрутизатора
-   [Yaf\_Router::\_\_construct](yaf-router.construct.html) - Конструктор класу YafRouter
-   [Yaf\_Router::getCurrentRoute](yaf-router.getcurrentroute.html) — Отримує ім'я діючого маршруту
-   [Yaf\_Router::getRoute](yaf-router.getroute.html) — Отримує маршрут на ім'я
-   [Yaf\_Router::getRoutes](yaf-router.getroutes.html) — Отримує зареєстровані маршрути
-   [Yaf\_Router::route](yaf-router.route.html) - Призначення route
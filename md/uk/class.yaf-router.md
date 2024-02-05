---
navigation:
  - yaf-route-rewrite.route.md: '« Yaf\_Route\_Rewrite::route'
  - yaf-router.addconfig.md: 'Yaf\_Router::addConfig »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Router
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Router

(Yaf >=1.0.0)

## Вступ

**Yaf\_Router** – це стандартний каркасний маршрутизатор. Маршрутизація - це процес отримання кінцевої точки URI (тої частини URI, яка йде після базового URI: дивіться [Yaf\_Request\_Abstract::setBaseUri()](yaf-request-abstract.setbaseuri.md)) та розкладання її на параметри, щоб визначити, який модуль, контролер та дія повинні отримати запит. Ці значення модуля, контролера, дії та інших параметрів упаковані в об'єкт [Yaf\_Request\_Abstract](class.yaf-request-abstract.md), який потім обробляється [Yaf\_Dispatcher](class.yaf-dispatcher.md). Маршрутизація відбувається лише один раз: при початковому отриманні запиту та до відправлення першого контролера . **Yaf\_Router** призначений для забезпечення функціональності, подібної до mod\_rewrite, з використанням чистих структур PHP. Він заснований на маршрутизації Ruby on Rails і не вимагає будь-яких попередніх знань про перезапис URL веб-сервера. Він призначений для роботи з одним правилом Apache mod\_rewrite (одним з):

**Приклад #1 Правило перезапису Apache**

RewriteEngine on RewriteRule !\\.(js|ico|gif|jpg|png|css|html)$ index.php

або (переважно):

**Приклад #2 Правило перезапису Apache**

RewriteEngine On RewriteCond %{REQUEST\_FILENAME} -s\[OR\]RewriteCond %{REQUEST\_FILENAME} -l\[OR\]RewriteCond %{REQUEST\_FILENAME} -d RewriteRule ^.\* \[NC,L\]RewriteRule ^.\*$ index.php\[NC,L\]

У разі використання Lighttpd використовуйте таке правило перезапису:

**Приклад #3 Правило перезапису для Lighttpd**

url.rewrite-once = ( ".\*\\?(.\*)$" => "/index.php?$1", ".\*\\.(js|ico|gif|jpg|png|css|html)$" => "$0", "" => "/index.php" )

Під час використання Nginx використовуйте таке правило перезапису:

**Приклад #4 Правило перезапису Nginx**

server { listen\*\*\*\*; server\_name yourdomain.com; root document\_root; index index.php index.md;

if (!-e $request\_filename) { rewrite ^/(.\*) /index.php/$1 last; } }

## Маршрут за замовчуванням

**Yaf\_Router** поставляється з попередньо налаштованим маршрутом за умовчанням [Yaf\_Route\_Static](class.yaf-route-static.md), який буде відповідати URI у формі контролера/дії. Крім того, ім'я модуля може бути зазначено як перший елемент шляху, що дозволяє використовувати URI форми модуля/контролера/дії. Нарешті, він також буде відповідати будь-яким додатковим параметрам, які додаються до URI за замовчуванням - controller /action/var1/value1/var2/value2.

> **Зауваження** :
> 
> Ім'я модуля має бути визначено у конфігурації з урахуванням application.module="Index,Foo,Bar", у цьому випадку тільки index, foo та bar можуть розглядатися як ім'я модуля. Якщо не налаштовано, є лише один модуль під назвою "Index".

Деякі приклади відповідності таких маршрутів:

**Приклад #5 Приклад использования[Yaf\_Route\_Static](class.yaf-route-static.md)(маршрут за замовчуванням)**

// Припускаючи наступне налаштування: $conf = array( "application" => array( "modules" => "Index,Blog", ), );

Тільки контролер:[http://example/news](http://example/news)controller == news Тільки дія (якщо визначено yaf.action\_prefer=1 в php.ini) action == news

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

\_routes

стек зареєстрованих маршрутів

\_current

після фази маршрутизації вказується назва, який маршрут використовується для маршрутизації поточного запиту. Ви можете отримати його ім'я за допомогою [Yaf\_Router::getCurrentRoute()](yaf-router.getcurrentroute.md)

## Зміст

-   [Yaf\_Router::addConfig](yaf-router.addconfig.md)— Додає настроєні маршрути до маршрутизатора
-   [Yaf\_Router::addRoute](yaf-router.addroute.md)— Додає новий маршрут до маршрутизатора
-   [Yaf\_Router::\_\_construct](yaf-router.construct.md) \- Конструктор класу Yaf\_Router
-   [Yaf\_Router::getCurrentRoute](yaf-router.getcurrentroute.md)— Отримує ім'я діючого маршруту
-   [Yaf\_Router::getRoute](yaf-router.getroute.md)— Отримує маршрут на ім'я
-   [Yaf\_Router::getRoutes](yaf-router.getroutes.md)— Отримує зареєстровані маршрути
-   [Yaf\_Router::route](yaf-router.route.md) \- Призначення route

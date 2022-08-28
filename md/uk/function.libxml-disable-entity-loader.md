Вимкнення можливості завантаження сутностей із зовнішніх джерел

-   [« libxml\_clear\_errors](function.libxml-clear-errors.html)
    
-   [libxml\_get\_errors »](function.libxml-get-errors.html)
    
-   [PHP Manual](index.html)
    
-   [Функции libxml](ref.libxml.html)
    
-   Вимкнення можливості завантаження сутностей із зовнішніх джерел
    

# libxmldisableentityloader

(PHP 5> = 5.2.11, PHP 7, PHP 8)

libxmldisableentityloader — Вимкнення можливості завантаження сутностей із зовнішніх джерел

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
libxml_disable_entity_loader(bool $disable = true): bool
```

Вимкнення/вмикання можливості завантажувати зовнішні сутності. Зверніть увагу, що вимкнення завантаження зовнішніх сутностей може спричинити загальні проблеми із завантаженням XML-документів. Однак у libxml 2.9.0 підстановка сутностей відключена за умовчанням, тому немає необхідності відключати завантаження зовнішніх сутностей, якщо немає необхідності дозволяти посилання на внутрішні сутності за допомогою **`LIBXML_NOENT`**. Як правило, краще використовувати [libxml\_set\_external\_entity\_loader()](function.libxml-set-external-entity-loader.html) для придушення завантаження зовнішніх сутностей.

### Список параметрів

`disable`

Вимкнення (**`true`**) або включення (**`false`**) модулів libxml (таких як [DOM](book.dom.html) [XMLWriter](book.xmlwriter.html) і [XMLReader](book.xmlreader.html)) для завантаження зовнішніх сутностей.

### Значення, що повертаються

Повертає попереднє значення.

### Дивіться також

-   [libxml\_use\_internal\_errors()](function.libxml-use-internal-errors.html) - Відключення помилок libxml та передача повноважень щодо вибірки та обробки інформації про помилки користувачеві
-   [libxml\_set\_external\_entity\_loader()](function.libxml-set-external-entity-loader.html) - Зміна завантажувача за умовчанням для зовнішніх об'єктів
-   [Константа **`LIBXML_NOENT`**](libxml.constants.html)
Клас MessageFormatter

-   [« Normalizer::normalize](normalizer.normalize.html)
    
-   [MessageFormatter::create »](messageformatter.create.html)
    
-   [PHP Manual](index.html)
    
-   [intl](book.intl.html)
    
-   Клас MessageFormatter
    

# Клас MessageFormatter

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

## Вступ

MessageFormatter - це клас, що дозволяє створювати склеювані, незалежні від мови повідомлення. Методи цього класу використовуються для створення всіх повідомлень, що показуються користувачеві.

Клас MessageFormatter збирає повідомлення з різних фрагментів (таких як текст, числа та дати), що поставляються програмою. Даний клас дозволяє програмі не замислюватися над тим, в якому порядку ці фрагменти треба склеювати. Клас використовує специфікації форматування для складання цих фрагментів повідомлення, що зберігається у вигляді одного рядка в сховищі ресурсів. Наприклад, MessageFormatter дозволить надрукувати фразу "Finished printing x out of y files..." в такий спосіб, щоб забезпечити гнучкість перекладу.

Раніше повідомлення кінцевого користувача створювалося як закінчена фраза і оброблялася як рядок. Така процедура призводила до проблем локалізації, оскільки структура фрази, порядок слів, формат чисел тощо дуже відрізнялися в різних мовах. Нейтральна до мови процедура створення повідомлень тримає кожну частину повідомлення окремо та надає ключі до даних. Використовуючи ці ключі, клас MessageFormatter може склеювати частини повідомлення, перетворювати їх відповідно до локалі та відображати у вигляді грамотного повідомлення кінцевому користувачеві.

MessageFormatter бере набір об'єктів, форматує їх і вставляє шаблон в потрібних місцях. Спільно з MessageFormatter корисно використовувати засоби форматування вибору (choice formatter) для обробки множини/однини, порівняння чисел і вибору з масиву елементів. Зазвичай формат повідомлення береться із ресурсів, а аргументи передаються під час виконання.

## Огляд класів

```classsynopsis

     
    

    
     
      class MessageFormatter
     
     {

    /* Методы */
    
   public __construct(string $locale, string $pattern)

    public static create(string $locale, string $pattern): ?MessageFormatter
public static formatMessage(string $locale, string $pattern, array $values): string|false
public format(array $values): string|false
public getErrorCode(): int
public getErrorMessage(): string
public getLocale(): string
public getPattern(): string|false
public static parseMessage(string $locale, string $pattern, string $message): array|false
public parse(string $string): array|false
public setPattern(string $pattern): bool

   }
```

## Дивіться також

-   [»  ICU. Документация по форматированию.](https://unicode-org.github.io/icu/userguide/format_parse/)
-   [»  ICU. Описание форматирования сообщений.](https://unicode-org.github.io/icu/userguide/format_parse/messages/)
-   [» ICU. Средства форматирования сообщений](https://unicode-org.github.io/icu/userguide/format_parse/messages/)
-   [» ICU. Средства форматирования выбора](http://icu-project.org/apiref/icu4c/classChoiceFormat.html#details)

## Зміст

-   [MessageFormatter::create](messageformatter.create.html) — Створює засіб форматування повідомлень
-   [MessageFormatter::formatMessage](messageformatter.formatmessage.html) — Швидко форматує повідомлення
-   [MessageFormatter::format](messageformatter.format.html) — Форматує повідомлення
-   [MessageFormatter::getErrorCode](messageformatter.geterrorcode.html) — Повертає код помилки останньої операції
-   [MessageFormatter::getErrorMessage](messageformatter.geterrormessage.html) — Повертає текст помилки останньої операції
-   [MessageFormatter::getLocale](messageformatter.getlocale.html) — Повертає локаль, для якої було створено засіб форматування
-   [MessageFormatter::getPattern](messageformatter.getpattern.html) — Повертає шаблон, який використовує засіб форматування
-   [MessageFormatter::parseMessage](messageformatter.parsemessage.html) — Швидко розбирає вхідний рядок
-   [MessageFormatter::parse](messageformatter.parse.html) — Розбирає рядок згідно з шаблоном
-   [MessageFormatter::setPattern](messageformatter.setpattern.html) — Встановлює шаблон, який використовує засіб форматування
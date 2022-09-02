---
navigation:
  - numberformatter.settextattribute.md: '« NumberFormatter::setTextAttribute'
  - locale.acceptfromhttp.md: 'Locale::acceptFromHttp »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас Locale
---
# Клас Locale

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

## Вступ

"Locale" - це ідентифікатор, який використовується для розпізнавання мови, культури або регіональних особливостей поведінки API. Локалі PHP організовані та позначені так само як і локалі CLDR, що використовуються ICU та багатьма виробниками систем Unix, Linux та Mac, Java тощо. Локалі позначаються згідно з мовними мітками стандарту RFC 4646 (який використовує тире, а не підкреслення) на додаток до традиційного позначення з використанням символу підкреслення. Функції даного класу розуміють обидва написання, якщо не вказано інше.

Приклади ідентифікаторів:

-   en-US (Англійська, США)
-   zh-Hant-TW (Китайська, Традиційне зображення, Тайвань)
-   fr-CA, fr-FR (Канадська Французька та Французька відповідно)

Клас Locale (і відповідні процедурні функції) використовується для взаємодії з ідентифікаторами локалів, перевірки правильного складання ідентифікатора, його коректності і т.д. Модулі використовуються CLDR в UAX #35 (і успадковується ICU), є коректними і використовуються скрізь вони були б у ICU.

Цей клас не можна інстанціювати як об'єкт. Усі методи/функції оголошено статичними.

**`null`** або порожній рядок будуть рахуватися за "базовий" локаль. "Базова" локаль - це "enУСPOSIX" в CLDR. Мовні мітки (і ідентифікатори локалі) реєстронезалежні. У даному класі присутній метод, що перетворює їх до канонічного вигляду.

## Огляд класів

```classsynopsis

     
    

    
     
      class Locale
     
     {

    /* Методы */
    
   public static acceptFromHttp(string $header): string|false
public static canonicalize(string $locale): ?string
public static composeLocale(array $subtags): string|false
public static filterMatches(string $languageTag, string $locale, bool $canonicalize = false): ?bool
locale_filter_matches(string $langtag, string $locale, bool $canonicalize = false): ?bool
public static getAllVariants(string $locale): ?array
public static getDefault(): string
public static getDisplayLanguage(string $locale, ?string $displayLocale = null): string|false
public static getDisplayName(string $locale, ?string $displayLocale = null): string|false
public static getDisplayRegion(string $locale, ?string $displayLocale = null): string|false
public static getDisplayScript(string $locale, ?string $displayLocale = null): string|false
public static getDisplayVariant(string $locale, ?string $displayLocale = null): string|false
public static getKeywords(string $locale): array|false|null
public static getPrimaryLanguage(string $locale): ?string
public static getRegion(string $locale): ?string
public static getScript(string $locale): ?string
public static lookup(    array $languageTag,    string $locale,    bool $canonicalize = false,    ?string $defaultLocale = null): ?string
public static parseLocale(string $locale): ?array
public static setDefault(string $locale): bool

   }
```

## Обумовлені константи

**`Locale::DEFAULT_LOCALE`** (null)

Використовується як параметр, що задає локаль у функціях, де це необхідно, таких як NumberFormatter. Ця константа змушує використовувати локаль за промовчанням.

Ці константи описують вибір локалі для методу getLocale різних класів.

**`Locale::ACTUAL_LOCALE`** (string)

Описує поточний локаль.

**`Locale::VALID_LOCALE`** (string)

Це найспецифічніша локаль, що підтримується ICU.

Ці константи описують, як розбираються або з чого складаються локалі. Вони використовуються як ключі масиву аргументів для [localecompose()](locale.composelocale.md) і як значення, що повертаються [localeparse()](locale.parselocale.md) у вигляді ключів асоціативного масиву, що повертається.

**`Locale::LANG_TAG`** (string)

Мітка для мови

**`Locale::EXTLANG_TAG`** (string)

Розширена мітка мови

**`Locale::SCRIPT_TAG`** (string)

Мітка зображення

**`Locale::REGION_TAG`** (string)

Мітка регіону

**`Locale::VARIANT_TAG`** (string)

Мітка варіанта

**`Locale::GRANDFATHERED_LANG_TAG`** (string)

Мітка мови у старому синтаксисі (grandfathered)

**`Locale::PRIVATE_TAG`** (string)

Приватна мітка

## Дивіться також

-   [» RFC 4646 - мітки для ідентифікаторів мов](http://www.faqs.org/rfcs/rfc4646)
-   [» RFC 4647 - перевірка мовних міток](http://www.faqs.org/rfcs/rfc4647)
-   [» Проект Unicode CLDR: Стандартний репозиторій даних локалей](http://www.unicode.org/cldr/)
-   [» Регістр мовних міток IANA](http://www.iana.org/assignments/language-subtag-registry)
-   [» Руководство пользователя ICU - Локаль](https://unicode-org.github.io/icu/userguide/locale/)
-   [» ICU api локалі](http://www.icu-project.org/apiref/icu4c/uloc_8h.md#details)

## Зміст

-   [Locale::acceptFromHttp](locale.acceptfromhttp.md) — Спробувати визначити найкращу локаль на основі заголовку HTTP "Accept-Language"
-   [Locale::canonicalize](locale.canonicalize.md) - Канонізувати рядок локалі
-   [Locale::composeLocale](locale.composelocale.md) — Повертає коректно відсортовані та розділені ідентифікатори локалі
-   [Locale::filterMatches](locale.filtermatches.md) — Перевірити, чи тег фільтра мови локалі відповідає
-   [Locale::getAllVariants](locale.getallvariants.md) — Отримання варіантів із переданої локалі
-   [Locale::getDefault](locale.getdefault.md) — Отримання значення локалі INTL за замовчуванням із опції 'defaultlocale'
-   [Locale::getDisplayLanguage](locale.getdisplaylanguage.md) — Повертає відповідним чином локалізоване ім'я мови для заданої локалі
-   [Locale::getDisplayName](locale.getdisplayname.md) - Повертає відповідним чином локалізоване ім'я локалі
-   [Locale::getDisplayRegion](locale.getdisplayregion.md) — Повертає відповідним чином локалізовану назву регіону для заданої локалі
-   [Locale::getDisplayScript](locale.getdisplayscript.md) — Повертає відповідним чином локалізовану назву алфавіту для заданої локалі
-   [Locale::getDisplayVariant](locale.getdisplayvariant.md) — Повертає відповідним чином локалізовану назву варіанта для заданої локалі
-   [Locale::getKeywords](locale.getkeywords.md) — Отримати ключові слова для локалі
-   [Locale::getPrimaryLanguage](locale.getprimarylanguage.md) — Отримати первинну мову для локалі
-   [Locale::getRegion](locale.getregion.md) — Отримати регіон для локалі
-   [Locale::getScript](locale.getscript.md) - Отримати алфавіт для локалі
-   [Locale::lookup](locale.lookup.md) — Пошук мовних позначок найбільш відповідних заданої локалі
-   [Locale::parseLocale](locale.parselocale.md) — Здобути асоціативний масив усіх підтегів локалі
-   [Locale::setDefault](locale.setdefault.md) — Встановити локаль за умовчанням під час виконання

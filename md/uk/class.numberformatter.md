---
navigation:
  - collator.sort.md: '« Collator::sort'
  - numberformatter.create.md: 'NumberFormatter::create »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: The NumberFormatter class
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# The NumberFormatter class

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

## Вступ

Програми зберігають і оперують числами використовуючи незалежне від локалі бінарне подання. Коли вони виводяться на екран або друкуються, вони конвертуються в рядки відповідно до вимог локалі. Наприклад, число 12345.67 виведеться як "12,345.67" у локалі US, як "12 345,67" у французькій локалі і як "12.345,67" у німецькій.

Викликаючи методи цього класу, ви можете форматувати числа, грошові одиниці та відсоткові величини у поданні потрібної локалі. Клас NumberFormatter чутливий до локалі, тому вам потрібно буде створювати новий екземпляр класу для кожної локалі. Методи NumberFormatter форматують примітивні типи чисел, такі як "double", і виводять їх у специфічному для локалі поданні.

Для грошових одиниць можна використовувати тип форматування грошових одиниць, який повертає рядок з відформатованим числом та символом грошової одиниці. Звичайно NumberFormatter не знає про курси обміну, так що для всіх грошових одиниць буде повернуто одне і те ж число. Наприклад, для числа 9988776.65 результат буде таким:

-   9 988 776,65 € для Франції
-   9.988.776,65 € для Німеччини
-   $9,988,776.65 для США

Для форматування відсоткових величин використовується тип форматування. За такого форматування число 0.75 буде виведено як 75%.

Для більш складного форматування, наприклад для аналізу числа, використовується форматування засноване на наборі правил.

## Огляд класів

```classsynopsis

    
     class NumberFormatter
     {

    /* Константы */
    
     public
     const
     int
      PATTERN_DECIMAL;

    public
     const
     int
      DECIMAL;

    public
     const
     int
      CURRENCY;

    public
     const
     int
      PERCENT;

    public
     const
     int
      SCIENTIFIC;

    public
     const
     int
      SPELLOUT;

    public
     const
     int
      ORDINAL;

    public
     const
     int
      DURATION;

    public
     const
     int
      PATTERN_RULEBASED;

    public
     const
     int
      IGNORE;

    public
     const
     int
      CURRENCY_ACCOUNTING;

    public
     const
     int
      DEFAULT_STYLE;

    public
     const
     int
      ROUND_CEILING;

    public
     const
     int
      ROUND_FLOOR;

    public
     const
     int
      ROUND_DOWN;

    public
     const
     int
      ROUND_UP;

    public
     const
     int
      ROUND_HALFEVEN;

    public
     const
     int
      ROUND_HALFDOWN;

    public
     const
     int
      ROUND_HALFUP;

    public
     const
     int
      PAD_BEFORE_PREFIX;

    public
     const
     int
      PAD_AFTER_PREFIX;

    public
     const
     int
      PAD_BEFORE_SUFFIX;

    public
     const
     int
      PAD_AFTER_SUFFIX;

    public
     const
     int
      PARSE_INT_ONLY;

    public
     const
     int
      GROUPING_USED;

    public
     const
     int
      DECIMAL_ALWAYS_SHOWN;

    public
     const
     int
      MAX_INTEGER_DIGITS;

    public
     const
     int
      MIN_INTEGER_DIGITS;

    public
     const
     int
      INTEGER_DIGITS;

    public
     const
     int
      MAX_FRACTION_DIGITS;

    public
     const
     int
      MIN_FRACTION_DIGITS;

    public
     const
     int
      FRACTION_DIGITS;

    public
     const
     int
      MULTIPLIER;

    public
     const
     int
      GROUPING_SIZE;

    public
     const
     int
      ROUNDING_MODE;

    public
     const
     int
      ROUNDING_INCREMENT;

    public
     const
     int
      FORMAT_WIDTH;

    public
     const
     int
      PADDING_POSITION;

    public
     const
     int
      SECONDARY_GROUPING_SIZE;

    public
     const
     int
      SIGNIFICANT_DIGITS_USED;

    public
     const
     int
      MIN_SIGNIFICANT_DIGITS;

    public
     const
     int
      MAX_SIGNIFICANT_DIGITS;

    public
     const
     int
      LENIENT_PARSE;

    public
     const
     int
      POSITIVE_PREFIX;

    public
     const
     int
      POSITIVE_SUFFIX;

    public
     const
     int
      NEGATIVE_PREFIX;

    public
     const
     int
      NEGATIVE_SUFFIX;

    public
     const
     int
      PADDING_CHARACTER;

    public
     const
     int
      CURRENCY_CODE;

    public
     const
     int
      DEFAULT_RULESET;

    public
     const
     int
      PUBLIC_RULESETS;

    public
     const
     int
      DECIMAL_SEPARATOR_SYMBOL;

    public
     const
     int
      GROUPING_SEPARATOR_SYMBOL;

    public
     const
     int
      PATTERN_SEPARATOR_SYMBOL;

    public
     const
     int
      PERCENT_SYMBOL;

    public
     const
     int
      ZERO_DIGIT_SYMBOL;

    public
     const
     int
      DIGIT_SYMBOL;

    public
     const
     int
      MINUS_SIGN_SYMBOL;

    public
     const
     int
      PLUS_SIGN_SYMBOL;

    public
     const
     int
      CURRENCY_SYMBOL;

    public
     const
     int
      INTL_CURRENCY_SYMBOL;

    public
     const
     int
      MONETARY_SEPARATOR_SYMBOL;

    public
     const
     int
      EXPONENTIAL_SYMBOL;

    public
     const
     int
      PERMILL_SYMBOL;

    public
     const
     int
      PAD_ESCAPE_SYMBOL;

    public
     const
     int
      INFINITY_SYMBOL;

    public
     const
     int
      NAN_SYMBOL;

    public
     const
     int
      SIGNIFICANT_DIGIT_SYMBOL;

    public
     const
     int
      MONETARY_GROUPING_SEPARATOR_SYMBOL;

    public
     const
     int
      TYPE_DEFAULT;

    public
     const
     int
      TYPE_INT32;

    public
     const
     int
      TYPE_INT64;

    public
     const
     int
      TYPE_DOUBLE;

    public
     const
     int
      TYPE_CURRENCY;


    /* Методы */
    
   public __construct(string $locale, int $style, ?string $pattern = null)

    public static create(string $locale, int $style, ?string $pattern = null): ?NumberFormatter
public formatCurrency(float $amount, string $currency): string|false
public format(int|float $num, int $type = NumberFormatter::TYPE_DEFAULT): string|false
public getAttribute(int $attribute): int|float|false
public getErrorCode(): int
public getErrorMessage(): string
public getLocale(int $type = ULOC_ACTUAL_LOCALE): string|false
public getPattern(): string|false
public getSymbol(int $symbol): string|false
public getTextAttribute(int $attribute): string|false
public parseCurrency(string $string, string &$currency, int &$offset = null): float|false
public parse(string $string, int $type = NumberFormatter::TYPE_DOUBLE, int &$offset = null): int|float|false
public setAttribute(int $attribute, int|float $value): bool
public setPattern(string $pattern): bool
public setSymbol(int $symbol, string $value): bool
public setTextAttribute(int $attribute, string $value): bool

   }
```

## Обумовлені константи

Ці стилі використовуються функцією [numfmt\_create()](numberformatter.create.md)для определения типа форматирования.

**`NumberFormatter::PATTERN_DECIMAL`**

Формат із десятковою точкою заданий шаблоном

**`NumberFormatter::DECIMAL`**

Формат із десятковою точкою

**`NumberFormatter::CURRENCY`**

грошовий формат

**`NumberFormatter::PERCENT`**

Відсотковий формат

**`NumberFormatter::SCIENTIFIC`**

Науковий формат

**`NumberFormatter::SPELLOUT`**

Розібраний формат на основі правил

**`NumberFormatter::ORDINAL`**

Чисельний формат на основі правил

**`NumberFormatter::DURATION`**

Формат тривалості на основі правил

**`NumberFormatter::PATTERN_RULEBASED`**

Формат на основі правил за шаблоном

**`NumberFormatter::CURRENCY_ACCOUNTING`**

Формат валюти для обліку, наприклад, `($3.00)` для негативної суми у валюті замість `-$3.00`. Доступно з PHP 7.4.1 та ICU 53.

**`NumberFormatter::DEFAULT_STYLE`**

Формат за промовчанням для локалі

**`NumberFormatter::IGNORE`**

Псевдонім для PATTERN\_DECIMAL

Дані константи визначають, як будуть розібрані чи відформатовані числа. Їх необхідно передавати функціям [numfmt\_format()](numberformatter.format.md) і [numfmt\_parse()](numberformatter.parse.md)

**`NumberFormatter::TYPE_DEFAULT`**

Тип визначається типом змінної

**`NumberFormatter::TYPE_INT32`**

Форматування/розбір як 32-бітного цілого

**`NumberFormatter::TYPE_INT64`**

Форматування/розбір як 64-бітного цілого

**`NumberFormatter::TYPE_DOUBLE`**

Форматування/розбір як раціонального (float)

**`NumberFormatter::TYPE_CURRENCY`**

Форматування/розбір як грошової одиниці. Застаріло, починаючи з PHP 8.3.0

Атрибут формата чисел для[numfmt\_get\_attribute()](numberformatter.getattribute.md) і [numfmt\_set\_attribute()](numberformatter.setattribute.md)

**`NumberFormatter::PARSE_INT_ONLY`**

Розбирати лише цілі.

**`NumberFormatter::GROUPING_USED`**

Використовувати роздільник, що групує.

**`NumberFormatter::DECIMAL_ALWAYS_SHOWN`**

Завжди показувати десяткову точку.

**`NumberFormatter::MAX_INTEGER_DIGITS`**

Максимальна кількість цілих цифр.

**`NumberFormatter::MIN_INTEGER_DIGITS`**

Мінімальна кількість цілих цифр.

**`NumberFormatter::INTEGER_DIGITS`**

Цілих цифр.

**`NumberFormatter::MAX_FRACTION_DIGITS`**

Максимальна кількість цифр після коми.

**`NumberFormatter::MIN_FRACTION_DIGITS`**

Мінімальна кількість цифр після коми.

**`NumberFormatter::FRACTION_DIGITS`**

Число цифр після коми.

**`NumberFormatter::MULTIPLIER`**

Множник.

**`NumberFormatter::GROUPING_SIZE`**

Розмір угруповання.

**`NumberFormatter::ROUNDING_MODE`**

Режим заокруглення.

**`NumberFormatter::ROUNDING_INCREMENT`**

Збільшення округлення.

**`NumberFormatter::FORMAT_WIDTH`**

Ширина, на яку буде доповнено виведення format().

**`NumberFormatter::PADDING_POSITION`**

Позиція з якою доповнення матиме місце. Дивіться опис констант доповнення.

**`NumberFormatter::SECONDARY_GROUPING_SIZE`**

Вторинний розмір угруповання.

**`NumberFormatter::SIGNIFICANT_DIGITS_USED`**

Використовувати цифри.

**`NumberFormatter::MIN_SIGNIFICANT_DIGITS`**

Мінімальна кількість цифр.

**`NumberFormatter::MAX_SIGNIFICANT_DIGITS`**

Максимальна кількість цифр.

**`NumberFormatter::LENIENT_PARSE`**

Режим поблажливий синтаксичного аналізу для заснованих на правилах форматів.

Атрибути тексту форматування чисел, що використовуються в [numfmt\_get\_text\_attribute()](numberformatter.gettextattribute.md) і [numfmt\_set\_text\_attribute()](numberformatter.settextattribute.md)

**`NumberFormatter::POSITIVE_PREFIX`**

Позитивний префікс.

**`NumberFormatter::POSITIVE_SUFFIX`**

Позитивний суфікс.

**`NumberFormatter::NEGATIVE_PREFIX`**

Негативний префікс.

**`NumberFormatter::NEGATIVE_SUFFIX`**

Негативний суфікс.

**`NumberFormatter::PADDING_CHARACTER`**

Символ для доповнення рядка.

**`NumberFormatter::CURRENCY_CODE`**

Код грошової одиниці ISO.

**`NumberFormatter::DEFAULT_RULESET`**

Набір стандартних правил. Доступно лише для форматування на основі правил.

**`NumberFormatter::PUBLIC_RULESETS`**

Публічний набір правил. Доступно лише для форматування на основі правил. Цей атрибут доступний лише для читання. Публічний набір правил повертається у вигляді рядка, в якому кожен набір правил відокремлений крапкою з комою (;).

Символи форматування чисел для [numfmt\_get\_symbol()](numberformatter.getsymbol.md) і [numfmt\_set\_symbol()](numberformatter.setsymbol.md)

**`NumberFormatter::DECIMAL_SEPARATOR_SYMBOL`**

Десятковий роздільник.

**`NumberFormatter::GROUPING_SEPARATOR_SYMBOL`**

Розділювач груп.

**`NumberFormatter::PATTERN_SEPARATOR_SYMBOL`**

Розділювач символ у шаблоні.

**`NumberFormatter::PERCENT_SYMBOL`**

Відсоток символ.

**`NumberFormatter::ZERO_DIGIT_SYMBOL`**

Нуль.

**`NumberFormatter::DIGIT_SYMBOL`**

Символ, що представляє цифру в шаблон.

**`NumberFormatter::MINUS_SIGN_SYMBOL`**

Мінус знак.

**`NumberFormatter::PLUS_SIGN_SYMBOL`**

Плюс знак.

**`NumberFormatter::CURRENCY_SYMBOL`**

Значок грошової одиниці символ.

**`NumberFormatter::INTL_CURRENCY_SYMBOL`**

The international currency symbol.

**`NumberFormatter::MONETARY_SEPARATOR_SYMBOL`**

Грошовий роздільник.

**`NumberFormatter::EXPONENTIAL_SYMBOL`**

Символ ступеня десяти.

**`NumberFormatter::PERMILL_SYMBOL`**

Символ проміле.

**`NumberFormatter::PAD_ESCAPE_SYMBOL`**

Екранування символ заповнювача.

**`NumberFormatter::INFINITY_SYMBOL`**

Нескінченності символ.

**`NumberFormatter::NAN_SYMBOL`**

Символ NAN (Not-a-number, нечисло).

**`NumberFormatter::SIGNIFICANT_DIGIT_SYMBOL`**

Значок цифри.

**`NumberFormatter::MONETARY_GROUPING_SEPARATOR_SYMBOL`**

Розділювач груп для фінансового формату.

Режими округлення для [numfmt\_get\_attribute()](numberformatter.getattribute.md) і [numfmt\_set\_attribute()](numberformatter.setattribute.md) з атрибутом **`NumberFormatter::ROUNDING_MODE`**

**`NumberFormatter::ROUND_CEILING`**

Округлення у бік позитивної нескінченності.

**`NumberFormatter::ROUND_DOWN`**

Округлення вниз.

**`NumberFormatter::ROUND_FLOOR`**

Округлення у бік негативної нескінченності.

**`NumberFormatter::ROUND_HALFDOWN`**

Округлення у бік "найближчого сусіда" крім випадків, коли вони на однаковій відстані. І тут округлення вниз.

**`NumberFormatter::ROUND_HALFEVEN`**

Округлення у бік "найближчого сусіда" крім випадків, коли вони на однаковій відстані. І тут округлення до парного значення.

**`NumberFormatter::ROUND_HALFUP`**

Округлення у бік "найближчого сусіда" крім випадків, коли вони на однаковій відстані. В цьому випадку заокруглення вгору.

**`NumberFormatter::ROUND_UP`**

Округлення вгору.

Значения позиции дополнения для[numfmt\_get\_attribute()](numberformatter.getattribute.md) і [numfmt\_set\_attribute()](numberformatter.setattribute.md) з атрибутом **`NumberFormatter::PADDING_POSITION`**

**`NumberFormatter::PAD_AFTER_PREFIX`**

Символи доповнення вставляються після префіксу.

**`NumberFormatter::PAD_AFTER_SUFFIX`**

Символи доповнення вставляються після суфіксу.

**`NumberFormatter::PAD_BEFORE_PREFIX`**

Символи доповнення вставляються до префіксу.

**`NumberFormatter::PAD_BEFORE_SUFFIX`**

Символи доповнення вставляються до суфіксу.

## Дивіться також

-   [»  ICU formatting documentation](https://unicode-org.github.io/icu/userguide/format_parse/)
-   [» ICU. Форматування чисел](https://unicode-org.github.io/icu/userguide/format_parse/numbers/)
-   [» ICU. Форматування десяткових дробів](https://unicode-org.github.io/icu-docs/apidoc/released/icu4c/classDecimalFormat.md)
-   [» ICU. Форматування на основі правил](https://unicode-org.github.io/icu/userguide/format_parse/numbers/rbnf.md)

## Зміст

-   [NumberFormatter::create](numberformatter.create.md)— Створює засіб форматування чисел
-   [NumberFormatter::formatCurrency](numberformatter.formatcurrency.md) \- Форматує значення валюти
-   [NumberFormatter::format](numberformatter.format.md) \- Форматує число
-   [NumberFormatter::getAttribute](numberformatter.getattribute.md)— Отримує атрибут
-   [NumberFormatter::getErrorCode](numberformatter.geterrorcode.md)— Отримує останній код помилки засобу форматування
-   [NumberFormatter::getErrorMessage](numberformatter.geterrormessage.md)— Отримує останнє повідомлення про помилку засобу форматування
-   [NumberFormatter::getLocale](numberformatter.getlocale.md)— Отримує локаль засобу форматування
-   [NumberFormatter::getPattern](numberformatter.getpattern.md)— Отримує шаблон засобу форматування
-   [NumberFormatter::getSymbol](numberformatter.getsymbol.md)— Отримує значення символу
-   [NumberFormatter::getTextAttribute](numberformatter.gettextattribute.md)— Отримує текстовий атрибут
-   [NumberFormatter::parseCurrency](numberformatter.parsecurrency.md) \- Розбирає номер валюти
-   [NumberFormatter::parse](numberformatter.parse.md) \- Розбирає число
-   [NumberFormatter::setAttribute](numberformatter.setattribute.md) \- Встановлює атрибут
-   [NumberFormatter::setPattern](numberformatter.setpattern.md)— Встановлює шаблон засобу форматування
-   [NumberFormatter::setSymbol](numberformatter.setsymbol.md)— Встановлює значення символу
-   [NumberFormatter::setTextAttribute](numberformatter.settextattribute.md) \- Встановлює текстовий атрибут

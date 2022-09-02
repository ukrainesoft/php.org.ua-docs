---
navigation:
  - collator.sort.md: '« Collator::sort'
  - numberformatter.create.md: 'NumberFormatter::create »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: NumberFormatter class
---
# NumberFormatter class

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

## Вступ

Програми зберігають і оперують числами використовуючи бінарну виставу, яка не залежить від локалі. Коли вони виводяться на екран або друкуються, вони конвертуються в рядки відповідно до вимог локалі. Наприклад, число 12345.67 виведеться як "12,345.67" у локалі US, як "12 345,67" у французькій локалі і як "12.345,67" у німецькій.

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

Ці стилі використовуються функцією [numfmtcreate()](numberformatter.create.md) визначення типу форматування.

**`NumberFormatter::PATTERN_DECIMAL`** (int)

Формат із десятковою точкою заданий шаблоном

**`NumberFormatter::DECIMAL`** (int)

Формат із десятковою точкою

**`NumberFormatter::CURRENCY`** (int)

грошовий формат

**`NumberFormatter::PERCENT`** (int)

Відсотковий формат

**`NumberFormatter::SCIENTIFIC`** (int)

Науковий формат

**`NumberFormatter::SPELLOUT`** (int)

Розібраний формат на основі правил

**`NumberFormatter::ORDINAL`** (int)

Чисельний формат на основі правил

**`NumberFormatter::DURATION`** (int)

Формат тривалості на основі правил

**`NumberFormatter::PATTERN_RULEBASED`** (int)

Формат на основі правил за шаблоном

**`NumberFormatter::CURRENCY_ACCOUNTING`** (int)

Формат валюти для обліку, наприклад, `($3.00)` для негативної суми у валюті замість `-$3.00`. Доступно з PHP 7.4.1 та ICU 53.

**`NumberFormatter::DEFAULT_STYLE`** (int)

Формат за промовчанням для локалі

**`NumberFormatter::IGNORE`** (int)

Псевдонім для PATTERNDECIMAL

Дані константи визначають, як будуть розібрані чи відформатовані числа. Їх необхідно передавати функціям [numfmtformat()](numberformatter.format.md) і [numfmtparse()](numberformatter.parse.md)

**`NumberFormatter::TYPE_DEFAULT`** (int)

Тип визначається типом змінної

**`NumberFormatter::TYPE_INT32`** (int)

Форматування/розбір як 32-бітового цілого

**`NumberFormatter::TYPE_INT64`** (int)

Форматування/розбір як 64-бітного цілого

**`NumberFormatter::TYPE_DOUBLE`** (int)

Форматування/розбір як раціонального (float)

**`NumberFormatter::TYPE_CURRENCY`** (int)

Форматування/розбір як грошової одиниці

Атрибут формату чисел для [numfmtgetattribute()](numberformatter.getattribute.md) і [numfmtsetattribute()](numberformatter.setattribute.md)

**`NumberFormatter::PARSE_INT_ONLY`** (int)

Розбирати лише цілі.

**`NumberFormatter::GROUPING_USED`** (int)

Використовувати роздільник, що групує.

**`NumberFormatter::DECIMAL_ALWAYS_SHOWN`** (int)

Завжди показувати десяткову точку.

**`NumberFormatter::MAX_INTEGER_DIGITS`** (int)

Максимальна кількість цілих цифр.

**`NumberFormatter::MIN_INTEGER_DIGITS`** (int)

Мінімальна кількість цілих цифр.

**`NumberFormatter::INTEGER_DIGITS`** (int)

Цілих цифр.

**`NumberFormatter::MAX_FRACTION_DIGITS`** (int)

Максимальна кількість цифр після коми.

**`NumberFormatter::MIN_FRACTION_DIGITS`** (int)

Мінімальна кількість цифр після коми.

**`NumberFormatter::FRACTION_DIGITS`** (int)

Число цифр після коми.

**`NumberFormatter::MULTIPLIER`** (int)

Множник.

**`NumberFormatter::GROUPING_SIZE`** (int)

Розмір угруповання.

**`NumberFormatter::ROUNDING_MODE`** (int)

Режим заокруглення.

**`NumberFormatter::ROUNDING_INCREMENT`** (int)

Збільшення округлення.

**`NumberFormatter::FORMAT_WIDTH`** (int)

Ширина, на яку буде доповнено виведення format().

**`NumberFormatter::PADDING_POSITION`** (int)

Позиція з якою доповнення матиме місце. Дивіться опис констант доповнення.

**`NumberFormatter::SECONDARY_GROUPING_SIZE`** (int)

Вторинний розмір угруповання.

**`NumberFormatter::SIGNIFICANT_DIGITS_USED`** (int)

Використовувати цифри.

**`NumberFormatter::MIN_SIGNIFICANT_DIGITS`** (int)

Мінімальна кількість цифр.

**`NumberFormatter::MAX_SIGNIFICANT_DIGITS`** (int)

Максимальна кількість цифр.

**`NumberFormatter::LENIENT_PARSE`** (int)

Режим поблажливий синтаксичного аналізу для заснованих на правилах форматів.

Атрибути тексту форматування чисел, що використовуються в [numfmtgettextattribute()](numberformatter.gettextattribute.md) і [numfmtsettextattribute()](numberformatter.settextattribute.md)

**`NumberFormatter::POSITIVE_PREFIX`** (int)

Позитивний префікс.

**`NumberFormatter::POSITIVE_SUFFIX`** (int)

Позитивний суфікс.

**`NumberFormatter::NEGATIVE_PREFIX`** (int)

Негативний префікс.

**`NumberFormatter::NEGATIVE_SUFFIX`** (int)

Негативний суфікс.

**`NumberFormatter::PADDING_CHARACTER`** (int)

Символ для доповнення рядка.

**`NumberFormatter::CURRENCY_CODE`** (int)

Код грошової одиниці ISO.

**`NumberFormatter::DEFAULT_RULESET`** (int)

Набір стандартних правил. Доступно лише для форматування на основі правил.

**`NumberFormatter::PUBLIC_RULESETS`** (int)

Публічний набір правил. Доступно лише для форматування на основі правил. Цей атрибут доступний лише для читання. Публічний набір правил повертається у вигляді рядка, в якому кожен набір правил відокремлений крапкою з комою (;).

Символи форматування чисел для [numfmtgetsymbol()](numberformatter.getsymbol.md) і [numfmtsetsymbol()](numberformatter.setsymbol.md)

**`NumberFormatter::DECIMAL_SEPARATOR_SYMBOL`** (int)

Десятковий роздільник.

**`NumberFormatter::GROUPING_SEPARATOR_SYMBOL`** (int)

Розділювач груп.

**`NumberFormatter::PATTERN_SEPARATOR_SYMBOL`** (int)

Розділювач символ у шаблоні.

**`NumberFormatter::PERCENT_SYMBOL`** (int)

Відсоток символ.

**`NumberFormatter::ZERO_DIGIT_SYMBOL`** (int)

Нуль.

**`NumberFormatter::DIGIT_SYMBOL`** (int)

Символ, що представляє цифру в шаблон.

**`NumberFormatter::MINUS_SIGN_SYMBOL`** (int)

Мінус знак.

**`NumberFormatter::PLUS_SIGN_SYMBOL`** (int)

Плюс знак.

**`NumberFormatter::CURRENCY_SYMBOL`** (int)

Значок грошової одиниці символ.

**`NumberFormatter::INTL_CURRENCY_SYMBOL`** (int)

The international currency symbol.

**`NumberFormatter::MONETARY_SEPARATOR_SYMBOL`** (int)

Грошовий роздільник.

**`NumberFormatter::EXPONENTIAL_SYMBOL`** (int)

Символ ступеня десяти.

**`NumberFormatter::PERMILL_SYMBOL`** (int)

Символ проміле.

**`NumberFormatter::PAD_ESCAPE_SYMBOL`** (int)

Екранування символ заповнювача.

**`NumberFormatter::INFINITY_SYMBOL`** (int)

Нескінченності символ.

**`NumberFormatter::NAN_SYMBOL`** (int)

Символ NAN (Not-a-number, нечисло).

**`NumberFormatter::SIGNIFICANT_DIGIT_SYMBOL`** (int)

Значок цифри.

**`NumberFormatter::MONETARY_GROUPING_SEPARATOR_SYMBOL`** (int)

Розділювач груп для фінансового формату.

Режими округлення для [numfmtgetattribute()](numberformatter.getattribute.md) і [numfmtsetattribute()](numberformatter.setattribute.md) з атрибутом **`NumberFormatter::ROUNDING_MODE`**

**`NumberFormatter::ROUND_CEILING`** (int)

Округлення у бік позитивної нескінченності.

**`NumberFormatter::ROUND_DOWN`** (int)

Округлення вниз.

**`NumberFormatter::ROUND_FLOOR`** (int)

Округлення у бік негативної нескінченності.

**`NumberFormatter::ROUND_HALFDOWN`** (int)

Округлення у бік "найближчого сусіда" крім випадків, коли вони на однаковій відстані. І тут округлення вниз.

**`NumberFormatter::ROUND_HALFEVEN`** (int)

Округлення у бік "найближчого сусіда" крім випадків, коли вони на однаковій відстані. І тут округлення до парного значення.

**`NumberFormatter::ROUND_HALFUP`** (int)

Округлення у бік "найближчого сусіда" крім випадків, коли вони на однаковій відстані. В цьому випадку заокруглення вгору.

**`NumberFormatter::ROUND_UP`** (int)

Округлення вгору.

Значення позиції доповнення для [numfmtgetattribute()](numberformatter.getattribute.md) і [numfmtsetattribute()](numberformatter.setattribute.md) з атрибутом **`NumberFormatter::PADDING_POSITION`**

**`NumberFormatter::PAD_AFTER_PREFIX`** (int)

Символи доповнення вставляються після префіксу.

**`NumberFormatter::PAD_AFTER_SUFFIX`** (int)

Символи доповнення вставляються після суфіксу.

**`NumberFormatter::PAD_BEFORE_PREFIX`** (int)

Символи доповнення вставляються до префіксу.

**`NumberFormatter::PAD_BEFORE_SUFFIX`** (int)

Символи доповнення вставляються до суфіксу.

## Дивіться також

-   [»  ICU formatting documentation](https://unicode-org.github.io/icu/userguide/format_parse/)
-   [» ICU. Форматування чисел](https://unicode-org.github.io/icu/userguide/format_parse/numbers/)
-   [» ICU. Форматування десяткових дробів](http://www.icu-project.org/apiref/icu4c/classDecimalFormat.md#details)
-   [»  ICU. Форматирование на основе правил](http://www.icu-project.org/apiref/icu4c/classRuleBasedNumberFormat.md#details)

## Зміст

-   [NumberFormatter::create](numberformatter.create.md) — Створює засіб форматування чисел
-   [NumberFormatter::formatCurrency](numberformatter.formatcurrency.md) - Форматує значення валюти
-   [NumberFormatter::format](numberformatter.format.md) - Форматує число
-   [NumberFormatter::getAttribute](numberformatter.getattribute.md) — Отримує атрибут
-   [NumberFormatter::getErrorCode](numberformatter.geterrorcode.md) — Отримує останній код помилки засобу форматування
-   [NumberFormatter::getErrorMessage](numberformatter.geterrormessage.md) — Отримує останнє повідомлення про помилку засобу форматування
-   [NumberFormatter::getLocale](numberformatter.getlocale.md) — Отримує локаль засобу форматування
-   [NumberFormatter::getPattern](numberformatter.getpattern.md) — Отримує шаблон засобу форматування
-   [NumberFormatter::getSymbol](numberformatter.getsymbol.md) — Отримує значення символу
-   [NumberFormatter::getTextAttribute](numberformatter.gettextattribute.md) — Отримує текстовий атрибут
-   [NumberFormatter::parseCurrency](numberformatter.parsecurrency.md) - Розбирає номер валюти
-   [NumberFormatter::parse](numberformatter.parse.md) - Розбирає число
-   [NumberFormatter::setAttribute](numberformatter.setattribute.md) - Встановлює атрибут
-   [NumberFormatter::setPattern](numberformatter.setpattern.md) — Встановлює шаблон засобу форматування
-   [NumberFormatter::setSymbol](numberformatter.setsymbol.md) — Встановлює значення символу
-   [NumberFormatter::setTextAttribute](numberformatter.settextattribute.md) - Встановлює текстовий атрибут

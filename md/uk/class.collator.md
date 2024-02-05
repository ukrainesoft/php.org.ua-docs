---
navigation:
  - intl.examples.basic.md: « Основи використання модуля
  - collator.asort.md: 'Collator::asort »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас Collator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Collator

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

## Вступ

Здійснює порівняння рядків із підтримкою порядку сортування специфічного для локалі.

## Огляд класів

```classsynopsis

    
     class Collator
     {

    /* Константы */
    
     const
     int
      DEFAULT_VALUE;

    const
     int
      PRIMARY;

    const
     int
      SECONDARY;

    const
     int
      TERTIARY;

    const
     int
      DEFAULT_STRENGTH;

    const
     int
      QUATERNARY;

    const
     int
      IDENTICAL;

    const
     int
      OFF;

    const
     int
      ON;

    const
     int
      SHIFTED;

    const
     int
      NON_IGNORABLE;

    const
     int
      LOWER_FIRST;

    const
     int
      UPPER_FIRST;

    const
     int
      FRENCH_COLLATION;

    const
     int
      ALTERNATE_HANDLING;

    const
     int
      CASE_FIRST;

    const
     int
      CASE_LEVEL;

    const
     int
      NORMALIZATION_MODE;

    const
     int
      STRENGTH;

    const
     int
      HIRAGANA_QUATERNARY_MODE;

    const
     int
      NUMERIC_COLLATION;

    const
     int
      SORT_REGULAR;

    const
     int
      SORT_STRING;

    const
     int
      SORT_NUMERIC;


    /* Методы */
    
   public __construct(string $locale)

    public asort(array &$array, int $flags = Collator::SORT_REGULAR): bool
public compare(string $string1, string $string2): int|false
public static create(string $locale): ?Collator
public getAttribute(int $attribute): int|false
public getErrorCode(): int|false
public getErrorMessage(): string|false
public getLocale(int $type): string|false
public getSortKey(string $string): string|false
public getStrength(): int
public setAttribute(int $attribute, int $value): bool
public setStrength(int $strength): bool
public sortWithSortKeys(array &$array): bool
public sort(array &$array, int $flags = Collator::SORT_REGULAR): bool

   }
```

## Обумовлені константи

**`Collator::FRENCH_COLLATION`**

Сортування рядків із акцентами з кінця рядка. Цей атрибут автоматично проставляється в *On* для французької та деяких інших локалей. Зазвичай користувачам не потрібно спеціально задавати цей параметр. Є деяка просадка продуктивності, якщо цей параметр встановлений як *On*але ніяк не впливає на довжину ключа сортування. Можливі значення:

-   **`Collator::ON`**
-   **`Collator::OFF`**(за замовчуванням)
-   **`Collator::DEFAULT_VALUE`**

**Приклад #1 Правила FRENCH\_COLLATION**

-   F=OFF cote < coté < côte < côté
-   F=ON cote < côte < coté < côté

**`Collator::ALTERNATE_HANDLING`**

Атрибут "Alternate" використовується для контролю обробки так званих "змінних символів" в UCA: пробілові символи, знаки пунктуації та символи. Якщо "Alternate" встановлено як *NonIgnorable* (N), то відмінності у цих символах будуть вважатися такими ж значущими, як і різницю між літерами. Якщо "Alternate" встановлено як *Shifted* (S), ці символи будуть мати низьку значимість. Значення *Shifted* найчастіше використовується в комбінації з *Strength* встановленим у "Quaternary". У таких випадках подібні символи будуть враховуватися при сортуванні, але тільки якщо всі інші аспекти рядків (літери, акценти, реєстр) ідентичні. Якщо "Alternate" не встановлено як "Shifted", то різниці між "Strength" рівним 3 та 4 не буде. Докладніше та з прикладами читайте у розділі "Variable\_Weighting" на сайті [» UCA](https://www.unicode.org/reports/tr10/). . Причина, через яку значення для "Alternate" не використовуються просто *On*в*Off* у цьому, що у майбутньому можуть бути додані додаткові варіанти. Опція UCA "Blanked" виражається за допомогою "Strength" встановленого в "Alternate" встановленого в "Shifted". Для більшості локалей цей параметр за промовчанням дорівнює "NonIgnorable". Якщо задано "Shifted", то обробка може бути повільніша у випадку якщо у вас багато рядків, що відрізняються лише пунктуацією. Довжина ключа сортування не торкається тільки якщо також не збільшувався рівень "Strength".

Можливі значення:

-   **`Collator::NON_IGNORABLE`**(за замовчуванням)
-   **`Collator::SHIFTED`**
-   **`Collator::DEFAULT_VALUE`**

**Приклад #2 ALTERNATE\_HANDLING rules**

-   S=3, A=N di Silva < Di Silva < diSilva < U.S.A. < USA
-   S=3, A=S di Silva = diSilva < Di Silva < U.S.A. = USA
-   S=4, A=S di Silva < diSilva < Di Silva < U.S.A. < USA

**`Collator::CASE_FIRST`**

Атрибут "Case\_First" використовується для визначення порядку сортування залежно від регістру символів за відсутності інших відмінностей у рядках. Можливі значення: *Uppercase\_First*(U),*Lowercase\_First*(L),*Default*и*Off*. . Між "Off" та "Lowercase\_First" практично немає різниці, так що користувачі зазвичай не використовують "Lowercase\_First", а тільки Off або Uppercase\_Перший. (Ті, кому дійсно цікава різниця між X та L можуть звернутися до `Налаштування Collation`). Завдання L чи U не позначається швидкості порівняння, але впливає довжину ключа сортування.

Можливі значення:

-   **`Collator::OFF`**(за замовчуванням)
-   **`Collator::LOWER_FIRST`**
-   **`Collator::UPPER_FIRST`**
-   **`Collator:DEFAULT`**

**Приклад #3 Правила CASE\_FIRST**

-   C=X or C=L "china" < "China" < "denmark" < "Denmark"
-   C=U "China" < "china" < "Denmark" < "denmark"

**`Collator::CASE_LEVEL`**

Атрибут "Case\_Level" використовується, коли акценти не важливі, а реєстр важливий. У таких випадках встановіть "Strength" у значення *Primary*, та "Case\_Level" в *On*. . У більшості локалів за замовчуванням встановлено значення "Off". Має незначний вплив на швидкість порівняння та довжину ключа сортування якщо встановлено як *On*

Можливі значення:

-   **`Collator::OFF`**(за замовчуванням)
-   **`Collator::ON`**
-   **`Collator::DEFAULT_VALUE`**

**Приклад #4 CASE\_LEVEL rules**

-   S=1, E=X role = Role = rôle
-   S=1, E=O role = rôle < Role

**`Collator::NORMALIZATION_MODE`**

Налаштування "Normalization" визначає, чи буде ретельно нормалізований текст у порівнянні чи ні. Навіть якщо це налаштування вимкнено (за замовчуванням для багатьох локалей), текст у загальному випадку буде порівнюватися коректно (подробиці UTN #5). Проблеми можуть бути лише з відмітками акцентів, розташованими в неканонічному порядку. Якщо встановлено як *On*, то буде гарантовано найкращий результат всім можливих варіантів тексту. Однак, якщо встановлено як *On* - це позначиться швидкості порівняння, залежно від кількості послідовностей, який необхідно нормалізувати. Будь-якого помітного впливу на довжину ключа сортування не буде. Якщо заздалегідь відомо, що текст вже нормалізовано як NFD або NFKD, необхідності використання цього параметра немає.

Можливі значення:

-   **`Collator::OFF`**(за замовчуванням)
-   **`Collator::ON`**
-   **`Collator::DEFAULT_VALUE`**

**`Collator::STRENGTH`**

ICU Collation Service підтримує безліч рівнів порівняння (вони називаються "Levels", але також відомі як "Strengths"). Використання цих налаштувань дозволяє ICU сортувати рядки точно відповідно до правил локалі. Однак, дозволяючи вибіркове використання цих рівнів, пошук рядка в тексті можна проводити за допомогою різних умов. Більше інформації описано у розділі присвяченій [collator\_set\_strength()](collator.setstrength.md)

Можливі значення:

-   **`Collator::PRIMARY`**
-   **`Collator::SECONDARY`**
-   **`Collator::TERTIARY`**(за замовчуванням)
-   **`Collator::QUATERNARY`**
-   **`Collator::IDENTICAL`**
-   **`Collator::DEFAULT_VALUE`**

**`Collator::HIRAGANA_QUATERNARY_MODE`**

Сумісність з JIS x 4061 вимагає введення додаткового рівня виділення символів Hiragana і Katakana. Якщо потрібна сумісність зі стандартом, цей атрибут необхідно задати як *On*, а "Strength" як "Quaternary". Це позначиться на довжині ключа сортування та швидкості порівняння.

Можливі значення:

-   **`Collator::OFF`**(за замовчуванням)
-   **`Collator::ON`**
-   **`Collator::DEFAULT_VALUE`**

**`Collator::NUMERIC_COLLATION`**

Якщо включений, цей атрибут генерує ключ порівняння для числового значення підрядка цифр, що складається. Це дозволяє при сортуванні поміщати '100' після '2'.

Можливі значення:

-   **`Collator::OFF`**(за замовчуванням)
-   **`Collator::ON`**
-   **`Collator::DEFAULT_VALUE`**

**`Collator::DEFAULT_VALUE`**

**`Collator::PRIMARY`**

**`Collator::SECONDARY`**

**`Collator::TERTIARY`**

**`Collator::DEFAULT_STRENGTH`**

**`Collator::QUATERNARY`**

**`Collator::IDENTICAL`**

**`Collator::OFF`**

**`Collator::ON`**

**`Collator::SHIFTED`**

**`Collator::NON_IGNORABLE`**

**`Collator::LOWER_FIRST`**

**`Collator::UPPER_FIRST`**

**`Collator::SORT_REGULAR`**

**`Collator::SORT_STRING`**

**`Collator::SORT_NUMERIC`**

## Зміст

-   [Collator::asort](collator.asort.md)— Сортує масив із збереженням асоціації індексу
-   [Collator::compare](collator.compare.md)— Порівнює два рядки Unicode
-   [Collator::\_\_construct](collator.construct.md) \- Створює новий екземпляр Collator
-   [Collator::create](collator.create.md) \- Створює новий екземпляр Collator
-   [Collator::getAttribute](collator.getattribute.md)— Отримує значення атрибуту зіставлення
-   [Collator::getErrorCode](collator.geterrorcode.md)— Отримує останній код помилки Collator
-   [Collator::getErrorMessage](collator.geterrormessage.md)— Отримує текст для останньої помилки коду Collator
-   [Collator::getLocale](collator.getlocale.md) \- Отримує назву локалі для Collator
-   [Collator::getSortKey](collator.getsortkey.md)— Отримує ключ сортування рядка
-   [Collator::getStrength](collator.getstrength.md)— Отримує поточну силу зіставлення
-   [Collator::setAttribute](collator.setattribute.md) \- Встановлює атрибут зіставлення
-   [Collator::setStrength](collator.setstrength.md) \- Встановлює силу зіставлення
-   [Collator::sortWithSortKeys](collator.sortwithsortkeys.md)— Сортує масив із використанням зазначеного Collator та ключів сортування
-   [Collator::sort](collator.sort.md)— Сортує масив із використанням зазначеного засобу сортування

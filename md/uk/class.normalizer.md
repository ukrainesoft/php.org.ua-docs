Клас Normalizer

-   [« Locale::setDefault](locale.setdefault.html)
    
-   [Normalizer::getRawDecomposition »](normalizer.getrawdecomposition.html)
    
-   [PHP Manual](index.html)
    
-   [intl](book.intl.html)
    
-   Клас Normalizer
    

# Клас Normalizer

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

## Вступ

Нормалізація - це процес перетворення символів та його послідовностей у формальне уявлення нижчого рівня. Цей процес дуже важливий при порівнянні рядків при сортуванні або пошуку, але також використовується при збереженні тексту, щоб бути впевненим в тому, що він зберігся коректно.

Консорціум Unicode визначив кілька форм нормалізації, що відображають різні потреби додатків:

-   Normalization Form D (NFD) - Канонічне розкладання
-   Normalization Form C (NFC) - Канонічне розкладання з наступним канонічним складанням
-   Normalization Form KD (NFKD) - Сумісне розкладання
-   Normalization Form KC (NFKC) - Сумісне розкладання з подальшим канонічним складанням

Різні форми задаються у вимогах наборів перетворень тексту. Перетворення обчислюються з алгоритму та набору файлів даних.

## Огляд класів

```classsynopsis

     
    

    
     
      class Normalizer
     
     {

    /* Методы */
    
   public static getRawDecomposition(string $string, int $form = Normalizer::FORM_C): ?string
public static isNormalized(string $string, int $form = Normalizer::FORM_C): bool
public static normalize(string $string, int $form = Normalizer::FORM_C): string|false

   }
```

## Обумовлені константи

Дані константи задають форму нормалізації, що використовується нормалізатором:

**`Normalizer::FORM_C`** (int)

Форма нормалізації C (NFC) - канонічне розкладання, після якого канонічна збірка

**`Normalizer::FORM_D`** (int)

Форма нормалізації D (NFD) - Канонічне розкладання

**`Normalizer::FORM_KC`** (int)

Форма нормалізації KC (NFKC) – Сумісне розкладання, після якого канонічна збірка

**`Normalizer::FORM_KD`** (int)

Форма нормалізації KD (NFKD) - Сумісне розкладання

**`Normalizer::NONE`** (int)

Без розкладання/складання

**`Normalizer::OPTION_DEFAULT`** (int)

Звичайні налаштування нормалізації

## Дивіться також

-   [»  Нормализация Unicode](http://unicode.org/reports/tr15/)
-   [»  Нормализация Unicode. FAQ](http://unicode.org/faq/normalization.html)
-   [»  ICU Руководство пользователя - нормализация](https://unicode-org.github.io/icu/userguide/transforms/normalization/)
-   [»  ICU Описание API - нормализация](http://www.icu-project.org/apiref/icu4c/unorm_8h.html)

## Зміст

-   [Normalizer::getRawDecomposition](normalizer.getrawdecomposition.html) — Витягує властивість DecompositionMapping для заданого символу UTF-8
-   [Normalizer::isNormalized](normalizer.isnormalized.html) — Перевірити, чи переданий рядок відповідає заданій формі нормалізації
-   [Normalizer::normalize](normalizer.normalize.html) - Нормалізація рядка
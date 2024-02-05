---
navigation:
  - locale.setdefault.md: '« Locale::setDefault'
  - normalizer.getrawdecomposition.md: 'Normalizer::getRawDecomposition »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас Normalizer
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

    /* Константы */
    
     public
     const
     int
      FORM_D;

    public
     const
     int
      NFD;

    public
     const
     int
      FORM_KD;

    public
     const
     int
      NFKD;

    public
     const
     int
      FORM_C;

    public
     const
     int
      NFC;

    public
     const
     int
      FORM_KC;

    public
     const
     int
      NFKC;

    public
     const
     int
      FORM_KC_CF;

    public
     const
     int
      NFKC_CF;


    /* Методы */
    
   public static getRawDecomposition(string $string, int $form = Normalizer::FORM_C): ?string
public static isNormalized(string $string, int $form = Normalizer::FORM_C): bool
public static normalize(string $string, int $form = Normalizer::FORM_C): string|false

   }
```

## Обумовлені константи

Дані константи задають форму нормалізації, що використовується нормалізатором:

**`Normalizer::FORM_C`**

Форма нормалізації C (NFC) - канонічне розкладання, після якого канонічна збірка

**`Normalizer::FORM_D`**

Форма нормалізації D (NFD) - Канонічне розкладання

**`Normalizer::NFD`**

**`Normalizer::FORM_KC`**

Форма нормалізації KC (NFKC) – Сумісне розкладання, після якого канонічна збірка

**`Normalizer::NFKC`**

**`Normalizer::FORM_KC_CF`**

**`Normalizer::FORM_KD`**

Форма нормалізації KD (NFKD) - Сумісне розкладання

**`Normalizer::NFKD`**

**`Normalizer::NFC`**

**`Normalizer::NFKC_CF`**

## Дивіться також

-   [»  Нормалізація Unicode](http://unicode.org/reports/tr15/)
-   [» Нормалізація Unicode. FAQ](http://unicode.org/faq/normalization.md)
-   [»  ICU Посібник користувача - нормалізація](https://unicode-org.github.io/icu/userguide/transforms/normalization/)
-   [»  ICU Опис API - нормалізація](https://unicode-org.github.io/icu-docs/apidoc/dev/icu4c/unorm_8h.md)

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Константа\*\*`Normalizer::NONE`\*\* було видалено. |

## Зміст

-   [Normalizer::getRawDecomposition](normalizer.getrawdecomposition.md)— Витягує властивість Decomposition\_Mapping для заданого символу UTF-8
-   [Normalizer::isNormalized](normalizer.isnormalized.md)— Перевірити, чи переданий рядок відповідає заданій формі нормалізації
-   [Normalizer::normalize](normalizer.normalize.md) \- Нормалізація рядка

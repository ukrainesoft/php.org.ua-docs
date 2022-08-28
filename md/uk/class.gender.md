Клас GenderGender

-   [« Пример использования](gender.example.admin.html)
    
-   [Gender\\Gender::connect »](gender-gender.connect.html)
    
-   [PHP Manual](index.html)
    
-   [Gender](book.gender.html)
    
-   Клас GenderGender
    

# Клас GenderGender

(PECL gender >= 0.6.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class Gender\Gender
     
     {
    
    /* Константы */
    
     const
     int
      IS_FEMALE = 70;

    const
     int
      IS_MOSTLY_FEMALE = 102;

    const
     int
      IS_MALE = 77;

    const
     int
      IS_MOSTLY_MALE = 109;

    const
     int
      IS_UNISEX_NAME = 63;

    const
     int
      IS_A_COUPLE = 67;

    const
     int
      NAME_NOT_FOUND = 32;

    const
     int
      ERROR_IN_NAME = 69;

    const
     int
      ANY_COUNTRY = 0;

    const
     int
      BRITAIN = 1;

    const
     int
      IRELAND = 2;

    const
     int
      USA = 3;

    const
     int
      SPAIN = 4;

    const
     int
      PORTUGAL = 5;

    const
     int
      ITALY = 6;

    const
     int
      MALTA = 7;

    const
     int
      FRANCE = 8;

    const
     int
      BELGIUM = 9;

    const
     int
      LUXEMBOURG = 10;

    const
     int
      NETHERLANDS = 11;

    const
     int
      GERMANY = 12;

    const
     int
      EAST_FRISIA = 13;

    const
     int
      AUSTRIA = 14;

    const
     int
      SWISS = 15;

    const
     int
      ICELAND = 16;

    const
     int
      DENMARK = 17;

    const
     int
      NORWAY = 18;

    const
     int
      SWEDEN = 19;

    const
     int
      FINLAND = 20;

    const
     int
      ESTONIA = 21;

    const
     int
      LATVIA = 22;

    const
     int
      LITHUANIA = 23;

    const
     int
      POLAND = 24;

    const
     int
      CZECH_REP = 25;

    const
     int
      SLOVAKIA = 26;

    const
     int
      HUNGARY = 27;

    const
     int
      ROMANIA = 28;

    const
     int
      BULGARIA = 29;

    const
     int
      BOSNIA = 30;

    const
     int
      CROATIA = 31;

    const
     int
      KOSOVO = 32;

    const
     int
      MACEDONIA = 33;

    const
     int
      MONTENEGRO = 34;

    const
     int
      SERBIA = 35;

    const
     int
      SLOVENIA = 36;

    const
     int
      ALBANIA = 37;

    const
     int
      GREECE = 38;

    const
     int
      RUSSIA = 39;

    const
     int
      BELARUS = 40;

    const
     int
      MOLDOVA = 41;

    const
     int
      UKRAINE = 42;

    const
     int
      ARMENIA = 43;

    const
     int
      AZERBAIJAN = 44;

    const
     int
      GEORGIA = 45;

    const
     int
      KAZAKH_UZBEK = 46;

    const
     int
      TURKEY = 47;

    const
     int
      ARABIA = 48;

    const
     int
      ISRAEL = 49;

    const
     int
      CHINA = 50;

    const
     int
      INDIA = 51;

    const
     int
      JAPAN = 52;

    const
     int
      KOREA = 53;


    /* Методы */
    
   public __construct(string $dsn = ?)

    public connect(string $dsn): bool
public country(int $country): array|false
public get(string $name, int $country = ?): int
public isNick(string $name0, string $name1, int $country = ?): array
public similarNames(string $name, int $country = ?): array

   }
```

## Обумовлені константи

**`Gender\Gender::IS_FEMALE`**

**`Gender\Gender::IS_MOSTLY_FEMALE`**

**`Gender\Gender::IS_MALE`**

**`Gender\Gender::IS_MOSTLY_MALE`**

**`Gender\Gender::IS_UNISEX_NAME`**

**`Gender\Gender::IS_A_COUPLE`**

**`Gender\Gender::NAME_NOT_FOUND`**

**`Gender\Gender::ERROR_IN_NAME`**

**`Gender\Gender::ANY_COUNTRY`**

**`Gender\Gender::BRITAIN`**

**`Gender\Gender::IRELAND`**

**`Gender\Gender::USA`**

**`Gender\Gender::SPAIN`**

**`Gender\Gender::PORTUGAL`**

**`Gender\Gender::ITALY`**

**`Gender\Gender::MALTA`**

**`Gender\Gender::FRANCE`**

**`Gender\Gender::BELGIUM`**

**`Gender\Gender::LUXEMBOURG`**

**`Gender\Gender::NETHERLANDS`**

**`Gender\Gender::GERMANY`**

**`Gender\Gender::EAST_FRISIA`**

**`Gender\Gender::AUSTRIA`**

**`Gender\Gender::SWISS`**

**`Gender\Gender::ICELAND`**

**`Gender\Gender::DENMARK`**

**`Gender\Gender::NORWAY`**

**`Gender\Gender::SWEDEN`**

**`Gender\Gender::FINLAND`**

**`Gender\Gender::ESTONIA`**

**`Gender\Gender::LATVIA`**

**`Gender\Gender::LITHUANIA`**

**`Gender\Gender::POLAND`**

**`Gender\Gender::CZECH_REP`**

**`Gender\Gender::SLOVAKIA`**

**`Gender\Gender::HUNGARY`**

**`Gender\Gender::ROMANIA`**

**`Gender\Gender::BULGARIA`**

**`Gender\Gender::BOSNIA`**

**`Gender\Gender::CROATIA`**

**`Gender\Gender::KOSOVO`**

**`Gender\Gender::MACEDONIA`**

**`Gender\Gender::MONTENEGRO`**

**`Gender\Gender::SERBIA`**

**`Gender\Gender::SLOVENIA`**

**`Gender\Gender::ALBANIA`**

**`Gender\Gender::GREECE`**

**`Gender\Gender::RUSSIA`**

**`Gender\Gender::BELARUS`**

**`Gender\Gender::MOLDOVA`**

**`Gender\Gender::UKRAINE`**

**`Gender\Gender::ARMENIA`**

**`Gender\Gender::AZERBAIJAN`**

**`Gender\Gender::GEORGIA`**

**`Gender\Gender::KAZAKH_UZBEK`**

**`Gender\Gender::TURKEY`**

**`Gender\Gender::ARABIA`**

**`Gender\Gender::ISRAEL`**

**`Gender\Gender::CHINA`**

**`Gender\Gender::INDIA`**

**`Gender\Gender::JAPAN`**

**`Gender\Gender::KOREA`**

## Зміст

-   [Gender\\Gender::connect](gender-gender.connect.html) — З'єднання із зовнішньою базою імен
-   [Gender\\Gender::\_\_construct](gender-gender.construct.html) - Конструктор об'єкта класу Gender
-   [Gender\\Gender::country](gender-gender.country.html) — Отримати текстову виставу країни
-   [Gender\\Gender::get](gender-gender.get.html) — Отримати підлогу на ім'я
-   [Gender\\Gender::isNick](gender-gender.isnick.html) — Перевіряє, чи name0 є псевдонімом для name1
-   [Gender\\Gender::similarNames](gender-gender.similarnames.html) — Отримати схожі імена
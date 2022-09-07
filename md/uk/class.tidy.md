---
navigation:
  - tidy.examples.basic.md: « Пример использования Tidy
  - tidy.body.md: 'tidy::body »'
  - index.md: PHP Manual
  - book.tidy.md: Tidy
title: 'Клас tidy'
---
# Клас [tidy](class.tidy.md)

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

## Вступ

HTML-сайт в HTML-файлі, виявлений Tidy.

## Огляд класів

```classsynopsis

     
    

    
     
      class tidy
     
     {

    /* Свойства */
    
     public
     ?string
      $errorBuffer = null;

    public
     ?string
      $value = null;


    /* Методы */
    
   public __construct(    ?string $filename = null,    array|string|null $config = null,    ?string $encoding = null,    bool $useIncludePath = false)

    public body(): ?tidyNode
public cleanRepair(): bool
public diagnose(): bool
tidy_get_error_buffer(tidy $tidy): string|false
public getConfig(): array
public getHtmlVer(): int
public getOpt(string $option): string|int|bool
public getOptDoc(string $option): string|false
public getRelease(): string
public getStatus(): int
public head(): ?tidyNode
public html(): ?tidyNode
public isXhtml(): bool
public isXml(): bool
public parseFile(    string $filename,    array|string|null $config = null,    ?string $encoding = null,    bool $useIncludePath = false): bool
tidy_parse_file(    string $filename,    array|string|null $config = null,    ?string $encoding = null,    bool $useIncludePath = false): tidy|false
public parseString(string $string, array|string|null $config = null, ?string $encoding = null): bool
tidy_parse_string(string $string, array|string|null $config = null, ?string $encoding = null): tidy|false
public static repairFile(    string $filename,    array|string|null $config = null,    ?string $encoding = null,    bool $useIncludePath = false): string|false
public static repairString(string $string, array|string|null $config = null, ?string $encoding = null): string|false
public root(): ?tidyNode

   }
```

## Властивості

value

HTML-подання вузла, включаючи навколишні теги.

## Зміст

-   [tidy::body](tidy.body.md) — Повертає об'єкт tidyNode, починаючи з тега розібраного tidy-дерева
-   [tidy::cleanRepair](tidy.cleanrepair.md) — Виконати налаштоване очищення та відновлення розібраної розмітки
-   [tidy::construct](tidy.construct.md) - Створює новий tidy-об'єкт
-   [tidy::diagnose](tidy.diagnose.md) — Запуск настроєної діагностики для розібраної та відновленої розмітки
-   [tidy::$errorBuffer](tidy.props.errorbuffer.md) — Повертає попередження та помилки, які виникли при розборі зазначеного документа
-   [tidy::getConfig](tidy.getconfig.md) — Отримує поточну конфігурацію Tidy
-   [tidy::getHtmlVer](tidy.gethtmlver.md) — Отримує виявлену HTML версію для зазначеного документа
-   [tidy::getOpt](tidy.getopt.md) — Повертає значення вказаного конфігураційного параметра для документа tidy
-   [tidy::getOptDoc](tidy.getoptdoc.md) — Повертає опис для опції із зазначеною назвою
-   [tidy::getRelease](tidy.getrelease.md) — Отримати дату релізу (версію) для бібліотеки Tidy
-   [tidy::getStatus](tidy.getstatus.md) — Отримує статус зазначеного документа
-   [tidy::head](tidy.head.md) — Повертає об'єкт tidyNode, починаючи з тега розібраного tidy-дерева
-   [tidy::html](tidy.html.md) — Повертає об'єкт tidyNode, починаючи з тега розібраного tidy-дерева
-   [tidy::isXhtml](tidy.isxhtml.md) — Визначає, чи є документ XHTML-документом
-   [tidy::isXml](tidy.isxml.md) — Визначає, чи документ є спільним XML-документом (не HTML/XHTML)
-   [tidy::parseFile](tidy.parsefile.md) — Розбір розмітки у файлі або URI
-   [tidy::parseString](tidy.parsestring.md) — Розбір документа, що зберігається у рядку
-   [tidy::repairFile](tidy.repairfile.md) — Відновлює розмітку файлу та повертає його у вигляді рядка
-   [tidy::repairString](tidy.repairstring.md) — Відновлює рядок, використовуючи наскільки можна конфігураційний файл
-   [tidy::root](tidy.root.md) - Повертає об'єкт tidyNode, що представляє вершину розібраного tidy-дерева

---
navigation:
  - commonmark-parser.finish.html: '« CommonMarkParser::finish'
  - commonmark-cql.construct.html: 'CommonMarkCQL::construct »'
  - index.md: PHP Manual
  - book.cmark.md: CommonMark
title: Клас CommonMarkCQL
---
# Клас CommonMarkCQL

(cmark >= 1.1.0)

## Вступ

CommonMark Query Language - це DSL для опису того, як проходити через дерево вузлів CommonMark, реалізоване у вигляді синтаксичного аналізатора та компілятора для невеликого набору інструкцій та віртуальної машини для виконання цих інструкцій.

##### Шляхи:

У найбільш спрощеній формі запит CQL поєднує такі шляхи та `/`, щоб описати, як рухатися по дереву:

-   firstChild
-   lastChild
-   previous
-   next
-   parent

Наприклад, `/firstChild/lastChild` переміщатиметься до останнього дочірнього вузла першого дочірнього вузла.

##### Цикли

CQL може бути заданий цикл, наприклад, через дочірні елементи або дочірні елементи до певного вузла з використанням шляху `children` або `siblings`. Наприклад, `/firstChild/children` буде переміщатися всіма дочірніми елементами першого дочірнього вузла.

##### Підзапити

CQL можна проінструктувати, як переміщатися, використовуючи підзапит, такий як `[/firstChild]`. Наприклад, `/firstChild/children[/firstChild]` перейде до першого дочірнього вузла всіх вузлів першого дочірнього вузла.

##### Обмеження циклів

Під час циклу CQL може бути проінструктовано обмежувати пройдений шлях до вузлів певного типу. Наприклад, `/children(BlockQuote)` буде переміщатися до дочірніх елементів вузла, де типом є `BlockQuote`. Наступні типи розпізнаються (без урахування регістру):

-   BlockQuote
-   List
-   Item
-   CodeBlock
-   HtmlBlock
-   CustomBlock
-   Параграф
-   Heading
-   ThematicBreak
-   Text
-   SoftBreak
-   LineBreak
-   Code
-   HtmlInline
-   CustomInline
-   Emphasis
-   Strong
-   Link
-   Image

Типи можуть використовуватись як об'єднання, наприклад, `/children(BlockQuote|List)` буде переміщатися до дочірніх елементів вузла, де типом є `BlockQuote` або `List`. Типи або об'єднання типів також можуть бути скасовані. Наприклад, `/children(~BlockQuote)` буде переміщатися до дочірніх елементів вузла, де тип не є `BlockQuote`, а `/children(~BlockQuote|Paragraph)` буде переміщатися до дочірніх вузлів, де тип не є `BlockQuote` або `Paragraph`

##### Обмеження шляхів

CQL можна доручити створити цикл для переміщення до вузла певного типу певним шляхом. Наприклад, `/firstChild(BlockQuote)` перейде до першого дочірнього вузла з типом `BlockQuote`. Зверніть увагу, що як і інші цикли, `children` і `siblings`, цей тип шляху може супроводжуватися лише підзапитом.

##### Зауваження щодо реалізації

Хоча CQL реалізований як частина модуля PHP CommonMark, він стоїть окремо від PHP і не використовує віртуальну машину PHP або внутрішню виставу значень.

## Огляд класів

```classsynopsis


    
    
     
      class CommonMark\CQL
     
     {
    

    /* Конструктор */
    
   public __construct(string $query)


    /* Методы */
    public __invoke(CommonMark\Node $root, callable $handler)

   }
```

## Зміст

-   [CommonMarkCQL::construct](commonmark-cql.construct.html) - Конструктор класу CQL
-   [CommonMarkCQL::invoke](commonmark-cql.invoke.html) - Виконання CQL

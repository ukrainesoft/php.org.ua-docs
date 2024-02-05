---
navigation:
  - commonmark-parser.finish.md: '« CommonMark\\Parser::finish'
  - commonmark-cql.construct.md: 'CommonMark\\CQL::\_\_construct »'
  - index.md: PHP Manual
  - book.cmark.md: CommonMark
title: Клас CommonMark\\CQL
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас CommonMark\\CQL

(cmark >= 1.1.0)

## Вступ

CommonMark Query Language - це DSL для опису того, як проходити через дерево вузлів CommonMark, реалізоване у вигляді синтаксичного аналізатора та компілятора для невеликого набору інструкцій та віртуальної машини для виконання цих інструкцій.

##### Шляхи:

У найбільш спрощеній формі запит CQL поєднує такі шляхи та , щоб описати, як рухатися по дереву:

-   firstChild
-   lastChild
-   previous
-   next
-   parent

Например,`/firstChild/lastChild`будет перемещаться к последнему дочернему узлу первого дочернего узла.

##### Цикли

CQL може бути заданий цикл, наприклад, через дочірні елементи або дочірні елементи до певного вузла з використанням шляху `children`или`siblings`Например,`/firstChild/children` буде переміщатися всіма дочірніми елементами першого дочірнього вузла.

##### Підзапити

CQL можна проінструктувати, як переміщатися, використовуючи підзапит, такий як `[/firstChild]`Например,`/firstChild/children[/firstChild]` перейде до першого дочірнього вузла всіх вузлів першого дочірнього вузла.

##### Обмеження циклів

Під час циклу CQL може бути проінструктовано обмежувати пройдений шлях до вузлів певного типу. Наприклад, `/children(BlockQuote)` буде переміщатися до дочірніх елементів вузла, де типом є `BlockQuote`. Наступні типи розпізнаються (без урахування регістру):

-   BlockQuote
-   List
-   Item
-   CodeBlock
-   HtmlBlock
-   CustomBlock
-   Paragraph
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

Типи можуть використовуватись як об'єднання, наприклад, `/children(BlockQuote|List)` буде переміщатися до дочірніх елементів вузла, де типом є `BlockQuote`или`List`. Типи або об'єднання типів також можуть бути скасовані. Наприклад, `/children(~BlockQuote)` буде переміщатися до дочірніх елементів вузла, де тип не є `BlockQuote`, а`/children(~BlockQuote|Paragraph)`будет перемещаться к дочерним узлам, где тип не является`BlockQuote`или`Paragraph`

##### Обмеження шляхів

CQL можна доручити створити цикл для переміщення до вузла певного типу певним шляхом. Наприклад, `/firstChild(BlockQuote)` перейде до першого дочірнього вузла з типом `BlockQuote`. Зверніть увагу, що як і інші цикли, `children`и`siblings`, цей тип шляху може супроводжуватися лише підзапитом.

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

-   [CommonMark\\CQL::\_\_construct](commonmark-cql.construct.md) \- Конструктор класу CQL
-   [CommonMark\\CQL::\_\_invoke](commonmark-cql.invoke.md) \- Виконання CQL

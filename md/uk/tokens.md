---
navigation:
  - types.comparisons.md: « Таблица сравнения типов в PHP
  - userlandnaming.md: Руководство по именованию »
  - index.md: PHP Manual
  - appendices.md: Appendices
title: Список тегів (tokens) парсера
---
# Список тегів (tokens) парсера

Різні частини PHP внутрішньо представлені токенами. Фрагмент коду, що містить неприпустиму послідовність токенів, може призвести до таких помилок, як `Parse error: syntax error, unexpected token "==", expecting "(" in script.php on line 10."`де токен `==` внутрішньо представлений як **`T_IS_EQUAL`**

У наведеній нижче таблиці перераховані всі токени. Вони також доступні як константи PHP.

> **Зауваження** **Використання T констант**
> 
> Значення T константи автоматично генеруються на основі базової інфраструктури синтаксичного аналізатора PHP. Це означає, що конкретне значення мітки може змінюватись між двома версіями PHP. Це означає, що ваш код ніколи не повинен безпосередньо покладатися на вихідні значення T, взяті з версії PHP X.Y.Z, щоб забезпечити деяку сумісність між кількома версіями PHP.
> 
> Щоб використовувати T константи у кількох версіях PHP, невизначені константи можуть бути визначені користувачем (з використанням великих чисел, таких як `10000`) з відповідною стратегією, яка працюватиме як з версіями PHP, так і зі значеннями T
> 
> ```php
> <?php
> // До PHP 7.4.0 значение T_FN не определено.
> defined('T_FN') || define('T_FN', 10001);
> ```

**Мітки**

| Метка | Синтаксис | Ссылка |
| --- | --- | --- |
| **`T_ABSTRACT`** | abstract | [Абстрактні класи](language.oop5.abstract.md) |
| **`T_AMPERSAND_FOLLOWED_BY_VAR_OR_VARARG`** | & | [Оголошення типів](language.types.declarations.md) (доступно, починаючи з PHP 8.1.0) |
| **`T_AMPERSAND_NOT_FOLLOWED_BY_VAR_OR_VARARG`** | & | [Оголошення типів](language.types.declarations.md) (доступно, починаючи з PHP 8.1.0) |
| **`T_AND_EQUAL`** | &= | [оператори присвоєння](language.operators.assignment.md) |
| **`T_ARRAY`** | array() | [array()](function.array.md) [синтаксис Масива](language.types.array.md#language.types.array.syntax) |
| **`T_ARRAY_CAST`** | (array) | [приведение типа](language.types.type-juggling.md#language.types.typecasting) |
| **`T_AS`** | ас | [foreach](control-structures.foreach.md) |
| **`T_ATTRIBUTE`** |  | [attributes](language.attributes.md) (доступно з PHP 8.0.0) |
| **`T_BAD_CHARACTER`** |  | все, що нижче ASCII 32 виключаючи t (0x09), n (0x0a) та r (0x0d) (доступно з PHP 7.4.0) |
| **`T_BOOLEAN_AND`** | && | [логічні оператори](language.operators.logical.md) |
| **`T_BOOLEAN_OR`** |  |  |
| **`T_BOOL_CAST`** | (bool) або (boolean) | [приведение типа](language.types.type-juggling.md#language.types.typecasting) |
| **`T_BREAK`** | break | [break](control-structures.break.md) |
| **`T_CALLABLE`** | callable | [callable](language.types.callable.md) |
| **`T_CASE`** | case | [switch](control-structures.switch.md) |
| **`T_CATCH`** | catch | [Исключения](language.exceptions.md) |
| **`T_CLASS`** | class | [класи та об'єкти](language.oop5.md) |
| **`T_CLASS_C`** | CLASS | [магічні константи](language.constants.predefined.md) |
| **`T_CLONE`** | clone | [класи та об'єкти](language.oop5.md) |
| **`T_CLOSE_TAG`** | ?> або %> | [PHP-код внутри HTML](language.basic-syntax.phpmode.md) |
| **`T_COALESCE`** |  | [оператори порівняння](language.operators.comparison.md#language.operators.comparison.coalesce) |
| **`T_COALESCE_EQUAL`** |  | [оператори присвоєння](language.operators.assignment.md) (доступно з PHP 7.4.0) |
| **`T_COMMENT`** | // або #, та / | [комментарии](language.basic-syntax.comments.md) |
| **`T_CONCAT_EQUAL`** |  | [оператори присвоєння](language.operators.assignment.md) |
| **`T_CONST`** | const | [константи класу](language.constants.md) |
| **`T_CONSTANT_ENCAPSED_STRING`** | "foo" або 'bar' | [рядковий синтаксис](language.types.string.md#language.types.string.syntax) |
| **`T_CONTINUE`** | continue | [continue](control-structures.continue.md) |
| **`T_CURLY_OPEN`** |  | [змінні всередині рядки](language.types.string.md#language.types.string.parsing.complex) |
| **`T_DEC`** |  | [оператори інкременту декременту](language.operators.increment.md) |
| **`T_DECLARE`** | declare | [declare](control-structures.declare.md) |
| **`T_DEFAULT`** | default | [switch](control-structures.switch.md) |
| **`T_DIR`** | DIR | [магічні константи](language.constants.predefined.md) |
| **`T_DIV_EQUAL`** |  | [оператори присвоєння](language.operators.assignment.md) |
| **`T_DNUMBER`** | 0.12 і т.д. | [числа з плаваючою точкою](language.types.float.md) |
| **`T_DO`** | до | [do..while](control-structures.do.while.md) |
| **`T_DOC_COMMENT`** |  | [PHPDoc-комментарии](language.basic-syntax.comments.md) |
| **`T_DOLLAR_OPEN_CURLY_BRACES`** |  | [змінна всередині рядка](language.types.string.md#language.types.string.parsing.complex) |
| **`T_DOUBLE_ARROW`** | \> | [синтаксис масивів](language.types.array.md#language.types.array.syntax) |
| **`T_DOUBLE_CAST`** | (real), (double) або (float) | [приведение типов](language.types.type-juggling.md#language.types.typecasting) |
| **`T_DOUBLE_COLON`** |  | Дивіться нижче **`T_PAAMAYIM_NEKUDOTAYIM`** |
| **`T_ECHO`** | echo | [echo](function.echo.md) |
| **`T_ELLIPSIS`** |  | [аргументи функції](functions.arguments.md#functions.variable-arg-list) |
| **`T_ELSE`** | else | [else](control-structures.else.md) |
| **`T_ELSEIF`** | elseif | [elseif](control-structures.elseif.md) |
| **`T_EMPTY`** | empty | [empty()](function.empty.md) |
| **`T_ENCAPSED_AND_WHITESPACE`** | "$a" | [константна частина рядка зі змінними](language.types.string.md#language.types.string.parsing) |
| **`T_ENDDECLARE`** | enddeclare | [declare](control-structures.declare.md) [альтернативний синтаксис](control-structures.alternative-syntax.md) |
| **`T_ENDFOR`** | endfor | [for](control-structures.for.md) [альтернативний синтаксис](control-structures.alternative-syntax.md) |
| **`T_ENDFOREACH`** | endforeach | [foreach](control-structures.foreach.md) [альтернативний синтаксис](control-structures.alternative-syntax.md) |
| **`T_ENDIF`** | endif | [іф](control-structures.if.md) [альтернативний синтаксис](control-structures.alternative-syntax.md) |
| **`T_ENDSWITCH`** | endswitch | [switch](control-structures.switch.md) [альтернативний синтаксис](control-structures.alternative-syntax.md) |
| **`T_ENDWHILE`** | endwhile | [while](control-structures.while.md) [альтернативний синтаксис](control-structures.alternative-syntax.md) |
| **`T_ENUM`** | enum | [Перечисления](language.types.enumerations.md) (доступно, починаючи з PHP 8.1.0) |
| **`T_END_HEREDOC`** |  | [синтаксис heredoc](language.types.string.md#language.types.string.syntax.heredoc) |
| **`T_EVAL`** | eval() | [eval()](function.eval.md) |
| **`T_EXIT`** | exit або die | [exit()](function.exit.md) [die()](function.die.md) |
| **`T_EXTENDS`** | extends | [extends](language.oop5.basic.md#language.oop5.basic.extends) [класи та об'єкти](language.oop5.md) |
| **`T_FILE`** | FILE | [магічні константи](language.constants.predefined.md) |
| **`T_FINAL`** | final | [Ключевое слово final](language.oop5.final.md) |
| **`T_FINALLY`** | finally | [Исключения](language.exceptions.md) |
| **`T_FN`** | фн | [стрілочні функції](functions.arrow.md) (доступно з PHP 7.4.0) |
| **`T_FOR`** | for | [for](control-structures.for.md) |
| **`T_FOREACH`** | foreach | [foreach](control-structures.foreach.md) |
| **`T_FUNCTION`** | function | [функції](language.functions.md) |
| **`T_FUNC_C`** | FUNCTION | [магічні константи](language.constants.predefined.md) |
| **`T_GLOBAL`** | global | [область видимості змінної](language.variables.scope.md) |
| **`T_GOTO`** | goto | [goto](control-structures.goto.md) |
| **`T_HALT_COMPILER`** | haltcompiler() | [haltcompiler](function.halt-compiler.md) |
| **`T_IF`** | іф | [іф](control-structures.if.md) |
| **`T_IMPLEMENTS`** | implements | [Інтерфейси об'єктів](language.oop5.interfaces.md) |
| **`T_INC`** |  | [оператори інкременту декременту](language.operators.increment.md) |
| **`T_INCLUDE`** | include() | [include](function.include.md) |
| **`T_INCLUDE_ONCE`** | includeonce() | [includeonce](function.include-once.md) |
| **`T_INLINE_HTML`** |  | [текст вне PHP](language.basic-syntax.phpmode.md) |
| **`T_INSTANCEOF`** | instanceof | [оператори типу](language.operators.type.md) |
| **`T_INSTEADOF`** | insteadof | [Трейти](language.oop5.traits.md) |
| **`T_INTERFACE`** | interface | [Інтерфейси об'єктів](language.oop5.interfaces.md) |
| **`T_INT_CAST`** | (int) або (integer) | [приведение типов](language.types.type-juggling.md#language.types.typecasting) |
| **`T_ISSET`** | isset() | [isset()](function.isset.md) |
| **`T_IS_EQUAL`** |  | [оператори порівняння](language.operators.comparison.md) |
| **`T_IS_GREATER_OR_EQUAL`** | \> | [оператори порівняння](language.operators.comparison.md) |
| **`T_IS_IDENTICAL`** |  | [оператори порівняння](language.operators.comparison.md) |
| **`T_IS_NOT_EQUAL`** | != або <> | [оператори порівняння](language.operators.comparison.md) |
| **`T_IS_NOT_IDENTICAL`** |  | [оператори порівняння](language.operators.comparison.md) |
| **`T_IS_SMALLER_OR_EQUAL`** | <= | [оператори порівняння](language.operators.comparison.md) |
| **`T_LINE`** | LINE | [магічні константи](language.constants.predefined.md) |
| **`T_LIST`** | list() | [list()](function.list.md) |
| **`T_LNUMBER`** | 123, 012, 0x1ac і т.д. | [цілі числа](language.types.integer.md) |
| **`T_LOGICAL_AND`** | and | [логічні оператори](language.operators.logical.md) |
| **`T_LOGICAL_OR`** | ор | [логічні оператори](language.operators.logical.md) |
| **`T_LOGICAL_XOR`** | xor | [логічні оператори](language.operators.logical.md) |
| **`T_MATCH`** | match | [match](control-structures.match.md) (доступно з PHP 8.0.0) |
| **`T_METHOD_C`** | METHOD | [магічні константи](language.constants.predefined.md) |
| **`T_MINUS_EQUAL`** |  | [оператори присвоєння](language.operators.assignment.md) |
| **`T_MOD_EQUAL`** |  | [оператори присвоєння](language.operators.assignment.md) |
| **`T_MUL_EQUAL`** |  | [оператори присвоєння](language.operators.assignment.md) |
| **`T_NAMESPACE`** | namespace | [пространства имён](language.namespaces.md) |
| **`T_NAME_FULLY_QUALIFIED`** | AppNamespace | [пространства имён](language.namespaces.md) (доступно, починаючи з PHP 8.0.0) |
| **`T_NAME_QUALIFIED`** | AppNamespace | [пространства имён](language.namespaces.md) (доступно, починаючи з PHP 8.0.0) |
| **`T_NAME_RELATIVE`** | namespaceNamespace | [пространства имён](language.namespaces.md) (доступно, починаючи з PHP 8.0.0) |
| **`T_NEW`** | new | [класи та об'єкти](language.oop5.md) |
| **`T_NS_C`** | NAMESPACE | [пространства имён](language.namespaces.md) |
| **`T_NS_SEPARATOR`** |  | [пространства имён](language.namespaces.md) |
| **`T_NUM_STRING`** | "$a" | [цифровий індекс масиву всередині рядка](language.types.string.md#language.types.string.parsing) |
| **`T_OBJECT_CAST`** | (object) | [приведение типов](language.types.type-juggling.md#language.types.typecasting) |
| **`T_OBJECT_OPERATOR`** | \> | [класи та об'єкти](language.oop5.md) |
| **`T_NULLSAFE_OBJECT_OPERATOR`** | ?-> | [класи та об'єкти](language.oop5.md) |
| **`T_OPEN_TAG`** |  | [PHP-код внутри HTML](language.basic-syntax.phpmode.md) |
| **`T_OPEN_TAG_WITH_ECHO`** |  | [PHP-код внутри HTML](language.basic-syntax.phpmode.md) |
| **`T_OR_EQUAL`** |  |  |
| **`T_PAAMAYIM_NEKUDOTAYIM`** |  | [](language.oop5.paamayim-nekudotayim.md). Також визначається як **`T_DOUBLE_COLON`** |
| **`T_PLUS_EQUAL`** |  | [оператори присвоєння](language.operators.assignment.md) |
| **`T_POW`** |  | [арифметичні оператори](language.operators.arithmetic.md) |
| **`T_POW_EQUAL`** |  | [оператори присвоєння](language.operators.assignment.md) |
| **`T_PRINT`** | print() | [print](function.print.md) |
| **`T_PRIVATE`** | private | [класи та об'єкти](language.oop5.md) |
| **`T_PROTECTED`** | protected | [класи та об'єкти](language.oop5.md) |
| **`T_PUBLIC`** | public | [класи та об'єкти](language.oop5.md) |
| **`T_READONLY`** | readonly | [класи та об'єкти](language.oop5.md) (доступно, починаючи з PHP 8.1.0) |
| **`T_REQUIRE`** | require() | [require](function.require.md) |
| **`T_REQUIRE_ONCE`** | requireonce() | [requireonce](function.require-once.md) |
| **`T_RETURN`** | return | [значення, що повертаються](functions.returning-values.md) |
| **`T_SL`** | << | [побітові оператори](language.operators.bitwise.md) |
| **`T_SL_EQUAL`** | <<= | [оператори присвоєння](language.operators.assignment.md) |
| **`T_SPACESHIP`** | <=> | [Оператори порівняння](language.operators.comparison.md) |
| **`T_SR`** | \>> | [побітові оператори](language.operators.bitwise.md) |
| **`T_SR_EQUAL`** | \>>= | [оператори присвоєння](language.operators.assignment.md) |
| **`T_START_HEREDOC`** | <<< | [синтаксис heredoc](language.types.string.md#language.types.string.syntax.heredoc) |
| **`T_STATIC`** | static | [область видимості змінної](language.variables.scope.md) |
| **`T_STRING`** | parent, self тощо. | ідентифікатори, наприклад, ключові слова на кшталт `parent` і `self`, сюди підходять імена функцій, класів та інших. Дивіться також **`T_CONSTANT_ENCAPSED_STRING`** |
| **`T_STRING_CAST`** | (string) | [приведение типов](language.types.type-juggling.md#language.types.typecasting) |
| **`T_STRING_VARNAME`** | "${a | [змінні всередині рядки](language.types.string.md#language.types.string.parsing.complex) |
| **`T_SWITCH`** | switch | [switch](control-structures.switch.md) |
| **`T_THROW`** | throw | [Исключения](language.exceptions.md) |
| **`T_TRAIT`** | trait | [Трейти](language.oop5.traits.md) |
| **`T_TRAIT_C`** | TRAIT | TRAIT |
| **`T_TRY`** | try | [Исключения](language.exceptions.md) |
| **`T_UNSET`** | unset() | [unset()](function.unset.md) |
| **`T_UNSET_CAST`** | (unset) | [приведение типов](language.types.type-juggling.md#language.types.typecasting) |
| **`T_USE`** | use | [пространства имён](language.namespaces.md) |
| **`T_VAR`** | var | [класи та об'єкти](language.oop5.md) |
| **`T_VARIABLE`** | $foo | [змінні](language.variables.md) |
| **`T_WHILE`** | while | [while](control-structures.while.md) [do..while](control-structures.do.while.md) |
| **`T_WHITESPACE`** | т рн |  |
| **`T_XOR_EQUAL`** |  | [оператори присвоєння](language.operators.assignment.md) |
| **`T_YIELD`** | yield | [генератори](language.generators.syntax.md#control-structures.yield) |
| **`T_YIELD_FROM`** | yield from | [generators](language.generators.syntax.md#control-structures.yield.from) |

Дивіться також [tokenname()](function.token-name.md)

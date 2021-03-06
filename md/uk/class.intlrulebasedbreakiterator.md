- [« IntlBreakIterator::setText](intlbreakiterator.settext.md)
- [IntlRuleBasedBreakIterator::\_\_construct »](intlrulebasedbreakiterator.construct.md)

- [PHP Manual](index.md)
- [intl](book.intl.md)
- Клас IntlRuleBasedBreakIterator

# Клас IntlRuleBasedBreakIterator

(PHP 5 \>= 5.5.0, PHP 7, PHP 8)

## Вступ

Підклас [IntlBreakIterator](class.intlbreakiterator.md), який
реалізує ітератор переривань ICU, чия поведінка задано набором правил.
Це найчастіше використовуваний тип ітератора переривань.

Правила описані в розділі [» Керівництво користувача з аналізу кордонів ICU](http://userguide.icu-project.org/boundaryanalysis#TOC-RBBI-Rules).

## Огляд класів

class **IntlRuleBasedBreakIterator** extends
[IntlBreakIterator](class.intlbreakiterator.md) {

/\* Успадковані константи \*/

const int `IntlBreakIterator::DONE` = -1;

const int `IntlBreakIterator::WORD_NONE` = 0;

const int `IntlBreakIterator::WORD_NONE_LIMIT` = 100;

const int `IntlBreakIterator::WORD_NUMBER` = 100;

const int `IntlBreakIterator::WORD_NUMBER_LIMIT` = 200;

const int `IntlBreakIterator::WORD_LETTER` = 200;

const int `IntlBreakIterator::WORD_LETTER_LIMIT` = 300;

const int `IntlBreakIterator::WORD_KANA` = 300;

const int `IntlBreakIterator::WORD_KANA_LIMIT` = 400;

const int `IntlBreakIterator::WORD_IDEO` = 400;

const int `IntlBreakIterator::WORD_IDEO_LIMIT` = 500;

const int `IntlBreakIterator::LINE_SOFT` = 0;

const int `IntlBreakIterator::LINE_SOFT_LIMIT` = 100;

const int `IntlBreakIterator::LINE_HARD` = 100;

const int `IntlBreakIterator::LINE_HARD_LIMIT` = 200;

const int `IntlBreakIterator::SENTENCE_TERM` = 0;

const int `IntlBreakIterator::SENTENCE_TERM_LIMIT` = 100;

const int `IntlBreakIterator::SENTENCE_SEP` = 100;

const int `IntlBreakIterator::SENTENCE_SEP_LIMIT` = 200;

/\* Методи \*/

public [\_\_construct](intlrulebasedbreakiterator.construct.md)(string
`$rules`, bool `$compiled` = **`false`**)

public
[getBinaryRules](intlrulebasedbreakiterator.getbinaryrules.md)():
string\|false

public [getRules](intlrulebasedbreakiterator.getrules.md)():
string\|false

public [getRuleStatus](intlrulebasedbreakiterator.getrulestatus.md)():
int

public
[getRuleStatusVec](intlrulebasedbreakiterator.getrulestatusvec.md)():
array\|false

/\* Наслідувані методи \*/

public static
[IntlBreakIterator::createCharacterInstance](intlbreakiterator.createcharacterinstance.md)(?string
`$locale` = **`null`**):
?[IntlBreakIterator](class.intlbreakiterator.md)

public static
[IntlBreakIterator::createCodePointInstance](intlbreakiterator.createcodepointinstance.md)():
[IntlCodePointBreakIterator](class.intlcodepointbreakiterator.md)

public static
[IntlBreakIterator::createLineInstance](intlbreakiterator.createlineinstance.md)(?string
`$locale` = **`null`**):
?[IntlBreakIterator](class.intlbreakiterator.md)

public static
[IntlBreakIterator::createSentenceInstance](intlbreakiterator.createsentenceinstance.md)(?string
`$locale` = **`null`**):
?[IntlBreakIterator](class.intlbreakiterator.md)

public static
[IntlBreakIterator::createTitleInstance](intlbreakiterator.createtitleinstance.md)(?string
`$locale` = **`null`**):
?[IntlBreakIterator](class.intlbreakiterator.md)

public static
[IntlBreakIterator::createWordInstance](intlbreakiterator.createwordinstance.md)(?string
`$locale` = **`null`**):
?[IntlBreakIterator](class.intlbreakiterator.md)

public [IntlBreakIterator::current](intlbreakiterator.current.md)():
int

public [IntlBreakIterator::first](intlbreakiterator.first.md)(): int

public
[IntlBreakIterator::following](intlbreakiterator.following.md)(int
`$offset`): int

public
[IntlBreakIterator::getErrorCode](intlbreakiterator.geterrorcode.md)():
int

**intl_get_error_code**(): int

public
[IntlBreakIterator::getErrorMessage](intlbreakiterator.geterrormessage.md)():
string\|false

**intl_get_error_message**(): string

public
[IntlBreakIterator::getLocale](intlbreakiterator.getlocale.md)(int
`$type`): string

public
[IntlBreakIterator::getPartsIterator](intlbreakiterator.getpartsiterator.md)(string
`$type` = IntlPartsIterator::KEY_SEQUENTIAL):
[IntlPartsIterator](class.intlpartsiterator.md)

public [IntlBreakIterator::getText](intlbreakiterator.gettext.md)():
?string

public
[IntlBreakIterator::isBoundary](intlbreakiterator.isboundary.md)(int
`$offset`): bool

public [IntlBreakIterator::last](intlbreakiterator.last.md)(): int

public [IntlBreakIterator::next](intlbreakiterator.next.md)(?int
`$offset` = **`null`**): int

public
[IntlBreakIterator::preceding](intlbreakiterator.preceding.md)(int
`$offset`): int

public [IntlBreakIterator::previous](intlbreakiterator.previous.md)():
int

public
[IntlBreakIterator::setText](intlbreakiterator.settext.md)(string
`$text`): ?bool

}

## Зміст

- [IntlRuleBasedBreakIterator::\_\_construct](intlrulebasedbreakiterator.construct.md)
- Створює ітератор на основі набору правил
- [IntlRuleBasedBreakIterator::getBinaryRules](intlrulebasedbreakiterator.getbinaryrules.md)
— Отримати бінарні дані зі скомпілованих правил
- [IntlRuleBasedBreakIterator::getRules](intlrulebasedbreakiterator.getrules.md)
— Отримати набір правил, які використовувалися під час створення цього об'єкта
- [IntlRuleBasedBreakIterator::getRuleStatus](intlrulebasedbreakiterator.getrulestatus.md)
— Отримати найбільше значення статусу правил зупинки, яке визначило
поточну позицію зупинки
- [IntlRuleBasedBreakIterator::getRuleStatusVec](intlrulebasedbreakiterator.getrulestatusvec.md)
— отримати значення статусів із правил зупину, які визначили
поточну позицію зупинки

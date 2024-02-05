---
navigation:
  - function.idn-to-utf8.md: « idn\_to\_utf8
  - intlchar.charage.md: 'IntlChar::charAge »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: IntlChar
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar

(PHP 7, PHP 8)

## Вступ

**IntlChar** надає доступ до деяких утилітарних методів, які можна використовувати для доступу до інформації про символи Unicode.

Імена методів і констант, представлені тут, близькі до імен та методів бібліотеки ICU, що знаходиться нижче.

## Огляд класів

```classsynopsis

    
     class IntlChar
     {

    /* Константы */
    
     public
     const
     string
      UNICODE_VERSION;

    public
     const
     int
      CODEPOINT_MIN;

    public
     const
     int
      CODEPOINT_MAX;

    public
     const
     float
      NO_NUMERIC_VALUE;

    public
     const
     int
      PROPERTY_ALPHABETIC;

    public
     const
     int
      PROPERTY_BINARY_START;

    public
     const
     int
      PROPERTY_ASCII_HEX_DIGIT;

    public
     const
     int
      PROPERTY_BIDI_CONTROL;

    public
     const
     int
      PROPERTY_BIDI_MIRRORED;

    public
     const
     int
      PROPERTY_DASH;

    public
     const
     int
      PROPERTY_DEFAULT_IGNORABLE_CODE_POINT;

    public
     const
     int
      PROPERTY_DEPRECATED;

    public
     const
     int
      PROPERTY_DIACRITIC;

    public
     const
     int
      PROPERTY_EXTENDER;

    public
     const
     int
      PROPERTY_FULL_COMPOSITION_EXCLUSION;

    public
     const
     int
      PROPERTY_GRAPHEME_BASE;

    public
     const
     int
      PROPERTY_GRAPHEME_EXTEND;

    public
     const
     int
      PROPERTY_GRAPHEME_LINK;

    public
     const
     int
      PROPERTY_HEX_DIGIT;

    public
     const
     int
      PROPERTY_HYPHEN;

    public
     const
     int
      PROPERTY_ID_CONTINUE;

    public
     const
     int
      PROPERTY_ID_START;

    public
     const
     int
      PROPERTY_IDEOGRAPHIC;

    public
     const
     int
      PROPERTY_IDS_BINARY_OPERATOR;

    public
     const
     int
      PROPERTY_IDS_TRINARY_OPERATOR;

    public
     const
     int
      PROPERTY_JOIN_CONTROL;

    public
     const
     int
      PROPERTY_LOGICAL_ORDER_EXCEPTION;

    public
     const
     int
      PROPERTY_LOWERCASE;

    public
     const
     int
      PROPERTY_MATH;

    public
     const
     int
      PROPERTY_NONCHARACTER_CODE_POINT;

    public
     const
     int
      PROPERTY_QUOTATION_MARK;

    public
     const
     int
      PROPERTY_RADICAL;

    public
     const
     int
      PROPERTY_SOFT_DOTTED;

    public
     const
     int
      PROPERTY_TERMINAL_PUNCTUATION;

    public
     const
     int
      PROPERTY_UNIFIED_IDEOGRAPH;

    public
     const
     int
      PROPERTY_UPPERCASE;

    public
     const
     int
      PROPERTY_WHITE_SPACE;

    public
     const
     int
      PROPERTY_XID_CONTINUE;

    public
     const
     int
      PROPERTY_XID_START;

    public
     const
     int
      PROPERTY_CASE_SENSITIVE;

    public
     const
     int
      PROPERTY_S_TERM;

    public
     const
     int
      PROPERTY_VARIATION_SELECTOR;

    public
     const
     int
      PROPERTY_NFD_INERT;

    public
     const
     int
      PROPERTY_NFKD_INERT;

    public
     const
     int
      PROPERTY_NFC_INERT;

    public
     const
     int
      PROPERTY_NFKC_INERT;

    public
     const
     int
      PROPERTY_SEGMENT_STARTER;

    public
     const
     int
      PROPERTY_PATTERN_SYNTAX;

    public
     const
     int
      PROPERTY_PATTERN_WHITE_SPACE;

    public
     const
     int
      PROPERTY_POSIX_ALNUM;

    public
     const
     int
      PROPERTY_POSIX_BLANK;

    public
     const
     int
      PROPERTY_POSIX_GRAPH;

    public
     const
     int
      PROPERTY_POSIX_PRINT;

    public
     const
     int
      PROPERTY_POSIX_XDIGIT;

    public
     const
     int
      PROPERTY_CASED;

    public
     const
     int
      PROPERTY_CASE_IGNORABLE;

    public
     const
     int
      PROPERTY_CHANGES_WHEN_LOWERCASED;

    public
     const
     int
      PROPERTY_CHANGES_WHEN_UPPERCASED;

    public
     const
     int
      PROPERTY_CHANGES_WHEN_TITLECASED;

    public
     const
     int
      PROPERTY_CHANGES_WHEN_CASEFOLDED;

    public
     const
     int
      PROPERTY_CHANGES_WHEN_CASEMAPPED;

    public
     const
     int
      PROPERTY_CHANGES_WHEN_NFKC_CASEFOLDED;

    public
     const
     int
      PROPERTY_BINARY_LIMIT;

    public
     const
     int
      PROPERTY_BIDI_CLASS;

    public
     const
     int
      PROPERTY_INT_START;

    public
     const
     int
      PROPERTY_BLOCK;

    public
     const
     int
      PROPERTY_CANONICAL_COMBINING_CLASS;

    public
     const
     int
      PROPERTY_DECOMPOSITION_TYPE;

    public
     const
     int
      PROPERTY_EAST_ASIAN_WIDTH;

    public
     const
     int
      PROPERTY_GENERAL_CATEGORY;

    public
     const
     int
      PROPERTY_JOINING_GROUP;

    public
     const
     int
      PROPERTY_JOINING_TYPE;

    public
     const
     int
      PROPERTY_LINE_BREAK;

    public
     const
     int
      PROPERTY_NUMERIC_TYPE;

    public
     const
     int
      PROPERTY_SCRIPT;

    public
     const
     int
      PROPERTY_HANGUL_SYLLABLE_TYPE;

    public
     const
     int
      PROPERTY_NFD_QUICK_CHECK;

    public
     const
     int
      PROPERTY_NFKD_QUICK_CHECK;

    public
     const
     int
      PROPERTY_NFC_QUICK_CHECK;

    public
     const
     int
      PROPERTY_NFKC_QUICK_CHECK;

    public
     const
     int
      PROPERTY_LEAD_CANONICAL_COMBINING_CLASS;

    public
     const
     int
      PROPERTY_TRAIL_CANONICAL_COMBINING_CLASS;

    public
     const
     int
      PROPERTY_GRAPHEME_CLUSTER_BREAK;

    public
     const
     int
      PROPERTY_SENTENCE_BREAK;

    public
     const
     int
      PROPERTY_WORD_BREAK;

    public
     const
     int
      PROPERTY_BIDI_PAIRED_BRACKET_TYPE;

    public
     const
     int
      PROPERTY_INT_LIMIT;

    public
     const
     int
      PROPERTY_GENERAL_CATEGORY_MASK;

    public
     const
     int
      PROPERTY_MASK_START;

    public
     const
     int
      PROPERTY_MASK_LIMIT;

    public
     const
     int
      PROPERTY_NUMERIC_VALUE;

    public
     const
     int
      PROPERTY_DOUBLE_START;

    public
     const
     int
      PROPERTY_DOUBLE_LIMIT;

    public
     const
     int
      PROPERTY_AGE;

    public
     const
     int
      PROPERTY_STRING_START;

    public
     const
     int
      PROPERTY_BIDI_MIRRORING_GLYPH;

    public
     const
     int
      PROPERTY_CASE_FOLDING;

    public
     const
     int
      PROPERTY_ISO_COMMENT;

    public
     const
     int
      PROPERTY_LOWERCASE_MAPPING;

    public
     const
     int
      PROPERTY_NAME;

    public
     const
     int
      PROPERTY_SIMPLE_CASE_FOLDING;

    public
     const
     int
      PROPERTY_SIMPLE_LOWERCASE_MAPPING;

    public
     const
     int
      PROPERTY_SIMPLE_TITLECASE_MAPPING;

    public
     const
     int
      PROPERTY_SIMPLE_UPPERCASE_MAPPING;

    public
     const
     int
      PROPERTY_TITLECASE_MAPPING;

    public
     const
     int
      PROPERTY_UNICODE_1_NAME;

    public
     const
     int
      PROPERTY_UPPERCASE_MAPPING;

    public
     const
     int
      PROPERTY_BIDI_PAIRED_BRACKET;

    public
     const
     int
      PROPERTY_STRING_LIMIT;

    public
     const
     int
      PROPERTY_SCRIPT_EXTENSIONS;

    public
     const
     int
      PROPERTY_OTHER_PROPERTY_START;

    public
     const
     int
      PROPERTY_OTHER_PROPERTY_LIMIT;

    public
     const
     int
      PROPERTY_INVALID_CODE;

    public
     const
     int
      CHAR_CATEGORY_UNASSIGNED;

    public
     const
     int
      CHAR_CATEGORY_GENERAL_OTHER_TYPES;

    public
     const
     int
      CHAR_CATEGORY_UPPERCASE_LETTER;

    public
     const
     int
      CHAR_CATEGORY_LOWERCASE_LETTER;

    public
     const
     int
      CHAR_CATEGORY_TITLECASE_LETTER;

    public
     const
     int
      CHAR_CATEGORY_MODIFIER_LETTER;

    public
     const
     int
      CHAR_CATEGORY_OTHER_LETTER;

    public
     const
     int
      CHAR_CATEGORY_NON_SPACING_MARK;

    public
     const
     int
      CHAR_CATEGORY_ENCLOSING_MARK;

    public
     const
     int
      CHAR_CATEGORY_COMBINING_SPACING_MARK;

    public
     const
     int
      CHAR_CATEGORY_DECIMAL_DIGIT_NUMBER;

    public
     const
     int
      CHAR_CATEGORY_LETTER_NUMBER;

    public
     const
     int
      CHAR_CATEGORY_OTHER_NUMBER;

    public
     const
     int
      CHAR_CATEGORY_SPACE_SEPARATOR;

    public
     const
     int
      CHAR_CATEGORY_LINE_SEPARATOR;

    public
     const
     int
      CHAR_CATEGORY_PARAGRAPH_SEPARATOR;

    public
     const
     int
      CHAR_CATEGORY_CONTROL_CHAR;

    public
     const
     int
      CHAR_CATEGORY_FORMAT_CHAR;

    public
     const
     int
      CHAR_CATEGORY_PRIVATE_USE_CHAR;

    public
     const
     int
      CHAR_CATEGORY_SURROGATE;

    public
     const
     int
      CHAR_CATEGORY_DASH_PUNCTUATION;

    public
     const
     int
      CHAR_CATEGORY_START_PUNCTUATION;

    public
     const
     int
      CHAR_CATEGORY_END_PUNCTUATION;

    public
     const
     int
      CHAR_CATEGORY_CONNECTOR_PUNCTUATION;

    public
     const
     int
      CHAR_CATEGORY_OTHER_PUNCTUATION;

    public
     const
     int
      CHAR_CATEGORY_MATH_SYMBOL;

    public
     const
     int
      CHAR_CATEGORY_CURRENCY_SYMBOL;

    public
     const
     int
      CHAR_CATEGORY_MODIFIER_SYMBOL;

    public
     const
     int
      CHAR_CATEGORY_OTHER_SYMBOL;

    public
     const
     int
      CHAR_CATEGORY_INITIAL_PUNCTUATION;

    public
     const
     int
      CHAR_CATEGORY_FINAL_PUNCTUATION;

    public
     const
     int
      CHAR_CATEGORY_CHAR_CATEGORY_COUNT;

    public
     const
     int
      CHAR_DIRECTION_LEFT_TO_RIGHT;

    public
     const
     int
      CHAR_DIRECTION_RIGHT_TO_LEFT;

    public
     const
     int
      CHAR_DIRECTION_EUROPEAN_NUMBER;

    public
     const
     int
      CHAR_DIRECTION_EUROPEAN_NUMBER_SEPARATOR;

    public
     const
     int
      CHAR_DIRECTION_EUROPEAN_NUMBER_TERMINATOR;

    public
     const
     int
      CHAR_DIRECTION_ARABIC_NUMBER;

    public
     const
     int
      CHAR_DIRECTION_COMMON_NUMBER_SEPARATOR;

    public
     const
     int
      CHAR_DIRECTION_BLOCK_SEPARATOR;

    public
     const
     int
      CHAR_DIRECTION_SEGMENT_SEPARATOR;

    public
     const
     int
      CHAR_DIRECTION_WHITE_SPACE_NEUTRAL;

    public
     const
     int
      CHAR_DIRECTION_OTHER_NEUTRAL;

    public
     const
     int
      CHAR_DIRECTION_LEFT_TO_RIGHT_EMBEDDING;

    public
     const
     int
      CHAR_DIRECTION_LEFT_TO_RIGHT_OVERRIDE;

    public
     const
     int
      CHAR_DIRECTION_RIGHT_TO_LEFT_ARABIC;

    public
     const
     int
      CHAR_DIRECTION_RIGHT_TO_LEFT_EMBEDDING;

    public
     const
     int
      CHAR_DIRECTION_RIGHT_TO_LEFT_OVERRIDE;

    public
     const
     int
      CHAR_DIRECTION_POP_DIRECTIONAL_FORMAT;

    public
     const
     int
      CHAR_DIRECTION_DIR_NON_SPACING_MARK;

    public
     const
     int
      CHAR_DIRECTION_BOUNDARY_NEUTRAL;

    public
     const
     int
      CHAR_DIRECTION_FIRST_STRONG_ISOLATE;

    public
     const
     int
      CHAR_DIRECTION_LEFT_TO_RIGHT_ISOLATE;

    public
     const
     int
      CHAR_DIRECTION_RIGHT_TO_LEFT_ISOLATE;

    public
     const
     int
      CHAR_DIRECTION_POP_DIRECTIONAL_ISOLATE;

    public
     const
     int
      CHAR_DIRECTION_CHAR_DIRECTION_COUNT;

    public
     const
     int
      BLOCK_CODE_NO_BLOCK;

    public
     const
     int
      BLOCK_CODE_BASIC_LATIN;

    public
     const
     int
      BLOCK_CODE_LATIN_1_SUPPLEMENT;

    public
     const
     int
      BLOCK_CODE_LATIN_EXTENDED_A;

    public
     const
     int
      BLOCK_CODE_LATIN_EXTENDED_B;

    public
     const
     int
      BLOCK_CODE_IPA_EXTENSIONS;

    public
     const
     int
      BLOCK_CODE_SPACING_MODIFIER_LETTERS;

    public
     const
     int
      BLOCK_CODE_COMBINING_DIACRITICAL_MARKS;

    public
     const
     int
      BLOCK_CODE_GREEK;

    public
     const
     int
      BLOCK_CODE_CYRILLIC;

    public
     const
     int
      BLOCK_CODE_ARMENIAN;

    public
     const
     int
      BLOCK_CODE_HEBREW;

    public
     const
     int
      BLOCK_CODE_ARABIC;

    public
     const
     int
      BLOCK_CODE_SYRIAC;

    public
     const
     int
      BLOCK_CODE_THAANA;

    public
     const
     int
      BLOCK_CODE_DEVANAGARI;

    public
     const
     int
      BLOCK_CODE_BENGALI;

    public
     const
     int
      BLOCK_CODE_GURMUKHI;

    public
     const
     int
      BLOCK_CODE_GUJARATI;

    public
     const
     int
      BLOCK_CODE_ORIYA;

    public
     const
     int
      BLOCK_CODE_TAMIL;

    public
     const
     int
      BLOCK_CODE_TELUGU;

    public
     const
     int
      BLOCK_CODE_KANNADA;

    public
     const
     int
      BLOCK_CODE_MALAYALAM;

    public
     const
     int
      BLOCK_CODE_SINHALA;

    public
     const
     int
      BLOCK_CODE_THAI;

    public
     const
     int
      BLOCK_CODE_LAO;

    public
     const
     int
      BLOCK_CODE_TIBETAN;

    public
     const
     int
      BLOCK_CODE_MYANMAR;

    public
     const
     int
      BLOCK_CODE_GEORGIAN;

    public
     const
     int
      BLOCK_CODE_HANGUL_JAMO;

    public
     const
     int
      BLOCK_CODE_ETHIOPIC;

    public
     const
     int
      BLOCK_CODE_CHEROKEE;

    public
     const
     int
      BLOCK_CODE_UNIFIED_CANADIAN_ABORIGINAL_SYLLABICS;

    public
     const
     int
      BLOCK_CODE_OGHAM;

    public
     const
     int
      BLOCK_CODE_RUNIC;

    public
     const
     int
      BLOCK_CODE_KHMER;

    public
     const
     int
      BLOCK_CODE_MONGOLIAN;

    public
     const
     int
      BLOCK_CODE_LATIN_EXTENDED_ADDITIONAL;

    public
     const
     int
      BLOCK_CODE_GREEK_EXTENDED;

    public
     const
     int
      BLOCK_CODE_GENERAL_PUNCTUATION;

    public
     const
     int
      BLOCK_CODE_SUPERSCRIPTS_AND_SUBSCRIPTS;

    public
     const
     int
      BLOCK_CODE_CURRENCY_SYMBOLS;

    public
     const
     int
      BLOCK_CODE_COMBINING_MARKS_FOR_SYMBOLS;

    public
     const
     int
      BLOCK_CODE_LETTERLIKE_SYMBOLS;

    public
     const
     int
      BLOCK_CODE_NUMBER_FORMS;

    public
     const
     int
      BLOCK_CODE_ARROWS;

    public
     const
     int
      BLOCK_CODE_MATHEMATICAL_OPERATORS;

    public
     const
     int
      BLOCK_CODE_MISCELLANEOUS_TECHNICAL;

    public
     const
     int
      BLOCK_CODE_CONTROL_PICTURES;

    public
     const
     int
      BLOCK_CODE_OPTICAL_CHARACTER_RECOGNITION;

    public
     const
     int
      BLOCK_CODE_ENCLOSED_ALPHANUMERICS;

    public
     const
     int
      BLOCK_CODE_BOX_DRAWING;

    public
     const
     int
      BLOCK_CODE_BLOCK_ELEMENTS;

    public
     const
     int
      BLOCK_CODE_GEOMETRIC_SHAPES;

    public
     const
     int
      BLOCK_CODE_MISCELLANEOUS_SYMBOLS;

    public
     const
     int
      BLOCK_CODE_DINGBATS;

    public
     const
     int
      BLOCK_CODE_BRAILLE_PATTERNS;

    public
     const
     int
      BLOCK_CODE_CJK_RADICALS_SUPPLEMENT;

    public
     const
     int
      BLOCK_CODE_KANGXI_RADICALS;

    public
     const
     int
      BLOCK_CODE_IDEOGRAPHIC_DESCRIPTION_CHARACTERS;

    public
     const
     int
      BLOCK_CODE_CJK_SYMBOLS_AND_PUNCTUATION;

    public
     const
     int
      BLOCK_CODE_HIRAGANA;

    public
     const
     int
      BLOCK_CODE_KATAKANA;

    public
     const
     int
      BLOCK_CODE_BOPOMOFO;

    public
     const
     int
      BLOCK_CODE_HANGUL_COMPATIBILITY_JAMO;

    public
     const
     int
      BLOCK_CODE_KANBUN;

    public
     const
     int
      BLOCK_CODE_BOPOMOFO_EXTENDED;

    public
     const
     int
      BLOCK_CODE_ENCLOSED_CJK_LETTERS_AND_MONTHS;

    public
     const
     int
      BLOCK_CODE_CJK_COMPATIBILITY;

    public
     const
     int
      BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_A;

    public
     const
     int
      BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS;

    public
     const
     int
      BLOCK_CODE_YI_SYLLABLES;

    public
     const
     int
      BLOCK_CODE_YI_RADICALS;

    public
     const
     int
      BLOCK_CODE_HANGUL_SYLLABLES;

    public
     const
     int
      BLOCK_CODE_HIGH_SURROGATES;

    public
     const
     int
      BLOCK_CODE_HIGH_PRIVATE_USE_SURROGATES;

    public
     const
     int
      BLOCK_CODE_LOW_SURROGATES;

    public
     const
     int
      BLOCK_CODE_PRIVATE_USE_AREA;

    public
     const
     int
      BLOCK_CODE_PRIVATE_USE;

    public
     const
     int
      BLOCK_CODE_CJK_COMPATIBILITY_IDEOGRAPHS;

    public
     const
     int
      BLOCK_CODE_ALPHABETIC_PRESENTATION_FORMS;

    public
     const
     int
      BLOCK_CODE_ARABIC_PRESENTATION_FORMS_A;

    public
     const
     int
      BLOCK_CODE_COMBINING_HALF_MARKS;

    public
     const
     int
      BLOCK_CODE_CJK_COMPATIBILITY_FORMS;

    public
     const
     int
      BLOCK_CODE_SMALL_FORM_VARIANTS;

    public
     const
     int
      BLOCK_CODE_ARABIC_PRESENTATION_FORMS_B;

    public
     const
     int
      BLOCK_CODE_SPECIALS;

    public
     const
     int
      BLOCK_CODE_HALFWIDTH_AND_FULLWIDTH_FORMS;

    public
     const
     int
      BLOCK_CODE_OLD_ITALIC;

    public
     const
     int
      BLOCK_CODE_GOTHIC;

    public
     const
     int
      BLOCK_CODE_DESERET;

    public
     const
     int
      BLOCK_CODE_BYZANTINE_MUSICAL_SYMBOLS;

    public
     const
     int
      BLOCK_CODE_MUSICAL_SYMBOLS;

    public
     const
     int
      BLOCK_CODE_MATHEMATICAL_ALPHANUMERIC_SYMBOLS;

    public
     const
     int
      BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_B;

    public
     const
     int
      BLOCK_CODE_CJK_COMPATIBILITY_IDEOGRAPHS_SUPPLEMENT;

    public
     const
     int
      BLOCK_CODE_TAGS;

    public
     const
     int
      BLOCK_CODE_CYRILLIC_SUPPLEMENT;

    public
     const
     int
      BLOCK_CODE_CYRILLIC_SUPPLEMENTARY;

    public
     const
     int
      BLOCK_CODE_TAGALOG;

    public
     const
     int
      BLOCK_CODE_HANUNOO;

    public
     const
     int
      BLOCK_CODE_BUHID;

    public
     const
     int
      BLOCK_CODE_TAGBANWA;

    public
     const
     int
      BLOCK_CODE_MISCELLANEOUS_MATHEMATICAL_SYMBOLS_A;

    public
     const
     int
      BLOCK_CODE_SUPPLEMENTAL_ARROWS_A;

    public
     const
     int
      BLOCK_CODE_SUPPLEMENTAL_ARROWS_B;

    public
     const
     int
      BLOCK_CODE_MISCELLANEOUS_MATHEMATICAL_SYMBOLS_B;

    public
     const
     int
      BLOCK_CODE_SUPPLEMENTAL_MATHEMATICAL_OPERATORS;

    public
     const
     int
      BLOCK_CODE_KATAKANA_PHONETIC_EXTENSIONS;

    public
     const
     int
      BLOCK_CODE_VARIATION_SELECTORS;

    public
     const
     int
      BLOCK_CODE_SUPPLEMENTARY_PRIVATE_USE_AREA_A;

    public
     const
     int
      BLOCK_CODE_SUPPLEMENTARY_PRIVATE_USE_AREA_B;

    public
     const
     int
      BLOCK_CODE_LIMBU;

    public
     const
     int
      BLOCK_CODE_TAI_LE;

    public
     const
     int
      BLOCK_CODE_KHMER_SYMBOLS;

    public
     const
     int
      BLOCK_CODE_PHONETIC_EXTENSIONS;

    public
     const
     int
      BLOCK_CODE_MISCELLANEOUS_SYMBOLS_AND_ARROWS;

    public
     const
     int
      BLOCK_CODE_YIJING_HEXAGRAM_SYMBOLS;

    public
     const
     int
      BLOCK_CODE_LINEAR_B_SYLLABARY;

    public
     const
     int
      BLOCK_CODE_LINEAR_B_IDEOGRAMS;

    public
     const
     int
      BLOCK_CODE_AEGEAN_NUMBERS;

    public
     const
     int
      BLOCK_CODE_UGARITIC;

    public
     const
     int
      BLOCK_CODE_SHAVIAN;

    public
     const
     int
      BLOCK_CODE_OSMANYA;

    public
     const
     int
      BLOCK_CODE_CYPRIOT_SYLLABARY;

    public
     const
     int
      BLOCK_CODE_TAI_XUAN_JING_SYMBOLS;

    public
     const
     int
      BLOCK_CODE_VARIATION_SELECTORS_SUPPLEMENT;

    public
     const
     int
      BLOCK_CODE_ANCIENT_GREEK_MUSICAL_NOTATION;

    public
     const
     int
      BLOCK_CODE_ANCIENT_GREEK_NUMBERS;

    public
     const
     int
      BLOCK_CODE_ARABIC_SUPPLEMENT;

    public
     const
     int
      BLOCK_CODE_BUGINESE;

    public
     const
     int
      BLOCK_CODE_CJK_STROKES;

    public
     const
     int
      BLOCK_CODE_COMBINING_DIACRITICAL_MARKS_SUPPLEMENT;

    public
     const
     int
      BLOCK_CODE_COPTIC;

    public
     const
     int
      BLOCK_CODE_ETHIOPIC_EXTENDED;

    public
     const
     int
      BLOCK_CODE_ETHIOPIC_SUPPLEMENT;

    public
     const
     int
      BLOCK_CODE_GEORGIAN_SUPPLEMENT;

    public
     const
     int
      BLOCK_CODE_GLAGOLITIC;

    public
     const
     int
      BLOCK_CODE_KHAROSHTHI;

    public
     const
     int
      BLOCK_CODE_MODIFIER_TONE_LETTERS;

    public
     const
     int
      BLOCK_CODE_NEW_TAI_LUE;

    public
     const
     int
      BLOCK_CODE_OLD_PERSIAN;

    public
     const
     int
      BLOCK_CODE_PHONETIC_EXTENSIONS_SUPPLEMENT;

    public
     const
     int
      BLOCK_CODE_SUPPLEMENTAL_PUNCTUATION;

    public
     const
     int
      BLOCK_CODE_SYLOTI_NAGRI;

    public
     const
     int
      BLOCK_CODE_TIFINAGH;

    public
     const
     int
      BLOCK_CODE_VERTICAL_FORMS;

    public
     const
     int
      BLOCK_CODE_NKO;

    public
     const
     int
      BLOCK_CODE_BALINESE;

    public
     const
     int
      BLOCK_CODE_LATIN_EXTENDED_C;

    public
     const
     int
      BLOCK_CODE_LATIN_EXTENDED_D;

    public
     const
     int
      BLOCK_CODE_PHAGS_PA;

    public
     const
     int
      BLOCK_CODE_PHOENICIAN;

    public
     const
     int
      BLOCK_CODE_CUNEIFORM;

    public
     const
     int
      BLOCK_CODE_CUNEIFORM_NUMBERS_AND_PUNCTUATION;

    public
     const
     int
      BLOCK_CODE_COUNTING_ROD_NUMERALS;

    public
     const
     int
      BLOCK_CODE_SUNDANESE;

    public
     const
     int
      BLOCK_CODE_LEPCHA;

    public
     const
     int
      BLOCK_CODE_OL_CHIKI;

    public
     const
     int
      BLOCK_CODE_CYRILLIC_EXTENDED_A;

    public
     const
     int
      BLOCK_CODE_VAI;

    public
     const
     int
      BLOCK_CODE_CYRILLIC_EXTENDED_B;

    public
     const
     int
      BLOCK_CODE_SAURASHTRA;

    public
     const
     int
      BLOCK_CODE_KAYAH_LI;

    public
     const
     int
      BLOCK_CODE_REJANG;

    public
     const
     int
      BLOCK_CODE_CHAM;

    public
     const
     int
      BLOCK_CODE_ANCIENT_SYMBOLS;

    public
     const
     int
      BLOCK_CODE_PHAISTOS_DISC;

    public
     const
     int
      BLOCK_CODE_LYCIAN;

    public
     const
     int
      BLOCK_CODE_CARIAN;

    public
     const
     int
      BLOCK_CODE_LYDIAN;

    public
     const
     int
      BLOCK_CODE_MAHJONG_TILES;

    public
     const
     int
      BLOCK_CODE_DOMINO_TILES;

    public
     const
     int
      BLOCK_CODE_SAMARITAN;

    public
     const
     int
      BLOCK_CODE_UNIFIED_CANADIAN_ABORIGINAL_SYLLABICS_EXTENDED;

    public
     const
     int
      BLOCK_CODE_TAI_THAM;

    public
     const
     int
      BLOCK_CODE_VEDIC_EXTENSIONS;

    public
     const
     int
      BLOCK_CODE_LISU;

    public
     const
     int
      BLOCK_CODE_BAMUM;

    public
     const
     int
      BLOCK_CODE_COMMON_INDIC_NUMBER_FORMS;

    public
     const
     int
      BLOCK_CODE_DEVANAGARI_EXTENDED;

    public
     const
     int
      BLOCK_CODE_HANGUL_JAMO_EXTENDED_A;

    public
     const
     int
      BLOCK_CODE_JAVANESE;

    public
     const
     int
      BLOCK_CODE_MYANMAR_EXTENDED_A;

    public
     const
     int
      BLOCK_CODE_TAI_VIET;

    public
     const
     int
      BLOCK_CODE_MEETEI_MAYEK;

    public
     const
     int
      BLOCK_CODE_HANGUL_JAMO_EXTENDED_B;

    public
     const
     int
      BLOCK_CODE_IMPERIAL_ARAMAIC;

    public
     const
     int
      BLOCK_CODE_OLD_SOUTH_ARABIAN;

    public
     const
     int
      BLOCK_CODE_AVESTAN;

    public
     const
     int
      BLOCK_CODE_INSCRIPTIONAL_PARTHIAN;

    public
     const
     int
      BLOCK_CODE_INSCRIPTIONAL_PAHLAVI;

    public
     const
     int
      BLOCK_CODE_OLD_TURKIC;

    public
     const
     int
      BLOCK_CODE_RUMI_NUMERAL_SYMBOLS;

    public
     const
     int
      BLOCK_CODE_KAITHI;

    public
     const
     int
      BLOCK_CODE_EGYPTIAN_HIEROGLYPHS;

    public
     const
     int
      BLOCK_CODE_ENCLOSED_ALPHANUMERIC_SUPPLEMENT;

    public
     const
     int
      BLOCK_CODE_ENCLOSED_IDEOGRAPHIC_SUPPLEMENT;

    public
     const
     int
      BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_C;

    public
     const
     int
      BLOCK_CODE_MANDAIC;

    public
     const
     int
      BLOCK_CODE_BATAK;

    public
     const
     int
      BLOCK_CODE_ETHIOPIC_EXTENDED_A;

    public
     const
     int
      BLOCK_CODE_BRAHMI;

    public
     const
     int
      BLOCK_CODE_BAMUM_SUPPLEMENT;

    public
     const
     int
      BLOCK_CODE_KANA_SUPPLEMENT;

    public
     const
     int
      BLOCK_CODE_PLAYING_CARDS;

    public
     const
     int
      BLOCK_CODE_MISCELLANEOUS_SYMBOLS_AND_PICTOGRAPHS;

    public
     const
     int
      BLOCK_CODE_EMOTICONS;

    public
     const
     int
      BLOCK_CODE_TRANSPORT_AND_MAP_SYMBOLS;

    public
     const
     int
      BLOCK_CODE_ALCHEMICAL_SYMBOLS;

    public
     const
     int
      BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_D;

    public
     const
     int
      BLOCK_CODE_ARABIC_EXTENDED_A;

    public
     const
     int
      BLOCK_CODE_ARABIC_MATHEMATICAL_ALPHABETIC_SYMBOLS;

    public
     const
     int
      BLOCK_CODE_CHAKMA;

    public
     const
     int
      BLOCK_CODE_MEETEI_MAYEK_EXTENSIONS;

    public
     const
     int
      BLOCK_CODE_MEROITIC_CURSIVE;

    public
     const
     int
      BLOCK_CODE_MEROITIC_HIEROGLYPHS;

    public
     const
     int
      BLOCK_CODE_MIAO;

    public
     const
     int
      BLOCK_CODE_SHARADA;

    public
     const
     int
      BLOCK_CODE_SORA_SOMPENG;

    public
     const
     int
      BLOCK_CODE_SUNDANESE_SUPPLEMENT;

    public
     const
     int
      BLOCK_CODE_TAKRI;

    public
     const
     int
      BLOCK_CODE_BASSA_VAH;

    public
     const
     int
      BLOCK_CODE_CAUCASIAN_ALBANIAN;

    public
     const
     int
      BLOCK_CODE_COPTIC_EPACT_NUMBERS;

    public
     const
     int
      BLOCK_CODE_COMBINING_DIACRITICAL_MARKS_EXTENDED;

    public
     const
     int
      BLOCK_CODE_DUPLOYAN;

    public
     const
     int
      BLOCK_CODE_ELBASAN;

    public
     const
     int
      BLOCK_CODE_GEOMETRIC_SHAPES_EXTENDED;

    public
     const
     int
      BLOCK_CODE_GRANTHA;

    public
     const
     int
      BLOCK_CODE_KHOJKI;

    public
     const
     int
      BLOCK_CODE_KHUDAWADI;

    public
     const
     int
      BLOCK_CODE_LATIN_EXTENDED_E;

    public
     const
     int
      BLOCK_CODE_LINEAR_A;

    public
     const
     int
      BLOCK_CODE_MAHAJANI;

    public
     const
     int
      BLOCK_CODE_MANICHAEAN;

    public
     const
     int
      BLOCK_CODE_MENDE_KIKAKUI;

    public
     const
     int
      BLOCK_CODE_MODI;

    public
     const
     int
      BLOCK_CODE_MRO;

    public
     const
     int
      BLOCK_CODE_MYANMAR_EXTENDED_B;

    public
     const
     int
      BLOCK_CODE_NABATAEAN;

    public
     const
     int
      BLOCK_CODE_OLD_NORTH_ARABIAN;

    public
     const
     int
      BLOCK_CODE_OLD_PERMIC;

    public
     const
     int
      BLOCK_CODE_ORNAMENTAL_DINGBATS;

    public
     const
     int
      BLOCK_CODE_PAHAWH_HMONG;

    public
     const
     int
      BLOCK_CODE_PALMYRENE;

    public
     const
     int
      BLOCK_CODE_PAU_CIN_HAU;

    public
     const
     int
      BLOCK_CODE_PSALTER_PAHLAVI;

    public
     const
     int
      BLOCK_CODE_SHORTHAND_FORMAT_CONTROLS;

    public
     const
     int
      BLOCK_CODE_SIDDHAM;

    public
     const
     int
      BLOCK_CODE_SINHALA_ARCHAIC_NUMBERS;

    public
     const
     int
      BLOCK_CODE_SUPPLEMENTAL_ARROWS_C;

    public
     const
     int
      BLOCK_CODE_TIRHUTA;

    public
     const
     int
      BLOCK_CODE_WARANG_CITI;

    public
     const
     int
      BLOCK_CODE_COUNT;

    public
     const
     int
      BLOCK_CODE_INVALID_CODE;

    public
     const
     int
      BPT_NONE;

    public
     const
     int
      BPT_OPEN;

    public
     const
     int
      BPT_CLOSE;

    public
     const
     int
      BPT_COUNT;

    public
     const
     int
      EA_NEUTRAL;

    public
     const
     int
      EA_AMBIGUOUS;

    public
     const
     int
      EA_HALFWIDTH;

    public
     const
     int
      EA_FULLWIDTH;

    public
     const
     int
      EA_NARROW;

    public
     const
     int
      EA_WIDE;

    public
     const
     int
      EA_COUNT;

    public
     const
     int
      UNICODE_CHAR_NAME;

    public
     const
     int
      UNICODE_10_CHAR_NAME;

    public
     const
     int
      EXTENDED_CHAR_NAME;

    public
     const
     int
      CHAR_NAME_ALIAS;

    public
     const
     int
      CHAR_NAME_CHOICE_COUNT;

    public
     const
     int
      SHORT_PROPERTY_NAME;

    public
     const
     int
      LONG_PROPERTY_NAME;

    public
     const
     int
      PROPERTY_NAME_CHOICE_COUNT;

    public
     const
     int
      DT_NONE;

    public
     const
     int
      DT_CANONICAL;

    public
     const
     int
      DT_COMPAT;

    public
     const
     int
      DT_CIRCLE;

    public
     const
     int
      DT_FINAL;

    public
     const
     int
      DT_FONT;

    public
     const
     int
      DT_FRACTION;

    public
     const
     int
      DT_INITIAL;

    public
     const
     int
      DT_ISOLATED;

    public
     const
     int
      DT_MEDIAL;

    public
     const
     int
      DT_NARROW;

    public
     const
     int
      DT_NOBREAK;

    public
     const
     int
      DT_SMALL;

    public
     const
     int
      DT_SQUARE;

    public
     const
     int
      DT_SUB;

    public
     const
     int
      DT_SUPER;

    public
     const
     int
      DT_VERTICAL;

    public
     const
     int
      DT_WIDE;

    public
     const
     int
      DT_COUNT;

    public
     const
     int
      JT_NON_JOINING;

    public
     const
     int
      JT_JOIN_CAUSING;

    public
     const
     int
      JT_DUAL_JOINING;

    public
     const
     int
      JT_LEFT_JOINING;

    public
     const
     int
      JT_RIGHT_JOINING;

    public
     const
     int
      JT_TRANSPARENT;

    public
     const
     int
      JT_COUNT;

    public
     const
     int
      JG_NO_JOINING_GROUP;

    public
     const
     int
      JG_AIN;

    public
     const
     int
      JG_ALAPH;

    public
     const
     int
      JG_ALEF;

    public
     const
     int
      JG_BEH;

    public
     const
     int
      JG_BETH;

    public
     const
     int
      JG_DAL;

    public
     const
     int
      JG_DALATH_RISH;

    public
     const
     int
      JG_E;

    public
     const
     int
      JG_FEH;

    public
     const
     int
      JG_FINAL_SEMKATH;

    public
     const
     int
      JG_GAF;

    public
     const
     int
      JG_GAMAL;

    public
     const
     int
      JG_HAH;

    public
     const
     int
      JG_TEH_MARBUTA_GOAL;

    public
     const
     int
      JG_HAMZA_ON_HEH_GOAL;

    public
     const
     int
      JG_HE;

    public
     const
     int
      JG_HEH;

    public
     const
     int
      JG_HEH_GOAL;

    public
     const
     int
      JG_HETH;

    public
     const
     int
      JG_KAF;

    public
     const
     int
      JG_KAPH;

    public
     const
     int
      JG_KNOTTED_HEH;

    public
     const
     int
      JG_LAM;

    public
     const
     int
      JG_LAMADH;

    public
     const
     int
      JG_MEEM;

    public
     const
     int
      JG_MIM;

    public
     const
     int
      JG_NOON;

    public
     const
     int
      JG_NUN;

    public
     const
     int
      JG_PE;

    public
     const
     int
      JG_QAF;

    public
     const
     int
      JG_QAPH;

    public
     const
     int
      JG_REH;

    public
     const
     int
      JG_REVERSED_PE;

    public
     const
     int
      JG_SAD;

    public
     const
     int
      JG_SADHE;

    public
     const
     int
      JG_SEEN;

    public
     const
     int
      JG_SEMKATH;

    public
     const
     int
      JG_SHIN;

    public
     const
     int
      JG_SWASH_KAF;

    public
     const
     int
      JG_SYRIAC_WAW;

    public
     const
     int
      JG_TAH;

    public
     const
     int
      JG_TAW;

    public
     const
     int
      JG_TEH_MARBUTA;

    public
     const
     int
      JG_TETH;

    public
     const
     int
      JG_WAW;

    public
     const
     int
      JG_YEH;

    public
     const
     int
      JG_YEH_BARREE;

    public
     const
     int
      JG_YEH_WITH_TAIL;

    public
     const
     int
      JG_YUDH;

    public
     const
     int
      JG_YUDH_HE;

    public
     const
     int
      JG_ZAIN;

    public
     const
     int
      JG_FE;

    public
     const
     int
      JG_KHAPH;

    public
     const
     int
      JG_ZHAIN;

    public
     const
     int
      JG_BURUSHASKI_YEH_BARREE;

    public
     const
     int
      JG_FARSI_YEH;

    public
     const
     int
      JG_NYA;

    public
     const
     int
      JG_ROHINGYA_YEH;

    public
     const
     int
      JG_MANICHAEAN_ALEPH;

    public
     const
     int
      JG_MANICHAEAN_AYIN;

    public
     const
     int
      JG_MANICHAEAN_BETH;

    public
     const
     int
      JG_MANICHAEAN_DALETH;

    public
     const
     int
      JG_MANICHAEAN_DHAMEDH;

    public
     const
     int
      JG_MANICHAEAN_FIVE;

    public
     const
     int
      JG_MANICHAEAN_GIMEL;

    public
     const
     int
      JG_MANICHAEAN_HETH;

    public
     const
     int
      JG_MANICHAEAN_HUNDRED;

    public
     const
     int
      JG_MANICHAEAN_KAPH;

    public
     const
     int
      JG_MANICHAEAN_LAMEDH;

    public
     const
     int
      JG_MANICHAEAN_MEM;

    public
     const
     int
      JG_MANICHAEAN_NUN;

    public
     const
     int
      JG_MANICHAEAN_ONE;

    public
     const
     int
      JG_MANICHAEAN_PE;

    public
     const
     int
      JG_MANICHAEAN_QOPH;

    public
     const
     int
      JG_MANICHAEAN_RESH;

    public
     const
     int
      JG_MANICHAEAN_SADHE;

    public
     const
     int
      JG_MANICHAEAN_SAMEKH;

    public
     const
     int
      JG_MANICHAEAN_TAW;

    public
     const
     int
      JG_MANICHAEAN_TEN;

    public
     const
     int
      JG_MANICHAEAN_TETH;

    public
     const
     int
      JG_MANICHAEAN_THAMEDH;

    public
     const
     int
      JG_MANICHAEAN_TWENTY;

    public
     const
     int
      JG_MANICHAEAN_WAW;

    public
     const
     int
      JG_MANICHAEAN_YODH;

    public
     const
     int
      JG_MANICHAEAN_ZAYIN;

    public
     const
     int
      JG_STRAIGHT_WAW;

    public
     const
     int
      JG_COUNT;

    public
     const
     int
      GCB_OTHER;

    public
     const
     int
      GCB_CONTROL;

    public
     const
     int
      GCB_CR;

    public
     const
     int
      GCB_EXTEND;

    public
     const
     int
      GCB_L;

    public
     const
     int
      GCB_LF;

    public
     const
     int
      GCB_LV;

    public
     const
     int
      GCB_LVT;

    public
     const
     int
      GCB_T;

    public
     const
     int
      GCB_V;

    public
     const
     int
      GCB_SPACING_MARK;

    public
     const
     int
      GCB_PREPEND;

    public
     const
     int
      GCB_REGIONAL_INDICATOR;

    public
     const
     int
      GCB_COUNT;

    public
     const
     int
      WB_OTHER;

    public
     const
     int
      WB_ALETTER;

    public
     const
     int
      WB_FORMAT;

    public
     const
     int
      WB_KATAKANA;

    public
     const
     int
      WB_MIDLETTER;

    public
     const
     int
      WB_MIDNUM;

    public
     const
     int
      WB_NUMERIC;

    public
     const
     int
      WB_EXTENDNUMLET;

    public
     const
     int
      WB_CR;

    public
     const
     int
      WB_EXTEND;

    public
     const
     int
      WB_LF;

    public
     const
     int
      WB_MIDNUMLET;

    public
     const
     int
      WB_NEWLINE;

    public
     const
     int
      WB_REGIONAL_INDICATOR;

    public
     const
     int
      WB_HEBREW_LETTER;

    public
     const
     int
      WB_SINGLE_QUOTE;

    public
     const
     int
      WB_DOUBLE_QUOTE;

    public
     const
     int
      WB_COUNT;

    public
     const
     int
      SB_OTHER;

    public
     const
     int
      SB_ATERM;

    public
     const
     int
      SB_CLOSE;

    public
     const
     int
      SB_FORMAT;

    public
     const
     int
      SB_LOWER;

    public
     const
     int
      SB_NUMERIC;

    public
     const
     int
      SB_OLETTER;

    public
     const
     int
      SB_SEP;

    public
     const
     int
      SB_SP;

    public
     const
     int
      SB_STERM;

    public
     const
     int
      SB_UPPER;

    public
     const
     int
      SB_CR;

    public
     const
     int
      SB_EXTEND;

    public
     const
     int
      SB_LF;

    public
     const
     int
      SB_SCONTINUE;

    public
     const
     int
      SB_COUNT;

    public
     const
     int
      LB_UNKNOWN;

    public
     const
     int
      LB_AMBIGUOUS;

    public
     const
     int
      LB_ALPHABETIC;

    public
     const
     int
      LB_BREAK_BOTH;

    public
     const
     int
      LB_BREAK_AFTER;

    public
     const
     int
      LB_BREAK_BEFORE;

    public
     const
     int
      LB_MANDATORY_BREAK;

    public
     const
     int
      LB_CONTINGENT_BREAK;

    public
     const
     int
      LB_CLOSE_PUNCTUATION;

    public
     const
     int
      LB_COMBINING_MARK;

    public
     const
     int
      LB_CARRIAGE_RETURN;

    public
     const
     int
      LB_EXCLAMATION;

    public
     const
     int
      LB_GLUE;

    public
     const
     int
      LB_HYPHEN;

    public
     const
     int
      LB_IDEOGRAPHIC;

    public
     const
     int
      LB_INSEPARABLE;

    public
     const
     int
      LB_INSEPERABLE;

    public
     const
     int
      LB_INFIX_NUMERIC;

    public
     const
     int
      LB_LINE_FEED;

    public
     const
     int
      LB_NONSTARTER;

    public
     const
     int
      LB_NUMERIC;

    public
     const
     int
      LB_OPEN_PUNCTUATION;

    public
     const
     int
      LB_POSTFIX_NUMERIC;

    public
     const
     int
      LB_PREFIX_NUMERIC;

    public
     const
     int
      LB_QUOTATION;

    public
     const
     int
      LB_COMPLEX_CONTEXT;

    public
     const
     int
      LB_SURROGATE;

    public
     const
     int
      LB_SPACE;

    public
     const
     int
      LB_BREAK_SYMBOLS;

    public
     const
     int
      LB_ZWSPACE;

    public
     const
     int
      LB_NEXT_LINE;

    public
     const
     int
      LB_WORD_JOINER;

    public
     const
     int
      LB_H2;

    public
     const
     int
      LB_H3;

    public
     const
     int
      LB_JL;

    public
     const
     int
      LB_JT;

    public
     const
     int
      LB_JV;

    public
     const
     int
      LB_CLOSE_PARENTHESIS;

    public
     const
     int
      LB_CONDITIONAL_JAPANESE_STARTER;

    public
     const
     int
      LB_HEBREW_LETTER;

    public
     const
     int
      LB_REGIONAL_INDICATOR;

    public
     const
     int
      LB_COUNT;

    public
     const
     int
      NT_NONE;

    public
     const
     int
      NT_DECIMAL;

    public
     const
     int
      NT_DIGIT;

    public
     const
     int
      NT_NUMERIC;

    public
     const
     int
      NT_COUNT;

    public
     const
     int
      HST_NOT_APPLICABLE;

    public
     const
     int
      HST_LEADING_JAMO;

    public
     const
     int
      HST_VOWEL_JAMO;

    public
     const
     int
      HST_TRAILING_JAMO;

    public
     const
     int
      HST_LV_SYLLABLE;

    public
     const
     int
      HST_LVT_SYLLABLE;

    public
     const
     int
      HST_COUNT;

    public
     const
     int
      FOLD_CASE_DEFAULT;

    public
     const
     int
      FOLD_CASE_EXCLUDE_SPECIAL_I;


    /* Методы */
    
   public static charAge(int|string $codepoint): ?array
public static charDigitValue(int|string $codepoint): ?int
public static charDirection(int|string $codepoint): ?int
public static charFromName(string $name, int $type = IntlChar::UNICODE_CHAR_NAME): ?int
public static charMirror(int|string $codepoint): int|string|null
public static charName(int|string $codepoint, int $type = IntlChar::UNICODE_CHAR_NAME): ?string
public static charType(int|string $codepoint): ?int
public static chr(int|string $codepoint): ?string
public static digit(int|string $codepoint, int $base = 10): int|false|null
public static enumCharNames(    int|string $start,    int|string $end,    callable $callback,    int $type = IntlChar::UNICODE_CHAR_NAME): bool
public static enumCharTypes(callable $callback): void
public static foldCase(int|string $codepoint, int $options = IntlChar::FOLD_CASE_DEFAULT): int|string|null
public static forDigit(int $digit, int $base = 10): int
public static getBidiPairedBracket(int|string $codepoint): int|string|null
public static getBlockCode(int|string $codepoint): ?int
public static getCombiningClass(int|string $codepoint): ?int
public static getFC_NFKC_Closure(int|string $codepoint): string|false|null
public static getIntPropertyMaxValue(int $property): int
public static getIntPropertyMinValue(int $property): int
public static getIntPropertyValue(int|string $codepoint, int $property): ?int
public static getNumericValue(int|string $codepoint): ?float
public static getPropertyEnum(string $alias): int
public static getPropertyName(int $property, int $type = IntlChar::LONG_PROPERTY_NAME): string|false
public static getPropertyValueEnum(int $property, string $name): int
public static getPropertyValueName(int $property, int $value, int $type = IntlChar::LONG_PROPERTY_NAME): string|false
public static getUnicodeVersion(): array
public static hasBinaryProperty(int|string $codepoint, int $property): ?bool
public static isalnum(int|string $codepoint): ?bool
public static isalpha(int|string $codepoint): ?bool
public static isbase(int|string $codepoint): ?bool
public static isblank(int|string $codepoint): ?bool
public static iscntrl(int|string $codepoint): ?bool
public static isdefined(int|string $codepoint): ?bool
public static isdigit(int|string $codepoint): ?bool
public static isgraph(int|string $codepoint): ?bool
public static isIDIgnorable(int|string $codepoint): ?bool
public static isIDPart(int|string $codepoint): ?bool
public static isIDStart(int|string $codepoint): ?bool
public static isISOControl(int|string $codepoint): ?bool
public static isJavaIDPart(int|string $codepoint): ?bool
public static isJavaIDStart(int|string $codepoint): ?bool
public static isJavaSpaceChar(int|string $codepoint): ?bool
public static islower(int|string $codepoint): ?bool
public static isMirrored(int|string $codepoint): ?bool
public static isprint(int|string $codepoint): ?bool
public static ispunct(int|string $codepoint): ?bool
public static isspace(int|string $codepoint): ?bool
public static istitle(int|string $codepoint): ?bool
public static isUAlphabetic(int|string $codepoint): ?bool
public static isULowercase(int|string $codepoint): ?bool
public static isupper(int|string $codepoint): ?bool
public static isUUppercase(int|string $codepoint): ?bool
public static isUWhiteSpace(int|string $codepoint): ?bool
public static isWhitespace(int|string $codepoint): ?bool
public static isxdigit(int|string $codepoint): ?bool
public static ord(int|string $character): ?int
public static tolower(int|string $codepoint): int|string|null
public static totitle(int|string $codepoint): int|string|null
public static toupper(int|string $codepoint): int|string|null

   }
```

## Обумовлені константи

**`IntlChar::UNICODE_VERSION`**

**`IntlChar::CODEPOINT_MIN`**

**`IntlChar::CODEPOINT_MAX`**

**`IntlChar::NO_NUMERIC_VALUE`**

Special value that is returned by[IntlChar::getNumericValue()](intlchar.getnumericvalue.md)when no numeric value is defined for a code point.

**`IntlChar::PROPERTY_ALPHABETIC`**

**`IntlChar::PROPERTY_BINARY_START`**

**`IntlChar::PROPERTY_ASCII_HEX_DIGIT`**

**`IntlChar::PROPERTY_BIDI_CONTROL`**

**`IntlChar::PROPERTY_BIDI_MIRRORED`**

**`IntlChar::PROPERTY_DASH`**

**`IntlChar::PROPERTY_DEFAULT_IGNORABLE_CODE_POINT`**

**`IntlChar::PROPERTY_DEPRECATED`**

**`IntlChar::PROPERTY_DIACRITIC`**

**`IntlChar::PROPERTY_EXTENDER`**

**`IntlChar::PROPERTY_FULL_COMPOSITION_EXCLUSION`**

**`IntlChar::PROPERTY_GRAPHEME_BASE`**

**`IntlChar::PROPERTY_GRAPHEME_EXTEND`**

**`IntlChar::PROPERTY_GRAPHEME_LINK`**

**`IntlChar::PROPERTY_HEX_DIGIT`**

**`IntlChar::PROPERTY_HYPHEN`**

**`IntlChar::PROPERTY_ID_CONTINUE`**

**`IntlChar::PROPERTY_ID_START`**

**`IntlChar::PROPERTY_IDEOGRAPHIC`**

**`IntlChar::PROPERTY_IDS_BINARY_OPERATOR`**

**`IntlChar::PROPERTY_IDS_TRINARY_OPERATOR`**

**`IntlChar::PROPERTY_JOIN_CONTROL`**

**`IntlChar::PROPERTY_LOGICAL_ORDER_EXCEPTION`**

**`IntlChar::PROPERTY_LOWERCASE`**

**`IntlChar::PROPERTY_MATH`**

**`IntlChar::PROPERTY_NONCHARACTER_CODE_POINT`**

**`IntlChar::PROPERTY_QUOTATION_MARK`**

**`IntlChar::PROPERTY_RADICAL`**

**`IntlChar::PROPERTY_SOFT_DOTTED`**

**`IntlChar::PROPERTY_TERMINAL_PUNCTUATION`**

**`IntlChar::PROPERTY_UNIFIED_IDEOGRAPH`**

**`IntlChar::PROPERTY_UPPERCASE`**

**`IntlChar::PROPERTY_WHITE_SPACE`**

**`IntlChar::PROPERTY_XID_CONTINUE`**

**`IntlChar::PROPERTY_XID_START`**

**`IntlChar::PROPERTY_CASE_SENSITIVE`**

**`IntlChar::PROPERTY_S_TERM`**

**`IntlChar::PROPERTY_VARIATION_SELECTOR`**

**`IntlChar::PROPERTY_NFD_INERT`**

**`IntlChar::PROPERTY_NFKD_INERT`**

**`IntlChar::PROPERTY_NFC_INERT`**

**`IntlChar::PROPERTY_NFKC_INERT`**

**`IntlChar::PROPERTY_SEGMENT_STARTER`**

**`IntlChar::PROPERTY_PATTERN_SYNTAX`**

**`IntlChar::PROPERTY_PATTERN_WHITE_SPACE`**

**`IntlChar::PROPERTY_POSIX_ALNUM`**

**`IntlChar::PROPERTY_POSIX_BLANK`**

**`IntlChar::PROPERTY_POSIX_GRAPH`**

**`IntlChar::PROPERTY_POSIX_PRINT`**

**`IntlChar::PROPERTY_POSIX_XDIGIT`**

**`IntlChar::PROPERTY_CASED`**

**`IntlChar::PROPERTY_CASE_IGNORABLE`**

**`IntlChar::PROPERTY_CHANGES_WHEN_LOWERCASED`**

**`IntlChar::PROPERTY_CHANGES_WHEN_UPPERCASED`**

**`IntlChar::PROPERTY_CHANGES_WHEN_TITLECASED`**

**`IntlChar::PROPERTY_CHANGES_WHEN_CASEFOLDED`**

**`IntlChar::PROPERTY_CHANGES_WHEN_CASEMAPPED`**

**`IntlChar::PROPERTY_CHANGES_WHEN_NFKC_CASEFOLDED`**

**`IntlChar::PROPERTY_BINARY_LIMIT`**

**`IntlChar::PROPERTY_BIDI_CLASS`**

**`IntlChar::PROPERTY_INT_START`**

**`IntlChar::PROPERTY_BLOCK`**

**`IntlChar::PROPERTY_CANONICAL_COMBINING_CLASS`**

**`IntlChar::PROPERTY_DECOMPOSITION_TYPE`**

**`IntlChar::PROPERTY_EAST_ASIAN_WIDTH`**

**`IntlChar::PROPERTY_GENERAL_CATEGORY`**

**`IntlChar::PROPERTY_JOINING_GROUP`**

**`IntlChar::PROPERTY_JOINING_TYPE`**

**`IntlChar::PROPERTY_LINE_BREAK`**

**`IntlChar::PROPERTY_NUMERIC_TYPE`**

**`IntlChar::PROPERTY_SCRIPT`**

**`IntlChar::PROPERTY_HANGUL_SYLLABLE_TYPE`**

**`IntlChar::PROPERTY_NFD_QUICK_CHECK`**

**`IntlChar::PROPERTY_NFKD_QUICK_CHECK`**

**`IntlChar::PROPERTY_NFC_QUICK_CHECK`**

**`IntlChar::PROPERTY_NFKC_QUICK_CHECK`**

**`IntlChar::PROPERTY_LEAD_CANONICAL_COMBINING_CLASS`**

**`IntlChar::PROPERTY_TRAIL_CANONICAL_COMBINING_CLASS`**

**`IntlChar::PROPERTY_GRAPHEME_CLUSTER_BREAK`**

**`IntlChar::PROPERTY_SENTENCE_BREAK`**

**`IntlChar::PROPERTY_WORD_BREAK`**

**`IntlChar::PROPERTY_BIDI_PAIRED_BRACKET_TYPE`**

**`IntlChar::PROPERTY_INT_LIMIT`**

**`IntlChar::PROPERTY_GENERAL_CATEGORY_MASK`**

**`IntlChar::PROPERTY_MASK_START`**

**`IntlChar::PROPERTY_MASK_LIMIT`**

**`IntlChar::PROPERTY_NUMERIC_VALUE`**

**`IntlChar::PROPERTY_DOUBLE_START`**

**`IntlChar::PROPERTY_DOUBLE_LIMIT`**

**`IntlChar::PROPERTY_AGE`**

**`IntlChar::PROPERTY_STRING_START`**

**`IntlChar::PROPERTY_BIDI_MIRRORING_GLYPH`**

**`IntlChar::PROPERTY_CASE_FOLDING`**

**`IntlChar::PROPERTY_ISO_COMMENT`**

**`IntlChar::PROPERTY_LOWERCASE_MAPPING`**

**`IntlChar::PROPERTY_NAME`**

**`IntlChar::PROPERTY_SIMPLE_CASE_FOLDING`**

**`IntlChar::PROPERTY_SIMPLE_LOWERCASE_MAPPING`**

**`IntlChar::PROPERTY_SIMPLE_TITLECASE_MAPPING`**

**`IntlChar::PROPERTY_SIMPLE_UPPERCASE_MAPPING`**

**`IntlChar::PROPERTY_TITLECASE_MAPPING`**

**`IntlChar::PROPERTY_UNICODE_1_NAME`**

**`IntlChar::PROPERTY_UPPERCASE_MAPPING`**

**`IntlChar::PROPERTY_BIDI_PAIRED_BRACKET`**

**`IntlChar::PROPERTY_STRING_LIMIT`**

**`IntlChar::PROPERTY_SCRIPT_EXTENSIONS`**

**`IntlChar::PROPERTY_OTHER_PROPERTY_START`**

**`IntlChar::PROPERTY_OTHER_PROPERTY_LIMIT`**

**`IntlChar::PROPERTY_INVALID_CODE`**

**`IntlChar::CHAR_CATEGORY_UNASSIGNED`**

**`IntlChar::CHAR_CATEGORY_GENERAL_OTHER_TYPES`**

**`IntlChar::CHAR_CATEGORY_UPPERCASE_LETTER`**

**`IntlChar::CHAR_CATEGORY_LOWERCASE_LETTER`**

**`IntlChar::CHAR_CATEGORY_TITLECASE_LETTER`**

**`IntlChar::CHAR_CATEGORY_MODIFIER_LETTER`**

**`IntlChar::CHAR_CATEGORY_OTHER_LETTER`**

**`IntlChar::CHAR_CATEGORY_NON_SPACING_MARK`**

**`IntlChar::CHAR_CATEGORY_ENCLOSING_MARK`**

**`IntlChar::CHAR_CATEGORY_COMBINING_SPACING_MARK`**

**`IntlChar::CHAR_CATEGORY_DECIMAL_DIGIT_NUMBER`**

**`IntlChar::CHAR_CATEGORY_LETTER_NUMBER`**

**`IntlChar::CHAR_CATEGORY_OTHER_NUMBER`**

**`IntlChar::CHAR_CATEGORY_SPACE_SEPARATOR`**

**`IntlChar::CHAR_CATEGORY_LINE_SEPARATOR`**

**`IntlChar::CHAR_CATEGORY_PARAGRAPH_SEPARATOR`**

**`IntlChar::CHAR_CATEGORY_CONTROL_CHAR`**

**`IntlChar::CHAR_CATEGORY_FORMAT_CHAR`**

**`IntlChar::CHAR_CATEGORY_PRIVATE_USE_CHAR`**

**`IntlChar::CHAR_CATEGORY_SURROGATE`**

**`IntlChar::CHAR_CATEGORY_DASH_PUNCTUATION`**

**`IntlChar::CHAR_CATEGORY_START_PUNCTUATION`**

**`IntlChar::CHAR_CATEGORY_END_PUNCTUATION`**

**`IntlChar::CHAR_CATEGORY_CONNECTOR_PUNCTUATION`**

**`IntlChar::CHAR_CATEGORY_OTHER_PUNCTUATION`**

**`IntlChar::CHAR_CATEGORY_MATH_SYMBOL`**

**`IntlChar::CHAR_CATEGORY_CURRENCY_SYMBOL`**

**`IntlChar::CHAR_CATEGORY_MODIFIER_SYMBOL`**

**`IntlChar::CHAR_CATEGORY_OTHER_SYMBOL`**

**`IntlChar::CHAR_CATEGORY_INITIAL_PUNCTUATION`**

**`IntlChar::CHAR_CATEGORY_FINAL_PUNCTUATION`**

**`IntlChar::CHAR_CATEGORY_CHAR_CATEGORY_COUNT`**

**`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT`**

**`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT`**

**`IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER`**

**`IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER_SEPARATOR`**

**`IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER_TERMINATOR`**

**`IntlChar::CHAR_DIRECTION_ARABIC_NUMBER`**

**`IntlChar::CHAR_DIRECTION_COMMON_NUMBER_SEPARATOR`**

**`IntlChar::CHAR_DIRECTION_BLOCK_SEPARATOR`**

**`IntlChar::CHAR_DIRECTION_SEGMENT_SEPARATOR`**

**`IntlChar::CHAR_DIRECTION_WHITE_SPACE_NEUTRAL`**

**`IntlChar::CHAR_DIRECTION_OTHER_NEUTRAL`**

**`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT_EMBEDDING`**

**`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT_OVERRIDE`**

**`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_ARABIC`**

**`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_EMBEDDING`**

**`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_OVERRIDE`**

**`IntlChar::CHAR_DIRECTION_POP_DIRECTIONAL_FORMAT`**

**`IntlChar::CHAR_DIRECTION_DIR_NON_SPACING_MARK`**

**`IntlChar::CHAR_DIRECTION_BOUNDARY_NEUTRAL`**

**`IntlChar::CHAR_DIRECTION_FIRST_STRONG_ISOLATE`**

**`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT_ISOLATE`**

**`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_ISOLATE`**

**`IntlChar::CHAR_DIRECTION_POP_DIRECTIONAL_ISOLATE`**

**`IntlChar::CHAR_DIRECTION_CHAR_DIRECTION_COUNT`**

**`IntlChar::BLOCK_CODE_NO_BLOCK`**

**`IntlChar::BLOCK_CODE_BASIC_LATIN`**

**`IntlChar::BLOCK_CODE_LATIN_1_SUPPLEMENT`**

**`IntlChar::BLOCK_CODE_LATIN_EXTENDED_A`**

**`IntlChar::BLOCK_CODE_LATIN_EXTENDED_B`**

**`IntlChar::BLOCK_CODE_IPA_EXTENSIONS`**

**`IntlChar::BLOCK_CODE_SPACING_MODIFIER_LETTERS`**

**`IntlChar::BLOCK_CODE_COMBINING_DIACRITICAL_MARKS`**

**`IntlChar::BLOCK_CODE_GREEK`**

**`IntlChar::BLOCK_CODE_CYRILLIC`**

**`IntlChar::BLOCK_CODE_ARMENIAN`**

**`IntlChar::BLOCK_CODE_HEBREW`**

**`IntlChar::BLOCK_CODE_ARABIC`**

**`IntlChar::BLOCK_CODE_SYRIAC`**

**`IntlChar::BLOCK_CODE_THAANA`**

**`IntlChar::BLOCK_CODE_DEVANAGARI`**

**`IntlChar::BLOCK_CODE_BENGALI`**

**`IntlChar::BLOCK_CODE_GURMUKHI`**

**`IntlChar::BLOCK_CODE_GUJARATI`**

**`IntlChar::BLOCK_CODE_ORIYA`**

**`IntlChar::BLOCK_CODE_TAMIL`**

**`IntlChar::BLOCK_CODE_TELUGU`**

**`IntlChar::BLOCK_CODE_KANNADA`**

**`IntlChar::BLOCK_CODE_MALAYALAM`**

**`IntlChar::BLOCK_CODE_SINHALA`**

**`IntlChar::BLOCK_CODE_THAI`**

**`IntlChar::BLOCK_CODE_LAO`**

**`IntlChar::BLOCK_CODE_TIBETAN`**

**`IntlChar::BLOCK_CODE_MYANMAR`**

**`IntlChar::BLOCK_CODE_GEORGIAN`**

**`IntlChar::BLOCK_CODE_HANGUL_JAMO`**

**`IntlChar::BLOCK_CODE_ETHIOPIC`**

**`IntlChar::BLOCK_CODE_CHEROKEE`**

**`IntlChar::BLOCK_CODE_UNIFIED_CANADIAN_ABORIGINAL_SYLLABICS`**

**`IntlChar::BLOCK_CODE_OGHAM`**

**`IntlChar::BLOCK_CODE_RUNIC`**

**`IntlChar::BLOCK_CODE_KHMER`**

**`IntlChar::BLOCK_CODE_MONGOLIAN`**

**`IntlChar::BLOCK_CODE_LATIN_EXTENDED_ADDITIONAL`**

**`IntlChar::BLOCK_CODE_GREEK_EXTENDED`**

**`IntlChar::BLOCK_CODE_GENERAL_PUNCTUATION`**

**`IntlChar::BLOCK_CODE_SUPERSCRIPTS_AND_SUBSCRIPTS`**

**`IntlChar::BLOCK_CODE_CURRENCY_SYMBOLS`**

**`IntlChar::BLOCK_CODE_COMBINING_MARKS_FOR_SYMBOLS`**

**`IntlChar::BLOCK_CODE_LETTERLIKE_SYMBOLS`**

**`IntlChar::BLOCK_CODE_NUMBER_FORMS`**

**`IntlChar::BLOCK_CODE_ARROWS`**

**`IntlChar::BLOCK_CODE_MATHEMATICAL_OPERATORS`**

**`IntlChar::BLOCK_CODE_MISCELLANEOUS_TECHNICAL`**

**`IntlChar::BLOCK_CODE_CONTROL_PICTURES`**

**`IntlChar::BLOCK_CODE_OPTICAL_CHARACTER_RECOGNITION`**

**`IntlChar::BLOCK_CODE_ENCLOSED_ALPHANUMERICS`**

**`IntlChar::BLOCK_CODE_BOX_DRAWING`**

**`IntlChar::BLOCK_CODE_BLOCK_ELEMENTS`**

**`IntlChar::BLOCK_CODE_GEOMETRIC_SHAPES`**

**`IntlChar::BLOCK_CODE_MISCELLANEOUS_SYMBOLS`**

**`IntlChar::BLOCK_CODE_DINGBATS`**

**`IntlChar::BLOCK_CODE_BRAILLE_PATTERNS`**

**`IntlChar::BLOCK_CODE_CJK_RADICALS_SUPPLEMENT`**

**`IntlChar::BLOCK_CODE_KANGXI_RADICALS`**

**`IntlChar::BLOCK_CODE_IDEOGRAPHIC_DESCRIPTION_CHARACTERS`**

**`IntlChar::BLOCK_CODE_CJK_SYMBOLS_AND_PUNCTUATION`**

**`IntlChar::BLOCK_CODE_HIRAGANA`**

**`IntlChar::BLOCK_CODE_KATAKANA`**

**`IntlChar::BLOCK_CODE_BOPOMOFO`**

**`IntlChar::BLOCK_CODE_HANGUL_COMPATIBILITY_JAMO`**

**`IntlChar::BLOCK_CODE_KANBUN`**

**`IntlChar::BLOCK_CODE_BOPOMOFO_EXTENDED`**

**`IntlChar::BLOCK_CODE_ENCLOSED_CJK_LETTERS_AND_MONTHS`**

**`IntlChar::BLOCK_CODE_CJK_COMPATIBILITY`**

**`IntlChar::BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_A`**

**`IntlChar::BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS`**

**`IntlChar::BLOCK_CODE_YI_SYLLABLES`**

**`IntlChar::BLOCK_CODE_YI_RADICALS`**

**`IntlChar::BLOCK_CODE_HANGUL_SYLLABLES`**

**`IntlChar::BLOCK_CODE_HIGH_SURROGATES`**

**`IntlChar::BLOCK_CODE_HIGH_PRIVATE_USE_SURROGATES`**

**`IntlChar::BLOCK_CODE_LOW_SURROGATES`**

**`IntlChar::BLOCK_CODE_PRIVATE_USE_AREA`**

**`IntlChar::BLOCK_CODE_PRIVATE_USE`**

**`IntlChar::BLOCK_CODE_CJK_COMPATIBILITY_IDEOGRAPHS`**

**`IntlChar::BLOCK_CODE_ALPHABETIC_PRESENTATION_FORMS`**

**`IntlChar::BLOCK_CODE_ARABIC_PRESENTATION_FORMS_A`**

**`IntlChar::BLOCK_CODE_COMBINING_HALF_MARKS`**

**`IntlChar::BLOCK_CODE_CJK_COMPATIBILITY_FORMS`**

**`IntlChar::BLOCK_CODE_SMALL_FORM_VARIANTS`**

**`IntlChar::BLOCK_CODE_ARABIC_PRESENTATION_FORMS_B`**

**`IntlChar::BLOCK_CODE_SPECIALS`**

**`IntlChar::BLOCK_CODE_HALFWIDTH_AND_FULLWIDTH_FORMS`**

**`IntlChar::BLOCK_CODE_OLD_ITALIC`**

**`IntlChar::BLOCK_CODE_GOTHIC`**

**`IntlChar::BLOCK_CODE_DESERET`**

**`IntlChar::BLOCK_CODE_BYZANTINE_MUSICAL_SYMBOLS`**

**`IntlChar::BLOCK_CODE_MUSICAL_SYMBOLS`**

**`IntlChar::BLOCK_CODE_MATHEMATICAL_ALPHANUMERIC_SYMBOLS`**

**`IntlChar::BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_B`**

**`IntlChar::BLOCK_CODE_CJK_COMPATIBILITY_IDEOGRAPHS_SUPPLEMENT`**

**`IntlChar::BLOCK_CODE_TAGS`**

**`IntlChar::BLOCK_CODE_CYRILLIC_SUPPLEMENT`**

**`IntlChar::BLOCK_CODE_CYRILLIC_SUPPLEMENTARY`**

**`IntlChar::BLOCK_CODE_TAGALOG`**

**`IntlChar::BLOCK_CODE_HANUNOO`**

**`IntlChar::BLOCK_CODE_BUHID`**

**`IntlChar::BLOCK_CODE_TAGBANWA`**

**`IntlChar::BLOCK_CODE_MISCELLANEOUS_MATHEMATICAL_SYMBOLS_A`**

**`IntlChar::BLOCK_CODE_SUPPLEMENTAL_ARROWS_A`**

**`IntlChar::BLOCK_CODE_SUPPLEMENTAL_ARROWS_B`**

**`IntlChar::BLOCK_CODE_MISCELLANEOUS_MATHEMATICAL_SYMBOLS_B`**

**`IntlChar::BLOCK_CODE_SUPPLEMENTAL_MATHEMATICAL_OPERATORS`**

**`IntlChar::BLOCK_CODE_KATAKANA_PHONETIC_EXTENSIONS`**

**`IntlChar::BLOCK_CODE_VARIATION_SELECTORS`**

**`IntlChar::BLOCK_CODE_SUPPLEMENTARY_PRIVATE_USE_AREA_A`**

**`IntlChar::BLOCK_CODE_SUPPLEMENTARY_PRIVATE_USE_AREA_B`**

**`IntlChar::BLOCK_CODE_LIMBU`**

**`IntlChar::BLOCK_CODE_TAI_LE`**

**`IntlChar::BLOCK_CODE_KHMER_SYMBOLS`**

**`IntlChar::BLOCK_CODE_PHONETIC_EXTENSIONS`**

**`IntlChar::BLOCK_CODE_MISCELLANEOUS_SYMBOLS_AND_ARROWS`**

**`IntlChar::BLOCK_CODE_YIJING_HEXAGRAM_SYMBOLS`**

**`IntlChar::BLOCK_CODE_LINEAR_B_SYLLABARY`**

**`IntlChar::BLOCK_CODE_LINEAR_B_IDEOGRAMS`**

**`IntlChar::BLOCK_CODE_AEGEAN_NUMBERS`**

**`IntlChar::BLOCK_CODE_UGARITIC`**

**`IntlChar::BLOCK_CODE_SHAVIAN`**

**`IntlChar::BLOCK_CODE_OSMANYA`**

**`IntlChar::BLOCK_CODE_CYPRIOT_SYLLABARY`**

**`IntlChar::BLOCK_CODE_TAI_XUAN_JING_SYMBOLS`**

**`IntlChar::BLOCK_CODE_VARIATION_SELECTORS_SUPPLEMENT`**

**`IntlChar::BLOCK_CODE_ANCIENT_GREEK_MUSICAL_NOTATION`**

**`IntlChar::BLOCK_CODE_ANCIENT_GREEK_NUMBERS`**

**`IntlChar::BLOCK_CODE_ARABIC_SUPPLEMENT`**

**`IntlChar::BLOCK_CODE_BUGINESE`**

**`IntlChar::BLOCK_CODE_CJK_STROKES`**

**`IntlChar::BLOCK_CODE_COMBINING_DIACRITICAL_MARKS_SUPPLEMENT`**

**`IntlChar::BLOCK_CODE_COPTIC`**

**`IntlChar::BLOCK_CODE_ETHIOPIC_EXTENDED`**

**`IntlChar::BLOCK_CODE_ETHIOPIC_SUPPLEMENT`**

**`IntlChar::BLOCK_CODE_GEORGIAN_SUPPLEMENT`**

**`IntlChar::BLOCK_CODE_GLAGOLITIC`**

**`IntlChar::BLOCK_CODE_KHAROSHTHI`**

**`IntlChar::BLOCK_CODE_MODIFIER_TONE_LETTERS`**

**`IntlChar::BLOCK_CODE_NEW_TAI_LUE`**

**`IntlChar::BLOCK_CODE_OLD_PERSIAN`**

**`IntlChar::BLOCK_CODE_PHONETIC_EXTENSIONS_SUPPLEMENT`**

**`IntlChar::BLOCK_CODE_SUPPLEMENTAL_PUNCTUATION`**

**`IntlChar::BLOCK_CODE_SYLOTI_NAGRI`**

**`IntlChar::BLOCK_CODE_TIFINAGH`**

**`IntlChar::BLOCK_CODE_VERTICAL_FORMS`**

**`IntlChar::BLOCK_CODE_NKO`**

**`IntlChar::BLOCK_CODE_BALINESE`**

**`IntlChar::BLOCK_CODE_LATIN_EXTENDED_C`**

**`IntlChar::BLOCK_CODE_LATIN_EXTENDED_D`**

**`IntlChar::BLOCK_CODE_PHAGS_PA`**

**`IntlChar::BLOCK_CODE_PHOENICIAN`**

**`IntlChar::BLOCK_CODE_CUNEIFORM`**

**`IntlChar::BLOCK_CODE_CUNEIFORM_NUMBERS_AND_PUNCTUATION`**

**`IntlChar::BLOCK_CODE_COUNTING_ROD_NUMERALS`**

**`IntlChar::BLOCK_CODE_SUNDANESE`**

**`IntlChar::BLOCK_CODE_LEPCHA`**

**`IntlChar::BLOCK_CODE_OL_CHIKI`**

**`IntlChar::BLOCK_CODE_CYRILLIC_EXTENDED_A`**

**`IntlChar::BLOCK_CODE_VAI`**

**`IntlChar::BLOCK_CODE_CYRILLIC_EXTENDED_B`**

**`IntlChar::BLOCK_CODE_SAURASHTRA`**

**`IntlChar::BLOCK_CODE_KAYAH_LI`**

**`IntlChar::BLOCK_CODE_REJANG`**

**`IntlChar::BLOCK_CODE_CHAM`**

**`IntlChar::BLOCK_CODE_ANCIENT_SYMBOLS`**

**`IntlChar::BLOCK_CODE_PHAISTOS_DISC`**

**`IntlChar::BLOCK_CODE_LYCIAN`**

**`IntlChar::BLOCK_CODE_CARIAN`**

**`IntlChar::BLOCK_CODE_LYDIAN`**

**`IntlChar::BLOCK_CODE_MAHJONG_TILES`**

**`IntlChar::BLOCK_CODE_DOMINO_TILES`**

**`IntlChar::BLOCK_CODE_SAMARITAN`**

**`IntlChar::BLOCK_CODE_UNIFIED_CANADIAN_ABORIGINAL_SYLLABICS_EXTENDED`**

**`IntlChar::BLOCK_CODE_TAI_THAM`**

**`IntlChar::BLOCK_CODE_VEDIC_EXTENSIONS`**

**`IntlChar::BLOCK_CODE_LISU`**

**`IntlChar::BLOCK_CODE_BAMUM`**

**`IntlChar::BLOCK_CODE_COMMON_INDIC_NUMBER_FORMS`**

**`IntlChar::BLOCK_CODE_DEVANAGARI_EXTENDED`**

**`IntlChar::BLOCK_CODE_HANGUL_JAMO_EXTENDED_A`**

**`IntlChar::BLOCK_CODE_JAVANESE`**

**`IntlChar::BLOCK_CODE_MYANMAR_EXTENDED_A`**

**`IntlChar::BLOCK_CODE_TAI_VIET`**

**`IntlChar::BLOCK_CODE_MEETEI_MAYEK`**

**`IntlChar::BLOCK_CODE_HANGUL_JAMO_EXTENDED_B`**

**`IntlChar::BLOCK_CODE_IMPERIAL_ARAMAIC`**

**`IntlChar::BLOCK_CODE_OLD_SOUTH_ARABIAN`**

**`IntlChar::BLOCK_CODE_AVESTAN`**

**`IntlChar::BLOCK_CODE_INSCRIPTIONAL_PARTHIAN`**

**`IntlChar::BLOCK_CODE_INSCRIPTIONAL_PAHLAVI`**

**`IntlChar::BLOCK_CODE_OLD_TURKIC`**

**`IntlChar::BLOCK_CODE_RUMI_NUMERAL_SYMBOLS`**

**`IntlChar::BLOCK_CODE_KAITHI`**

**`IntlChar::BLOCK_CODE_EGYPTIAN_HIEROGLYPHS`**

**`IntlChar::BLOCK_CODE_ENCLOSED_ALPHANUMERIC_SUPPLEMENT`**

**`IntlChar::BLOCK_CODE_ENCLOSED_IDEOGRAPHIC_SUPPLEMENT`**

**`IntlChar::BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_C`**

**`IntlChar::BLOCK_CODE_MANDAIC`**

**`IntlChar::BLOCK_CODE_BATAK`**

**`IntlChar::BLOCK_CODE_ETHIOPIC_EXTENDED_A`**

**`IntlChar::BLOCK_CODE_BRAHMI`**

**`IntlChar::BLOCK_CODE_BAMUM_SUPPLEMENT`**

**`IntlChar::BLOCK_CODE_KANA_SUPPLEMENT`**

**`IntlChar::BLOCK_CODE_PLAYING_CARDS`**

**`IntlChar::BLOCK_CODE_MISCELLANEOUS_SYMBOLS_AND_PICTOGRAPHS`**

**`IntlChar::BLOCK_CODE_EMOTICONS`**

**`IntlChar::BLOCK_CODE_TRANSPORT_AND_MAP_SYMBOLS`**

**`IntlChar::BLOCK_CODE_ALCHEMICAL_SYMBOLS`**

**`IntlChar::BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_D`**

**`IntlChar::BLOCK_CODE_ARABIC_EXTENDED_A`**

**`IntlChar::BLOCK_CODE_ARABIC_MATHEMATICAL_ALPHABETIC_SYMBOLS`**

**`IntlChar::BLOCK_CODE_CHAKMA`**

**`IntlChar::BLOCK_CODE_MEETEI_MAYEK_EXTENSIONS`**

**`IntlChar::BLOCK_CODE_MEROITIC_CURSIVE`**

**`IntlChar::BLOCK_CODE_MEROITIC_HIEROGLYPHS`**

**`IntlChar::BLOCK_CODE_MIAO`**

**`IntlChar::BLOCK_CODE_SHARADA`**

**`IntlChar::BLOCK_CODE_SORA_SOMPENG`**

**`IntlChar::BLOCK_CODE_SUNDANESE_SUPPLEMENT`**

**`IntlChar::BLOCK_CODE_TAKRI`**

**`IntlChar::BLOCK_CODE_BASSA_VAH`**

**`IntlChar::BLOCK_CODE_CAUCASIAN_ALBANIAN`**

**`IntlChar::BLOCK_CODE_COPTIC_EPACT_NUMBERS`**

**`IntlChar::BLOCK_CODE_COMBINING_DIACRITICAL_MARKS_EXTENDED`**

**`IntlChar::BLOCK_CODE_DUPLOYAN`**

**`IntlChar::BLOCK_CODE_ELBASAN`**

**`IntlChar::BLOCK_CODE_GEOMETRIC_SHAPES_EXTENDED`**

**`IntlChar::BLOCK_CODE_GRANTHA`**

**`IntlChar::BLOCK_CODE_KHOJKI`**

**`IntlChar::BLOCK_CODE_KHUDAWADI`**

**`IntlChar::BLOCK_CODE_LATIN_EXTENDED_E`**

**`IntlChar::BLOCK_CODE_LINEAR_A`**

**`IntlChar::BLOCK_CODE_MAHAJANI`**

**`IntlChar::BLOCK_CODE_MANICHAEAN`**

**`IntlChar::BLOCK_CODE_MENDE_KIKAKUI`**

**`IntlChar::BLOCK_CODE_MODI`**

**`IntlChar::BLOCK_CODE_MRO`**

**`IntlChar::BLOCK_CODE_MYANMAR_EXTENDED_B`**

**`IntlChar::BLOCK_CODE_NABATAEAN`**

**`IntlChar::BLOCK_CODE_OLD_NORTH_ARABIAN`**

**`IntlChar::BLOCK_CODE_OLD_PERMIC`**

**`IntlChar::BLOCK_CODE_ORNAMENTAL_DINGBATS`**

**`IntlChar::BLOCK_CODE_PAHAWH_HMONG`**

**`IntlChar::BLOCK_CODE_PALMYRENE`**

**`IntlChar::BLOCK_CODE_PAU_CIN_HAU`**

**`IntlChar::BLOCK_CODE_PSALTER_PAHLAVI`**

**`IntlChar::BLOCK_CODE_SHORTHAND_FORMAT_CONTROLS`**

**`IntlChar::BLOCK_CODE_SIDDHAM`**

**`IntlChar::BLOCK_CODE_SINHALA_ARCHAIC_NUMBERS`**

**`IntlChar::BLOCK_CODE_SUPPLEMENTAL_ARROWS_C`**

**`IntlChar::BLOCK_CODE_TIRHUTA`**

**`IntlChar::BLOCK_CODE_WARANG_CITI`**

**`IntlChar::BLOCK_CODE_COUNT`**

**`IntlChar::BLOCK_CODE_INVALID_CODE`**

**`IntlChar::BPT_NONE`**

**`IntlChar::BPT_OPEN`**

**`IntlChar::BPT_CLOSE`**

**`IntlChar::BPT_COUNT`**

**`IntlChar::EA_NEUTRAL`**

**`IntlChar::EA_AMBIGUOUS`**

**`IntlChar::EA_HALFWIDTH`**

**`IntlChar::EA_FULLWIDTH`**

**`IntlChar::EA_NARROW`**

**`IntlChar::EA_WIDE`**

**`IntlChar::EA_COUNT`**

**`IntlChar::UNICODE_CHAR_NAME`**

**`IntlChar::UNICODE_10_CHAR_NAME`**

**`IntlChar::EXTENDED_CHAR_NAME`**

**`IntlChar::CHAR_NAME_ALIAS`**

**`IntlChar::CHAR_NAME_CHOICE_COUNT`**

**`IntlChar::SHORT_PROPERTY_NAME`**

**`IntlChar::LONG_PROPERTY_NAME`**

**`IntlChar::PROPERTY_NAME_CHOICE_COUNT`**

**`IntlChar::DT_NONE`**

**`IntlChar::DT_CANONICAL`**

**`IntlChar::DT_COMPAT`**

**`IntlChar::DT_CIRCLE`**

**`IntlChar::DT_FINAL`**

**`IntlChar::DT_FONT`**

**`IntlChar::DT_FRACTION`**

**`IntlChar::DT_INITIAL`**

**`IntlChar::DT_ISOLATED`**

**`IntlChar::DT_MEDIAL`**

**`IntlChar::DT_NARROW`**

**`IntlChar::DT_NOBREAK`**

**`IntlChar::DT_SMALL`**

**`IntlChar::DT_SQUARE`**

**`IntlChar::DT_SUB`**

**`IntlChar::DT_SUPER`**

**`IntlChar::DT_VERTICAL`**

**`IntlChar::DT_WIDE`**

**`IntlChar::DT_COUNT`**

**`IntlChar::JT_NON_JOINING`**

**`IntlChar::JT_JOIN_CAUSING`**

**`IntlChar::JT_DUAL_JOINING`**

**`IntlChar::JT_LEFT_JOINING`**

**`IntlChar::JT_RIGHT_JOINING`**

**`IntlChar::JT_TRANSPARENT`**

**`IntlChar::JT_COUNT`**

**`IntlChar::JG_NO_JOINING_GROUP`**

**`IntlChar::JG_AIN`**

**`IntlChar::JG_ALAPH`**

**`IntlChar::JG_ALEF`**

**`IntlChar::JG_BEH`**

**`IntlChar::JG_BETH`**

**`IntlChar::JG_DAL`**

**`IntlChar::JG_DALATH_RISH`**

**`IntlChar::JG_E`**

**`IntlChar::JG_FEH`**

**`IntlChar::JG_FINAL_SEMKATH`**

**`IntlChar::JG_GAF`**

**`IntlChar::JG_GAMAL`**

**`IntlChar::JG_HAH`**

**`IntlChar::JG_TEH_MARBUTA_GOAL`**

**`IntlChar::JG_HAMZA_ON_HEH_GOAL`**

**`IntlChar::JG_HE`**

**`IntlChar::JG_HEH`**

**`IntlChar::JG_HEH_GOAL`**

**`IntlChar::JG_HETH`**

**`IntlChar::JG_KAF`**

**`IntlChar::JG_KAPH`**

**`IntlChar::JG_KNOTTED_HEH`**

**`IntlChar::JG_LAM`**

**`IntlChar::JG_LAMADH`**

**`IntlChar::JG_MEEM`**

**`IntlChar::JG_MIM`**

**`IntlChar::JG_NOON`**

**`IntlChar::JG_NUN`**

**`IntlChar::JG_PE`**

**`IntlChar::JG_QAF`**

**`IntlChar::JG_QAPH`**

**`IntlChar::JG_REH`**

**`IntlChar::JG_REVERSED_PE`**

**`IntlChar::JG_SAD`**

**`IntlChar::JG_SADHE`**

**`IntlChar::JG_SEEN`**

**`IntlChar::JG_SEMKATH`**

**`IntlChar::JG_SHIN`**

**`IntlChar::JG_SWASH_KAF`**

**`IntlChar::JG_SYRIAC_WAW`**

**`IntlChar::JG_TAH`**

**`IntlChar::JG_TAW`**

**`IntlChar::JG_TEH_MARBUTA`**

**`IntlChar::JG_TETH`**

**`IntlChar::JG_WAW`**

**`IntlChar::JG_YEH`**

**`IntlChar::JG_YEH_BARREE`**

**`IntlChar::JG_YEH_WITH_TAIL`**

**`IntlChar::JG_YUDH`**

**`IntlChar::JG_YUDH_HE`**

**`IntlChar::JG_ZAIN`**

**`IntlChar::JG_FE`**

**`IntlChar::JG_KHAPH`**

**`IntlChar::JG_ZHAIN`**

**`IntlChar::JG_BURUSHASKI_YEH_BARREE`**

**`IntlChar::JG_FARSI_YEH`**

**`IntlChar::JG_NYA`**

**`IntlChar::JG_ROHINGYA_YEH`**

**`IntlChar::JG_MANICHAEAN_ALEPH`**

**`IntlChar::JG_MANICHAEAN_AYIN`**

**`IntlChar::JG_MANICHAEAN_BETH`**

**`IntlChar::JG_MANICHAEAN_DALETH`**

**`IntlChar::JG_MANICHAEAN_DHAMEDH`**

**`IntlChar::JG_MANICHAEAN_FIVE`**

**`IntlChar::JG_MANICHAEAN_GIMEL`**

**`IntlChar::JG_MANICHAEAN_HETH`**

**`IntlChar::JG_MANICHAEAN_HUNDRED`**

**`IntlChar::JG_MANICHAEAN_KAPH`**

**`IntlChar::JG_MANICHAEAN_LAMEDH`**

**`IntlChar::JG_MANICHAEAN_MEM`**

**`IntlChar::JG_MANICHAEAN_NUN`**

**`IntlChar::JG_MANICHAEAN_ONE`**

**`IntlChar::JG_MANICHAEAN_PE`**

**`IntlChar::JG_MANICHAEAN_QOPH`**

**`IntlChar::JG_MANICHAEAN_RESH`**

**`IntlChar::JG_MANICHAEAN_SADHE`**

**`IntlChar::JG_MANICHAEAN_SAMEKH`**

**`IntlChar::JG_MANICHAEAN_TAW`**

**`IntlChar::JG_MANICHAEAN_TEN`**

**`IntlChar::JG_MANICHAEAN_TETH`**

**`IntlChar::JG_MANICHAEAN_THAMEDH`**

**`IntlChar::JG_MANICHAEAN_TWENTY`**

**`IntlChar::JG_MANICHAEAN_WAW`**

**`IntlChar::JG_MANICHAEAN_YODH`**

**`IntlChar::JG_MANICHAEAN_ZAYIN`**

**`IntlChar::JG_STRAIGHT_WAW`**

**`IntlChar::JG_COUNT`**

**`IntlChar::GCB_OTHER`**

**`IntlChar::GCB_CONTROL`**

**`IntlChar::GCB_CR`**

**`IntlChar::GCB_EXTEND`**

**`IntlChar::GCB_L`**

**`IntlChar::GCB_LF`**

**`IntlChar::GCB_LV`**

**`IntlChar::GCB_LVT`**

**`IntlChar::GCB_T`**

**`IntlChar::GCB_V`**

**`IntlChar::GCB_SPACING_MARK`**

**`IntlChar::GCB_PREPEND`**

**`IntlChar::GCB_REGIONAL_INDICATOR`**

**`IntlChar::GCB_COUNT`**

**`IntlChar::WB_OTHER`**

**`IntlChar::WB_ALETTER`**

**`IntlChar::WB_FORMAT`**

**`IntlChar::WB_KATAKANA`**

**`IntlChar::WB_MIDLETTER`**

**`IntlChar::WB_MIDNUM`**

**`IntlChar::WB_NUMERIC`**

**`IntlChar::WB_EXTENDNUMLET`**

**`IntlChar::WB_CR`**

**`IntlChar::WB_EXTEND`**

**`IntlChar::WB_LF`**

**`IntlChar::WB_MIDNUMLET`**

**`IntlChar::WB_NEWLINE`**

**`IntlChar::WB_REGIONAL_INDICATOR`**

**`IntlChar::WB_HEBREW_LETTER`**

**`IntlChar::WB_SINGLE_QUOTE`**

**`IntlChar::WB_DOUBLE_QUOTE`**

**`IntlChar::WB_COUNT`**

**`IntlChar::SB_OTHER`**

**`IntlChar::SB_ATERM`**

**`IntlChar::SB_CLOSE`**

**`IntlChar::SB_FORMAT`**

**`IntlChar::SB_LOWER`**

**`IntlChar::SB_NUMERIC`**

**`IntlChar::SB_OLETTER`**

**`IntlChar::SB_SEP`**

**`IntlChar::SB_SP`**

**`IntlChar::SB_STERM`**

**`IntlChar::SB_UPPER`**

**`IntlChar::SB_CR`**

**`IntlChar::SB_EXTEND`**

**`IntlChar::SB_LF`**

**`IntlChar::SB_SCONTINUE`**

**`IntlChar::SB_COUNT`**

**`IntlChar::LB_UNKNOWN`**

**`IntlChar::LB_AMBIGUOUS`**

**`IntlChar::LB_ALPHABETIC`**

**`IntlChar::LB_BREAK_BOTH`**

**`IntlChar::LB_BREAK_AFTER`**

**`IntlChar::LB_BREAK_BEFORE`**

**`IntlChar::LB_MANDATORY_BREAK`**

**`IntlChar::LB_CONTINGENT_BREAK`**

**`IntlChar::LB_CLOSE_PUNCTUATION`**

**`IntlChar::LB_COMBINING_MARK`**

**`IntlChar::LB_CARRIAGE_RETURN`**

**`IntlChar::LB_EXCLAMATION`**

**`IntlChar::LB_GLUE`**

**`IntlChar::LB_HYPHEN`**

**`IntlChar::LB_IDEOGRAPHIC`**

**`IntlChar::LB_INSEPARABLE`**

**`IntlChar::LB_INSEPERABLE`**

**`IntlChar::LB_INFIX_NUMERIC`**

**`IntlChar::LB_LINE_FEED`**

**`IntlChar::LB_NONSTARTER`**

**`IntlChar::LB_NUMERIC`**

**`IntlChar::LB_OPEN_PUNCTUATION`**

**`IntlChar::LB_POSTFIX_NUMERIC`**

**`IntlChar::LB_PREFIX_NUMERIC`**

**`IntlChar::LB_QUOTATION`**

**`IntlChar::LB_COMPLEX_CONTEXT`**

**`IntlChar::LB_SURROGATE`**

**`IntlChar::LB_SPACE`**

**`IntlChar::LB_BREAK_SYMBOLS`**

**`IntlChar::LB_ZWSPACE`**

**`IntlChar::LB_NEXT_LINE`**

**`IntlChar::LB_WORD_JOINER`**

**`IntlChar::LB_H2`**

**`IntlChar::LB_H3`**

**`IntlChar::LB_JL`**

**`IntlChar::LB_JT`**

**`IntlChar::LB_JV`**

**`IntlChar::LB_CLOSE_PARENTHESIS`**

**`IntlChar::LB_CONDITIONAL_JAPANESE_STARTER`**

**`IntlChar::LB_HEBREW_LETTER`**

**`IntlChar::LB_REGIONAL_INDICATOR`**

**`IntlChar::LB_COUNT`**

**`IntlChar::NT_NONE`**

**`IntlChar::NT_DECIMAL`**

**`IntlChar::NT_DIGIT`**

**`IntlChar::NT_NUMERIC`**

**`IntlChar::NT_COUNT`**

**`IntlChar::HST_NOT_APPLICABLE`**

**`IntlChar::HST_LEADING_JAMO`**

**`IntlChar::HST_VOWEL_JAMO`**

**`IntlChar::HST_TRAILING_JAMO`**

**`IntlChar::HST_LV_SYLLABLE`**

**`IntlChar::HST_LVT_SYLLABLE`**

**`IntlChar::HST_COUNT`**

**`IntlChar::FOLD_CASE_DEFAULT`**

**`IntlChar::FOLD_CASE_EXCLUDE_SPECIAL_I`**

## список змін

| Версия | Опис |
| --- | --- |
| 7.0.6 | Добавлена константа\*\*`IntlChar::NO_NUMERIC_VALUE`\*\* |

## Зміст

-   [IntlChar::charAge](intlchar.charage.md) — Отримати "вік" символьного коду
-   [IntlChar::charDigitValue](intlchar.chardigitvalue.md)— Отримати десяткову цифру із символу десяткової цифри
-   [IntlChar::charDirection](intlchar.chardirection.md)— Отримати категорію напряму листа для символу
-   [IntlChar::charFromName](intlchar.charfromname.md)— Знайти символ Unicode на його ім'я та повернути його код
-   [IntlChar::charMirror](intlchar.charmirror.md) — Отримати "дзеркальний" символ за кодом
-   [IntlChar::charName](intlchar.charname.md)— Отримати ім'я Unicode
-   [IntlChar::charType](intlchar.chartype.md)— Отримати головну категорію, до якої входить символ
-   [IntlChar::chr](intlchar.chr.md)— Отримати символ Unicode за його кодом
-   [IntlChar::digit](intlchar.digit.md)— Отримати десяткове число із символу Unicode із заданою основою
-   [IntlChar::enumCharNames](intlchar.enumcharnames.md)— Перелічує всі присвоєні символи Unicode у заданому діапазоні
-   [IntlChar::enumCharTypes](intlchar.enumchartypes.md)— Перелік послідовностей символів Unicode згрупованих за ними.
-   [IntlChar::foldCase](intlchar.foldcase.md)— Перетворює регістр заданого символу.
-   [IntlChar::forDigit](intlchar.fordigit.md)— Отримати символ, який представляє задане число в заданій основі
-   [IntlChar::getBidiPairedBracket](intlchar.getbidipairedbracket.md)— Отримати парну дужку для символу
-   [IntlChar::getBlockCode](intlchar.getblockcode.md)— Отримати блок розміщення символу Unicode
-   [IntlChar::getCombiningClass](intlchar.getcombiningclass.md)— Отримати комбінуючий клас для символу
-   [IntlChar::getFC\_NFKC\_Closure](intlchar.getfc-nfkc-closure.md) \- Отримати властивість FC\_NFKC\_Closure для символу
-   [IntlChar::getIntPropertyMaxValue](intlchar.getintpropertymaxvalue.md)— Отримати мінімальне значення для властивості Unicode
-   [IntlChar::getIntPropertyMinValue](intlchar.getintpropertyminvalue.md)— Отримати мінімальне значення для властивості Unicode
-   [IntlChar::getIntPropertyValue](intlchar.getintpropertyvalue.md)— Отримати значення властивості Unicode для символу
-   [IntlChar::getNumericValue](intlchar.getnumericvalue.md)— Отримати числову виставу для символу Unicode
-   [IntlChar::getPropertyEnum](intlchar.getpropertyenum.md)— Отримати значення константи властивості на його ім'я
-   [IntlChar::getPropertyName](intlchar.getpropertyname.md) \- Отримати Unicode ім'я властивості
-   [IntlChar::getPropertyValueEnum](intlchar.getpropertyvalueenum.md)— Повернути числовий ідентифікатор властивості на його ім'я
-   [IntlChar::getPropertyValueName](intlchar.getpropertyvaluename.md)— Отримати ім'я Unicode для значення властивості
-   [IntlChar::getUnicodeVersion](intlchar.getunicodeversion.md)— Отримати версію Unicode
-   [IntlChar::hasBinaryProperty](intlchar.hasbinaryproperty.md)— Перевірити бінарну властивість Unicode для символу
-   [IntlChar::isalnum](intlchar.isalnum.md)— Перевірити, чи є символ буквою чи цифрою
-   [IntlChar::isalpha](intlchar.isalpha.md)— Перевірити, чи є символ літерою
-   [IntlChar::isbase](intlchar.isbase.md)— Перевірити, чи символ є базовим
-   [IntlChar::isblank](intlchar.isblank.md) - Перевірити, чи є символ "порожнім" або "горизонтальним пропуском"
-   [IntlChar::iscntrl](intlchar.iscntrl.md)— Перевірити, чи є символ керуючим
-   [IntlChar::isdefined](intlchar.isdefined.md)— Перевірити, чи є символ.
-   [IntlChar::isdigit](intlchar.isdigit.md)— Перевірити, чи символ є цифрою
-   [IntlChar::isgraph](intlchar.isgraph.md)— Перевірити, чи є символом графічним символом
-   [IntlChar::isIDIgnorable](intlchar.isidignorable.md)— Перевірити, чи символ ігнорується
-   [IntlChar::isIDPart](intlchar.isidpart.md)— Перевірити, чи можна використовувати символ в ідентифікаторі
-   [IntlChar::isIDStart](intlchar.isidstart.md)— Перевірити, чи можна використовувати символ на початку ідентифікатора
-   [IntlChar::isISOControl](intlchar.isisocontrol.md)— Перевірити, чи є символ керуючим відповідно до ISO
-   [IntlChar::isJavaIDPart](intlchar.isjavaidpart.md)— Перевірити, чи символ допустимий в ідентифікаторі Java
-   [IntlChar::isJavaIDStart](intlchar.isjavaidstart.md)— Перевірити, чи символ може бути першим в ідентифікаторі Java
-   [IntlChar::isJavaSpaceChar](intlchar.isjavaspacechar.md)— Перевірити, чи є символ пробельним з точки зору Java
-   [IntlChar::islower](intlchar.islower.md)— Перевірити, чи у нижньому регістрі символ
-   [IntlChar::isMirrored](intlchar.ismirrored.md)— Перевірити, якщо символ має властивість Bidi\_Mirrored
-   [IntlChar::isprint](intlchar.isprint.md)— Перевіряє, чи символ відображається.
-   [IntlChar::ispunct](intlchar.ispunct.md)— Перевіряє, чи є символом пунктуації.
-   [IntlChar::isspace](intlchar.isspace.md)— Перевіряє, чи символ є пробельним.
-   [IntlChar::istitle](intlchar.istitle.md)— Перевірити, чи символ є титульним (Titlecase)
-   [IntlChar::isUAlphabetic](intlchar.isualphabetic.md)— Перевірити, чи встановлено символ символу Alphabetic
-   [IntlChar::isULowercase](intlchar.isulowercase.md)— Перевірити, чи символ є символом у нижньому регістрі
-   [IntlChar::isupper](intlchar.isupper.md) — Перевірити, чи входить символ у категорію "Lu" (літера у верхньому регістрі)
-   [IntlChar::isUUppercase](intlchar.isuuppercase.md)— Перевірити, чи символ є символом у верхньому регістрі
-   [IntlChar::isUWhiteSpace](intlchar.isuwhitespace.md)— Перевірити, чи має символ властивість White\_Space (пробіловий символ)
-   [IntlChar::isWhitespace](intlchar.iswhitespace.md)— Перевірити, чи символ є пробільним з точки зору ICU
-   [IntlChar::isxdigit](intlchar.isxdigit.md)— Перевіряє, чи кодова точка відноситься до шістнадцяткової цифри.
-   [IntlChar::ord](intlchar.ord.md)— Отримати код символ Unicode
-   [IntlChar::tolower](intlchar.tolower.md)— Перетворює символ Unicode на нижній регістр
-   [IntlChar::totitle](intlchar.totitle.md)— Перетворює символ Unicode на титульний регістр (titlecase)
-   [IntlChar::toupper](intlchar.toupper.md)— Перетворює символ Unicode у верхній регістр

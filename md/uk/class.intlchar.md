- [« idn_to_utf8](function.idn-to-utf8.md)
- [IntlChar::charAge »](intlchar.charage.md)

- [PHP Manual](index.md)
- [intl](book.intl.md)
- IntlChar

# IntlChar

(PHP 7, PHP 8)

## Вступ

**IntlChar** надає доступ до деякої кількості утилітарних
методи, які можна використовувати для доступу до інформації про символи
Unicode.

Імена методів та констант, представлені тут, близькі до імен та
методів бібліотеки ICU, що лежить нижче.

## Огляд класів

class **IntlChar** {

/\* Constants \*/

const string `UNICODE_VERSION` = 6.3;

const int `CODEPOINT_MIN` = 0;

const int `CODEPOINT_MAX` = 1114111;

const float `NO_NUMERIC_VALUE` = -123456789;

const int `PROPERTY_ALPHABETIC` = 0;

const int `PROPERTY_BINARY_START` = 0;

const int `PROPERTY_ASCII_HEX_DIGIT` = 1;

const int `PROPERTY_BIDI_CONTROL` = 2;

const int `PROPERTY_BIDI_MIRRORED` = 3;

const int `PROPERTY_DASH` = 4;

const int `PROPERTY_DEFAULT_IGNORABLE_CODE_POINT` = 5;

const int `PROPERTY_DEPRECATED` = 6;

const int `PROPERTY_DIACRITIC` = 7;

const int `PROPERTY_EXTENDER` = 8;

const int `PROPERTY_FULL_COMPOSITION_EXCLUSION` = 9;

const int `PROPERTY_GRAPHEME_BASE` = 10;

const int `PROPERTY_GRAPHEME_EXTEND` = 11;

const int `PROPERTY_GRAPHEME_LINK` = 12;

const int `PROPERTY_HEX_DIGIT` = 13;

const int `PROPERTY_HYPHEN` = 14;

const int `PROPERTY_ID_CONTINUE` = 15;

const int `PROPERTY_ID_START` = 16;

const int `PROPERTY_IDEOGRAPHIC` = 17;

const int `PROPERTY_IDS_BINARY_OPERATOR` = 18;

const int `PROPERTY_IDS_TRINARY_OPERATOR` = 19;

const int `PROPERTY_JOIN_CONTROL` = 20;

const int `PROPERTY_LOGICAL_ORDER_EXCEPTION` = 21;

const int `PROPERTY_LOWERCASE` = 22;

const int `PROPERTY_MATH` = 23;

const int `PROPERTY_NONCHARACTER_CODE_POINT` = 24;

const int `PROPERTY_QUOTATION_MARK` = 25;

const int `PROPERTY_RADICAL` = 26;

const int `PROPERTY_SOFT_DOTTED` = 27;

const int `PROPERTY_TERMINAL_PUNCTUATION` = 28;

const int `PROPERTY_UNIFIED_IDEOGRAPH` = 29;

const int `PROPERTY_UPPERCASE` = 30;

const int `PROPERTY_WHITE_SPACE` = 31;

const int `PROPERTY_XID_CONTINUE` = 32;

const int `PROPERTY_XID_START` = 33;

const int `PROPERTY_CASE_SENSITIVE` = 34;

const int `PROPERTY_S_TERM` = 35;

const int `PROPERTY_VARIATION_SELECTOR` = 36;

const int `PROPERTY_NFD_INERT` = 37;

const int `PROPERTY_NFKD_INERT` = 38;

const int `PROPERTY_NFC_INERT` = 39;

const int `PROPERTY_NFKC_INERT` = 40;

const int `PROPERTY_SEGMENT_STARTER` = 41;

const int `PROPERTY_PATTERN_SYNTAX` = 42;

const int `PROPERTY_PATTERN_WHITE_SPACE` = 43;

const int `PROPERTY_POSIX_ALNUM` = 44;

const int `PROPERTY_POSIX_BLANK` = 45;

const int `PROPERTY_POSIX_GRAPH` = 46;

const int `PROPERTY_POSIX_PRINT` = 47;

const int `PROPERTY_POSIX_XDIGIT` = 48;

const int `PROPERTY_CASED` = 49;

const int `PROPERTY_CASE_IGNORABLE` = 50;

const int `PROPERTY_CHANGES_WHEN_LOWERCASED` = 51;

const int `PROPERTY_CHANGES_WHEN_UPPERCASED` = 52;

const int `PROPERTY_CHANGES_WHEN_TITLECASED` = 53;

const int `PROPERTY_CHANGES_WHEN_CASEFOLDED` = 54;

const int `PROPERTY_CHANGES_WHEN_CASEMAPPED` = 55;

const int `PROPERTY_CHANGES_WHEN_NFKC_CASEFOLDED` = 56;

const int `PROPERTY_BINARY_LIMIT` = 57;

const int `PROPERTY_BIDI_CLASS` = 4096;

const int `PROPERTY_INT_START` = 4096;

const int `PROPERTY_BLOCK` = 4097;

const int `PROPERTY_CANONICAL_COMBINING_CLASS` = 4098;

const int `PROPERTY_DECOMPOSITION_TYPE` = 4099;

const int `PROPERTY_EAST_ASIAN_WIDTH` = 4100;

const int `PROPERTY_GENERAL_CATEGORY` = 4101;

const int `PROPERTY_JOINING_GROUP` = 4102;

const int `PROPERTY_JOINING_TYPE` = 4103;

const int `PROPERTY_LINE_BREAK` = 4104;

const int `PROPERTY_NUMERIC_TYPE` = 4105;

const int `PROPERTY_SCRIPT` = 4106;

const int `PROPERTY_HANGUL_SYLLABLE_TYPE` = 4107;

const int `PROPERTY_NFD_QUICK_CHECK` = 4108;

const int `PROPERTY_NFKD_QUICK_CHECK` = 4109;

const int `PROPERTY_NFC_QUICK_CHECK` = 4110;

const int `PROPERTY_NFKC_QUICK_CHECK` = 4111;

const int `PROPERTY_LEAD_CANONICAL_COMBINING_CLASS` = 4112;

const int `PROPERTY_TRAIL_CANONICAL_COMBINING_CLASS` = 4113;

const int `PROPERTY_GRAPHEME_CLUSTER_BREAK` = 4114;

const int `PROPERTY_SENTENCE_BREAK` = 4115;

const int `PROPERTY_WORD_BREAK` = 4116;

const int `PROPERTY_BIDI_PAIRED_BRACKET_TYPE` = 4117;

const int `PROPERTY_INT_LIMIT` = 4118;

const int `PROPERTY_GENERAL_CATEGORY_MASK` = 8192;

const int `PROPERTY_MASK_START` = 8192;

const int `PROPERTY_MASK_LIMIT` = 8193;

const int `PROPERTY_NUMERIC_VALUE` = 12288;

const int `PROPERTY_DOUBLE_START` = 12288;

const int `PROPERTY_DOUBLE_LIMIT` = 12289;

const int `PROPERTY_AGE` = 16384;

const int `PROPERTY_STRING_START` = 16384;

const int `PROPERTY_BIDI_MIRRORING_GLYPH` = 16385;

const int `PROPERTY_CASE_FOLDING` = 16386;

const int `PROPERTY_ISO_COMMENT` = 16387;

const int `PROPERTY_LOWERCASE_MAPPING` = 16388;

const int `PROPERTY_NAME` = 16389;

const int `PROPERTY_SIMPLE_CASE_FOLDING` = 16390;

const int `PROPERTY_SIMPLE_LOWERCASE_MAPPING` = 16391;

const int `PROPERTY_SIMPLE_TITLECASE_MAPPING` = 16392;

const int `PROPERTY_SIMPLE_UPPERCASE_MAPPING` = 16393;

const int `PROPERTY_TITLECASE_MAPPING` = 16394;

const int `PROPERTY_UNICODE_1_NAME` = 16395;

const int `PROPERTY_UPPERCASE_MAPPING` = 16396;

const int `PROPERTY_BIDI_PAIRED_BRACKET` = 16397;

const int `PROPERTY_STRING_LIMIT` = 16398;

const int `PROPERTY_SCRIPT_EXTENSIONS` = 28672;

const int `PROPERTY_OTHER_PROPERTY_START` = 28672;

const int `PROPERTY_OTHER_PROPERTY_LIMIT` = 28673;

const int `PROPERTY_INVALID_CODE` = -1;

const int `CHAR_CATEGORY_UNASSIGNED` = 0;

const int `CHAR_CATEGORY_GENERAL_OTHER_TYPES` = 0;

const int `CHAR_CATEGORY_UPPERCASE_LETTER` = 1;

const int `CHAR_CATEGORY_LOWERCASE_LETTER` = 2;

const int `CHAR_CATEGORY_TITLECASE_LETTER` = 3;

const int `CHAR_CATEGORY_MODIFIER_LETTER` = 4;

const int `CHAR_CATEGORY_OTHER_LETTER` = 5;

const int `CHAR_CATEGORY_NON_SPACING_MARK` = 6;

const int `CHAR_CATEGORY_ENCLOSING_MARK` = 7;

const int `CHAR_CATEGORY_COMBINING_SPACING_MARK` = 8;

const int `CHAR_CATEGORY_DECIMAL_DIGIT_NUMBER` = 9;

const int `CHAR_CATEGORY_LETTER_NUMBER` = 10;

const int `CHAR_CATEGORY_OTHER_NUMBER` = 11;

const int `CHAR_CATEGORY_SPACE_SEPARATOR` = 12;

const int `CHAR_CATEGORY_LINE_SEPARATOR` = 13;

const int `CHAR_CATEGORY_PARAGRAPH_SEPARATOR` = 14;

const int `CHAR_CATEGORY_CONTROL_CHAR` = 15;

const int `CHAR_CATEGORY_FORMAT_CHAR` = 16;

const int `CHAR_CATEGORY_PRIVATE_USE_CHAR` = 17;

const int `CHAR_CATEGORY_SURROGATE` = 18;

const int `CHAR_CATEGORY_DASH_PUNCTUATION` = 19;

const int `CHAR_CATEGORY_START_PUNCTUATION` = 20;

const int `CHAR_CATEGORY_END_PUNCTUATION` = 21;

const int `CHAR_CATEGORY_CONNECTOR_PUNCTUATION` = 22;

const int `CHAR_CATEGORY_OTHER_PUNCTUATION` = 23;

const int `CHAR_CATEGORY_MATH_SYMBOL` = 24;

const int `CHAR_CATEGORY_CURRENCY_SYMBOL` = 25;

const int `CHAR_CATEGORY_MODIFIER_SYMBOL` = 26;

const int `CHAR_CATEGORY_OTHER_SYMBOL` = 27;

const int `CHAR_CATEGORY_INITIAL_PUNCTUATION` = 28;

const int `CHAR_CATEGORY_FINAL_PUNCTUATION` = 29;

const int `CHAR_CATEGORY_CHAR_CATEGORY_COUNT` = 30;

const int `CHAR_DIRECTION_LEFT_TO_RIGHT` = 0;

const int `CHAR_DIRECTION_RIGHT_TO_LEFT` = 1;

const int `CHAR_DIRECTION_EUROPEAN_NUMBER` = 2;

const int `CHAR_DIRECTION_EUROPEAN_NUMBER_SEPARATOR` = 3;

const int `CHAR_DIRECTION_EUROPEAN_NUMBER_TERMINATOR` = 4;

const int `CHAR_DIRECTION_ARABIC_NUMBER` = 5;

const int `CHAR_DIRECTION_COMMON_NUMBER_SEPARATOR` = 6;

const int `CHAR_DIRECTION_BLOCK_SEPARATOR` = 7;

const int `CHAR_DIRECTION_SEGMENT_SEPARATOR` = 8;

const int `CHAR_DIRECTION_WHITE_SPACE_NEUTRAL` = 9;

const int `CHAR_DIRECTION_OTHER_NEUTRAL` = 10;

const int `CHAR_DIRECTION_LEFT_TO_RIGHT_EMBEDDING` = 11;

const int `CHAR_DIRECTION_LEFT_TO_RIGHT_OVERRIDE` = 12;

const int `CHAR_DIRECTION_RIGHT_TO_LEFT_ARABIC` = 13;

const int `CHAR_DIRECTION_RIGHT_TO_LEFT_EMBEDDING` = 14;

const int `CHAR_DIRECTION_RIGHT_TO_LEFT_OVERRIDE` = 15;

const int `CHAR_DIRECTION_POP_DIRECTIONAL_FORMAT` = 16;

const int `CHAR_DIRECTION_DIR_NON_SPACING_MARK` = 17;

const int `CHAR_DIRECTION_BOUNDARY_NEUTRAL` = 18;

const int `CHAR_DIRECTION_FIRST_STRONG_ISOLATE` = 19;

const int `CHAR_DIRECTION_LEFT_TO_RIGHT_ISOLATE` = 20;

const int `CHAR_DIRECTION_RIGHT_TO_LEFT_ISOLATE` = 21;

const int `CHAR_DIRECTION_POP_DIRECTIONAL_ISOLATE` = 22;

const int `CHAR_DIRECTION_CHAR_DIRECTION_COUNT` = 23;

const int `BLOCK_CODE_NO_BLOCK` = 0;

const int `BLOCK_CODE_BASIC_LATIN` = 1;

const int `BLOCK_CODE_LATIN_1_SUPPLEMENT` = 2;

const int `BLOCK_CODE_LATIN_EXTENDED_A` = 3;

const int `BLOCK_CODE_LATIN_EXTENDED_B` = 4;

const int `BLOCK_CODE_IPA_EXTENSIONS` = 5;

const int `BLOCK_CODE_SPACING_MODIFIER_LETTERS` = 6;

const int `BLOCK_CODE_COMBINING_DIACRITICAL_MARKS` = 7;

const int `BLOCK_CODE_GREEK` = 8;

const int `BLOCK_CODE_CYRILLIC` = 9;

const int `BLOCK_CODE_ARMENIAN` = 10;

const int `BLOCK_CODE_HEBREW` = 11;

const int `BLOCK_CODE_ARABIC` = 12;

const int `BLOCK_CODE_SYRIAC` = 13;

const int `BLOCK_CODE_THAANA` = 14;

const int `BLOCK_CODE_DEVANAGARI` = 15;

const int `BLOCK_CODE_BENGALI` = 16;

const int `BLOCK_CODE_GURMUKHI` = 17;

const int `BLOCK_CODE_GUJARATI` = 18;

const int `BLOCK_CODE_ORIYA` = 19;

const int `BLOCK_CODE_TAMIL` = 20;

const int `BLOCK_CODE_TELUGU` = 21;

const int `BLOCK_CODE_KANNADA` = 22;

const int `BLOCK_CODE_MALAYALAM` = 23;

const int `BLOCK_CODE_SINHALA` = 24;

const int `BLOCK_CODE_THAI` = 25;

const int `BLOCK_CODE_LAO` = 26;

const int `BLOCK_CODE_TIBETAN` = 27;

const int `BLOCK_CODE_MYANMAR` = 28;

const int `BLOCK_CODE_GEORGIAN` = 29;

const int `BLOCK_CODE_HANGUL_JAMO` = 30;

const int `BLOCK_CODE_ETHIOPIC` = 31;

const int `BLOCK_CODE_CHEROKEE` = 32;

const int `BLOCK_CODE_UNIFIED_CANADIAN_ABORIGINAL_SYLLABICS` = 33;

const int `BLOCK_CODE_OGHAM` = 34;

const int `BLOCK_CODE_RUNIC` = 35;

const int `BLOCK_CODE_KHMER` = 36;

const int `BLOCK_CODE_MONGOLIAN` = 37;

const int `BLOCK_CODE_LATIN_EXTENDED_ADDITIONAL` = 38;

const int `BLOCK_CODE_GREEK_EXTENDED` = 39;

const int `BLOCK_CODE_GENERAL_PUNCTUATION` = 40;

const int `BLOCK_CODE_SUPERSCRIPTS_AND_SUBSCRIPTS` = 41;

const int `BLOCK_CODE_CURRENCY_SYMBOLS` = 42;

const int `BLOCK_CODE_COMBINING_MARKS_FOR_SYMBOLS` = 43;

const int `BLOCK_CODE_LETTERLIKE_SYMBOLS` = 44;

const int `BLOCK_CODE_NUMBER_FORMS` = 45;

const int `BLOCK_CODE_ARROWS` = 46;

const int `BLOCK_CODE_MATHEMATICAL_OPERATORS` = 47;

const int `BLOCK_CODE_MISCELLANEOUS_TECHNICAL` = 48;

const int `BLOCK_CODE_CONTROL_PICTURES` = 49;

const int `BLOCK_CODE_OPTICAL_CHARACTER_RECOGNITION` = 50;

const int `BLOCK_CODE_ENCLOSED_ALPHANUMERICS` = 51;

const int `BLOCK_CODE_BOX_DRAWING` = 52;

const int `BLOCK_CODE_BLOCK_ELEMENTS` = 53;

const int `BLOCK_CODE_GEOMETRIC_SHAPES` = 54;

const int `BLOCK_CODE_MISCELLANEOUS_SYMBOLS` = 55;

const int `BLOCK_CODE_DINGBATS` = 56;

const int `BLOCK_CODE_BRAILLE_PATTERNS` = 57;

const int `BLOCK_CODE_CJK_RADICALS_SUPPLEMENT` = 58;

const int `BLOCK_CODE_KANGXI_RADICALS` = 59;

const int `BLOCK_CODE_IDEOGRAPHIC_DESCRIPTION_CHARACTERS` = 60;

const int `BLOCK_CODE_CJK_SYMBOLS_AND_PUNCTUATION` = 61;

const int `BLOCK_CODE_HIRAGANA` = 62;

const int `BLOCK_CODE_KATAKANA` = 63;

const int `BLOCK_CODE_BOPOMOFO` = 64;

const int `BLOCK_CODE_HANGUL_COMPATIBILITY_JAMO` = 65;

const int `BLOCK_CODE_KANBUN` = 66;

const int `BLOCK_CODE_BOPOMOFO_EXTENDED` = 67;

const int `BLOCK_CODE_ENCLOSED_CJK_LETTERS_AND_MONTHS` = 68;

const int `BLOCK_CODE_CJK_COMPATIBILITY` = 69;

const int `BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_A` = 70;

const int `BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS` = 71;

const int `BLOCK_CODE_YI_SYLLABLES` = 72;

const int `BLOCK_CODE_YI_RADICALS` = 73;

const int `BLOCK_CODE_HANGUL_SYLLABLES` = 74;

const int `BLOCK_CODE_HIGH_SURROGATES` = 75;

const int `BLOCK_CODE_HIGH_PRIVATE_USE_SURROGATES` = 76;

const int `BLOCK_CODE_LOW_SURROGATES` = 77;

const int `BLOCK_CODE_PRIVATE_USE_AREA` = 78;

const int `BLOCK_CODE_PRIVATE_USE` = 78;

const int `BLOCK_CODE_CJK_COMPATIBILITY_IDEOGRAPHS` = 79;

const int `BLOCK_CODE_ALPHABETIC_PRESENTATION_FORMS` = 80;

const int `BLOCK_CODE_ARABIC_PRESENTATION_FORMS_A` = 81;

const int `BLOCK_CODE_COMBINING_HALF_MARKS` = 82;

const int `BLOCK_CODE_CJK_COMPATIBILITY_FORMS` = 83;

const int `BLOCK_CODE_SMALL_FORM_VARIANTS` = 84;

const int `BLOCK_CODE_ARABIC_PRESENTATION_FORMS_B` = 85;

const int `BLOCK_CODE_SPECIALS` = 86;

const int `BLOCK_CODE_HALFWIDTH_AND_FULLWIDTH_FORMS` = 87;

const int `BLOCK_CODE_OLD_ITALIC` = 88;

const int `BLOCK_CODE_GOTHIC` = 89;

const int `BLOCK_CODE_DESERET` = 90;

const int `BLOCK_CODE_BYZANTINE_MUSICAL_SYMBOLS` = 91;

const int `BLOCK_CODE_MUSICAL_SYMBOLS` = 92;

const int `BLOCK_CODE_MATHEMATICAL_ALPHANUMERIC_SYMBOLS` = 93;

const int `BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_B` = 94;

const int `BLOCK_CODE_CJK_COMPATIBILITY_IDEOGRAPHS_SUPPLEMENT` = 95;

const int `BLOCK_CODE_TAGS` = 96;

const int `BLOCK_CODE_CYRILLIC_SUPPLEMENT` = 97;

const int `BLOCK_CODE_CYRILLIC_SUPPLEMENTARY` = 97;

const int `BLOCK_CODE_TAGALOG` = 98;

const int `BLOCK_CODE_HANUNOO` = 99;

const int `BLOCK_CODE_BUHID` = 100;

const int `BLOCK_CODE_TAGBANWA` = 101;

const int `BLOCK_CODE_MISCELLANEOUS_MATHEMATICAL_SYMBOLS_A` = 102;

const int `BLOCK_CODE_SUPPLEMENTAL_ARROWS_A` = 103;

const int `BLOCK_CODE_SUPPLEMENTAL_ARROWS_B` = 104;

const int `BLOCK_CODE_MISCELLANEOUS_MATHEMATICAL_SYMBOLS_B` = 105;

const int `BLOCK_CODE_SUPPLEMENTAL_MATHEMATICAL_OPERATORS` = 106;

const int `BLOCK_CODE_KATAKANA_PHONETIC_EXTENSIONS` = 107;

const int `BLOCK_CODE_VARIATION_SELECTORS` = 108;

const int `BLOCK_CODE_SUPPLEMENTARY_PRIVATE_USE_AREA_A` = 109;

const int `BLOCK_CODE_SUPPLEMENTARY_PRIVATE_USE_AREA_B` = 110;

const int `BLOCK_CODE_LIMBU` = 111;

const int `BLOCK_CODE_TAI_LE` = 112;

const int `BLOCK_CODE_KHMER_SYMBOLS` = 113;

const int `BLOCK_CODE_PHONETIC_EXTENSIONS` = 114;

const int `BLOCK_CODE_MISCELLANEOUS_SYMBOLS_AND_ARROWS` = 115;

const int `BLOCK_CODE_YIJING_HEXAGRAM_SYMBOLS` = 116;

const int `BLOCK_CODE_LINEAR_B_SYLLABARY` = 117;

const int `BLOCK_CODE_LINEAR_B_IDEOGRAMS` = 118;

const int `BLOCK_CODE_AEGEAN_NUMBERS` = 119;

const int `BLOCK_CODE_UGARITIC` = 120;

const int `BLOCK_CODE_SHAVIAN` = 121;

const int `BLOCK_CODE_OSMANYA` = 122;

const int `BLOCK_CODE_CYPRIOT_SYLLABARY` = 123;

const int `BLOCK_CODE_TAI_XUAN_JING_SYMBOLS` = 124;

const int `BLOCK_CODE_VARIATION_SELECTORS_SUPPLEMENT` = 125;

const int `BLOCK_CODE_ANCIENT_GREEK_MUSICAL_NOTATION` = 126;

const int `BLOCK_CODE_ANCIENT_GREEK_NUMBERS` = 127;

const int `BLOCK_CODE_ARABIC_SUPPLEMENT` = 128;

const int `BLOCK_CODE_BUGINESE` = 129;

const int `BLOCK_CODE_CJK_STROKES` = 130;

const int `BLOCK_CODE_COMBINING_DIACRITICAL_MARKS_SUPPLEMENT` = 131;

const int `BLOCK_CODE_COPTIC` = 132;

const int `BLOCK_CODE_ETHIOPIC_EXTENDED` = 133;

const int `BLOCK_CODE_ETHIOPIC_SUPPLEMENT` = 134;

const int `BLOCK_CODE_GEORGIAN_SUPPLEMENT` = 135;

const int `BLOCK_CODE_GLAGOLITIC` = 136;

const int `BLOCK_CODE_KHAROSHTHI` = 137;

const int `BLOCK_CODE_MODIFIER_TONE_LETTERS` = 138;

const int `BLOCK_CODE_NEW_TAI_LUE` = 139;

const int `BLOCK_CODE_OLD_PERSIAN` = 140;

const int `BLOCK_CODE_PHONETIC_EXTENSIONS_SUPPLEMENT` = 141;

const int `BLOCK_CODE_SUPPLEMENTAL_PUNCTUATION` = 142;

const int `BLOCK_CODE_SYLOTI_NAGRI` = 143;

const int `BLOCK_CODE_TIFINAGH` = 144;

const int `BLOCK_CODE_VERTICAL_FORMS` = 145;

const int `BLOCK_CODE_NKO` = 146;

const int `BLOCK_CODE_BALINESE` = 147;

const int `BLOCK_CODE_LATIN_EXTENDED_C` = 148;

const int `BLOCK_CODE_LATIN_EXTENDED_D` = 149;

const int `BLOCK_CODE_PHAGS_PA` = 150;

const int `BLOCK_CODE_PHOENICIAN` = 151;

const int `BLOCK_CODE_CUNEIFORM` = 152;

const int `BLOCK_CODE_CUNEIFORM_NUMBERS_AND_PUNCTUATION` = 153;

const int `BLOCK_CODE_COUNTING_ROD_NUMERALS` = 154;

const int `BLOCK_CODE_SUNDANESE` = 155;

const int `BLOCK_CODE_LEPCHA` = 156;

const int `BLOCK_CODE_OL_CHIKI` = 157;

const int `BLOCK_CODE_CYRILLIC_EXTENDED_A` = 158;

const int `BLOCK_CODE_VAI` = 159;

const int `BLOCK_CODE_CYRILLIC_EXTENDED_B` = 160;

const int `BLOCK_CODE_SAURASHTRA` = 161;

const int `BLOCK_CODE_KAYAH_LI` = 162;

const int `BLOCK_CODE_REJANG` = 163;

const int `BLOCK_CODE_CHAM` = 164;

const int `BLOCK_CODE_ANCIENT_SYMBOLS` = 165;

const int `BLOCK_CODE_PHAISTOS_DISC` = 166;

const int `BLOCK_CODE_LYCIAN` = 167;

const int `BLOCK_CODE_CARIAN` = 168;

const int `BLOCK_CODE_LYDIAN` = 169;

const int `BLOCK_CODE_MAHJONG_TILES` = 170;

const int `BLOCK_CODE_DOMINO_TILES` = 171;

const int `BLOCK_CODE_SAMARITAN` = 172;

const int `BLOCK_CODE_UNIFIED_CANADIAN_ABORIGINAL_SYLLABICS_EXTENDED` =
173;

const int `BLOCK_CODE_TAI_THAM` = 174;

const int `BLOCK_CODE_VEDIC_EXTENSIONS` = 175;

const int `BLOCK_CODE_LISU` = 176;

const int `BLOCK_CODE_BAMUM` = 177;

const int `BLOCK_CODE_COMMON_INDIC_NUMBER_FORMS` = 178;

const int `BLOCK_CODE_DEVANAGARI_EXTENDED` = 179;

const int `BLOCK_CODE_HANGUL_JAMO_EXTENDED_A` = 180;

const int `BLOCK_CODE_JAVANESE` = 181;

const int `BLOCK_CODE_MYANMAR_EXTENDED_A` = 182;

const int `BLOCK_CODE_TAI_VIET` = 183;

const int `BLOCK_CODE_MEETEI_MAYEK` = 184;

const int `BLOCK_CODE_HANGUL_JAMO_EXTENDED_B` = 185;

const int `BLOCK_CODE_IMPERIAL_ARAMAIC` = 186;

const int `BLOCK_CODE_OLD_SOUTH_ARABIAN` = 187;

const int `BLOCK_CODE_AVESTAN` = 188;

const int `BLOCK_CODE_INSCRIPTIONAL_PARTHIAN` = 189;

const int `BLOCK_CODE_INSCRIPTIONAL_PAHLAVI` = 190;

const int `BLOCK_CODE_OLD_TURKIC` = 191;

const int `BLOCK_CODE_RUMI_NUMERAL_SYMBOLS` = 192;

const int `BLOCK_CODE_KAITHI` = 193;

const int `BLOCK_CODE_EGYPTIAN_HIEROGLYPHS` = 194;

const int `BLOCK_CODE_ENCLOSED_ALPHANUMERIC_SUPPLEMENT` = 195;

const int `BLOCK_CODE_ENCLOSED_IDEOGRAPHIC_SUPPLEMENT` = 196;

const int `BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_C` = 197;

const int `BLOCK_CODE_MANDAIC` = 198;

const int `BLOCK_CODE_BATAK` = 199;

const int `BLOCK_CODE_ETHIOPIC_EXTENDED_A` = 200;

const int `BLOCK_CODE_BRAHMI` = 201;

const int `BLOCK_CODE_BAMUM_SUPPLEMENT` = 202;

const int `BLOCK_CODE_KANA_SUPPLEMENT` = 203;

const int `BLOCK_CODE_PLAYING_CARDS` = 204;

const int `BLOCK_CODE_MISCELLANEOUS_SYMBOLS_AND_PICTOGRAPHS` = 205;

const int `BLOCK_CODE_EMOTICONS` = 206;

const int `BLOCK_CODE_TRANSPORT_AND_MAP_SYMBOLS` = 207;

const int `BLOCK_CODE_ALCHEMICAL_SYMBOLS` = 208;

const int `BLOCK_CODE_CJK_UNIFIED_IDEOGRAPHS_EXTENSION_D` = 209;

const int `BLOCK_CODE_ARABIC_EXTENDED_A` = 210;

const int `BLOCK_CODE_ARABIC_MATHEMATICAL_ALPHABETIC_SYMBOLS` = 211;

const int `BLOCK_CODE_CHAKMA` = 212;

const int `BLOCK_CODE_MEETEI_MAYEK_EXTENSIONS` = 213;

const int `BLOCK_CODE_MEROITIC_CURSIVE` = 214;

const int `BLOCK_CODE_MEROITIC_HIEROGLYPHS` = 215;

const int `BLOCK_CODE_MIAO` = 216;

const int `BLOCK_CODE_SHARADA` = 217;

const int `BLOCK_CODE_SORA_SOMPENG` = 218;

const int `BLOCK_CODE_SUNDANESE_SUPPLEMENT` = 219;

const int `BLOCK_CODE_TAKRI` = 220;

const int `BLOCK_CODE_COUNT` = 221;

const int `BLOCK_CODE_INVALID_CODE` = -1;

const int `BPT_NONE` = 0;

const int `BPT_OPEN` = 1;

const int `BPT_CLOSE` = 2;

const int `BPT_COUNT` = 3;

const int `EA_NEUTRAL` = 0;

const int `EA_AMBIGUOUS` = 1;

const int `EA_HALFWIDTH` = 2;

const int `EA_FULLWIDTH` = 3;

const int `EA_NARROW` = 4;

const int `EA_WIDE` = 5;

const int `EA_COUNT` = 6;

const int `UNICODE_CHAR_NAME` = 0;

const int `UNICODE_10_CHAR_NAME` = 1;

const int `EXTENDED_CHAR_NAME` = 2;

const int `CHAR_NAME_ALIAS` = 3;

const int `CHAR_NAME_CHOICE_COUNT` = 4;

const int `SHORT_PROPERTY_NAME` = 0;

const int `LONG_PROPERTY_NAME` = 1;

const int `PROPERTY_NAME_CHOICE_COUNT` = 2;

const int `DT_NONE` = 0;

const int `DT_CANONICAL` = 1;

const int `DT_COMPAT` = 2;

const int `DT_CIRCLE` = 3;

const int `DT_FINAL` = 4;

const int `DT_FONT` = 5;

const int `DT_FRACTION` = 6;

const int `DT_INITIAL` = 7;

const int `DT_ISOLATED` = 8;

const int `DT_MEDIAL` = 9;

const int `DT_NARROW` = 10;

const int `DT_NOBREAK` = 11;

const int `DT_SMALL` = 12;

const int `DT_SQUARE` = 13;

const int `DT_SUB` = 14;

const int `DT_SUPER` = 15;

const int `DT_VERTICAL` = 16;

const int `DT_WIDE` = 17;

const int `DT_COUNT` = 18;

const int `JT_NON_JOINING` = 0;

const int `JT_JOIN_CAUSING` = 1;

const int `JT_DUAL_JOINING` = 2;

const int `JT_LEFT_JOINING` = 3;

const int `JT_RIGHT_JOINING` = 4;

const int `JT_TRANSPARENT` = 5;

const int `JT_COUNT` = 6;

const int `JG_NO_JOINING_GROUP` = 0;

const int `JG_AIN` = 1;

const int `JG_ALAPH` = 2;

const int `JG_ALEF` = 3;

const int `JG_BEH` = 4;

const int `JG_BETH` = 5;

const int `JG_DAL` = 6;

const int `JG_DALATH_RISH` = 7;

const int `JG_E` = 8;

const int `JG_FEH` = 9;

const int `JG_FINAL_SEMKATH` = 10;

const int `JG_GAF` = 11;

const int `JG_GAMAL` = 12;

const int `JG_HAH` = 13;

const int `JG_TEH_MARBUTA_GOAL` = 14;

const int `JG_HAMZA_ON_HEH_GOAL` = 14;

const int `JG_HE` = 15;

const int `JG_HEH` = 16;

const int `JG_HEH_GOAL` = 17;

const int `JG_HETH` = 18;

const int `JG_KAF` = 19;

const int `JG_KAPH` = 20;

const int `JG_KNOTTED_HEH` = 21;

const int `JG_LAM` = 22;

const int `JG_LAMADH` = 23;

const int `JG_MEEM` = 24;

const int `JG_MIM` = 25;

const int `JG_NOON` = 26;

const int `JG_NUN` = 27;

const int `JG_PE` = 28;

const int `JG_QAF` = 29;

const int `JG_QAPH` = 30;

const int `JG_REH` = 31;

const int `JG_REVERSED_PE` = 32;

const int `JG_SAD` = 33;

const int `JG_SADHE` = 34;

const int `JG_SEEN` = 35;

const int `JG_SEMKATH` = 36;

const int `JG_SHIN` = 37;

const int `JG_SWASH_KAF` = 38;

const int `JG_SYRIAC_WAW` = 39;

const int `JG_TAH` = 40;

const int `JG_TAW` = 41;

const int `JG_TEH_MARBUTA` = 42;

const int `JG_TETH` = 43;

const int `JG_WAW` = 44;

const int `JG_YEH` = 45;

const int `JG_YEH_BARREE` = 46;

const int `JG_YEH_WITH_TAIL` = 47;

const int `JG_YUDH` = 48;

const int `JG_YUDH_HE` = 49;

const int `JG_ZAIN` = 50;

const int `JG_FE` = 51;

const int `JG_KHAPH` = 52;

const int `JG_ZHAIN` = 53;

const int `JG_BURUSHASKI_YEH_BARREE` = 54;

const int `JG_FARSI_YEH` = 55;

const int `JG_NYA` = 56;

const int `JG_ROHINGYA_YEH` = 57;

const int `JG_COUNT` = 58;

const int `GCB_OTHER` = 0;

const int `GCB_CONTROL` = 1;

const int `GCB_CR` = 2;

const int `GCB_EXTEND` = 3;

const int `GCB_L` = 4;

const int `GCB_LF` = 5;

const int `GCB_LV` = 6;

const int `GCB_LVT` = 7;

const int `GCB_T` = 8;

const int `GCB_V` = 9;

const int `GCB_SPACING_MARK` = 10;

const int `GCB_PREPEND` = 11;

const int `GCB_REGIONAL_INDICATOR` = 12;

const int `GCB_COUNT` = 13;

const int `WB_OTHER` = 0;

const int `WB_ALETTER` = 1;

const int `WB_FORMAT` = 2;

const int `WB_KATAKANA` = 3;

const int `WB_MIDLETTER` = 4;

const int `WB_MIDNUM` = 5;

const int `WB_NUMERIC` = 6;

const int `WB_EXTENDNUMLET` = 7;

const int `WB_CR` = 8;

const int `WB_EXTEND` = 9;

const int `WB_LF` = 10;

const int `WB_MIDNUMLET` = 11;

const int `WB_NEWLINE` = 12;

const int `WB_REGIONAL_INDICATOR` = 13;

const int `WB_HEBREW_LETTER` = 14;

const int `WB_SINGLE_QUOTE` = 15;

const int `WB_DOUBLE_QUOTE` = 16;

const int `WB_COUNT` = 17;

const int `SB_OTHER` = 0;

const int `SB_ATERM` = 1;

const int `SB_CLOSE` = 2;

const int `SB_FORMAT` = 3;

const int `SB_LOWER` = 4;

const int `SB_NUMERIC` = 5;

const int `SB_OLETTER` = 6;

const int `SB_SEP` = 7;

const int `SB_SP` = 8;

const int `SB_STERM` = 9;

const int `SB_UPPER` = 10;

const int `SB_CR` = 11;

const int `SB_EXTEND` = 12;

const int `SB_LF` = 13;

const int `SB_SCONTINUE` = 14;

const int `SB_COUNT` = 15;

const int `LB_UNKNOWN` = 0;

const int `LB_AMBIGUOUS` = 1;

const int `LB_ALPHABETIC` = 2;

const int `LB_BREAK_BOTH` = 3;

const int `LB_BREAK_AFTER` = 4;

const int `LB_BREAK_BEFORE` = 5;

const int `LB_MANDATORY_BREAK` = 6;

const int `LB_CONTINGENT_BREAK` = 7;

const int `LB_CLOSE_PUNCTUATION` = 8;

const int `LB_COMBINING_MARK` = 9;

const int `LB_CARRIAGE_RETURN` = 10;

const int `LB_EXCLAMATION` = 11;

const int `LB_GLUE` = 12;

const int `LB_HYPHEN` = 13;

const int `LB_IDEOGRAPHIC` = 14;

const int `LB_INSEPARABLE` = 15;

const int `LB_INSEPERABLE` = 15;

const int `LB_INFIX_NUMERIC` = 16;

const int `LB_LINE_FEED` = 17;

const int `LB_NONSTARTER` = 18;

const int `LB_NUMERIC` = 19;

const int `LB_OPEN_PUNCTUATION` = 20;

const int `LB_POSTFIX_NUMERIC` = 21;

const int `LB_PREFIX_NUMERIC` = 22;

const int `LB_QUOTATION` = 23;

const int `LB_COMPLEX_CONTEXT` = 24;

const int `LB_SURROGATE` = 25;

const int `LB_SPACE` = 26;

const int `LB_BREAK_SYMBOLS` = 27;

const int `LB_ZWSPACE` = 28;

const int `LB_NEXT_LINE` = 29;

const int `LB_WORD_JOINER` = 30;

const int `LB_H2` = 31;

const int `LB_H3` = 32;

const int `LB_JL` = 33;

const int `LB_JT` = 34;

const int `LB_JV` = 35;

const int `LB_CLOSE_PARENTHESIS` = 36;

const int `LB_CONDITIONAL_JAPANESE_STARTER` = 37;

const int `LB_HEBREW_LETTER` = 38;

const int `LB_REGIONAL_INDICATOR` = 39;

const int `LB_COUNT` = 40;

const int `NT_NONE` = 0;

const int `NT_DECIMAL` = 1;

const int `NT_DIGIT` = 2;

const int `NT_NUMERIC` = 3;

const int `NT_COUNT` = 4;

const int `HST_NOT_APPLICABLE` = 0;

const int `HST_LEADING_JAMO` = 1;

const int `HST_VOWEL_JAMO` = 2;

const int `HST_TRAILING_JAMO` = 3;

const int `HST_LV_SYLLABLE` = 4;

const int `HST_LVT_SYLLABLE` = 5;

const int `HST_COUNT` = 6;

/\* Методи \*/

public static [charAge](intlchar.charage.md)(int\|string
`$codepoint`): ?array

public static [charDigitValue](intlchar.chardigitvalue.md)(int\|string
`$codepoint`): ?int

public static [charDirection](intlchar.chardirection.md)(int\|string
`$codepoint`): ?int

public static [charFromName](intlchar.charfromname.md)(string `$name`,
int `$type` = IntlChar::UNICODE_CHAR_NAME): ?int

public static [charMirror](intlchar.charmirror.md)(int\|string
`$codepoint`): int\|string\|null

public static [charName](intlchar.charname.md)(int\|string
`$codepoint`, int `$type` = IntlChar::UNICODE_CHAR_NAME): ?string

public static [charType](intlchar.chartype.md)(int\|string
`$codepoint`): ?int

public static [chr](intlchar.chr.md)(int\|string `$codepoint`):
?string

public static [digit](intlchar.digit.md)(int\|string `$codepoint`, int
`$base` = 10): int\|false\|null

public static [enumCharNames](intlchar.enumcharnames.md)(
int\|string `$start`,
int\|string `$end`,
[callable](language.types.callable.md) `$callback`,
int `$type` = IntlChar::UNICODE_CHAR_NAME
): ?bool

public static
[enumCharTypes](intlchar.enumchartypes.md)([callable](language.types.callable.md)
`$callback`): void

public static [foldCase](intlchar.foldcase.md)(int\|string
`$codepoint`, int `$options` = IntlChar::FOLD_CASE_DEFAULT):
int\|string\|null

public static [forDigit](intlchar.fordigit.md)(int `$digit`, int
`$base` = 10): int

public static
[getBidiPairedBracket](intlchar.getbidipairedbracket.md)(int\|string
`$codepoint`): int\|string\|null

public static [getBlockCode](intlchar.getblockcode.md)(int\|string
`$codepoint`): ?int

public static
[getCombiningClass](intlchar.getcombiningclass.md)(int\|string
`$codepoint`): ?int

public static
[getFC_NFKC_Closure](intlchar.getfc-nfkc-closure.md)(int\|string
`$codepoint`): string\|false\|null

public static
[getIntPropertyMaxValue](intlchar.getintpropertymaxvalue.md)(int
`$property`): int

public static
[getIntPropertyMinValue](intlchar.getintpropertyminvalue.md)(int
`$property`): int

public static
[getIntPropertyValue](intlchar.getintpropertyvalue.md)(int\|string
`$codepoint`, int `$property`): ?int

public static
[getNumericValue](intlchar.getnumericvalue.md)(int\|string
`$codepoint`): ?float

public static [getPropertyEnum](intlchar.getpropertyenum.md)(string
`$alias`): int

public static [getPropertyName](intlchar.getpropertyname.md)(int
`$property`, int `$type` = IntlChar::LONG_PROPERTY_NAME): string\|false

public static
[getPropertyValueEnum](intlchar.getpropertyvalueenum.md)(int
`$property`, string `$name`): int

public static
[getPropertyValueName](intlchar.getpropertyvaluename.md)(int
`$property`, int `$value`, int `$type` = IntlChar::LONG_PROPERTY_NAME):
string\|false

public static [getUnicodeVersion](intlchar.getunicodeversion.md)():
array

public static
[hasBinaryProperty](intlchar.hasbinaryproperty.md)(int\|string
`$codepoint`, int `$property`): ?bool

public static [isalnum](intlchar.isalnum.md)(int\|string
`$codepoint`): ?bool

public static [isalpha](intlchar.isalpha.md)(int\|string
`$codepoint`): ?bool

public static [isbase](intlchar.isbase.md)(int\|string `$codepoint`):
?bool

public static [isblank](intlchar.isblank.md)(int\|string
`$codepoint`): ?bool

public static [iscntrl](intlchar.iscntrl.md)(int\|string
`$codepoint`): ?bool

public static [isdefined](intlchar.isdefined.md)(int\|string
`$codepoint`): ?bool

public static [isdigit](intlchar.isdigit.md)(int\|string
`$codepoint`): ?bool

public static [isgraph](intlchar.isgraph.md)(int\|string
`$codepoint`): ?bool

public static [isIDIgnorable](intlchar.isidignorable.md)(int\|string
`$codepoint`): ?bool

public static [isIDPart](intlchar.isidpart.md)(int\|string
`$codepoint`): ?bool

public static [isIDStart](intlchar.isidstart.md)(int\|string
`$codepoint`): ?bool

public static [isISOControl](intlchar.isisocontrol.md)(int\|string
`$codepoint`): ?bool

public static [isJavaIDPart](intlchar.isjavaidpart.md)(int\|string
`$codepoint`): ?bool

public static [isJavaIDStart](intlchar.isjavaidstart.md)(int\|string
`$codepoint`): ?bool

public static
[isJavaSpaceChar](intlchar.isjavaspacechar.md)(int\|string
`$codepoint`): ?bool

public static [islower](intlchar.islower.md)(int\|string
`$codepoint`): ?bool

public static [isMirrored](intlchar.ismirrored.md)(int\|string
`$codepoint`): ?bool

public static [isprint](intlchar.isprint.md)(int\|string
`$codepoint`): ?bool

public static [ispunct](intlchar.ispunct.md)(int\|string
`$codepoint`): ?bool

public static [isspace](intlchar.isspace.md)(int\|string
`$codepoint`): ?bool

public static [istitle](intlchar.istitle.md)(int\|string
`$codepoint`): ?bool

public static [isUAlphabetic](intlchar.isualphabetic.md)(int\|string
`$codepoint`): ?bool

public static [isULowercase](intlchar.isulowercase.md)(int\|string
`$codepoint`): ?bool

public static [isupper](intlchar.isupper.md)(int\|string
`$codepoint`): ?bool

public static [isUUppercase](intlchar.isuuppercase.md)(int\|string
`$codepoint`): ?bool

public static [isUWhiteSpace](intlchar.isuwhitespace.md)(int\|string
`$codepoint`): ?bool

public static [isWhitespace](intlchar.iswhitespace.md)(int\|string
`$codepoint`): ?bool

public static [isxdigit](intlchar.isxdigit.md)(int\|string
`$codepoint`): ?bool

public static [ord](intlchar.ord.md)(int\|string `$character`): ?int

public static [tolower](intlchar.tolower.md)(int\|string
`$codepoint`): int\|string\|null

public static [totitle](intlchar.totitle.md)(int\|string
`$codepoint`): int\|string\|null

public static [toupper](intlchar.toupper.md)(int\|string
`$codepoint`): int\|string\|null

}

## Зумовлені константи

**`IntlChar::UNICODE_VERSION`**

**`IntlChar::CODEPOINT_MIN`**

**`IntlChar::CODEPOINT_MAX`**

**`IntlChar::NO_NUMERIC_VALUE`**
Special value that is returned by
[IntlChar::getNumericValue()](intlchar.getnumericvalue.md) when no
numeric value is defined for a code point.

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

## Список змін

| Версія | Опис                                             |
| ------ | ------------------------------------------------ |
| 7.0.6  | Додано константу **IntlChar::NO_NUMERIC_VALUE**. |

## Зміст

- [IntlChar::charAge](intlchar.charage.md) - Отримати "вік"
символьного коду
- [IntlChar::charDigitValue](intlchar.chardigitvalue.md) — Отримати
десяткову цифру із символу десяткової цифри
- [IntlChar::charDirection](intlchar.chardirection.md) — Отримати
категорію направлення листа для символу
- [IntlChar::charFromName](intlchar.charfromname.md) — Знайти символ
Unicode по його імені та повернути його код
- [IntlChar::charMirror](intlchar.charmirror.md) — Отримати
"дзеркальний" символ за кодом
- [IntlChar::charName](intlchar.charname.md) — Отримати назву символу
Unicode
- [IntlChar::charType](intlchar.chartype.md) — Отримати головну
категорію, до якої входить символ
- [IntlChar::chr](intlchar.chr.md) — Отримати символ Unicode на його
коду
- [IntlChar::digit](intlchar.digit.md) — Отримати десяткове число
із символу Unicode із заданою основою
- [IntlChar::enumCharNames](intlchar.enumcharnames.md) - Перераховує
усі присвоєні символи Unicode у заданому діапазоні
- [IntlChar::enumCharTypes](intlchar.enumchartypes.md) -
Перелік послідовностей символів Unicode згрупованих за
їм категоріям
- [IntlChar::foldCase](intlchar.foldcase.md) - Виробляє
перетворення регістру заданого символу
- [IntlChar::forDigit](intlchar.fordigit.md) — Отримати символ
що представляє задане число у заданій підставі
- [IntlChar::getBidiPairedBracket](intlchar.getbidipairedbracket.md)
— Отримати парну дужку для символу
- [IntlChar::getBlockCode](intlchar.getblockcode.md) — Отримати блок
розміщення символу Unicode
- [IntlChar::getCombiningClass](intlchar.getcombiningclass.md) -
Отримати комбінуючий клас для символу
- [IntlChar::getFC_NFKC_Closure](intlchar.getfc-nfkc-closure.md) -
Отримати властивість FC_NFKC_Closure для символу
- [IntlChar::getIntPropertyMaxValue](intlchar.getintpropertymaxvalue.md)
— Отримати мінімальне значення для якості Unicode
- [IntlChar::getIntPropertyMinValue](intlchar.getintpropertyminvalue.md)
— Отримати мінімальне значення для якості Unicode
- [IntlChar::getIntPropertyValue](intlchar.getintpropertyvalue.md) -
Отримати значення властивості Unicode для символу
- [IntlChar::getNumericValue](intlchar.getnumericvalue.md) -
Отримати числову виставу для символу Unicode
- [IntlChar::getPropertyEnum](intlchar.getpropertyenum.md) -
Отримати значення константи властивості на його ім'я
- [IntlChar::getPropertyName](intlchar.getpropertyname.md) -
Отримати Unicode ім'я властивості
- [IntlChar::getPropertyValueEnum](intlchar.getpropertyvalueenum.md)
— Повернути числовий ідентифікатор властивості на його ім'я
- [IntlChar::getPropertyValueName](intlchar.getpropertyvaluename.md)
— Отримати ім'я Unicode для значення властивості
- [IntlChar::getUnicodeVersion](intlchar.getunicodeversion.md) -
Отримати версію Unicode
- [IntlChar::hasBinaryProperty](intlchar.hasbinaryproperty.md) -
Перевірити бінарну властивість Unicode для символу
- [IntlChar::isalnum](intlchar.isalnum.md) — Перевірити, чи є
символ буквою чи цифрою
- [IntlChar::isalpha](intlchar.isalpha.md) — Перевірити, чи є
символ буквою
- [IntlChar::isbase](intlchar.isbase.md) — Перевірити, чи є
символ базовим
- [IntlChar::isblank](intlchar.isblank.md) — Перевірити, чи є
знак "порожнім" або "горизонтальним пропуском"
- [IntlChar::iscntrl](intlchar.iscntrl.md) — Перевірити, чи є
символ керуючим
- [IntlChar::isdefined](intlchar.isdefined.md) — Перевірити,
чи визначено символ
- [IntlChar::isdigit](intlchar.isdigit.md) — Перевірити, чи є
символ цифрою
- [IntlChar::isgraph](intlchar.isgraph.md) — Перевірити, чи є
символ графічний символ
- [IntlChar::isIDIgnorable](intlchar.isidignorable.md) — Перевірити,
чи є символ ігнорованим
- [IntlChar::isIDPart](intlchar.isidpart.md) — Перевірити, допустимо
чи використовувати символ в ідентифікаторі
- [IntlChar::isIDStart](intlchar.isidstart.md) — Перевірити,
чи можна використовувати символ на початку ідентифікатора
- [IntlChar::isISOControl](intlchar.isisocontrol.md) — Перевірити,
чи є символ керуючим відповідно до ISO
- [IntlChar::isJavaIDPart](intlchar.isjavaidpart.md) — Перевірити,
чи є символ допустимим в ідентифікаторі Java
- [IntlChar::isJavaIDStart](intlchar.isjavaidstart.md) — Перевірити,
чи може символ бути першим в ідентифікаторі Java
- [IntlChar::isJavaSpaceChar](intlchar.isjavaspacechar.md)
Перевірити, чи є символ пробельним з точки зору Java
- [IntlChar::islower](intlchar.islower.md) — Перевірити, чи в нижньому
регістрі символ
- [IntlChar::isMirrored](intlchar.ismirrored.md) — Перевірити, якщо у
символу властивість Bidi_Mirrored
- [IntlChar::isprint](intlchar.isprint.md) — Перевіряє, чи є
символ відображається
- [IntlChar::ispunct](intlchar.ispunct.md) — Перевіряє, чи є
символ пунктуації символ
- [IntlChar::isspace](intlchar.isspace.md) — Перевіряє, чи є
символ пробільний
- [IntlChar::istitle](intlchar.istitle.md) — Перевірити, чи є
символ титульним (Titlecase)
- [IntlChar::isUAlphabetic](intlchar.isualphabetic.md) — Перевірити,
чи встановлено у символу властивість Alphabetic
- [IntlChar::isULowercase](intlchar.isulowercase.md) — Перевірити,
чи є символ символом у нижньому регістрі
- [IntlChar::isupper](intlchar.isupper.md) — Перевірити, чи входить
символ у категорію "Lu" (літера у верхньому регістрі)
- [IntlChar::isUUppercase](intlchar.isuuppercase.md) — Перевірити,
чи є символ символом у верхньому регістрі
- [IntlChar::isUWhiteSpace](intlchar.isuwhitespace.md) — Перевірити,
чи має символ властивість White_Space (пробельний символ)
- [IntlChar::isWhitespace](intlchar.iswhitespace.md) — Перевірити,
чи є символ пробельним з точки зору ICU
- [IntlChar::isxdigit](intlchar.isxdigit.md) — Перевірити, чи є
чи символ шістнадцятковою цифрою
- [IntlChar::ord](intlchar.ord.md) — Отримати код Unicode
- [IntlChar::tolower](intlchar.tolower.md) — Перетворення символу
Unicode в нижній регістр
- [IntlChar::totitle](intlchar.totitle.md) — Перетворює символ
Unicode у titlecase
- [IntlChar::toupper](intlchar.toupper.md) — Перетворення символу
Unicode у верхній регістр

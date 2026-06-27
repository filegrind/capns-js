# CapDag-JS Test Catalog

**Total Tests:** 348

**Numbered Tests:** 348

**Unnumbered Tests:** 0

**Numbered Tests Missing Descriptions:** 0

**Numbering Mismatches:** 10

All numbered test numbers are unique.

This catalog lists all tests in the CapDag-JS codebase.

| Test # | Function Name | Description | File |
|--------|---------------|-------------|------|
| test001 | `test001_capUrnCreation` | TEST001: Test that cap URN is created with tags parsed correctly and direction specs accessible | capdag.test.js:143 |
| test002 | `test002_directionSpecsRequired` | TEST002: Test that missing 'in' or 'out' defaults to media: wildcard | capdag.test.js:153 |
| test003 | `test003_directionMatching` | TEST003: Test that direction specs must match exactly, different in/out types don't match, wildcard matches any | capdag.test.js:164 |
| test004 | `test004_unquotedValuesLowercased` | TEST004: Test that unquoted keys and values are normalized to lowercase. Key lookup is case-insensitive: uppercase variants of `ext` resolve to the same keyed tag. | capdag.test.js:181 |
| test005 | `test005_quotedValuesPreserveCase` | TEST005: Test that quoted values preserve case while unquoted are lowercased | capdag.test.js:189 |
| test006 | `test006_quotedValueSpecialChars` | TEST006: Test that quoted values can contain special characters (semicolons, equals, spaces) | capdag.test.js:195 |
| test007 | `test007_quotedValueEscapeSequences` | TEST007: Test that escape sequences in quoted values (\" and \\) are parsed correctly | capdag.test.js:201 |
| test008 | `test008_mixedQuotedUnquoted` | TEST008: Test that mixed quoted and unquoted values in same URN parse correctly | capdag.test.js:208 |
| test009 | `test009_unterminatedQuoteError` | TEST009: Test that unterminated quote produces UnterminatedQuote error | capdag.test.js:215 |
| test010 | `test010_invalidEscapeSequenceError` | TEST010: Test that invalid escape sequences (like \n, \x) produce InvalidEscapeSequence error | capdag.test.js:228 |
| test011 | `test011_serializationSmartQuoting` | TEST011: Test that serialization uses smart quoting (no quotes for simple lowercase, quotes for special chars/uppercase) | capdag.test.js:242 |
| test012 | `test012_roundTripSimple` | TEST012: Test that simple cap URN round-trips (parse -> serialize -> parse equals original) | capdag.test.js:251 |
| test013 | `test013_roundTripQuoted` | TEST013: Test that quoted values round-trip preserving case and spaces | capdag.test.js:259 |
| test014 | `test014_roundTripEscapes` | TEST014: Test that escape sequences round-trip correctly | capdag.test.js:268 |
| test015 | `test015_capPrefixRequired` | TEST015: Test that cap: prefix is required and case-insensitive | capdag.test.js:278 |
| test016 | `test016_trailingSemicolonEquivalence` | TEST016: Test that trailing semicolon is equivalent (same hash, same string, matches) | capdag.test.js:290 |
| test017 | `test017_tagMatching` | TEST017: Test tag matching: exact match, subset match, wildcard match, value mismatch | capdag.test.js:335 |
| test018 | `test018_matchingCaseSensitiveValues` | TEST018: Test that quoted values with different case do NOT match (case-sensitive) | capdag.test.js:359 |
| test019 | `test019_missingTagHandling` | TEST019: Missing tag in instance causes rejection — pattern's tags are constraints | capdag.test.js:366 |
| test020 | `test020_specificity` | TEST020: Specificity is the sum of per-tag truth-table scores across in/out/y. Marker tags (bare segments and `key=*`) score 2 (must-have-any), exact `key=value` tags score 3, missing/`?` score 0, `!` scores 1. test6204_Urn() builds "cap:in=media:void;out=media:record;<tags>" so the directional baseline is: in:  media:void   -> {void=*}    -> 2 out: media:record -> {record=*}  -> 2 Total directional baseline: 4. | capdag.test.js:388 |
| test021 | `test021_builder` | TEST021: Test builder creates cap URN with marker + keyed tags and direction specs. `op` is no longer a special key — operation names are markers (value-less tags). | capdag.test.js:417 |
| test022 | `test022_builderRequiresDirection` | TEST022: Test builder requires both in_spec and out_spec | capdag.test.js:431 |
| test023 | `test023_builderPreservesCase` | TEST023: Test builder lowercases keys but preserves value case | capdag.test.js:445 |
| test024 | `test024_compatibility` | TEST024: Directional accepts — pattern's tags are constraints, instance must satisfy | capdag.test.js:456 |
| test025 | `test025_bestMatch` | TEST025: Test find_best_match returns most specific matching cap | capdag.test.js:476 |
| test026 | `test026_mergeAndSubset` | TEST026: Test merge combines tags from both caps, subset keeps only specified tags | capdag.test.js:489 |
| test027 | `test027_wildcardTag` | TEST027: Test with_wildcard_tag sets tag to wildcard, including in/out | capdag.test.js:508 |
| test028 | `test028_emptyCapUrnNotAllowed` | TEST028: Test empty cap URN is illegal | capdag.test.js:521 |
| test029 | `test029_minimalCapUrn` | TEST029: Test minimal valid cap URN has just in and out, empty tags | capdag.test.js:530 |
| test030 | `test030_extendedCharacterSupport` | TEST030: Test extended characters (forward slashes, colons) in tag values | capdag.test.js:538 |
| test031 | `test031_wildcardRestrictions` | TEST031: Test wildcard rejected in keys but accepted in values | capdag.test.js:545 |
| test032 | `test032_duplicateKeyRejection` | TEST032: Test duplicate keys are rejected with DuplicateKey error | capdag.test.js:563 |
| test033 | `test033_numericKeyRestriction` | TEST033: Test pure numeric keys rejected, mixed alphanumeric allowed, numeric values allowed | capdag.test.js:572 |
| test034 | `test034_emptyValueError` | TEST034: Test empty values are rejected | capdag.test.js:586 |
| test035 | `test035_hasTagCaseSensitive` | TEST035: Test has_tag is case-sensitive for values, case-insensitive for keys, works for in/out | capdag.test.js:599 |
| test036 | `test036_withTagPreservesValue` | TEST036: Test with_tag preserves value case | capdag.test.js:611 |
| test037 | `test037_withTagRejectsEmptyValue` | TEST037: Test with_tag rejects empty value | capdag.test.js:618 |
| test038 | `test038_semanticEquivalence` | TEST038: Test semantic equivalence of unquoted and quoted simple lowercase values | capdag.test.js:628 |
| test039 | `test039_getTagReturnsDirectionSpecs` | TEST039: Test get_tag returns direction specs (in/out) with case-insensitive lookup | capdag.test.js:636 |
| test040 | `test040_matchingSemanticsExactMatch` | TEST040: Matching semantics - exact match succeeds | capdag.test.js:645 |
| test041 | `test041_matchingSemanticsCapMissingTag` | TEST041: Matching semantics - cap missing tag matches (implicit wildcard) | capdag.test.js:652 |
| test042 | `test042_matchingSemanticsCapHasExtraTag` | TEST042: Pattern rejects instance missing required tags | capdag.test.js:660 |
| test043 | `test043_matchingSemanticsRequestHasWildcard` | TEST043: Matching semantics - request wildcard matches specific cap value | capdag.test.js:668 |
| test044 | `test044_matchingSemanticsCapHasWildcard` | TEST044: Matching semantics - cap wildcard matches specific request value | capdag.test.js:675 |
| test045 | `test045_matchingSemanticsValueMismatch` | TEST045: Matching semantics - value mismatch does not match | capdag.test.js:682 |
| test046 | `test046_matchingSemanticsFallbackPattern` | TEST046: Matching semantics - fallback pattern (cap missing tag = implicit wildcard) | capdag.test.js:689 |
| test047 | `test047_matchingSemanticsThumbnailVoidInput` | TEST047: Matching semantics - thumbnail fallback with void input | capdag.test.js:697 |
| test048 | `test048_matchingSemanticsWildcardDirection` | TEST048: Matching semantics - wildcard direction matches anything | capdag.test.js:704 |
| test049 | `test049_matchingSemanticsCrossDimension` | TEST049: Non-overlapping tags — neither direction accepts | capdag.test.js:711 |
| test050 | `test050_matchingSemanticsDirectionMismatch` | TEST050: Matching semantics - direction mismatch prevents matching | capdag.test.js:719 |
| test060 | `test060_wrongPrefixFails` | TEST060: Test wrong prefix fails with InvalidPrefix error showing expected and actual prefix | capdag.test.js:867 |
| test062 | `test062_isRecord` | TEST062: Test is_record returns true when record marker tag is present indicating key-value structure | capdag.test.js:880 |
| test063 | `test063_isScalar` | TEST063: Test is_scalar returns true when list marker tag is absent (scalar is default) | capdag.test.js:891 |
| test064 | `test064_isList` | TEST064: Test is_list returns true when list marker tag is present indicating ordered collection | capdag.test.js:904 |
| test065 | `test065_isOpaque` | TEST065: Test is_opaque returns true when record marker is absent (opaque is default) | capdag.test.js:913 |
| test066 | `test066_isJson` | TEST066: Test is_json returns true only when fmt=json content-format tag is present | capdag.test.js:924 |
| test067 | `test067_isText` | TEST067: Text-representability is now carried by the orthogonal `enc=` tag (the old text marker and isText() are gone). A media is "text" iff it declares an encoding. | capdag.test.js:935 |
| test068 | `test068_isVoid` | TEST068: Test is_void returns true when void flag or type=void tag is present | capdag.test.js:948 |
| test071 | `test071_toStringRoundtrip` | TEST071: Test to_string roundtrip ensures serialization and deserialization preserve URN structure | capdag.test.js:956 |
| test072 | `test072_constantsParse` | TEST072: Test all media URN constants parse successfully as valid media URNs | capdag.test.js:966 |
| test074 | `test074_mediaUrnMatching` | TEST074: Test media URN conforms_to using tagged URN semantics with specific and generic requirements | capdag.test.js:986 |
| test075 | `test075_accepts` | TEST075: Test accepts with implicit wildcards where handlers with fewer tags can handle more requests | capdag.test.js:1000 |
| test076 | `test076_specificity` | TEST076: Test specificity increases with more tags for ranking conformance | capdag.test.js:1011 |
| test077 | `test077_serdeRoundtrip` | TEST077: Test serde roundtrip serializes to JSON string and deserializes back correctly | capdag.test.js:1020 |
| test078 | `test078_debugMatchingBehavior` | TEST078: conforms_to behavior between MEDIA_OBJECT and MEDIA_STRING | capdag.test.js:1029 |
| test100 | `test100_resolvedIsRecord` | TEST100: Test ResolvedMediaDef is_record returns true when record marker is present | capdag.test.js:1096 |
| test101 | `test101_resolvedIsScalar` | TEST101: Test ResolvedMediaDef is_scalar returns true when list marker is absent | capdag.test.js:1102 |
| test102 | `test102_resolvedIsList` | TEST102: Test ResolvedMediaDef is_list returns true when list marker is present | capdag.test.js:1108 |
| test103 | `test103_resolvedIsJson` | TEST103: Test ResolvedMediaDef is_json returns true when json tag is present | capdag.test.js:1114 |
| test105 | `test105_metadataPropagation` | TEST105: Test metadata propagates from media def def to resolved media def | capdag.test.js:1126 |
| test106 | `test106_metadataWithValidation` | TEST106: Test metadata and validation can coexist in media definition | capdag.test.js:1149 |
| test107 | `test107_extensionsPropagation` | TEST107: Test extensions field propagates from media def def to resolved | capdag.test.js:1168 |
| test108 | `test108_extensionsSerialization` | TEST108: Test creating new cap with URN, title, and command verifies correct initialization | capdag.test.js:1184 |
| test109 | `test109_extensionsWithMetadataAndValidation` | TEST109: Test creating cap with metadata initializes and retrieves metadata correctly | capdag.test.js:1192 |
| test110 | `test110_multipleExtensions` | TEST110: Test cap matching with subset semantics for request fulfillment | capdag.test.js:1211 |
| test115 | `test115_capArgSerialization` | TEST115: Test CapArg serialization and deserialization with multiple sources | capdag.test.js:1227 |
| test116 | `test116_capArgConstructors` | TEST116: Test CapArg constructor methods basic and with_description create args correctly | capdag.test.js:1260 |
| test150 | `test150_capManifestJsonSerialization` | TEST150: JSON roundtrip | capdag.test.js:1288 |
| test156 | `test156_stdinSourceFromData` | TEST156: Test creating StdinSource Data variant with byte vector | capdag.test.js:1444 |
| test157 | `test157_stdinSourceFromFileReference` | TEST157: Test creating StdinSource FileReference variant with all required fields | capdag.test.js:1455 |
| test158 | `test158_stdinSourceWithEmptyData` | TEST158: Test StdinSource Data with empty vector stores and retrieves correctly | capdag.test.js:1472 |
| test159 | `test159_stdinSourceWithBinaryContent` | TEST159: Test StdinSource Data with binary content like PNG header bytes | capdag.test.js:1480 |
| test274 | `test274_capArgumentValueNew` | TEST274: Test CapArgumentValue::new stores media_urn and raw byte value | capdag.test.js:1494 |
| test275 | `test275_capArgumentValueFromStr` | TEST275: Test CapArgumentValue::from_str converts string to UTF-8 bytes | capdag.test.js:1501 |
| test276 | `test276_capArgumentValueAsStrValid` | TEST276: Test CapArgumentValue::value_as_str succeeds for UTF-8 data | capdag.test.js:1508 |
| test277 | `test277_capArgumentValueAsStrInvalidUtf8` | TEST277: Test CapArgumentValue::value_as_str fails for non-UTF-8 binary data | capdag.test.js:1514 |
| test278 | `test278_capArgumentValueEmpty` | TEST278: Test CapArgumentValue::new with empty value stores empty vec | capdag.test.js:1526 |
| test282 | `test282_capArgumentValueUnicode` | TEST282: Test CapArgumentValue::from_str with Unicode string preserves all characters | capdag.test.js:1535 |
| test283 | `test283_capArgumentValueLargeBinary` | TEST283: Test CapArgumentValue with large binary payload preserves all bytes | capdag.test.js:1541 |
| test304 | `test304_mediaAvailabilityOutputConstant` | TEST304: Test MEDIA_AVAILABILITY_OUTPUT constant parses as valid media URN with correct tags | capdag.test.js:1560 |
| test305 | `test305_mediaPathOutputConstant` | TEST305: Test MEDIA_PATH_OUTPUT constant parses as valid media URN with correct tags | capdag.test.js:1569 |
| test306 | `test306_availabilityAndPathOutputDistinct` | TEST306: Test MEDIA_AVAILABILITY_OUTPUT and MEDIA_PATH_OUTPUT are distinct URNs | capdag.test.js:1578 |
| test307 | `test307_modelAvailabilityUrn` | TEST307: Test model_availability_urn builds valid cap URN with correct op and media defs | capdag.test.js:1592 |
| test308 | `test308_modelPathUrn` | TEST308: Test model_path_urn builds valid cap URN with correct op and media defs | capdag.test.js:1604 |
| test309 | `test309_modelAvailabilityAndPathAreDistinct` | TEST309: Test model_availability_urn and model_path_urn produce distinct URNs | capdag.test.js:1616 |
| test310 | `test310_llmGenerateTextUrn` | TEST310: llm_generate_text_urn() produces a valid cap URN with enc=utf-8 in/out specs | capdag.test.js:1623 |
| test312 | `test312_allUrnBuildersProduceValidUrns` | TEST312: Test all URN builders produce parseable cap URNs | capdag.test.js:1646 |
| test321 | `test321_cartridgeInfoIsSigned` | TEST321: CartridgeInfo.is_signed() returns true when signature is present | capdag.test.js:2044 |
| test322 | `test322_cartridgeInfoBuildForPlatform` | TEST322: CartridgeInfo.build_for_platform() returns the build matching the current platform | capdag.test.js:2056 |
| test323 | `test323_cartridgeRepoServerValidateRegistry` | TEST323: CartridgeRepoServer requires schema 5.0 and rejects older. | capdag.test.js:2090 |
| test325 | `test325_cartridgeRepoServerGetCartridges` | TEST325: CartridgeRepoServer.getCartridges() wraps the transformed flat array (across both channels) in the response envelope. | capdag.test.js:2167 |
| test326 | `test326_cartridgeRepoServerGetCartridgeById` | TEST326: CartridgeRepoServer.getCartridgeById() requires (channel, id). Same id looked up in the wrong channel must miss — channels are independent namespaces. | capdag.test.js:2181 |
| test334 | `test334_cartridgeRepoClientNeedsSync` | TEST334: CartridgeRepoClient.needsSync() returns true when cache is empty / stale, false right after a fresh update. | capdag.test.js:2391 |
| test597 | `test597_capArgWithFullDefinition` | TEST597: CapArg::with_full_definition stores all fields including optional ones | capdag.test.js:1344 |
| test640 | `test640_inOnlyIsIllegal` | TEST640: cap:in collapses to the same illegal bare top form | capdag.test.js:3057 |
| test641 | `test641_outOnlyIsIllegal` | TEST641: cap:out collapses to the same illegal bare top form | capdag.test.js:3066 |
| test642 | `test642_inOutWithoutValuesAreIllegal` | TEST642: cap:in;out collapses to the same illegal bare top form | capdag.test.js:3075 |
| test643 | `test643_explicitAsteriskIsIllegal` | TEST643: cap:in=*;out=* is the same illegal bare top form | capdag.test.js:3084 |
| test644 | `test644_specificInWildcardOutIsIllegal` | TEST644: cap:in=media:;out=* is the same illegal bare top form | capdag.test.js:3093 |
| test645 | `test645_wildcardInSpecificOut` | TEST645: cap:in=*;out=media:text has wildcard in, specific out | capdag.test.js:3102 |
| test646 | `test646_invalidInSpecFails` | TEST646: cap:in=foo fails (invalid media URN) | capdag.test.js:3109 |
| test647 | `test647_invalidOutSpecFails` | TEST647: cap:in=media:;out=bar fails (invalid media URN) | capdag.test.js:3118 |
| test648 | `test648_wildcardAcceptsSpecific` | TEST648: Wildcard in/out match specific caps | capdag.test.js:3127 |
| test649 | `test649_specificityScoring` | TEST649: Specificity - wildcard has 0, specific has tag count | capdag.test.js:3136 |
| test650 | `test650_wildcardPreserveOtherTags` | TEST650: cap:in=media:;out=media:;test preserves other tags | capdag.test.js:3145 |
| test653 | `test653_invalidEffectNoneDeclarationRejected` | TEST653: invalid effect=none declarations fail at construction. | capdag.test.js:3192 |
| test654 | `test654_effectNonePreservesRuntimeMedia` | TEST654: effect=none preserves runtime media identity. | capdag.test.js:3201 |
| test655 | `test655_effectDeclaredUsesDeclaredOutput` | TEST655: default effect=declared does not preserve runtime refinements. | capdag.test.js:3210 |
| test656 | `test656_invalidEffectNoneFailsHard` | TEST656: invalid effect=none declarations fail hard at construction. | capdag.test.js:3221 |
| test657 | `test657_effectDispatchRequiresExplicitWildcard` | TEST657: omitted effect means declared; unconstrained effect must be explicit. | capdag.test.js:3230 |
| test890 | `test890_directionSemanticMatching` | TEST890: Semantic direction matching - generic provider matches specific request | capdag.test.js:730 |
| test891 | `test891_directionSemanticSpecificity` | TEST891: Semantic direction specificity — more constraints in either axis means a higher score under the truth-table-driven sum. media: (top, no tags) scores 0; each marker tag scores 2; each exact-value tag (e.g. ext=png) scores 4. | capdag.test.js:783 |
| test939 | `test939_capUrnCanonicalFormDropsWildcardInOut` | TEST939: The canonical form drops `in=media:` and `out=media:` segments. Every spelling of "the same cap with wildcard in/out" collapses to one byte-identical canonical string. This is the contract that makes registry lookups work: the cap-publisher hashes `<canonical-urn>` to compute the cache key, and every language port (Rust, Go, Python, JS, ObjC) must agree on the canonical form for cross-language lookups to land on the same key. A regression that emitted the wildcard segments would silently move the published cap to a different SHA-256 bucket, 404'ing every reader that hashes the canonical form. | capdag.test.js:307 |
| test1294 | `test1294_rule11VoidInputWithStdinRejected` | TEST1294: RULE11 - void-input cap with stdin source rejected | capdag.test.js:2992 |
| test1295 | `test1295_rule11NonVoidInputWithoutStdinRejected` | TEST1295: RULE11 - non-void-input cap without stdin source rejected | capdag.test.js:3007 |
| test1296 | `test1296_rule11VoidInputCliFlagOnly` | TEST1296: RULE11 - void-input cap with only cli_flag sources passes | capdag.test.js:3022 |
| test1297 | `test1297_rule11NonVoidInputWithStdin` | TEST1297: RULE11 - non-void-input cap with stdin source passes | capdag.test.js:3032 |
| test1298 | `test1298_isBool` | TEST1298: is_bool returns true only when bool marker tag is present | capdag.test.js:2800 |
| test1299 | `test1299_isFilePath` | TEST1299: isFilePath returns true for the single file-path media URN, false for everything else. There is no "array" variant — cardinality is carried by is_sequence on the wire, not by URN tags. | capdag.test.js:2814 |
| test1302 | `test1302_predicateConstantConsistency` | TEST1302: predicates are consistent with constants — every constant triggers exactly the expected predicates | capdag.test.js:2833 |
| test1303 | `test1303_withoutTag` | TEST1303: without_tag removes tag, rejects structural keys, case-insensitive for keys | capdag.test.js:2872 |
| test1304 | `test1304_withInOutSpec` | TEST1304: with_in_spec and with_out_spec change direction specs | capdag.test.js:2892 |
| test1305 | `test1305_findAllMatches` | TEST1305: CapMatcher::find_all_matches returns all matching caps sorted by specificity | capdag.test.js:2922 |
| test1306 | `test1306_areCompatible` | TEST1306: CapMatcher::are_compatible detects bidirectional overlap | capdag.test.js:2940 |
| test1307 | `test1307_withTagRejectsStructuralKeys` | TEST1307: with_tag rejects structural keys | capdag.test.js:2965 |
| test1312 | `test1312_isImage` | TEST1312: is_image returns true only when image marker tag is present | capdag.test.js:2755 |
| test1313 | `test1313_isAudio` | TEST1313: is_audio returns true only when audio marker tag is present | capdag.test.js:2767 |
| test1314 | `test1314_isVideo` | TEST1314: is_video returns true only when video marker tag is present | capdag.test.js:2778 |
| test1315 | `test1315_isNumeric` | TEST1315: is_numeric returns true only when numeric marker tag is present | capdag.test.js:2788 |
| test1800 | `test1800_kindIdentityOnlyForBareCap` | TEST1800: Identity classifier — only explicit effect=none qualifies. | capdag.test.js:6014 |
| test1801 | `test1801_kindSourceWhenInputIsVoid` | TEST1801: Source classifier — in=media:void, out non-void. | capdag.test.js:6041 |
| test1802 | `test1802_kindSinkWhenOutputIsVoid` | TEST1802: Sink classifier — out=media:void, in non-void. | capdag.test.js:6050 |
| test1803 | `test1803_kindEffectWhenBothSidesVoid` | TEST1803: Effect classifier — both sides void. Reads as `() → ()`. | capdag.test.js:6059 |
| test1804 | `test1804_kindTransformForNormalDataProcessors` | TEST1804: Transform classifier — at least one side non-void, and the cap is not the bare identity. | capdag.test.js:6070 |
| test1805 | `test1805_kindInvariantUnderCanonicalSpellings` | TEST1805: Kind is invariant under canonicalization. The same morphism written in many surface forms must classify the same way once parsed. | capdag.test.js:6120 |
| test1810 | `test1810_mediaVoidIsAtomic` | TEST1810: media:void is atomic — refinements are parse errors. Mirrored across every language port (Rust, Go, Python, Swift/ObjC, JS) under the SAME number. Any divergence is a wire-level inconsistency — the unit type's atomicity is part of the protocol's deepest layer, not a per-port detail. | capdag.test.js:6085 |
| test1820 | `test1820_specificityQuestionIsZero` | TEST1820: A `?`-valued cap-tag scores 0. Same as missing. | capdag.test.js:6161 |
| test1821 | `test1821_specificityMustNotHaveIsFive` | TEST1821: A `!`-valued cap-tag scores 5 (top of negative chain). | capdag.test.js:6171 |
| test1822 | `test1822_specificityMustHaveAnyIsTwo` | TEST1822: A `*`-valued cap-tag (including bare markers) scores 2. | capdag.test.js:6178 |
| test1823 | `test1823_specificityExactValueIsFour` | TEST1823: An exact-valued cap-tag scores 4. | capdag.test.js:6192 |
| test1824 | `test1824_specificityCombinedYAxis` | TEST1824: All six forms compose additively on a single cap. y combining 0+1+2+3+4+5 must sum to 15. | capdag.test.js:6200 |
| test1830 | `test1830_canonicalizeNoConstraint` | TEST1830: ?x ≡ x? ≡ x=? all canonicalize to ?x. | capdag.test.js:6211 |
| test1831 | `test1831_canonicalizeAbsentOrNotValue` | TEST1831: ?x=v and x?=v both canonicalize to x?=v. The third hypothetical form `x=?v` is NOT recognized as a qualifier — a value starting with `?` is just an exact value beginning with a `?` character. | capdag.test.js:6224 |
| test1832 | `test1832_canonicalizeMustHaveAny` | TEST1832: x ≡ x=* both canonicalize to bare x. | capdag.test.js:6240 |
| test1833 | `test1833_canonicalizePresentNotValue` | TEST1833: !x=v and x!=v both canonicalize to x!=v. The third hypothetical form `x=!v` is NOT recognized as a qualifier — a value starting with `!` is just an exact value beginning with a `!` character. | capdag.test.js:6253 |
| test1834 | `test1834_canonicalizeExactValue` | TEST1834: x=v stays as x=v. | capdag.test.js:6269 |
| test1835 | `test1835_canonicalizeMustNotHave` | TEST1835: !x ≡ x! ≡ x=! all canonicalize to !x. | capdag.test.js:6275 |
| test1843 | `test1843_rejectInvalidCombinations` | TEST1843: Invalid qualifier combinations must be rejected. | capdag.test.js:6313 |
| test1844 | `test1844_axisWeightingOutDominates` | TEST1844: out-axis difference dominates combined in+y differences. | capdag.test.js:6328 |
| test1845 | `test1845_axisWeightingInDominatesY` | TEST1845: With equal out, in-axis dominates over y-axis. | capdag.test.js:6338 |
| test1846 | `test1846_axisWeightingDecodedLayout` | TEST1846: Decoded layout — 10000*out + 100*in + y. | capdag.test.js:6348 |
| test1848 | `test1848_capVersionNonZeroOnWire` | TEST1848: Cap with version=N round-trips with `version: N` on wire | capdag.test.js:6372 |
| test1849 | `test1849_resolveForHostCompatibleLatest` | TEST1849: latest version has a host build → Compatible, resolving to the latest version and that platform's native-format package. | capdag.test.js:2494 |
| test1850 | `test1850_resolveForHostCompatibleOutdated` | TEST1850: the latest version lacks a host build but an older version has one → CompatibleOutdated, resolving to the NEWEST older version with a host build (not the oldest), with a reason naming both the latest and the resolved. | capdag.test.js:2512 |
| test1851 | `test1851_resolveForHostIncompatible` | TEST1851: no version ships a host build → Incompatible, no resolved version/package, reason states the host platform. | capdag.test.js:2530 |
| test1852 | `test1852_resolveForHostSkipsBuildWithNoInstaller` | TEST1852: a host build whose packages[] is empty AND has no legacy `package` ships no installer; resolution must SKIP it (not resolve to an un-downloadable version) and fall through to an older usable version. | capdag.test.js:2546 |
| test1853 | `test1853_hostPlatformNormalizedForm` | TEST1853: hostPlatform() returns a normalized {os}-{arch} string with arch aarch64/arm64 mapped to arm64 — the exact form the registry uses. | capdag.test.js:2565 |
| test1874 | `test1874_registryUrlFromBuildEnvRejectsEmptyString` | TEST1874: an exported-but-empty env ('') is neither a dev build nor a valid identity and MUST fail hard, so the build can never silently hash the empty string into a fake registry slug. | capdag.test.js:2597 |
| test1880 | `test1880_aliasNameNormalizationRules` | TEST1880: alias name normalization lowercases and accepts the allowed char class; rejects colon, whitespace, and out-of-class chars. | capdag.test.js:6395 |
| test1881 | `test1881_tokenUrnVsAliasDetection` | TEST1881: URN-vs-alias detection keys purely on the presence of ':'. | capdag.test.js:6407 |
| test1882 | `test1882_classifyAliasTargetByPrefix` | TEST1882: alias target classification distinguishes cap from media by prefix and rejects a non-URN target. | capdag.test.js:6417 |
| test1887 | `test1887_manifestSerdeRoundTripsAliases` | TEST1887: the Manifest type round-trips an `aliases` map. | capdag.test.js:6426 |
| test6201 | `test6201_emptyCapIsIllegal` | TEST6201: cap: (empty) is the illegal bare top form | capdag.test.js:3048 |
| test6204 | `test6204_Urn` | TEST6204: Urn | capdag.test.js:118 |
| test6206 | `test6206_CapFabAddCapPopulatesEdgesAndNodes` | Add a cap and check it becomes an edge with from/to nodes and carries the registry name we passed. This is exactly the shape the renderer depends on. | capdag.test.js:1387 |
| test6208 | `test6208_CapFabGetOutgoingConformsToMatching` | getOutgoing takes a concrete source URN and returns edges whose from_spec the source conforms to. It must NOT be a plain string lookup. | capdag.test.js:1405 |
| test6212 | `test6212_xv5InlineSpecRedefinitionDetected` | TEST6212: XV5 - Test inline media def redefinition of existing registry spec is detected and rejected | capdag.test.js:823 |
| test6216 | `test6216_xv5NewInlineSpecAllowed` | TEST6216: XV5 - Test new inline media def (not in registry) is allowed | capdag.test.js:840 |
| test6220 | `test6220_xv5EmptyMediaDefsAllowed` | TEST6220: XV5 - Test empty media_defs (no inline specs) passes XV5 validation | capdag.test.js:855 |
| test6224 | `test6224_CapFabDistinctRegistryNames` | Each edge must carry the registry name it was added with. This is how the renderer colours/groups edges by provenance in browse mode. | capdag.test.js:1426 |
| test6228 | `test6228_LlmGenerateTextUrnSpecs` | Mirror-specific coverage: llm_generate_text_urn input/output specs conform to MEDIA_STRING | capdag.test.js:1635 |
| test6232 | `test6232_JS_buildExtensionIndex` | These tests cover JS-specific functionality not in the Rust numbering scheme but are important for capdag-js correctness. | capdag.test.js:1666 |
| test6236 | `test6236_JS_mediaUrnsForExtension` | TEST6236: J s media urns for extension | capdag.test.js:1683 |
| test6240 | `test6240_JS_getExtensionMappings` | TEST0070: J s get extension mappings | capdag.test.js:1712 |
| test6242 | `test6242_JS_resolveMediaUrnFromSpecs` | TEST0073: J s resolve media urn from specs | capdag.test.js:1723 |
| test6246 | `test6246_JS_capJSONSerialization` | TEST6246: J s cap j s o n serialization | capdag.test.js:1736 |
| test6249 | `test6249_JS_capDocumentationRoundTrip` | JS round-trip for the documentation field on Cap. Mirrors TEST920 in capdag/src/cap/definition.rs — the body is non-trivial (newlines, backticks, embedded quotes, Unicode) so escaping mismatches between JSON.stringify on this side and the Rust serializer on the other side surface as failures here. | capdag.test.js:1759 |
| test6253 | `test6253_JS_capDocumentationOmittedWhenNull` | When documentation is null, toJSON must omit the field entirely. This matches the Rust serializer's skip-when-None semantics and the ObjC toDictionary behaviour. A regression where null is emitted as `documentation: null` would break the symmetric round-trip with Rust (which has no null sentinel) and pollute generated JSON. | capdag.test.js:1781 |
| test6257 | `test6257_JS_mediaDefDocumentationPropagatesThroughResolve` | Documentation propagates from a mediaDefs definition through resolveMediaUrn into the resolved MediaDef. Mirrors TEST924 on the Rust side. This is the path every UI consumer uses, so a break here makes the new field invisible everywhere downstream. | capdag.test.js:1804 |
| test6261 | `test6261_JS_stdinSourceKindConstants` | TEST6261: J s stdin source kind constants | capdag.test.js:1835 |
| test6265 | `test6265_JS_stdinSourceNullData` | TEST6265: J s stdin source null data | capdag.test.js:1842 |
| test6269 | `test6269_JS_mediaDefConstruction` | TEST6269: J s media def construction | capdag.test.js:1850 |
| test6272 | `test6272_isCollection` | Mirror-specific coverage: isCollection returns true when collection marker tag is present Mirror-specific coverage: N/A for JS (MEDIA_COLLECTION constants removed - no longer exists) | capdag.test.js:2822 |
| test6275 | `test6275_Machine_emptyInput` | --- Machine parser tests (mirrors parser.rs tests) --- | capdag.test.js:3244 |
| test6277 | `test6277_Machine_whitespaceOnly` | TEST0088: Machine whitespace only | capdag.test.js:3249 |
| test6279 | `test6279_Machine_headerOnlyNoWirings` | TEST0089: Machine header only no wirings | capdag.test.js:3254 |
| test6280 | `test6280_Machine_duplicateAlias` | TEST0090: Machine duplicate alias | capdag.test.js:3262 |
| test6282 | `test6282_resolveCustomMediaDef` | TEST6282: Test resolving custom media URN from local media_defs takes precedence over registry | capdag.test.js:1044 |
| test6283 | `test6283_resolveCustomWithSchema` | TEST6283: Test resolving custom record media def with schema from local media_defs | capdag.test.js:1054 |
| test6284 | `test6284_resolveUnresolvableFailsHard` | TEST6284: Test resolving unknown media URN fails with UnresolvableMediaUrn error | capdag.test.js:1071 |
| test6286 | `test6286_Machine_simpleLinearChain` | TEST0094: Machine simple linear chain | capdag.test.js:3274 |
| test6288 | `test6288_Machine_twoStepChain` | TEST0095: Machine two step chain | capdag.test.js:3290 |
| test6290 | `test6290_Machine_fanOut` | TEST0096: Machine fan out | capdag.test.js:3305 |
| test6292 | `test6292_Machine_fanInSecondaryAssignedByPriorWiring` | TEST0097: Machine fan in secondary assigned by prior wiring | capdag.test.js:3323 |
| test6294 | `test6294_Machine_fanInSecondaryUnassignedGetsWildcard` | TEST0098: Machine fan in secondary unassigned gets wildcard | capdag.test.js:3337 |
| test6297 | `test6297_resolvedIsBinary` | TEST6297: Test ResolvedMediaDef is_binary returns true when enc tag is absent | capdag.test.js:1090 |
| test6298 | `test6298_resolvedIsText` | TEST6298: Test ResolvedMediaDef is_text returns true when enc tag is present | capdag.test.js:1120 |
| test6306 | `test6306_Machine_loopEdge` | TEST6306: Machine loop edge | capdag.test.js:3349 |
| test6308 | `test6308_Machine_undefinedAliasFails` | TEST6308: Machine undefined alias fails | capdag.test.js:3359 |
| test6310 | `test6310_Machine_nodeAliasCollision` | TEST6310: Machine node alias collision | capdag.test.js:3367 |
| test6312 | `test6312_Machine_conflictingMediaTypesFail` | TEST6312: Machine conflicting media types fail | capdag.test.js:3378 |
| test6315 | `test6315_Machine_multilineFormat` | TEST6315: Machine multiline format | capdag.test.js:3391 |
| test6318 | `test6318_Machine_differentAliasesSameGraph` | TEST6318: Machine different aliases same graph | capdag.test.js:3402 |
| test6321 | `test6321_Machine_malformedInputFails` | TEST6321: Machine malformed input fails | capdag.test.js:3415 |
| test6323 | `test6323_Machine_unterminatedBracketFails` | TEST6323: Machine unterminated bracket fails | capdag.test.js:3423 |
| test6327 | `test6327_Machine_lineBasedSimpleChain` | --- Machine parser line-based mode tests --- | capdag.test.js:3432 |
| test6331 | `test6331_Machine_lineBasedTwoStepChain` | TEST6331: Machine line based two step chain | capdag.test.js:3446 |
| test6334 | `test6334_Machine_lineBasedLoop` | TEST6334: Machine line based loop | capdag.test.js:3457 |
| test6337 | `test6337_Machine_lineBasedFanIn` | TEST6337: Machine line based fan in | capdag.test.js:3467 |
| test6341 | `test6341_Machine_mixedBracketedAndLineBased` | TEST6341: Machine mixed bracketed and line based | capdag.test.js:3481 |
| test6345 | `test6345_Machine_lineBasedEquivalentToBracketed` | TEST6345: Machine line based equivalent to bracketed | capdag.test.js:3490 |
| test6349 | `test6349_Machine_lineBasedFormatSerialization` | TEST6349: Machine line based format serialization | capdag.test.js:3503 |
| test6353 | `test6353_Machine_lineBasedAndBracketedParseSameGraph` | TEST6353: Machine line based and bracketed parse same graph | capdag.test.js:3525 |
| test6357 | `test6357_Machine_edgeEquivalenceSameUrns` | --- Machine graph tests (mirrors graph.rs tests) --- | capdag.test.js:3551 |
| test6361 | `test6361_Machine_edgeEquivalenceDifferentCapUrns` | TEST6361: Machine edge equivalence different cap urns | capdag.test.js:3568 |
| test6365 | `test6365_Machine_edgeEquivalenceDifferentTargets` | TEST6365: Machine edge equivalence different targets | capdag.test.js:3585 |
| test6369 | `test6369_Machine_edgeEquivalenceDifferentLoopFlag` | TEST6369: Machine edge equivalence different loop flag | capdag.test.js:3602 |
| test6372 | `test6372_Machine_edgeEquivalenceSourceOrderIndependent` | TEST6372: Machine edge equivalence source order independent | capdag.test.js:3619 |
| test6375 | `test6375_Machine_edgeEquivalenceDifferentSourceCount` | TEST6375: Machine edge equivalence different source count | capdag.test.js:3636 |
| test6377 | `test6377_Machine_graphEquivalenceSameEdges` | TEST6377: Machine graph equivalence same edges | capdag.test.js:3653 |
| test6380 | `test6380_Machine_graphEquivalenceReorderedEdges` | TEST6380: Machine graph equivalence reordered edges | capdag.test.js:3669 |
| test6383 | `test6383_Machine_graphNotEquivalentDifferentEdgeCount` | TEST6383: Machine graph not equivalent different edge count | capdag.test.js:3685 |
| test6386 | `test6386_Machine_graphNotEquivalentDifferentCap` | TEST6386: Machine graph not equivalent different cap | capdag.test.js:3700 |
| test6389 | `test6389_Machine_graphEmpty` | TEST6389: Machine graph empty | capdag.test.js:3714 |
| test6392 | `test6392_Machine_graphEmptyEquivalence` | TEST6392: Machine graph empty equivalence | capdag.test.js:3721 |
| test6395 | `test6395_Machine_rootSourcesLinearChain` | TEST6395: Machine root sources linear chain | capdag.test.js:3728 |
| test6397 | `test6397_Machine_leafTargetsLinearChain` | TEST6397: Machine leaf targets linear chain | capdag.test.js:3743 |
| test6398 | `test6398_Machine_rootSourcesFanIn` | TEST6398: Machine root sources fan in | capdag.test.js:3758 |
| test6400 | `test6400_Machine_displayEdge` | TEST6400: Machine display edge | capdag.test.js:3771 |
| test6402 | `test6402_Machine_displayGraph` | TEST6402: Machine display graph | capdag.test.js:3783 |
| test6404 | `test6404_Machine_serializeSingleEdge` | --- Machine serializer tests (mirrors serializer.rs tests) --- | capdag.test.js:3796 |
| test6406 | `test6406_Machine_serializeTwoEdgeChain` | TEST6406: Machine serialize two edge chain | capdag.test.js:3812 |
| test6408 | `test6408_Machine_serializeEmptyGraph` | TEST6408: Machine serialize empty graph | capdag.test.js:3826 |
| test6410 | `test6410_Machine_roundtripSingleEdge` | TEST6410: Machine roundtrip single edge | capdag.test.js:3831 |
| test6413 | `test6413_Machine_roundtripTwoEdgeChain` | TEST6413: Machine roundtrip two edge chain | capdag.test.js:3845 |
| test6415 | `test6415_Machine_roundtripFanOut` | TEST6415: Machine roundtrip fan out | capdag.test.js:3860 |
| test6417 | `test6417_Machine_roundtripLoopEdge` | TEST6417: Machine roundtrip loop edge | capdag.test.js:3876 |
| test6419 | `test6419_Machine_serializationIsDeterministic` | TEST6419: Machine serialization is deterministic | capdag.test.js:3890 |
| test6421 | `test6421_Machine_reorderedEdgesProduceSameNotation` | TEST6421: Machine reordered edges produce same notation | capdag.test.js:3904 |
| test6429 | `test6429_Machine_multilineSerializeFormat` | TEST6429: Machine multiline serialize format | capdag.test.js:3921 |
| test6432 | `test6432_Machine_aliasFromOpTag` | Aliases are pure-index `edge_<N>` regardless of the cap's tags; there is no privileged `op` tag to derive a friendlier name from. | capdag.test.js:3937 |
| test6434 | `test6434_Machine_aliasFallbackWithoutOpTag` | TEST6434: Machine alias fallback without op tag | capdag.test.js:3949 |
| test6436 | `test6436_Machine_duplicateOpTagsDisambiguated` | Pure-index aliases inherently disambiguate edges that share a marker tag. | capdag.test.js:3961 |
| test6437 | `test6437_Machine_builderSingleEdge` | --- Machine builder tests --- | capdag.test.js:3983 |
| test6438 | `test6438_Machine_builderWithLoop` | TEST6438: Machine builder with loop | capdag.test.js:3996 |
| test6439 | `test6439_Machine_builderChaining` | TEST6439: Machine builder chaining | capdag.test.js:4009 |
| test6440 | `test6440_Machine_builderEquivalentToParsed` | TEST6440: Machine builder equivalent to parsed | capdag.test.js:4018 |
| test6442 | `test6442_Machine_builderRoundTrip` | TEST6442: Machine builder round trip | capdag.test.js:4031 |
| test6444 | `test6444_Machine_capUrnIsEquivalent` | --- CapUrn.isEquivalent/isComparable tests --- | capdag.test.js:4043 |
| test6446 | `test6446_Machine_capUrnIsComparable` | TEST6446: Machine cap urn is comparable | capdag.test.js:4052 |
| test6448 | `test6448_Machine_capUrnInMediaUrn` | TEST6448: Machine cap urn in media urn | capdag.test.js:4060 |
| test6449 | `test6449_Machine_capUrnOutMediaUrn` | TEST6449: Machine cap urn out media urn | capdag.test.js:4068 |
| test6450 | `test6450_Machine_mediaUrnIsEquivalent` | --- MediaUrn.isEquivalent/isComparable tests --- | capdag.test.js:4077 |
| test6451 | `test6451_Machine_mediaUrnIsComparable` | TEST6451: Machine media urn is comparable | capdag.test.js:4086 |
| test6452 | `test6452_Machine_parseMachineWithAST_headerLocation` | Phase 0A: Position tracking tests | capdag.test.js:4099 |
| test6453 | `test6453_Machine_parseMachineWithAST_wiringLocation` | TEST6453: Machine parse machine with a s t wiring location | capdag.test.js:4116 |
| test6454 | `test6454_Machine_parseMachineWithAST_multilinePositions` | TEST6454: Machine parse machine with a s t multiline positions | capdag.test.js:4131 |
| test6455 | `test6455_Machine_parseMachineWithAST_fanInSourceLocations` | TEST6455: Machine parse machine with a s t fan in source locations | capdag.test.js:4141 |
| test6456 | `test6456_Machine_parseMachineWithAST_aliasMap` | TEST6456: Machine parse machine with a s t alias map | capdag.test.js:4153 |
| test6457 | `test6457_Machine_parseMachineWithAST_nodeMedia` | TEST6457: Machine parse machine with a s t node media | capdag.test.js:4172 |
| test6458 | `test6458_Machine_errorLocation_parseError` | TEST6458: Machine error location parse error | capdag.test.js:4185 |
| test6459 | `test6459_Machine_errorLocation_duplicateAlias` | TEST6459: Machine error location duplicate alias | capdag.test.js:4196 |
| test6460 | `test6460_Machine_errorLocation_undefinedAlias` | TEST6460: Machine error location undefined alias | capdag.test.js:4211 |
| test6462 | `test6462_Machine_toMermaid_linearChain` | Phase 0C: Machine.toMermaid() tests | capdag.test.js:4225 |
| test6463 | `test6463_Machine_toMermaid_loopEdge` | TEST6463: Machine to mermaid loop edge | capdag.test.js:4244 |
| test6464 | `test6464_Machine_toMermaid_emptyGraph` | TEST6464: Machine to mermaid empty graph | capdag.test.js:4256 |
| test6465 | `test6465_Machine_toMermaid_fanIn` | TEST6465: Machine to mermaid fan in | capdag.test.js:4263 |
| test6466 | `test6466_Machine_toMermaid_fanOut` | TEST6466: Machine to mermaid fan out | capdag.test.js:4275 |
| test6467 | `test6467_Machine_capRegistryEntry_construction` | Phase 0B: FabricRegistryClient tests | capdag.test.js:4295 |
| test6468 | `test6468_Machine_mediaRegistryEntry_construction` | TEST6468: Machine media registry entry construction | capdag.test.js:4319 |
| test6469 | `test6469_Machine_capRegistryClient_construction` | TEST6469: Machine cap registry client construction | capdag.test.js:4333 |
| test6470 | `test6470_Machine_capRegistryEntry_defaults` | TEST6470: Machine cap registry entry defaults | capdag.test.js:4341 |
| test6471 | `test6471_Renderer_cardinalityLabel_allFourCases` | TEST6471: Renderer cardinality label all four cases | capdag.test.js:4407 |
| test6472 | `test6472_Renderer_cardinalityLabel_usesUnicodeArrow` | TEST6472: Renderer cardinality label uses unicode arrow | capdag.test.js:4415 |
| test6473 | `test6473_Renderer_cardinalityFromCap_findsStdinArgNotFirstArg` | TEST6473: Renderer cardinality from cap finds stdin arg not first arg | capdag.test.js:4424 |
| test6474 | `test6474_Renderer_cardinalityFromCap_scalarDefaultsWhenFieldsMissing` | TEST6474: Renderer cardinality from cap scalar defaults when fields missing | capdag.test.js:4449 |
| test6475 | `test6475_Renderer_cardinalityFromCap_outputOnlySequence` | TEST6475: Renderer cardinality from cap output only sequence | capdag.test.js:4458 |
| test6476 | `test6476_Renderer_cardinalityFromCap_rejectsStringIsSequence` | TEST6476: Renderer cardinality from cap rejects string is sequence | capdag.test.js:4470 |
| test6478 | `test6478_Renderer_cardinalityFromCap_throwsOnNonObject` | TEST6478: Renderer cardinality from cap throws on non object | capdag.test.js:4484 |
| test6479 | `test6479_Renderer_canonicalMediaUrn_normalizesTagOrder` | TEST6479: Renderer canonical media urn normalizes tag order | capdag.test.js:4504 |
| test6480 | `test6480_Renderer_canonicalMediaUrn_preservesValueTags` | TEST6480: Renderer canonical media urn preserves value tags | capdag.test.js:4514 |
| test6481 | `test6481_Renderer_canonicalMediaUrn_rejectsCapUrn` | TEST6481: Renderer canonical media urn rejects cap urn | capdag.test.js:4520 |
| test6482 | `test6482_Renderer_mediaNodeLabel_rejectsUrnDerivedLabels` | TEST6482: Renderer media node label rejects urn derived labels | capdag.test.js:4533 |
| test6483 | `test6483_Renderer_buildBrowseGraphData_rejectsMissingMediaTitles` | TEST6483: Renderer build browse graph data rejects missing media titles | capdag.test.js:4548 |
| test6484 | `test6484_Renderer_validateStrandStep_rejectsUnknownVariant` | TEST6484: Renderer validate strand step rejects unknown variant | capdag.test.js:4606 |
| test6486 | `test6486_Renderer_validateStrandStep_requiresBooleanIsSequence` | TEST6486: Renderer validate strand step requires boolean is sequence | capdag.test.js:4624 |
| test6487 | `test6487_Renderer_classifyStrandCapSteps_capFlags` | TEST6487: Renderer classify strand cap steps cap flags | capdag.test.js:4647 |
| test6488 | `test6488_Renderer_classifyStrandCapSteps_nestedForks` | TEST6488: Renderer classify strand cap steps nested forks | capdag.test.js:4669 |
| test6489 | `test6489_Renderer_buildStrandGraphData_singleCapPlain` | TEST6489: Renderer build strand graph data single cap plain | capdag.test.js:4700 |
| test6491 | `test6491_Renderer_buildStrandGraphData_sequenceShowsCardinality` | TEST6491: Renderer build strand graph data sequence shows cardinality | capdag.test.js:4728 |
| test6492 | `test6492_Renderer_buildStrandGraphData_foreachCollectSpan` | TEST6492: Renderer build strand graph data foreach collect span | capdag.test.js:4749 |
| test6493 | `test6493_Renderer_buildStrandGraphData_standaloneCollect` | TEST6493: Renderer build strand graph data standalone collect | capdag.test.js:4801 |
| test6494 | `test6494_Renderer_buildStrandGraphData_unclosedForEachBody` | TEST6494: Renderer build strand graph data unclosed for each body | capdag.test.js:4829 |
| test6495 | `test6495_Renderer_buildStrandGraphData_nestedForEachThrows` | TEST6495: Renderer build strand graph data nested for each throws | capdag.test.js:4867 |
| test6496 | `test6496_Renderer_collapseStrand_singleCapBodyKeepsCapOwnLabel` | TEST6496: Renderer collapse strand single cap body keeps cap own label | capdag.test.js:4896 |
| test6497 | `test6497_Renderer_collapseStrand_unclosedForEachBodyCollapses` | TEST6497: Renderer collapse strand unclosed for each body collapses | capdag.test.js:4949 |
| test6498 | `test6498_Renderer_collapseStrand_standaloneCollectCollapses` | TEST6498: Renderer collapse strand standalone collect collapses | capdag.test.js:5006 |
| test6499 | `test6499_Renderer_collapseStrand_sequenceProducingCapBeforeForeach` | TEST6499: Renderer collapse strand sequence producing cap before foreach | capdag.test.js:5050 |
| test6500 | `test6500_Renderer_collapseStrand_plainCapMergesTrailingOutput` | TEST6500: Renderer collapse strand plain cap merges trailing output | capdag.test.js:5115 |
| test6501 | `test6501_Renderer_collapseStrand_plainCapDistinctTargetNoMerge` | TEST6501: Renderer collapse strand plain cap distinct target no merge | capdag.test.js:5152 |
| test6502 | `test6502_Renderer_validateStrandPayload_missingSourceMediaUrn` | TEST6502: Renderer validate strand payload missing source media urn | capdag.test.js:5179 |
| test6503 | `test6503_Renderer_validateBodyOutcome_rejectsNegativeIndex` | ---------------- run builder ---------------- | capdag.test.js:5192 |
| test6504 | `test6504_Renderer_buildRunGraphData_pagesSuccessesAndFailures` | TEST6504: Renderer build run graph data pages successes and failures | capdag.test.js:5203 |
| test6505 | `test6505_Renderer_buildRunGraphData_failureWithoutFailedCapRendersFullTrace` | TEST6505: Renderer build run graph data failure without failed cap renders full trace | capdag.test.js:5274 |
| test6506 | `test6506_Renderer_buildRunGraphData_usesCapUrnIsEquivalentForFailedCap` | TEST6506: Renderer build run graph data uses cap urn is equivalent for failed cap | capdag.test.js:5313 |
| test6507 | `test6507_Renderer_buildRunGraphData_backboneHasNoForeachNode` | TEST6507: Renderer build run graph data backbone has no foreach node | capdag.test.js:5373 |
| test6508 | `test6508_Renderer_buildRunGraphData_allFailedDropsTargetPlaceholder` | TEST6508: Renderer build run graph data all failed drops target placeholder | capdag.test.js:5428 |
| test6509 | `test6509_Renderer_buildRunGraphData_unclosedForeachSuccessNoMerge` | TEST6509: Renderer build run graph data unclosed foreach success no merge | capdag.test.js:5494 |
| test6510 | `test6510_Renderer_buildRunGraphData_closedForeachSuccessMergesAtCollectTarget` | TEST6510: Renderer build run graph data closed foreach success merges at collect target | capdag.test.js:5556 |
| test6511 | `test6511_Renderer_validateEditorGraphPayload_rejectsUnknownKind` | ---------------- editor-graph builder ---------------- | capdag.test.js:5611 |
| test6512 | `test6512_Renderer_buildEditorGraphData_collapsesCapsIntoLabeledEdges` | TEST6512: Renderer build editor graph data collapses caps into labeled edges | capdag.test.js:5626 |
| test6513 | `test6513_Renderer_buildEditorGraphData_loopMarkedEdgeGetsLoopClass` | TEST6513: Renderer build editor graph data loop marked edge gets loop class | capdag.test.js:5665 |
| test6514 | `test6514_Renderer_buildEditorGraphData_cardinalityFromDataSlotSequenceFlags` | TEST6514: Renderer build editor graph data cardinality from data slot sequence flags | capdag.test.js:5684 |
| test6515 | `test6515_Renderer_buildEditorGraphData_capWithoutCompleteArgsIsDropped` | TEST6515: Renderer build editor graph data cap without complete args is dropped | capdag.test.js:5704 |
| test6516 | `test6516_Renderer_buildEditorGraphData_rejectsEdgeWithMissingSource` | TEST6516: Renderer build editor graph data rejects edge with missing source | capdag.test.js:5722 |
| test6517 | `test6517_Renderer_buildResolvedMachineGraphData_singleStrandLinearChain` | ---------------- resolved-machine builder ---------------- | capdag.test.js:5738 |
| test6518 | `test6518_Renderer_buildResolvedMachineGraphData_loopEdgeGetsLoopClass` | TEST6518: Renderer build resolved machine graph data loop edge gets loop class | capdag.test.js:5797 |
| test6519 | `test6519_Renderer_buildResolvedMachineGraphData_fanInProducesEdgePerAssignment` | TEST6519: Renderer build resolved machine graph data fan in produces edge per assignment | capdag.test.js:5832 |
| test6520 | `test6520_Renderer_buildResolvedMachineGraphData_multiStrandKeepsStrandsDisjoint` | TEST6520: Renderer build resolved machine graph data multi strand keeps strands disjoint | capdag.test.js:5873 |
| test6521 | `test6521_Renderer_buildResolvedMachineGraphData_duplicateNodeIdAcrossStrandsFailsHard` | TEST6521: Renderer build resolved machine graph data duplicate node id across strands fails hard | capdag.test.js:5936 |
| test6522 | `test6522_Renderer_validateResolvedMachinePayload_rejectsMissingFields` | TEST6522: Renderer validate resolved machine payload rejects missing fields | capdag.test.js:5972 |
| test6544 | `test6544_builderRejectsStructuralKeys` | TEST6544: builder rejects structural keys on tag/marker | capdag.test.js:2973 |
| test6550 | `test6550_cartridgeInfoConstruction` | TEST320-335: CartridgeRepoServer and CartridgeRepoClient tests | capdag.test.js:2010 |
| test6557 | `test6557_cartridgeRepoServerTransformToArray` | TEST6557: CartridgeRepoServer walks both channels and emits a flat CartridgeInfo array preserving channel provenance. Release entries appear first. | capdag.test.js:2129 |
| test6563 | `test6563_cartridgeRepoServerSearchCartridges` | TEST6563: CartridgeRepoServer.searchCartridges() filters across both channels by name/description/tags/cap titles. Cap URN strings are not substring-matched. | capdag.test.js:2213 |
| test6565 | `test6565_cartridgeRepoServerGetByCategory` | TEST6565: CartridgeRepoServer.getCartridgesByCategory() filters cartridges by category across both channels. | capdag.test.js:2235 |
| test6568 | `test6568_cartridgeRepoServerGetByCap` | TEST6568: CartridgeRepoServer.getCartridgesByCap() parses the input URN and matches each declared cap via `conformsTo`. Tag-order differences resolve because matching is order-theoretic, not string. | capdag.test.js:2254 |
| test6570 | `test6570_cartridgeRepoClientUpdateCache` | TEST6570: CartridgeRepoClient updates its local cache keyed by "<channel>:<id>". The cache holds release and nightly entries independently — the same id is allowed in both. | capdag.test.js:2271 |
| test6572 | `test6572_cartridgeRepoClientGetSuggestions` | TEST6572: CartridgeRepoClient.getSuggestionsForCap() returns cartridge suggestions with channel propagated onto each suggestion. | capdag.test.js:2299 |
| test6575 | `test6575_cartridgeRepoClientGetCartridge` | TEST6575: CartridgeRepoClient.getCartridge() requires (channel, id). Same id in the wrong channel must miss. | capdag.test.js:2329 |
| test6577 | `test6577_cartridgeRepoClientGetAllCaps` | TEST6577: CartridgeRepoClient.getAllAvailableCaps() returns the set of normalized URNs across both channels. | capdag.test.js:2374 |
| test6582 | `test6582_cartridgeRepoServerClientIntegration` | TEST6582: Round-trip: server produces a v5.0 response, client consumes it, channel provenance is preserved end-to-end. | capdag.test.js:2410 |
| test6620 | `test6620_wildcardGenericFormsRejected` | TEST6620: Generic top-to-top spellings are all rejected. | capdag.test.js:3154 |
| test6621 | `test6621_capIdentityConstantWorks` | TEST6621: CAP_IDENTITY constant names the true identity cap, not bare cap: | capdag.test.js:3175 |
| test6733 | `test6733_truthTableFullCrossProduct` | TEST6733: Full 6×6 truth table. | capdag.test.js:6285 |
| test6737 | `test6737_capVersionZeroOmittedOnWire` | TEST6737: Cap with version=0 round-trips with no `version` key on wire | capdag.test.js:6360 |
| test6738 | `test6738_registryUrlFromBuildEnvPassesThroughNonempty` | TEST6738: a non-empty MFR_CARTRIDGE_REGISTRY_URL passes through verbatim — a published build reports exactly the URL it was compiled with. | capdag.test.js:2582 |
| test6740 | `test6740_registryUrlFromBuildEnvNoneForDev` | TEST6740: an unset env (null/undefined) yields null — a dev build has no baked registry and loads only `dev/` cartridges. | capdag.test.js:2589 |
---

## Numbering Mismatches

These tests have a numbering disagreement between the function name and the authoritative immediate TEST comment/docstring above the test. This is reported explicitly so comment sync does not silently overwrite a misnumbered test.

- `test6240` / `test0070` / `test6240_JS_getExtensionMappings` — capdag.test.js:1712
- `test6242` / `test0073` / `test6242_JS_resolveMediaUrnFromSpecs` — capdag.test.js:1723
- `test6277` / `test0088` / `test6277_Machine_whitespaceOnly` — capdag.test.js:3249
- `test6279` / `test0089` / `test6279_Machine_headerOnlyNoWirings` — capdag.test.js:3254
- `test6280` / `test0090` / `test6280_Machine_duplicateAlias` — capdag.test.js:3262
- `test6286` / `test0094` / `test6286_Machine_simpleLinearChain` — capdag.test.js:3274
- `test6288` / `test0095` / `test6288_Machine_twoStepChain` — capdag.test.js:3290
- `test6290` / `test0096` / `test6290_Machine_fanOut` — capdag.test.js:3305
- `test6292` / `test0097` / `test6292_Machine_fanInSecondaryAssignedByPriorWiring` — capdag.test.js:3323
- `test6294` / `test0098` / `test6294_Machine_fanInSecondaryUnassignedGetsWildcard` — capdag.test.js:3337

---

*Generated from CapDag-JS source tree*
*Total tests: 348*
*Total numbered tests: 348*
*Total unnumbered tests: 0*
*Total numbered tests missing descriptions: 0*
*Total numbering mismatches: 10*

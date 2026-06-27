# CapDag-JS Test Catalog

**Total Tests:** 348

**Numbered Tests:** 348

**Unnumbered Tests:** 0

**Numbered Tests Missing Descriptions:** 0

**Numbering Mismatches:** 74

All numbered test numbers are unique.

This catalog lists all tests in the CapDag-JS codebase.

| Test # | Function Name | Description | File |
|--------|---------------|-------------|------|
| test001 | `test001_capUrnCreation` | TEST1: Test that cap URN is created with tags parsed correctly and direction specs accessible | capdag.test.js:143 |
| test002 | `test002_directionSpecsRequired` | TEST2: Test that missing 'in' or 'out' defaults to media: wildcard | capdag.test.js:153 |
| test003 | `test003_directionMatching` | TEST3: Test that direction specs must match exactly, different in/out types don't match, wildcard matches any | capdag.test.js:164 |
| test004 | `test004_unquotedValuesLowercased` | TEST4: Test that unquoted keys and values are normalized to lowercase | capdag.test.js:179 |
| test005 | `test005_quotedValuesPreserveCase` | TEST5: Test that quoted values preserve case while unquoted are lowercased | capdag.test.js:187 |
| test006 | `test006_quotedValueSpecialChars` | TEST6: Test that quoted values can contain special characters (semicolons, equals, spaces) | capdag.test.js:193 |
| test007 | `test007_quotedValueEscapeSequences` | TEST7: Test that escape sequences in quoted values (\" and \\) are parsed correctly | capdag.test.js:199 |
| test008 | `test008_mixedQuotedUnquoted` | TEST8: Test that mixed quoted and unquoted values in same URN parse correctly | capdag.test.js:206 |
| test009 | `test009_unterminatedQuoteError` | TEST9: Test that unterminated quote produces UnterminatedQuote error | capdag.test.js:213 |
| test010 | `test010_invalidEscapeSequenceError` | TEST10: Test that invalid escape sequences (like \n, \x) produce InvalidEscapeSequence error | capdag.test.js:226 |
| test011 | `test011_serializationSmartQuoting` | TEST11: Test that serialization uses smart quoting (no quotes for simple lowercase, quotes for special chars/uppercase) | capdag.test.js:240 |
| test012 | `test012_roundTripSimple` | TEST12: Test that simple cap URN round-trips (parse -> serialize -> parse equals original) | capdag.test.js:249 |
| test013 | `test013_roundTripQuoted` | TEST13: Test that quoted values round-trip preserving case and spaces | capdag.test.js:257 |
| test014 | `test014_roundTripEscapes` | TEST14: Test that escape sequences round-trip correctly | capdag.test.js:266 |
| test015 | `test015_capPrefixRequired` | TEST15: Test that cap: prefix is required and case-insensitive | capdag.test.js:276 |
| test016 | `test016_trailingSemicolonEquivalence` | TEST16: Test that trailing semicolon is equivalent (same hash, same string, matches) | capdag.test.js:288 |
| test017 | `test017_tagMatching` | TEST17: Test tag matching: exact match, subset match, wildcard match, value mismatch | capdag.test.js:324 |
| test018 | `test018_matchingCaseSensitiveValues` | TEST18: Test that quoted values with different case do NOT match (case-sensitive) | capdag.test.js:348 |
| test019 | `test019_missingTagHandling` | TEST19: Missing tag in instance causes rejection — pattern's tags are constraints | capdag.test.js:355 |
| test020 | `test020_specificity` | TEST020: Specificity is the sum of per-tag truth-table scores across in/out/y. Marker tags (bare segments and `key=*`) score 2 (must-have-any), exact `key=value` tags score 3, missing/`?` score 0, `!` scores 1. test6204_Urn() builds "cap:in=media:void;out=media:record;<tags>" so the directional baseline is: in:  media:void   -> {void=*}    -> 2 out: media:record -> {record=*}  -> 2 Total directional baseline: 4. | capdag.test.js:377 |
| test021 | `test021_builder` | TEST21: Test builder creates cap URN with correct tags and direction specs | capdag.test.js:405 |
| test022 | `test022_builderRequiresDirection` | TEST22: Test builder requires both in_spec and out_spec | capdag.test.js:419 |
| test023 | `test023_builderPreservesCase` | TEST23: Test builder lowercases keys but preserves value case | capdag.test.js:433 |
| test024 | `test024_compatibility` | TEST24: Directional accepts — pattern's tags are constraints, instance must satisfy | capdag.test.js:444 |
| test025 | `test025_bestMatch` | TEST25: Test find_best_match returns most specific matching cap | capdag.test.js:464 |
| test026 | `test026_mergeAndSubset` | TEST26: Test merge combines tags from both caps, subset keeps only specified tags | capdag.test.js:477 |
| test027 | `test027_wildcardTag` | TEST27: Test with_wildcard_tag sets tag to wildcard, including in/out | capdag.test.js:496 |
| test028 | `test028_emptyCapUrnNotAllowed` | TEST28: Test empty cap URN is illegal after effect transition | capdag.test.js:509 |
| test029 | `test029_minimalCapUrn` | TEST29: Test minimal valid cap URN has just in and out, empty tags | capdag.test.js:518 |
| test030 | `test030_extendedCharacterSupport` | TEST30: Test extended characters (forward slashes, colons) in tag values | capdag.test.js:526 |
| test031 | `test031_wildcardRestrictions` | TEST31: Test wildcard rejected in keys but accepted in values | capdag.test.js:533 |
| test032 | `test032_duplicateKeyRejection` | TEST32: Test duplicate keys are rejected with DuplicateKey error | capdag.test.js:551 |
| test033 | `test033_numericKeyRestriction` | TEST33: Test pure numeric keys rejected, mixed alphanumeric allowed, numeric values allowed | capdag.test.js:560 |
| test034 | `test034_emptyValueError` | TEST34: Test empty values are rejected | capdag.test.js:574 |
| test035 | `test035_hasTagCaseSensitive` | TEST35: Test has_tag is case-sensitive for values, case-insensitive for keys, works for in/out | capdag.test.js:587 |
| test036 | `test036_withTagPreservesValue` | TEST36: Test with_tag preserves value case | capdag.test.js:599 |
| test037 | `test037_withTagRejectsEmptyValue` | TEST37: Test with_tag rejects empty value | capdag.test.js:606 |
| test038 | `test038_semanticEquivalence` | TEST38: Test semantic equivalence of unquoted and quoted simple lowercase values | capdag.test.js:616 |
| test039 | `test039_getTagReturnsDirectionSpecs` | TEST39: Test get_tag returns direction specs (in/out) with case-insensitive lookup | capdag.test.js:624 |
| test040 | `test040_matchingSemanticsExactMatch` | TEST40: Matching semantics - exact match succeeds | capdag.test.js:633 |
| test041 | `test041_matchingSemanticsCapMissingTag` | TEST41: Matching semantics - cap missing tag matches (implicit wildcard) | capdag.test.js:640 |
| test042 | `test042_matchingSemanticsCapHasExtraTag` | TEST42: Pattern rejects instance missing required tags | capdag.test.js:648 |
| test043 | `test043_matchingSemanticsRequestHasWildcard` | TEST43: Matching semantics - request wildcard matches specific cap value | capdag.test.js:656 |
| test044 | `test044_matchingSemanticsCapHasWildcard` | TEST44: Matching semantics - cap wildcard matches specific request value | capdag.test.js:663 |
| test045 | `test045_matchingSemanticsValueMismatch` | TEST45: Matching semantics - value mismatch does not match | capdag.test.js:670 |
| test046 | `test046_matchingSemanticsFallbackPattern` | TEST46: Matching semantics - fallback pattern (cap missing tag = implicit wildcard) | capdag.test.js:677 |
| test047 | `test047_matchingSemanticsThumbnailVoidInput` | TEST47: Matching semantics - thumbnail fallback with void input | capdag.test.js:685 |
| test048 | `test048_matchingSemanticsWildcardDirection` | TEST48: Matching semantics - wildcard direction matches anything | capdag.test.js:692 |
| test049 | `test049_matchingSemanticsCrossDimension` | TEST49: Non-overlapping tags — neither direction accepts | capdag.test.js:699 |
| test050 | `test050_matchingSemanticsDirectionMismatch` | TEST50: Matching semantics - direction mismatch prevents matching | capdag.test.js:707 |
| test060 | `test060_wrongPrefixFails` | TEST60: Test wrong prefix fails with InvalidPrefix error showing expected and actual prefix | capdag.test.js:852 |
| test062 | `test062_isRecord` | TEST62: Test is_record returns true when record marker tag is present indicating key-value structure | capdag.test.js:865 |
| test063 | `test063_isScalar` | TEST63: Test is_scalar returns true when list marker tag is absent (scalar is default) | capdag.test.js:876 |
| test064 | `test064_isList` | TEST64: Test is_list returns true when list marker tag is present indicating ordered collection | capdag.test.js:889 |
| test065 | `test065_isOpaque` | TEST65: Test is_opaque returns true when record marker is absent (opaque is default) | capdag.test.js:898 |
| test066 | `test066_isJson` | TEST66: Test is_json returns true only when json marker tag is present for JSON representation | capdag.test.js:909 |
| test067 | `test067_isText` | TEST67: Text-representability is now carried by the orthogonal `enc=` tag (the old `textable` marker and is_text() are gone). A media is "text" iff it declares an encoding. enc is orthogonal to format/numeric, so only media that actually carry enc= are text. | capdag.test.js:918 |
| test068 | `test068_isVoid` | TEST68: Test is_void returns true when void flag or type=void tag is present | capdag.test.js:931 |
| test071 | `test071_toStringRoundtrip` | TEST71: Test to_string roundtrip ensures serialization and deserialization preserve URN structure | capdag.test.js:939 |
| test072 | `test072_constantsParse` | TEST72: Test all media URN constants parse successfully as valid media URNs | capdag.test.js:949 |
| test074 | `test074_mediaUrnMatching` | TEST74: Test media URN conforms_to using tagged URN semantics with specific and generic requirements | capdag.test.js:969 |
| test075 | `test075_accepts` | TEST75: Test accepts with implicit wildcards where handlers with fewer tags can handle more requests | capdag.test.js:983 |
| test076 | `test076_specificity` | TEST76: Test specificity increases with more tags for ranking conformance | capdag.test.js:994 |
| test077 | `test077_serdeRoundtrip` | TEST77: Test serde roundtrip serializes to JSON string and deserializes back correctly | capdag.test.js:1003 |
| test078 | `test078_debugMatchingBehavior` | TEST78: conforms_to behavior between MEDIA_OBJECT and MEDIA_STRING | capdag.test.js:1012 |
| test93 | `test93_resolveUnresolvableFailsHard` | TEST93: Test resolving unknown media URN fails with UnresolvableMediaUrn error | capdag.test.js:1054 |
| test99 | `test99_resolvedIsBinary` | TEST99: Test ResolvedMediaDef is_binary returns true when enc tag is absent | capdag.test.js:1073 |
| test100 | `test100_resolvedIsRecord` | TEST100: Test ResolvedMediaDef is_record returns true when record marker is present | capdag.test.js:1079 |
| test101 | `test101_resolvedIsScalar` | TEST101: Test ResolvedMediaDef is_scalar returns true when list marker is absent | capdag.test.js:1085 |
| test102 | `test102_resolvedIsList` | TEST102: Test ResolvedMediaDef is_list returns true when list marker is present | capdag.test.js:1091 |
| test103 | `test103_resolvedIsJson` | TEST103: Test ResolvedMediaDef is_json returns true when json tag is present | capdag.test.js:1097 |
| test104 | `test104_resolvedIsText` | TEST104: Test ResolvedMediaDef is_text returns true when enc tag is present | capdag.test.js:1103 |
| test105 | `test105_metadataPropagation` | TEST105: Test metadata propagates from media def def to resolved media def | capdag.test.js:1109 |
| test106 | `test106_metadataWithValidation` | TEST106: Test metadata and validation can coexist in media definition | capdag.test.js:1132 |
| test107 | `test107_extensionsPropagation` | TEST107: Test extensions field propagates from media def def to resolved | capdag.test.js:1151 |
| test108 | `test108_extensionsSerialization` | TEST108: Test creating new cap with URN, title, and command verifies correct initialization | capdag.test.js:1167 |
| test109 | `test109_extensionsWithMetadataAndValidation` | TEST109: Test creating cap with metadata initializes and retrieves metadata correctly | capdag.test.js:1175 |
| test110 | `test110_multipleExtensions` | TEST110: Test cap matching with subset semantics for request fulfillment | capdag.test.js:1194 |
| test115 | `test115_capArgSerialization` | TEST115: Test CapArg serialization and deserialization with multiple sources | capdag.test.js:1210 |
| test116 | `test116_capArgConstructors` | TEST116: Test CapArg constructor methods basic and with_description create args correctly | capdag.test.js:1243 |
| test125 | `test125_effectNonePreservesRuntimeMedia` | TEST125: effect=none preserves runtime media identity | capdag.test.js:3163 |
| test126 | `test126_effectDeclaredUsesDeclaredOutput` | TEST126: default effect=declared uses the declared output | capdag.test.js:3172 |
| test127 | `test127_invalidEffectNoneFailsHard` | TEST127: invalid effect=none declarations fail hard | capdag.test.js:3183 |
| test128 | `test128_effectDispatchRequiresExplicitWildcard` | TEST128: omitted effect means declared; unconstrained effect must be explicit | capdag.test.js:3192 |
| test150 | `test150_capManifestJsonSerialization` | TEST150: JSON roundtrip | capdag.test.js:1271 |
| test156 | `test156_stdinSourceFromData` | TEST156: Test creating StdinSource Data variant with byte vector | capdag.test.js:1427 |
| test157 | `test157_stdinSourceFromFileReference` | TEST157: Test creating StdinSource FileReference variant with all required fields | capdag.test.js:1438 |
| test158 | `test158_stdinSourceWithEmptyData` | TEST158: Test StdinSource Data with empty vector stores and retrieves correctly | capdag.test.js:1455 |
| test159 | `test159_stdinSourceWithBinaryContent` | TEST159: Test StdinSource Data with binary content like PNG header bytes | capdag.test.js:1463 |
| test274 | `test274_capArgumentValueNew` | TEST274: Test CapArgumentValue::new stores media_urn and raw byte value | capdag.test.js:1477 |
| test275 | `test275_capArgumentValueFromStr` | TEST275: Test CapArgumentValue::from_str converts string to UTF-8 bytes | capdag.test.js:1484 |
| test276 | `test276_capArgumentValueAsStrValid` | TEST276: Test CapArgumentValue::value_as_str succeeds for UTF-8 data | capdag.test.js:1491 |
| test277 | `test277_capArgumentValueAsStrInvalidUtf8` | TEST277: Test CapArgumentValue::value_as_str fails for non-UTF-8 binary data | capdag.test.js:1497 |
| test278 | `test278_capArgumentValueEmpty` | TEST278: Test CapArgumentValue::new with empty value stores empty vec | capdag.test.js:1509 |
| test282 | `test282_capArgumentValueUnicode` | TEST282: Test CapArgumentValue::from_str with Unicode string preserves all characters | capdag.test.js:1518 |
| test283 | `test283_capArgumentValueLargeBinary` | TEST283: Test CapArgumentValue with large binary payload preserves all bytes | capdag.test.js:1524 |
| test304 | `test304_mediaAvailabilityOutputConstant` | TEST304: Test MEDIA_AVAILABILITY_OUTPUT constant parses as valid media URN with correct tags | capdag.test.js:1543 |
| test305 | `test305_mediaPathOutputConstant` | TEST305: Test MEDIA_PATH_OUTPUT constant parses as valid media URN with correct tags | capdag.test.js:1552 |
| test306 | `test306_availabilityAndPathOutputDistinct` | TEST306: Test MEDIA_AVAILABILITY_OUTPUT and MEDIA_PATH_OUTPUT are distinct URNs | capdag.test.js:1561 |
| test307 | `test307_modelAvailabilityUrn` | TEST307: Test model_availability_urn builds valid cap URN with correct op and media defs | capdag.test.js:1575 |
| test308 | `test308_modelPathUrn` | TEST308: Test model_path_urn builds valid cap URN with correct op and media defs | capdag.test.js:1587 |
| test309 | `test309_modelAvailabilityAndPathAreDistinct` | TEST309: Test model_availability_urn and model_path_urn produce distinct URNs | capdag.test.js:1599 |
| test310 | `test310_llmGenerateTextUrn` | TEST310: llm_generate_text_urn() produces a valid cap URN with a UTF-8 text input and plain-text terminal output. | capdag.test.js:1606 |
| test312 | `test312_allUrnBuildersProduceValidUrns` | TEST312: Test all URN builders produce parseable cap URNs | capdag.test.js:1629 |
| test320 | `test320_cartridgeInfoConstruction` | TEST320-335: CartridgeRepoServer and CartridgeRepoClient tests | capdag.test.js:1993 |
| test321 | `test321_cartridgeInfoIsSigned` | TEST321: CartridgeInfo.is_signed() returns true when signature (team_id + signed_at) is present, false when either is empty. | capdag.test.js:2027 |
| test322 | `test322_cartridgeInfoBuildForPlatform` | TEST322: CartridgeInfo.build_for_platform() returns the build that matches the requested platform string and None otherwise. | capdag.test.js:2039 |
| test323 | `test323_cartridgeRepoServerValidateRegistry` | TEST323: CartridgeRepoServer requires schema 5.0 and rejects older. | capdag.test.js:2073 |
| test324 | `test324_cartridgeRepoServerTransformToArray` | TEST324: CartridgeRepoServer transforms a v4.0 entry into a flat CartridgeInfo, preserving cap_groups verbatim. | capdag.test.js:2110 |
| test325 | `test325_cartridgeRepoServerGetCartridges` | TEST325: get_cartridges() wraps the transformed array in the response envelope. | capdag.test.js:2147 |
| test326 | `test326_cartridgeRepoServerGetCartridgeById` | TEST326: get_cartridge_by_id requires a channel and returns Some for a known (channel, id), None otherwise. The same id looked up in the wrong channel must miss — channels are independent namespaces. | capdag.test.js:2159 |
| test327 | `test327_cartridgeRepoServerSearchCartridges` | TEST327: search_cartridges matches against name/description/tags and cap titles, but never against cap URN strings. | capdag.test.js:2189 |
| test328 | `test328_cartridgeRepoServerGetByCategory` | TEST328: CartridgeRepoServer.getCartridgesByCategory() filters cartridges by category across both channels. | capdag.test.js:2211 |
| test329 | `test329_cartridgeRepoServerGetByCap` | TEST329: CartridgeRepoServer.getCartridgesByCap() parses the input URN and matches each declared cap via `conformsTo`. Tag-order differences resolve because matching is order-theoretic, not string. | capdag.test.js:2230 |
| test330 | `test330_cartridgeRepoClientUpdateCache` | TEST330: CartridgeRepoClient updates its local cache keyed by "<channel>:<id>". The cache holds release and nightly entries independently — the same id is allowed in both. | capdag.test.js:2247 |
| test331 | `test331_cartridgeRepoClientGetSuggestions` | TEST331: CartridgeRepoClient.getSuggestionsForCap() returns cartridge suggestions with channel propagated onto each suggestion. | capdag.test.js:2275 |
| test332 | `test332_cartridgeRepoClientGetCartridge` | TEST332: get_cartridge requires a (channel, id) pair and returns the cached entry for known pairs, None otherwise. The same id in the wrong channel must miss. | capdag.test.js:2304 |
| test333 | `test333_cartridgeRepoClientGetAllCaps` | TEST333: get_all_available_caps returns the deduplicated set of normalized URNs across cartridges. | capdag.test.js:2348 |
| test334 | `test334_cartridgeRepoClientNeedsSync` | TEST334: needs_sync returns true on an empty cache, false right after a successful update. | capdag.test.js:2364 |
| test335 | `test335_cartridgeRepoServerClientIntegration` | TEST335: Round-trip: server produces a v5.0 response, client consumes it, channel provenance is preserved end-to-end. | capdag.test.js:2383 |
| test546 | `test546_isImage` | TEST546: is_image returns true only when image marker tag is present | capdag.test.js:2719 |
| test547 | `test547_isAudio` | TEST547: is_audio returns true only when audio marker tag is present | capdag.test.js:2731 |
| test548 | `test548_isVideo` | TEST548: is_video returns true only when video marker tag is present | capdag.test.js:2742 |
| test549 | `test549_isNumeric` | TEST549: is_numeric returns true only when numeric marker tag is present | capdag.test.js:2752 |
| test550 | `test550_isBool` | TEST550: is_bool returns true only when bool marker tag is present | capdag.test.js:2764 |
| test551 | `test551_isFilePath` | TEST551: is_file_path returns true for the single file-path media URN, false for everything else. There is no "array" variant — cardinality is carried by is_sequence on the wire, not by URN tags. | capdag.test.js:2776 |
| test558 | `test558_predicateConstantConsistency` | TEST558: predicates are consistent with constants — every constant triggers exactly the expected predicates | capdag.test.js:2795 |
| test559 | `test559_withoutTag` | TEST559: without_tag removes tag, rejects structural keys, case-insensitive for keys | capdag.test.js:2834 |
| test560 | `test560_withInOutSpec` | TEST560: with_in_spec and with_out_spec change direction specs | capdag.test.js:2854 |
| test563 | `test563_findAllMatches` | TEST563: CapMatcher::find_all_matches returns all matching caps sorted by specificity | capdag.test.js:2884 |
| test564 | `test564_areCompatible` | TEST564: CapMatcher::are_compatible detects bidirectional overlap | capdag.test.js:2902 |
| test566 | `test566_withTagRejectsStructuralKeys` | TEST566: with_tag rejects structural keys | capdag.test.js:2927 |
| test597 | `test597_capArgWithFullDefinition` | TEST597: CapArg::with_full_definition stores all fields including optional ones | capdag.test.js:1327 |
| test640 | `test640_inOnlyIsIllegal` | TEST640: cap:in defaults to the same illegal bare top form | capdag.test.js:3019 |
| test641 | `test641_outOnlyIsIllegal` | TEST641: cap:out defaults to the same illegal bare top form | capdag.test.js:3028 |
| test642 | `test642_inOutWithoutValuesAreIllegal` | TEST642: cap:in;out becomes the same illegal bare top form | capdag.test.js:3037 |
| test643 | `test643_explicitAsteriskIsIllegal` | TEST643: cap:in=*;out=* is the same illegal bare top form | capdag.test.js:3046 |
| test644 | `test644_specificInWildcardOutIsIllegal` | TEST644: cap:in=media:;out=* is the same illegal bare top form | capdag.test.js:3055 |
| test645 | `test645_wildcardInSpecificOut` | TEST645: cap:in=*;out=media:text has wildcard in, specific out | capdag.test.js:3064 |
| test646 | `test646_invalidInSpecFails` | TEST646: cap:in=foo fails (invalid media URN) | capdag.test.js:3071 |
| test647 | `test647_invalidOutSpecFails` | TEST647: cap:in=media:;out=bar fails (invalid media URN) | capdag.test.js:3080 |
| test648 | `test648_wildcardAcceptsSpecific` | TEST648: Wildcard in/out match specific caps | capdag.test.js:3089 |
| test649 | `test649_specificityScoring` | TEST649: Specificity - wildcard has 0, specific has tag count | capdag.test.js:3098 |
| test650 | `test650_wildcardPreserveOtherTags` | TEST650: cap:in=media:;out=media:;test preserves other tags | capdag.test.js:3107 |
| test653 | `test653_invalidEffectNoneDeclarationRejected` | TEST653: invalid effect=none declarations fail at construction | capdag.test.js:3154 |
| test890 | `test890_directionSemanticMatching` | TEST890: Semantic direction matching - generic provider matches specific request | capdag.test.js:718 |
| test891 | `test891_directionSemanticSpecificity` | TEST891: Semantic direction specificity — more constraints in either axis means a higher score under the truth-table-driven sum. media: (top, no tags) scores 0; each marker tag scores 2; each exact tag scores 3. | capdag.test.js:768 |
| test939 | `test939_capUrnCanonicalFormDropsWildcardInOut` | TEST939: The canonical form drops `in=media:` and `out=media:` segments. Every spelling of "the same cap with wildcard in/out" collapses to one byte-identical canonical string. This is the contract that makes registry lookups work: the cap-publisher hashes `<canonical-urn>` to compute the cache key, and every language port (Rust, Go, Python, JS, ObjC) must agree on the canonical form for cross-language lookups to land on the same key. A regression that emitted the wildcard segments would silently move the published cap to a different SHA-256 bucket, 404'ing every reader that hashes the canonical form. | capdag.test.js:296 |
| test1294 | `test1294_rule11VoidInputWithStdinRejected` | TEST1294: RULE11 - void-input cap with stdin source rejected | capdag.test.js:2954 |
| test1295 | `test1295_rule11NonVoidInputWithoutStdinRejected` | TEST1295: RULE11 - non-void-input cap without stdin source rejected | capdag.test.js:2969 |
| test1296 | `test1296_rule11VoidInputCliFlagOnly` | TEST1296: RULE11 - void-input cap with only cli_flag sources passes | capdag.test.js:2984 |
| test1297 | `test1297_rule11NonVoidInputWithStdin` | TEST1297: RULE11 - non-void-input cap with stdin source passes | capdag.test.js:2994 |
| test1800 | `test1800_kindIdentityOnlyForBareCap` | TEST1800: Identity classifier — and only explicit effect=none qualifies. | capdag.test.js:5976 |
| test1801 | `test1801_kindSourceWhenInputIsVoid` | TEST1801: Source classifier — in=media:void, out non-void. | capdag.test.js:6003 |
| test1802 | `test1802_kindSinkWhenOutputIsVoid` | TEST1802: Sink classifier — out=media:void, in non-void. | capdag.test.js:6012 |
| test1803 | `test1803_kindEffectWhenBothSidesVoid` | TEST1803: Effect classifier — both sides void. Reads as `() → ()`. | capdag.test.js:6021 |
| test1804 | `test1804_kindTransformForNormalDataProcessors` | TEST1804: Transform classifier — at least one side non-void, and the cap is not the bare identity. The default kind for ordinary data-processing caps. | capdag.test.js:6031 |
| test1805 | `test1805_kindInvariantUnderCanonicalSpellings` | TEST1805: Kind is invariant under canonicalization. The same morphism written in many surface forms must classify the same way once parsed. This pins the rule that kind is a property of the cap as a structured object, not of any particular spelling. | capdag.test.js:6074 |
| test1810 | `test1810_mediaVoidIsAtomic` | TEST1810: media:void is atomic — refinements are parse errors. Mirrored across every language port (Rust, Go, Python, Swift/ObjC, JS) under the SAME number. Any divergence is a wire-level inconsistency — the unit type's atomicity is part of the protocol's deepest layer, not a per-port detail. The bare `media:void` parses successfully; any combination with another tag (marker or key=value) MUST fail with VoidNotAtomic. This forecloses a fake taxonomy of unit values; reasons or labels for *why* void is used belong on the cap URN's non-directional tags or in cap args. | capdag.test.js:6041 |
| test1820 | `test1820_specificityQuestionIsZero` | TEST1820: A `?`-valued cap-tag scores 0. Same as missing. | capdag.test.js:6115 |
| test1821 | `test1821_specificityMustNotHaveIsFive` | TEST1821: A `!`-valued cap-tag scores 5 (top of negative chain). | capdag.test.js:6125 |
| test1822 | `test1822_specificityMustHaveAnyIsTwo` | TEST1822: A `*`-valued cap-tag (including bare markers) scores 2. | capdag.test.js:6132 |
| test1823 | `test1823_specificityExactValueIsFour` | TEST1823: An exact-valued cap-tag scores 4. | capdag.test.js:6146 |
| test1824 | `test1824_specificityCombinedYAxis` | TEST1824: All six forms compose additively on a single cap. This pins the truth-table sum across the y axis as a whole. | capdag.test.js:6153 |
| test1830 | `test1830_canonicalizeNoConstraint` | TEST1830: ?x ≡ x? ≡ x=? all canonicalize to ?x. | capdag.test.js:6164 |
| test1831 | `test1831_canonicalizeAbsentOrNotValue` | TEST1831: ?x=v and x?=v both canonicalize to x?=v. The third hypothetical form `x=?v` is NOT recognized as a qualifier — a value starting with `?` is just an exact value beginning with a `?` character. | capdag.test.js:6174 |
| test1832 | `test1832_canonicalizeMustHaveAny` | TEST1832: x ≡ x=* both canonicalize to bare x. | capdag.test.js:6190 |
| test1833 | `test1833_canonicalizePresentNotValue` | TEST1833: !x=v and x!=v both canonicalize to x!=v. The third hypothetical form `x=!v` is NOT recognized as a qualifier — a value starting with `!` is just an exact value beginning with a `!` character. | capdag.test.js:6200 |
| test1834 | `test1834_canonicalizeExactValue` | TEST1834: x=v stays as x=v (the lone exact-value form). | capdag.test.js:6216 |
| test1835 | `test1835_canonicalizeMustNotHave` | TEST1835: !x ≡ x! ≡ x=! all canonicalize to !x. | capdag.test.js:6222 |
| test1842 | `test1842_truthTableFullCrossProduct` | TEST1842: Full 6×6 truth table. | capdag.test.js:6232 |
| test1845 | `test1845_axisWeightingInDominatesY` | TEST1845: With equal out-axis, in-axis dominates over y-axis. | capdag.test.js:6285 |
| test1848 | `test1848_capVersionNonZeroOnWire` | TEST1848: Cap with version=N round-trips with `version: N` on wire | capdag.test.js:6319 |
| test1849 | `test1849_resolveForHostCompatibleLatest` | TEST1849: latest version has a host build → Compatible, resolving to the latest version and that platform's native-format package. | capdag.test.js:2466 |
| test1850 | `test1850_resolveForHostCompatibleOutdated` | TEST1850: the latest version lacks a host build but an older version has one → CompatibleOutdated, resolving to the older version with a reason naming both the latest and the resolved version. | capdag.test.js:2482 |
| test1851 | `test1851_resolveForHostIncompatible` | TEST1851: no version ships a host build → Incompatible, no resolved version/package, reason states the host platform. | capdag.test.js:2499 |
| test1852 | `test1852_resolveForHostSkipsBuildWithNoInstaller` | TEST1852: a host build whose packages[] is empty AND has no legacy `package` ships no installer; resolution must SKIP it (not resolve to an un-downloadable version) and fall through to an older usable version. | capdag.test.js:2513 |
| test1853 | `test1853_hostPlatformNormalizedForm` | TEST1853: host_platform() returns a normalized {os}-{arch} string with arch aarch64 mapped to arm64 — the exact form the registry uses. | capdag.test.js:2531 |
| test1872 | `test1872_registryUrlFromBuildEnvPassesThroughNonempty` | TEST1872: a non-empty MFR_CARTRIDGE_REGISTRY_URL passes through verbatim — a published build reports exactly the URL it was compiled with. | capdag.test.js:2548 |
| test1873 | `test1873_registryUrlFromBuildEnvNoneForDev` | TEST1873: an unset env (null/undefined) yields null — a dev build has no baked registry and loads only `dev/` cartridges. | capdag.test.js:2555 |
| test1874 | `test1874_registryUrlFromBuildEnvRejectsEmptyString` | TEST1874: an exported-but-empty env (`Some("")`) is neither a dev build nor a valid identity and MUST fail hard at compile time, so the build can never silently hash the empty string into a fake registry slug. We assert the panic rather than letting a bogus empty primary registry ship. | capdag.test.js:2561 |
| test1880 | `test1880_aliasNameNormalizationRules` | TEST1880: alias name normalization lowercases and accepts the allowed character class; rejects colon, whitespace, and out-of-class chars with the right error. A broken validator would let a URN-shaped or whitespace name through, or mangle a valid name. | capdag.test.js:6341 |
| test1881 | `test1881_tokenUrnVsAliasDetection` | TEST1881: URN-vs-alias detection keys purely on the presence of ':'. The whole design rests on this discriminator being exact. | capdag.test.js:6353 |
| test1882 | `test1882_classifyAliasTargetByPrefix` | TEST1882: alias target classification distinguishes cap from media by prefix and rejects a non-URN target. The typed-boundary enforcement in the registry depends on this. | capdag.test.js:6362 |
| test1887 | `test1887_manifestSerdeRoundTripsAliases` | TEST1887: the Manifest type round-trips an `aliases` map. | capdag.test.js:6371 |
| test6201 | `test6201_emptyCapIsIllegal` | TEST6201: cap: (empty) is the illegal bare top form | capdag.test.js:3010 |
| test6204 | `test6204_Urn` | TEST6204: Urn | capdag.test.js:118 |
| test6206 | `test6206_CapFabAddCapPopulatesEdgesAndNodes` | Add a cap and check it becomes an edge with from/to nodes and carries the registry name we passed. This is exactly the shape the renderer depends on. | capdag.test.js:1370 |
| test6208 | `test6208_CapFabGetOutgoingConformsToMatching` | getOutgoing takes a concrete source URN and returns edges whose from_spec the source conforms to. It must NOT be a plain string lookup. | capdag.test.js:1388 |
| test6212 | `test6212_xv5InlineSpecRedefinitionDetected` | TEST6212: XV5 - Test inline media def redefinition of existing registry spec is detected and rejected | capdag.test.js:808 |
| test6216 | `test6216_xv5NewInlineSpecAllowed` | TEST6216: XV5 - Test new inline media def (not in registry) is allowed | capdag.test.js:825 |
| test6220 | `test6220_xv5EmptyMediaDefsAllowed` | TEST6220: XV5 - Test empty media_defs (no inline specs) passes XV5 validation | capdag.test.js:840 |
| test6224 | `test6224_CapFabDistinctRegistryNames` | Each edge must carry the registry name it was added with. This is how the renderer colours/groups edges by provenance in browse mode. | capdag.test.js:1409 |
| test6228 | `test6228_LlmGenerateTextUrnSpecs` | Mirror-specific coverage: llm_generate_text_urn input/output specs conform to MEDIA_STRING | capdag.test.js:1618 |
| test6232 | `test6232_JS_buildExtensionIndex` | These tests cover JS-specific functionality not in the Rust numbering scheme but are important for capdag-js correctness. | capdag.test.js:1649 |
| test6236 | `test6236_JS_mediaUrnsForExtension` | TEST6236: J s media urns for extension | capdag.test.js:1666 |
| test6240 | `test6240_JS_getExtensionMappings` | TEST0070: J s get extension mappings | capdag.test.js:1695 |
| test6242 | `test6242_JS_resolveMediaUrnFromSpecs` | TEST0073: J s resolve media urn from specs | capdag.test.js:1706 |
| test6246 | `test6246_JS_capJSONSerialization` | TEST6246: J s cap j s o n serialization | capdag.test.js:1719 |
| test6249 | `test6249_JS_capDocumentationRoundTrip` | JS round-trip for the documentation field on Cap. Mirrors TEST920 in capdag/src/cap/definition.rs — the body is non-trivial (newlines, backticks, embedded quotes, Unicode) so escaping mismatches between JSON.stringify on this side and the Rust serializer on the other side surface as failures here. | capdag.test.js:1742 |
| test6253 | `test6253_JS_capDocumentationOmittedWhenNull` | When documentation is null, toJSON must omit the field entirely. This matches the Rust serializer's skip-when-None semantics and the ObjC toDictionary behaviour. A regression where null is emitted as `documentation: null` would break the symmetric round-trip with Rust (which has no null sentinel) and pollute generated JSON. | capdag.test.js:1764 |
| test6257 | `test6257_JS_mediaDefDocumentationPropagatesThroughResolve` | Documentation propagates from a mediaDefs definition through resolveMediaUrn into the resolved MediaDef. Mirrors TEST924 on the Rust side. This is the path every UI consumer uses, so a break here makes the new field invisible everywhere downstream. | capdag.test.js:1787 |
| test6261 | `test6261_JS_stdinSourceKindConstants` | TEST6261: J s stdin source kind constants | capdag.test.js:1818 |
| test6265 | `test6265_JS_stdinSourceNullData` | TEST6265: J s stdin source null data | capdag.test.js:1825 |
| test6269 | `test6269_JS_mediaDefConstruction` | TEST6269: J s media def construction | capdag.test.js:1833 |
| test6272 | `test6272_isCollection` | Mirror-specific coverage: isCollection returns true when collection marker tag is present Mirror-specific coverage: N/A for JS (MEDIA_COLLECTION constants removed - no longer exists) | capdag.test.js:2784 |
| test6275 | `test6275_Machine_emptyInput` | --- Machine parser tests (mirrors parser.rs tests) --- | capdag.test.js:3206 |
| test6277 | `test6277_Machine_whitespaceOnly` | TEST0088: Machine whitespace only | capdag.test.js:3211 |
| test6279 | `test6279_Machine_headerOnlyNoWirings` | TEST0089: Machine header only no wirings | capdag.test.js:3216 |
| test6280 | `test6280_Machine_duplicateAlias` | TEST0090: Machine duplicate alias | capdag.test.js:3224 |
| test6282 | `test6282_resolveCustomMediaDef` | TEST6282: Test resolving a custom media URN from a registry-seeded media def | capdag.test.js:1027 |
| test6283 | `test6283_resolveCustomWithSchema` | TEST6283: Test resolving a custom record media def carrying a schema from a registry-seeded media def | capdag.test.js:1037 |
| test6286 | `test6286_Machine_simpleLinearChain` | TEST0094: Machine simple linear chain | capdag.test.js:3236 |
| test6288 | `test6288_Machine_twoStepChain` | TEST0095: Machine two step chain | capdag.test.js:3252 |
| test6290 | `test6290_Machine_fanOut` | TEST0096: Machine fan out | capdag.test.js:3267 |
| test6292 | `test6292_Machine_fanInSecondaryAssignedByPriorWiring` | TEST0097: Machine fan in secondary assigned by prior wiring | capdag.test.js:3285 |
| test6294 | `test6294_Machine_fanInSecondaryUnassignedGetsWildcard` | TEST0098: Machine fan in secondary unassigned gets wildcard | capdag.test.js:3299 |
| test6306 | `test6306_Machine_loopEdge` | TEST6306: Machine loop edge | capdag.test.js:3311 |
| test6308 | `test6308_Machine_undefinedAliasFails` | TEST6308: Machine undefined alias fails | capdag.test.js:3321 |
| test6310 | `test6310_Machine_nodeAliasCollision` | TEST6310: Machine node alias collision | capdag.test.js:3329 |
| test6312 | `test6312_Machine_conflictingMediaTypesFail` | TEST6312: Machine conflicting media types fail | capdag.test.js:3340 |
| test6315 | `test6315_Machine_multilineFormat` | TEST6315: Machine multiline format | capdag.test.js:3353 |
| test6318 | `test6318_Machine_differentAliasesSameGraph` | TEST6318: Machine different aliases same graph | capdag.test.js:3364 |
| test6321 | `test6321_Machine_malformedInputFails` | TEST6321: Machine malformed input fails | capdag.test.js:3377 |
| test6323 | `test6323_Machine_unterminatedBracketFails` | TEST6323: Machine unterminated bracket fails | capdag.test.js:3385 |
| test6327 | `test6327_Machine_lineBasedSimpleChain` | --- Machine parser line-based mode tests --- | capdag.test.js:3394 |
| test6331 | `test6331_Machine_lineBasedTwoStepChain` | TEST6331: Machine line based two step chain | capdag.test.js:3408 |
| test6334 | `test6334_Machine_lineBasedLoop` | TEST6334: Machine line based loop | capdag.test.js:3419 |
| test6337 | `test6337_Machine_lineBasedFanIn` | TEST6337: Machine line based fan in | capdag.test.js:3429 |
| test6341 | `test6341_Machine_mixedBracketedAndLineBased` | TEST6341: Machine mixed bracketed and line based | capdag.test.js:3443 |
| test6345 | `test6345_Machine_lineBasedEquivalentToBracketed` | TEST6345: Machine line based equivalent to bracketed | capdag.test.js:3452 |
| test6349 | `test6349_Machine_lineBasedFormatSerialization` | TEST6349: Machine line based format serialization | capdag.test.js:3465 |
| test6353 | `test6353_Machine_lineBasedAndBracketedParseSameGraph` | TEST6353: Machine line based and bracketed parse same graph | capdag.test.js:3487 |
| test6357 | `test6357_Machine_edgeEquivalenceSameUrns` | --- Machine graph tests (mirrors graph.rs tests) --- | capdag.test.js:3513 |
| test6361 | `test6361_Machine_edgeEquivalenceDifferentCapUrns` | TEST6361: Machine edge equivalence different cap urns | capdag.test.js:3530 |
| test6365 | `test6365_Machine_edgeEquivalenceDifferentTargets` | TEST6365: Machine edge equivalence different targets | capdag.test.js:3547 |
| test6369 | `test6369_Machine_edgeEquivalenceDifferentLoopFlag` | TEST6369: Machine edge equivalence different loop flag | capdag.test.js:3564 |
| test6372 | `test6372_Machine_edgeEquivalenceSourceOrderIndependent` | TEST6372: Machine edge equivalence source order independent | capdag.test.js:3581 |
| test6375 | `test6375_Machine_edgeEquivalenceDifferentSourceCount` | TEST6375: Machine edge equivalence different source count | capdag.test.js:3598 |
| test6377 | `test6377_Machine_graphEquivalenceSameEdges` | TEST6377: Machine graph equivalence same edges | capdag.test.js:3615 |
| test6380 | `test6380_Machine_graphEquivalenceReorderedEdges` | TEST6380: Machine graph equivalence reordered edges | capdag.test.js:3631 |
| test6383 | `test6383_Machine_graphNotEquivalentDifferentEdgeCount` | TEST6383: Machine graph not equivalent different edge count | capdag.test.js:3647 |
| test6386 | `test6386_Machine_graphNotEquivalentDifferentCap` | TEST6386: Machine graph not equivalent different cap | capdag.test.js:3662 |
| test6389 | `test6389_Machine_graphEmpty` | TEST6389: Machine graph empty | capdag.test.js:3676 |
| test6392 | `test6392_Machine_graphEmptyEquivalence` | TEST6392: Machine graph empty equivalence | capdag.test.js:3683 |
| test6395 | `test6395_Machine_rootSourcesLinearChain` | TEST6395: Machine root sources linear chain | capdag.test.js:3690 |
| test6397 | `test6397_Machine_leafTargetsLinearChain` | TEST6397: Machine leaf targets linear chain | capdag.test.js:3705 |
| test6398 | `test6398_Machine_rootSourcesFanIn` | TEST6398: Machine root sources fan in | capdag.test.js:3720 |
| test6400 | `test6400_Machine_displayEdge` | TEST6400: Machine display edge | capdag.test.js:3733 |
| test6402 | `test6402_Machine_displayGraph` | TEST6402: Machine display graph | capdag.test.js:3745 |
| test6404 | `test6404_Machine_serializeSingleEdge` | --- Machine serializer tests (mirrors serializer.rs tests) --- | capdag.test.js:3758 |
| test6406 | `test6406_Machine_serializeTwoEdgeChain` | TEST6406: Machine serialize two edge chain | capdag.test.js:3774 |
| test6408 | `test6408_Machine_serializeEmptyGraph` | TEST6408: Machine serialize empty graph | capdag.test.js:3788 |
| test6410 | `test6410_Machine_roundtripSingleEdge` | TEST6410: Machine roundtrip single edge | capdag.test.js:3793 |
| test6413 | `test6413_Machine_roundtripTwoEdgeChain` | TEST6413: Machine roundtrip two edge chain | capdag.test.js:3807 |
| test6415 | `test6415_Machine_roundtripFanOut` | TEST6415: Machine roundtrip fan out | capdag.test.js:3822 |
| test6417 | `test6417_Machine_roundtripLoopEdge` | TEST6417: Machine roundtrip loop edge | capdag.test.js:3838 |
| test6419 | `test6419_Machine_serializationIsDeterministic` | TEST6419: Machine serialization is deterministic | capdag.test.js:3852 |
| test6421 | `test6421_Machine_reorderedEdgesProduceSameNotation` | TEST6421: Machine reordered edges produce same notation | capdag.test.js:3866 |
| test6429 | `test6429_Machine_multilineSerializeFormat` | TEST6429: Machine multiline serialize format | capdag.test.js:3883 |
| test6432 | `test6432_Machine_aliasFromOpTag` | Aliases are pure-index `edge_<N>` regardless of the cap's tags; there is no privileged `op` tag to derive a friendlier name from. | capdag.test.js:3899 |
| test6434 | `test6434_Machine_aliasFallbackWithoutOpTag` | TEST6434: Machine alias fallback without op tag | capdag.test.js:3911 |
| test6436 | `test6436_Machine_duplicateOpTagsDisambiguated` | Pure-index aliases inherently disambiguate edges that share a marker tag. | capdag.test.js:3923 |
| test6437 | `test6437_Machine_builderSingleEdge` | --- Machine builder tests --- | capdag.test.js:3945 |
| test6438 | `test6438_Machine_builderWithLoop` | TEST6438: Machine builder with loop | capdag.test.js:3958 |
| test6439 | `test6439_Machine_builderChaining` | TEST6439: Machine builder chaining | capdag.test.js:3971 |
| test6440 | `test6440_Machine_builderEquivalentToParsed` | TEST6440: Machine builder equivalent to parsed | capdag.test.js:3980 |
| test6442 | `test6442_Machine_builderRoundTrip` | TEST6442: Machine builder round trip | capdag.test.js:3993 |
| test6444 | `test6444_Machine_capUrnIsEquivalent` | --- CapUrn.isEquivalent/isComparable tests --- | capdag.test.js:4005 |
| test6446 | `test6446_Machine_capUrnIsComparable` | TEST6446: Machine cap urn is comparable | capdag.test.js:4014 |
| test6448 | `test6448_Machine_capUrnInMediaUrn` | TEST6448: Machine cap urn in media urn | capdag.test.js:4022 |
| test6449 | `test6449_Machine_capUrnOutMediaUrn` | TEST6449: Machine cap urn out media urn | capdag.test.js:4030 |
| test6450 | `test6450_Machine_mediaUrnIsEquivalent` | --- MediaUrn.isEquivalent/isComparable tests --- | capdag.test.js:4039 |
| test6451 | `test6451_Machine_mediaUrnIsComparable` | TEST6451: Machine media urn is comparable | capdag.test.js:4048 |
| test6452 | `test6452_Machine_parseMachineWithAST_headerLocation` | Phase 0A: Position tracking tests | capdag.test.js:4061 |
| test6453 | `test6453_Machine_parseMachineWithAST_wiringLocation` | TEST6453: Machine parse machine with a s t wiring location | capdag.test.js:4078 |
| test6454 | `test6454_Machine_parseMachineWithAST_multilinePositions` | TEST6454: Machine parse machine with a s t multiline positions | capdag.test.js:4093 |
| test6455 | `test6455_Machine_parseMachineWithAST_fanInSourceLocations` | TEST6455: Machine parse machine with a s t fan in source locations | capdag.test.js:4103 |
| test6456 | `test6456_Machine_parseMachineWithAST_aliasMap` | TEST6456: Machine parse machine with a s t alias map | capdag.test.js:4115 |
| test6457 | `test6457_Machine_parseMachineWithAST_nodeMedia` | TEST6457: Machine parse machine with a s t node media | capdag.test.js:4134 |
| test6458 | `test6458_Machine_errorLocation_parseError` | TEST6458: Machine error location parse error | capdag.test.js:4147 |
| test6459 | `test6459_Machine_errorLocation_duplicateAlias` | TEST6459: Machine error location duplicate alias | capdag.test.js:4158 |
| test6460 | `test6460_Machine_errorLocation_undefinedAlias` | TEST6460: Machine error location undefined alias | capdag.test.js:4173 |
| test6462 | `test6462_Machine_toMermaid_linearChain` | Phase 0C: Machine.toMermaid() tests | capdag.test.js:4187 |
| test6463 | `test6463_Machine_toMermaid_loopEdge` | TEST6463: Machine to mermaid loop edge | capdag.test.js:4206 |
| test6464 | `test6464_Machine_toMermaid_emptyGraph` | TEST6464: Machine to mermaid empty graph | capdag.test.js:4218 |
| test6465 | `test6465_Machine_toMermaid_fanIn` | TEST6465: Machine to mermaid fan in | capdag.test.js:4225 |
| test6466 | `test6466_Machine_toMermaid_fanOut` | TEST6466: Machine to mermaid fan out | capdag.test.js:4237 |
| test6467 | `test6467_Machine_capRegistryEntry_construction` | Phase 0B: FabricRegistryClient tests | capdag.test.js:4257 |
| test6468 | `test6468_Machine_mediaRegistryEntry_construction` | TEST6468: Machine media registry entry construction | capdag.test.js:4281 |
| test6469 | `test6469_Machine_capRegistryClient_construction` | TEST6469: Machine cap registry client construction | capdag.test.js:4295 |
| test6470 | `test6470_Machine_capRegistryEntry_defaults` | TEST6470: Machine cap registry entry defaults | capdag.test.js:4303 |
| test6471 | `test6471_Renderer_cardinalityLabel_allFourCases` | TEST6471: Renderer cardinality label all four cases | capdag.test.js:4369 |
| test6472 | `test6472_Renderer_cardinalityLabel_usesUnicodeArrow` | TEST6472: Renderer cardinality label uses unicode arrow | capdag.test.js:4377 |
| test6473 | `test6473_Renderer_cardinalityFromCap_findsStdinArgNotFirstArg` | TEST6473: Renderer cardinality from cap finds stdin arg not first arg | capdag.test.js:4386 |
| test6474 | `test6474_Renderer_cardinalityFromCap_scalarDefaultsWhenFieldsMissing` | TEST6474: Renderer cardinality from cap scalar defaults when fields missing | capdag.test.js:4411 |
| test6475 | `test6475_Renderer_cardinalityFromCap_outputOnlySequence` | TEST6475: Renderer cardinality from cap output only sequence | capdag.test.js:4420 |
| test6476 | `test6476_Renderer_cardinalityFromCap_rejectsStringIsSequence` | TEST6476: Renderer cardinality from cap rejects string is sequence | capdag.test.js:4432 |
| test6478 | `test6478_Renderer_cardinalityFromCap_throwsOnNonObject` | TEST6478: Renderer cardinality from cap throws on non object | capdag.test.js:4446 |
| test6479 | `test6479_Renderer_canonicalMediaUrn_normalizesTagOrder` | TEST6479: Renderer canonical media urn normalizes tag order | capdag.test.js:4466 |
| test6480 | `test6480_Renderer_canonicalMediaUrn_preservesValueTags` | TEST6480: Renderer canonical media urn preserves value tags | capdag.test.js:4476 |
| test6481 | `test6481_Renderer_canonicalMediaUrn_rejectsCapUrn` | TEST6481: Renderer canonical media urn rejects cap urn | capdag.test.js:4482 |
| test6482 | `test6482_Renderer_mediaNodeLabel_rejectsUrnDerivedLabels` | TEST6482: Renderer media node label rejects urn derived labels | capdag.test.js:4495 |
| test6483 | `test6483_Renderer_buildBrowseGraphData_rejectsMissingMediaTitles` | TEST6483: Renderer build browse graph data rejects missing media titles | capdag.test.js:4510 |
| test6484 | `test6484_Renderer_validateStrandStep_rejectsUnknownVariant` | TEST6484: Renderer validate strand step rejects unknown variant | capdag.test.js:4568 |
| test6486 | `test6486_Renderer_validateStrandStep_requiresBooleanIsSequence` | TEST6486: Renderer validate strand step requires boolean is sequence | capdag.test.js:4586 |
| test6487 | `test6487_Renderer_classifyStrandCapSteps_capFlags` | TEST6487: Renderer classify strand cap steps cap flags | capdag.test.js:4609 |
| test6488 | `test6488_Renderer_classifyStrandCapSteps_nestedForks` | TEST6488: Renderer classify strand cap steps nested forks | capdag.test.js:4631 |
| test6489 | `test6489_Renderer_buildStrandGraphData_singleCapPlain` | TEST6489: Renderer build strand graph data single cap plain | capdag.test.js:4662 |
| test6491 | `test6491_Renderer_buildStrandGraphData_sequenceShowsCardinality` | TEST6491: Renderer build strand graph data sequence shows cardinality | capdag.test.js:4690 |
| test6492 | `test6492_Renderer_buildStrandGraphData_foreachCollectSpan` | TEST6492: Renderer build strand graph data foreach collect span | capdag.test.js:4711 |
| test6493 | `test6493_Renderer_buildStrandGraphData_standaloneCollect` | TEST6493: Renderer build strand graph data standalone collect | capdag.test.js:4763 |
| test6494 | `test6494_Renderer_buildStrandGraphData_unclosedForEachBody` | TEST6494: Renderer build strand graph data unclosed for each body | capdag.test.js:4791 |
| test6495 | `test6495_Renderer_buildStrandGraphData_nestedForEachThrows` | TEST6495: Renderer build strand graph data nested for each throws | capdag.test.js:4829 |
| test6496 | `test6496_Renderer_collapseStrand_singleCapBodyKeepsCapOwnLabel` | TEST6496: Renderer collapse strand single cap body keeps cap own label | capdag.test.js:4858 |
| test6497 | `test6497_Renderer_collapseStrand_unclosedForEachBodyCollapses` | TEST6497: Renderer collapse strand unclosed for each body collapses | capdag.test.js:4911 |
| test6498 | `test6498_Renderer_collapseStrand_standaloneCollectCollapses` | TEST6498: Renderer collapse strand standalone collect collapses | capdag.test.js:4968 |
| test6499 | `test6499_Renderer_collapseStrand_sequenceProducingCapBeforeForeach` | TEST6499: Renderer collapse strand sequence producing cap before foreach | capdag.test.js:5012 |
| test6500 | `test6500_Renderer_collapseStrand_plainCapMergesTrailingOutput` | TEST6500: Renderer collapse strand plain cap merges trailing output | capdag.test.js:5077 |
| test6501 | `test6501_Renderer_collapseStrand_plainCapDistinctTargetNoMerge` | TEST6501: Renderer collapse strand plain cap distinct target no merge | capdag.test.js:5114 |
| test6502 | `test6502_Renderer_validateStrandPayload_missingSourceMediaUrn` | TEST6502: Renderer validate strand payload missing source media urn | capdag.test.js:5141 |
| test6503 | `test6503_Renderer_validateBodyOutcome_rejectsNegativeIndex` | ---------------- run builder ---------------- | capdag.test.js:5154 |
| test6504 | `test6504_Renderer_buildRunGraphData_pagesSuccessesAndFailures` | TEST6504: Renderer build run graph data pages successes and failures | capdag.test.js:5165 |
| test6505 | `test6505_Renderer_buildRunGraphData_failureWithoutFailedCapRendersFullTrace` | TEST6505: Renderer build run graph data failure without failed cap renders full trace | capdag.test.js:5236 |
| test6506 | `test6506_Renderer_buildRunGraphData_usesCapUrnIsEquivalentForFailedCap` | TEST6506: Renderer build run graph data uses cap urn is equivalent for failed cap | capdag.test.js:5275 |
| test6507 | `test6507_Renderer_buildRunGraphData_backboneHasNoForeachNode` | TEST6507: Renderer build run graph data backbone has no foreach node | capdag.test.js:5335 |
| test6508 | `test6508_Renderer_buildRunGraphData_allFailedDropsTargetPlaceholder` | TEST6508: Renderer build run graph data all failed drops target placeholder | capdag.test.js:5390 |
| test6509 | `test6509_Renderer_buildRunGraphData_unclosedForeachSuccessNoMerge` | TEST6509: Renderer build run graph data unclosed foreach success no merge | capdag.test.js:5456 |
| test6510 | `test6510_Renderer_buildRunGraphData_closedForeachSuccessMergesAtCollectTarget` | TEST6510: Renderer build run graph data closed foreach success merges at collect target | capdag.test.js:5518 |
| test6511 | `test6511_Renderer_validateEditorGraphPayload_rejectsUnknownKind` | ---------------- editor-graph builder ---------------- | capdag.test.js:5573 |
| test6512 | `test6512_Renderer_buildEditorGraphData_collapsesCapsIntoLabeledEdges` | TEST6512: Renderer build editor graph data collapses caps into labeled edges | capdag.test.js:5588 |
| test6513 | `test6513_Renderer_buildEditorGraphData_loopMarkedEdgeGetsLoopClass` | TEST6513: Renderer build editor graph data loop marked edge gets loop class | capdag.test.js:5627 |
| test6514 | `test6514_Renderer_buildEditorGraphData_cardinalityFromDataSlotSequenceFlags` | TEST6514: Renderer build editor graph data cardinality from data slot sequence flags | capdag.test.js:5646 |
| test6515 | `test6515_Renderer_buildEditorGraphData_capWithoutCompleteArgsIsDropped` | TEST6515: Renderer build editor graph data cap without complete args is dropped | capdag.test.js:5666 |
| test6516 | `test6516_Renderer_buildEditorGraphData_rejectsEdgeWithMissingSource` | TEST6516: Renderer build editor graph data rejects edge with missing source | capdag.test.js:5684 |
| test6517 | `test6517_Renderer_buildResolvedMachineGraphData_singleStrandLinearChain` | ---------------- resolved-machine builder ---------------- | capdag.test.js:5700 |
| test6518 | `test6518_Renderer_buildResolvedMachineGraphData_loopEdgeGetsLoopClass` | TEST6518: Renderer build resolved machine graph data loop edge gets loop class | capdag.test.js:5759 |
| test6519 | `test6519_Renderer_buildResolvedMachineGraphData_fanInProducesEdgePerAssignment` | TEST6519: Renderer build resolved machine graph data fan in produces edge per assignment | capdag.test.js:5794 |
| test6520 | `test6520_Renderer_buildResolvedMachineGraphData_multiStrandKeepsStrandsDisjoint` | TEST6520: Renderer build resolved machine graph data multi strand keeps strands disjoint | capdag.test.js:5835 |
| test6521 | `test6521_Renderer_buildResolvedMachineGraphData_duplicateNodeIdAcrossStrandsFailsHard` | TEST6521: Renderer build resolved machine graph data duplicate node id across strands fails hard | capdag.test.js:5898 |
| test6522 | `test6522_Renderer_validateResolvedMachinePayload_rejectsMissingFields` | TEST6522: Renderer validate resolved machine payload rejects missing fields | capdag.test.js:5934 |
| test6544 | `test6544_builderRejectsStructuralKeys` | TEST6544: builder rejects structural keys on tag/marker | capdag.test.js:2935 |
| test6620 | `test6620_wildcardGenericFormsRejected` | TEST6620: Generic top-to-top spellings are all rejected. | capdag.test.js:3116 |
| test6621 | `test6621_capIdentityConstantWorks` | TEST6621: CAP_IDENTITY constant names the true identity cap, not bare cap: | capdag.test.js:3137 |
| test6734 | `test6734_rejectInvalidCombinations` | TEST6734: Invalid qualifier combinations must be rejected. | capdag.test.js:6260 |
| test6735 | `test6735_axisWeightingOutDominates` | TEST6735: out-axis difference dominates combined in+y differences. | capdag.test.js:6275 |
| test6736 | `test6736_axisWeightingDecodedLayout` | TEST6736: Decoded layout — 10000*out + 100*in + y. | capdag.test.js:6295 |
| test6737 | `test6737_capVersionZeroOmittedOnWire` | TEST6737: Cap with version=0 round-trips with no `version` key on wire | capdag.test.js:6307 |
---

## Numbering Mismatches

These tests have a numbering disagreement between the function name and the authoritative immediate TEST comment/docstring above the test. This is reported explicitly so comment sync does not silently overwrite a misnumbered test.

- `test001` / `test1` / `test001_capUrnCreation` — capdag.test.js:143
- `test002` / `test2` / `test002_directionSpecsRequired` — capdag.test.js:153
- `test003` / `test3` / `test003_directionMatching` — capdag.test.js:164
- `test004` / `test4` / `test004_unquotedValuesLowercased` — capdag.test.js:179
- `test005` / `test5` / `test005_quotedValuesPreserveCase` — capdag.test.js:187
- `test006` / `test6` / `test006_quotedValueSpecialChars` — capdag.test.js:193
- `test007` / `test7` / `test007_quotedValueEscapeSequences` — capdag.test.js:199
- `test008` / `test8` / `test008_mixedQuotedUnquoted` — capdag.test.js:206
- `test009` / `test9` / `test009_unterminatedQuoteError` — capdag.test.js:213
- `test010` / `test10` / `test010_invalidEscapeSequenceError` — capdag.test.js:226
- `test011` / `test11` / `test011_serializationSmartQuoting` — capdag.test.js:240
- `test012` / `test12` / `test012_roundTripSimple` — capdag.test.js:249
- `test013` / `test13` / `test013_roundTripQuoted` — capdag.test.js:257
- `test014` / `test14` / `test014_roundTripEscapes` — capdag.test.js:266
- `test015` / `test15` / `test015_capPrefixRequired` — capdag.test.js:276
- `test016` / `test16` / `test016_trailingSemicolonEquivalence` — capdag.test.js:288
- `test017` / `test17` / `test017_tagMatching` — capdag.test.js:324
- `test018` / `test18` / `test018_matchingCaseSensitiveValues` — capdag.test.js:348
- `test019` / `test19` / `test019_missingTagHandling` — capdag.test.js:355
- `test021` / `test21` / `test021_builder` — capdag.test.js:405
- `test022` / `test22` / `test022_builderRequiresDirection` — capdag.test.js:419
- `test023` / `test23` / `test023_builderPreservesCase` — capdag.test.js:433
- `test024` / `test24` / `test024_compatibility` — capdag.test.js:444
- `test025` / `test25` / `test025_bestMatch` — capdag.test.js:464
- `test026` / `test26` / `test026_mergeAndSubset` — capdag.test.js:477
- `test027` / `test27` / `test027_wildcardTag` — capdag.test.js:496
- `test028` / `test28` / `test028_emptyCapUrnNotAllowed` — capdag.test.js:509
- `test029` / `test29` / `test029_minimalCapUrn` — capdag.test.js:518
- `test030` / `test30` / `test030_extendedCharacterSupport` — capdag.test.js:526
- `test031` / `test31` / `test031_wildcardRestrictions` — capdag.test.js:533
- `test032` / `test32` / `test032_duplicateKeyRejection` — capdag.test.js:551
- `test033` / `test33` / `test033_numericKeyRestriction` — capdag.test.js:560
- `test034` / `test34` / `test034_emptyValueError` — capdag.test.js:574
- `test035` / `test35` / `test035_hasTagCaseSensitive` — capdag.test.js:587
- `test036` / `test36` / `test036_withTagPreservesValue` — capdag.test.js:599
- `test037` / `test37` / `test037_withTagRejectsEmptyValue` — capdag.test.js:606
- `test038` / `test38` / `test038_semanticEquivalence` — capdag.test.js:616
- `test039` / `test39` / `test039_getTagReturnsDirectionSpecs` — capdag.test.js:624
- `test040` / `test40` / `test040_matchingSemanticsExactMatch` — capdag.test.js:633
- `test041` / `test41` / `test041_matchingSemanticsCapMissingTag` — capdag.test.js:640
- `test042` / `test42` / `test042_matchingSemanticsCapHasExtraTag` — capdag.test.js:648
- `test043` / `test43` / `test043_matchingSemanticsRequestHasWildcard` — capdag.test.js:656
- `test044` / `test44` / `test044_matchingSemanticsCapHasWildcard` — capdag.test.js:663
- `test045` / `test45` / `test045_matchingSemanticsValueMismatch` — capdag.test.js:670
- `test046` / `test46` / `test046_matchingSemanticsFallbackPattern` — capdag.test.js:677
- `test047` / `test47` / `test047_matchingSemanticsThumbnailVoidInput` — capdag.test.js:685
- `test048` / `test48` / `test048_matchingSemanticsWildcardDirection` — capdag.test.js:692
- `test049` / `test49` / `test049_matchingSemanticsCrossDimension` — capdag.test.js:699
- `test050` / `test50` / `test050_matchingSemanticsDirectionMismatch` — capdag.test.js:707
- `test060` / `test60` / `test060_wrongPrefixFails` — capdag.test.js:852
- `test062` / `test62` / `test062_isRecord` — capdag.test.js:865
- `test063` / `test63` / `test063_isScalar` — capdag.test.js:876
- `test064` / `test64` / `test064_isList` — capdag.test.js:889
- `test065` / `test65` / `test065_isOpaque` — capdag.test.js:898
- `test066` / `test66` / `test066_isJson` — capdag.test.js:909
- `test067` / `test67` / `test067_isText` — capdag.test.js:918
- `test068` / `test68` / `test068_isVoid` — capdag.test.js:931
- `test071` / `test71` / `test071_toStringRoundtrip` — capdag.test.js:939
- `test072` / `test72` / `test072_constantsParse` — capdag.test.js:949
- `test074` / `test74` / `test074_mediaUrnMatching` — capdag.test.js:969
- `test075` / `test75` / `test075_accepts` — capdag.test.js:983
- `test076` / `test76` / `test076_specificity` — capdag.test.js:994
- `test077` / `test77` / `test077_serdeRoundtrip` — capdag.test.js:1003
- `test078` / `test78` / `test078_debugMatchingBehavior` — capdag.test.js:1012
- `test6240` / `test0070` / `test6240_JS_getExtensionMappings` — capdag.test.js:1695
- `test6242` / `test0073` / `test6242_JS_resolveMediaUrnFromSpecs` — capdag.test.js:1706
- `test6277` / `test0088` / `test6277_Machine_whitespaceOnly` — capdag.test.js:3211
- `test6279` / `test0089` / `test6279_Machine_headerOnlyNoWirings` — capdag.test.js:3216
- `test6280` / `test0090` / `test6280_Machine_duplicateAlias` — capdag.test.js:3224
- `test6286` / `test0094` / `test6286_Machine_simpleLinearChain` — capdag.test.js:3236
- `test6288` / `test0095` / `test6288_Machine_twoStepChain` — capdag.test.js:3252
- `test6290` / `test0096` / `test6290_Machine_fanOut` — capdag.test.js:3267
- `test6292` / `test0097` / `test6292_Machine_fanInSecondaryAssignedByPriorWiring` — capdag.test.js:3285
- `test6294` / `test0098` / `test6294_Machine_fanInSecondaryUnassignedGetsWildcard` — capdag.test.js:3299

---

*Generated from CapDag-JS source tree*
*Total tests: 348*
*Total numbered tests: 348*
*Total unnumbered tests: 0*
*Total numbered tests missing descriptions: 0*
*Total numbering mismatches: 74*

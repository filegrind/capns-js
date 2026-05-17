# JS Test Catalog

**Total Tests:** 335

**Numbered Tests:** 185

**Unnumbered Tests:** 150

**Numbered Tests Missing Descriptions:** 0

**Numbering Mismatches:** 0

All numbered test numbers are unique.

This catalog lists all tests in the JS codebase.

| Test # | Function Name | Description | File |
|--------|---------------|-------------|------|
| test001 | `test001_capUrnCreation` | TEST001: Test that cap URN is created with tags parsed correctly and direction specs accessible | capdag.test.js:133 |
| test002 | `test002_directionSpecsRequired` | TEST002: Test that missing 'in' or 'out' defaults to media: wildcard | capdag.test.js:143 |
| test003 | `test003_directionMatching` | TEST003: Test that direction specs must match exactly, different in/out types don't match, wildcard matches any | capdag.test.js:154 |
| test004 | `test004_unquotedValuesLowercased` | TEST004: Test that unquoted keys and values are normalized to lowercase. Key lookup is case-insensitive: uppercase variants of `ext` resolve to the same keyed tag. | capdag.test.js:171 |
| test005 | `test005_quotedValuesPreserveCase` | TEST005: Test that quoted values preserve case while unquoted are lowercased | capdag.test.js:179 |
| test006 | `test006_quotedValueSpecialChars` | TEST006: Test that quoted values can contain special characters (semicolons, equals, spaces) | capdag.test.js:185 |
| test007 | `test007_quotedValueEscapeSequences` | TEST007: Test that escape sequences in quoted values (\" and \\) are parsed correctly | capdag.test.js:191 |
| test008 | `test008_mixedQuotedUnquoted` | TEST008: Test that mixed quoted and unquoted values in same URN parse correctly | capdag.test.js:198 |
| test009 | `test009_unterminatedQuoteError` | TEST009: Test that unterminated quote produces UnterminatedQuote error | capdag.test.js:205 |
| test010 | `test010_invalidEscapeSequenceError` | TEST010: Test that invalid escape sequences (like \n, \x) produce InvalidEscapeSequence error | capdag.test.js:218 |
| test011 | `test011_serializationSmartQuoting` | TEST011: Test that serialization uses smart quoting (no quotes for simple lowercase, quotes for special chars/uppercase) | capdag.test.js:232 |
| test012 | `test012_roundTripSimple` | TEST012: Test that simple cap URN round-trips (parse -> serialize -> parse equals original) | capdag.test.js:241 |
| test013 | `test013_roundTripQuoted` | TEST013: Test that quoted values round-trip preserving case and spaces | capdag.test.js:249 |
| test014 | `test014_roundTripEscapes` | TEST014: Test that escape sequences round-trip correctly | capdag.test.js:258 |
| test015 | `test015_capPrefixRequired` | TEST015: Test that cap: prefix is required and case-insensitive | capdag.test.js:268 |
| test016 | `test016_trailingSemicolonEquivalence` | TEST016: Test that trailing semicolon is equivalent (same hash, same string, matches) | capdag.test.js:280 |
| test017 | `test017_tagMatching` | TEST017: Test tag matching: exact match, subset match, wildcard match, value mismatch | capdag.test.js:325 |
| test018 | `test018_matchingCaseSensitiveValues` | TEST018: Test that quoted values with different case do NOT match (case-sensitive) | capdag.test.js:349 |
| test019 | `test019_missingTagHandling` | TEST019: Missing tag in instance causes rejection — pattern's tags are constraints | capdag.test.js:356 |
| test020 | `test020_specificity` | TEST020: Specificity is the sum of per-tag truth-table scores across in/out/y. Marker tags (bare segments and `key=*`) score 2 (must-have-any), exact `key=value` tags score 3, missing/`?` score 0, `!` scores 1. testUrn() builds "cap:in=media:void;out=media:record;<tags>" so the directional baseline is: in:  media:void   -> {void=*}    -> 2 out: media:record -> {record=*}  -> 2 Total directional baseline: 4. | capdag.test.js:378 |
| test021 | `test021_builder` | TEST021: Test builder creates cap URN with marker + keyed tags and direction specs. `op` is no longer a special key — operation names are markers (value-less tags). | capdag.test.js:407 |
| test022 | `test022_builderRequiresDirection` | TEST022: Test builder requires both in_spec and out_spec | capdag.test.js:421 |
| test023 | `test023_builderPreservesCase` | TEST023: Test builder lowercases keys but preserves value case | capdag.test.js:435 |
| test024 | `test024_compatibility` | TEST024: Directional accepts — pattern's tags are constraints, instance must satisfy | capdag.test.js:446 |
| test025 | `test025_bestMatch` | TEST025: Test find_best_match returns most specific matching cap | capdag.test.js:466 |
| test026 | `test026_mergeAndSubset` | TEST026: Test merge combines tags from both caps, subset keeps only specified tags | capdag.test.js:479 |
| test027 | `test027_wildcardTag` | TEST027: Test with_wildcard_tag sets tag to wildcard, including in/out | capdag.test.js:498 |
| test028 | `test028_emptyCapUrnNotAllowed` | TEST028: Test empty cap URN is illegal | capdag.test.js:511 |
| test029 | `test029_minimalCapUrn` | TEST029: Test minimal valid cap URN has just in and out, empty tags | capdag.test.js:520 |
| test030 | `test030_extendedCharacterSupport` | TEST030: Test extended characters (forward slashes, colons) in tag values | capdag.test.js:528 |
| test031 | `test031_wildcardRestrictions` | TEST031: Test wildcard rejected in keys but accepted in values | capdag.test.js:535 |
| test032 | `test032_duplicateKeyRejection` | TEST032: Test duplicate keys are rejected with DuplicateKey error | capdag.test.js:553 |
| test033 | `test033_numericKeyRestriction` | TEST033: Test pure numeric keys rejected, mixed alphanumeric allowed, numeric values allowed | capdag.test.js:562 |
| test034 | `test034_emptyValueError` | TEST034: Test empty values are rejected | capdag.test.js:576 |
| test035 | `test035_hasTagCaseSensitive` | TEST035: Test has_tag is case-sensitive for values, case-insensitive for keys, works for in/out | capdag.test.js:589 |
| test036 | `test036_withTagPreservesValue` | TEST036: Test with_tag preserves value case | capdag.test.js:601 |
| test037 | `test037_withTagRejectsEmptyValue` | TEST037: Test with_tag rejects empty value | capdag.test.js:608 |
| test038 | `test038_semanticEquivalence` | TEST038: Test semantic equivalence of unquoted and quoted simple lowercase values | capdag.test.js:618 |
| test039 | `test039_getTagReturnsDirectionSpecs` | TEST039: Test get_tag returns direction specs (in/out) with case-insensitive lookup | capdag.test.js:626 |
| test040 | `test040_matchingSemanticsExactMatch` | TEST040: Matching semantics - exact match succeeds | capdag.test.js:635 |
| test041 | `test041_matchingSemanticsCapMissingTag` | TEST041: Matching semantics - cap missing tag matches (implicit wildcard) | capdag.test.js:642 |
| test042 | `test042_matchingSemanticsCapHasExtraTag` | TEST042: Pattern rejects instance missing required tags | capdag.test.js:650 |
| test043 | `test043_matchingSemanticsRequestHasWildcard` | TEST043: Matching semantics - request wildcard matches specific cap value | capdag.test.js:658 |
| test044 | `test044_matchingSemanticsCapHasWildcard` | TEST044: Matching semantics - cap wildcard matches specific request value | capdag.test.js:665 |
| test045 | `test045_matchingSemanticsValueMismatch` | TEST045: Matching semantics - value mismatch does not match | capdag.test.js:672 |
| test046 | `test046_matchingSemanticsFallbackPattern` | TEST046: Matching semantics - fallback pattern (cap missing tag = implicit wildcard) | capdag.test.js:679 |
| test047 | `test047_matchingSemanticsThumbnailVoidInput` | TEST047: Matching semantics - thumbnail fallback with void input | capdag.test.js:687 |
| test048 | `test048_matchingSemanticsWildcardDirection` | TEST048: Matching semantics - wildcard direction matches anything | capdag.test.js:694 |
| test049 | `test049_matchingSemanticsCrossDimension` | TEST049: Non-overlapping tags — neither direction accepts | capdag.test.js:701 |
| test050 | `test050_matchingSemanticsDirectionMismatch` | TEST050: Matching semantics - direction mismatch prevents matching | capdag.test.js:709 |
| test054 | `test054_xv5InlineSpecRedefinitionDetected` | TEST054: XV5 - Test inline media spec redefinition of existing registry spec is detected and rejected | capdag.test.js:813 |
| test055 | `test055_xv5NewInlineSpecAllowed` | TEST055: XV5 - Test new inline media spec (not in registry) is allowed | capdag.test.js:830 |
| test056 | `test056_xv5EmptyMediaSpecsAllowed` | TEST056: XV5 - Test empty media_specs (no inline specs) passes XV5 validation | capdag.test.js:845 |
| test060 | `test060_wrongPrefixFails` | TEST060: Test wrong prefix fails with InvalidPrefix error showing expected and actual prefix | capdag.test.js:857 |
| test061 | `test061_isBinary` | TEST061: Test is_binary returns true when textable tag is absent (binary = not textable) | capdag.test.js:866 |
| test062 | `test062_isRecord` | TEST062: Test is_record returns true when record marker tag is present indicating key-value structure | capdag.test.js:882 |
| test063 | `test063_isScalar` | TEST063: Test is_scalar returns true when list marker tag is absent (scalar is default) | capdag.test.js:893 |
| test064 | `test064_isList` | TEST064: Test is_list returns true when list marker tag is present indicating ordered collection | capdag.test.js:906 |
| test065 | `test065_isOpaque` | TEST065: Test is_opaque returns true when record marker is absent (opaque is default) | capdag.test.js:915 |
| test066 | `test066_isJson` | TEST066: Test is_json returns true only when json marker tag is present for JSON representation | capdag.test.js:926 |
| test067 | `test067_isText` | TEST067: Test is_text returns true only when textable marker tag is present | capdag.test.js:932 |
| test068 | `test068_isVoid` | TEST068: Test is_void returns true when void flag or type=void tag is present | capdag.test.js:943 |
| test071 | `test071_toStringRoundtrip` | TEST071: Test to_string roundtrip ensures serialization and deserialization preserve URN structure | capdag.test.js:951 |
| test072 | `test072_constantsParse` | TEST072: Test all media URN constants parse successfully as valid media URNs | capdag.test.js:961 |
| test074 | `test074_mediaUrnMatching` | TEST074: Test media URN conforms_to using tagged URN semantics with specific and generic requirements | capdag.test.js:981 |
| test075 | `test075_accepts` | TEST075: Test accepts with implicit wildcards where handlers with fewer tags can handle more requests | capdag.test.js:995 |
| test076 | `test076_specificity` | TEST076: Test specificity increases with more tags for ranking conformance | capdag.test.js:1006 |
| test077 | `test077_serdeRoundtrip` | TEST077: Test serde roundtrip serializes to JSON string and deserializes back correctly | capdag.test.js:1015 |
| test078 | `test078_debugMatchingBehavior` | TEST078: conforms_to behavior between MEDIA_OBJECT and MEDIA_STRING | capdag.test.js:1024 |
| test091 | `test091_resolveCustomMediaSpec` | TEST091: Test resolving custom media URN from local media_specs takes precedence over registry | capdag.test.js:1039 |
| test092 | `test092_resolveCustomWithSchema` | TEST092: Test resolving custom record media spec with schema from local media_specs | capdag.test.js:1049 |
| test093 | `test093_resolveUnresolvableFailsHard` | TEST093: Test resolving unknown media URN fails with UnresolvableMediaUrn error | capdag.test.js:1066 |
| test099 | `test099_resolvedIsBinary` | TEST099: Test ResolvedMediaSpec is_binary returns true when textable tag is absent | capdag.test.js:1085 |
| test100 | `test100_resolvedIsRecord` | TEST100: Test ResolvedMediaSpec is_record returns true when record marker is present | capdag.test.js:1091 |
| test101 | `test101_resolvedIsScalar` | TEST101: Test ResolvedMediaSpec is_scalar returns true when list marker is absent | capdag.test.js:1097 |
| test102 | `test102_resolvedIsList` | TEST102: Test ResolvedMediaSpec is_list returns true when list marker is present | capdag.test.js:1103 |
| test103 | `test103_resolvedIsJson` | TEST103: Test ResolvedMediaSpec is_json returns true when json tag is present | capdag.test.js:1109 |
| test104 | `test104_resolvedIsText` | TEST104: Test ResolvedMediaSpec is_text returns true when textable tag is present | capdag.test.js:1115 |
| test105 | `test105_metadataPropagation` | TEST105: Test metadata propagates from media spec def to resolved media spec | capdag.test.js:1121 |
| test106 | `test106_metadataWithValidation` | TEST106: Test metadata and validation can coexist in media spec definition | capdag.test.js:1144 |
| test107 | `test107_extensionsPropagation` | TEST107: Test extensions field propagates from media spec def to resolved | capdag.test.js:1163 |
| test108 | `test108_extensionsSerialization` | TEST108: Test creating new cap with URN, title, and command verifies correct initialization | capdag.test.js:1179 |
| test109 | `test109_extensionsWithMetadataAndValidation` | TEST109: Test creating cap with metadata initializes and retrieves metadata correctly | capdag.test.js:1187 |
| test110 | `test110_multipleExtensions` | TEST110: Test cap matching with subset semantics for request fulfillment | capdag.test.js:1206 |
| test115 | `test115_capArgSerialization` | TEST115: Test CapArg serialization and deserialization with multiple sources | capdag.test.js:1222 |
| test116 | `test116_capArgConstructors` | TEST116: Test CapArg constructor methods basic and with_description create args correctly | capdag.test.js:1255 |
| test150 | `test150_capManifestJsonSerialization` | TEST150: JSON roundtrip | capdag.test.js:1283 |
| test156 | `test156_stdinSourceFromData` | TEST156: Test creating StdinSource Data variant with byte vector | capdag.test.js:1439 |
| test157 | `test157_stdinSourceFromFileReference` | TEST157: Test creating StdinSource FileReference variant with all required fields | capdag.test.js:1450 |
| test158 | `test158_stdinSourceWithEmptyData` | TEST158: Test StdinSource Data with empty vector stores and retrieves correctly | capdag.test.js:1467 |
| test159 | `test159_stdinSourceWithBinaryContent` | TEST159: Test StdinSource Data with binary content like PNG header bytes | capdag.test.js:1475 |
| test274 | `test274_capArgumentValueNew` | TEST274: Test CapArgumentValue::new stores media_urn and raw byte value | capdag.test.js:1489 |
| test275 | `test275_capArgumentValueFromStr` | TEST275: Test CapArgumentValue::from_str converts string to UTF-8 bytes | capdag.test.js:1496 |
| test276 | `test276_capArgumentValueAsStrValid` | TEST276: Test CapArgumentValue::value_as_str succeeds for UTF-8 data | capdag.test.js:1503 |
| test277 | `test277_capArgumentValueAsStrInvalidUtf8` | TEST277: Test CapArgumentValue::value_as_str fails for non-UTF-8 binary data | capdag.test.js:1509 |
| test278 | `test278_capArgumentValueEmpty` | TEST278: Test CapArgumentValue::new with empty value stores empty vec | capdag.test.js:1521 |
| test282 | `test282_capArgumentValueUnicode` | TEST282: Test CapArgumentValue::from_str with Unicode string preserves all characters | capdag.test.js:1530 |
| test283 | `test283_capArgumentValueLargeBinary` | TEST283: Test CapArgumentValue with large binary payload preserves all bytes | capdag.test.js:1536 |
| test304 | `test304_mediaAvailabilityOutputConstant` | TEST304: Test MEDIA_AVAILABILITY_OUTPUT constant parses as valid media URN with correct tags | capdag.test.js:1555 |
| test305 | `test305_mediaPathOutputConstant` | TEST305: Test MEDIA_PATH_OUTPUT constant parses as valid media URN with correct tags | capdag.test.js:1565 |
| test306 | `test306_availabilityAndPathOutputDistinct` | TEST306: Test MEDIA_AVAILABILITY_OUTPUT and MEDIA_PATH_OUTPUT are distinct URNs | capdag.test.js:1575 |
| test307 | `test307_modelAvailabilityUrn` | TEST307: Test model_availability_urn builds valid cap URN with correct op and media specs | capdag.test.js:1589 |
| test308 | `test308_modelPathUrn` | TEST308: Test model_path_urn builds valid cap URN with correct op and media specs | capdag.test.js:1601 |
| test309 | `test309_modelAvailabilityAndPathAreDistinct` | TEST309: Test model_availability_urn and model_path_urn produce distinct URNs | capdag.test.js:1613 |
| test310 | `test310_llmGenerateTextUrn` | TEST310: llm_generate_text_urn() produces a valid cap URN with textable in/out specs | capdag.test.js:1620 |
| test312 | `test312_allUrnBuildersProduceValidUrns` | TEST312: Test all URN builders produce parseable cap URNs | capdag.test.js:1643 |
| test320 | `test320_cartridgeInfoConstruction` | TEST320-335: CartridgeRepoServer and CartridgeRepoClient tests | capdag.test.js:2000 |
| test321 | `test321_cartridgeInfoIsSigned` | TEST321: CartridgeInfo.is_signed() returns true when signature is present | capdag.test.js:2034 |
| test322 | `test322_cartridgeInfoBuildForPlatform` | TEST322: CartridgeInfo.build_for_platform() returns the build matching the current platform | capdag.test.js:2046 |
| test323 | `test323_cartridgeRepoServerValidateRegistry` | TEST323: CartridgeRepoServer requires schema 5.0 and rejects older. | capdag.test.js:2080 |
| test324 | `test324_cartridgeRepoServerTransformToArray` | TEST324: CartridgeRepoServer walks both channels and emits a flat CartridgeInfo array preserving channel provenance. Release entries appear first. | capdag.test.js:2119 |
| test325 | `test325_cartridgeRepoServerGetCartridges` | TEST325: CartridgeRepoServer.getCartridges() wraps the transformed flat array (across both channels) in the response envelope. | capdag.test.js:2157 |
| test326 | `test326_cartridgeRepoServerGetCartridgeById` | TEST326: CartridgeRepoServer.getCartridgeById() requires (channel, id). Same id looked up in the wrong channel must miss — channels are independent namespaces. | capdag.test.js:2171 |
| test327 | `test327_cartridgeRepoServerSearchCartridges` | TEST327: CartridgeRepoServer.searchCartridges() filters across both channels by name/description/tags/cap titles. Cap URN strings are not substring-matched. | capdag.test.js:2203 |
| test328 | `test328_cartridgeRepoServerGetByCategory` | TEST328: CartridgeRepoServer.getCartridgesByCategory() filters cartridges by category across both channels. | capdag.test.js:2225 |
| test329 | `test329_cartridgeRepoServerGetByCap` | TEST329: CartridgeRepoServer.getCartridgesByCap() parses the input URN and matches each declared cap via `conformsTo`. Tag-order differences resolve because matching is order-theoretic, not string. | capdag.test.js:2244 |
| test330 | `test330_cartridgeRepoClientUpdateCache` | TEST330: CartridgeRepoClient updates its local cache keyed by "<channel>:<id>". The cache holds release and nightly entries independently — the same id is allowed in both. | capdag.test.js:2261 |
| test331 | `test331_cartridgeRepoClientGetSuggestions` | TEST331: CartridgeRepoClient.getSuggestionsForCap() returns cartridge suggestions with channel propagated onto each suggestion. | capdag.test.js:2289 |
| test332 | `test332_cartridgeRepoClientGetCartridge` | TEST332: CartridgeRepoClient.getCartridge() requires (channel, id). Same id in the wrong channel must miss. | capdag.test.js:2319 |
| test333 | `test333_cartridgeRepoClientGetAllCaps` | TEST333: CartridgeRepoClient.getAllAvailableCaps() returns the set of normalized URNs across both channels. | capdag.test.js:2364 |
| test334 | `test334_cartridgeRepoClientNeedsSync` | TEST334: CartridgeRepoClient.needsSync() returns true when cache is empty / stale, false right after a fresh update. | capdag.test.js:2381 |
| test335 | `test335_cartridgeRepoServerClientIntegration` | TEST335: Round-trip: server produces a v5.0 response, client consumes it, channel provenance is preserved end-to-end. | capdag.test.js:2400 |
| test597 | `test597_capArgWithFullDefinition` | TEST597: CapArg::with_full_definition stores all fields including optional ones | capdag.test.js:1339 |
| test639 | `test639_emptyCapIsIllegal` | TEST639: cap: (empty) is the illegal bare top form | capdag.test.js:2727 |
| test640 | `test640_inOnlyIsIllegal` | TEST640: cap:in collapses to the same illegal bare top form | capdag.test.js:2736 |
| test641 | `test641_outOnlyIsIllegal` | TEST641: cap:out collapses to the same illegal bare top form | capdag.test.js:2745 |
| test642 | `test642_inOutWithoutValuesAreIllegal` | TEST642: cap:in;out collapses to the same illegal bare top form | capdag.test.js:2754 |
| test643 | `test643_explicitAsteriskIsIllegal` | TEST643: cap:in=*;out=* is the same illegal bare top form | capdag.test.js:2763 |
| test644 | `test644_specificInWildcardOutIsIllegal` | TEST644: cap:in=media:;out=* is the same illegal bare top form | capdag.test.js:2772 |
| test645 | `test645_wildcardInSpecificOut` | TEST645: cap:in=*;out=media:text has wildcard in, specific out | capdag.test.js:2781 |
| test646 | `test646_invalidInSpecFails` | TEST646: cap:in=foo fails (invalid media URN) | capdag.test.js:2788 |
| test647 | `test647_invalidOutSpecFails` | TEST647: cap:in=media:;out=bar fails (invalid media URN) | capdag.test.js:2797 |
| test648 | `test648_wildcardAcceptsSpecific` | TEST648: Wildcard in/out match specific caps | capdag.test.js:2806 |
| test649 | `test649_specificityScoring` | TEST649: Specificity - wildcard has 0, specific has tag count | capdag.test.js:2815 |
| test650 | `test650_wildcardPreserveOtherTags` | TEST650: cap:in=media:;out=media:;test preserves other tags | capdag.test.js:2824 |
| test651 | `test651_wildcardGenericFormsRejected` | TEST651: Generic top-to-top spellings are all rejected. | capdag.test.js:2833 |
| test652 | `test652_capIdentityConstantWorks` | TEST652: CAP_IDENTITY constant names the true identity cap, not bare cap: | capdag.test.js:2854 |
| test653 | `test653_invalidEffectNoneDeclarationRejected` | TEST653: invalid effect=none declarations fail at construction. | capdag.test.js:2871 |
| test654 | `test654_effectNonePreservesRuntimeMedia` | TEST654: effect=none preserves runtime media identity. | capdag.test.js:2880 |
| test655 | `test655_effectDeclaredUsesDeclaredOutput` | TEST655: default effect=declared does not preserve runtime refinements. | capdag.test.js:2889 |
| test656 | `test656_invalidEffectNoneFailsHard` | TEST656: invalid effect=none declarations fail hard at construction. | capdag.test.js:2900 |
| test657 | `test657_effectDispatchRequiresExplicitWildcard` | TEST657: omitted effect means declared; unconstrained effect must be explicit. | capdag.test.js:2909 |
| test890 | `test890_directionSemanticMatching` | TEST890: Semantic direction matching - generic provider matches specific request | capdag.test.js:720 |
| test891 | `test891_directionSemanticSpecificity` | TEST891: Semantic direction specificity — more constraints in either axis means a higher score under the truth-table-driven sum. media: (top, no tags) scores 0; each marker tag scores 2; each exact tag scores 3. | capdag.test.js:773 |
| test939 | `test939_capUrnCanonicalFormDropsWildcardInOut` | TEST939: The canonical form drops `in=media:` and `out=media:` segments. Every spelling of "the same cap with wildcard in/out" collapses to one byte-identical canonical string. This is the contract that makes registry lookups work: the cap-publisher hashes `<canonical-urn>` to compute the cache key, and every language port (Rust, Go, Python, JS, ObjC) must agree on the canonical form for cross-language lookups to land on the same key. A regression that emitted the wildcard segments would silently move the published cap to a different SHA-256 bucket, 404'ing every reader that hashes the canonical form. | capdag.test.js:297 |
| test1294 | `test1294_rule11VoidInputWithStdinRejected` | TEST1294: RULE11 - void-input cap with stdin source rejected | capdag.test.js:2671 |
| test1295 | `test1295_rule11NonVoidInputWithoutStdinRejected` | TEST1295: RULE11 - non-void-input cap without stdin source rejected | capdag.test.js:2686 |
| test1296 | `test1296_rule11VoidInputCliFlagOnly` | TEST1296: RULE11 - void-input cap with only cli_flag sources passes | capdag.test.js:2701 |
| test1297 | `test1297_rule11NonVoidInputWithStdin` | TEST1297: RULE11 - non-void-input cap with stdin source passes | capdag.test.js:2711 |
| test1298 | `test1298_isBool` | TEST1298: is_bool returns true only when bool marker tag is present | capdag.test.js:2482 |
| test1299 | `test1299_isFilePath` | TEST1299: isFilePath returns true for the single file-path media URN, false for everything else. There is no "array" variant — cardinality is carried by is_sequence on the wire, not by URN tags. | capdag.test.js:2496 |
| test1302 | `test1302_predicateConstantConsistency` | TEST1302: predicates are consistent with constants — every constant triggers exactly the expected predicates | capdag.test.js:2515 |
| test1303 | `test1303_withoutTag` | TEST1303: without_tag removes tag, rejects structural keys, case-insensitive for keys | capdag.test.js:2555 |
| test1304 | `test1304_withInOutSpec` | TEST1304: with_in_spec and with_out_spec change direction specs | capdag.test.js:2575 |
| test1305 | `test1305_findAllMatches` | TEST1305: CapMatcher::find_all_matches returns all matching caps sorted by specificity | capdag.test.js:2604 |
| test1306 | `test1306_areCompatible` | TEST1306: CapMatcher::are_compatible detects bidirectional overlap | capdag.test.js:2622 |
| test1307 | `test1307_withTagRejectsStructuralKeys` | TEST1307: with_tag rejects structural keys | capdag.test.js:2647 |
| test1308 | `test1308_builderRejectsStructuralKeys` | TEST1308: builder rejects structural keys on tag/marker | capdag.test.js:2655 |
| test1312 | `test1312_isImage` | TEST1312: is_image returns true only when image marker tag is present | capdag.test.js:2437 |
| test1313 | `test1313_isAudio` | TEST1313: is_audio returns true only when audio marker tag is present | capdag.test.js:2449 |
| test1314 | `test1314_isVideo` | TEST1314: is_video returns true only when video marker tag is present | capdag.test.js:2460 |
| test1315 | `test1315_isNumeric` | TEST1315: is_numeric returns true only when numeric marker tag is present | capdag.test.js:2470 |
| test1800 | `test1800_kindIdentityOnlyForBareCap` | TEST1800: Identity classifier — only explicit effect=none qualifies. | capdag.test.js:5575 |
| test1801 | `test1801_kindSourceWhenInputIsVoid` | TEST1801: Source classifier — in=media:void, out non-void. | capdag.test.js:5602 |
| test1802 | `test1802_kindSinkWhenOutputIsVoid` | TEST1802: Sink classifier — out=media:void, in non-void. | capdag.test.js:5611 |
| test1803 | `test1803_kindEffectWhenBothSidesVoid` | TEST1803: Effect classifier — both sides void. Reads as `() → ()`. | capdag.test.js:5620 |
| test1804 | `test1804_kindTransformForNormalDataProcessors` | TEST1804: Transform classifier — at least one side non-void, and the cap is not the bare identity. | capdag.test.js:5631 |
| test1805 | `test1805_kindInvariantUnderCanonicalSpellings` | TEST1805: Kind is invariant under canonicalization. The same morphism written in many surface forms must classify the same way once parsed. | capdag.test.js:5681 |
| test1810 | `test1810_mediaVoidIsAtomic` | TEST1810: media:void is atomic — refinements are parse errors. Mirrored across every language port (Rust, Go, Python, Swift/ObjC, JS) under the SAME number. Any divergence is a wire-level inconsistency — the unit type's atomicity is part of the protocol's deepest layer, not a per-port detail. | capdag.test.js:5646 |
| test1820 | `test1820_specificityQuestionIsZero` | TEST1820: A `?`-valued cap-tag scores 0. Same as missing. | capdag.test.js:5722 |
| test1821 | `test1821_specificityMustNotHaveIsFive` | TEST1821: A `!`-valued cap-tag scores 5 (top of negative chain). | capdag.test.js:5732 |
| test1822 | `test1822_specificityMustHaveAnyIsTwo` | TEST1822: A `*`-valued cap-tag (including bare markers) scores 2. | capdag.test.js:5739 |
| test1823 | `test1823_specificityExactValueIsFour` | TEST1823: An exact-valued cap-tag scores 4. | capdag.test.js:5753 |
| test1824 | `test1824_specificityCombinedYAxis` | TEST1824: All six forms compose additively on a single cap. y combining 0+1+2+3+4+5 must sum to 15. | capdag.test.js:5761 |
| test1830 | `test1830_canonicalizeNoConstraint` | TEST1830: ?x ≡ x? ≡ x=? all canonicalize to ?x. | capdag.test.js:5772 |
| test1831 | `test1831_canonicalizeAbsentOrNotValue` | TEST1831: ?x=v and x?=v both canonicalize to x?=v. The third hypothetical form `x=?v` is NOT recognized as a qualifier — a value starting with `?` is just an exact value beginning with a `?` character. | capdag.test.js:5785 |
| test1832 | `test1832_canonicalizeMustHaveAny` | TEST1832: x ≡ x=* both canonicalize to bare x. | capdag.test.js:5801 |
| test1833 | `test1833_canonicalizePresentNotValue` | TEST1833: !x=v and x!=v both canonicalize to x!=v. The third hypothetical form `x=!v` is NOT recognized as a qualifier — a value starting with `!` is just an exact value beginning with a `!` character. | capdag.test.js:5814 |
| test1834 | `test1834_canonicalizeExactValue` | TEST1834: x=v stays as x=v. | capdag.test.js:5830 |
| test1835 | `test1835_canonicalizeMustNotHave` | TEST1835: !x ≡ x! ≡ x=! all canonicalize to !x. | capdag.test.js:5836 |
| test1842 | `test1842_truthTableFullCrossProduct` | TEST1842: Full 6×6 truth table. | capdag.test.js:5846 |
| test1843 | `test1843_rejectInvalidCombinations` | TEST1843: Invalid qualifier combinations must be rejected. | capdag.test.js:5874 |
| test1844 | `test1844_axisWeightingOutDominates` | TEST1844: out-axis difference dominates combined in+y differences. | capdag.test.js:5889 |
| test1845 | `test1845_axisWeightingInDominatesY` | TEST1845: With equal out, in-axis dominates over y-axis. | capdag.test.js:5899 |
| test1846 | `test1846_axisWeightingDecodedLayout` | TEST1846: Decoded layout — 10000*out + 100*in + y. | capdag.test.js:5909 |
| | | | |
| unnumbered | `testCapFabAddCapPopulatesEdgesAndNodes` | Add a cap and check it becomes an edge with from/to nodes and carries the registry name we passed. This is exactly the shape the renderer depends on. | capdag.test.js:1382 |
| unnumbered | `testCapFabDistinctRegistryNames` | Each edge must carry the registry name it was added with. This is how the renderer colours/groups edges by provenance in browse mode. | capdag.test.js:1421 |
| unnumbered | `testCapFabGetOutgoingConformsToMatching` | getOutgoing takes a concrete source URN and returns edges whose from_spec the source conforms to. It must NOT be a plain string lookup. | capdag.test.js:1400 |
| unnumbered | `testJS_buildExtensionIndex` | These tests cover JS-specific functionality not in the Rust numbering scheme but are important for capdag-js correctness. | capdag.test.js:1663 |
| unnumbered | `testJS_capDocumentationOmittedWhenNull` | When documentation is null, toJSON must omit the field entirely. This matches the Rust serializer's skip-when-None semantics and the ObjC toDictionary behaviour. A regression where null is emitted as `documentation: null` would break the symmetric round-trip with Rust (which has no null sentinel) and pollute generated JSON. | capdag.test.js:1774 |
| unnumbered | `testJS_capDocumentationRoundTrip` | JS round-trip for the documentation field on Cap. Mirrors TEST920 in capdag/src/cap/definition.rs — the body is non-trivial (newlines, backticks, embedded quotes, Unicode) so escaping mismatches between JSON.stringify on this side and the Rust serializer on the other side surface as failures here. | capdag.test.js:1752 |
| unnumbered | `testJS_capJSONSerialization` |  | capdag.test.js:1729 |
| unnumbered | `testJS_getExtensionMappings` |  | capdag.test.js:1707 |
| unnumbered | `testJS_mediaSpecConstruction` |  | capdag.test.js:1840 |
| unnumbered | `testJS_mediaSpecDocumentationPropagatesThroughResolve` | Documentation propagates from a mediaSpecs definition through resolveMediaUrn into the resolved MediaSpec. Mirrors TEST924 on the Rust side. This is the path every UI consumer uses, so a break here makes the new field invisible everywhere downstream. | capdag.test.js:1797 |
| unnumbered | `testJS_mediaUrnsForExtension` |  | capdag.test.js:1679 |
| unnumbered | `testJS_resolveMediaUrnFromSpecs` |  | capdag.test.js:1717 |
| unnumbered | `testJS_stdinSourceKindConstants` |  | capdag.test.js:1827 |
| unnumbered | `testJS_stdinSourceNullData` |  | capdag.test.js:1833 |
| unnumbered | `testLlmGenerateTextUrnSpecs` | Mirror-specific coverage: llm_generate_text_urn input/output specs conform to MEDIA_STRING | capdag.test.js:1632 |
| unnumbered | `testMachine_aliasFallbackWithoutOpTag` |  | capdag.test.js:3579 |
| unnumbered | `testMachine_aliasFromOpTag` | Aliases are pure-index `edge_<N>` regardless of the cap's tags; there is no privileged `op` tag to derive a friendlier name from. | capdag.test.js:3568 |
| unnumbered | `testMachine_builderChaining` |  | capdag.test.js:3637 |
| unnumbered | `testMachine_builderEquivalentToParsed` |  | capdag.test.js:3645 |
| unnumbered | `testMachine_builderRoundTrip` |  | capdag.test.js:3657 |
| unnumbered | `testMachine_builderSingleEdge` | --- Machine builder tests --- | capdag.test.js:3613 |
| unnumbered | `testMachine_builderWithLoop` |  | capdag.test.js:3625 |
| unnumbered | `testMachine_capRegistryClient_construction` |  | capdag.test.js:3941 |
| unnumbered | `testMachine_capRegistryEntry_construction` | Phase 0B: FabricRegistryClient tests | capdag.test.js:3905 |
| unnumbered | `testMachine_capRegistryEntry_defaults` |  | capdag.test.js:3948 |
| unnumbered | `testMachine_capUrnInMediaUrn` |  | capdag.test.js:3684 |
| unnumbered | `testMachine_capUrnIsComparable` |  | capdag.test.js:3677 |
| unnumbered | `testMachine_capUrnIsEquivalent` | --- CapUrn.isEquivalent/isComparable tests --- | capdag.test.js:3669 |
| unnumbered | `testMachine_capUrnOutMediaUrn` |  | capdag.test.js:3691 |
| unnumbered | `testMachine_conflictingMediaTypesFail` |  | capdag.test.js:3045 |
| unnumbered | `testMachine_differentAliasesSameGraph` |  | capdag.test.js:3067 |
| unnumbered | `testMachine_displayEdge` |  | capdag.test.js:3412 |
| unnumbered | `testMachine_displayGraph` |  | capdag.test.js:3423 |
| unnumbered | `testMachine_duplicateAlias` |  | capdag.test.js:2938 |
| unnumbered | `testMachine_duplicateOpTagsDisambiguated` | Pure-index aliases inherently disambiguate edges that share a marker tag. | capdag.test.js:3591 |
| unnumbered | `testMachine_edgeEquivalenceDifferentCapUrns` |  | capdag.test.js:3223 |
| unnumbered | `testMachine_edgeEquivalenceDifferentLoopFlag` |  | capdag.test.js:3255 |
| unnumbered | `testMachine_edgeEquivalenceDifferentSourceCount` |  | capdag.test.js:3287 |
| unnumbered | `testMachine_edgeEquivalenceDifferentTargets` |  | capdag.test.js:3239 |
| unnumbered | `testMachine_edgeEquivalenceSameUrns` | --- Machine graph tests (mirrors graph.rs tests) --- | capdag.test.js:3207 |
| unnumbered | `testMachine_edgeEquivalenceSourceOrderIndependent` |  | capdag.test.js:3271 |
| unnumbered | `testMachine_emptyInput` | --- Machine parser tests (mirrors parser.rs tests) --- | capdag.test.js:2923 |
| unnumbered | `testMachine_errorLocation_duplicateAlias` |  | capdag.test.js:3811 |
| unnumbered | `testMachine_errorLocation_parseError` |  | capdag.test.js:3801 |
| unnumbered | `testMachine_errorLocation_undefinedAlias` |  | capdag.test.js:3825 |
| unnumbered | `testMachine_fanInSecondaryAssignedByPriorWiring` |  | capdag.test.js:2995 |
| unnumbered | `testMachine_fanInSecondaryUnassignedGetsWildcard` |  | capdag.test.js:3008 |
| unnumbered | `testMachine_fanOut` |  | capdag.test.js:2978 |
| unnumbered | `testMachine_graphEmpty` |  | capdag.test.js:3360 |
| unnumbered | `testMachine_graphEmptyEquivalence` |  | capdag.test.js:3366 |
| unnumbered | `testMachine_graphEquivalenceReorderedEdges` |  | capdag.test.js:3318 |
| unnumbered | `testMachine_graphEquivalenceSameEdges` |  | capdag.test.js:3303 |
| unnumbered | `testMachine_graphNotEquivalentDifferentCap` |  | capdag.test.js:3347 |
| unnumbered | `testMachine_graphNotEquivalentDifferentEdgeCount` |  | capdag.test.js:3333 |
| unnumbered | `testMachine_headerOnlyNoWirings` |  | capdag.test.js:2931 |
| unnumbered | `testMachine_leafTargetsLinearChain` |  | capdag.test.js:3386 |
| unnumbered | `testMachine_lineBasedAndBracketedParseSameGraph` |  | capdag.test.js:3181 |
| unnumbered | `testMachine_lineBasedEquivalentToBracketed` |  | capdag.test.js:3148 |
| unnumbered | `testMachine_lineBasedFanIn` |  | capdag.test.js:3127 |
| unnumbered | `testMachine_lineBasedFormatSerialization` |  | capdag.test.js:3160 |
| unnumbered | `testMachine_lineBasedLoop` |  | capdag.test.js:3118 |
| unnumbered | `testMachine_lineBasedSimpleChain` | --- Machine parser line-based mode tests --- | capdag.test.js:3095 |
| unnumbered | `testMachine_lineBasedTwoStepChain` |  | capdag.test.js:3108 |
| unnumbered | `testMachine_loopEdge` |  | capdag.test.js:3019 |
| unnumbered | `testMachine_malformedInputFails` |  | capdag.test.js:3079 |
| unnumbered | `testMachine_mediaRegistryEntry_construction` |  | capdag.test.js:3928 |
| unnumbered | `testMachine_mediaUrnIsComparable` |  | capdag.test.js:3708 |
| unnumbered | `testMachine_mediaUrnIsEquivalent` | --- MediaUrn.isEquivalent/isComparable tests --- | capdag.test.js:3700 |
| unnumbered | `testMachine_mixedBracketedAndLineBased` |  | capdag.test.js:3140 |
| unnumbered | `testMachine_multilineFormat` |  | capdag.test.js:3057 |
| unnumbered | `testMachine_multilineSerializeFormat` |  | capdag.test.js:3552 |
| unnumbered | `testMachine_nodeAliasCollision` |  | capdag.test.js:3035 |
| unnumbered | `testMachine_parseMachineWithAST_aliasMap` |  | capdag.test.js:3771 |
| unnumbered | `testMachine_parseMachineWithAST_fanInSourceLocations` |  | capdag.test.js:3760 |
| unnumbered | `testMachine_parseMachineWithAST_headerLocation` | Phase 0A: Position tracking tests | capdag.test.js:3721 |
| unnumbered | `testMachine_parseMachineWithAST_multilinePositions` |  | capdag.test.js:3751 |
| unnumbered | `testMachine_parseMachineWithAST_nodeMedia` |  | capdag.test.js:3789 |
| unnumbered | `testMachine_parseMachineWithAST_wiringLocation` |  | capdag.test.js:3737 |
| unnumbered | `testMachine_reorderedEdgesProduceSameNotation` |  | capdag.test.js:3536 |
| unnumbered | `testMachine_rootSourcesFanIn` |  | capdag.test.js:3400 |
| unnumbered | `testMachine_rootSourcesLinearChain` |  | capdag.test.js:3372 |
| unnumbered | `testMachine_roundtripFanOut` |  | capdag.test.js:3495 |
| unnumbered | `testMachine_roundtripLoopEdge` |  | capdag.test.js:3510 |
| unnumbered | `testMachine_roundtripSingleEdge` |  | capdag.test.js:3468 |
| unnumbered | `testMachine_roundtripTwoEdgeChain` |  | capdag.test.js:3481 |
| unnumbered | `testMachine_serializationIsDeterministic` |  | capdag.test.js:3523 |
| unnumbered | `testMachine_serializeEmptyGraph` |  | capdag.test.js:3464 |
| unnumbered | `testMachine_serializeSingleEdge` | --- Machine serializer tests (mirrors serializer.rs tests) --- | capdag.test.js:3436 |
| unnumbered | `testMachine_serializeTwoEdgeChain` |  | capdag.test.js:3451 |
| unnumbered | `testMachine_simpleLinearChain` |  | capdag.test.js:2949 |
| unnumbered | `testMachine_toMermaid_emptyGraph` |  | capdag.test.js:3868 |
| unnumbered | `testMachine_toMermaid_fanIn` |  | capdag.test.js:3874 |
| unnumbered | `testMachine_toMermaid_fanOut` |  | capdag.test.js:3885 |
| unnumbered | `testMachine_toMermaid_linearChain` | Phase 0C: Machine.toMermaid() tests | capdag.test.js:3839 |
| unnumbered | `testMachine_toMermaid_loopEdge` |  | capdag.test.js:3857 |
| unnumbered | `testMachine_twoStepChain` |  | capdag.test.js:2964 |
| unnumbered | `testMachine_undefinedAliasFails` |  | capdag.test.js:3028 |
| unnumbered | `testMachine_unterminatedBracketFails` |  | capdag.test.js:3086 |
| unnumbered | `testMachine_whitespaceOnly` |  | capdag.test.js:2927 |
| unnumbered | `testRenderer_buildBrowseGraphData_rejectsMissingMediaTitles` |  | capdag.test.js:4143 |
| unnumbered | `testRenderer_buildEditorGraphData_capWithoutCompleteArgsIsDropped` |  | capdag.test.js:5271 |
| unnumbered | `testRenderer_buildEditorGraphData_cardinalityFromDataSlotSequenceFlags` |  | capdag.test.js:5252 |
| unnumbered | `testRenderer_buildEditorGraphData_collapsesCapsIntoLabeledEdges` |  | capdag.test.js:5196 |
| unnumbered | `testRenderer_buildEditorGraphData_loopMarkedEdgeGetsLoopClass` |  | capdag.test.js:5234 |
| unnumbered | `testRenderer_buildEditorGraphData_rejectsEdgeWithMissingSource` |  | capdag.test.js:5288 |
| unnumbered | `testRenderer_buildResolvedMachineGraphData_duplicateNodeIdAcrossStrandsFailsHard` |  | capdag.test.js:5498 |
| unnumbered | `testRenderer_buildResolvedMachineGraphData_fanInProducesEdgePerAssignment` |  | capdag.test.js:5396 |
| unnumbered | `testRenderer_buildResolvedMachineGraphData_loopEdgeGetsLoopClass` |  | capdag.test.js:5362 |
| unnumbered | `testRenderer_buildResolvedMachineGraphData_multiStrandKeepsStrandsDisjoint` |  | capdag.test.js:5436 |
| unnumbered | `testRenderer_buildResolvedMachineGraphData_singleStrandLinearChain` | ---------------- resolved-machine builder ---------------- | capdag.test.js:5304 |
| unnumbered | `testRenderer_buildRunGraphData_allFailedDropsTargetPlaceholder` |  | capdag.test.js:5001 |
| unnumbered | `testRenderer_buildRunGraphData_backboneHasNoForeachNode` |  | capdag.test.js:4947 |
| unnumbered | `testRenderer_buildRunGraphData_closedForeachSuccessMergesAtCollectTarget` |  | capdag.test.js:5127 |
| unnumbered | `testRenderer_buildRunGraphData_failureWithoutFailedCapRendersFullTrace` |  | capdag.test.js:4850 |
| unnumbered | `testRenderer_buildRunGraphData_pagesSuccessesAndFailures` |  | capdag.test.js:4780 |
| unnumbered | `testRenderer_buildRunGraphData_unclosedForeachSuccessNoMerge` |  | capdag.test.js:5066 |
| unnumbered | `testRenderer_buildRunGraphData_usesCapUrnIsEquivalentForFailedCap` |  | capdag.test.js:4888 |
| unnumbered | `testRenderer_buildStrandGraphData_foreachCollectSpan` |  | capdag.test.js:4337 |
| unnumbered | `testRenderer_buildStrandGraphData_nestedForEachThrows` |  | capdag.test.js:4452 |
| unnumbered | `testRenderer_buildStrandGraphData_sequenceShowsCardinality` |  | capdag.test.js:4317 |
| unnumbered | `testRenderer_buildStrandGraphData_singleCapPlain` |  | capdag.test.js:4290 |
| unnumbered | `testRenderer_buildStrandGraphData_standaloneCollect` |  | capdag.test.js:4388 |
| unnumbered | `testRenderer_buildStrandGraphData_unclosedForEachBody` |  | capdag.test.js:4415 |
| unnumbered | `testRenderer_canonicalMediaUrn_normalizesTagOrder` |  | capdag.test.js:4103 |
| unnumbered | `testRenderer_canonicalMediaUrn_preservesValueTags` |  | capdag.test.js:4112 |
| unnumbered | `testRenderer_canonicalMediaUrn_rejectsCapUrn` |  | capdag.test.js:4117 |
| unnumbered | `testRenderer_cardinalityFromCap_findsStdinArgNotFirstArg` |  | capdag.test.js:4028 |
| unnumbered | `testRenderer_cardinalityFromCap_outputOnlySequence` |  | capdag.test.js:4060 |
| unnumbered | `testRenderer_cardinalityFromCap_rejectsStringIsSequence` |  | capdag.test.js:4071 |
| unnumbered | `testRenderer_cardinalityFromCap_scalarDefaultsWhenFieldsMissing` |  | capdag.test.js:4052 |
| unnumbered | `testRenderer_cardinalityFromCap_throwsOnNonObject` |  | capdag.test.js:4084 |
| unnumbered | `testRenderer_cardinalityLabel_allFourCases` |  | capdag.test.js:4013 |
| unnumbered | `testRenderer_cardinalityLabel_usesUnicodeArrow` |  | capdag.test.js:4020 |
| unnumbered | `testRenderer_classifyStrandCapSteps_capFlags` |  | capdag.test.js:4239 |
| unnumbered | `testRenderer_classifyStrandCapSteps_nestedForks` |  | capdag.test.js:4260 |
| unnumbered | `testRenderer_collapseStrand_plainCapDistinctTargetNoMerge` |  | capdag.test.js:4731 |
| unnumbered | `testRenderer_collapseStrand_plainCapMergesTrailingOutput` |  | capdag.test.js:4695 |
| unnumbered | `testRenderer_collapseStrand_sequenceProducingCapBeforeForeach` |  | capdag.test.js:4631 |
| unnumbered | `testRenderer_collapseStrand_singleCapBodyKeepsCapOwnLabel` |  | capdag.test.js:4480 |
| unnumbered | `testRenderer_collapseStrand_standaloneCollectCollapses` |  | capdag.test.js:4588 |
| unnumbered | `testRenderer_collapseStrand_unclosedForEachBodyCollapses` |  | capdag.test.js:4532 |
| unnumbered | `testRenderer_mediaNodeLabel_rejectsUrnDerivedLabels` |  | capdag.test.js:4129 |
| unnumbered | `testRenderer_validateBodyOutcome_rejectsNegativeIndex` | ---------------- run builder ---------------- | capdag.test.js:4770 |
| unnumbered | `testRenderer_validateEditorGraphPayload_rejectsUnknownKind` | ---------------- editor-graph builder ---------------- | capdag.test.js:5182 |
| unnumbered | `testRenderer_validateResolvedMachinePayload_rejectsMissingFields` |  | capdag.test.js:5533 |
| unnumbered | `testRenderer_validateStrandPayload_missingSourceSpec` |  | capdag.test.js:4757 |
| unnumbered | `testRenderer_validateStrandStep_rejectsUnknownVariant` |  | capdag.test.js:4200 |
| unnumbered | `testRenderer_validateStrandStep_requiresBooleanIsSequence` |  | capdag.test.js:4217 |
| unnumbered | `testUrn` |  | capdag.test.js:108 |
| unnumbered | `testisCollection` | Mirror-specific coverage: isCollection returns true when collection marker tag is present Mirror-specific coverage: N/A for JS (MEDIA_COLLECTION constants removed - no longer exists) | capdag.test.js:2504 |
---

## Unnumbered Tests

The following tests are cataloged but do not currently participate in numeric test indexing.

- `testCapFabAddCapPopulatesEdgesAndNodes` — capdag.test.js:1382
- `testCapFabDistinctRegistryNames` — capdag.test.js:1421
- `testCapFabGetOutgoingConformsToMatching` — capdag.test.js:1400
- `testJS_buildExtensionIndex` — capdag.test.js:1663
- `testJS_capDocumentationOmittedWhenNull` — capdag.test.js:1774
- `testJS_capDocumentationRoundTrip` — capdag.test.js:1752
- `testJS_capJSONSerialization` — capdag.test.js:1729
- `testJS_getExtensionMappings` — capdag.test.js:1707
- `testJS_mediaSpecConstruction` — capdag.test.js:1840
- `testJS_mediaSpecDocumentationPropagatesThroughResolve` — capdag.test.js:1797
- `testJS_mediaUrnsForExtension` — capdag.test.js:1679
- `testJS_resolveMediaUrnFromSpecs` — capdag.test.js:1717
- `testJS_stdinSourceKindConstants` — capdag.test.js:1827
- `testJS_stdinSourceNullData` — capdag.test.js:1833
- `testLlmGenerateTextUrnSpecs` — capdag.test.js:1632
- `testMachine_aliasFallbackWithoutOpTag` — capdag.test.js:3579
- `testMachine_aliasFromOpTag` — capdag.test.js:3568
- `testMachine_builderChaining` — capdag.test.js:3637
- `testMachine_builderEquivalentToParsed` — capdag.test.js:3645
- `testMachine_builderRoundTrip` — capdag.test.js:3657
- `testMachine_builderSingleEdge` — capdag.test.js:3613
- `testMachine_builderWithLoop` — capdag.test.js:3625
- `testMachine_capRegistryClient_construction` — capdag.test.js:3941
- `testMachine_capRegistryEntry_construction` — capdag.test.js:3905
- `testMachine_capRegistryEntry_defaults` — capdag.test.js:3948
- `testMachine_capUrnInMediaUrn` — capdag.test.js:3684
- `testMachine_capUrnIsComparable` — capdag.test.js:3677
- `testMachine_capUrnIsEquivalent` — capdag.test.js:3669
- `testMachine_capUrnOutMediaUrn` — capdag.test.js:3691
- `testMachine_conflictingMediaTypesFail` — capdag.test.js:3045
- `testMachine_differentAliasesSameGraph` — capdag.test.js:3067
- `testMachine_displayEdge` — capdag.test.js:3412
- `testMachine_displayGraph` — capdag.test.js:3423
- `testMachine_duplicateAlias` — capdag.test.js:2938
- `testMachine_duplicateOpTagsDisambiguated` — capdag.test.js:3591
- `testMachine_edgeEquivalenceDifferentCapUrns` — capdag.test.js:3223
- `testMachine_edgeEquivalenceDifferentLoopFlag` — capdag.test.js:3255
- `testMachine_edgeEquivalenceDifferentSourceCount` — capdag.test.js:3287
- `testMachine_edgeEquivalenceDifferentTargets` — capdag.test.js:3239
- `testMachine_edgeEquivalenceSameUrns` — capdag.test.js:3207
- `testMachine_edgeEquivalenceSourceOrderIndependent` — capdag.test.js:3271
- `testMachine_emptyInput` — capdag.test.js:2923
- `testMachine_errorLocation_duplicateAlias` — capdag.test.js:3811
- `testMachine_errorLocation_parseError` — capdag.test.js:3801
- `testMachine_errorLocation_undefinedAlias` — capdag.test.js:3825
- `testMachine_fanInSecondaryAssignedByPriorWiring` — capdag.test.js:2995
- `testMachine_fanInSecondaryUnassignedGetsWildcard` — capdag.test.js:3008
- `testMachine_fanOut` — capdag.test.js:2978
- `testMachine_graphEmpty` — capdag.test.js:3360
- `testMachine_graphEmptyEquivalence` — capdag.test.js:3366
- `testMachine_graphEquivalenceReorderedEdges` — capdag.test.js:3318
- `testMachine_graphEquivalenceSameEdges` — capdag.test.js:3303
- `testMachine_graphNotEquivalentDifferentCap` — capdag.test.js:3347
- `testMachine_graphNotEquivalentDifferentEdgeCount` — capdag.test.js:3333
- `testMachine_headerOnlyNoWirings` — capdag.test.js:2931
- `testMachine_leafTargetsLinearChain` — capdag.test.js:3386
- `testMachine_lineBasedAndBracketedParseSameGraph` — capdag.test.js:3181
- `testMachine_lineBasedEquivalentToBracketed` — capdag.test.js:3148
- `testMachine_lineBasedFanIn` — capdag.test.js:3127
- `testMachine_lineBasedFormatSerialization` — capdag.test.js:3160
- `testMachine_lineBasedLoop` — capdag.test.js:3118
- `testMachine_lineBasedSimpleChain` — capdag.test.js:3095
- `testMachine_lineBasedTwoStepChain` — capdag.test.js:3108
- `testMachine_loopEdge` — capdag.test.js:3019
- `testMachine_malformedInputFails` — capdag.test.js:3079
- `testMachine_mediaRegistryEntry_construction` — capdag.test.js:3928
- `testMachine_mediaUrnIsComparable` — capdag.test.js:3708
- `testMachine_mediaUrnIsEquivalent` — capdag.test.js:3700
- `testMachine_mixedBracketedAndLineBased` — capdag.test.js:3140
- `testMachine_multilineFormat` — capdag.test.js:3057
- `testMachine_multilineSerializeFormat` — capdag.test.js:3552
- `testMachine_nodeAliasCollision` — capdag.test.js:3035
- `testMachine_parseMachineWithAST_aliasMap` — capdag.test.js:3771
- `testMachine_parseMachineWithAST_fanInSourceLocations` — capdag.test.js:3760
- `testMachine_parseMachineWithAST_headerLocation` — capdag.test.js:3721
- `testMachine_parseMachineWithAST_multilinePositions` — capdag.test.js:3751
- `testMachine_parseMachineWithAST_nodeMedia` — capdag.test.js:3789
- `testMachine_parseMachineWithAST_wiringLocation` — capdag.test.js:3737
- `testMachine_reorderedEdgesProduceSameNotation` — capdag.test.js:3536
- `testMachine_rootSourcesFanIn` — capdag.test.js:3400
- `testMachine_rootSourcesLinearChain` — capdag.test.js:3372
- `testMachine_roundtripFanOut` — capdag.test.js:3495
- `testMachine_roundtripLoopEdge` — capdag.test.js:3510
- `testMachine_roundtripSingleEdge` — capdag.test.js:3468
- `testMachine_roundtripTwoEdgeChain` — capdag.test.js:3481
- `testMachine_serializationIsDeterministic` — capdag.test.js:3523
- `testMachine_serializeEmptyGraph` — capdag.test.js:3464
- `testMachine_serializeSingleEdge` — capdag.test.js:3436
- `testMachine_serializeTwoEdgeChain` — capdag.test.js:3451
- `testMachine_simpleLinearChain` — capdag.test.js:2949
- `testMachine_toMermaid_emptyGraph` — capdag.test.js:3868
- `testMachine_toMermaid_fanIn` — capdag.test.js:3874
- `testMachine_toMermaid_fanOut` — capdag.test.js:3885
- `testMachine_toMermaid_linearChain` — capdag.test.js:3839
- `testMachine_toMermaid_loopEdge` — capdag.test.js:3857
- `testMachine_twoStepChain` — capdag.test.js:2964
- `testMachine_undefinedAliasFails` — capdag.test.js:3028
- `testMachine_unterminatedBracketFails` — capdag.test.js:3086
- `testMachine_whitespaceOnly` — capdag.test.js:2927
- `testRenderer_buildBrowseGraphData_rejectsMissingMediaTitles` — capdag.test.js:4143
- `testRenderer_buildEditorGraphData_capWithoutCompleteArgsIsDropped` — capdag.test.js:5271
- `testRenderer_buildEditorGraphData_cardinalityFromDataSlotSequenceFlags` — capdag.test.js:5252
- `testRenderer_buildEditorGraphData_collapsesCapsIntoLabeledEdges` — capdag.test.js:5196
- `testRenderer_buildEditorGraphData_loopMarkedEdgeGetsLoopClass` — capdag.test.js:5234
- `testRenderer_buildEditorGraphData_rejectsEdgeWithMissingSource` — capdag.test.js:5288
- `testRenderer_buildResolvedMachineGraphData_duplicateNodeIdAcrossStrandsFailsHard` — capdag.test.js:5498
- `testRenderer_buildResolvedMachineGraphData_fanInProducesEdgePerAssignment` — capdag.test.js:5396
- `testRenderer_buildResolvedMachineGraphData_loopEdgeGetsLoopClass` — capdag.test.js:5362
- `testRenderer_buildResolvedMachineGraphData_multiStrandKeepsStrandsDisjoint` — capdag.test.js:5436
- `testRenderer_buildResolvedMachineGraphData_singleStrandLinearChain` — capdag.test.js:5304
- `testRenderer_buildRunGraphData_allFailedDropsTargetPlaceholder` — capdag.test.js:5001
- `testRenderer_buildRunGraphData_backboneHasNoForeachNode` — capdag.test.js:4947
- `testRenderer_buildRunGraphData_closedForeachSuccessMergesAtCollectTarget` — capdag.test.js:5127
- `testRenderer_buildRunGraphData_failureWithoutFailedCapRendersFullTrace` — capdag.test.js:4850
- `testRenderer_buildRunGraphData_pagesSuccessesAndFailures` — capdag.test.js:4780
- `testRenderer_buildRunGraphData_unclosedForeachSuccessNoMerge` — capdag.test.js:5066
- `testRenderer_buildRunGraphData_usesCapUrnIsEquivalentForFailedCap` — capdag.test.js:4888
- `testRenderer_buildStrandGraphData_foreachCollectSpan` — capdag.test.js:4337
- `testRenderer_buildStrandGraphData_nestedForEachThrows` — capdag.test.js:4452
- `testRenderer_buildStrandGraphData_sequenceShowsCardinality` — capdag.test.js:4317
- `testRenderer_buildStrandGraphData_singleCapPlain` — capdag.test.js:4290
- `testRenderer_buildStrandGraphData_standaloneCollect` — capdag.test.js:4388
- `testRenderer_buildStrandGraphData_unclosedForEachBody` — capdag.test.js:4415
- `testRenderer_canonicalMediaUrn_normalizesTagOrder` — capdag.test.js:4103
- `testRenderer_canonicalMediaUrn_preservesValueTags` — capdag.test.js:4112
- `testRenderer_canonicalMediaUrn_rejectsCapUrn` — capdag.test.js:4117
- `testRenderer_cardinalityFromCap_findsStdinArgNotFirstArg` — capdag.test.js:4028
- `testRenderer_cardinalityFromCap_outputOnlySequence` — capdag.test.js:4060
- `testRenderer_cardinalityFromCap_rejectsStringIsSequence` — capdag.test.js:4071
- `testRenderer_cardinalityFromCap_scalarDefaultsWhenFieldsMissing` — capdag.test.js:4052
- `testRenderer_cardinalityFromCap_throwsOnNonObject` — capdag.test.js:4084
- `testRenderer_cardinalityLabel_allFourCases` — capdag.test.js:4013
- `testRenderer_cardinalityLabel_usesUnicodeArrow` — capdag.test.js:4020
- `testRenderer_classifyStrandCapSteps_capFlags` — capdag.test.js:4239
- `testRenderer_classifyStrandCapSteps_nestedForks` — capdag.test.js:4260
- `testRenderer_collapseStrand_plainCapDistinctTargetNoMerge` — capdag.test.js:4731
- `testRenderer_collapseStrand_plainCapMergesTrailingOutput` — capdag.test.js:4695
- `testRenderer_collapseStrand_sequenceProducingCapBeforeForeach` — capdag.test.js:4631
- `testRenderer_collapseStrand_singleCapBodyKeepsCapOwnLabel` — capdag.test.js:4480
- `testRenderer_collapseStrand_standaloneCollectCollapses` — capdag.test.js:4588
- `testRenderer_collapseStrand_unclosedForEachBodyCollapses` — capdag.test.js:4532
- `testRenderer_mediaNodeLabel_rejectsUrnDerivedLabels` — capdag.test.js:4129
- `testRenderer_validateBodyOutcome_rejectsNegativeIndex` — capdag.test.js:4770
- `testRenderer_validateEditorGraphPayload_rejectsUnknownKind` — capdag.test.js:5182
- `testRenderer_validateResolvedMachinePayload_rejectsMissingFields` — capdag.test.js:5533
- `testRenderer_validateStrandPayload_missingSourceSpec` — capdag.test.js:4757
- `testRenderer_validateStrandStep_rejectsUnknownVariant` — capdag.test.js:4200
- `testRenderer_validateStrandStep_requiresBooleanIsSequence` — capdag.test.js:4217
- `testUrn` — capdag.test.js:108
- `testisCollection` — capdag.test.js:2504

---

*Generated from JS source tree*
*Total tests: 335*
*Total numbered tests: 185*
*Total unnumbered tests: 150*
*Total numbered tests missing descriptions: 0*
*Total numbering mismatches: 0*

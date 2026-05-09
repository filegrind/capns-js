# JS Test Catalog

**Total Tests:** 323

**Numbered Tests:** 173

**Unnumbered Tests:** 150

**Numbered Tests Missing Descriptions:** 0

**Numbering Mismatches:** 0

All numbered test numbers are unique.

This catalog lists all tests in the JS codebase.

| Test # | Function Name | Description | File |
|--------|---------------|-------------|------|
| test001 | `test001_capUrnCreation` | TEST001: Test that cap URN is created with tags parsed correctly and direction specs accessible | capdag.test.js:132 |
| test002 | `test002_directionSpecsRequired` | TEST002: Test that missing 'in' or 'out' defaults to media: wildcard | capdag.test.js:142 |
| test003 | `test003_directionMatching` | TEST003: Test that direction specs must match exactly, different in/out types don't match, wildcard matches any | capdag.test.js:153 |
| test004 | `test004_unquotedValuesLowercased` | TEST004: Test that unquoted keys and values are normalized to lowercase. Key lookup is case-insensitive: uppercase variants of `ext` resolve to the same keyed tag. | capdag.test.js:170 |
| test005 | `test005_quotedValuesPreserveCase` | TEST005: Test that quoted values preserve case while unquoted are lowercased | capdag.test.js:178 |
| test006 | `test006_quotedValueSpecialChars` | TEST006: Test that quoted values can contain special characters (semicolons, equals, spaces) | capdag.test.js:184 |
| test007 | `test007_quotedValueEscapeSequences` | TEST007: Test that escape sequences in quoted values (\" and \\) are parsed correctly | capdag.test.js:190 |
| test008 | `test008_mixedQuotedUnquoted` | TEST008: Test that mixed quoted and unquoted values in same URN parse correctly | capdag.test.js:197 |
| test009 | `test009_unterminatedQuoteError` | TEST009: Test that unterminated quote produces UnterminatedQuote error | capdag.test.js:204 |
| test010 | `test010_invalidEscapeSequenceError` | TEST010: Test that invalid escape sequences (like \n, \x) produce InvalidEscapeSequence error | capdag.test.js:217 |
| test011 | `test011_serializationSmartQuoting` | TEST011: Test that serialization uses smart quoting (no quotes for simple lowercase, quotes for special chars/uppercase) | capdag.test.js:231 |
| test012 | `test012_roundTripSimple` | TEST012: Test that simple cap URN round-trips (parse -> serialize -> parse equals original) | capdag.test.js:240 |
| test013 | `test013_roundTripQuoted` | TEST013: Test that quoted values round-trip preserving case and spaces | capdag.test.js:248 |
| test014 | `test014_roundTripEscapes` | TEST014: Test that escape sequences round-trip correctly | capdag.test.js:257 |
| test015 | `test015_capPrefixRequired` | TEST015: Test that cap: prefix is required and case-insensitive | capdag.test.js:267 |
| test016 | `test016_trailingSemicolonEquivalence` | TEST016: Test that trailing semicolon is equivalent (same hash, same string, matches) | capdag.test.js:279 |
| test017 | `test017_tagMatching` | TEST017: Test tag matching: exact match, subset match, wildcard match, value mismatch | capdag.test.js:287 |
| test018 | `test018_matchingCaseSensitiveValues` | TEST018: Test that quoted values with different case do NOT match (case-sensitive) | capdag.test.js:311 |
| test019 | `test019_missingTagHandling` | TEST019: Missing tag in instance causes rejection — pattern's tags are constraints | capdag.test.js:318 |
| test020 | `test020_specificity` | TEST020: Specificity is the sum of per-tag truth-table scores across in/out/y. Marker tags (bare segments and `key=*`) score 2 (must-have-any), exact `key=value` tags score 3, missing/`?` score 0, `!` scores 1. testUrn() builds "cap:in=media:void;out=media:record;<tags>" so the directional baseline is: in:  media:void   -> {void=*}    -> 2 out: media:record -> {record=*}  -> 2 Total directional baseline: 4. | capdag.test.js:340 |
| test021 | `test021_builder` | TEST021: Test builder creates cap URN with marker + keyed tags and direction specs. `op` is no longer a special key — operation names are markers (value-less tags). | capdag.test.js:369 |
| test022 | `test022_builderRequiresDirection` | TEST022: Test builder requires both in_spec and out_spec | capdag.test.js:383 |
| test023 | `test023_builderPreservesCase` | TEST023: Test builder lowercases keys but preserves value case | capdag.test.js:397 |
| test024 | `test024_compatibility` | TEST024: Directional accepts — pattern's tags are constraints, instance must satisfy | capdag.test.js:408 |
| test025 | `test025_bestMatch` | TEST025: Test find_best_match returns most specific matching cap | capdag.test.js:428 |
| test026 | `test026_mergeAndSubset` | TEST026: Test merge combines tags from both caps, subset keeps only specified tags | capdag.test.js:441 |
| test027 | `test027_wildcardTag` | TEST027: Test with_wildcard_tag sets tag to wildcard, including in/out | capdag.test.js:460 |
| test028 | `test028_emptyCapUrnNotAllowed` | TEST028: Test empty cap URN defaults to media: wildcard | capdag.test.js:473 |
| test029 | `test029_minimalCapUrn` | TEST029: Test minimal valid cap URN has just in and out, empty tags | capdag.test.js:480 |
| test030 | `test030_extendedCharacterSupport` | TEST030: Test extended characters (forward slashes, colons) in tag values | capdag.test.js:488 |
| test031 | `test031_wildcardRestrictions` | TEST031: Test wildcard rejected in keys but accepted in values | capdag.test.js:495 |
| test032 | `test032_duplicateKeyRejection` | TEST032: Test duplicate keys are rejected with DuplicateKey error | capdag.test.js:513 |
| test033 | `test033_numericKeyRestriction` | TEST033: Test pure numeric keys rejected, mixed alphanumeric allowed, numeric values allowed | capdag.test.js:522 |
| test034 | `test034_emptyValueError` | TEST034: Test empty values are rejected | capdag.test.js:536 |
| test035 | `test035_hasTagCaseSensitive` | TEST035: Test has_tag is case-sensitive for values, case-insensitive for keys, works for in/out | capdag.test.js:549 |
| test036 | `test036_withTagPreservesValue` | TEST036: Test with_tag preserves value case | capdag.test.js:561 |
| test037 | `test037_withTagRejectsEmptyValue` | TEST037: Test with_tag rejects empty value | capdag.test.js:568 |
| test038 | `test038_semanticEquivalence` | TEST038: Test semantic equivalence of unquoted and quoted simple lowercase values | capdag.test.js:578 |
| test039 | `test039_getTagReturnsDirectionSpecs` | TEST039: Test get_tag returns direction specs (in/out) with case-insensitive lookup | capdag.test.js:586 |
| test040 | `test040_matchingSemanticsExactMatch` | TEST040: Matching semantics - exact match succeeds | capdag.test.js:595 |
| test041 | `test041_matchingSemanticsCapMissingTag` | TEST041: Matching semantics - cap missing tag matches (implicit wildcard) | capdag.test.js:602 |
| test042 | `test042_matchingSemanticsCapHasExtraTag` | TEST042: Pattern rejects instance missing required tags | capdag.test.js:610 |
| test043 | `test043_matchingSemanticsRequestHasWildcard` | TEST043: Matching semantics - request wildcard matches specific cap value | capdag.test.js:618 |
| test044 | `test044_matchingSemanticsCapHasWildcard` | TEST044: Matching semantics - cap wildcard matches specific request value | capdag.test.js:625 |
| test045 | `test045_matchingSemanticsValueMismatch` | TEST045: Matching semantics - value mismatch does not match | capdag.test.js:632 |
| test046 | `test046_matchingSemanticsFallbackPattern` | TEST046: Matching semantics - fallback pattern (cap missing tag = implicit wildcard) | capdag.test.js:639 |
| test047 | `test047_matchingSemanticsThumbnailVoidInput` | TEST047: Matching semantics - thumbnail fallback with void input | capdag.test.js:647 |
| test048 | `test048_matchingSemanticsWildcardDirection` | TEST048: Matching semantics - wildcard direction matches anything | capdag.test.js:654 |
| test049 | `test049_matchingSemanticsCrossDimension` | TEST049: Non-overlapping tags — neither direction accepts | capdag.test.js:661 |
| test050 | `test050_matchingSemanticsDirectionMismatch` | TEST050: Matching semantics - direction mismatch prevents matching | capdag.test.js:669 |
| test054 | `test054_xv5InlineSpecRedefinitionDetected` | TEST054: XV5 - Test inline media spec redefinition of existing registry spec is detected and rejected | capdag.test.js:773 |
| test055 | `test055_xv5NewInlineSpecAllowed` | TEST055: XV5 - Test new inline media spec (not in registry) is allowed | capdag.test.js:790 |
| test056 | `test056_xv5EmptyMediaSpecsAllowed` | TEST056: XV5 - Test empty media_specs (no inline specs) passes XV5 validation | capdag.test.js:805 |
| test060 | `test060_wrongPrefixFails` | TEST060: Test wrong prefix fails with InvalidPrefix error showing expected and actual prefix | capdag.test.js:817 |
| test061 | `test061_isBinary` | TEST061: Test is_binary returns true when textable tag is absent (binary = not textable) | capdag.test.js:826 |
| test062 | `test062_isRecord` | TEST062: Test is_record returns true when record marker tag is present indicating key-value structure | capdag.test.js:842 |
| test063 | `test063_isScalar` | TEST063: Test is_scalar returns true when list marker tag is absent (scalar is default) | capdag.test.js:853 |
| test064 | `test064_isList` | TEST064: Test is_list returns true when list marker tag is present indicating ordered collection | capdag.test.js:866 |
| test065 | `test065_isOpaque` | TEST065: Test is_opaque returns true when record marker is absent (opaque is default) | capdag.test.js:875 |
| test066 | `test066_isJson` | TEST066: Test is_json returns true only when json marker tag is present for JSON representation | capdag.test.js:886 |
| test067 | `test067_isText` | TEST067: Test is_text returns true only when textable marker tag is present | capdag.test.js:892 |
| test068 | `test068_isVoid` | TEST068: Test is_void returns true when void flag or type=void tag is present | capdag.test.js:903 |
| test071 | `test071_toStringRoundtrip` | TEST071: Test to_string roundtrip ensures serialization and deserialization preserve URN structure | capdag.test.js:911 |
| test072 | `test072_constantsParse` | TEST072: Test all media URN constants parse successfully as valid media URNs | capdag.test.js:921 |
| test074 | `test074_mediaUrnMatching` | TEST074: Test media URN conforms_to using tagged URN semantics with specific and generic requirements | capdag.test.js:941 |
| test075 | `test075_accepts` | TEST075: Test accepts with implicit wildcards where handlers with fewer tags can handle more requests | capdag.test.js:955 |
| test076 | `test076_specificity` | TEST076: Test specificity increases with more tags for ranking conformance | capdag.test.js:966 |
| test077 | `test077_serdeRoundtrip` | TEST077: Test serde roundtrip serializes to JSON string and deserializes back correctly | capdag.test.js:975 |
| test078 | `test078_debugMatchingBehavior` | TEST078: conforms_to behavior between MEDIA_OBJECT and MEDIA_STRING | capdag.test.js:984 |
| test091 | `test091_resolveCustomMediaSpec` | TEST091: Test resolving custom media URN from local media_specs takes precedence over registry | capdag.test.js:999 |
| test092 | `test092_resolveCustomWithSchema` | TEST092: Test resolving custom record media spec with schema from local media_specs | capdag.test.js:1009 |
| test093 | `test093_resolveUnresolvableFailsHard` | TEST093: Test resolving unknown media URN fails with UnresolvableMediaUrn error | capdag.test.js:1026 |
| test099 | `test099_resolvedIsBinary` | TEST099: Test ResolvedMediaSpec is_binary returns true when textable tag is absent | capdag.test.js:1045 |
| test100 | `test100_resolvedIsRecord` | TEST100: Test ResolvedMediaSpec is_record returns true when record marker is present | capdag.test.js:1051 |
| test101 | `test101_resolvedIsScalar` | TEST101: Test ResolvedMediaSpec is_scalar returns true when list marker is absent | capdag.test.js:1057 |
| test102 | `test102_resolvedIsList` | TEST102: Test ResolvedMediaSpec is_list returns true when list marker is present | capdag.test.js:1063 |
| test103 | `test103_resolvedIsJson` | TEST103: Test ResolvedMediaSpec is_json returns true when json tag is present | capdag.test.js:1069 |
| test104 | `test104_resolvedIsText` | TEST104: Test ResolvedMediaSpec is_text returns true when textable tag is present | capdag.test.js:1075 |
| test105 | `test105_metadataPropagation` | TEST105: Test metadata propagates from media spec def to resolved media spec | capdag.test.js:1081 |
| test106 | `test106_metadataWithValidation` | TEST106: Test metadata and validation can coexist in media spec definition | capdag.test.js:1104 |
| test107 | `test107_extensionsPropagation` | TEST107: Test extensions field propagates from media spec def to resolved | capdag.test.js:1123 |
| test108 | `test108_extensionsSerialization` | TEST108: Test creating new cap with URN, title, and command verifies correct initialization | capdag.test.js:1139 |
| test109 | `test109_extensionsWithMetadataAndValidation` | TEST109: Test creating cap with metadata initializes and retrieves metadata correctly | capdag.test.js:1147 |
| test110 | `test110_multipleExtensions` | TEST110: Test cap matching with subset semantics for request fulfillment | capdag.test.js:1166 |
| test156 | `test156_stdinSourceFromData` | TEST156: Test creating StdinSource Data variant with byte vector | capdag.test.js:1253 |
| test157 | `test157_stdinSourceFromFileReference` | TEST157: Test creating StdinSource FileReference variant with all required fields | capdag.test.js:1264 |
| test158 | `test158_stdinSourceWithEmptyData` | TEST158: Test StdinSource Data with empty vector stores and retrieves correctly | capdag.test.js:1281 |
| test159 | `test159_stdinSourceWithBinaryContent` | TEST159: Test StdinSource Data with binary content like PNG header bytes | capdag.test.js:1289 |
| test274 | `test274_capArgumentValueNew` | TEST274: Test CapArgumentValue::new stores media_urn and raw byte value | capdag.test.js:1303 |
| test275 | `test275_capArgumentValueFromStr` | TEST275: Test CapArgumentValue::from_str converts string to UTF-8 bytes | capdag.test.js:1310 |
| test276 | `test276_capArgumentValueAsStrValid` | TEST276: Test CapArgumentValue::value_as_str succeeds for UTF-8 data | capdag.test.js:1317 |
| test277 | `test277_capArgumentValueAsStrInvalidUtf8` | TEST277: Test CapArgumentValue::value_as_str fails for non-UTF-8 binary data | capdag.test.js:1323 |
| test278 | `test278_capArgumentValueEmpty` | TEST278: Test CapArgumentValue::new with empty value stores empty vec | capdag.test.js:1335 |
| test282 | `test282_capArgumentValueUnicode` | TEST282: Test CapArgumentValue::from_str with Unicode string preserves all characters | capdag.test.js:1344 |
| test283 | `test283_capArgumentValueLargeBinary` | TEST283: Test CapArgumentValue with large binary payload preserves all bytes | capdag.test.js:1350 |
| test304 | `test304_mediaAvailabilityOutputConstant` | TEST304: Test MEDIA_AVAILABILITY_OUTPUT constant parses as valid media URN with correct tags | capdag.test.js:1369 |
| test305 | `test305_mediaPathOutputConstant` | TEST305: Test MEDIA_PATH_OUTPUT constant parses as valid media URN with correct tags | capdag.test.js:1379 |
| test306 | `test306_availabilityAndPathOutputDistinct` | TEST306: Test MEDIA_AVAILABILITY_OUTPUT and MEDIA_PATH_OUTPUT are distinct URNs | capdag.test.js:1389 |
| test307 | `test307_modelAvailabilityUrn` | TEST307: Test model_availability_urn builds valid cap URN with correct op and media specs | capdag.test.js:1403 |
| test308 | `test308_modelPathUrn` | TEST308: Test model_path_urn builds valid cap URN with correct op and media specs | capdag.test.js:1415 |
| test309 | `test309_modelAvailabilityAndPathAreDistinct` | TEST309: Test model_availability_urn and model_path_urn produce distinct URNs | capdag.test.js:1427 |
| test310 | `test310_llmGenerateTextUrn` | TEST310: llm_generate_text_urn() produces a valid cap URN with textable in/out specs | capdag.test.js:1434 |
| test312 | `test312_allUrnBuildersProduceValidUrns` | TEST312: Test all URN builders produce parseable cap URNs | capdag.test.js:1457 |
| test320 | `test320_cartridgeInfoConstruction` | TEST320-335: CartridgeRepoServer and CartridgeRepoClient tests | capdag.test.js:1820 |
| test321 | `test321_cartridgeInfoIsSigned` | TEST321: CartridgeInfo.is_signed() returns true when signature is present | capdag.test.js:1854 |
| test322 | `test322_cartridgeInfoBuildForPlatform` | TEST322: CartridgeInfo.build_for_platform() returns the build matching the current platform | capdag.test.js:1866 |
| test323 | `test323_cartridgeRepoServerValidateRegistry` | TEST323: CartridgeRepoServer requires schema 5.0 and rejects older. | capdag.test.js:1900 |
| test324 | `test324_cartridgeRepoServerTransformToArray` | TEST324: CartridgeRepoServer walks both channels and emits a flat CartridgeInfo array preserving channel provenance. Release entries appear first. | capdag.test.js:1939 |
| test325 | `test325_cartridgeRepoServerGetCartridges` | TEST325: CartridgeRepoServer.getCartridges() wraps the transformed flat array (across both channels) in the response envelope. | capdag.test.js:1977 |
| test326 | `test326_cartridgeRepoServerGetCartridgeById` | TEST326: CartridgeRepoServer.getCartridgeById() requires (channel, id). Same id looked up in the wrong channel must miss — channels are independent namespaces. | capdag.test.js:1991 |
| test327 | `test327_cartridgeRepoServerSearchCartridges` | TEST327: CartridgeRepoServer.searchCartridges() filters across both channels by name/description/tags/cap titles. Cap URN strings are not substring-matched. | capdag.test.js:2023 |
| test328 | `test328_cartridgeRepoServerGetByCategory` | TEST328: CartridgeRepoServer.getCartridgesByCategory() filters cartridges by category across both channels. | capdag.test.js:2045 |
| test329 | `test329_cartridgeRepoServerGetByCap` | TEST329: CartridgeRepoServer.getCartridgesByCap() parses the input URN and matches each declared cap via `conformsTo`. Tag-order differences resolve because matching is order-theoretic, not string. | capdag.test.js:2064 |
| test330 | `test330_cartridgeRepoClientUpdateCache` | TEST330: CartridgeRepoClient updates its local cache keyed by "<channel>:<id>". The cache holds release and nightly entries independently — the same id is allowed in both. | capdag.test.js:2081 |
| test331 | `test331_cartridgeRepoClientGetSuggestions` | TEST331: CartridgeRepoClient.getSuggestionsForCap() returns cartridge suggestions with channel propagated onto each suggestion. | capdag.test.js:2109 |
| test332 | `test332_cartridgeRepoClientGetCartridge` | TEST332: CartridgeRepoClient.getCartridge() requires (channel, id). Same id in the wrong channel must miss. | capdag.test.js:2139 |
| test333 | `test333_cartridgeRepoClientGetAllCaps` | TEST333: CartridgeRepoClient.getAllAvailableCaps() returns the set of normalized URNs across both channels. | capdag.test.js:2184 |
| test334 | `test334_cartridgeRepoClientNeedsSync` | TEST334: CartridgeRepoClient.needsSync() returns true when cache is empty / stale, false right after a fresh update. | capdag.test.js:2201 |
| test335 | `test335_cartridgeRepoServerClientIntegration` | TEST335: Round-trip: server produces a v5.0 response, client consumes it, channel provenance is preserved end-to-end. | capdag.test.js:2220 |
| test639 | `test639_emptyCapDefaultsToMediaWildcard` | TEST639: cap: (empty) defaults to in=media:;out=media: | capdag.test.js:2530 |
| test640 | `test640_inOnlyDefaultsOutToMedia` | TEST640: cap:in defaults out to media: | capdag.test.js:2538 |
| test641 | `test641_outOnlyDefaultsInToMedia` | TEST641: cap:out defaults in to media: | capdag.test.js:2545 |
| test642 | `test642_inOutWithoutValuesBecomeMedia` | TEST642: cap:in;out both become media: | capdag.test.js:2552 |
| test643 | `test643_explicitAsteriskIsWildcard` | TEST643: cap:in=*;out=* becomes media: | capdag.test.js:2559 |
| test644 | `test644_specificInWildcardOut` | TEST644: cap:in=media:;out=* has specific in, wildcard out | capdag.test.js:2566 |
| test645 | `test645_wildcardInSpecificOut` | TEST645: cap:in=*;out=media:text has wildcard in, specific out | capdag.test.js:2573 |
| test646 | `test646_invalidInSpecFails` | TEST646: cap:in=foo fails (invalid media URN) | capdag.test.js:2580 |
| test647 | `test647_invalidOutSpecFails` | TEST647: cap:in=media:;out=bar fails (invalid media URN) | capdag.test.js:2589 |
| test648 | `test648_wildcardAcceptsSpecific` | TEST648: Wildcard in/out match specific caps | capdag.test.js:2598 |
| test649 | `test649_specificityScoring` | TEST649: Specificity - wildcard has 0, specific has tag count | capdag.test.js:2607 |
| test651 | `test651_identityFormsEquivalent` | TEST651: All identity forms produce the same CapUrn | capdag.test.js:2618 |
| test653 | `test653_identityRoutingIsolation` | TEST653: Identity (no tags) does not match specific requests via routing | capdag.test.js:2638 |
| test890 | `test890_directionSemanticMatching` | TEST890: Semantic direction matching - generic provider matches specific request | capdag.test.js:680 |
| test891 | `test891_directionSemanticSpecificity` | TEST891: Semantic direction specificity — more constraints in either axis means a higher score under the truth-table-driven sum. media: (top, no tags) scores 0; each marker tag scores 2; each exact tag scores 3. | capdag.test.js:733 |
| test1294 | `test1294_rule11VoidInputWithStdinRejected` | TEST1294: RULE11 - void-input cap with stdin source rejected | capdag.test.js:2474 |
| test1295 | `test1295_rule11NonVoidInputWithoutStdinRejected` | TEST1295: RULE11 - non-void-input cap without stdin source rejected | capdag.test.js:2489 |
| test1296 | `test1296_rule11VoidInputCliFlagOnly` | TEST1296: RULE11 - void-input cap with only cli_flag sources passes | capdag.test.js:2504 |
| test1297 | `test1297_rule11NonVoidInputWithStdin` | TEST1297: RULE11 - non-void-input cap with stdin source passes | capdag.test.js:2514 |
| test1298 | `test1298_isBool` | TEST1298: is_bool returns true only when bool marker tag is present | capdag.test.js:2302 |
| test1299 | `test1299_isFilePath` | TEST1299: isFilePath returns true for the single file-path media URN, false for everything else. There is no "array" variant — cardinality is carried by is_sequence on the wire, not by URN tags. | capdag.test.js:2316 |
| test1302 | `test1302_predicateConstantConsistency` | TEST1302: predicates are consistent with constants — every constant triggers exactly the expected predicates | capdag.test.js:2335 |
| test1303 | `test1303_withoutTag` | TEST1303: without_tag removes tag, ignores in/out, case-insensitive for keys | capdag.test.js:2375 |
| test1304 | `test1304_withInOutSpec` | TEST1304: with_in_spec and with_out_spec change direction specs | capdag.test.js:2397 |
| test1305 | `test1305_findAllMatches` | TEST1305: CapMatcher::find_all_matches returns all matching caps sorted by specificity | capdag.test.js:2420 |
| test1306 | `test1306_areCompatible` | TEST1306: CapMatcher::are_compatible detects bidirectional overlap | capdag.test.js:2438 |
| test1307 | `test1307_withTagIgnoresInOut` | TEST1307: with_tag silently ignores in/out keys | capdag.test.js:2463 |
| test1312 | `test1312_isImage` | TEST1312: is_image returns true only when image marker tag is present | capdag.test.js:2257 |
| test1313 | `test1313_isAudio` | TEST1313: is_audio returns true only when audio marker tag is present | capdag.test.js:2269 |
| test1314 | `test1314_isVideo` | TEST1314: is_video returns true only when video marker tag is present | capdag.test.js:2280 |
| test1315 | `test1315_isNumeric` | TEST1315: is_numeric returns true only when numeric marker tag is present | capdag.test.js:2290 |
| test1800 | `test1800_kindIdentityOnlyForBareCap` | TEST1800: Identity classifier — only the bare cap: form qualifies. Adding any tag (even one that doesn't constrain in/out) demotes the cap to Transform because the operation/metadata axis is no longer fully generic. | capdag.test.js:5317 |
| test1801 | `test1801_kindSourceWhenInputIsVoid` | TEST1801: Source classifier — in=media:void, out non-void. | capdag.test.js:5338 |
| test1802 | `test1802_kindSinkWhenOutputIsVoid` | TEST1802: Sink classifier — out=media:void, in non-void. | capdag.test.js:5347 |
| test1803 | `test1803_kindEffectWhenBothSidesVoid` | TEST1803: Effect classifier — both sides void. Reads as `() → ()`. | capdag.test.js:5356 |
| test1804 | `test1804_kindTransformForNormalDataProcessors` | TEST1804: Transform classifier — at least one side non-void, and the cap is not the bare identity. | capdag.test.js:5367 |
| test1805 | `test1805_kindInvariantUnderCanonicalSpellings` | TEST1805: Kind is invariant under canonicalization. The same morphism written in many surface forms must classify the same way once parsed. | capdag.test.js:5417 |
| test1810 | `test1810_mediaVoidIsAtomic` | TEST1810: media:void is atomic — refinements are parse errors. Mirrored across every language port (Rust, Go, Python, Swift/ObjC, JS) under the SAME number. Any divergence is a wire-level inconsistency — the unit type's atomicity is part of the protocol's deepest layer, not a per-port detail. | capdag.test.js:5382 |
| test1820 | `test1820_specificityQuestionIsZero` | TEST1820: A `?`-valued cap-tag scores 0. Same as missing. | capdag.test.js:5458 |
| test1821 | `test1821_specificityMustNotHaveIsFive` | TEST1821: A `!`-valued cap-tag scores 5 (top of negative chain). | capdag.test.js:5468 |
| test1822 | `test1822_specificityMustHaveAnyIsTwo` | TEST1822: A `*`-valued cap-tag (including bare markers) scores 2. | capdag.test.js:5475 |
| test1823 | `test1823_specificityExactValueIsFour` | TEST1823: An exact-valued cap-tag scores 4. | capdag.test.js:5489 |
| test1824 | `test1824_specificityCombinedYAxis` | TEST1824: All six forms compose additively on a single cap. y combining 0+1+2+3+4+5 must sum to 15. | capdag.test.js:5497 |
| test1830 | `test1830_canonicalizeNoConstraint` | TEST1830: ?x ≡ x? ≡ x=? all canonicalize to ?x. | capdag.test.js:5508 |
| test1831 | `test1831_canonicalizeAbsentOrNotValue` | TEST1831: ?x=v and x?=v both canonicalize to x?=v. The third hypothetical form `x=?v` is NOT recognized as a qualifier — a value starting with `?` is just an exact value beginning with a `?` character. | capdag.test.js:5521 |
| test1832 | `test1832_canonicalizeMustHaveAny` | TEST1832: x ≡ x=* both canonicalize to bare x. | capdag.test.js:5537 |
| test1833 | `test1833_canonicalizePresentNotValue` | TEST1833: !x=v and x!=v both canonicalize to x!=v. The third hypothetical form `x=!v` is NOT recognized as a qualifier — a value starting with `!` is just an exact value beginning with a `!` character. | capdag.test.js:5550 |
| test1834 | `test1834_canonicalizeExactValue` | TEST1834: x=v stays as x=v. | capdag.test.js:5566 |
| test1835 | `test1835_canonicalizeMustNotHave` | TEST1835: !x ≡ x! ≡ x=! all canonicalize to !x. | capdag.test.js:5572 |
| test1842 | `test1842_truthTableFullCrossProduct` | TEST1842: Full 6×6 truth table. | capdag.test.js:5582 |
| test1843 | `test1843_rejectInvalidCombinations` | TEST1843: Invalid qualifier combinations must be rejected. | capdag.test.js:5610 |
| test1844 | `test1844_axisWeightingOutDominates` | TEST1844: out-axis difference dominates combined in+y differences. | capdag.test.js:5625 |
| test1845 | `test1845_axisWeightingInDominatesY` | TEST1845: With equal out, in-axis dominates over y-axis. | capdag.test.js:5635 |
| test1846 | `test1846_axisWeightingDecodedLayout` | TEST1846: Decoded layout — 10000*out + 100*in + y. | capdag.test.js:5645 |
| | | | |
| unnumbered | `testCapFabAddCapPopulatesEdgesAndNodes` | Add a cap and check it becomes an edge with from/to nodes and carries the registry name we passed. This is exactly the shape the renderer depends on. | capdag.test.js:1196 |
| unnumbered | `testCapFabDistinctRegistryNames` | Each edge must carry the registry name it was added with. This is how the renderer colours/groups edges by provenance in browse mode. | capdag.test.js:1235 |
| unnumbered | `testCapFabGetOutgoingConformsToMatching` | getOutgoing takes a concrete source URN and returns edges whose from_spec the source conforms to. It must NOT be a plain string lookup. | capdag.test.js:1214 |
| unnumbered | `testJS_buildExtensionIndex` | These tests cover JS-specific functionality not in the Rust numbering scheme but are important for capdag-js correctness. | capdag.test.js:1477 |
| unnumbered | `testJS_capDocumentationOmittedWhenNull` | When documentation is null, toJSON must omit the field entirely. This matches the Rust serializer's skip-when-None semantics and the ObjC toDictionary behaviour. A regression where null is emitted as `documentation: null` would break the symmetric round-trip with Rust (which has no null sentinel) and pollute generated JSON. | capdag.test.js:1594 |
| unnumbered | `testJS_capDocumentationRoundTrip` | JS round-trip for the documentation field on Cap. Mirrors TEST920 in capdag/src/cap/definition.rs — the body is non-trivial (newlines, backticks, embedded quotes, Unicode) so escaping mismatches between JSON.stringify on this side and the Rust serializer on the other side surface as failures here. | capdag.test.js:1572 |
| unnumbered | `testJS_capJSONSerialization` |  | capdag.test.js:1545 |
| unnumbered | `testJS_capWithMediaSpecs` |  | capdag.test.js:1531 |
| unnumbered | `testJS_getExtensionMappings` |  | capdag.test.js:1521 |
| unnumbered | `testJS_mediaSpecConstruction` |  | capdag.test.js:1660 |
| unnumbered | `testJS_mediaSpecDocumentationPropagatesThroughResolve` | Documentation propagates from a mediaSpecs definition through resolveMediaUrn into the resolved MediaSpec. Mirrors TEST924 on the Rust side. This is the path every UI consumer uses, so a break here makes the new field invisible everywhere downstream. | capdag.test.js:1617 |
| unnumbered | `testJS_mediaUrnsForExtension` |  | capdag.test.js:1493 |
| unnumbered | `testJS_stdinSourceKindConstants` |  | capdag.test.js:1647 |
| unnumbered | `testJS_stdinSourceNullData` |  | capdag.test.js:1653 |
| unnumbered | `testLlmGenerateTextUrnSpecs` | Mirror-specific coverage: llm_generate_text_urn input/output specs conform to MEDIA_STRING | capdag.test.js:1446 |
| unnumbered | `testMachine_aliasFallbackWithoutOpTag` |  | capdag.test.js:3318 |
| unnumbered | `testMachine_aliasFromOpTag` | Aliases are pure-index `edge_<N>` regardless of the cap's tags; there is no privileged `op` tag to derive a friendlier name from. | capdag.test.js:3307 |
| unnumbered | `testMachine_builderChaining` |  | capdag.test.js:3376 |
| unnumbered | `testMachine_builderEquivalentToParsed` |  | capdag.test.js:3384 |
| unnumbered | `testMachine_builderRoundTrip` |  | capdag.test.js:3396 |
| unnumbered | `testMachine_builderSingleEdge` | --- Machine builder tests --- | capdag.test.js:3352 |
| unnumbered | `testMachine_builderWithLoop` |  | capdag.test.js:3364 |
| unnumbered | `testMachine_capRegistryClient_construction` |  | capdag.test.js:3680 |
| unnumbered | `testMachine_capRegistryEntry_construction` | Phase 0B: FabricRegistryClient tests | capdag.test.js:3644 |
| unnumbered | `testMachine_capRegistryEntry_defaults` |  | capdag.test.js:3687 |
| unnumbered | `testMachine_capUrnInMediaUrn` |  | capdag.test.js:3423 |
| unnumbered | `testMachine_capUrnIsComparable` |  | capdag.test.js:3416 |
| unnumbered | `testMachine_capUrnIsEquivalent` | --- CapUrn.isEquivalent/isComparable tests --- | capdag.test.js:3408 |
| unnumbered | `testMachine_capUrnOutMediaUrn` |  | capdag.test.js:3430 |
| unnumbered | `testMachine_conflictingMediaTypesFail` |  | capdag.test.js:2784 |
| unnumbered | `testMachine_differentAliasesSameGraph` |  | capdag.test.js:2806 |
| unnumbered | `testMachine_displayEdge` |  | capdag.test.js:3151 |
| unnumbered | `testMachine_displayGraph` |  | capdag.test.js:3162 |
| unnumbered | `testMachine_duplicateAlias` |  | capdag.test.js:2677 |
| unnumbered | `testMachine_duplicateOpTagsDisambiguated` | Pure-index aliases inherently disambiguate edges that share a marker tag. | capdag.test.js:3330 |
| unnumbered | `testMachine_edgeEquivalenceDifferentCapUrns` |  | capdag.test.js:2962 |
| unnumbered | `testMachine_edgeEquivalenceDifferentLoopFlag` |  | capdag.test.js:2994 |
| unnumbered | `testMachine_edgeEquivalenceDifferentSourceCount` |  | capdag.test.js:3026 |
| unnumbered | `testMachine_edgeEquivalenceDifferentTargets` |  | capdag.test.js:2978 |
| unnumbered | `testMachine_edgeEquivalenceSameUrns` | --- Machine graph tests (mirrors graph.rs tests) --- | capdag.test.js:2946 |
| unnumbered | `testMachine_edgeEquivalenceSourceOrderIndependent` |  | capdag.test.js:3010 |
| unnumbered | `testMachine_emptyInput` | --- Machine parser tests (mirrors parser.rs tests) --- | capdag.test.js:2662 |
| unnumbered | `testMachine_errorLocation_duplicateAlias` |  | capdag.test.js:3550 |
| unnumbered | `testMachine_errorLocation_parseError` |  | capdag.test.js:3540 |
| unnumbered | `testMachine_errorLocation_undefinedAlias` |  | capdag.test.js:3564 |
| unnumbered | `testMachine_fanInSecondaryAssignedByPriorWiring` |  | capdag.test.js:2734 |
| unnumbered | `testMachine_fanInSecondaryUnassignedGetsWildcard` |  | capdag.test.js:2747 |
| unnumbered | `testMachine_fanOut` |  | capdag.test.js:2717 |
| unnumbered | `testMachine_graphEmpty` |  | capdag.test.js:3099 |
| unnumbered | `testMachine_graphEmptyEquivalence` |  | capdag.test.js:3105 |
| unnumbered | `testMachine_graphEquivalenceReorderedEdges` |  | capdag.test.js:3057 |
| unnumbered | `testMachine_graphEquivalenceSameEdges` |  | capdag.test.js:3042 |
| unnumbered | `testMachine_graphNotEquivalentDifferentCap` |  | capdag.test.js:3086 |
| unnumbered | `testMachine_graphNotEquivalentDifferentEdgeCount` |  | capdag.test.js:3072 |
| unnumbered | `testMachine_headerOnlyNoWirings` |  | capdag.test.js:2670 |
| unnumbered | `testMachine_leafTargetsLinearChain` |  | capdag.test.js:3125 |
| unnumbered | `testMachine_lineBasedAndBracketedParseSameGraph` |  | capdag.test.js:2920 |
| unnumbered | `testMachine_lineBasedEquivalentToBracketed` |  | capdag.test.js:2887 |
| unnumbered | `testMachine_lineBasedFanIn` |  | capdag.test.js:2866 |
| unnumbered | `testMachine_lineBasedFormatSerialization` |  | capdag.test.js:2899 |
| unnumbered | `testMachine_lineBasedLoop` |  | capdag.test.js:2857 |
| unnumbered | `testMachine_lineBasedSimpleChain` | --- Machine parser line-based mode tests --- | capdag.test.js:2834 |
| unnumbered | `testMachine_lineBasedTwoStepChain` |  | capdag.test.js:2847 |
| unnumbered | `testMachine_loopEdge` |  | capdag.test.js:2758 |
| unnumbered | `testMachine_malformedInputFails` |  | capdag.test.js:2818 |
| unnumbered | `testMachine_mediaRegistryEntry_construction` |  | capdag.test.js:3667 |
| unnumbered | `testMachine_mediaUrnIsComparable` |  | capdag.test.js:3447 |
| unnumbered | `testMachine_mediaUrnIsEquivalent` | --- MediaUrn.isEquivalent/isComparable tests --- | capdag.test.js:3439 |
| unnumbered | `testMachine_mixedBracketedAndLineBased` |  | capdag.test.js:2879 |
| unnumbered | `testMachine_multilineFormat` |  | capdag.test.js:2796 |
| unnumbered | `testMachine_multilineSerializeFormat` |  | capdag.test.js:3291 |
| unnumbered | `testMachine_nodeAliasCollision` |  | capdag.test.js:2774 |
| unnumbered | `testMachine_parseMachineWithAST_aliasMap` |  | capdag.test.js:3510 |
| unnumbered | `testMachine_parseMachineWithAST_fanInSourceLocations` |  | capdag.test.js:3499 |
| unnumbered | `testMachine_parseMachineWithAST_headerLocation` | Phase 0A: Position tracking tests | capdag.test.js:3460 |
| unnumbered | `testMachine_parseMachineWithAST_multilinePositions` |  | capdag.test.js:3490 |
| unnumbered | `testMachine_parseMachineWithAST_nodeMedia` |  | capdag.test.js:3528 |
| unnumbered | `testMachine_parseMachineWithAST_wiringLocation` |  | capdag.test.js:3476 |
| unnumbered | `testMachine_reorderedEdgesProduceSameNotation` |  | capdag.test.js:3275 |
| unnumbered | `testMachine_rootSourcesFanIn` |  | capdag.test.js:3139 |
| unnumbered | `testMachine_rootSourcesLinearChain` |  | capdag.test.js:3111 |
| unnumbered | `testMachine_roundtripFanOut` |  | capdag.test.js:3234 |
| unnumbered | `testMachine_roundtripLoopEdge` |  | capdag.test.js:3249 |
| unnumbered | `testMachine_roundtripSingleEdge` |  | capdag.test.js:3207 |
| unnumbered | `testMachine_roundtripTwoEdgeChain` |  | capdag.test.js:3220 |
| unnumbered | `testMachine_serializationIsDeterministic` |  | capdag.test.js:3262 |
| unnumbered | `testMachine_serializeEmptyGraph` |  | capdag.test.js:3203 |
| unnumbered | `testMachine_serializeSingleEdge` | --- Machine serializer tests (mirrors serializer.rs tests) --- | capdag.test.js:3175 |
| unnumbered | `testMachine_serializeTwoEdgeChain` |  | capdag.test.js:3190 |
| unnumbered | `testMachine_simpleLinearChain` |  | capdag.test.js:2688 |
| unnumbered | `testMachine_toMermaid_emptyGraph` |  | capdag.test.js:3607 |
| unnumbered | `testMachine_toMermaid_fanIn` |  | capdag.test.js:3613 |
| unnumbered | `testMachine_toMermaid_fanOut` |  | capdag.test.js:3624 |
| unnumbered | `testMachine_toMermaid_linearChain` | Phase 0C: Machine.toMermaid() tests | capdag.test.js:3578 |
| unnumbered | `testMachine_toMermaid_loopEdge` |  | capdag.test.js:3596 |
| unnumbered | `testMachine_twoStepChain` |  | capdag.test.js:2703 |
| unnumbered | `testMachine_undefinedAliasFails` |  | capdag.test.js:2767 |
| unnumbered | `testMachine_unterminatedBracketFails` |  | capdag.test.js:2825 |
| unnumbered | `testMachine_whitespaceOnly` |  | capdag.test.js:2666 |
| unnumbered | `testRenderer_buildBrowseGraphData_rejectsMissingMediaTitles` |  | capdag.test.js:3882 |
| unnumbered | `testRenderer_buildEditorGraphData_capWithoutCompleteArgsIsDropped` |  | capdag.test.js:5010 |
| unnumbered | `testRenderer_buildEditorGraphData_cardinalityFromDataSlotSequenceFlags` |  | capdag.test.js:4991 |
| unnumbered | `testRenderer_buildEditorGraphData_collapsesCapsIntoLabeledEdges` |  | capdag.test.js:4935 |
| unnumbered | `testRenderer_buildEditorGraphData_loopMarkedEdgeGetsLoopClass` |  | capdag.test.js:4973 |
| unnumbered | `testRenderer_buildEditorGraphData_rejectsEdgeWithMissingSource` |  | capdag.test.js:5027 |
| unnumbered | `testRenderer_buildResolvedMachineGraphData_duplicateNodeIdAcrossStrandsFailsHard` |  | capdag.test.js:5237 |
| unnumbered | `testRenderer_buildResolvedMachineGraphData_fanInProducesEdgePerAssignment` |  | capdag.test.js:5135 |
| unnumbered | `testRenderer_buildResolvedMachineGraphData_loopEdgeGetsLoopClass` |  | capdag.test.js:5101 |
| unnumbered | `testRenderer_buildResolvedMachineGraphData_multiStrandKeepsStrandsDisjoint` |  | capdag.test.js:5175 |
| unnumbered | `testRenderer_buildResolvedMachineGraphData_singleStrandLinearChain` | ---------------- resolved-machine builder ---------------- | capdag.test.js:5043 |
| unnumbered | `testRenderer_buildRunGraphData_allFailedDropsTargetPlaceholder` |  | capdag.test.js:4740 |
| unnumbered | `testRenderer_buildRunGraphData_backboneHasNoForeachNode` |  | capdag.test.js:4686 |
| unnumbered | `testRenderer_buildRunGraphData_closedForeachSuccessMergesAtCollectTarget` |  | capdag.test.js:4866 |
| unnumbered | `testRenderer_buildRunGraphData_failureWithoutFailedCapRendersFullTrace` |  | capdag.test.js:4589 |
| unnumbered | `testRenderer_buildRunGraphData_pagesSuccessesAndFailures` |  | capdag.test.js:4519 |
| unnumbered | `testRenderer_buildRunGraphData_unclosedForeachSuccessNoMerge` |  | capdag.test.js:4805 |
| unnumbered | `testRenderer_buildRunGraphData_usesCapUrnIsEquivalentForFailedCap` |  | capdag.test.js:4627 |
| unnumbered | `testRenderer_buildStrandGraphData_foreachCollectSpan` |  | capdag.test.js:4076 |
| unnumbered | `testRenderer_buildStrandGraphData_nestedForEachThrows` |  | capdag.test.js:4191 |
| unnumbered | `testRenderer_buildStrandGraphData_sequenceShowsCardinality` |  | capdag.test.js:4056 |
| unnumbered | `testRenderer_buildStrandGraphData_singleCapPlain` |  | capdag.test.js:4029 |
| unnumbered | `testRenderer_buildStrandGraphData_standaloneCollect` |  | capdag.test.js:4127 |
| unnumbered | `testRenderer_buildStrandGraphData_unclosedForEachBody` |  | capdag.test.js:4154 |
| unnumbered | `testRenderer_canonicalMediaUrn_normalizesTagOrder` |  | capdag.test.js:3842 |
| unnumbered | `testRenderer_canonicalMediaUrn_preservesValueTags` |  | capdag.test.js:3851 |
| unnumbered | `testRenderer_canonicalMediaUrn_rejectsCapUrn` |  | capdag.test.js:3856 |
| unnumbered | `testRenderer_cardinalityFromCap_findsStdinArgNotFirstArg` |  | capdag.test.js:3767 |
| unnumbered | `testRenderer_cardinalityFromCap_outputOnlySequence` |  | capdag.test.js:3799 |
| unnumbered | `testRenderer_cardinalityFromCap_rejectsStringIsSequence` |  | capdag.test.js:3810 |
| unnumbered | `testRenderer_cardinalityFromCap_scalarDefaultsWhenFieldsMissing` |  | capdag.test.js:3791 |
| unnumbered | `testRenderer_cardinalityFromCap_throwsOnNonObject` |  | capdag.test.js:3823 |
| unnumbered | `testRenderer_cardinalityLabel_allFourCases` |  | capdag.test.js:3752 |
| unnumbered | `testRenderer_cardinalityLabel_usesUnicodeArrow` |  | capdag.test.js:3759 |
| unnumbered | `testRenderer_classifyStrandCapSteps_capFlags` |  | capdag.test.js:3978 |
| unnumbered | `testRenderer_classifyStrandCapSteps_nestedForks` |  | capdag.test.js:3999 |
| unnumbered | `testRenderer_collapseStrand_plainCapDistinctTargetNoMerge` |  | capdag.test.js:4470 |
| unnumbered | `testRenderer_collapseStrand_plainCapMergesTrailingOutput` |  | capdag.test.js:4434 |
| unnumbered | `testRenderer_collapseStrand_sequenceProducingCapBeforeForeach` |  | capdag.test.js:4370 |
| unnumbered | `testRenderer_collapseStrand_singleCapBodyKeepsCapOwnLabel` |  | capdag.test.js:4219 |
| unnumbered | `testRenderer_collapseStrand_standaloneCollectCollapses` |  | capdag.test.js:4327 |
| unnumbered | `testRenderer_collapseStrand_unclosedForEachBodyCollapses` |  | capdag.test.js:4271 |
| unnumbered | `testRenderer_mediaNodeLabel_rejectsUrnDerivedLabels` |  | capdag.test.js:3868 |
| unnumbered | `testRenderer_validateBodyOutcome_rejectsNegativeIndex` | ---------------- run builder ---------------- | capdag.test.js:4509 |
| unnumbered | `testRenderer_validateEditorGraphPayload_rejectsUnknownKind` | ---------------- editor-graph builder ---------------- | capdag.test.js:4921 |
| unnumbered | `testRenderer_validateResolvedMachinePayload_rejectsMissingFields` |  | capdag.test.js:5272 |
| unnumbered | `testRenderer_validateStrandPayload_missingSourceSpec` |  | capdag.test.js:4496 |
| unnumbered | `testRenderer_validateStrandStep_rejectsUnknownVariant` |  | capdag.test.js:3939 |
| unnumbered | `testRenderer_validateStrandStep_requiresBooleanIsSequence` |  | capdag.test.js:3956 |
| unnumbered | `testUrn` |  | capdag.test.js:107 |
| unnumbered | `testisCollection` | Mirror-specific coverage: isCollection returns true when collection marker tag is present Mirror-specific coverage: N/A for JS (MEDIA_COLLECTION constants removed - no longer exists) | capdag.test.js:2324 |
---

## Unnumbered Tests

The following tests are cataloged but do not currently participate in numeric test indexing.

- `testCapFabAddCapPopulatesEdgesAndNodes` — capdag.test.js:1196
- `testCapFabDistinctRegistryNames` — capdag.test.js:1235
- `testCapFabGetOutgoingConformsToMatching` — capdag.test.js:1214
- `testJS_buildExtensionIndex` — capdag.test.js:1477
- `testJS_capDocumentationOmittedWhenNull` — capdag.test.js:1594
- `testJS_capDocumentationRoundTrip` — capdag.test.js:1572
- `testJS_capJSONSerialization` — capdag.test.js:1545
- `testJS_capWithMediaSpecs` — capdag.test.js:1531
- `testJS_getExtensionMappings` — capdag.test.js:1521
- `testJS_mediaSpecConstruction` — capdag.test.js:1660
- `testJS_mediaSpecDocumentationPropagatesThroughResolve` — capdag.test.js:1617
- `testJS_mediaUrnsForExtension` — capdag.test.js:1493
- `testJS_stdinSourceKindConstants` — capdag.test.js:1647
- `testJS_stdinSourceNullData` — capdag.test.js:1653
- `testLlmGenerateTextUrnSpecs` — capdag.test.js:1446
- `testMachine_aliasFallbackWithoutOpTag` — capdag.test.js:3318
- `testMachine_aliasFromOpTag` — capdag.test.js:3307
- `testMachine_builderChaining` — capdag.test.js:3376
- `testMachine_builderEquivalentToParsed` — capdag.test.js:3384
- `testMachine_builderRoundTrip` — capdag.test.js:3396
- `testMachine_builderSingleEdge` — capdag.test.js:3352
- `testMachine_builderWithLoop` — capdag.test.js:3364
- `testMachine_capRegistryClient_construction` — capdag.test.js:3680
- `testMachine_capRegistryEntry_construction` — capdag.test.js:3644
- `testMachine_capRegistryEntry_defaults` — capdag.test.js:3687
- `testMachine_capUrnInMediaUrn` — capdag.test.js:3423
- `testMachine_capUrnIsComparable` — capdag.test.js:3416
- `testMachine_capUrnIsEquivalent` — capdag.test.js:3408
- `testMachine_capUrnOutMediaUrn` — capdag.test.js:3430
- `testMachine_conflictingMediaTypesFail` — capdag.test.js:2784
- `testMachine_differentAliasesSameGraph` — capdag.test.js:2806
- `testMachine_displayEdge` — capdag.test.js:3151
- `testMachine_displayGraph` — capdag.test.js:3162
- `testMachine_duplicateAlias` — capdag.test.js:2677
- `testMachine_duplicateOpTagsDisambiguated` — capdag.test.js:3330
- `testMachine_edgeEquivalenceDifferentCapUrns` — capdag.test.js:2962
- `testMachine_edgeEquivalenceDifferentLoopFlag` — capdag.test.js:2994
- `testMachine_edgeEquivalenceDifferentSourceCount` — capdag.test.js:3026
- `testMachine_edgeEquivalenceDifferentTargets` — capdag.test.js:2978
- `testMachine_edgeEquivalenceSameUrns` — capdag.test.js:2946
- `testMachine_edgeEquivalenceSourceOrderIndependent` — capdag.test.js:3010
- `testMachine_emptyInput` — capdag.test.js:2662
- `testMachine_errorLocation_duplicateAlias` — capdag.test.js:3550
- `testMachine_errorLocation_parseError` — capdag.test.js:3540
- `testMachine_errorLocation_undefinedAlias` — capdag.test.js:3564
- `testMachine_fanInSecondaryAssignedByPriorWiring` — capdag.test.js:2734
- `testMachine_fanInSecondaryUnassignedGetsWildcard` — capdag.test.js:2747
- `testMachine_fanOut` — capdag.test.js:2717
- `testMachine_graphEmpty` — capdag.test.js:3099
- `testMachine_graphEmptyEquivalence` — capdag.test.js:3105
- `testMachine_graphEquivalenceReorderedEdges` — capdag.test.js:3057
- `testMachine_graphEquivalenceSameEdges` — capdag.test.js:3042
- `testMachine_graphNotEquivalentDifferentCap` — capdag.test.js:3086
- `testMachine_graphNotEquivalentDifferentEdgeCount` — capdag.test.js:3072
- `testMachine_headerOnlyNoWirings` — capdag.test.js:2670
- `testMachine_leafTargetsLinearChain` — capdag.test.js:3125
- `testMachine_lineBasedAndBracketedParseSameGraph` — capdag.test.js:2920
- `testMachine_lineBasedEquivalentToBracketed` — capdag.test.js:2887
- `testMachine_lineBasedFanIn` — capdag.test.js:2866
- `testMachine_lineBasedFormatSerialization` — capdag.test.js:2899
- `testMachine_lineBasedLoop` — capdag.test.js:2857
- `testMachine_lineBasedSimpleChain` — capdag.test.js:2834
- `testMachine_lineBasedTwoStepChain` — capdag.test.js:2847
- `testMachine_loopEdge` — capdag.test.js:2758
- `testMachine_malformedInputFails` — capdag.test.js:2818
- `testMachine_mediaRegistryEntry_construction` — capdag.test.js:3667
- `testMachine_mediaUrnIsComparable` — capdag.test.js:3447
- `testMachine_mediaUrnIsEquivalent` — capdag.test.js:3439
- `testMachine_mixedBracketedAndLineBased` — capdag.test.js:2879
- `testMachine_multilineFormat` — capdag.test.js:2796
- `testMachine_multilineSerializeFormat` — capdag.test.js:3291
- `testMachine_nodeAliasCollision` — capdag.test.js:2774
- `testMachine_parseMachineWithAST_aliasMap` — capdag.test.js:3510
- `testMachine_parseMachineWithAST_fanInSourceLocations` — capdag.test.js:3499
- `testMachine_parseMachineWithAST_headerLocation` — capdag.test.js:3460
- `testMachine_parseMachineWithAST_multilinePositions` — capdag.test.js:3490
- `testMachine_parseMachineWithAST_nodeMedia` — capdag.test.js:3528
- `testMachine_parseMachineWithAST_wiringLocation` — capdag.test.js:3476
- `testMachine_reorderedEdgesProduceSameNotation` — capdag.test.js:3275
- `testMachine_rootSourcesFanIn` — capdag.test.js:3139
- `testMachine_rootSourcesLinearChain` — capdag.test.js:3111
- `testMachine_roundtripFanOut` — capdag.test.js:3234
- `testMachine_roundtripLoopEdge` — capdag.test.js:3249
- `testMachine_roundtripSingleEdge` — capdag.test.js:3207
- `testMachine_roundtripTwoEdgeChain` — capdag.test.js:3220
- `testMachine_serializationIsDeterministic` — capdag.test.js:3262
- `testMachine_serializeEmptyGraph` — capdag.test.js:3203
- `testMachine_serializeSingleEdge` — capdag.test.js:3175
- `testMachine_serializeTwoEdgeChain` — capdag.test.js:3190
- `testMachine_simpleLinearChain` — capdag.test.js:2688
- `testMachine_toMermaid_emptyGraph` — capdag.test.js:3607
- `testMachine_toMermaid_fanIn` — capdag.test.js:3613
- `testMachine_toMermaid_fanOut` — capdag.test.js:3624
- `testMachine_toMermaid_linearChain` — capdag.test.js:3578
- `testMachine_toMermaid_loopEdge` — capdag.test.js:3596
- `testMachine_twoStepChain` — capdag.test.js:2703
- `testMachine_undefinedAliasFails` — capdag.test.js:2767
- `testMachine_unterminatedBracketFails` — capdag.test.js:2825
- `testMachine_whitespaceOnly` — capdag.test.js:2666
- `testRenderer_buildBrowseGraphData_rejectsMissingMediaTitles` — capdag.test.js:3882
- `testRenderer_buildEditorGraphData_capWithoutCompleteArgsIsDropped` — capdag.test.js:5010
- `testRenderer_buildEditorGraphData_cardinalityFromDataSlotSequenceFlags` — capdag.test.js:4991
- `testRenderer_buildEditorGraphData_collapsesCapsIntoLabeledEdges` — capdag.test.js:4935
- `testRenderer_buildEditorGraphData_loopMarkedEdgeGetsLoopClass` — capdag.test.js:4973
- `testRenderer_buildEditorGraphData_rejectsEdgeWithMissingSource` — capdag.test.js:5027
- `testRenderer_buildResolvedMachineGraphData_duplicateNodeIdAcrossStrandsFailsHard` — capdag.test.js:5237
- `testRenderer_buildResolvedMachineGraphData_fanInProducesEdgePerAssignment` — capdag.test.js:5135
- `testRenderer_buildResolvedMachineGraphData_loopEdgeGetsLoopClass` — capdag.test.js:5101
- `testRenderer_buildResolvedMachineGraphData_multiStrandKeepsStrandsDisjoint` — capdag.test.js:5175
- `testRenderer_buildResolvedMachineGraphData_singleStrandLinearChain` — capdag.test.js:5043
- `testRenderer_buildRunGraphData_allFailedDropsTargetPlaceholder` — capdag.test.js:4740
- `testRenderer_buildRunGraphData_backboneHasNoForeachNode` — capdag.test.js:4686
- `testRenderer_buildRunGraphData_closedForeachSuccessMergesAtCollectTarget` — capdag.test.js:4866
- `testRenderer_buildRunGraphData_failureWithoutFailedCapRendersFullTrace` — capdag.test.js:4589
- `testRenderer_buildRunGraphData_pagesSuccessesAndFailures` — capdag.test.js:4519
- `testRenderer_buildRunGraphData_unclosedForeachSuccessNoMerge` — capdag.test.js:4805
- `testRenderer_buildRunGraphData_usesCapUrnIsEquivalentForFailedCap` — capdag.test.js:4627
- `testRenderer_buildStrandGraphData_foreachCollectSpan` — capdag.test.js:4076
- `testRenderer_buildStrandGraphData_nestedForEachThrows` — capdag.test.js:4191
- `testRenderer_buildStrandGraphData_sequenceShowsCardinality` — capdag.test.js:4056
- `testRenderer_buildStrandGraphData_singleCapPlain` — capdag.test.js:4029
- `testRenderer_buildStrandGraphData_standaloneCollect` — capdag.test.js:4127
- `testRenderer_buildStrandGraphData_unclosedForEachBody` — capdag.test.js:4154
- `testRenderer_canonicalMediaUrn_normalizesTagOrder` — capdag.test.js:3842
- `testRenderer_canonicalMediaUrn_preservesValueTags` — capdag.test.js:3851
- `testRenderer_canonicalMediaUrn_rejectsCapUrn` — capdag.test.js:3856
- `testRenderer_cardinalityFromCap_findsStdinArgNotFirstArg` — capdag.test.js:3767
- `testRenderer_cardinalityFromCap_outputOnlySequence` — capdag.test.js:3799
- `testRenderer_cardinalityFromCap_rejectsStringIsSequence` — capdag.test.js:3810
- `testRenderer_cardinalityFromCap_scalarDefaultsWhenFieldsMissing` — capdag.test.js:3791
- `testRenderer_cardinalityFromCap_throwsOnNonObject` — capdag.test.js:3823
- `testRenderer_cardinalityLabel_allFourCases` — capdag.test.js:3752
- `testRenderer_cardinalityLabel_usesUnicodeArrow` — capdag.test.js:3759
- `testRenderer_classifyStrandCapSteps_capFlags` — capdag.test.js:3978
- `testRenderer_classifyStrandCapSteps_nestedForks` — capdag.test.js:3999
- `testRenderer_collapseStrand_plainCapDistinctTargetNoMerge` — capdag.test.js:4470
- `testRenderer_collapseStrand_plainCapMergesTrailingOutput` — capdag.test.js:4434
- `testRenderer_collapseStrand_sequenceProducingCapBeforeForeach` — capdag.test.js:4370
- `testRenderer_collapseStrand_singleCapBodyKeepsCapOwnLabel` — capdag.test.js:4219
- `testRenderer_collapseStrand_standaloneCollectCollapses` — capdag.test.js:4327
- `testRenderer_collapseStrand_unclosedForEachBodyCollapses` — capdag.test.js:4271
- `testRenderer_mediaNodeLabel_rejectsUrnDerivedLabels` — capdag.test.js:3868
- `testRenderer_validateBodyOutcome_rejectsNegativeIndex` — capdag.test.js:4509
- `testRenderer_validateEditorGraphPayload_rejectsUnknownKind` — capdag.test.js:4921
- `testRenderer_validateResolvedMachinePayload_rejectsMissingFields` — capdag.test.js:5272
- `testRenderer_validateStrandPayload_missingSourceSpec` — capdag.test.js:4496
- `testRenderer_validateStrandStep_rejectsUnknownVariant` — capdag.test.js:3939
- `testRenderer_validateStrandStep_requiresBooleanIsSequence` — capdag.test.js:3956
- `testUrn` — capdag.test.js:107
- `testisCollection` — capdag.test.js:2324

---

*Generated from JS source tree*
*Total tests: 323*
*Total numbered tests: 173*
*Total unnumbered tests: 150*
*Total numbered tests missing descriptions: 0*
*Total numbering mismatches: 0*

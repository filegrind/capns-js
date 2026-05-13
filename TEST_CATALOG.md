# JS Test Catalog

**Total Tests:** 328

**Numbered Tests:** 178

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
| test017 | `test017_tagMatching` | TEST017: Test tag matching: exact match, subset match, wildcard match, value mismatch | capdag.test.js:318 |
| test018 | `test018_matchingCaseSensitiveValues` | TEST018: Test that quoted values with different case do NOT match (case-sensitive) | capdag.test.js:342 |
| test019 | `test019_missingTagHandling` | TEST019: Missing tag in instance causes rejection — pattern's tags are constraints | capdag.test.js:349 |
| test020 | `test020_specificity` | TEST020: Specificity is the sum of per-tag truth-table scores across in/out/y. Marker tags (bare segments and `key=*`) score 2 (must-have-any), exact `key=value` tags score 3, missing/`?` score 0, `!` scores 1. testUrn() builds "cap:in=media:void;out=media:record;<tags>" so the directional baseline is: in:  media:void   -> {void=*}    -> 2 out: media:record -> {record=*}  -> 2 Total directional baseline: 4. | capdag.test.js:371 |
| test021 | `test021_builder` | TEST021: Test builder creates cap URN with marker + keyed tags and direction specs. `op` is no longer a special key — operation names are markers (value-less tags). | capdag.test.js:400 |
| test022 | `test022_builderRequiresDirection` | TEST022: Test builder requires both in_spec and out_spec | capdag.test.js:414 |
| test023 | `test023_builderPreservesCase` | TEST023: Test builder lowercases keys but preserves value case | capdag.test.js:428 |
| test024 | `test024_compatibility` | TEST024: Directional accepts — pattern's tags are constraints, instance must satisfy | capdag.test.js:439 |
| test025 | `test025_bestMatch` | TEST025: Test find_best_match returns most specific matching cap | capdag.test.js:459 |
| test026 | `test026_mergeAndSubset` | TEST026: Test merge combines tags from both caps, subset keeps only specified tags | capdag.test.js:472 |
| test027 | `test027_wildcardTag` | TEST027: Test with_wildcard_tag sets tag to wildcard, including in/out | capdag.test.js:491 |
| test028 | `test028_emptyCapUrnNotAllowed` | TEST028: Test empty cap URN defaults to media: wildcard | capdag.test.js:504 |
| test029 | `test029_minimalCapUrn` | TEST029: Test minimal valid cap URN has just in and out, empty tags | capdag.test.js:511 |
| test030 | `test030_extendedCharacterSupport` | TEST030: Test extended characters (forward slashes, colons) in tag values | capdag.test.js:519 |
| test031 | `test031_wildcardRestrictions` | TEST031: Test wildcard rejected in keys but accepted in values | capdag.test.js:526 |
| test032 | `test032_duplicateKeyRejection` | TEST032: Test duplicate keys are rejected with DuplicateKey error | capdag.test.js:544 |
| test033 | `test033_numericKeyRestriction` | TEST033: Test pure numeric keys rejected, mixed alphanumeric allowed, numeric values allowed | capdag.test.js:553 |
| test034 | `test034_emptyValueError` | TEST034: Test empty values are rejected | capdag.test.js:567 |
| test035 | `test035_hasTagCaseSensitive` | TEST035: Test has_tag is case-sensitive for values, case-insensitive for keys, works for in/out | capdag.test.js:580 |
| test036 | `test036_withTagPreservesValue` | TEST036: Test with_tag preserves value case | capdag.test.js:592 |
| test037 | `test037_withTagRejectsEmptyValue` | TEST037: Test with_tag rejects empty value | capdag.test.js:599 |
| test038 | `test038_semanticEquivalence` | TEST038: Test semantic equivalence of unquoted and quoted simple lowercase values | capdag.test.js:609 |
| test039 | `test039_getTagReturnsDirectionSpecs` | TEST039: Test get_tag returns direction specs (in/out) with case-insensitive lookup | capdag.test.js:617 |
| test040 | `test040_matchingSemanticsExactMatch` | TEST040: Matching semantics - exact match succeeds | capdag.test.js:626 |
| test041 | `test041_matchingSemanticsCapMissingTag` | TEST041: Matching semantics - cap missing tag matches (implicit wildcard) | capdag.test.js:633 |
| test042 | `test042_matchingSemanticsCapHasExtraTag` | TEST042: Pattern rejects instance missing required tags | capdag.test.js:641 |
| test043 | `test043_matchingSemanticsRequestHasWildcard` | TEST043: Matching semantics - request wildcard matches specific cap value | capdag.test.js:649 |
| test044 | `test044_matchingSemanticsCapHasWildcard` | TEST044: Matching semantics - cap wildcard matches specific request value | capdag.test.js:656 |
| test045 | `test045_matchingSemanticsValueMismatch` | TEST045: Matching semantics - value mismatch does not match | capdag.test.js:663 |
| test046 | `test046_matchingSemanticsFallbackPattern` | TEST046: Matching semantics - fallback pattern (cap missing tag = implicit wildcard) | capdag.test.js:670 |
| test047 | `test047_matchingSemanticsThumbnailVoidInput` | TEST047: Matching semantics - thumbnail fallback with void input | capdag.test.js:678 |
| test048 | `test048_matchingSemanticsWildcardDirection` | TEST048: Matching semantics - wildcard direction matches anything | capdag.test.js:685 |
| test049 | `test049_matchingSemanticsCrossDimension` | TEST049: Non-overlapping tags — neither direction accepts | capdag.test.js:692 |
| test050 | `test050_matchingSemanticsDirectionMismatch` | TEST050: Matching semantics - direction mismatch prevents matching | capdag.test.js:700 |
| test054 | `test054_xv5InlineSpecRedefinitionDetected` | TEST054: XV5 - Test inline media spec redefinition of existing registry spec is detected and rejected | capdag.test.js:804 |
| test055 | `test055_xv5NewInlineSpecAllowed` | TEST055: XV5 - Test new inline media spec (not in registry) is allowed | capdag.test.js:821 |
| test056 | `test056_xv5EmptyMediaSpecsAllowed` | TEST056: XV5 - Test empty media_specs (no inline specs) passes XV5 validation | capdag.test.js:836 |
| test060 | `test060_wrongPrefixFails` | TEST060: Test wrong prefix fails with InvalidPrefix error showing expected and actual prefix | capdag.test.js:848 |
| test061 | `test061_isBinary` | TEST061: Test is_binary returns true when textable tag is absent (binary = not textable) | capdag.test.js:857 |
| test062 | `test062_isRecord` | TEST062: Test is_record returns true when record marker tag is present indicating key-value structure | capdag.test.js:873 |
| test063 | `test063_isScalar` | TEST063: Test is_scalar returns true when list marker tag is absent (scalar is default) | capdag.test.js:884 |
| test064 | `test064_isList` | TEST064: Test is_list returns true when list marker tag is present indicating ordered collection | capdag.test.js:897 |
| test065 | `test065_isOpaque` | TEST065: Test is_opaque returns true when record marker is absent (opaque is default) | capdag.test.js:906 |
| test066 | `test066_isJson` | TEST066: Test is_json returns true only when json marker tag is present for JSON representation | capdag.test.js:917 |
| test067 | `test067_isText` | TEST067: Test is_text returns true only when textable marker tag is present | capdag.test.js:923 |
| test068 | `test068_isVoid` | TEST068: Test is_void returns true when void flag or type=void tag is present | capdag.test.js:934 |
| test071 | `test071_toStringRoundtrip` | TEST071: Test to_string roundtrip ensures serialization and deserialization preserve URN structure | capdag.test.js:942 |
| test072 | `test072_constantsParse` | TEST072: Test all media URN constants parse successfully as valid media URNs | capdag.test.js:952 |
| test074 | `test074_mediaUrnMatching` | TEST074: Test media URN conforms_to using tagged URN semantics with specific and generic requirements | capdag.test.js:972 |
| test075 | `test075_accepts` | TEST075: Test accepts with implicit wildcards where handlers with fewer tags can handle more requests | capdag.test.js:986 |
| test076 | `test076_specificity` | TEST076: Test specificity increases with more tags for ranking conformance | capdag.test.js:997 |
| test077 | `test077_serdeRoundtrip` | TEST077: Test serde roundtrip serializes to JSON string and deserializes back correctly | capdag.test.js:1006 |
| test078 | `test078_debugMatchingBehavior` | TEST078: conforms_to behavior between MEDIA_OBJECT and MEDIA_STRING | capdag.test.js:1015 |
| test091 | `test091_resolveCustomMediaSpec` | TEST091: Test resolving custom media URN from local media_specs takes precedence over registry | capdag.test.js:1030 |
| test092 | `test092_resolveCustomWithSchema` | TEST092: Test resolving custom record media spec with schema from local media_specs | capdag.test.js:1040 |
| test093 | `test093_resolveUnresolvableFailsHard` | TEST093: Test resolving unknown media URN fails with UnresolvableMediaUrn error | capdag.test.js:1057 |
| test099 | `test099_resolvedIsBinary` | TEST099: Test ResolvedMediaSpec is_binary returns true when textable tag is absent | capdag.test.js:1076 |
| test100 | `test100_resolvedIsRecord` | TEST100: Test ResolvedMediaSpec is_record returns true when record marker is present | capdag.test.js:1082 |
| test101 | `test101_resolvedIsScalar` | TEST101: Test ResolvedMediaSpec is_scalar returns true when list marker is absent | capdag.test.js:1088 |
| test102 | `test102_resolvedIsList` | TEST102: Test ResolvedMediaSpec is_list returns true when list marker is present | capdag.test.js:1094 |
| test103 | `test103_resolvedIsJson` | TEST103: Test ResolvedMediaSpec is_json returns true when json tag is present | capdag.test.js:1100 |
| test104 | `test104_resolvedIsText` | TEST104: Test ResolvedMediaSpec is_text returns true when textable tag is present | capdag.test.js:1106 |
| test105 | `test105_metadataPropagation` | TEST105: Test metadata propagates from media spec def to resolved media spec | capdag.test.js:1112 |
| test106 | `test106_metadataWithValidation` | TEST106: Test metadata and validation can coexist in media spec definition | capdag.test.js:1135 |
| test107 | `test107_extensionsPropagation` | TEST107: Test extensions field propagates from media spec def to resolved | capdag.test.js:1154 |
| test108 | `test108_extensionsSerialization` | TEST108: Test creating new cap with URN, title, and command verifies correct initialization | capdag.test.js:1170 |
| test109 | `test109_extensionsWithMetadataAndValidation` | TEST109: Test creating cap with metadata initializes and retrieves metadata correctly | capdag.test.js:1178 |
| test110 | `test110_multipleExtensions` | TEST110: Test cap matching with subset semantics for request fulfillment | capdag.test.js:1197 |
| test115 | `test115_capArgSerialization` | TEST115: Test CapArg serialization and deserialization with multiple sources | capdag.test.js:1213 |
| test116 | `test116_capArgConstructors` | TEST116: Test CapArg constructor methods basic and with_description create args correctly | capdag.test.js:1246 |
| test150 | `test150_capManifestJsonSerialization` | TEST150: JSON roundtrip | capdag.test.js:1274 |
| test156 | `test156_stdinSourceFromData` | TEST156: Test creating StdinSource Data variant with byte vector | capdag.test.js:1430 |
| test157 | `test157_stdinSourceFromFileReference` | TEST157: Test creating StdinSource FileReference variant with all required fields | capdag.test.js:1441 |
| test158 | `test158_stdinSourceWithEmptyData` | TEST158: Test StdinSource Data with empty vector stores and retrieves correctly | capdag.test.js:1458 |
| test159 | `test159_stdinSourceWithBinaryContent` | TEST159: Test StdinSource Data with binary content like PNG header bytes | capdag.test.js:1466 |
| test274 | `test274_capArgumentValueNew` | TEST274: Test CapArgumentValue::new stores media_urn and raw byte value | capdag.test.js:1480 |
| test275 | `test275_capArgumentValueFromStr` | TEST275: Test CapArgumentValue::from_str converts string to UTF-8 bytes | capdag.test.js:1487 |
| test276 | `test276_capArgumentValueAsStrValid` | TEST276: Test CapArgumentValue::value_as_str succeeds for UTF-8 data | capdag.test.js:1494 |
| test277 | `test277_capArgumentValueAsStrInvalidUtf8` | TEST277: Test CapArgumentValue::value_as_str fails for non-UTF-8 binary data | capdag.test.js:1500 |
| test278 | `test278_capArgumentValueEmpty` | TEST278: Test CapArgumentValue::new with empty value stores empty vec | capdag.test.js:1512 |
| test282 | `test282_capArgumentValueUnicode` | TEST282: Test CapArgumentValue::from_str with Unicode string preserves all characters | capdag.test.js:1521 |
| test283 | `test283_capArgumentValueLargeBinary` | TEST283: Test CapArgumentValue with large binary payload preserves all bytes | capdag.test.js:1527 |
| test304 | `test304_mediaAvailabilityOutputConstant` | TEST304: Test MEDIA_AVAILABILITY_OUTPUT constant parses as valid media URN with correct tags | capdag.test.js:1546 |
| test305 | `test305_mediaPathOutputConstant` | TEST305: Test MEDIA_PATH_OUTPUT constant parses as valid media URN with correct tags | capdag.test.js:1556 |
| test306 | `test306_availabilityAndPathOutputDistinct` | TEST306: Test MEDIA_AVAILABILITY_OUTPUT and MEDIA_PATH_OUTPUT are distinct URNs | capdag.test.js:1566 |
| test307 | `test307_modelAvailabilityUrn` | TEST307: Test model_availability_urn builds valid cap URN with correct op and media specs | capdag.test.js:1580 |
| test308 | `test308_modelPathUrn` | TEST308: Test model_path_urn builds valid cap URN with correct op and media specs | capdag.test.js:1592 |
| test309 | `test309_modelAvailabilityAndPathAreDistinct` | TEST309: Test model_availability_urn and model_path_urn produce distinct URNs | capdag.test.js:1604 |
| test310 | `test310_llmGenerateTextUrn` | TEST310: llm_generate_text_urn() produces a valid cap URN with textable in/out specs | capdag.test.js:1611 |
| test312 | `test312_allUrnBuildersProduceValidUrns` | TEST312: Test all URN builders produce parseable cap URNs | capdag.test.js:1634 |
| test320 | `test320_cartridgeInfoConstruction` | TEST320-335: CartridgeRepoServer and CartridgeRepoClient tests | capdag.test.js:1991 |
| test321 | `test321_cartridgeInfoIsSigned` | TEST321: CartridgeInfo.is_signed() returns true when signature is present | capdag.test.js:2025 |
| test322 | `test322_cartridgeInfoBuildForPlatform` | TEST322: CartridgeInfo.build_for_platform() returns the build matching the current platform | capdag.test.js:2037 |
| test323 | `test323_cartridgeRepoServerValidateRegistry` | TEST323: CartridgeRepoServer requires schema 5.0 and rejects older. | capdag.test.js:2071 |
| test324 | `test324_cartridgeRepoServerTransformToArray` | TEST324: CartridgeRepoServer walks both channels and emits a flat CartridgeInfo array preserving channel provenance. Release entries appear first. | capdag.test.js:2110 |
| test325 | `test325_cartridgeRepoServerGetCartridges` | TEST325: CartridgeRepoServer.getCartridges() wraps the transformed flat array (across both channels) in the response envelope. | capdag.test.js:2148 |
| test326 | `test326_cartridgeRepoServerGetCartridgeById` | TEST326: CartridgeRepoServer.getCartridgeById() requires (channel, id). Same id looked up in the wrong channel must miss — channels are independent namespaces. | capdag.test.js:2162 |
| test327 | `test327_cartridgeRepoServerSearchCartridges` | TEST327: CartridgeRepoServer.searchCartridges() filters across both channels by name/description/tags/cap titles. Cap URN strings are not substring-matched. | capdag.test.js:2194 |
| test328 | `test328_cartridgeRepoServerGetByCategory` | TEST328: CartridgeRepoServer.getCartridgesByCategory() filters cartridges by category across both channels. | capdag.test.js:2216 |
| test329 | `test329_cartridgeRepoServerGetByCap` | TEST329: CartridgeRepoServer.getCartridgesByCap() parses the input URN and matches each declared cap via `conformsTo`. Tag-order differences resolve because matching is order-theoretic, not string. | capdag.test.js:2235 |
| test330 | `test330_cartridgeRepoClientUpdateCache` | TEST330: CartridgeRepoClient updates its local cache keyed by "<channel>:<id>". The cache holds release and nightly entries independently — the same id is allowed in both. | capdag.test.js:2252 |
| test331 | `test331_cartridgeRepoClientGetSuggestions` | TEST331: CartridgeRepoClient.getSuggestionsForCap() returns cartridge suggestions with channel propagated onto each suggestion. | capdag.test.js:2280 |
| test332 | `test332_cartridgeRepoClientGetCartridge` | TEST332: CartridgeRepoClient.getCartridge() requires (channel, id). Same id in the wrong channel must miss. | capdag.test.js:2310 |
| test333 | `test333_cartridgeRepoClientGetAllCaps` | TEST333: CartridgeRepoClient.getAllAvailableCaps() returns the set of normalized URNs across both channels. | capdag.test.js:2355 |
| test334 | `test334_cartridgeRepoClientNeedsSync` | TEST334: CartridgeRepoClient.needsSync() returns true when cache is empty / stale, false right after a fresh update. | capdag.test.js:2372 |
| test335 | `test335_cartridgeRepoServerClientIntegration` | TEST335: Round-trip: server produces a v5.0 response, client consumes it, channel provenance is preserved end-to-end. | capdag.test.js:2391 |
| test597 | `test597_capArgWithFullDefinition` | TEST597: CapArg::with_full_definition stores all fields including optional ones | capdag.test.js:1330 |
| test639 | `test639_emptyCapDefaultsToMediaWildcard` | TEST639: cap: (empty) defaults to in=media:;out=media: | capdag.test.js:2701 |
| test640 | `test640_inOnlyDefaultsOutToMedia` | TEST640: cap:in defaults out to media: | capdag.test.js:2709 |
| test641 | `test641_outOnlyDefaultsInToMedia` | TEST641: cap:out defaults in to media: | capdag.test.js:2716 |
| test642 | `test642_inOutWithoutValuesBecomeMedia` | TEST642: cap:in;out both become media: | capdag.test.js:2723 |
| test643 | `test643_explicitAsteriskIsWildcard` | TEST643: cap:in=*;out=* becomes media: | capdag.test.js:2730 |
| test644 | `test644_specificInWildcardOut` | TEST644: cap:in=media:;out=* has specific in, wildcard out | capdag.test.js:2737 |
| test645 | `test645_wildcardInSpecificOut` | TEST645: cap:in=*;out=media:text has wildcard in, specific out | capdag.test.js:2744 |
| test646 | `test646_invalidInSpecFails` | TEST646: cap:in=foo fails (invalid media URN) | capdag.test.js:2751 |
| test647 | `test647_invalidOutSpecFails` | TEST647: cap:in=media:;out=bar fails (invalid media URN) | capdag.test.js:2760 |
| test648 | `test648_wildcardAcceptsSpecific` | TEST648: Wildcard in/out match specific caps | capdag.test.js:2769 |
| test649 | `test649_specificityScoring` | TEST649: Specificity - wildcard has 0, specific has tag count | capdag.test.js:2778 |
| test651 | `test651_identityFormsEquivalent` | TEST651: All identity forms produce the same CapUrn | capdag.test.js:2789 |
| test653 | `test653_identityRoutingIsolation` | TEST653: Identity (no tags) does not match specific requests via routing | capdag.test.js:2809 |
| test890 | `test890_directionSemanticMatching` | TEST890: Semantic direction matching - generic provider matches specific request | capdag.test.js:711 |
| test891 | `test891_directionSemanticSpecificity` | TEST891: Semantic direction specificity — more constraints in either axis means a higher score under the truth-table-driven sum. media: (top, no tags) scores 0; each marker tag scores 2; each exact tag scores 3. | capdag.test.js:764 |
| test939 | `test939_capUrnCanonicalFormDropsWildcardInOut` | TEST939: The canonical form drops `in=media:` and `out=media:` segments. Every spelling of "the same cap with wildcard in/out" collapses to one byte-identical canonical string. This is the contract that makes registry lookups work: the cap-publisher hashes `<canonical-urn>` to compute the cache key, and every language port (Rust, Go, Python, JS, ObjC) must agree on the canonical form for cross-language lookups to land on the same key. A regression that emitted the wildcard segments would silently move the published cap to a different SHA-256 bucket, 404'ing every reader that hashes the canonical form. | capdag.test.js:296 |
| test1294 | `test1294_rule11VoidInputWithStdinRejected` | TEST1294: RULE11 - void-input cap with stdin source rejected | capdag.test.js:2645 |
| test1295 | `test1295_rule11NonVoidInputWithoutStdinRejected` | TEST1295: RULE11 - non-void-input cap without stdin source rejected | capdag.test.js:2660 |
| test1296 | `test1296_rule11VoidInputCliFlagOnly` | TEST1296: RULE11 - void-input cap with only cli_flag sources passes | capdag.test.js:2675 |
| test1297 | `test1297_rule11NonVoidInputWithStdin` | TEST1297: RULE11 - non-void-input cap with stdin source passes | capdag.test.js:2685 |
| test1298 | `test1298_isBool` | TEST1298: is_bool returns true only when bool marker tag is present | capdag.test.js:2473 |
| test1299 | `test1299_isFilePath` | TEST1299: isFilePath returns true for the single file-path media URN, false for everything else. There is no "array" variant — cardinality is carried by is_sequence on the wire, not by URN tags. | capdag.test.js:2487 |
| test1302 | `test1302_predicateConstantConsistency` | TEST1302: predicates are consistent with constants — every constant triggers exactly the expected predicates | capdag.test.js:2506 |
| test1303 | `test1303_withoutTag` | TEST1303: without_tag removes tag, ignores in/out, case-insensitive for keys | capdag.test.js:2546 |
| test1304 | `test1304_withInOutSpec` | TEST1304: with_in_spec and with_out_spec change direction specs | capdag.test.js:2568 |
| test1305 | `test1305_findAllMatches` | TEST1305: CapMatcher::find_all_matches returns all matching caps sorted by specificity | capdag.test.js:2591 |
| test1306 | `test1306_areCompatible` | TEST1306: CapMatcher::are_compatible detects bidirectional overlap | capdag.test.js:2609 |
| test1307 | `test1307_withTagIgnoresInOut` | TEST1307: with_tag silently ignores in/out keys | capdag.test.js:2634 |
| test1312 | `test1312_isImage` | TEST1312: is_image returns true only when image marker tag is present | capdag.test.js:2428 |
| test1313 | `test1313_isAudio` | TEST1313: is_audio returns true only when audio marker tag is present | capdag.test.js:2440 |
| test1314 | `test1314_isVideo` | TEST1314: is_video returns true only when video marker tag is present | capdag.test.js:2451 |
| test1315 | `test1315_isNumeric` | TEST1315: is_numeric returns true only when numeric marker tag is present | capdag.test.js:2461 |
| test1800 | `test1800_kindIdentityOnlyForBareCap` | TEST1800: Identity classifier — only the bare cap: form qualifies. Adding any tag (even one that doesn't constrain in/out) demotes the cap to Transform because the operation/metadata axis is no longer fully generic. | capdag.test.js:5488 |
| test1801 | `test1801_kindSourceWhenInputIsVoid` | TEST1801: Source classifier — in=media:void, out non-void. | capdag.test.js:5509 |
| test1802 | `test1802_kindSinkWhenOutputIsVoid` | TEST1802: Sink classifier — out=media:void, in non-void. | capdag.test.js:5518 |
| test1803 | `test1803_kindEffectWhenBothSidesVoid` | TEST1803: Effect classifier — both sides void. Reads as `() → ()`. | capdag.test.js:5527 |
| test1804 | `test1804_kindTransformForNormalDataProcessors` | TEST1804: Transform classifier — at least one side non-void, and the cap is not the bare identity. | capdag.test.js:5538 |
| test1805 | `test1805_kindInvariantUnderCanonicalSpellings` | TEST1805: Kind is invariant under canonicalization. The same morphism written in many surface forms must classify the same way once parsed. | capdag.test.js:5588 |
| test1810 | `test1810_mediaVoidIsAtomic` | TEST1810: media:void is atomic — refinements are parse errors. Mirrored across every language port (Rust, Go, Python, Swift/ObjC, JS) under the SAME number. Any divergence is a wire-level inconsistency — the unit type's atomicity is part of the protocol's deepest layer, not a per-port detail. | capdag.test.js:5553 |
| test1820 | `test1820_specificityQuestionIsZero` | TEST1820: A `?`-valued cap-tag scores 0. Same as missing. | capdag.test.js:5629 |
| test1821 | `test1821_specificityMustNotHaveIsFive` | TEST1821: A `!`-valued cap-tag scores 5 (top of negative chain). | capdag.test.js:5639 |
| test1822 | `test1822_specificityMustHaveAnyIsTwo` | TEST1822: A `*`-valued cap-tag (including bare markers) scores 2. | capdag.test.js:5646 |
| test1823 | `test1823_specificityExactValueIsFour` | TEST1823: An exact-valued cap-tag scores 4. | capdag.test.js:5660 |
| test1824 | `test1824_specificityCombinedYAxis` | TEST1824: All six forms compose additively on a single cap. y combining 0+1+2+3+4+5 must sum to 15. | capdag.test.js:5668 |
| test1830 | `test1830_canonicalizeNoConstraint` | TEST1830: ?x ≡ x? ≡ x=? all canonicalize to ?x. | capdag.test.js:5679 |
| test1831 | `test1831_canonicalizeAbsentOrNotValue` | TEST1831: ?x=v and x?=v both canonicalize to x?=v. The third hypothetical form `x=?v` is NOT recognized as a qualifier — a value starting with `?` is just an exact value beginning with a `?` character. | capdag.test.js:5692 |
| test1832 | `test1832_canonicalizeMustHaveAny` | TEST1832: x ≡ x=* both canonicalize to bare x. | capdag.test.js:5708 |
| test1833 | `test1833_canonicalizePresentNotValue` | TEST1833: !x=v and x!=v both canonicalize to x!=v. The third hypothetical form `x=!v` is NOT recognized as a qualifier — a value starting with `!` is just an exact value beginning with a `!` character. | capdag.test.js:5721 |
| test1834 | `test1834_canonicalizeExactValue` | TEST1834: x=v stays as x=v. | capdag.test.js:5737 |
| test1835 | `test1835_canonicalizeMustNotHave` | TEST1835: !x ≡ x! ≡ x=! all canonicalize to !x. | capdag.test.js:5743 |
| test1842 | `test1842_truthTableFullCrossProduct` | TEST1842: Full 6×6 truth table. | capdag.test.js:5753 |
| test1843 | `test1843_rejectInvalidCombinations` | TEST1843: Invalid qualifier combinations must be rejected. | capdag.test.js:5781 |
| test1844 | `test1844_axisWeightingOutDominates` | TEST1844: out-axis difference dominates combined in+y differences. | capdag.test.js:5796 |
| test1845 | `test1845_axisWeightingInDominatesY` | TEST1845: With equal out, in-axis dominates over y-axis. | capdag.test.js:5806 |
| test1846 | `test1846_axisWeightingDecodedLayout` | TEST1846: Decoded layout — 10000*out + 100*in + y. | capdag.test.js:5816 |
| | | | |
| unnumbered | `testCapFabAddCapPopulatesEdgesAndNodes` | Add a cap and check it becomes an edge with from/to nodes and carries the registry name we passed. This is exactly the shape the renderer depends on. | capdag.test.js:1373 |
| unnumbered | `testCapFabDistinctRegistryNames` | Each edge must carry the registry name it was added with. This is how the renderer colours/groups edges by provenance in browse mode. | capdag.test.js:1412 |
| unnumbered | `testCapFabGetOutgoingConformsToMatching` | getOutgoing takes a concrete source URN and returns edges whose from_spec the source conforms to. It must NOT be a plain string lookup. | capdag.test.js:1391 |
| unnumbered | `testJS_buildExtensionIndex` | These tests cover JS-specific functionality not in the Rust numbering scheme but are important for capdag-js correctness. | capdag.test.js:1654 |
| unnumbered | `testJS_capDocumentationOmittedWhenNull` | When documentation is null, toJSON must omit the field entirely. This matches the Rust serializer's skip-when-None semantics and the ObjC toDictionary behaviour. A regression where null is emitted as `documentation: null` would break the symmetric round-trip with Rust (which has no null sentinel) and pollute generated JSON. | capdag.test.js:1765 |
| unnumbered | `testJS_capDocumentationRoundTrip` | JS round-trip for the documentation field on Cap. Mirrors TEST920 in capdag/src/cap/definition.rs — the body is non-trivial (newlines, backticks, embedded quotes, Unicode) so escaping mismatches between JSON.stringify on this side and the Rust serializer on the other side surface as failures here. | capdag.test.js:1743 |
| unnumbered | `testJS_capJSONSerialization` |  | capdag.test.js:1720 |
| unnumbered | `testJS_getExtensionMappings` |  | capdag.test.js:1698 |
| unnumbered | `testJS_mediaSpecConstruction` |  | capdag.test.js:1831 |
| unnumbered | `testJS_mediaSpecDocumentationPropagatesThroughResolve` | Documentation propagates from a mediaSpecs definition through resolveMediaUrn into the resolved MediaSpec. Mirrors TEST924 on the Rust side. This is the path every UI consumer uses, so a break here makes the new field invisible everywhere downstream. | capdag.test.js:1788 |
| unnumbered | `testJS_mediaUrnsForExtension` |  | capdag.test.js:1670 |
| unnumbered | `testJS_resolveMediaUrnFromSpecs` |  | capdag.test.js:1708 |
| unnumbered | `testJS_stdinSourceKindConstants` |  | capdag.test.js:1818 |
| unnumbered | `testJS_stdinSourceNullData` |  | capdag.test.js:1824 |
| unnumbered | `testLlmGenerateTextUrnSpecs` | Mirror-specific coverage: llm_generate_text_urn input/output specs conform to MEDIA_STRING | capdag.test.js:1623 |
| unnumbered | `testMachine_aliasFallbackWithoutOpTag` |  | capdag.test.js:3489 |
| unnumbered | `testMachine_aliasFromOpTag` | Aliases are pure-index `edge_<N>` regardless of the cap's tags; there is no privileged `op` tag to derive a friendlier name from. | capdag.test.js:3478 |
| unnumbered | `testMachine_builderChaining` |  | capdag.test.js:3547 |
| unnumbered | `testMachine_builderEquivalentToParsed` |  | capdag.test.js:3555 |
| unnumbered | `testMachine_builderRoundTrip` |  | capdag.test.js:3567 |
| unnumbered | `testMachine_builderSingleEdge` | --- Machine builder tests --- | capdag.test.js:3523 |
| unnumbered | `testMachine_builderWithLoop` |  | capdag.test.js:3535 |
| unnumbered | `testMachine_capRegistryClient_construction` |  | capdag.test.js:3851 |
| unnumbered | `testMachine_capRegistryEntry_construction` | Phase 0B: FabricRegistryClient tests | capdag.test.js:3815 |
| unnumbered | `testMachine_capRegistryEntry_defaults` |  | capdag.test.js:3858 |
| unnumbered | `testMachine_capUrnInMediaUrn` |  | capdag.test.js:3594 |
| unnumbered | `testMachine_capUrnIsComparable` |  | capdag.test.js:3587 |
| unnumbered | `testMachine_capUrnIsEquivalent` | --- CapUrn.isEquivalent/isComparable tests --- | capdag.test.js:3579 |
| unnumbered | `testMachine_capUrnOutMediaUrn` |  | capdag.test.js:3601 |
| unnumbered | `testMachine_conflictingMediaTypesFail` |  | capdag.test.js:2955 |
| unnumbered | `testMachine_differentAliasesSameGraph` |  | capdag.test.js:2977 |
| unnumbered | `testMachine_displayEdge` |  | capdag.test.js:3322 |
| unnumbered | `testMachine_displayGraph` |  | capdag.test.js:3333 |
| unnumbered | `testMachine_duplicateAlias` |  | capdag.test.js:2848 |
| unnumbered | `testMachine_duplicateOpTagsDisambiguated` | Pure-index aliases inherently disambiguate edges that share a marker tag. | capdag.test.js:3501 |
| unnumbered | `testMachine_edgeEquivalenceDifferentCapUrns` |  | capdag.test.js:3133 |
| unnumbered | `testMachine_edgeEquivalenceDifferentLoopFlag` |  | capdag.test.js:3165 |
| unnumbered | `testMachine_edgeEquivalenceDifferentSourceCount` |  | capdag.test.js:3197 |
| unnumbered | `testMachine_edgeEquivalenceDifferentTargets` |  | capdag.test.js:3149 |
| unnumbered | `testMachine_edgeEquivalenceSameUrns` | --- Machine graph tests (mirrors graph.rs tests) --- | capdag.test.js:3117 |
| unnumbered | `testMachine_edgeEquivalenceSourceOrderIndependent` |  | capdag.test.js:3181 |
| unnumbered | `testMachine_emptyInput` | --- Machine parser tests (mirrors parser.rs tests) --- | capdag.test.js:2833 |
| unnumbered | `testMachine_errorLocation_duplicateAlias` |  | capdag.test.js:3721 |
| unnumbered | `testMachine_errorLocation_parseError` |  | capdag.test.js:3711 |
| unnumbered | `testMachine_errorLocation_undefinedAlias` |  | capdag.test.js:3735 |
| unnumbered | `testMachine_fanInSecondaryAssignedByPriorWiring` |  | capdag.test.js:2905 |
| unnumbered | `testMachine_fanInSecondaryUnassignedGetsWildcard` |  | capdag.test.js:2918 |
| unnumbered | `testMachine_fanOut` |  | capdag.test.js:2888 |
| unnumbered | `testMachine_graphEmpty` |  | capdag.test.js:3270 |
| unnumbered | `testMachine_graphEmptyEquivalence` |  | capdag.test.js:3276 |
| unnumbered | `testMachine_graphEquivalenceReorderedEdges` |  | capdag.test.js:3228 |
| unnumbered | `testMachine_graphEquivalenceSameEdges` |  | capdag.test.js:3213 |
| unnumbered | `testMachine_graphNotEquivalentDifferentCap` |  | capdag.test.js:3257 |
| unnumbered | `testMachine_graphNotEquivalentDifferentEdgeCount` |  | capdag.test.js:3243 |
| unnumbered | `testMachine_headerOnlyNoWirings` |  | capdag.test.js:2841 |
| unnumbered | `testMachine_leafTargetsLinearChain` |  | capdag.test.js:3296 |
| unnumbered | `testMachine_lineBasedAndBracketedParseSameGraph` |  | capdag.test.js:3091 |
| unnumbered | `testMachine_lineBasedEquivalentToBracketed` |  | capdag.test.js:3058 |
| unnumbered | `testMachine_lineBasedFanIn` |  | capdag.test.js:3037 |
| unnumbered | `testMachine_lineBasedFormatSerialization` |  | capdag.test.js:3070 |
| unnumbered | `testMachine_lineBasedLoop` |  | capdag.test.js:3028 |
| unnumbered | `testMachine_lineBasedSimpleChain` | --- Machine parser line-based mode tests --- | capdag.test.js:3005 |
| unnumbered | `testMachine_lineBasedTwoStepChain` |  | capdag.test.js:3018 |
| unnumbered | `testMachine_loopEdge` |  | capdag.test.js:2929 |
| unnumbered | `testMachine_malformedInputFails` |  | capdag.test.js:2989 |
| unnumbered | `testMachine_mediaRegistryEntry_construction` |  | capdag.test.js:3838 |
| unnumbered | `testMachine_mediaUrnIsComparable` |  | capdag.test.js:3618 |
| unnumbered | `testMachine_mediaUrnIsEquivalent` | --- MediaUrn.isEquivalent/isComparable tests --- | capdag.test.js:3610 |
| unnumbered | `testMachine_mixedBracketedAndLineBased` |  | capdag.test.js:3050 |
| unnumbered | `testMachine_multilineFormat` |  | capdag.test.js:2967 |
| unnumbered | `testMachine_multilineSerializeFormat` |  | capdag.test.js:3462 |
| unnumbered | `testMachine_nodeAliasCollision` |  | capdag.test.js:2945 |
| unnumbered | `testMachine_parseMachineWithAST_aliasMap` |  | capdag.test.js:3681 |
| unnumbered | `testMachine_parseMachineWithAST_fanInSourceLocations` |  | capdag.test.js:3670 |
| unnumbered | `testMachine_parseMachineWithAST_headerLocation` | Phase 0A: Position tracking tests | capdag.test.js:3631 |
| unnumbered | `testMachine_parseMachineWithAST_multilinePositions` |  | capdag.test.js:3661 |
| unnumbered | `testMachine_parseMachineWithAST_nodeMedia` |  | capdag.test.js:3699 |
| unnumbered | `testMachine_parseMachineWithAST_wiringLocation` |  | capdag.test.js:3647 |
| unnumbered | `testMachine_reorderedEdgesProduceSameNotation` |  | capdag.test.js:3446 |
| unnumbered | `testMachine_rootSourcesFanIn` |  | capdag.test.js:3310 |
| unnumbered | `testMachine_rootSourcesLinearChain` |  | capdag.test.js:3282 |
| unnumbered | `testMachine_roundtripFanOut` |  | capdag.test.js:3405 |
| unnumbered | `testMachine_roundtripLoopEdge` |  | capdag.test.js:3420 |
| unnumbered | `testMachine_roundtripSingleEdge` |  | capdag.test.js:3378 |
| unnumbered | `testMachine_roundtripTwoEdgeChain` |  | capdag.test.js:3391 |
| unnumbered | `testMachine_serializationIsDeterministic` |  | capdag.test.js:3433 |
| unnumbered | `testMachine_serializeEmptyGraph` |  | capdag.test.js:3374 |
| unnumbered | `testMachine_serializeSingleEdge` | --- Machine serializer tests (mirrors serializer.rs tests) --- | capdag.test.js:3346 |
| unnumbered | `testMachine_serializeTwoEdgeChain` |  | capdag.test.js:3361 |
| unnumbered | `testMachine_simpleLinearChain` |  | capdag.test.js:2859 |
| unnumbered | `testMachine_toMermaid_emptyGraph` |  | capdag.test.js:3778 |
| unnumbered | `testMachine_toMermaid_fanIn` |  | capdag.test.js:3784 |
| unnumbered | `testMachine_toMermaid_fanOut` |  | capdag.test.js:3795 |
| unnumbered | `testMachine_toMermaid_linearChain` | Phase 0C: Machine.toMermaid() tests | capdag.test.js:3749 |
| unnumbered | `testMachine_toMermaid_loopEdge` |  | capdag.test.js:3767 |
| unnumbered | `testMachine_twoStepChain` |  | capdag.test.js:2874 |
| unnumbered | `testMachine_undefinedAliasFails` |  | capdag.test.js:2938 |
| unnumbered | `testMachine_unterminatedBracketFails` |  | capdag.test.js:2996 |
| unnumbered | `testMachine_whitespaceOnly` |  | capdag.test.js:2837 |
| unnumbered | `testRenderer_buildBrowseGraphData_rejectsMissingMediaTitles` |  | capdag.test.js:4053 |
| unnumbered | `testRenderer_buildEditorGraphData_capWithoutCompleteArgsIsDropped` |  | capdag.test.js:5181 |
| unnumbered | `testRenderer_buildEditorGraphData_cardinalityFromDataSlotSequenceFlags` |  | capdag.test.js:5162 |
| unnumbered | `testRenderer_buildEditorGraphData_collapsesCapsIntoLabeledEdges` |  | capdag.test.js:5106 |
| unnumbered | `testRenderer_buildEditorGraphData_loopMarkedEdgeGetsLoopClass` |  | capdag.test.js:5144 |
| unnumbered | `testRenderer_buildEditorGraphData_rejectsEdgeWithMissingSource` |  | capdag.test.js:5198 |
| unnumbered | `testRenderer_buildResolvedMachineGraphData_duplicateNodeIdAcrossStrandsFailsHard` |  | capdag.test.js:5408 |
| unnumbered | `testRenderer_buildResolvedMachineGraphData_fanInProducesEdgePerAssignment` |  | capdag.test.js:5306 |
| unnumbered | `testRenderer_buildResolvedMachineGraphData_loopEdgeGetsLoopClass` |  | capdag.test.js:5272 |
| unnumbered | `testRenderer_buildResolvedMachineGraphData_multiStrandKeepsStrandsDisjoint` |  | capdag.test.js:5346 |
| unnumbered | `testRenderer_buildResolvedMachineGraphData_singleStrandLinearChain` | ---------------- resolved-machine builder ---------------- | capdag.test.js:5214 |
| unnumbered | `testRenderer_buildRunGraphData_allFailedDropsTargetPlaceholder` |  | capdag.test.js:4911 |
| unnumbered | `testRenderer_buildRunGraphData_backboneHasNoForeachNode` |  | capdag.test.js:4857 |
| unnumbered | `testRenderer_buildRunGraphData_closedForeachSuccessMergesAtCollectTarget` |  | capdag.test.js:5037 |
| unnumbered | `testRenderer_buildRunGraphData_failureWithoutFailedCapRendersFullTrace` |  | capdag.test.js:4760 |
| unnumbered | `testRenderer_buildRunGraphData_pagesSuccessesAndFailures` |  | capdag.test.js:4690 |
| unnumbered | `testRenderer_buildRunGraphData_unclosedForeachSuccessNoMerge` |  | capdag.test.js:4976 |
| unnumbered | `testRenderer_buildRunGraphData_usesCapUrnIsEquivalentForFailedCap` |  | capdag.test.js:4798 |
| unnumbered | `testRenderer_buildStrandGraphData_foreachCollectSpan` |  | capdag.test.js:4247 |
| unnumbered | `testRenderer_buildStrandGraphData_nestedForEachThrows` |  | capdag.test.js:4362 |
| unnumbered | `testRenderer_buildStrandGraphData_sequenceShowsCardinality` |  | capdag.test.js:4227 |
| unnumbered | `testRenderer_buildStrandGraphData_singleCapPlain` |  | capdag.test.js:4200 |
| unnumbered | `testRenderer_buildStrandGraphData_standaloneCollect` |  | capdag.test.js:4298 |
| unnumbered | `testRenderer_buildStrandGraphData_unclosedForEachBody` |  | capdag.test.js:4325 |
| unnumbered | `testRenderer_canonicalMediaUrn_normalizesTagOrder` |  | capdag.test.js:4013 |
| unnumbered | `testRenderer_canonicalMediaUrn_preservesValueTags` |  | capdag.test.js:4022 |
| unnumbered | `testRenderer_canonicalMediaUrn_rejectsCapUrn` |  | capdag.test.js:4027 |
| unnumbered | `testRenderer_cardinalityFromCap_findsStdinArgNotFirstArg` |  | capdag.test.js:3938 |
| unnumbered | `testRenderer_cardinalityFromCap_outputOnlySequence` |  | capdag.test.js:3970 |
| unnumbered | `testRenderer_cardinalityFromCap_rejectsStringIsSequence` |  | capdag.test.js:3981 |
| unnumbered | `testRenderer_cardinalityFromCap_scalarDefaultsWhenFieldsMissing` |  | capdag.test.js:3962 |
| unnumbered | `testRenderer_cardinalityFromCap_throwsOnNonObject` |  | capdag.test.js:3994 |
| unnumbered | `testRenderer_cardinalityLabel_allFourCases` |  | capdag.test.js:3923 |
| unnumbered | `testRenderer_cardinalityLabel_usesUnicodeArrow` |  | capdag.test.js:3930 |
| unnumbered | `testRenderer_classifyStrandCapSteps_capFlags` |  | capdag.test.js:4149 |
| unnumbered | `testRenderer_classifyStrandCapSteps_nestedForks` |  | capdag.test.js:4170 |
| unnumbered | `testRenderer_collapseStrand_plainCapDistinctTargetNoMerge` |  | capdag.test.js:4641 |
| unnumbered | `testRenderer_collapseStrand_plainCapMergesTrailingOutput` |  | capdag.test.js:4605 |
| unnumbered | `testRenderer_collapseStrand_sequenceProducingCapBeforeForeach` |  | capdag.test.js:4541 |
| unnumbered | `testRenderer_collapseStrand_singleCapBodyKeepsCapOwnLabel` |  | capdag.test.js:4390 |
| unnumbered | `testRenderer_collapseStrand_standaloneCollectCollapses` |  | capdag.test.js:4498 |
| unnumbered | `testRenderer_collapseStrand_unclosedForEachBodyCollapses` |  | capdag.test.js:4442 |
| unnumbered | `testRenderer_mediaNodeLabel_rejectsUrnDerivedLabels` |  | capdag.test.js:4039 |
| unnumbered | `testRenderer_validateBodyOutcome_rejectsNegativeIndex` | ---------------- run builder ---------------- | capdag.test.js:4680 |
| unnumbered | `testRenderer_validateEditorGraphPayload_rejectsUnknownKind` | ---------------- editor-graph builder ---------------- | capdag.test.js:5092 |
| unnumbered | `testRenderer_validateResolvedMachinePayload_rejectsMissingFields` |  | capdag.test.js:5443 |
| unnumbered | `testRenderer_validateStrandPayload_missingSourceSpec` |  | capdag.test.js:4667 |
| unnumbered | `testRenderer_validateStrandStep_rejectsUnknownVariant` |  | capdag.test.js:4110 |
| unnumbered | `testRenderer_validateStrandStep_requiresBooleanIsSequence` |  | capdag.test.js:4127 |
| unnumbered | `testUrn` |  | capdag.test.js:107 |
| unnumbered | `testisCollection` | Mirror-specific coverage: isCollection returns true when collection marker tag is present Mirror-specific coverage: N/A for JS (MEDIA_COLLECTION constants removed - no longer exists) | capdag.test.js:2495 |
---

## Unnumbered Tests

The following tests are cataloged but do not currently participate in numeric test indexing.

- `testCapFabAddCapPopulatesEdgesAndNodes` — capdag.test.js:1373
- `testCapFabDistinctRegistryNames` — capdag.test.js:1412
- `testCapFabGetOutgoingConformsToMatching` — capdag.test.js:1391
- `testJS_buildExtensionIndex` — capdag.test.js:1654
- `testJS_capDocumentationOmittedWhenNull` — capdag.test.js:1765
- `testJS_capDocumentationRoundTrip` — capdag.test.js:1743
- `testJS_capJSONSerialization` — capdag.test.js:1720
- `testJS_getExtensionMappings` — capdag.test.js:1698
- `testJS_mediaSpecConstruction` — capdag.test.js:1831
- `testJS_mediaSpecDocumentationPropagatesThroughResolve` — capdag.test.js:1788
- `testJS_mediaUrnsForExtension` — capdag.test.js:1670
- `testJS_resolveMediaUrnFromSpecs` — capdag.test.js:1708
- `testJS_stdinSourceKindConstants` — capdag.test.js:1818
- `testJS_stdinSourceNullData` — capdag.test.js:1824
- `testLlmGenerateTextUrnSpecs` — capdag.test.js:1623
- `testMachine_aliasFallbackWithoutOpTag` — capdag.test.js:3489
- `testMachine_aliasFromOpTag` — capdag.test.js:3478
- `testMachine_builderChaining` — capdag.test.js:3547
- `testMachine_builderEquivalentToParsed` — capdag.test.js:3555
- `testMachine_builderRoundTrip` — capdag.test.js:3567
- `testMachine_builderSingleEdge` — capdag.test.js:3523
- `testMachine_builderWithLoop` — capdag.test.js:3535
- `testMachine_capRegistryClient_construction` — capdag.test.js:3851
- `testMachine_capRegistryEntry_construction` — capdag.test.js:3815
- `testMachine_capRegistryEntry_defaults` — capdag.test.js:3858
- `testMachine_capUrnInMediaUrn` — capdag.test.js:3594
- `testMachine_capUrnIsComparable` — capdag.test.js:3587
- `testMachine_capUrnIsEquivalent` — capdag.test.js:3579
- `testMachine_capUrnOutMediaUrn` — capdag.test.js:3601
- `testMachine_conflictingMediaTypesFail` — capdag.test.js:2955
- `testMachine_differentAliasesSameGraph` — capdag.test.js:2977
- `testMachine_displayEdge` — capdag.test.js:3322
- `testMachine_displayGraph` — capdag.test.js:3333
- `testMachine_duplicateAlias` — capdag.test.js:2848
- `testMachine_duplicateOpTagsDisambiguated` — capdag.test.js:3501
- `testMachine_edgeEquivalenceDifferentCapUrns` — capdag.test.js:3133
- `testMachine_edgeEquivalenceDifferentLoopFlag` — capdag.test.js:3165
- `testMachine_edgeEquivalenceDifferentSourceCount` — capdag.test.js:3197
- `testMachine_edgeEquivalenceDifferentTargets` — capdag.test.js:3149
- `testMachine_edgeEquivalenceSameUrns` — capdag.test.js:3117
- `testMachine_edgeEquivalenceSourceOrderIndependent` — capdag.test.js:3181
- `testMachine_emptyInput` — capdag.test.js:2833
- `testMachine_errorLocation_duplicateAlias` — capdag.test.js:3721
- `testMachine_errorLocation_parseError` — capdag.test.js:3711
- `testMachine_errorLocation_undefinedAlias` — capdag.test.js:3735
- `testMachine_fanInSecondaryAssignedByPriorWiring` — capdag.test.js:2905
- `testMachine_fanInSecondaryUnassignedGetsWildcard` — capdag.test.js:2918
- `testMachine_fanOut` — capdag.test.js:2888
- `testMachine_graphEmpty` — capdag.test.js:3270
- `testMachine_graphEmptyEquivalence` — capdag.test.js:3276
- `testMachine_graphEquivalenceReorderedEdges` — capdag.test.js:3228
- `testMachine_graphEquivalenceSameEdges` — capdag.test.js:3213
- `testMachine_graphNotEquivalentDifferentCap` — capdag.test.js:3257
- `testMachine_graphNotEquivalentDifferentEdgeCount` — capdag.test.js:3243
- `testMachine_headerOnlyNoWirings` — capdag.test.js:2841
- `testMachine_leafTargetsLinearChain` — capdag.test.js:3296
- `testMachine_lineBasedAndBracketedParseSameGraph` — capdag.test.js:3091
- `testMachine_lineBasedEquivalentToBracketed` — capdag.test.js:3058
- `testMachine_lineBasedFanIn` — capdag.test.js:3037
- `testMachine_lineBasedFormatSerialization` — capdag.test.js:3070
- `testMachine_lineBasedLoop` — capdag.test.js:3028
- `testMachine_lineBasedSimpleChain` — capdag.test.js:3005
- `testMachine_lineBasedTwoStepChain` — capdag.test.js:3018
- `testMachine_loopEdge` — capdag.test.js:2929
- `testMachine_malformedInputFails` — capdag.test.js:2989
- `testMachine_mediaRegistryEntry_construction` — capdag.test.js:3838
- `testMachine_mediaUrnIsComparable` — capdag.test.js:3618
- `testMachine_mediaUrnIsEquivalent` — capdag.test.js:3610
- `testMachine_mixedBracketedAndLineBased` — capdag.test.js:3050
- `testMachine_multilineFormat` — capdag.test.js:2967
- `testMachine_multilineSerializeFormat` — capdag.test.js:3462
- `testMachine_nodeAliasCollision` — capdag.test.js:2945
- `testMachine_parseMachineWithAST_aliasMap` — capdag.test.js:3681
- `testMachine_parseMachineWithAST_fanInSourceLocations` — capdag.test.js:3670
- `testMachine_parseMachineWithAST_headerLocation` — capdag.test.js:3631
- `testMachine_parseMachineWithAST_multilinePositions` — capdag.test.js:3661
- `testMachine_parseMachineWithAST_nodeMedia` — capdag.test.js:3699
- `testMachine_parseMachineWithAST_wiringLocation` — capdag.test.js:3647
- `testMachine_reorderedEdgesProduceSameNotation` — capdag.test.js:3446
- `testMachine_rootSourcesFanIn` — capdag.test.js:3310
- `testMachine_rootSourcesLinearChain` — capdag.test.js:3282
- `testMachine_roundtripFanOut` — capdag.test.js:3405
- `testMachine_roundtripLoopEdge` — capdag.test.js:3420
- `testMachine_roundtripSingleEdge` — capdag.test.js:3378
- `testMachine_roundtripTwoEdgeChain` — capdag.test.js:3391
- `testMachine_serializationIsDeterministic` — capdag.test.js:3433
- `testMachine_serializeEmptyGraph` — capdag.test.js:3374
- `testMachine_serializeSingleEdge` — capdag.test.js:3346
- `testMachine_serializeTwoEdgeChain` — capdag.test.js:3361
- `testMachine_simpleLinearChain` — capdag.test.js:2859
- `testMachine_toMermaid_emptyGraph` — capdag.test.js:3778
- `testMachine_toMermaid_fanIn` — capdag.test.js:3784
- `testMachine_toMermaid_fanOut` — capdag.test.js:3795
- `testMachine_toMermaid_linearChain` — capdag.test.js:3749
- `testMachine_toMermaid_loopEdge` — capdag.test.js:3767
- `testMachine_twoStepChain` — capdag.test.js:2874
- `testMachine_undefinedAliasFails` — capdag.test.js:2938
- `testMachine_unterminatedBracketFails` — capdag.test.js:2996
- `testMachine_whitespaceOnly` — capdag.test.js:2837
- `testRenderer_buildBrowseGraphData_rejectsMissingMediaTitles` — capdag.test.js:4053
- `testRenderer_buildEditorGraphData_capWithoutCompleteArgsIsDropped` — capdag.test.js:5181
- `testRenderer_buildEditorGraphData_cardinalityFromDataSlotSequenceFlags` — capdag.test.js:5162
- `testRenderer_buildEditorGraphData_collapsesCapsIntoLabeledEdges` — capdag.test.js:5106
- `testRenderer_buildEditorGraphData_loopMarkedEdgeGetsLoopClass` — capdag.test.js:5144
- `testRenderer_buildEditorGraphData_rejectsEdgeWithMissingSource` — capdag.test.js:5198
- `testRenderer_buildResolvedMachineGraphData_duplicateNodeIdAcrossStrandsFailsHard` — capdag.test.js:5408
- `testRenderer_buildResolvedMachineGraphData_fanInProducesEdgePerAssignment` — capdag.test.js:5306
- `testRenderer_buildResolvedMachineGraphData_loopEdgeGetsLoopClass` — capdag.test.js:5272
- `testRenderer_buildResolvedMachineGraphData_multiStrandKeepsStrandsDisjoint` — capdag.test.js:5346
- `testRenderer_buildResolvedMachineGraphData_singleStrandLinearChain` — capdag.test.js:5214
- `testRenderer_buildRunGraphData_allFailedDropsTargetPlaceholder` — capdag.test.js:4911
- `testRenderer_buildRunGraphData_backboneHasNoForeachNode` — capdag.test.js:4857
- `testRenderer_buildRunGraphData_closedForeachSuccessMergesAtCollectTarget` — capdag.test.js:5037
- `testRenderer_buildRunGraphData_failureWithoutFailedCapRendersFullTrace` — capdag.test.js:4760
- `testRenderer_buildRunGraphData_pagesSuccessesAndFailures` — capdag.test.js:4690
- `testRenderer_buildRunGraphData_unclosedForeachSuccessNoMerge` — capdag.test.js:4976
- `testRenderer_buildRunGraphData_usesCapUrnIsEquivalentForFailedCap` — capdag.test.js:4798
- `testRenderer_buildStrandGraphData_foreachCollectSpan` — capdag.test.js:4247
- `testRenderer_buildStrandGraphData_nestedForEachThrows` — capdag.test.js:4362
- `testRenderer_buildStrandGraphData_sequenceShowsCardinality` — capdag.test.js:4227
- `testRenderer_buildStrandGraphData_singleCapPlain` — capdag.test.js:4200
- `testRenderer_buildStrandGraphData_standaloneCollect` — capdag.test.js:4298
- `testRenderer_buildStrandGraphData_unclosedForEachBody` — capdag.test.js:4325
- `testRenderer_canonicalMediaUrn_normalizesTagOrder` — capdag.test.js:4013
- `testRenderer_canonicalMediaUrn_preservesValueTags` — capdag.test.js:4022
- `testRenderer_canonicalMediaUrn_rejectsCapUrn` — capdag.test.js:4027
- `testRenderer_cardinalityFromCap_findsStdinArgNotFirstArg` — capdag.test.js:3938
- `testRenderer_cardinalityFromCap_outputOnlySequence` — capdag.test.js:3970
- `testRenderer_cardinalityFromCap_rejectsStringIsSequence` — capdag.test.js:3981
- `testRenderer_cardinalityFromCap_scalarDefaultsWhenFieldsMissing` — capdag.test.js:3962
- `testRenderer_cardinalityFromCap_throwsOnNonObject` — capdag.test.js:3994
- `testRenderer_cardinalityLabel_allFourCases` — capdag.test.js:3923
- `testRenderer_cardinalityLabel_usesUnicodeArrow` — capdag.test.js:3930
- `testRenderer_classifyStrandCapSteps_capFlags` — capdag.test.js:4149
- `testRenderer_classifyStrandCapSteps_nestedForks` — capdag.test.js:4170
- `testRenderer_collapseStrand_plainCapDistinctTargetNoMerge` — capdag.test.js:4641
- `testRenderer_collapseStrand_plainCapMergesTrailingOutput` — capdag.test.js:4605
- `testRenderer_collapseStrand_sequenceProducingCapBeforeForeach` — capdag.test.js:4541
- `testRenderer_collapseStrand_singleCapBodyKeepsCapOwnLabel` — capdag.test.js:4390
- `testRenderer_collapseStrand_standaloneCollectCollapses` — capdag.test.js:4498
- `testRenderer_collapseStrand_unclosedForEachBodyCollapses` — capdag.test.js:4442
- `testRenderer_mediaNodeLabel_rejectsUrnDerivedLabels` — capdag.test.js:4039
- `testRenderer_validateBodyOutcome_rejectsNegativeIndex` — capdag.test.js:4680
- `testRenderer_validateEditorGraphPayload_rejectsUnknownKind` — capdag.test.js:5092
- `testRenderer_validateResolvedMachinePayload_rejectsMissingFields` — capdag.test.js:5443
- `testRenderer_validateStrandPayload_missingSourceSpec` — capdag.test.js:4667
- `testRenderer_validateStrandStep_rejectsUnknownVariant` — capdag.test.js:4110
- `testRenderer_validateStrandStep_requiresBooleanIsSequence` — capdag.test.js:4127
- `testUrn` — capdag.test.js:107
- `testisCollection` — capdag.test.js:2495

---

*Generated from JS source tree*
*Total tests: 328*
*Total numbered tests: 178*
*Total unnumbered tests: 150*
*Total numbered tests missing descriptions: 0*
*Total numbering mismatches: 0*

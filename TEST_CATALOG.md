# Test catalogue — capdag/capdag-js

Generated from the catalogue table by `sdx catalog export`. Edit the tests, not this file.

371 tests: 371 numbered, 0 unnumbered.

## Numbered

| Number | Repository | Language | Test | Location | Description |
|---|---|---|---|---|---|
| TEST1 | capdag/capdag-js | js | `test001_capUrnCreation` | capdag.test.js:157 | TEST1: Test that cap URN is created with tags parsed correctly and direction specs accessible |
| TEST2 | capdag/capdag-js | js | `test002_directionSpecsRequired` | capdag.test.js:167 | TEST2: Test that missing 'in' or 'out' defaults to media: wildcard |
| TEST3 | capdag/capdag-js | js | `test003_directionMatching` | capdag.test.js:178 | TEST3: Test that direction specs must match exactly, different in/out types don't match, wildcard matches any |
| TEST4 | capdag/capdag-js | js | `test004_unquotedValuesLowercased` | capdag.test.js:193 | TEST4: Test that unquoted keys and values are normalized to lowercase |
| TEST5 | capdag/capdag-js | js | `test005_quotedValuesPreserveCase` | capdag.test.js:201 | TEST5: Test that quoted values preserve case while unquoted are lowercased |
| TEST6 | capdag/capdag-js | js | `test006_quotedValueSpecialChars` | capdag.test.js:207 | TEST6: Test that quoted values can contain special characters (semicolons, equals, spaces) |
| TEST7 | capdag/capdag-js | js | `test007_quotedValueEscapeSequences` | capdag.test.js:213 | TEST7: Test that escape sequences in quoted values (\" and \\) are parsed correctly |
| TEST8 | capdag/capdag-js | js | `test008_mixedQuotedUnquoted` | capdag.test.js:220 | TEST8: Test that mixed quoted and unquoted values in same URN parse correctly |
| TEST9 | capdag/capdag-js | js | `test009_unterminatedQuoteError` | capdag.test.js:227 | TEST9: Test that unterminated quote produces UnterminatedQuote error |
| TEST10 | capdag/capdag-js | js | `test010_invalidEscapeSequenceError` | capdag.test.js:240 | TEST10: Test that invalid escape sequences (like \n, \x) produce InvalidEscapeSequence error |
| TEST11 | capdag/capdag-js | js | `test011_serializationSmartQuoting` | capdag.test.js:254 | TEST11: Test that serialization uses smart quoting (no quotes for simple lowercase, quotes for special chars/uppercase) |
| TEST12 | capdag/capdag-js | js | `test012_roundTripSimple` | capdag.test.js:263 | TEST12: Test that simple cap URN round-trips (parse -> serialize -> parse equals original) |
| TEST13 | capdag/capdag-js | js | `test013_roundTripQuoted` | capdag.test.js:271 | TEST13: Test that quoted values round-trip preserving case and spaces |
| TEST14 | capdag/capdag-js | js | `test014_roundTripEscapes` | capdag.test.js:280 | TEST14: Test that escape sequences round-trip correctly |
| TEST15 | capdag/capdag-js | js | `test015_capPrefixRequired` | capdag.test.js:290 | TEST15: Test that cap: prefix is required and case-insensitive |
| TEST16 | capdag/capdag-js | js | `test016_trailingSemicolonEquivalence` | capdag.test.js:302 | TEST16: Test that trailing semicolon is equivalent (same hash, same string, matches) |
| TEST17 | capdag/capdag-js | js | `test017_tagMatching` | capdag.test.js:338 | TEST17: Test tag matching: exact match, subset match, wildcard match, value mismatch |
| TEST18 | capdag/capdag-js | js | `test018_matchingCaseSensitiveValues` | capdag.test.js:362 | TEST18: Test that quoted values with different case do NOT match (case-sensitive) |
| TEST19 | capdag/capdag-js | js | `test019_missingTagHandling` | capdag.test.js:369 | TEST19: Missing tag in instance causes rejection — pattern's tags are constraints |
| TEST20 | capdag/capdag-js | js | `test020_specificity` | capdag.test.js:391 | TEST020: Specificity is the sum of per-tag truth-table scores across in/out/y. Marker tags (bare segments and `key=*`) score 2 (must-have-any), exact `key=value` tags score 3, missing/`?` score 0, `!` scores 1. test6204_Urn() builds "cap:in=media:void;out=media:record;<tags>" so the directional baseline is: in:  media:void   -> {void=*}    -> 2 out: media:record -> {record=*}  -> 2 Total directional baseline: 4. |
| TEST21 | capdag/capdag-js | js | `test021_builder` | capdag.test.js:419 | TEST21: Test builder creates cap URN with correct tags and direction specs |
| TEST22 | capdag/capdag-js | js | `test022_builderRequiresDirection` | capdag.test.js:433 | TEST22: Test builder requires both in_spec and out_spec |
| TEST23 | capdag/capdag-js | js | `test023_builderPreservesCase` | capdag.test.js:447 | TEST23: Test builder lowercases keys but preserves value case |
| TEST24 | capdag/capdag-js | js | `test024_compatibility` | capdag.test.js:458 | TEST24: Directional accepts — pattern's tags are constraints, instance must satisfy |
| TEST25 | capdag/capdag-js | js | `test025_bestMatch` | capdag.test.js:478 | TEST25: Test find_best_match returns most specific matching cap |
| TEST26 | capdag/capdag-js | js | `test026_mergeAndSubset` | capdag.test.js:491 | TEST26: Test merge combines tags from both caps, subset keeps only specified tags |
| TEST27 | capdag/capdag-js | js | `test027_wildcardTag` | capdag.test.js:510 | TEST27: Test with_wildcard_tag sets tag to wildcard, including in/out |
| TEST28 | capdag/capdag-js | js | `test028_emptyCapUrnNotAllowed` | capdag.test.js:523 | TEST28: Test empty cap URN is illegal after effect transition |
| TEST29 | capdag/capdag-js | js | `test029_minimalCapUrn` | capdag.test.js:532 | TEST29: Test minimal valid cap URN has just in and out, empty tags |
| TEST30 | capdag/capdag-js | js | `test030_extendedCharacterSupport` | capdag.test.js:540 | TEST30: Test extended characters (forward slashes, colons) in tag values |
| TEST31 | capdag/capdag-js | js | `test031_wildcardRestrictions` | capdag.test.js:547 | TEST31: Test wildcard rejected in keys but accepted in values |
| TEST32 | capdag/capdag-js | js | `test032_duplicateKeyRejection` | capdag.test.js:565 | TEST32: Test duplicate keys are rejected with DuplicateKey error |
| TEST33 | capdag/capdag-js | js | `test033_numericKeyRestriction` | capdag.test.js:574 | TEST33: Test pure numeric keys rejected, mixed alphanumeric allowed, numeric values allowed |
| TEST34 | capdag/capdag-js | js | `test034_emptyValueError` | capdag.test.js:588 | TEST34: Test empty values are rejected |
| TEST35 | capdag/capdag-js | js | `test035_hasTagCaseSensitive` | capdag.test.js:601 | TEST35: Test has_tag is case-sensitive for values, case-insensitive for keys, works for in/out |
| TEST36 | capdag/capdag-js | js | `test036_withTagPreservesValue` | capdag.test.js:613 | TEST36: Test with_tag preserves value case |
| TEST37 | capdag/capdag-js | js | `test037_withTagRejectsEmptyValue` | capdag.test.js:620 | TEST37: Test with_tag rejects empty value |
| TEST38 | capdag/capdag-js | js | `test038_semanticEquivalence` | capdag.test.js:630 | TEST38: Test semantic equivalence of unquoted and quoted simple lowercase values |
| TEST39 | capdag/capdag-js | js | `test039_getTagReturnsDirectionSpecs` | capdag.test.js:638 | TEST39: Test get_tag returns direction specs (in/out) with case-insensitive lookup |
| TEST40 | capdag/capdag-js | js | `test040_matchingSemanticsExactMatch` | capdag.test.js:647 | TEST40: Matching semantics - exact match succeeds |
| TEST41 | capdag/capdag-js | js | `test041_matchingSemanticsCapMissingTag` | capdag.test.js:654 | TEST41: Matching semantics - cap missing tag matches (implicit wildcard) |
| TEST42 | capdag/capdag-js | js | `test042_matchingSemanticsCapHasExtraTag` | capdag.test.js:662 | TEST42: Pattern rejects instance missing required tags |
| TEST43 | capdag/capdag-js | js | `test043_matchingSemanticsRequestHasWildcard` | capdag.test.js:670 | TEST43: Matching semantics - request wildcard matches specific cap value |
| TEST44 | capdag/capdag-js | js | `test044_matchingSemanticsCapHasWildcard` | capdag.test.js:677 | TEST44: Matching semantics - cap wildcard matches specific request value |
| TEST45 | capdag/capdag-js | js | `test045_matchingSemanticsValueMismatch` | capdag.test.js:684 | TEST45: Matching semantics - value mismatch does not match |
| TEST46 | capdag/capdag-js | js | `test046_matchingSemanticsFallbackPattern` | capdag.test.js:691 | TEST46: Matching semantics - fallback pattern (cap missing tag = implicit wildcard) |
| TEST47 | capdag/capdag-js | js | `test047_matchingSemanticsThumbnailVoidInput` | capdag.test.js:699 | TEST47: Matching semantics - thumbnail fallback with void input |
| TEST48 | capdag/capdag-js | js | `test048_matchingSemanticsWildcardDirection` | capdag.test.js:706 | TEST48: Matching semantics - wildcard direction matches anything |
| TEST49 | capdag/capdag-js | js | `test049_matchingSemanticsCrossDimension` | capdag.test.js:713 | TEST49: Non-overlapping tags — neither direction accepts |
| TEST50 | capdag/capdag-js | js | `test050_matchingSemanticsDirectionMismatch` | capdag.test.js:721 | TEST50: Matching semantics - direction mismatch prevents matching |
| TEST60 | capdag/capdag-js | js | `test060_wrongPrefixFails` | capdag.test.js:866 | TEST60: Test wrong prefix fails with InvalidPrefix error showing expected and actual prefix |
| TEST62 | capdag/capdag-js | js | `test062_isRecord` | capdag.test.js:879 | TEST62: Test is_record returns true when record marker tag is present indicating key-value structure |
| TEST63 | capdag/capdag-js | js | `test063_isScalar` | capdag.test.js:890 | TEST63: Test is_scalar returns true when list marker tag is absent (scalar is default) |
| TEST64 | capdag/capdag-js | js | `test064_isList` | capdag.test.js:903 | TEST64: Test is_list returns true when list marker tag is present indicating ordered collection |
| TEST65 | capdag/capdag-js | js | `test065_isOpaque` | capdag.test.js:912 | TEST65: Test is_opaque returns true when record marker is absent (opaque is default) |
| TEST66 | capdag/capdag-js | js | `test066_isJson` | capdag.test.js:923 | TEST66: Test is_json returns true only when json marker tag is present for JSON representation |
| TEST67 | capdag/capdag-js | js | `test067_isText` | capdag.test.js:932 | TEST67: Text-representability is now carried by the orthogonal `enc=` tag (the old `textable` marker and is_text() are gone). A media is "text" iff it declares an encoding. enc is orthogonal to format/numeric, so only media that actually carry enc= are text. |
| TEST68 | capdag/capdag-js | js | `test068_isVoid` | capdag.test.js:945 | TEST68: Test is_void returns true when void flag or type=void tag is present |
| TEST71 | capdag/capdag-js | js | `test071_toStringRoundtrip` | capdag.test.js:953 | TEST71: Test to_string roundtrip ensures serialization and deserialization preserve URN structure |
| TEST72 | capdag/capdag-js | js | `test072_constantsParse` | capdag.test.js:963 | TEST72: Test all media URN constants parse successfully as valid media URNs |
| TEST74 | capdag/capdag-js | js | `test074_mediaUrnMatching` | capdag.test.js:983 | TEST74: Test media URN conforms_to using tagged URN semantics with specific and generic requirements |
| TEST75 | capdag/capdag-js | js | `test075_accepts` | capdag.test.js:997 | TEST75: Test accepts with implicit wildcards where handlers with fewer tags can handle more requests |
| TEST76 | capdag/capdag-js | js | `test076_specificity` | capdag.test.js:1008 | TEST76: Test specificity increases with more tags for ranking conformance |
| TEST77 | capdag/capdag-js | js | `test077_serdeRoundtrip` | capdag.test.js:1017 | TEST77: Test serde roundtrip serializes to JSON string and deserializes back correctly |
| TEST78 | capdag/capdag-js | js | `test078_debugMatchingBehavior` | capdag.test.js:1026 | TEST78: conforms_to behavior between MEDIA_OBJECT and MEDIA_STRING |
| TEST93 | capdag/capdag-js | js | `test93_resolveUnresolvableFailsHard` | capdag.test.js:1068 | TEST93: Test resolving unknown media URN fails with UnresolvableMediaUrn error |
| TEST99 | capdag/capdag-js | js | `test99_resolvedIsBinary` | capdag.test.js:1087 | TEST99: Test ResolvedMediaDef is_binary returns true when enc tag is absent |
| TEST100 | capdag/capdag-js | js | `test100_resolvedIsRecord` | capdag.test.js:1093 | TEST100: Test ResolvedMediaDef is_record returns true when record marker is present |
| TEST101 | capdag/capdag-js | js | `test101_resolvedIsScalar` | capdag.test.js:1099 | TEST101: Test ResolvedMediaDef is_scalar returns true when list marker is absent |
| TEST102 | capdag/capdag-js | js | `test102_resolvedIsList` | capdag.test.js:1105 | TEST102: Test ResolvedMediaDef is_list returns true when list marker is present |
| TEST103 | capdag/capdag-js | js | `test103_resolvedIsJson` | capdag.test.js:1111 | TEST103: Test ResolvedMediaDef is_json returns true when json tag is present |
| TEST104 | capdag/capdag-js | js | `test104_resolvedIsText` | capdag.test.js:1117 | TEST104: Test ResolvedMediaDef is_text returns true when enc tag is present |
| TEST105 | capdag/capdag-js | js | `test105_metadataPropagation` | capdag.test.js:1123 | TEST105: Test metadata propagates from media def def to resolved media def |
| TEST106 | capdag/capdag-js | js | `test106_metadataWithValidation` | capdag.test.js:1146 | TEST106: Test metadata and validation can coexist in media definition |
| TEST107 | capdag/capdag-js | js | `test107_extensionsPropagation` | capdag.test.js:1165 | TEST107: Test extensions field propagates from media def def to resolved |
| TEST108 | capdag/capdag-js | js | `test108_extensionsSerialization` | capdag.test.js:1181 | TEST108: Test creating new cap with URN, title, and command verifies correct initialization |
| TEST109 | capdag/capdag-js | js | `test109_extensionsWithMetadataAndValidation` | capdag.test.js:1189 | TEST109: Test creating cap with metadata initializes and retrieves metadata correctly |
| TEST110 | capdag/capdag-js | js | `test110_multipleExtensions` | capdag.test.js:1208 | TEST110: Test cap matching with subset semantics for request fulfillment |
| TEST115 | capdag/capdag-js | js | `test115_capArgSerialization` | capdag.test.js:1224 | TEST115: Test CapArg serialization and deserialization with multiple sources |
| TEST116 | capdag/capdag-js | js | `test116_capArgConstructors` | capdag.test.js:1257 | TEST116: Test CapArg constructor methods basic and with_description create args correctly |
| TEST125 | capdag/capdag-js | js | `test125_effectNonePreservesRuntimeMedia` | capdag.test.js:3239 | TEST125: effect=none preserves runtime media identity |
| TEST126 | capdag/capdag-js | js | `test126_effectDeclaredUsesDeclaredOutput` | capdag.test.js:3248 | TEST126: default effect=declared uses the declared output |
| TEST127 | capdag/capdag-js | js | `test127_invalidEffectNoneFailsHard` | capdag.test.js:3259 | TEST127: invalid effect=none declarations fail hard |
| TEST128 | capdag/capdag-js | js | `test128_effectDispatchRequiresExplicitWildcard` | capdag.test.js:3342 | TEST128: omitted effect means declared; unconstrained effect must be explicit |
| TEST150 | capdag/capdag-js | js | `test150_capManifestJsonSerialization` | capdag.test.js:1285 | TEST150: JSON roundtrip |
| TEST156 | capdag/capdag-js | js | `test156_stdinSourceFromData` | capdag.test.js:1441 | TEST156: Test creating StdinSource Data variant with byte vector |
| TEST157 | capdag/capdag-js | js | `test157_stdinSourceFromFileReference` | capdag.test.js:1452 | TEST157: Test creating StdinSource FileReference variant with all required fields |
| TEST158 | capdag/capdag-js | js | `test158_stdinSourceWithEmptyData` | capdag.test.js:1469 | TEST158: Test StdinSource Data with empty vector stores and retrieves correctly |
| TEST159 | capdag/capdag-js | js | `test159_stdinSourceWithBinaryContent` | capdag.test.js:1477 | TEST159: Test StdinSource Data with binary content like PNG header bytes |
| TEST274 | capdag/capdag-js | js | `test274_capArgumentValueNew` | capdag.test.js:1491 | TEST274: Test CapArgumentValue::new stores media_urn and raw byte value |
| TEST275 | capdag/capdag-js | js | `test275_capArgumentValueFromStr` | capdag.test.js:1498 | TEST275: Test CapArgumentValue::from_str converts string to UTF-8 bytes |
| TEST276 | capdag/capdag-js | js | `test276_capArgumentValueAsStrValid` | capdag.test.js:1505 | TEST276: Test CapArgumentValue::value_as_str succeeds for UTF-8 data |
| TEST277 | capdag/capdag-js | js | `test277_capArgumentValueAsStrInvalidUtf8` | capdag.test.js:1511 | TEST277: Test CapArgumentValue::value_as_str fails for non-UTF-8 binary data |
| TEST278 | capdag/capdag-js | js | `test278_capArgumentValueEmpty` | capdag.test.js:1523 | TEST278: Test CapArgumentValue::new with empty value stores empty vec |
| TEST282 | capdag/capdag-js | js | `test282_capArgumentValueUnicode` | capdag.test.js:1532 | TEST282: Test CapArgumentValue::from_str with Unicode string preserves all characters |
| TEST283 | capdag/capdag-js | js | `test283_capArgumentValueLargeBinary` | capdag.test.js:1538 | TEST283: Test CapArgumentValue with large binary payload preserves all bytes |
| TEST304 | capdag/capdag-js | js | `test304_mediaAvailabilityOutputConstant` | capdag.test.js:1557 | TEST304: Test MEDIA_AVAILABILITY_OUTPUT constant parses as valid media URN with correct tags |
| TEST305 | capdag/capdag-js | js | `test305_mediaPathOutputConstant` | capdag.test.js:1566 | TEST305: Test MEDIA_PATH_OUTPUT constant parses as valid media URN with correct tags |
| TEST306 | capdag/capdag-js | js | `test306_availabilityAndPathOutputDistinct` | capdag.test.js:1575 | TEST306: Test MEDIA_AVAILABILITY_OUTPUT and MEDIA_PATH_OUTPUT are distinct URNs |
| TEST307 | capdag/capdag-js | js | `test307_modelAvailabilityUrn` | capdag.test.js:1589 | TEST307: Test model_availability_urn builds valid cap URN with correct op and media defs |
| TEST308 | capdag/capdag-js | js | `test308_modelPathUrn` | capdag.test.js:1601 | TEST308: Test model_path_urn builds valid cap URN with correct op and media defs |
| TEST309 | capdag/capdag-js | js | `test309_modelAvailabilityAndPathAreDistinct` | capdag.test.js:1613 | TEST309: Test model_availability_urn and model_path_urn produce distinct URNs |
| TEST310 | capdag/capdag-js | js | `test310_llmGenerateTextUrn` | capdag.test.js:1620 | TEST310: llm_generate_text_urn() produces a valid cap URN with a UTF-8 text input and plain-text terminal output. |
| TEST312 | capdag/capdag-js | js | `test312_allUrnBuildersProduceValidUrns` | capdag.test.js:1643 | TEST312: Test all URN builders produce parseable cap URNs |
| TEST320 | capdag/capdag-js | js | `test320_cartridgeInfoConstruction` | capdag.test.js:2009 | TEST320-335: CartridgeRepoServer and CartridgeRepoClient tests |
| TEST321 | capdag/capdag-js | js | `test321_cartridgeInfoIsSigned` | capdag.test.js:2043 | TEST321: CartridgeInfo.is_signed() returns true when signature (team_id + signed_at) is present, false when either is empty. |
| TEST322 | capdag/capdag-js | js | `test322_cartridgeInfoBuildForPlatform` | capdag.test.js:2055 | TEST322: CartridgeInfo.build_for_platform() returns the build that matches the requested platform string and None otherwise. |
| TEST323 | capdag/capdag-js | js | `test323_cartridgeRepoServerValidateRegistry` | capdag.test.js:2089 | TEST323: CartridgeRepoServer requires schema 5.0 and rejects older. |
| TEST324 | capdag/capdag-js | js | `test324_cartridgeRepoServerTransformToArray` | capdag.test.js:2126 | TEST324: CartridgeRepoServer transforms a v4.0 entry into a flat CartridgeInfo, preserving cap_groups verbatim. |
| TEST325 | capdag/capdag-js | js | `test325_cartridgeRepoServerGetCartridges` | capdag.test.js:2163 | TEST325: get_cartridges() wraps the transformed array in the response envelope. |
| TEST326 | capdag/capdag-js | js | `test326_cartridgeRepoServerGetCartridgeById` | capdag.test.js:2175 | TEST326: get_cartridge_by_id requires a channel and returns Some for a known (channel, id), None otherwise. The same id looked up in the wrong channel must miss — channels are independent namespaces. |
| TEST327 | capdag/capdag-js | js | `test327_cartridgeRepoServerSearchCartridges` | capdag.test.js:2205 | TEST327: search_cartridges matches against name/description/tags and cap titles, but never against cap URN strings. |
| TEST328 | capdag/capdag-js | js | `test328_cartridgeRepoServerGetByCategory` | capdag.test.js:2227 | TEST328: CartridgeRepoServer.getCartridgesByCategory() filters cartridges by category across both channels. |
| TEST329 | capdag/capdag-js | js | `test329_cartridgeRepoServerGetByCap` | capdag.test.js:2246 | TEST329: CartridgeRepoServer.getCartridgesByCap() parses the input URN and matches each declared cap via `conformsTo`. Tag-order differences resolve because matching is order-theoretic, not string. |
| TEST330 | capdag/capdag-js | js | `test330_cartridgeRepoClientUpdateCache` | capdag.test.js:2263 | TEST330: CartridgeRepoClient updates its local cache keyed by "<channel>:<id>". The cache holds release and nightly entries independently — the same id is allowed in both. |
| TEST331 | capdag/capdag-js | js | `test331_cartridgeRepoClientGetSuggestions` | capdag.test.js:2291 | TEST331: CartridgeRepoClient.getSuggestionsForCap() returns cartridge suggestions with channel propagated onto each suggestion. |
| TEST332 | capdag/capdag-js | js | `test332_cartridgeRepoClientGetCartridge` | capdag.test.js:2320 | TEST332: get_cartridge requires a (channel, id) pair and returns the cached entry for known pairs, None otherwise. The same id in the wrong channel must miss. |
| TEST333 | capdag/capdag-js | js | `test333_cartridgeRepoClientGetAllCaps` | capdag.test.js:2364 | TEST333: get_all_available_caps returns the deduplicated set of normalized URNs across cartridges. |
| TEST334 | capdag/capdag-js | js | `test334_cartridgeRepoClientNeedsSync` | capdag.test.js:2380 | TEST334: needs_sync returns true on an empty cache, false right after a successful update. |
| TEST335 | capdag/capdag-js | js | `test335_cartridgeRepoServerClientIntegration` | capdag.test.js:2399 | TEST335: Round-trip: server produces a v5.0 response, client consumes it, channel provenance is preserved end-to-end. |
| TEST546 | capdag/capdag-js | js | `test546_isImage` | capdag.test.js:2737 | TEST546: is_image returns true only when image marker tag is present |
| TEST547 | capdag/capdag-js | js | `test547_isAudio` | capdag.test.js:2749 | TEST547: is_audio returns true only when audio marker tag is present |
| TEST548 | capdag/capdag-js | js | `test548_isVideo` | capdag.test.js:2760 | TEST548: is_video returns true only when video marker tag is present |
| TEST549 | capdag/capdag-js | js | `test549_isNumeric` | capdag.test.js:2770 | TEST549: is_numeric returns true only when numeric marker tag is present |
| TEST550 | capdag/capdag-js | js | `test550_isBool` | capdag.test.js:2782 | TEST550: is_bool returns true only when bool marker tag is present |
| TEST551 | capdag/capdag-js | js | `test551_isFilePath` | capdag.test.js:2794 | TEST551: is_file_path returns true for the single file-path media URN, false for everything else. There is no "array" variant — cardinality is carried by is_sequence on the wire, not by URN tags. |
| TEST553 | capdag/capdag-js | js | `test553_isLiveFeed` | capdag.test.js:2801 | TEST553: is_live_feed returns true for every URN carrying the `live` marker tag (the reference-media family the runtime resolves via providers), false for everything else — including content URNs a feed delivers. |
| TEST558 | capdag/capdag-js | js | `test558_predicateConstantConsistency` | capdag.test.js:2823 | TEST558: predicates are consistent with constants — every constant triggers exactly the expected predicates |
| TEST559 | capdag/capdag-js | js | `test559_withoutTag` | capdag.test.js:2862 | TEST559: without_tag removes tag, rejects structural keys, case-insensitive for keys |
| TEST560 | capdag/capdag-js | js | `test560_withInOutSpec` | capdag.test.js:2882 | TEST560: with_in_spec and with_out_spec change direction specs |
| TEST563 | capdag/capdag-js | js | `test563_findAllMatches` | capdag.test.js:2912 | TEST563: CapMatcher::find_all_matches returns all matching caps sorted by specificity |
| TEST564 | capdag/capdag-js | js | `test564_areCompatible` | capdag.test.js:2930 | TEST564: CapMatcher::are_compatible detects bidirectional overlap |
| TEST566 | capdag/capdag-js | js | `test566_withTagRejectsStructuralKeys` | capdag.test.js:2955 | TEST566: with_tag rejects structural keys |
| TEST597 | capdag/capdag-js | js | `test597_capArgWithFullDefinition` | capdag.test.js:1341 | TEST597: CapArg::with_full_definition stores all fields including optional ones |
| TEST640 | capdag/capdag-js | js | `test640_inOnlyIsIllegal` | capdag.test.js:3095 | TEST640: cap:in defaults to the same illegal bare top form |
| TEST641 | capdag/capdag-js | js | `test641_outOnlyIsIllegal` | capdag.test.js:3104 | TEST641: cap:out defaults to the same illegal bare top form |
| TEST642 | capdag/capdag-js | js | `test642_inOutWithoutValuesAreIllegal` | capdag.test.js:3113 | TEST642: cap:in;out becomes the same illegal bare top form |
| TEST643 | capdag/capdag-js | js | `test643_explicitAsteriskIsIllegal` | capdag.test.js:3122 | TEST643: cap:in=*;out=* is the same illegal bare top form |
| TEST644 | capdag/capdag-js | js | `test644_specificInWildcardOutIsIllegal` | capdag.test.js:3131 | TEST644: cap:in=media:;out=* is the same illegal bare top form |
| TEST645 | capdag/capdag-js | js | `test645_wildcardInSpecificOut` | capdag.test.js:3140 | TEST645: cap:in=*;out=media:text has wildcard in, specific out |
| TEST646 | capdag/capdag-js | js | `test646_invalidInSpecFails` | capdag.test.js:3147 | TEST646: cap:in=foo fails (invalid media URN) |
| TEST647 | capdag/capdag-js | js | `test647_invalidOutSpecFails` | capdag.test.js:3156 | TEST647: cap:in=media:;out=bar fails (invalid media URN) |
| TEST648 | capdag/capdag-js | js | `test648_wildcardAcceptsSpecific` | capdag.test.js:3165 | TEST648: Wildcard in/out match specific caps |
| TEST649 | capdag/capdag-js | js | `test649_specificityScoring` | capdag.test.js:3174 | TEST649: Specificity - wildcard has 0, specific has tag count |
| TEST650 | capdag/capdag-js | js | `test650_wildcardPreserveOtherTags` | capdag.test.js:3183 | TEST650: cap:in=media:;out=media:;test preserves other tags |
| TEST653 | capdag/capdag-js | js | `test653_invalidEffectNoneDeclarationRejected` | capdag.test.js:3230 | TEST653: invalid effect=none declarations fail at construction |
| TEST890 | capdag/capdag-js | js | `test890_directionSemanticMatching` | capdag.test.js:732 | TEST890: Semantic direction matching - generic candidate matches specific request |
| TEST891 | capdag/capdag-js | js | `test891_directionSemanticSpecificity` | capdag.test.js:782 | TEST891: Semantic direction specificity — more constraints in either axis means a higher score under the truth-table-driven sum. media: (top, no tags) scores 0; each marker tag scores 2; each exact tag scores 3. |
| TEST939 | capdag/capdag-js | js | `test939_capUrnCanonicalFormDropsWildcardInOut` | capdag.test.js:310 | TEST939: The canonical form drops `in=media:` and `out=media:` segments. Every spelling of "the same cap with wildcard in/out" collapses to one byte-identical canonical string. This is the contract that makes registry lookups work: the cap-publisher hashes `<canonical-urn>` to compute the cache key, and every language port (Rust, Go, Python, JS, ObjC) must agree on the canonical form for cross-language lookups to land on the same key. A regression that emitted the wildcard segments would silently move the published cap to a different SHA-256 bucket, 404'ing every reader that hashes the canonical form. |
| TEST1196 | capdag/capdag-js | js | `test1196_aliasedSerializationUsesAliasAndDropsHeader` | capdag.test.js:6952 | TEST1196: toMachineNotationAliased references an aliased cap DIRECTLY in the wiring by its display alias (shortest, then alphabetical) with NO header, and keeps the synthetic `edge_N` token + header for a cap that has no alias. |
| TEST1294 | capdag/capdag-js | js | `test1294_rule11VoidInputWithStdinRejected` | capdag.test.js:2982 | TEST1294: RULE11 - void-input cap with stdin source rejected |
| TEST1295 | capdag/capdag-js | js | `test1295_rule11NonVoidInputWithoutStdinRejected` | capdag.test.js:2997 | TEST1295: RULE11 - non-void-input cap without stdin source rejected |
| TEST1296 | capdag/capdag-js | js | `test1296_rule11VoidInputCliFlagOnly` | capdag.test.js:3012 | TEST1296: RULE11 - void-input cap with only cli_flag sources passes |
| TEST1297 | capdag/capdag-js | js | `test1297_rule11NonVoidInputWithStdin` | capdag.test.js:3070 | TEST1297: RULE11 - non-void-input cap with stdin source passes |
| TEST1450 | capdag/capdag-js | js | `test1450_planRequestDefaults` | capdag.test.js:7050 | TEST1450: a defaults-only request is AUTO with every knob at its default, and the proto JSON carries the documented wire shape. |
| TEST1451 | capdag/capdag-js | js | `test1451_planRequestKnobValidation` | capdag.test.js:7069 | TEST1451: at-depth REQUIRES a positive depth; a depth anywhere else is invalid; ranking never flips the request to CONFIGURED but any space-constraining knob does (mode is forced to CONFIGURED on the wire). |
| TEST1452 | capdag/capdag-js | js | `test1452_knobProtoRoundTrip` | capdag.test.js:7110 | TEST1452: every knob round-trips value → proto number → value, and an unknown value/number fails hard in both directions. |
| TEST1453 | capdag/capdag-js | js | `test1453_planResponseParsers` | capdag.test.js:7129 | TEST1453: candidate/target parsers accept realistic proto-JSON and sort candidates by rank; malformed payloads (missing field, wrong type) fail hard with the offending path in the message. |
| TEST1514 | capdag/capdag-js | js | `test1514_installSourceVocabularyTolerance` | capdag.test.js:7019 | TEST1514: the provenance vocabulary grows with installers. A workspace build install parses to its named value; a spelling this build does not know parses, is preserved VERBATIM, round-trips, and is not BUNDLE (the one semantic value) — an unknown telemetry hint can never fail the cartridge.json parse and take the cartridge down with it. |
| TEST1800 | capdag/capdag-js | js | `test1800_kindIdentityOnlyForBareCap` | capdag.test.js:6348 | TEST1800: Identity classifier — and only explicit effect=none qualifies. |
| TEST1801 | capdag/capdag-js | js | `test1801_kindSourceWhenInputIsVoid` | capdag.test.js:6375 | TEST1801: Source classifier — in=media:void, out non-void. |
| TEST1802 | capdag/capdag-js | js | `test1802_kindSinkWhenOutputIsVoid` | capdag.test.js:6384 | TEST1802: Sink classifier — out=media:void, in non-void. |
| TEST1803 | capdag/capdag-js | js | `test1803_kindEffectWhenBothSidesVoid` | capdag.test.js:6393 | TEST1803: Effect classifier — both sides void. Reads as `() → ()`. |
| TEST1804 | capdag/capdag-js | js | `test1804_kindTransformForNormalDataProcessors` | capdag.test.js:6403 | TEST1804: Transform classifier — at least one side non-void, and the cap is not the bare identity. The default kind for ordinary data-processing caps. |
| TEST1805 | capdag/capdag-js | js | `test1805_kindInvariantUnderCanonicalSpellings` | capdag.test.js:6446 | TEST1805: Kind is invariant under canonicalization. The same morphism written in many surface forms must classify the same way once parsed. This pins the rule that kind is a property of the cap as a structured object, not of any particular spelling. |
| TEST1810 | capdag/capdag-js | js | `test1810_mediaVoidIsAtomic` | capdag.test.js:6413 | TEST1810: media:void is atomic — refinements are parse errors. Mirrored across every language port (Rust, Go, Python, Swift/ObjC, JS) under the SAME number. Any divergence is a wire-level inconsistency — the unit type's atomicity is part of the protocol's deepest layer, not a per-port detail. The bare `media:void` parses successfully; any combination with another tag (marker or key=value) MUST fail with VoidNotAtomic. This forecloses a fake taxonomy of unit values; reasons or labels for *why* void is used belong on the cap URN's non-directional tags or in cap args. |
| TEST1820 | capdag/capdag-js | js | `test1820_specificityQuestionIsZero` | capdag.test.js:6487 | TEST1820: A `?`-valued cap-tag scores 0. Same as missing. |
| TEST1821 | capdag/capdag-js | js | `test1821_specificityMustNotHaveIsFive` | capdag.test.js:6497 | TEST1821: A `!`-valued cap-tag scores 5 (top of negative chain). |
| TEST1822 | capdag/capdag-js | js | `test1822_specificityMustHaveAnyIsTwo` | capdag.test.js:6504 | TEST1822: A `*`-valued cap-tag (including bare markers) scores 2. |
| TEST1823 | capdag/capdag-js | js | `test1823_specificityExactValueIsFour` | capdag.test.js:6518 | TEST1823: An exact-valued cap-tag scores 4. |
| TEST1824 | capdag/capdag-js | js | `test1824_specificityCombinedYAxis` | capdag.test.js:6525 | TEST1824: All six forms compose additively on a single cap. This pins the truth-table sum across the y axis as a whole. |
| TEST1830 | capdag/capdag-js | js | `test1830_canonicalizeNoConstraint` | capdag.test.js:6536 | TEST1830: ?x ≡ x? ≡ x=? all canonicalize to ?x. |
| TEST1831 | capdag/capdag-js | js | `test1831_canonicalizeAbsentOrNotValue` | capdag.test.js:6546 | TEST1831: ?x=v and x?=v both canonicalize to x?=v. The third hypothetical form `x=?v` is NOT recognized as a qualifier — a value starting with `?` is just an exact value beginning with a `?` character. |
| TEST1832 | capdag/capdag-js | js | `test1832_canonicalizeMustHaveAny` | capdag.test.js:6562 | TEST1832: x ≡ x=* both canonicalize to bare x. |
| TEST1833 | capdag/capdag-js | js | `test1833_canonicalizePresentNotValue` | capdag.test.js:6572 | TEST1833: !x=v and x!=v both canonicalize to x!=v. The third hypothetical form `x=!v` is NOT recognized as a qualifier — a value starting with `!` is just an exact value beginning with a `!` character. |
| TEST1834 | capdag/capdag-js | js | `test1834_canonicalizeExactValue` | capdag.test.js:6588 | TEST1834: x=v stays as x=v (the lone exact-value form). |
| TEST1835 | capdag/capdag-js | js | `test1835_canonicalizeMustNotHave` | capdag.test.js:6594 | TEST1835: !x ≡ x! ≡ x=! all canonicalize to !x. |
| TEST1842 | capdag/capdag-js | js | `test1842_truthTableFullCrossProduct` | capdag.test.js:6604 | TEST1842: Full 6×6 truth table. |
| TEST1845 | capdag/capdag-js | js | `test1845_axisWeightingInDominatesY` | capdag.test.js:6657 | TEST1845: With equal out-axis, in-axis dominates over y-axis. |
| TEST1848 | capdag/capdag-js | js | `test1848_capVersionNonZeroOnWire` | capdag.test.js:6691 | TEST1848: Cap with version=N round-trips with `version: N` on wire |
| TEST1849 | capdag/capdag-js | js | `test1849_resolveForHostCompatibleLatest` | capdag.test.js:2482 | TEST1849: latest version has a host build → Compatible, resolving to the latest version and that platform's native-format package. |
| TEST1850 | capdag/capdag-js | js | `test1850_resolveForHostCompatibleOutdated` | capdag.test.js:2498 | TEST1850: the latest version lacks a host build but an older version has one → CompatibleOutdated, resolving to the older version with a reason naming both the latest and the resolved version. |
| TEST1851 | capdag/capdag-js | js | `test1851_resolveForHostIncompatible` | capdag.test.js:2515 | TEST1851: no version ships a host build → Incompatible, no resolved version/package, reason states the host platform. |
| TEST1852 | capdag/capdag-js | js | `test1852_resolveForHostSkipsBuildWithNoInstaller` | capdag.test.js:2529 | TEST1852: a host build whose packages[] is empty AND has no legacy `package` ships no installer; resolution must SKIP it (not resolve to an un-downloadable version) and fall through to an older usable version. |
| TEST1853 | capdag/capdag-js | js | `test1853_hostPlatformNormalizedForm` | capdag.test.js:2547 | TEST1853: host_platform() returns a normalized {os}-{arch} string with arch aarch64 mapped to arm64 — the exact form the registry uses. |
| TEST1872 | capdag/capdag-js | js | `test1872_registryUrlFromBuildEnvPassesThroughNonempty` | capdag.test.js:2564 | TEST1872: a non-empty MFR_CARTRIDGE_REGISTRY_URL passes through verbatim — a published build reports exactly the URL it was compiled with. |
| TEST1873 | capdag/capdag-js | js | `test1873_registryUrlFromBuildEnvNoneForDev` | capdag.test.js:2571 | TEST1873: an unset env (null/undefined) yields null — a dev build has no baked registry and loads only `dev/` cartridges. |
| TEST1874 | capdag/capdag-js | js | `test1874_registryUrlFromBuildEnvRejectsEmptyString` | capdag.test.js:2577 | TEST1874: an exported-but-empty env (`Some("")`) is neither a dev build nor a valid identity and MUST fail hard at compile time, so the build can never silently hash the empty string into a fake registry slug. We assert the panic rather than letting a bogus empty primary registry ship. |
| TEST1880 | capdag/capdag-js | js | `test1880_aliasNameNormalizationRules` | capdag.test.js:6846 | TEST1880: alias name normalization lowercases and accepts the allowed character class; rejects colon, whitespace, and out-of-class chars with the right error. A broken validator would let a URN-shaped or whitespace name through, or mangle a valid name. |
| TEST1881 | capdag/capdag-js | js | `test1881_tokenUrnVsAliasDetection` | capdag.test.js:6858 | TEST1881: URN-vs-alias detection keys purely on the presence of ':'. The whole design rests on this discriminator being exact. |
| TEST1882 | capdag/capdag-js | js | `test1882_classifyAliasTargetByPrefix` | capdag.test.js:6867 | TEST1882: alias target classification distinguishes cap from media by prefix and rejects a non-URN target. The typed-boundary enforcement in the registry depends on this. |
| TEST1887 | capdag/capdag-js | js | `test1887_manifestSerdeRoundTripsAliases` | capdag.test.js:6876 | TEST1887: the Manifest type round-trips an `aliases` map. |
| TEST1894 | capdag/capdag-js | js | `test1894_selectDisplayAliasOrdering` | capdag.test.js:6895 | TEST1894: selectDisplayAlias picks the SHORTEST name, ties broken alphabetically. This is the deterministic ordering every aliased-display surface relies on; a regression here silently changes which alias the whole UI renders. |
| TEST1895 | capdag/capdag-js | js | `test1895_displayAliasForUrn` | capdag.test.js:6911 | TEST1895: displayAliasForUrn reverse-resolves a URN to its display alias. Proves: (1) the shortest-then-alphabetical winner among multiple aliases on the same target, (2) a NON-canonical query URN (different tag order) still resolves because the query is canonicalised before matching, (3) a URN with no alias returns null, (4) a non-URN string returns null. |
| TEST1896 | capdag/capdag-js | js | `test1896_cachedCapAliasesFiltersToCapTargets` | capdag.test.js:6938 | TEST1896: cachedCapAliases returns only CAP-targeted aliases as [name, target] pairs — media aliases are excluded. Drives the notation editor's registered-alias completions. |
| TEST1953 | capdag/capdag-js | js | `test1953_rule14StreamingOnlyOnMainInput` | capdag.test.js:3026 | TEST1953: RULE14 — `streaming: true` is accepted on the main input (the stdin arg equivalent to `in=`), survives the JSON round-trip, and is refused on any other argument: a side option has no wire stream, so it has nothing to consume incrementally, and the rule keeps the executor's hop rule one-dimensional. |
| TEST1964 | capdag/capdag-js | js | `test1964_unknownDefinitionFieldIsRefused` | capdag.test.js:3054 | TEST1964: a definition field this capdag does not know is a NEWER fabric, not noise — parsing refuses it, naming the key, for arguments and outputs alike. The field being dropped is how a cartridge built on an older capdag once advertised a `streaming` input as bounded. |
| TEST6201 | capdag/capdag-js | js | `test6201_emptyCapIsIllegal` | capdag.test.js:3086 | TEST6201: cap: (empty) is the illegal bare top form |
| TEST6204 | capdag/capdag-js | js | `test6204_Urn` | capdag.test.js:132 | TEST6204: Urn |
| TEST6206 | capdag/capdag-js | js | `test6206_CapFabAddCapPopulatesEdgesAndNodes` | capdag.test.js:1384 | Add a cap and check it becomes an edge with from/to nodes and carries the registry name we passed. This is exactly the shape the renderer depends on. |
| TEST6208 | capdag/capdag-js | js | `test6208_CapFabGetOutgoingConformsToMatching` | capdag.test.js:1402 | getOutgoing takes a concrete source URN and returns edges whose from_spec the source conforms to. It must NOT be a plain string lookup. |
| TEST6212 | capdag/capdag-js | js | `test6212_xv5InlineSpecRedefinitionDetected` | capdag.test.js:822 | TEST6212: XV5 - Test inline media def redefinition of existing registry spec is detected and rejected |
| TEST6216 | capdag/capdag-js | js | `test6216_xv5NewInlineSpecAllowed` | capdag.test.js:839 | TEST6216: XV5 - Test new inline media def (not in registry) is allowed |
| TEST6220 | capdag/capdag-js | js | `test6220_xv5EmptyMediaDefsAllowed` | capdag.test.js:854 | TEST6220: XV5 - Test empty media_defs (no inline specs) passes XV5 validation |
| TEST6224 | capdag/capdag-js | js | `test6224_CapFabDistinctRegistryNames` | capdag.test.js:1423 | Each edge must carry the registry name it was added with. This is how the renderer colours/groups edges by provenance in browse mode. |
| TEST6228 | capdag/capdag-js | js | `test6228_LlmGenerateTextUrnSpecs` | capdag.test.js:1632 | Mirror-specific coverage: llm_generate_text_urn input/output specs conform to MEDIA_STRING |
| TEST6232 | capdag/capdag-js | js | `test6232_JS_buildExtensionIndex` | capdag.test.js:1663 | These tests cover JS-specific functionality not in the Rust numbering scheme but are important for capdag-js correctness. |
| TEST6236 | capdag/capdag-js | js | `test6236_JS_mediaUrnsForExtension` | capdag.test.js:1680 | TEST6236: J s media urns for extension |
| TEST6240 | capdag/capdag-js | js | `test6240_JS_getExtensionMappings` | capdag.test.js:1709 | TEST6240: J s get extension mappings |
| TEST6242 | capdag/capdag-js | js | `test6242_JS_resolveMediaUrnFromSpecs` | capdag.test.js:1720 | TEST6242: J s resolve media urn from specs |
| TEST6246 | capdag/capdag-js | js | `test6246_JS_capJSONSerialization` | capdag.test.js:1733 | TEST6246: J s cap j s o n serialization |
| TEST6249 | capdag/capdag-js | js | `test6249_JS_capDocumentationRoundTrip` | capdag.test.js:1756 | JS round-trip for the documentation field on Cap. Mirrors TEST920 in capdag/src/cap/definition.rs — the body is non-trivial (newlines, backticks, embedded quotes, Unicode) so escaping mismatches between JSON.stringify on this side and the Rust serializer on the other side surface as failures here. |
| TEST6253 | capdag/capdag-js | js | `test6253_JS_capDocumentationOmittedWhenNull` | capdag.test.js:1778 | When documentation is null, toJSON must omit the field entirely. This matches the Rust serializer's skip-when-None semantics and the ObjC toDictionary behaviour. A regression where null is emitted as `documentation: null` would break the symmetric round-trip with Rust (which has no null sentinel) and pollute generated JSON. |
| TEST6257 | capdag/capdag-js | js | `test6257_JS_mediaDefDocumentationPropagatesThroughResolve` | capdag.test.js:1801 | Documentation propagates from a mediaDefs definition through resolveMediaUrn into the resolved MediaDef. Mirrors TEST924 on the Rust side. This is the path every UI consumer uses, so a break here makes the new field invisible everywhere downstream. |
| TEST6261 | capdag/capdag-js | js | `test6261_JS_stdinSourceKindConstants` | capdag.test.js:1832 | TEST6261: J s stdin source kind constants |
| TEST6265 | capdag/capdag-js | js | `test6265_JS_stdinSourceNullData` | capdag.test.js:1839 | TEST6265: J s stdin source null data |
| TEST6269 | capdag/capdag-js | js | `test6269_JS_mediaDefConstruction` | capdag.test.js:1847 | TEST6269: J s media def construction |
| TEST6272 | capdag/capdag-js | js | `test6272_isCollection` | capdag.test.js:2812 | Mirror-specific coverage: isCollection returns true when collection marker tag is present Mirror-specific coverage: N/A for JS (MEDIA_COLLECTION constants removed - no longer exists) |
| TEST6275 | capdag/capdag-js | js | `test6275_Machine_emptyInput` | capdag.test.js:3356 | --- Machine parser tests (mirrors parser.rs tests) --- |
| TEST6277 | capdag/capdag-js | js | `test6277_Machine_whitespaceOnly` | capdag.test.js:3361 | TEST6277: Machine whitespace only |
| TEST6279 | capdag/capdag-js | js | `test6279_Machine_headerOnlyNoWirings` | capdag.test.js:3366 | TEST6279: Machine header only no wirings |
| TEST6280 | capdag/capdag-js | js | `test6280_Machine_duplicateAlias` | capdag.test.js:3374 | TEST6280: Machine duplicate alias |
| TEST6282 | capdag/capdag-js | js | `test6282_resolveCustomMediaDef` | capdag.test.js:1041 | TEST6282: Test resolving a custom media URN from a registry-seeded media def |
| TEST6283 | capdag/capdag-js | js | `test6283_resolveCustomWithSchema` | capdag.test.js:1051 | TEST6283: Test resolving a custom record media def carrying a schema from a registry-seeded media def |
| TEST6286 | capdag/capdag-js | js | `test6286_Machine_simpleLinearChain` | capdag.test.js:3386 | TEST6286: Machine simple linear chain |
| TEST6288 | capdag/capdag-js | js | `test6288_Machine_twoStepChain` | capdag.test.js:3402 | TEST6288: Machine two step chain |
| TEST6290 | capdag/capdag-js | js | `test6290_Machine_fanOut` | capdag.test.js:3417 | TEST6290: Machine fan out |
| TEST6292 | capdag/capdag-js | js | `test6292_Machine_fanInSecondaryAssignedByPriorWiring` | capdag.test.js:3435 | TEST6292: Machine fan in secondary assigned by prior wiring |
| TEST6294 | capdag/capdag-js | js | `test6294_Machine_fanInSecondaryUnassignedGetsWildcard` | capdag.test.js:3449 | TEST6294: Machine fan in secondary unassigned gets wildcard |
| TEST6306 | capdag/capdag-js | js | `test6306_Machine_loopKeywordIsNotGrammar` | capdag.test.js:3464 | TEST6306: The retired LOOP keyword is no longer grammar. A wiring that still writes `LOOP <cap>` before the cap alias no longer parses — `LOOP` is now an ordinary alias, so `pages -> LOOP p2t -> texts` is two aliases in the cap position with no arrow between them, which is a syntax error. |
| TEST6308 | capdag/capdag-js | js | `test6308_Machine_undefinedAliasFails` | capdag.test.js:3482 | TEST6308: Machine undefined alias fails |
| TEST6310 | capdag/capdag-js | js | `test6310_Machine_nodeAliasCollision` | capdag.test.js:3490 | TEST6310: Machine node alias collision |
| TEST6312 | capdag/capdag-js | js | `test6312_Machine_conflictingMediaTypesFail` | capdag.test.js:3501 | TEST6312: Machine conflicting media types fail |
| TEST6315 | capdag/capdag-js | js | `test6315_Machine_multilineFormat` | capdag.test.js:3514 | TEST6315: Machine multiline format |
| TEST6318 | capdag/capdag-js | js | `test6318_Machine_differentAliasesSameGraph` | capdag.test.js:3525 | TEST6318: Machine different aliases same graph |
| TEST6321 | capdag/capdag-js | js | `test6321_Machine_malformedInputFails` | capdag.test.js:3538 | TEST6321: Machine malformed input fails |
| TEST6323 | capdag/capdag-js | js | `test6323_Machine_unterminatedBracketFails` | capdag.test.js:3546 | TEST6323: Machine unterminated bracket fails |
| TEST6327 | capdag/capdag-js | js | `test6327_Machine_lineBasedSimpleChain` | capdag.test.js:3555 | --- Machine parser line-based mode tests --- |
| TEST6331 | capdag/capdag-js | js | `test6331_Machine_lineBasedTwoStepChain` | capdag.test.js:3569 | TEST6331: Machine line based two step chain |
| TEST6334 | capdag/capdag-js | js | `test6334_Machine_lineBasedLoopKeywordIsNotGrammar` | capdag.test.js:3581 | TEST6334: The retired LOOP keyword is not grammar in line-based mode either — `pages -> LOOP p2t -> texts` is a syntax error, same as the bracketed form. |
| TEST6337 | capdag/capdag-js | js | `test6337_Machine_lineBasedFanIn` | capdag.test.js:3592 | TEST6337: Machine line based fan in |
| TEST6341 | capdag/capdag-js | js | `test6341_Machine_mixedBracketedAndLineBased` | capdag.test.js:3606 | TEST6341: Machine mixed bracketed and line based |
| TEST6345 | capdag/capdag-js | js | `test6345_Machine_lineBasedEquivalentToBracketed` | capdag.test.js:3615 | TEST6345: Machine line based equivalent to bracketed |
| TEST6349 | capdag/capdag-js | js | `test6349_Machine_lineBasedFormatSerialization` | capdag.test.js:3628 | TEST6349: Machine line based format serialization |
| TEST6353 | capdag/capdag-js | js | `test6353_Machine_lineBasedAndBracketedParseSameGraph` | capdag.test.js:3650 | TEST6353: Machine line based and bracketed parse same graph |
| TEST6357 | capdag/capdag-js | js | `test6357_Machine_edgeEquivalenceSameUrns` | capdag.test.js:3676 | --- Machine graph tests (mirrors graph.rs tests) --- |
| TEST6361 | capdag/capdag-js | js | `test6361_Machine_edgeEquivalenceDifferentCapUrns` | capdag.test.js:3693 | TEST6361: Machine edge equivalence different cap urns |
| TEST6365 | capdag/capdag-js | js | `test6365_Machine_edgeEquivalenceDifferentTargets` | capdag.test.js:3710 | TEST6365: Machine edge equivalence different targets |
| TEST6369 | capdag/capdag-js | js | `test6369_Machine_edgeEquivalenceDifferentLoopFlag` | capdag.test.js:3727 | TEST6369: Machine edge equivalence different loop flag |
| TEST6372 | capdag/capdag-js | js | `test6372_Machine_edgeEquivalenceSourceOrderIndependent` | capdag.test.js:3744 | TEST6372: Machine edge equivalence source order independent |
| TEST6375 | capdag/capdag-js | js | `test6375_Machine_edgeEquivalenceDifferentSourceCount` | capdag.test.js:3761 | TEST6375: Machine edge equivalence different source count |
| TEST6377 | capdag/capdag-js | js | `test6377_Machine_graphEquivalenceSameEdges` | capdag.test.js:3778 | TEST6377: Machine graph equivalence same edges |
| TEST6380 | capdag/capdag-js | js | `test6380_Machine_graphEquivalenceReorderedEdges` | capdag.test.js:3794 | TEST6380: Machine graph equivalence reordered edges |
| TEST6383 | capdag/capdag-js | js | `test6383_Machine_graphNotEquivalentDifferentEdgeCount` | capdag.test.js:3810 | TEST6383: Machine graph not equivalent different edge count |
| TEST6386 | capdag/capdag-js | js | `test6386_Machine_graphNotEquivalentDifferentCap` | capdag.test.js:3825 | TEST6386: Machine graph not equivalent different cap |
| TEST6389 | capdag/capdag-js | js | `test6389_Machine_graphEmpty` | capdag.test.js:3839 | TEST6389: Machine graph empty |
| TEST6392 | capdag/capdag-js | js | `test6392_Machine_graphEmptyEquivalence` | capdag.test.js:3846 | TEST6392: Machine graph empty equivalence |
| TEST6395 | capdag/capdag-js | js | `test6395_Machine_rootSourcesLinearChain` | capdag.test.js:3853 | TEST6395: Machine root sources linear chain |
| TEST6397 | capdag/capdag-js | js | `test6397_Machine_leafTargetsLinearChain` | capdag.test.js:3868 | TEST6397: Machine leaf targets linear chain |
| TEST6398 | capdag/capdag-js | js | `test6398_Machine_rootSourcesFanIn` | capdag.test.js:3883 | TEST6398: Machine root sources fan in |
| TEST6400 | capdag/capdag-js | js | `test6400_Machine_displayEdge` | capdag.test.js:3896 | TEST6400: Machine display edge |
| TEST6402 | capdag/capdag-js | js | `test6402_Machine_displayGraph` | capdag.test.js:3908 | TEST6402: Machine display graph |
| TEST6404 | capdag/capdag-js | js | `test6404_Machine_serializeSingleEdge` | capdag.test.js:3921 | --- Machine serializer tests (mirrors serializer.rs tests) --- |
| TEST6406 | capdag/capdag-js | js | `test6406_Machine_serializeTwoEdgeChain` | capdag.test.js:3937 | TEST6406: Machine serialize two edge chain |
| TEST6408 | capdag/capdag-js | js | `test6408_Machine_serializeEmptyGraph` | capdag.test.js:3951 | TEST6408: Machine serialize empty graph |
| TEST6410 | capdag/capdag-js | js | `test6410_Machine_roundtripSingleEdge` | capdag.test.js:3956 | TEST6410: Machine roundtrip single edge |
| TEST6413 | capdag/capdag-js | js | `test6413_Machine_roundtripTwoEdgeChain` | capdag.test.js:3970 | TEST6413: Machine roundtrip two edge chain |
| TEST6415 | capdag/capdag-js | js | `test6415_Machine_roundtripFanOut` | capdag.test.js:3985 | TEST6415: Machine roundtrip fan out |
| TEST6417 | capdag/capdag-js | js | `test6417_Machine_loopEdgeSerializesWithoutLoopText` | capdag.test.js:4005 | TEST6417: A per-item map (`is_loop`) edge serializes WITHOUT any LOOP marker — `is_loop` is a derived cardinality property, not authored notation text. The pure-JS parse path has no cap definitions to re-derive cardinality, so the reparsed edge has `isLoop === false`; editors get the derived value from the engine, not from re-parsing. |
| TEST6419 | capdag/capdag-js | js | `test6419_Machine_serializationIsDeterministic` | capdag.test.js:4027 | TEST6419: Machine serialization is deterministic |
| TEST6421 | capdag/capdag-js | js | `test6421_Machine_reorderedEdgesProduceSameNotation` | capdag.test.js:4041 | TEST6421: Machine reordered edges produce same notation |
| TEST6429 | capdag/capdag-js | js | `test6429_Machine_multilineSerializeFormat` | capdag.test.js:4058 | TEST6429: Machine multiline serialize format |
| TEST6432 | capdag/capdag-js | js | `test6432_Machine_aliasFromOpTag` | capdag.test.js:4074 | Aliases are pure-index `edge_<N>` regardless of the cap's tags; there is no privileged `op` tag to derive a friendlier name from. |
| TEST6434 | capdag/capdag-js | js | `test6434_Machine_aliasFallbackWithoutOpTag` | capdag.test.js:4086 | TEST6434: Machine alias fallback without op tag |
| TEST6436 | capdag/capdag-js | js | `test6436_Machine_duplicateOpTagsDisambiguated` | capdag.test.js:4098 | Pure-index aliases inherently disambiguate edges that share a marker tag. |
| TEST6437 | capdag/capdag-js | js | `test6437_Machine_builderSingleEdge` | capdag.test.js:4120 | --- Machine builder tests --- |
| TEST6438 | capdag/capdag-js | js | `test6438_Machine_builderWithLoop` | capdag.test.js:4133 | TEST6438: Machine builder with loop |
| TEST6439 | capdag/capdag-js | js | `test6439_Machine_builderChaining` | capdag.test.js:4146 | TEST6439: Machine builder chaining |
| TEST6440 | capdag/capdag-js | js | `test6440_Machine_builderEquivalentToParsed` | capdag.test.js:4155 | TEST6440: Machine builder equivalent to parsed |
| TEST6442 | capdag/capdag-js | js | `test6442_Machine_builderRoundTrip` | capdag.test.js:4168 | TEST6442: Machine builder round trip |
| TEST6444 | capdag/capdag-js | js | `test6444_Machine_capUrnIsEquivalent` | capdag.test.js:4180 | --- CapUrn.isEquivalent/isComparable tests --- |
| TEST6446 | capdag/capdag-js | js | `test6446_Machine_capUrnIsComparable` | capdag.test.js:4189 | TEST6446: Machine cap urn is comparable |
| TEST6448 | capdag/capdag-js | js | `test6448_Machine_capUrnInMediaUrn` | capdag.test.js:4197 | TEST6448: Machine cap urn in media urn |
| TEST6449 | capdag/capdag-js | js | `test6449_Machine_capUrnOutMediaUrn` | capdag.test.js:4205 | TEST6449: Machine cap urn out media urn |
| TEST6450 | capdag/capdag-js | js | `test6450_Machine_mediaUrnIsEquivalent` | capdag.test.js:4214 | --- MediaUrn.isEquivalent/isComparable tests --- |
| TEST6451 | capdag/capdag-js | js | `test6451_Machine_mediaUrnIsComparable` | capdag.test.js:4223 | TEST6451: Machine media urn is comparable |
| TEST6452 | capdag/capdag-js | js | `test6452_Machine_parseMachineWithAST_headerLocation` | capdag.test.js:4236 | Phase 0A: Position tracking tests |
| TEST6453 | capdag/capdag-js | js | `test6453_Machine_parseMachineWithAST_wiringLocation` | capdag.test.js:4253 | TEST6453: Machine parse machine with a s t wiring location |
| TEST6454 | capdag/capdag-js | js | `test6454_Machine_parseMachineWithAST_multilinePositions` | capdag.test.js:4268 | TEST6454: Machine parse machine with a s t multiline positions |
| TEST6455 | capdag/capdag-js | js | `test6455_Machine_parseMachineWithAST_fanInSourceLocations` | capdag.test.js:4278 | TEST6455: Machine parse machine with a s t fan in source locations |
| TEST6456 | capdag/capdag-js | js | `test6456_Machine_parseMachineWithAST_aliasMap` | capdag.test.js:4290 | TEST6456: Machine parse machine with a s t alias map |
| TEST6457 | capdag/capdag-js | js | `test6457_Machine_parseMachineWithAST_nodeMedia` | capdag.test.js:4309 | TEST6457: Machine parse machine with a s t node media |
| TEST6458 | capdag/capdag-js | js | `test6458_Machine_errorLocation_parseError` | capdag.test.js:4322 | TEST6458: Machine error location parse error |
| TEST6459 | capdag/capdag-js | js | `test6459_Machine_errorLocation_duplicateAlias` | capdag.test.js:4333 | TEST6459: Machine error location duplicate alias |
| TEST6460 | capdag/capdag-js | js | `test6460_Machine_errorLocation_undefinedAlias` | capdag.test.js:4348 | TEST6460: Machine error location undefined alias |
| TEST6462 | capdag/capdag-js | js | `test6462_Machine_toMermaid_linearChain` | capdag.test.js:4362 | Phase 0C: Machine.toMermaid() tests |
| TEST6463 | capdag/capdag-js | js | `test6463_Machine_toMermaid_loopEdge` | capdag.test.js:4384 | TEST6463: Mermaid renders a per-item map (`is_loop`) edge with a dotted line — `is_loop` is a kept render property — but emits NO "LOOP" text, since that keyword is retired. The loop edge is built programmatically because the grammar no longer has any way to author one. |
| TEST6464 | capdag/capdag-js | js | `test6464_Machine_toMermaid_emptyGraph` | capdag.test.js:4398 | TEST6464: Machine to mermaid empty graph |
| TEST6465 | capdag/capdag-js | js | `test6465_Machine_toMermaid_fanIn` | capdag.test.js:4405 | TEST6465: Machine to mermaid fan in |
| TEST6466 | capdag/capdag-js | js | `test6466_Machine_toMermaid_fanOut` | capdag.test.js:4417 | TEST6466: Machine to mermaid fan out |
| TEST6467 | capdag/capdag-js | js | `test6467_Machine_capRegistryEntry_construction` | capdag.test.js:4437 | Phase 0B: FabricRegistryClient tests |
| TEST6468 | capdag/capdag-js | js | `test6468_Machine_mediaRegistryEntry_construction` | capdag.test.js:4461 | TEST6468: Machine media registry entry construction |
| TEST6469 | capdag/capdag-js | js | `test6469_Machine_capRegistryClient_construction` | capdag.test.js:4475 | TEST6469: Machine cap registry client construction |
| TEST6470 | capdag/capdag-js | js | `test6470_Machine_capRegistryEntry_defaults` | capdag.test.js:4483 | TEST6470: Machine cap registry entry defaults |
| TEST6471 | capdag/capdag-js | js | `test6471_Renderer_cardinalityLabel_allFourCases` | capdag.test.js:4549 | TEST6471: Renderer cardinality label all four cases |
| TEST6472 | capdag/capdag-js | js | `test6472_Renderer_cardinalityLabel_usesUnicodeArrow` | capdag.test.js:4557 | TEST6472: Renderer cardinality label uses unicode arrow |
| TEST6473 | capdag/capdag-js | js | `test6473_Renderer_cardinalityFromCap_findsStdinArgNotFirstArg` | capdag.test.js:4566 | TEST6473: Renderer cardinality from cap finds stdin arg not first arg |
| TEST6474 | capdag/capdag-js | js | `test6474_Renderer_cardinalityFromCap_scalarDefaultsWhenFieldsMissing` | capdag.test.js:4591 | TEST6474: Renderer cardinality from cap scalar defaults when fields missing |
| TEST6475 | capdag/capdag-js | js | `test6475_Renderer_cardinalityFromCap_outputOnlySequence` | capdag.test.js:4600 | TEST6475: Renderer cardinality from cap output only sequence |
| TEST6476 | capdag/capdag-js | js | `test6476_Renderer_cardinalityFromCap_rejectsStringIsSequence` | capdag.test.js:4612 | TEST6476: Renderer cardinality from cap rejects string is sequence |
| TEST6478 | capdag/capdag-js | js | `test6478_Renderer_cardinalityFromCap_throwsOnNonObject` | capdag.test.js:4626 | TEST6478: Renderer cardinality from cap throws on non object |
| TEST6479 | capdag/capdag-js | js | `test6479_Renderer_canonicalMediaUrn_normalizesTagOrder` | capdag.test.js:4646 | TEST6479: Renderer canonical media urn normalizes tag order |
| TEST6480 | capdag/capdag-js | js | `test6480_Renderer_canonicalMediaUrn_preservesValueTags` | capdag.test.js:4656 | TEST6480: Renderer canonical media urn preserves value tags |
| TEST6481 | capdag/capdag-js | js | `test6481_Renderer_canonicalMediaUrn_rejectsCapUrn` | capdag.test.js:4662 | TEST6481: Renderer canonical media urn rejects cap urn |
| TEST6482 | capdag/capdag-js | js | `test6482_Renderer_mediaNodeLabel_rejectsUrnDerivedLabels` | capdag.test.js:4675 | TEST6482: Renderer media node label rejects urn derived labels |
| TEST6483 | capdag/capdag-js | js | `test6483_Renderer_buildBrowseGraphData_rejectsMissingMediaTitles` | capdag.test.js:4690 | TEST6483: Renderer build browse graph data rejects missing media titles |
| TEST6484 | capdag/capdag-js | js | `test6484_Renderer_validateStrandStep_rejectsUnknownVariant` | capdag.test.js:4780 | TEST6484: Renderer validate strand step rejects unknown variant |
| TEST6486 | capdag/capdag-js | js | `test6486_Renderer_validateStrandStep_requiresBooleanIsSequence` | capdag.test.js:4799 | TEST6486: Renderer validate strand step requires boolean is sequence |
| TEST6487 | capdag/capdag-js | js | `test6487_Renderer_classifyStrandCapSteps_capFlags` | capdag.test.js:4823 | TEST6487: Renderer classify strand cap steps cap flags |
| TEST6488 | capdag/capdag-js | js | `test6488_Renderer_classifyStrandCapSteps_nestedForks` | capdag.test.js:4845 | TEST6488: Renderer classify strand cap steps nested forks |
| TEST6489 | capdag/capdag-js | js | `test6489_Renderer_buildStrandGraphData_singleCapPlain` | capdag.test.js:4876 | TEST6489: Renderer build strand graph data single cap plain |
| TEST6491 | capdag/capdag-js | js | `test6491_Renderer_buildStrandGraphData_sequenceShowsCardinality` | capdag.test.js:4904 | TEST6491: Renderer build strand graph data sequence shows cardinality |
| TEST6492 | capdag/capdag-js | js | `test6492_Renderer_buildStrandGraphData_foreachCollectSpan` | capdag.test.js:4925 | TEST6492: Renderer build strand graph data foreach collect span |
| TEST6493 | capdag/capdag-js | js | `test6493_Renderer_buildStrandGraphData_standaloneCollect` | capdag.test.js:4977 | TEST6493: Renderer build strand graph data standalone collect |
| TEST6494 | capdag/capdag-js | js | `test6494_Renderer_buildStrandGraphData_unclosedForEachBody` | capdag.test.js:5005 | TEST6494: Renderer build strand graph data unclosed for each body |
| TEST6495 | capdag/capdag-js | js | `test6495_Renderer_buildStrandGraphData_nestedForEachThrows` | capdag.test.js:5043 | TEST6495: Renderer build strand graph data nested for each throws |
| TEST6496 | capdag/capdag-js | js | `test6496_Renderer_collapseStrand_singleCapBodyKeepsCapOwnLabel` | capdag.test.js:5072 | TEST6496: Renderer collapse strand single cap body keeps cap own label |
| TEST6497 | capdag/capdag-js | js | `test6497_Renderer_collapseStrand_unclosedForEachBodyCollapses` | capdag.test.js:5125 | TEST6497: Renderer collapse strand unclosed for each body collapses |
| TEST6498 | capdag/capdag-js | js | `test6498_Renderer_collapseStrand_standaloneCollectCollapses` | capdag.test.js:5182 | TEST6498: Renderer collapse strand standalone collect collapses |
| TEST6499 | capdag/capdag-js | js | `test6499_Renderer_collapseStrand_sequenceProducingCapBeforeForeach` | capdag.test.js:5226 | TEST6499: Renderer collapse strand sequence producing cap before foreach |
| TEST6500 | capdag/capdag-js | js | `test6500_Renderer_collapseStrand_plainCapMergesTrailingOutput` | capdag.test.js:5291 | TEST6500: Renderer collapse strand plain cap merges trailing output |
| TEST6501 | capdag/capdag-js | js | `test6501_Renderer_collapseStrand_plainCapDistinctTargetNoMerge` | capdag.test.js:5328 | TEST6501: Renderer collapse strand plain cap distinct target no merge |
| TEST6502 | capdag/capdag-js | js | `test6502_Renderer_validateStrandPayload_missingSourceMediaUrn` | capdag.test.js:5355 | TEST6502: Renderer validate strand payload missing source media urn |
| TEST6503 | capdag/capdag-js | js | `test6503_Renderer_validateBodyOutcome_rejectsNegativeIndex` | capdag.test.js:5411 | ---------------- run builder ---------------- |
| TEST6504 | capdag/capdag-js | js | `test6504_Renderer_buildRunGraphData_pagesSuccessesAndFailures` | capdag.test.js:5530 | TEST6504: Renderer build run graph data pages successes and failures |
| TEST6505 | capdag/capdag-js | js | `test6505_Renderer_buildRunGraphData_unattributedFailureStopsAtEntry` | capdag.test.js:5603 | TEST6505: Renderer run graph keeps an unattributed body failure at its entry |
| TEST6506 | capdag/capdag-js | js | `test6506_Renderer_buildRunGraphData_resolvesExactFailedStepToken` | capdag.test.js:5641 | TEST6506: Renderer run graph resolves a failure by exact stable step token |
| TEST6507 | capdag/capdag-js | js | `test6507_Renderer_buildRunGraphData_backboneHasNoForeachNode` | capdag.test.js:5708 | TEST6507: Renderer build run graph data backbone has no foreach node |
| TEST6508 | capdag/capdag-js | js | `test6508_Renderer_buildRunGraphData_allFailedDropsTargetPlaceholder` | capdag.test.js:5763 | TEST6508: Renderer build run graph data all failed drops target placeholder |
| TEST6509 | capdag/capdag-js | js | `test6509_Renderer_buildRunGraphData_unclosedForeachSuccessNoMerge` | capdag.test.js:5828 | TEST6509: Renderer build run graph data unclosed foreach success no merge |
| TEST6510 | capdag/capdag-js | js | `test6510_Renderer_buildRunGraphData_closedForeachSuccessMergesAtCollectTarget` | capdag.test.js:5890 | TEST6510: Renderer build run graph data closed foreach success merges at collect target |
| TEST6511 | capdag/capdag-js | js | `test6511_Renderer_validateEditorGraphPayload_rejectsUnknownKind` | capdag.test.js:5945 | ---------------- editor-graph builder ---------------- |
| TEST6512 | capdag/capdag-js | js | `test6512_Renderer_buildEditorGraphData_collapsesCapsIntoLabeledEdges` | capdag.test.js:5960 | TEST6512: Renderer build editor graph data collapses caps into labeled edges |
| TEST6513 | capdag/capdag-js | js | `test6513_Renderer_buildEditorGraphData_loopMarkedEdgeGetsLoopClass` | capdag.test.js:5999 | TEST6513: Renderer build editor graph data loop marked edge gets loop class |
| TEST6514 | capdag/capdag-js | js | `test6514_Renderer_buildEditorGraphData_cardinalityFromDataSlotSequenceFlags` | capdag.test.js:6018 | TEST6514: Renderer build editor graph data cardinality from data slot sequence flags |
| TEST6515 | capdag/capdag-js | js | `test6515_Renderer_buildEditorGraphData_capWithoutCompleteArgsIsDropped` | capdag.test.js:6038 | TEST6515: Renderer build editor graph data cap without complete args is dropped |
| TEST6516 | capdag/capdag-js | js | `test6516_Renderer_buildEditorGraphData_rejectsEdgeWithMissingSource` | capdag.test.js:6056 | TEST6516: Renderer build editor graph data rejects edge with missing source |
| TEST6517 | capdag/capdag-js | js | `test6517_Renderer_buildResolvedMachineGraphData_singleStrandLinearChain` | capdag.test.js:6072 | ---------------- resolved-machine builder ---------------- |
| TEST6518 | capdag/capdag-js | js | `test6518_Renderer_buildResolvedMachineGraphData_loopEdgeGetsLoopClass` | capdag.test.js:6131 | TEST6518: Renderer build resolved machine graph data loop edge gets loop class |
| TEST6519 | capdag/capdag-js | js | `test6519_Renderer_buildResolvedMachineGraphData_fanInProducesEdgePerAssignment` | capdag.test.js:6166 | TEST6519: Renderer build resolved machine graph data fan in produces edge per assignment |
| TEST6520 | capdag/capdag-js | js | `test6520_Renderer_buildResolvedMachineGraphData_multiStrandKeepsStrandsDisjoint` | capdag.test.js:6207 | TEST6520: Renderer build resolved machine graph data multi strand keeps strands disjoint |
| TEST6521 | capdag/capdag-js | js | `test6521_Renderer_buildResolvedMachineGraphData_duplicateNodeIdAcrossStrandsFailsHard` | capdag.test.js:6270 | TEST6521: Renderer build resolved machine graph data duplicate node id across strands fails hard |
| TEST6522 | capdag/capdag-js | js | `test6522_Renderer_validateResolvedMachinePayload_rejectsMissingFields` | capdag.test.js:6306 | TEST6522: Renderer validate resolved machine payload rejects missing fields |
| TEST6544 | capdag/capdag-js | js | `test6544_builderRejectsStructuralKeys` | capdag.test.js:2963 | TEST6544: builder rejects structural keys on tag/marker |
| TEST6620 | capdag/capdag-js | js | `test6620_wildcardGenericFormsRejected` | capdag.test.js:3192 | TEST6620: Generic top-to-top spellings are all rejected. |
| TEST6621 | capdag/capdag-js | js | `test6621_capIdentityConstantWorks` | capdag.test.js:3213 | TEST6621: CAP_IDENTITY constant names the true identity cap, not bare cap: |
| TEST6734 | capdag/capdag-js | js | `test6734_rejectInvalidCombinations` | capdag.test.js:6632 | TEST6734: Invalid qualifier combinations must be rejected. |
| TEST6735 | capdag/capdag-js | js | `test6735_axisWeightingOutDominates` | capdag.test.js:6647 | TEST6735: out-axis difference dominates combined in+y differences. |
| TEST6736 | capdag/capdag-js | js | `test6736_axisWeightingDecodedLayout` | capdag.test.js:6667 | TEST6736: Decoded layout — 10000*out + 100*in + y. |
| TEST6737 | capdag/capdag-js | js | `test6737_capVersionZeroOmittedOnWire` | capdag.test.js:6679 | TEST6737: Cap with version=0 round-trips with no `version` key on wire |
| TEST7100 | capdag/capdag-js | js | `test7100_streamUrnReturnsStdinSourceUrnWhenItDiffersFromSlotUrn` | capdag.test.js:6708 | TEST7100: streamUrn() returns the stdin source's URN when it differs from the declared slot media_urn — the stdin URN, not the slot URN, is what the runtime demuxes the arg's input stream by. |
| TEST7101 | capdag/capdag-js | js | `test7101_streamUrnFallsBackToDeclaredMediaUrnWithoutStdinSource` | capdag.test.js:6721 | TEST7101: streamUrn() falls back to the declared slot media_urn when the arg declares no stdin source — a producer-fed arg may be delivered by its declared URN without ever appearing on stdin. |
| TEST7102 | capdag/capdag-js | js | `test7102_isMainInputTrueOnTagOrderInsensitiveEquivalenceToInSpec` | capdag.test.js:6732 | TEST7102: isMainInput() is true when the stdin URN is order-theoretically EQUIVALENT to the cap's in= spec even when the two strings list their tags in a different order — the comparison is the MediaUrn equivalence predicate, never a string comparison. |
| TEST7103 | capdag/capdag-js | js | `test7103_isMainInputFalseWithoutEquivalentStdinSource` | capdag.test.js:6748 | TEST7103: isMainInput() is false for cli_flag-only and position-only args (no stdin source means never the main input, whatever the declared slot URN says), and false when the stdin URN is not equivalent to in=. |
| TEST7104 | capdag/capdag-js | js | `test7104_multiArgCapExactlyOneMainInputAndPartitionOfRest` | capdag.test.js:6775 | TEST7104: A realistic multi-arg cap (one stdin main input; one required, defaultless cli_flag arg; several defaulted cli_flag args): exactly one arg is the main input, and partitioning the remaining args by required-without-default vs has-default yields the expected sets. |
| TEST7120 | capdag/capdag-js | js | `test7120_Renderer_validateStrandPayload_requiresAuthoritativeInputs` | capdag.test.js:5367 | TEST7120: Renderer requires the authoritative cap input graph |
| TEST7121 | capdag/capdag-js | js | `test7121_Renderer_validateBodyOutcome_requiresExplicitFailureCoordinate` | capdag.test.js:5422 | TEST7121: Renderer body outcomes require an explicit stable failure coordinate |
| TEST7122 | capdag/capdag-js | js | `test7122_Renderer_validateRunPayload_requiresForEachRegionCoordinate` | capdag.test.js:5483 | TEST7122: Renderer body outcomes reject execution-region tokens for non-ForEach steps |
| TEST8121 | capdag/capdag-js | js | `test8121_effectConformanceDeclaredAsymmetry` | capdag.test.js:3269 | TEST8121: isConformantRuntimeOutput — effect=declared accepts a more specific emission, rejects a more generic one |
| TEST8122 | capdag/capdag-js | js | `test8122_effectConformanceNoneRequiresEquivalence` | capdag.test.js:3293 | TEST8122: isConformantRuntimeOutput — effect=none requires the emission to be tag-equivalent to the runtime input; MORE specific is still a lie |
| TEST8123 | capdag/capdag-js | js | `test8123_effectConformancePatchRequiresPatchedInput` | capdag.test.js:3321 | TEST8123: isConformantRuntimeOutput — effect=patch requires exactly the delta-patched input type |

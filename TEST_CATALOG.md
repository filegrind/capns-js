# JS Test Catalog

**Total Tests:** 344

**Numbered Tests:** 344

**Unnumbered Tests:** 0

**Numbered Tests Missing Descriptions:** 0

**Numbering Mismatches:** 0

All numbered test numbers are unique.

This catalog lists all tests in the JS codebase.

| Test # | Function Name | Description | File |
|--------|---------------|-------------|------|
| test001 | `test001_capUrnCreation` | TEST001: Test that cap URN is created with tags parsed correctly and direction specs accessible | capdag.test.js:140 |
| test002 | `test002_directionSpecsRequired` | TEST002: Test that missing 'in' or 'out' defaults to media: wildcard | capdag.test.js:150 |
| test003 | `test003_directionMatching` | TEST003: Test that direction specs must match exactly, different in/out types don't match, wildcard matches any | capdag.test.js:161 |
| test004 | `test004_unquotedValuesLowercased` | TEST004: Test that unquoted keys and values are normalized to lowercase. Key lookup is case-insensitive: uppercase variants of `ext` resolve to the same keyed tag. | capdag.test.js:178 |
| test005 | `test005_quotedValuesPreserveCase` | TEST005: Test that quoted values preserve case while unquoted are lowercased | capdag.test.js:186 |
| test006 | `test006_quotedValueSpecialChars` | TEST006: Test that quoted values can contain special characters (semicolons, equals, spaces) | capdag.test.js:192 |
| test007 | `test007_quotedValueEscapeSequences` | TEST007: Test that escape sequences in quoted values (\" and \\) are parsed correctly | capdag.test.js:198 |
| test008 | `test008_mixedQuotedUnquoted` | TEST008: Test that mixed quoted and unquoted values in same URN parse correctly | capdag.test.js:205 |
| test009 | `test009_unterminatedQuoteError` | TEST009: Test that unterminated quote produces UnterminatedQuote error | capdag.test.js:212 |
| test010 | `test010_invalidEscapeSequenceError` | TEST010: Test that invalid escape sequences (like \n, \x) produce InvalidEscapeSequence error | capdag.test.js:225 |
| test011 | `test011_serializationSmartQuoting` | TEST011: Test that serialization uses smart quoting (no quotes for simple lowercase, quotes for special chars/uppercase) | capdag.test.js:239 |
| test012 | `test012_roundTripSimple` | TEST012: Test that simple cap URN round-trips (parse -> serialize -> parse equals original) | capdag.test.js:248 |
| test013 | `test013_roundTripQuoted` | TEST013: Test that quoted values round-trip preserving case and spaces | capdag.test.js:256 |
| test014 | `test014_roundTripEscapes` | TEST014: Test that escape sequences round-trip correctly | capdag.test.js:265 |
| test015 | `test015_capPrefixRequired` | TEST015: Test that cap: prefix is required and case-insensitive | capdag.test.js:275 |
| test016 | `test016_trailingSemicolonEquivalence` | TEST016: Test that trailing semicolon is equivalent (same hash, same string, matches) | capdag.test.js:287 |
| test017 | `test017_tagMatching` | TEST017: Test tag matching: exact match, subset match, wildcard match, value mismatch | capdag.test.js:332 |
| test018 | `test018_matchingCaseSensitiveValues` | TEST018: Test that quoted values with different case do NOT match (case-sensitive) | capdag.test.js:356 |
| test019 | `test019_missingTagHandling` | TEST019: Missing tag in instance causes rejection — pattern's tags are constraints | capdag.test.js:363 |
| test020 | `test020_specificity` | TEST020: Specificity is the sum of per-tag truth-table scores across in/out/y. Marker tags (bare segments and `key=*`) score 2 (must-have-any), exact `key=value` tags score 3, missing/`?` score 0, `!` scores 1. test0051_Urn() builds "cap:in=media:void;out=media:record;<tags>" so the directional baseline is: in:  media:void   -> {void=*}    -> 2 out: media:record -> {record=*}  -> 2 Total directional baseline: 4. | capdag.test.js:385 |
| test021 | `test021_builder` | TEST021: Test builder creates cap URN with marker + keyed tags and direction specs. `op` is no longer a special key — operation names are markers (value-less tags). | capdag.test.js:414 |
| test022 | `test022_builderRequiresDirection` | TEST022: Test builder requires both in_spec and out_spec | capdag.test.js:428 |
| test023 | `test023_builderPreservesCase` | TEST023: Test builder lowercases keys but preserves value case | capdag.test.js:442 |
| test024 | `test024_compatibility` | TEST024: Directional accepts — pattern's tags are constraints, instance must satisfy | capdag.test.js:453 |
| test025 | `test025_bestMatch` | TEST025: Test find_best_match returns most specific matching cap | capdag.test.js:473 |
| test026 | `test026_mergeAndSubset` | TEST026: Test merge combines tags from both caps, subset keeps only specified tags | capdag.test.js:486 |
| test027 | `test027_wildcardTag` | TEST027: Test with_wildcard_tag sets tag to wildcard, including in/out | capdag.test.js:505 |
| test028 | `test028_emptyCapUrnNotAllowed` | TEST028: Test empty cap URN is illegal | capdag.test.js:518 |
| test029 | `test029_minimalCapUrn` | TEST029: Test minimal valid cap URN has just in and out, empty tags | capdag.test.js:527 |
| test030 | `test030_extendedCharacterSupport` | TEST030: Test extended characters (forward slashes, colons) in tag values | capdag.test.js:535 |
| test031 | `test031_wildcardRestrictions` | TEST031: Test wildcard rejected in keys but accepted in values | capdag.test.js:542 |
| test032 | `test032_duplicateKeyRejection` | TEST032: Test duplicate keys are rejected with DuplicateKey error | capdag.test.js:560 |
| test033 | `test033_numericKeyRestriction` | TEST033: Test pure numeric keys rejected, mixed alphanumeric allowed, numeric values allowed | capdag.test.js:569 |
| test034 | `test034_emptyValueError` | TEST034: Test empty values are rejected | capdag.test.js:583 |
| test035 | `test035_hasTagCaseSensitive` | TEST035: Test has_tag is case-sensitive for values, case-insensitive for keys, works for in/out | capdag.test.js:596 |
| test036 | `test036_withTagPreservesValue` | TEST036: Test with_tag preserves value case | capdag.test.js:608 |
| test037 | `test037_withTagRejectsEmptyValue` | TEST037: Test with_tag rejects empty value | capdag.test.js:615 |
| test038 | `test038_semanticEquivalence` | TEST038: Test semantic equivalence of unquoted and quoted simple lowercase values | capdag.test.js:625 |
| test039 | `test039_getTagReturnsDirectionSpecs` | TEST039: Test get_tag returns direction specs (in/out) with case-insensitive lookup | capdag.test.js:633 |
| test040 | `test040_matchingSemanticsExactMatch` | TEST040: Matching semantics - exact match succeeds | capdag.test.js:642 |
| test041 | `test041_matchingSemanticsCapMissingTag` | TEST041: Matching semantics - cap missing tag matches (implicit wildcard) | capdag.test.js:649 |
| test042 | `test042_matchingSemanticsCapHasExtraTag` | TEST042: Pattern rejects instance missing required tags | capdag.test.js:657 |
| test043 | `test043_matchingSemanticsRequestHasWildcard` | TEST043: Matching semantics - request wildcard matches specific cap value | capdag.test.js:665 |
| test044 | `test044_matchingSemanticsCapHasWildcard` | TEST044: Matching semantics - cap wildcard matches specific request value | capdag.test.js:672 |
| test045 | `test045_matchingSemanticsValueMismatch` | TEST045: Matching semantics - value mismatch does not match | capdag.test.js:679 |
| test046 | `test046_matchingSemanticsFallbackPattern` | TEST046: Matching semantics - fallback pattern (cap missing tag = implicit wildcard) | capdag.test.js:686 |
| test047 | `test047_matchingSemanticsThumbnailVoidInput` | TEST047: Matching semantics - thumbnail fallback with void input | capdag.test.js:694 |
| test048 | `test048_matchingSemanticsWildcardDirection` | TEST048: Matching semantics - wildcard direction matches anything | capdag.test.js:701 |
| test049 | `test049_matchingSemanticsCrossDimension` | TEST049: Non-overlapping tags — neither direction accepts | capdag.test.js:708 |
| test050 | `test050_matchingSemanticsDirectionMismatch` | TEST050: Matching semantics - direction mismatch prevents matching | capdag.test.js:716 |
| test0051 | `test0051_Urn` | TEST0051: Urn | capdag.test.js:115 |
| test0052 | `test0052_CapFabAddCapPopulatesEdgesAndNodes` | Add a cap and check it becomes an edge with from/to nodes and carries the registry name we passed. This is exactly the shape the renderer depends on. | capdag.test.js:1384 |
| test0053 | `test0053_CapFabGetOutgoingConformsToMatching` | getOutgoing takes a concrete source URN and returns edges whose from_spec the source conforms to. It must NOT be a plain string lookup. | capdag.test.js:1402 |
| test054 | `test054_xv5InlineSpecRedefinitionDetected` | TEST054: XV5 - Test inline media def redefinition of existing registry spec is detected and rejected | capdag.test.js:820 |
| test055 | `test055_xv5NewInlineSpecAllowed` | TEST055: XV5 - Test new inline media def (not in registry) is allowed | capdag.test.js:837 |
| test056 | `test056_xv5EmptyMediaDefsAllowed` | TEST056: XV5 - Test empty media_defs (no inline specs) passes XV5 validation | capdag.test.js:852 |
| test0057 | `test0057_CapFabDistinctRegistryNames` | Each edge must carry the registry name it was added with. This is how the renderer colours/groups edges by provenance in browse mode. | capdag.test.js:1423 |
| test0058 | `test0058_LlmGenerateTextUrnSpecs` | Mirror-specific coverage: llm_generate_text_urn input/output specs conform to MEDIA_STRING | capdag.test.js:1632 |
| test0059 | `test0059_JS_buildExtensionIndex` | These tests cover JS-specific functionality not in the Rust numbering scheme but are important for capdag-js correctness. | capdag.test.js:1663 |
| test060 | `test060_wrongPrefixFails` | TEST060: Test wrong prefix fails with InvalidPrefix error showing expected and actual prefix | capdag.test.js:864 |
| test062 | `test062_isRecord` | TEST062: Test is_record returns true when record marker tag is present indicating key-value structure | capdag.test.js:877 |
| test063 | `test063_isScalar` | TEST063: Test is_scalar returns true when list marker tag is absent (scalar is default) | capdag.test.js:888 |
| test064 | `test064_isList` | TEST064: Test is_list returns true when list marker tag is present indicating ordered collection | capdag.test.js:901 |
| test065 | `test065_isOpaque` | TEST065: Test is_opaque returns true when record marker is absent (opaque is default) | capdag.test.js:910 |
| test066 | `test066_isJson` | TEST066: Test is_json returns true only when fmt=json content-format tag is present | capdag.test.js:921 |
| test067 | `test067_isText` | TEST067: Text-representability is now carried by the orthogonal `enc=` tag (the old text marker and isText() are gone). A media is "text" iff it declares an encoding. | capdag.test.js:932 |
| test068 | `test068_isVoid` | TEST068: Test is_void returns true when void flag or type=void tag is present | capdag.test.js:945 |
| test0069 | `test0069_JS_mediaUrnsForExtension` | TEST0069: J s media urns for extension | capdag.test.js:1680 |
| test0070 | `test0070_JS_getExtensionMappings` | TEST0070: J s get extension mappings | capdag.test.js:1709 |
| test071 | `test071_toStringRoundtrip` | TEST071: Test to_string roundtrip ensures serialization and deserialization preserve URN structure | capdag.test.js:953 |
| test072 | `test072_constantsParse` | TEST072: Test all media URN constants parse successfully as valid media URNs | capdag.test.js:963 |
| test0073 | `test0073_JS_resolveMediaUrnFromSpecs` | TEST0073: J s resolve media urn from specs | capdag.test.js:1720 |
| test074 | `test074_mediaUrnMatching` | TEST074: Test media URN conforms_to using tagged URN semantics with specific and generic requirements | capdag.test.js:983 |
| test075 | `test075_accepts` | TEST075: Test accepts with implicit wildcards where handlers with fewer tags can handle more requests | capdag.test.js:997 |
| test076 | `test076_specificity` | TEST076: Test specificity increases with more tags for ranking conformance | capdag.test.js:1008 |
| test077 | `test077_serdeRoundtrip` | TEST077: Test serde roundtrip serializes to JSON string and deserializes back correctly | capdag.test.js:1017 |
| test078 | `test078_debugMatchingBehavior` | TEST078: conforms_to behavior between MEDIA_OBJECT and MEDIA_STRING | capdag.test.js:1026 |
| test0079 | `test0079_JS_capJSONSerialization` | TEST0079: J s cap j s o n serialization | capdag.test.js:1733 |
| test0080 | `test0080_JS_capDocumentationRoundTrip` | JS round-trip for the documentation field on Cap. Mirrors TEST920 in capdag/src/cap/definition.rs — the body is non-trivial (newlines, backticks, embedded quotes, Unicode) so escaping mismatches between JSON.stringify on this side and the Rust serializer on the other side surface as failures here. | capdag.test.js:1756 |
| test0081 | `test0081_JS_capDocumentationOmittedWhenNull` | When documentation is null, toJSON must omit the field entirely. This matches the Rust serializer's skip-when-None semantics and the ObjC toDictionary behaviour. A regression where null is emitted as `documentation: null` would break the symmetric round-trip with Rust (which has no null sentinel) and pollute generated JSON. | capdag.test.js:1778 |
| test0082 | `test0082_JS_mediaDefDocumentationPropagatesThroughResolve` | Documentation propagates from a mediaDefs definition through resolveMediaUrn into the resolved MediaDef. Mirrors TEST924 on the Rust side. This is the path every UI consumer uses, so a break here makes the new field invisible everywhere downstream. | capdag.test.js:1801 |
| test0083 | `test0083_JS_stdinSourceKindConstants` | TEST0083: J s stdin source kind constants | capdag.test.js:1832 |
| test0084 | `test0084_JS_stdinSourceNullData` | TEST0084: J s stdin source null data | capdag.test.js:1839 |
| test0085 | `test0085_JS_mediaDefConstruction` | TEST0085: J s media def construction | capdag.test.js:1847 |
| test0086 | `test0086_isCollection` | Mirror-specific coverage: isCollection returns true when collection marker tag is present Mirror-specific coverage: N/A for JS (MEDIA_COLLECTION constants removed - no longer exists) | capdag.test.js:2819 |
| test0087 | `test0087_Machine_emptyInput` | --- Machine parser tests (mirrors parser.rs tests) --- | capdag.test.js:3241 |
| test0088 | `test0088_Machine_whitespaceOnly` | TEST0088: Machine whitespace only | capdag.test.js:3246 |
| test0089 | `test0089_Machine_headerOnlyNoWirings` | TEST0089: Machine header only no wirings | capdag.test.js:3251 |
| test0090 | `test0090_Machine_duplicateAlias` | TEST0090: Machine duplicate alias | capdag.test.js:3259 |
| test091 | `test091_resolveCustomMediaDef` | TEST091: Test resolving custom media URN from local media_defs takes precedence over registry | capdag.test.js:1041 |
| test092 | `test092_resolveCustomWithSchema` | TEST092: Test resolving custom record media def with schema from local media_defs | capdag.test.js:1051 |
| test093 | `test093_resolveUnresolvableFailsHard` | TEST093: Test resolving unknown media URN fails with UnresolvableMediaUrn error | capdag.test.js:1068 |
| test0094 | `test0094_Machine_simpleLinearChain` | TEST0094: Machine simple linear chain | capdag.test.js:3271 |
| test0095 | `test0095_Machine_twoStepChain` | TEST0095: Machine two step chain | capdag.test.js:3287 |
| test0096 | `test0096_Machine_fanOut` | TEST0096: Machine fan out | capdag.test.js:3302 |
| test0097 | `test0097_Machine_fanInSecondaryAssignedByPriorWiring` | TEST0097: Machine fan in secondary assigned by prior wiring | capdag.test.js:3320 |
| test0098 | `test0098_Machine_fanInSecondaryUnassignedGetsWildcard` | TEST0098: Machine fan in secondary unassigned gets wildcard | capdag.test.js:3334 |
| test099 | `test099_resolvedIsBinary` | TEST099: Test ResolvedMediaDef is_binary returns true when enc tag is absent | capdag.test.js:1087 |
| test100 | `test100_resolvedIsRecord` | TEST100: Test ResolvedMediaDef is_record returns true when record marker is present | capdag.test.js:1093 |
| test101 | `test101_resolvedIsScalar` | TEST101: Test ResolvedMediaDef is_scalar returns true when list marker is absent | capdag.test.js:1099 |
| test102 | `test102_resolvedIsList` | TEST102: Test ResolvedMediaDef is_list returns true when list marker is present | capdag.test.js:1105 |
| test103 | `test103_resolvedIsJson` | TEST103: Test ResolvedMediaDef is_json returns true when json tag is present | capdag.test.js:1111 |
| test104 | `test104_resolvedIsText` | TEST104: Test ResolvedMediaDef is_text returns true when enc tag is present | capdag.test.js:1117 |
| test105 | `test105_metadataPropagation` | TEST105: Test metadata propagates from media def def to resolved media def | capdag.test.js:1123 |
| test106 | `test106_metadataWithValidation` | TEST106: Test metadata and validation can coexist in media definition | capdag.test.js:1146 |
| test107 | `test107_extensionsPropagation` | TEST107: Test extensions field propagates from media def def to resolved | capdag.test.js:1165 |
| test108 | `test108_extensionsSerialization` | TEST108: Test creating new cap with URN, title, and command verifies correct initialization | capdag.test.js:1181 |
| test109 | `test109_extensionsWithMetadataAndValidation` | TEST109: Test creating cap with metadata initializes and retrieves metadata correctly | capdag.test.js:1189 |
| test110 | `test110_multipleExtensions` | TEST110: Test cap matching with subset semantics for request fulfillment | capdag.test.js:1208 |
| test0111 | `test0111_Machine_loopEdge` | TEST0111: Machine loop edge | capdag.test.js:3346 |
| test0112 | `test0112_Machine_undefinedAliasFails` | TEST0112: Machine undefined alias fails | capdag.test.js:3356 |
| test0113 | `test0113_Machine_nodeAliasCollision` | TEST0113: Machine node alias collision | capdag.test.js:3364 |
| test0114 | `test0114_Machine_conflictingMediaTypesFail` | TEST0114: Machine conflicting media types fail | capdag.test.js:3375 |
| test115 | `test115_capArgSerialization` | TEST115: Test CapArg serialization and deserialization with multiple sources | capdag.test.js:1224 |
| test116 | `test116_capArgConstructors` | TEST116: Test CapArg constructor methods basic and with_description create args correctly | capdag.test.js:1257 |
| test0117 | `test0117_Machine_multilineFormat` | TEST0117: Machine multiline format | capdag.test.js:3388 |
| test0118 | `test0118_Machine_differentAliasesSameGraph` | TEST0118: Machine different aliases same graph | capdag.test.js:3399 |
| test0119 | `test0119_Machine_malformedInputFails` | TEST0119: Machine malformed input fails | capdag.test.js:3412 |
| test0120 | `test0120_Machine_unterminatedBracketFails` | TEST0120: Machine unterminated bracket fails | capdag.test.js:3420 |
| test0121 | `test0121_Machine_lineBasedSimpleChain` | --- Machine parser line-based mode tests --- | capdag.test.js:3429 |
| test0122 | `test0122_Machine_lineBasedTwoStepChain` | TEST0122: Machine line based two step chain | capdag.test.js:3443 |
| test0123 | `test0123_Machine_lineBasedLoop` | TEST0123: Machine line based loop | capdag.test.js:3454 |
| test0124 | `test0124_Machine_lineBasedFanIn` | TEST0124: Machine line based fan in | capdag.test.js:3464 |
| test0125 | `test0125_Machine_mixedBracketedAndLineBased` | TEST0125: Machine mixed bracketed and line based | capdag.test.js:3478 |
| test0126 | `test0126_Machine_lineBasedEquivalentToBracketed` | TEST0126: Machine line based equivalent to bracketed | capdag.test.js:3487 |
| test0127 | `test0127_Machine_lineBasedFormatSerialization` | TEST0127: Machine line based format serialization | capdag.test.js:3500 |
| test0128 | `test0128_Machine_lineBasedAndBracketedParseSameGraph` | TEST0128: Machine line based and bracketed parse same graph | capdag.test.js:3522 |
| test0129 | `test0129_Machine_edgeEquivalenceSameUrns` | --- Machine graph tests (mirrors graph.rs tests) --- | capdag.test.js:3548 |
| test0130 | `test0130_Machine_edgeEquivalenceDifferentCapUrns` | TEST0130: Machine edge equivalence different cap urns | capdag.test.js:3565 |
| test0131 | `test0131_Machine_edgeEquivalenceDifferentTargets` | TEST0131: Machine edge equivalence different targets | capdag.test.js:3582 |
| test0132 | `test0132_Machine_edgeEquivalenceDifferentLoopFlag` | TEST0132: Machine edge equivalence different loop flag | capdag.test.js:3599 |
| test0133 | `test0133_Machine_edgeEquivalenceSourceOrderIndependent` | TEST0133: Machine edge equivalence source order independent | capdag.test.js:3616 |
| test0134 | `test0134_Machine_edgeEquivalenceDifferentSourceCount` | TEST0134: Machine edge equivalence different source count | capdag.test.js:3633 |
| test0135 | `test0135_Machine_graphEquivalenceSameEdges` | TEST0135: Machine graph equivalence same edges | capdag.test.js:3650 |
| test0136 | `test0136_Machine_graphEquivalenceReorderedEdges` | TEST0136: Machine graph equivalence reordered edges | capdag.test.js:3666 |
| test0137 | `test0137_Machine_graphNotEquivalentDifferentEdgeCount` | TEST0137: Machine graph not equivalent different edge count | capdag.test.js:3682 |
| test0138 | `test0138_Machine_graphNotEquivalentDifferentCap` | TEST0138: Machine graph not equivalent different cap | capdag.test.js:3697 |
| test0139 | `test0139_Machine_graphEmpty` | TEST0139: Machine graph empty | capdag.test.js:3711 |
| test0140 | `test0140_Machine_graphEmptyEquivalence` | TEST0140: Machine graph empty equivalence | capdag.test.js:3718 |
| test0141 | `test0141_Machine_rootSourcesLinearChain` | TEST0141: Machine root sources linear chain | capdag.test.js:3725 |
| test0142 | `test0142_Machine_leafTargetsLinearChain` | TEST0142: Machine leaf targets linear chain | capdag.test.js:3740 |
| test0143 | `test0143_Machine_rootSourcesFanIn` | TEST0143: Machine root sources fan in | capdag.test.js:3755 |
| test0144 | `test0144_Machine_displayEdge` | TEST0144: Machine display edge | capdag.test.js:3768 |
| test0145 | `test0145_Machine_displayGraph` | TEST0145: Machine display graph | capdag.test.js:3780 |
| test0146 | `test0146_Machine_serializeSingleEdge` | --- Machine serializer tests (mirrors serializer.rs tests) --- | capdag.test.js:3793 |
| test0147 | `test0147_Machine_serializeTwoEdgeChain` | TEST0147: Machine serialize two edge chain | capdag.test.js:3809 |
| test0148 | `test0148_Machine_serializeEmptyGraph` | TEST0148: Machine serialize empty graph | capdag.test.js:3823 |
| test0149 | `test0149_Machine_roundtripSingleEdge` | TEST0149: Machine roundtrip single edge | capdag.test.js:3828 |
| test150 | `test150_capManifestJsonSerialization` | TEST150: JSON roundtrip | capdag.test.js:1285 |
| test0151 | `test0151_Machine_roundtripTwoEdgeChain` | TEST0151: Machine roundtrip two edge chain | capdag.test.js:3842 |
| test0152 | `test0152_Machine_roundtripFanOut` | TEST0152: Machine roundtrip fan out | capdag.test.js:3857 |
| test0153 | `test0153_Machine_roundtripLoopEdge` | TEST0153: Machine roundtrip loop edge | capdag.test.js:3873 |
| test0154 | `test0154_Machine_serializationIsDeterministic` | TEST0154: Machine serialization is deterministic | capdag.test.js:3887 |
| test0155 | `test0155_Machine_reorderedEdgesProduceSameNotation` | TEST0155: Machine reordered edges produce same notation | capdag.test.js:3901 |
| test156 | `test156_stdinSourceFromData` | TEST156: Test creating StdinSource Data variant with byte vector | capdag.test.js:1441 |
| test157 | `test157_stdinSourceFromFileReference` | TEST157: Test creating StdinSource FileReference variant with all required fields | capdag.test.js:1452 |
| test158 | `test158_stdinSourceWithEmptyData` | TEST158: Test StdinSource Data with empty vector stores and retrieves correctly | capdag.test.js:1469 |
| test159 | `test159_stdinSourceWithBinaryContent` | TEST159: Test StdinSource Data with binary content like PNG header bytes | capdag.test.js:1477 |
| test0160 | `test0160_Machine_multilineSerializeFormat` | TEST0160: Machine multiline serialize format | capdag.test.js:3918 |
| test0161 | `test0161_Machine_aliasFromOpTag` | Aliases are pure-index `edge_<N>` regardless of the cap's tags; there is no privileged `op` tag to derive a friendlier name from. | capdag.test.js:3934 |
| test0162 | `test0162_Machine_aliasFallbackWithoutOpTag` | TEST0162: Machine alias fallback without op tag | capdag.test.js:3946 |
| test0163 | `test0163_Machine_duplicateOpTagsDisambiguated` | Pure-index aliases inherently disambiguate edges that share a marker tag. | capdag.test.js:3958 |
| test0164 | `test0164_Machine_builderSingleEdge` | --- Machine builder tests --- | capdag.test.js:3980 |
| test0165 | `test0165_Machine_builderWithLoop` | TEST0165: Machine builder with loop | capdag.test.js:3993 |
| test0166 | `test0166_Machine_builderChaining` | TEST0166: Machine builder chaining | capdag.test.js:4006 |
| test0167 | `test0167_Machine_builderEquivalentToParsed` | TEST0167: Machine builder equivalent to parsed | capdag.test.js:4015 |
| test0168 | `test0168_Machine_builderRoundTrip` | TEST0168: Machine builder round trip | capdag.test.js:4028 |
| test0169 | `test0169_Machine_capUrnIsEquivalent` | --- CapUrn.isEquivalent/isComparable tests --- | capdag.test.js:4040 |
| test0170 | `test0170_Machine_capUrnIsComparable` | TEST0170: Machine cap urn is comparable | capdag.test.js:4049 |
| test0171 | `test0171_Machine_capUrnInMediaUrn` | TEST0171: Machine cap urn in media urn | capdag.test.js:4057 |
| test0172 | `test0172_Machine_capUrnOutMediaUrn` | TEST0172: Machine cap urn out media urn | capdag.test.js:4065 |
| test0173 | `test0173_Machine_mediaUrnIsEquivalent` | --- MediaUrn.isEquivalent/isComparable tests --- | capdag.test.js:4074 |
| test0174 | `test0174_Machine_mediaUrnIsComparable` | TEST0174: Machine media urn is comparable | capdag.test.js:4083 |
| test0175 | `test0175_Machine_parseMachineWithAST_headerLocation` | Phase 0A: Position tracking tests | capdag.test.js:4096 |
| test0176 | `test0176_Machine_parseMachineWithAST_wiringLocation` | TEST0176: Machine parse machine with a s t wiring location | capdag.test.js:4113 |
| test0177 | `test0177_Machine_parseMachineWithAST_multilinePositions` | TEST0177: Machine parse machine with a s t multiline positions | capdag.test.js:4128 |
| test0178 | `test0178_Machine_parseMachineWithAST_fanInSourceLocations` | TEST0178: Machine parse machine with a s t fan in source locations | capdag.test.js:4138 |
| test0179 | `test0179_Machine_parseMachineWithAST_aliasMap` | TEST0179: Machine parse machine with a s t alias map | capdag.test.js:4150 |
| test0180 | `test0180_Machine_parseMachineWithAST_nodeMedia` | TEST0180: Machine parse machine with a s t node media | capdag.test.js:4169 |
| test0181 | `test0181_Machine_errorLocation_parseError` | TEST0181: Machine error location parse error | capdag.test.js:4182 |
| test0182 | `test0182_Machine_errorLocation_duplicateAlias` | TEST0182: Machine error location duplicate alias | capdag.test.js:4193 |
| test0183 | `test0183_Machine_errorLocation_undefinedAlias` | TEST0183: Machine error location undefined alias | capdag.test.js:4208 |
| test0184 | `test0184_Machine_toMermaid_linearChain` | Phase 0C: Machine.toMermaid() tests | capdag.test.js:4222 |
| test0185 | `test0185_Machine_toMermaid_loopEdge` | TEST0185: Machine to mermaid loop edge | capdag.test.js:4241 |
| test0186 | `test0186_Machine_toMermaid_emptyGraph` | TEST0186: Machine to mermaid empty graph | capdag.test.js:4253 |
| test0187 | `test0187_Machine_toMermaid_fanIn` | TEST0187: Machine to mermaid fan in | capdag.test.js:4260 |
| test0188 | `test0188_Machine_toMermaid_fanOut` | TEST0188: Machine to mermaid fan out | capdag.test.js:4272 |
| test0189 | `test0189_Machine_capRegistryEntry_construction` | Phase 0B: FabricRegistryClient tests | capdag.test.js:4292 |
| test0190 | `test0190_Machine_mediaRegistryEntry_construction` | TEST0190: Machine media registry entry construction | capdag.test.js:4316 |
| test0191 | `test0191_Machine_capRegistryClient_construction` | TEST0191: Machine cap registry client construction | capdag.test.js:4330 |
| test0192 | `test0192_Machine_capRegistryEntry_defaults` | TEST0192: Machine cap registry entry defaults | capdag.test.js:4338 |
| test0193 | `test0193_Renderer_cardinalityLabel_allFourCases` | TEST0193: Renderer cardinality label all four cases | capdag.test.js:4404 |
| test0194 | `test0194_Renderer_cardinalityLabel_usesUnicodeArrow` | TEST0194: Renderer cardinality label uses unicode arrow | capdag.test.js:4412 |
| test0195 | `test0195_Renderer_cardinalityFromCap_findsStdinArgNotFirstArg` | TEST0195: Renderer cardinality from cap finds stdin arg not first arg | capdag.test.js:4421 |
| test0196 | `test0196_Renderer_cardinalityFromCap_scalarDefaultsWhenFieldsMissing` | TEST0196: Renderer cardinality from cap scalar defaults when fields missing | capdag.test.js:4446 |
| test0197 | `test0197_Renderer_cardinalityFromCap_outputOnlySequence` | TEST0197: Renderer cardinality from cap output only sequence | capdag.test.js:4455 |
| test0198 | `test0198_Renderer_cardinalityFromCap_rejectsStringIsSequence` | TEST0198: Renderer cardinality from cap rejects string is sequence | capdag.test.js:4467 |
| test0199 | `test0199_Renderer_cardinalityFromCap_throwsOnNonObject` | TEST0199: Renderer cardinality from cap throws on non object | capdag.test.js:4481 |
| test0200 | `test0200_Renderer_canonicalMediaUrn_normalizesTagOrder` | TEST0200: Renderer canonical media urn normalizes tag order | capdag.test.js:4501 |
| test0201 | `test0201_Renderer_canonicalMediaUrn_preservesValueTags` | TEST0201: Renderer canonical media urn preserves value tags | capdag.test.js:4511 |
| test0202 | `test0202_Renderer_canonicalMediaUrn_rejectsCapUrn` | TEST0202: Renderer canonical media urn rejects cap urn | capdag.test.js:4517 |
| test0203 | `test0203_Renderer_mediaNodeLabel_rejectsUrnDerivedLabels` | TEST0203: Renderer media node label rejects urn derived labels | capdag.test.js:4530 |
| test0204 | `test0204_Renderer_buildBrowseGraphData_rejectsMissingMediaTitles` | TEST0204: Renderer build browse graph data rejects missing media titles | capdag.test.js:4545 |
| test0205 | `test0205_Renderer_validateStrandStep_rejectsUnknownVariant` | TEST0205: Renderer validate strand step rejects unknown variant | capdag.test.js:4603 |
| test0206 | `test0206_Renderer_validateStrandStep_requiresBooleanIsSequence` | TEST0206: Renderer validate strand step requires boolean is sequence | capdag.test.js:4621 |
| test0207 | `test0207_Renderer_classifyStrandCapSteps_capFlags` | TEST0207: Renderer classify strand cap steps cap flags | capdag.test.js:4644 |
| test0208 | `test0208_Renderer_classifyStrandCapSteps_nestedForks` | TEST0208: Renderer classify strand cap steps nested forks | capdag.test.js:4666 |
| test0209 | `test0209_Renderer_buildStrandGraphData_singleCapPlain` | TEST0209: Renderer build strand graph data single cap plain | capdag.test.js:4697 |
| test0210 | `test0210_Renderer_buildStrandGraphData_sequenceShowsCardinality` | TEST0210: Renderer build strand graph data sequence shows cardinality | capdag.test.js:4725 |
| test0211 | `test0211_Renderer_buildStrandGraphData_foreachCollectSpan` | TEST0211: Renderer build strand graph data foreach collect span | capdag.test.js:4746 |
| test0212 | `test0212_Renderer_buildStrandGraphData_standaloneCollect` | TEST0212: Renderer build strand graph data standalone collect | capdag.test.js:4798 |
| test0213 | `test0213_Renderer_buildStrandGraphData_unclosedForEachBody` | TEST0213: Renderer build strand graph data unclosed for each body | capdag.test.js:4826 |
| test0214 | `test0214_Renderer_buildStrandGraphData_nestedForEachThrows` | TEST0214: Renderer build strand graph data nested for each throws | capdag.test.js:4864 |
| test0215 | `test0215_Renderer_collapseStrand_singleCapBodyKeepsCapOwnLabel` | TEST0215: Renderer collapse strand single cap body keeps cap own label | capdag.test.js:4893 |
| test0216 | `test0216_Renderer_collapseStrand_unclosedForEachBodyCollapses` | TEST0216: Renderer collapse strand unclosed for each body collapses | capdag.test.js:4946 |
| test0217 | `test0217_Renderer_collapseStrand_standaloneCollectCollapses` | TEST0217: Renderer collapse strand standalone collect collapses | capdag.test.js:5003 |
| test0218 | `test0218_Renderer_collapseStrand_sequenceProducingCapBeforeForeach` | TEST0218: Renderer collapse strand sequence producing cap before foreach | capdag.test.js:5047 |
| test0219 | `test0219_Renderer_collapseStrand_plainCapMergesTrailingOutput` | TEST0219: Renderer collapse strand plain cap merges trailing output | capdag.test.js:5112 |
| test0220 | `test0220_Renderer_collapseStrand_plainCapDistinctTargetNoMerge` | TEST0220: Renderer collapse strand plain cap distinct target no merge | capdag.test.js:5149 |
| test0221 | `test0221_Renderer_validateStrandPayload_missingSourceMediaUrn` | TEST0221: Renderer validate strand payload missing source media urn | capdag.test.js:5176 |
| test0222 | `test0222_Renderer_validateBodyOutcome_rejectsNegativeIndex` | ---------------- run builder ---------------- | capdag.test.js:5189 |
| test0223 | `test0223_Renderer_buildRunGraphData_pagesSuccessesAndFailures` | TEST0223: Renderer build run graph data pages successes and failures | capdag.test.js:5200 |
| test0224 | `test0224_Renderer_buildRunGraphData_failureWithoutFailedCapRendersFullTrace` | TEST0224: Renderer build run graph data failure without failed cap renders full trace | capdag.test.js:5271 |
| test0225 | `test0225_Renderer_buildRunGraphData_usesCapUrnIsEquivalentForFailedCap` | TEST0225: Renderer build run graph data uses cap urn is equivalent for failed cap | capdag.test.js:5310 |
| test0226 | `test0226_Renderer_buildRunGraphData_backboneHasNoForeachNode` | TEST0226: Renderer build run graph data backbone has no foreach node | capdag.test.js:5370 |
| test0227 | `test0227_Renderer_buildRunGraphData_allFailedDropsTargetPlaceholder` | TEST0227: Renderer build run graph data all failed drops target placeholder | capdag.test.js:5425 |
| test0228 | `test0228_Renderer_buildRunGraphData_unclosedForeachSuccessNoMerge` | TEST0228: Renderer build run graph data unclosed foreach success no merge | capdag.test.js:5491 |
| test0229 | `test0229_Renderer_buildRunGraphData_closedForeachSuccessMergesAtCollectTarget` | TEST0229: Renderer build run graph data closed foreach success merges at collect target | capdag.test.js:5553 |
| test0230 | `test0230_Renderer_validateEditorGraphPayload_rejectsUnknownKind` | ---------------- editor-graph builder ---------------- | capdag.test.js:5608 |
| test0231 | `test0231_Renderer_buildEditorGraphData_collapsesCapsIntoLabeledEdges` | TEST0231: Renderer build editor graph data collapses caps into labeled edges | capdag.test.js:5623 |
| test0232 | `test0232_Renderer_buildEditorGraphData_loopMarkedEdgeGetsLoopClass` | TEST0232: Renderer build editor graph data loop marked edge gets loop class | capdag.test.js:5662 |
| test0233 | `test0233_Renderer_buildEditorGraphData_cardinalityFromDataSlotSequenceFlags` | TEST0233: Renderer build editor graph data cardinality from data slot sequence flags | capdag.test.js:5681 |
| test0234 | `test0234_Renderer_buildEditorGraphData_capWithoutCompleteArgsIsDropped` | TEST0234: Renderer build editor graph data cap without complete args is dropped | capdag.test.js:5701 |
| test0235 | `test0235_Renderer_buildEditorGraphData_rejectsEdgeWithMissingSource` | TEST0235: Renderer build editor graph data rejects edge with missing source | capdag.test.js:5719 |
| test0236 | `test0236_Renderer_buildResolvedMachineGraphData_singleStrandLinearChain` | ---------------- resolved-machine builder ---------------- | capdag.test.js:5735 |
| test0237 | `test0237_Renderer_buildResolvedMachineGraphData_loopEdgeGetsLoopClass` | TEST0237: Renderer build resolved machine graph data loop edge gets loop class | capdag.test.js:5794 |
| test0238 | `test0238_Renderer_buildResolvedMachineGraphData_fanInProducesEdgePerAssignment` | TEST0238: Renderer build resolved machine graph data fan in produces edge per assignment | capdag.test.js:5829 |
| test0239 | `test0239_Renderer_buildResolvedMachineGraphData_multiStrandKeepsStrandsDisjoint` | TEST0239: Renderer build resolved machine graph data multi strand keeps strands disjoint | capdag.test.js:5870 |
| test0240 | `test0240_Renderer_buildResolvedMachineGraphData_duplicateNodeIdAcrossStrandsFailsHard` | TEST0240: Renderer build resolved machine graph data duplicate node id across strands fails hard | capdag.test.js:5933 |
| test0241 | `test0241_Renderer_validateResolvedMachinePayload_rejectsMissingFields` | TEST0241: Renderer validate resolved machine payload rejects missing fields | capdag.test.js:5969 |
| test274 | `test274_capArgumentValueNew` | TEST274: Test CapArgumentValue::new stores media_urn and raw byte value | capdag.test.js:1491 |
| test275 | `test275_capArgumentValueFromStr` | TEST275: Test CapArgumentValue::from_str converts string to UTF-8 bytes | capdag.test.js:1498 |
| test276 | `test276_capArgumentValueAsStrValid` | TEST276: Test CapArgumentValue::value_as_str succeeds for UTF-8 data | capdag.test.js:1505 |
| test277 | `test277_capArgumentValueAsStrInvalidUtf8` | TEST277: Test CapArgumentValue::value_as_str fails for non-UTF-8 binary data | capdag.test.js:1511 |
| test278 | `test278_capArgumentValueEmpty` | TEST278: Test CapArgumentValue::new with empty value stores empty vec | capdag.test.js:1523 |
| test282 | `test282_capArgumentValueUnicode` | TEST282: Test CapArgumentValue::from_str with Unicode string preserves all characters | capdag.test.js:1532 |
| test283 | `test283_capArgumentValueLargeBinary` | TEST283: Test CapArgumentValue with large binary payload preserves all bytes | capdag.test.js:1538 |
| test304 | `test304_mediaAvailabilityOutputConstant` | TEST304: Test MEDIA_AVAILABILITY_OUTPUT constant parses as valid media URN with correct tags | capdag.test.js:1557 |
| test305 | `test305_mediaPathOutputConstant` | TEST305: Test MEDIA_PATH_OUTPUT constant parses as valid media URN with correct tags | capdag.test.js:1566 |
| test306 | `test306_availabilityAndPathOutputDistinct` | TEST306: Test MEDIA_AVAILABILITY_OUTPUT and MEDIA_PATH_OUTPUT are distinct URNs | capdag.test.js:1575 |
| test307 | `test307_modelAvailabilityUrn` | TEST307: Test model_availability_urn builds valid cap URN with correct op and media defs | capdag.test.js:1589 |
| test308 | `test308_modelPathUrn` | TEST308: Test model_path_urn builds valid cap URN with correct op and media defs | capdag.test.js:1601 |
| test309 | `test309_modelAvailabilityAndPathAreDistinct` | TEST309: Test model_availability_urn and model_path_urn produce distinct URNs | capdag.test.js:1613 |
| test310 | `test310_llmGenerateTextUrn` | TEST310: llm_generate_text_urn() produces a valid cap URN with enc=utf-8 in/out specs | capdag.test.js:1620 |
| test312 | `test312_allUrnBuildersProduceValidUrns` | TEST312: Test all URN builders produce parseable cap URNs | capdag.test.js:1643 |
| test320 | `test320_cartridgeInfoConstruction` | TEST320-335: CartridgeRepoServer and CartridgeRepoClient tests | capdag.test.js:2007 |
| test321 | `test321_cartridgeInfoIsSigned` | TEST321: CartridgeInfo.is_signed() returns true when signature is present | capdag.test.js:2041 |
| test322 | `test322_cartridgeInfoBuildForPlatform` | TEST322: CartridgeInfo.build_for_platform() returns the build matching the current platform | capdag.test.js:2053 |
| test323 | `test323_cartridgeRepoServerValidateRegistry` | TEST323: CartridgeRepoServer requires schema 5.0 and rejects older. | capdag.test.js:2087 |
| test324 | `test324_cartridgeRepoServerTransformToArray` | TEST324: CartridgeRepoServer walks both channels and emits a flat CartridgeInfo array preserving channel provenance. Release entries appear first. | capdag.test.js:2126 |
| test325 | `test325_cartridgeRepoServerGetCartridges` | TEST325: CartridgeRepoServer.getCartridges() wraps the transformed flat array (across both channels) in the response envelope. | capdag.test.js:2164 |
| test326 | `test326_cartridgeRepoServerGetCartridgeById` | TEST326: CartridgeRepoServer.getCartridgeById() requires (channel, id). Same id looked up in the wrong channel must miss — channels are independent namespaces. | capdag.test.js:2178 |
| test327 | `test327_cartridgeRepoServerSearchCartridges` | TEST327: CartridgeRepoServer.searchCartridges() filters across both channels by name/description/tags/cap titles. Cap URN strings are not substring-matched. | capdag.test.js:2210 |
| test328 | `test328_cartridgeRepoServerGetByCategory` | TEST328: CartridgeRepoServer.getCartridgesByCategory() filters cartridges by category across both channels. | capdag.test.js:2232 |
| test329 | `test329_cartridgeRepoServerGetByCap` | TEST329: CartridgeRepoServer.getCartridgesByCap() parses the input URN and matches each declared cap via `conformsTo`. Tag-order differences resolve because matching is order-theoretic, not string. | capdag.test.js:2251 |
| test330 | `test330_cartridgeRepoClientUpdateCache` | TEST330: CartridgeRepoClient updates its local cache keyed by "<channel>:<id>". The cache holds release and nightly entries independently — the same id is allowed in both. | capdag.test.js:2268 |
| test331 | `test331_cartridgeRepoClientGetSuggestions` | TEST331: CartridgeRepoClient.getSuggestionsForCap() returns cartridge suggestions with channel propagated onto each suggestion. | capdag.test.js:2296 |
| test332 | `test332_cartridgeRepoClientGetCartridge` | TEST332: CartridgeRepoClient.getCartridge() requires (channel, id). Same id in the wrong channel must miss. | capdag.test.js:2326 |
| test333 | `test333_cartridgeRepoClientGetAllCaps` | TEST333: CartridgeRepoClient.getAllAvailableCaps() returns the set of normalized URNs across both channels. | capdag.test.js:2371 |
| test334 | `test334_cartridgeRepoClientNeedsSync` | TEST334: CartridgeRepoClient.needsSync() returns true when cache is empty / stale, false right after a fresh update. | capdag.test.js:2388 |
| test335 | `test335_cartridgeRepoServerClientIntegration` | TEST335: Round-trip: server produces a v5.0 response, client consumes it, channel provenance is preserved end-to-end. | capdag.test.js:2407 |
| test597 | `test597_capArgWithFullDefinition` | TEST597: CapArg::with_full_definition stores all fields including optional ones | capdag.test.js:1341 |
| test639 | `test639_emptyCapIsIllegal` | TEST639: cap: (empty) is the illegal bare top form | capdag.test.js:3045 |
| test640 | `test640_inOnlyIsIllegal` | TEST640: cap:in collapses to the same illegal bare top form | capdag.test.js:3054 |
| test641 | `test641_outOnlyIsIllegal` | TEST641: cap:out collapses to the same illegal bare top form | capdag.test.js:3063 |
| test642 | `test642_inOutWithoutValuesAreIllegal` | TEST642: cap:in;out collapses to the same illegal bare top form | capdag.test.js:3072 |
| test643 | `test643_explicitAsteriskIsIllegal` | TEST643: cap:in=*;out=* is the same illegal bare top form | capdag.test.js:3081 |
| test644 | `test644_specificInWildcardOutIsIllegal` | TEST644: cap:in=media:;out=* is the same illegal bare top form | capdag.test.js:3090 |
| test645 | `test645_wildcardInSpecificOut` | TEST645: cap:in=*;out=media:text has wildcard in, specific out | capdag.test.js:3099 |
| test646 | `test646_invalidInSpecFails` | TEST646: cap:in=foo fails (invalid media URN) | capdag.test.js:3106 |
| test647 | `test647_invalidOutSpecFails` | TEST647: cap:in=media:;out=bar fails (invalid media URN) | capdag.test.js:3115 |
| test648 | `test648_wildcardAcceptsSpecific` | TEST648: Wildcard in/out match specific caps | capdag.test.js:3124 |
| test649 | `test649_specificityScoring` | TEST649: Specificity - wildcard has 0, specific has tag count | capdag.test.js:3133 |
| test650 | `test650_wildcardPreserveOtherTags` | TEST650: cap:in=media:;out=media:;test preserves other tags | capdag.test.js:3142 |
| test651 | `test651_wildcardGenericFormsRejected` | TEST651: Generic top-to-top spellings are all rejected. | capdag.test.js:3151 |
| test652 | `test652_capIdentityConstantWorks` | TEST652: CAP_IDENTITY constant names the true identity cap, not bare cap: | capdag.test.js:3172 |
| test653 | `test653_invalidEffectNoneDeclarationRejected` | TEST653: invalid effect=none declarations fail at construction. | capdag.test.js:3189 |
| test654 | `test654_effectNonePreservesRuntimeMedia` | TEST654: effect=none preserves runtime media identity. | capdag.test.js:3198 |
| test655 | `test655_effectDeclaredUsesDeclaredOutput` | TEST655: default effect=declared does not preserve runtime refinements. | capdag.test.js:3207 |
| test656 | `test656_invalidEffectNoneFailsHard` | TEST656: invalid effect=none declarations fail hard at construction. | capdag.test.js:3218 |
| test657 | `test657_effectDispatchRequiresExplicitWildcard` | TEST657: omitted effect means declared; unconstrained effect must be explicit. | capdag.test.js:3227 |
| test890 | `test890_directionSemanticMatching` | TEST890: Semantic direction matching - generic provider matches specific request | capdag.test.js:727 |
| test891 | `test891_directionSemanticSpecificity` | TEST891: Semantic direction specificity — more constraints in either axis means a higher score under the truth-table-driven sum. media: (top, no tags) scores 0; each marker tag scores 2; each exact-value tag (e.g. ext=png) scores 4. | capdag.test.js:780 |
| test939 | `test939_capUrnCanonicalFormDropsWildcardInOut` | TEST939: The canonical form drops `in=media:` and `out=media:` segments. Every spelling of "the same cap with wildcard in/out" collapses to one byte-identical canonical string. This is the contract that makes registry lookups work: the cap-publisher hashes `<canonical-urn>` to compute the cache key, and every language port (Rust, Go, Python, JS, ObjC) must agree on the canonical form for cross-language lookups to land on the same key. A regression that emitted the wildcard segments would silently move the published cap to a different SHA-256 bucket, 404'ing every reader that hashes the canonical form. | capdag.test.js:304 |
| test1294 | `test1294_rule11VoidInputWithStdinRejected` | TEST1294: RULE11 - void-input cap with stdin source rejected | capdag.test.js:2989 |
| test1295 | `test1295_rule11NonVoidInputWithoutStdinRejected` | TEST1295: RULE11 - non-void-input cap without stdin source rejected | capdag.test.js:3004 |
| test1296 | `test1296_rule11VoidInputCliFlagOnly` | TEST1296: RULE11 - void-input cap with only cli_flag sources passes | capdag.test.js:3019 |
| test1297 | `test1297_rule11NonVoidInputWithStdin` | TEST1297: RULE11 - non-void-input cap with stdin source passes | capdag.test.js:3029 |
| test1298 | `test1298_isBool` | TEST1298: is_bool returns true only when bool marker tag is present | capdag.test.js:2797 |
| test1299 | `test1299_isFilePath` | TEST1299: isFilePath returns true for the single file-path media URN, false for everything else. There is no "array" variant — cardinality is carried by is_sequence on the wire, not by URN tags. | capdag.test.js:2811 |
| test1302 | `test1302_predicateConstantConsistency` | TEST1302: predicates are consistent with constants — every constant triggers exactly the expected predicates | capdag.test.js:2830 |
| test1303 | `test1303_withoutTag` | TEST1303: without_tag removes tag, rejects structural keys, case-insensitive for keys | capdag.test.js:2869 |
| test1304 | `test1304_withInOutSpec` | TEST1304: with_in_spec and with_out_spec change direction specs | capdag.test.js:2889 |
| test1305 | `test1305_findAllMatches` | TEST1305: CapMatcher::find_all_matches returns all matching caps sorted by specificity | capdag.test.js:2919 |
| test1306 | `test1306_areCompatible` | TEST1306: CapMatcher::are_compatible detects bidirectional overlap | capdag.test.js:2937 |
| test1307 | `test1307_withTagRejectsStructuralKeys` | TEST1307: with_tag rejects structural keys | capdag.test.js:2962 |
| test1308 | `test1308_builderRejectsStructuralKeys` | TEST1308: builder rejects structural keys on tag/marker | capdag.test.js:2970 |
| test1312 | `test1312_isImage` | TEST1312: is_image returns true only when image marker tag is present | capdag.test.js:2752 |
| test1313 | `test1313_isAudio` | TEST1313: is_audio returns true only when audio marker tag is present | capdag.test.js:2764 |
| test1314 | `test1314_isVideo` | TEST1314: is_video returns true only when video marker tag is present | capdag.test.js:2775 |
| test1315 | `test1315_isNumeric` | TEST1315: is_numeric returns true only when numeric marker tag is present | capdag.test.js:2785 |
| test1800 | `test1800_kindIdentityOnlyForBareCap` | TEST1800: Identity classifier — only explicit effect=none qualifies. | capdag.test.js:6011 |
| test1801 | `test1801_kindSourceWhenInputIsVoid` | TEST1801: Source classifier — in=media:void, out non-void. | capdag.test.js:6038 |
| test1802 | `test1802_kindSinkWhenOutputIsVoid` | TEST1802: Sink classifier — out=media:void, in non-void. | capdag.test.js:6047 |
| test1803 | `test1803_kindEffectWhenBothSidesVoid` | TEST1803: Effect classifier — both sides void. Reads as `() → ()`. | capdag.test.js:6056 |
| test1804 | `test1804_kindTransformForNormalDataProcessors` | TEST1804: Transform classifier — at least one side non-void, and the cap is not the bare identity. | capdag.test.js:6067 |
| test1805 | `test1805_kindInvariantUnderCanonicalSpellings` | TEST1805: Kind is invariant under canonicalization. The same morphism written in many surface forms must classify the same way once parsed. | capdag.test.js:6117 |
| test1810 | `test1810_mediaVoidIsAtomic` | TEST1810: media:void is atomic — refinements are parse errors. Mirrored across every language port (Rust, Go, Python, Swift/ObjC, JS) under the SAME number. Any divergence is a wire-level inconsistency — the unit type's atomicity is part of the protocol's deepest layer, not a per-port detail. | capdag.test.js:6082 |
| test1820 | `test1820_specificityQuestionIsZero` | TEST1820: A `?`-valued cap-tag scores 0. Same as missing. | capdag.test.js:6158 |
| test1821 | `test1821_specificityMustNotHaveIsFive` | TEST1821: A `!`-valued cap-tag scores 5 (top of negative chain). | capdag.test.js:6168 |
| test1822 | `test1822_specificityMustHaveAnyIsTwo` | TEST1822: A `*`-valued cap-tag (including bare markers) scores 2. | capdag.test.js:6175 |
| test1823 | `test1823_specificityExactValueIsFour` | TEST1823: An exact-valued cap-tag scores 4. | capdag.test.js:6189 |
| test1824 | `test1824_specificityCombinedYAxis` | TEST1824: All six forms compose additively on a single cap. y combining 0+1+2+3+4+5 must sum to 15. | capdag.test.js:6197 |
| test1830 | `test1830_canonicalizeNoConstraint` | TEST1830: ?x ≡ x? ≡ x=? all canonicalize to ?x. | capdag.test.js:6208 |
| test1831 | `test1831_canonicalizeAbsentOrNotValue` | TEST1831: ?x=v and x?=v both canonicalize to x?=v. The third hypothetical form `x=?v` is NOT recognized as a qualifier — a value starting with `?` is just an exact value beginning with a `?` character. | capdag.test.js:6221 |
| test1832 | `test1832_canonicalizeMustHaveAny` | TEST1832: x ≡ x=* both canonicalize to bare x. | capdag.test.js:6237 |
| test1833 | `test1833_canonicalizePresentNotValue` | TEST1833: !x=v and x!=v both canonicalize to x!=v. The third hypothetical form `x=!v` is NOT recognized as a qualifier — a value starting with `!` is just an exact value beginning with a `!` character. | capdag.test.js:6250 |
| test1834 | `test1834_canonicalizeExactValue` | TEST1834: x=v stays as x=v. | capdag.test.js:6266 |
| test1835 | `test1835_canonicalizeMustNotHave` | TEST1835: !x ≡ x! ≡ x=! all canonicalize to !x. | capdag.test.js:6272 |
| test1842 | `test1842_truthTableFullCrossProduct` | TEST1842: Full 6×6 truth table. | capdag.test.js:6282 |
| test1843 | `test1843_rejectInvalidCombinations` | TEST1843: Invalid qualifier combinations must be rejected. | capdag.test.js:6310 |
| test1844 | `test1844_axisWeightingOutDominates` | TEST1844: out-axis difference dominates combined in+y differences. | capdag.test.js:6325 |
| test1845 | `test1845_axisWeightingInDominatesY` | TEST1845: With equal out, in-axis dominates over y-axis. | capdag.test.js:6335 |
| test1846 | `test1846_axisWeightingDecodedLayout` | TEST1846: Decoded layout — 10000*out + 100*in + y. | capdag.test.js:6345 |
| test1847 | `test1847_capVersionZeroOmittedOnWire` | TEST1847: Cap with version=0 round-trips with no `version` key on wire | capdag.test.js:6357 |
| test1848 | `test1848_capVersionNonZeroOnWire` | TEST1848: Cap with version=N round-trips with `version: N` on wire | capdag.test.js:6369 |
| test1849 | `test1849_resolveForHostCompatibleLatest` | TEST1849: latest version has a host build → Compatible, resolving to the latest version and that platform's native-format package. | capdag.test.js:2491 |
| test1850 | `test1850_resolveForHostCompatibleOutdated` | TEST1850: the latest version lacks a host build but an older version has one → CompatibleOutdated, resolving to the NEWEST older version with a host build (not the oldest), with a reason naming both the latest and the resolved. | capdag.test.js:2509 |
| test1851 | `test1851_resolveForHostIncompatible` | TEST1851: no version ships a host build → Incompatible, no resolved version/package, reason states the host platform. | capdag.test.js:2527 |
| test1852 | `test1852_resolveForHostSkipsBuildWithNoInstaller` | TEST1852: a host build whose packages[] is empty AND has no legacy `package` ships no installer; resolution must SKIP it (not resolve to an un-downloadable version) and fall through to an older usable version. | capdag.test.js:2543 |
| test1853 | `test1853_hostPlatformNormalizedForm` | TEST1853: hostPlatform() returns a normalized {os}-{arch} string with arch aarch64/arm64 mapped to arm64 — the exact form the registry uses. | capdag.test.js:2562 |
| test1872 | `test1872_registryUrlFromBuildEnvPassesThroughNonempty` | TEST1872: a non-empty MFR_CARTRIDGE_REGISTRY_URL passes through verbatim — a published build reports exactly the URL it was compiled with. | capdag.test.js:2579 |
| test1873 | `test1873_registryUrlFromBuildEnvNoneForDev` | TEST1873: an unset env (null/undefined) yields null — a dev build has no baked registry and loads only `dev/` cartridges. | capdag.test.js:2586 |
| test1874 | `test1874_registryUrlFromBuildEnvRejectsEmptyString` | TEST1874: an exported-but-empty env ('') is neither a dev build nor a valid identity and MUST fail hard, so the build can never silently hash the empty string into a fake registry slug. | capdag.test.js:2594 |
---

*Generated from JS source tree*
*Total tests: 344*
*Total numbered tests: 344*
*Total unnumbered tests: 0*
*Total numbered tests missing descriptions: 0*
*Total numbering mismatches: 0*

## Fontbakery report

Fontbakery version: 0.8.4

<details>
<summary><b>[15] PrintShoppe.ttf</b></summary>
<details>
<summary>🔥 <b>FAIL:</b> Checking file is named canonically.</summary>

* [com.google.fonts/check/canonical_filename](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/canonical_filename)
<pre>--- Rationale ---
A font&#x27;s filename must be composed in the following manner:
&lt;familyname&gt;-&lt;stylename&gt;.ttf
- Nunito-Regular.ttf,
- Oswald-BoldItalic.ttf
Variable fonts must list the axis tags in alphabetical order in square brackets
and separated by commas:
- Roboto[wdth,wght].ttf
- Familyname-Italic[wght].ttf</pre>

* 🔥 **FAIL** Style name used in "fonts/ttf/PrintShoppe.ttf" is not canonical. You should rebuild the font using any of the following style names: "Thin", "ExtraLight", "Light", "Regular", "Medium", "SemiBold", "Bold", "ExtraBold", "Black", "Thin Italic", "ExtraLight Italic", "Light Italic", "Italic", "Medium Italic", "SemiBold Italic", "Bold Italic", "ExtraBold Italic", "Black Italic". [code: bad-static-filename]

</details>
<details>
<summary>🔥 <b>FAIL:</b> Checking OS/2 fsType does not impose restrictions.</summary>

* [com.google.fonts/check/fstype](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/fstype)
<pre>--- Rationale ---
The fsType in the OS/2 table is a legacy DRM-related field. Fonts in the Google
Fonts collection must have it set to zero (also known as &quot;Installable
Embedding&quot;). This setting indicates that the fonts can be embedded in documents
and permanently installed by applications on remote systems.
More detailed info is available at:
https://docs.microsoft.com/en-us/typography/opentype/spec/os2#fstype</pre>

* 🔥 **FAIL** In this font fsType is set to 4 meaning that:
The font may be embedded, and temporarily loaded on the remote system, but documents that use it must not be editable.

No such DRM restrictions can be enabled on the Google Fonts collection, so the fsType field must be set to zero (Installable Embedding) instead. [code: drm]

</details>
<details>
<summary>🔥 <b>FAIL:</b> Check `Google Fonts Latin Core` glyph coverage.</summary>

* [com.google.fonts/check/glyph_coverage](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/glyph_coverage)
<pre>--- Rationale ---
Google Fonts expects that fonts in its collection support at least the minimal
set of characters defined in the `GF-latin-core` glyph-set.</pre>

* 🔥 **FAIL** Missing required codepoints: 0x0021 (EXCLAMATION MARK), 0x0022 (QUOTATION MARK), 0x0023 (NUMBER SIGN), 0x0024 (DOLLAR SIGN) and 156 more. [code: missing-codepoints]

</details>
<details>
<summary>🔥 <b>FAIL:</b> Check license file has good copyright string.</summary>

* [com.google.fonts/check/license/OFL_copyright](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/license/OFL_copyright)
<pre>--- Rationale ---
An OFL.txt file&#x27;s first line should be the font copyright e.g:
&quot;Copyright 2019 The Montserrat Project Authors
(https://github.com/julietaula/montserrat)&quot;</pre>

* 🔥 **FAIL** First line in license file does not match expected format: "copyright 20** the my font project authors (https://github.com/googlefonts/my-font-repository)"

</details>
<details>
<summary>🔥 <b>FAIL:</b> Check copyright namerecords match license file.</summary>

* [com.google.fonts/check/name/license](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/name/license)
<pre>--- Rationale ---
A known licensing description must be provided in the NameID 14 (LICENSE
DESCRIPTION) entries of the name table.
The source of truth for this check (to determine which license is in use) is a
file placed side-by-side to your font project including the licensing terms.
Depending on the chosen license, one of the following string snippets is
expected to be found on the NameID 13 (LICENSE DESCRIPTION) entries of the name
table:
- &quot;This Font Software is licensed under the SIL Open Font License, Version 1.1.
This license is available with a FAQ at: https://scripts.sil.org/OFL&quot;
- &quot;Licensed under the Apache License, Version 2.0&quot;
- &quot;Licensed under the Ubuntu Font Licence 1.0.&quot;
Currently accepted licenses are Apache or Open Font License.
For a small set of legacy families the Ubuntu Font License may be acceptable as
well.
When in doubt, please choose OFL for new font projects.</pre>

* 🔥 **FAIL** Font lacks NameID 13 (LICENSE DESCRIPTION). A proper licensing entry must be set. [code: missing]

</details>
<details>
<summary>🔥 <b>FAIL:</b> OS/2.fsSelection bit 7 (USE_TYPO_METRICS) is set in all fonts.</summary>

* [com.google.fonts/check/os2/use_typo_metrics](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/os2/use_typo_metrics)
<pre>--- Rationale ---
All fonts on the Google Fonts collection should have OS/2.fsSelection bit 7
(USE_TYPO_METRICS) set. This requirement is part of the vertical metrics scheme
established as a Google Fonts policy aiming at a common ground supported by all
major font rendering environments.
For more details, read:
https://github.com/googlefonts/gf-docs/blob/main/VerticalMetrics/README.md
Below is the portion of that document that is most relevant to this check:
Use_Typo_Metrics must be enabled. This will force MS Applications to use the
OS/2 Typo values instead of the Win values. By doing this, we can freely set the
Win values to avoid clipping and control the line height with the typo values.
It has the added benefit of future line height compatibility. When a new script
is added, we simply change the Win values to the new yMin and yMax, without
needing to worry if the line height have changed.</pre>

* 🔥 **FAIL** OS/2.fsSelection bit 7 (USE_TYPO_METRICS) wasNOT set in the following fonts: ['fonts/ttf/PrintShoppe.ttf']. [code: missing-os2-fsselection-bit7]

</details>
<details>
<summary>🔥 <b>FAIL:</b> Checking OS/2 Metrics match hhea Metrics.</summary>

* [com.google.fonts/check/os2_metrics_match_hhea](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/universal.html#com.google.fonts/check/os2_metrics_match_hhea)
<pre>--- Rationale ---
OS/2 and hhea vertical metric values should match. This will produce the same
linespacing on Mac, GNU+Linux and Windows.
- Mac OS X uses the hhea values.
- Windows uses OS/2 or Win, depending on the OS or fsSelection bit value.
When OS/2 and hhea vertical metrics match, the same linespacing results on
macOS, GNU+Linux and Windows. Unfortunately as of 2018, Google Fonts has
released many fonts with vertical metrics that don&#x27;t match in this way. When we
fix this issue in these existing families, we will create a visible change in
line/paragraph layout for either Windows or macOS users, which will upset some
of them.
But we have a duty to fix broken stuff, and inconsistent paragraph layout is
unacceptably broken when it is possible to avoid it.
If users complain and prefer the old broken version, they have the freedom to
take care of their own situation.</pre>

* 🔥 **FAIL** OS/2 sTypoAscender (800) and hhea ascent (1000) must be equal. [code: ascender]

</details>
<details>
<summary>🔥 <b>FAIL:</b> Font contains glyphs for whitespace characters?</summary>

* [com.google.fonts/check/whitespace_glyphs](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/universal.html#com.google.fonts/check/whitespace_glyphs)

* 🔥 **FAIL** Whitespace glyph missing for codepoint 0x00A0. [code: missing-whitespace-glyph-0x00A0]

</details>
<details>
<summary>⚠ <b>WARN:</b> Checking OS/2 achVendID.</summary>

* [com.google.fonts/check/vendor_id](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/vendor_id)
<pre>--- Rationale ---
Microsoft keeps a list of font vendors and their respective contact info. This
list is updated regularly and is indexed by a 4-char &quot;Vendor ID&quot; which is stored
in the achVendID field of the OS/2 table.
Registering your ID is not mandatory, but it is a good practice since some
applications may display the type designer / type foundry contact info on some
dialog and also because that info will be visible on Microsoft&#x27;s website:
https://docs.microsoft.com/en-us/typography/vendors/
This check verifies whether or not a given font&#x27;s vendor ID is registered in
that list or if it has some of the default values used by the most common font
editors.
Each new FontBakery release includes a cached copy of that list of vendor IDs.
If you registered recently, you&#x27;re safe to ignore warnings emitted by this
check, since your ID will soon be included in one of our upcoming releases.</pre>

* ⚠ **WARN** OS/2 VendorID value 'NONE' is not yet recognized. If you registered it recently, then it's safe to ignore this warning message. Otherwise, you should set it to your own unique 4 character code, and register it with Microsoft at https://www.microsoft.com/typography/links/vendorlist.aspx
 [code: unknown]

</details>
<details>
<summary>⚠ <b>WARN:</b> Font has old ttfautohint applied?</summary>

* [com.google.fonts/check/old_ttfautohint](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/old_ttfautohint)
<pre>--- Rationale ---
Check if font has been hinted with an outdated version of ttfautohint.</pre>

* ⚠ **WARN** ttfautohint used in font = 1.8.3; latest = 1.8.4; Need to re-run with the newer version! [code: old-ttfa]

</details>
<details>
<summary>⚠ <b>WARN:</b> Ensure fonts have ScriptLangTags declared on the 'meta' table.</summary>

* [com.google.fonts/check/meta/script_lang_tags](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/googlefonts.html#com.google.fonts/check/meta/script_lang_tags)
<pre>--- Rationale ---
The OpenType &#x27;meta&#x27; table originated at Apple. Microsoft added it to OT with
just two DataMap records:
- dlng: comma-separated ScriptLangTags that indicate which scripts, or languages
and scripts, with possible variants, the font is designed for
- slng: comma-separated ScriptLangTags that indicate which scripts, or languages
and scripts, with possible variants, the font supports
The slng structure is intended to describe which languages and scripts the font
overall supports. For example, a Traditional Chinese font that also contains
Latin characters, can indicate Hant,Latn, showing that it supports Hant, the
Traditional Chinese variant of the Hani script, and it also supports the Latn
script
The dlng structure is far more interesting. A font may contain various glyphs,
but only a particular subset of the glyphs may be truly &quot;leading&quot; in the design,
while other glyphs may have been included for technical reasons. Such a
Traditional Chinese font could only list Hant there, showing that it’s designed
for Traditional Chinese, but the font would omit Latn, because the developers
don’t think the font is really recommended for purely Latin-script use.
The tags used in the structures can comprise just script, or also language and
script. For example, if a font has Bulgarian Cyrillic alternates in the locl
feature for the cyrl BGR OT languagesystem, it could also indicate in dlng
explicitly that it supports bul-Cyrl. (Note that the scripts and languages in
meta use the ISO language and script codes, not the OpenType ones).
This check ensures that the font has the meta table containing the slng and dlng
structures.
All families in the Google Fonts collection should contain the &#x27;meta&#x27; table.
Windows 10 already uses it when deciding on which fonts to fall back to. The
Google Fonts API and also other environments could use the data for smarter
filtering. Most importantly, those entries should be added to the Noto fonts.
In the font making process, some environments store this data in external files
already. But the meta table provides a convenient way to store this inside the
font file, so some tools may add the data, and unrelated tools may read this
data. This makes the solution much more portable and universal.</pre>

* ⚠ **WARN** This font file does not have a 'meta' table. [code: lacks-meta-table]

</details>
<details>
<summary>⚠ <b>WARN:</b> Check if each glyph has the recommended amount of contours.</summary>

* [com.google.fonts/check/contour_count](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/universal.html#com.google.fonts/check/contour_count)
<pre>--- Rationale ---
Visually QAing thousands of glyphs by hand is tiring. Most glyphs can only be
constructured in a handful of ways. This means a glyph&#x27;s contour count will only
differ slightly amongst different fonts, e.g a &#x27;g&#x27; could either be 2 or 3
contours, depending on whether its double story or single story.
However, a quotedbl should have 2 contours, unless the font belongs to a display
family.
This check currently does not cover variable fonts because there&#x27;s plenty of
alternative ways of constructing glyphs with multiple outlines for each feature
in a VarFont. The expected contour count data for this check is currently
optimized for the typical construction of glyphs in static fonts.</pre>

* ⚠ **WARN** This check inspects the glyph outlines and detects the total number of contours in each of them. The expected values are infered from the typical ammounts of contours observed in a large collection of reference font families. The divergences listed below may simply indicate a significantly different design on some of your glyphs. On the other hand, some of these may flag actual bugs in the font such as glyphs mapped to an incorrect codepoint. Please consider reviewing the design and codepoint assignment of these to make sure they are correct.

The following glyphs do not have the recommended number of contours:

 - Glyph name: A	Contours detected: 0	Expected: 2
 - Glyph name: B	Contours detected: 0	Expected: 2 or 3
 - Glyph name: C	Contours detected: 0	Expected: 1
 - Glyph name: K	Contours detected: 0	Expected: 1 or 2
 - Glyph name: M	Contours detected: 0	Expected: 1
 - Glyph name: O	Contours detected: 0	Expected: 2
 - Glyph name: Q	Contours detected: 0	Expected: 2
 - Glyph name: S	Contours detected: 0	Expected: 1
 - Glyph name: V	Contours detected: 0	Expected: 1
 - Glyph name: W	Contours detected: 0	Expected: 1 or 2
 - Glyph name: a	Contours detected: 0	Expected: 2
 - Glyph name: b	Contours detected: 0	Expected: 2
 - Glyph name: c	Contours detected: 0	Expected: 1
 - Glyph name: d	Contours detected: 0	Expected: 2
 - Glyph name: e	Contours detected: 0	Expected: 2
 - Glyph name: f	Contours detected: 0	Expected: 1
 - Glyph name: g	Contours detected: 0	Expected: 2 or 3
 - Glyph name: h	Contours detected: 0	Expected: 1
 - Glyph name: i	Contours detected: 0	Expected: 2
 - Glyph name: j	Contours detected: 0	Expected: 2
 - Glyph name: k	Contours detected: 0	Expected: 1 or 2
 - Glyph name: l	Contours detected: 0	Expected: 1
 - Glyph name: m	Contours detected: 0	Expected: 1
 - Glyph name: n	Contours detected: 0	Expected: 1
 - Glyph name: o	Contours detected: 0	Expected: 2
 - Glyph name: p	Contours detected: 0	Expected: 2
 - Glyph name: q	Contours detected: 0	Expected: 2
 - Glyph name: r	Contours detected: 0	Expected: 1
 - Glyph name: s	Contours detected: 0	Expected: 1
 - Glyph name: t	Contours detected: 0	Expected: 1
 - Glyph name: u	Contours detected: 0	Expected: 1
 - Glyph name: v	Contours detected: 0	Expected: 1
 - Glyph name: w	Contours detected: 0	Expected: 1
 - Glyph name: x	Contours detected: 0	Expected: 1
 - Glyph name: y	Contours detected: 0	Expected: 1
 - Glyph name: z	Contours detected: 0	Expected: 1
 - Glyph name: A	Contours detected: 0	Expected: 2
 - Glyph name: B	Contours detected: 0	Expected: 2 or 3
 - Glyph name: C	Contours detected: 0	Expected: 1
 - Glyph name: K	Contours detected: 0	Expected: 1 or 2
 - Glyph name: M	Contours detected: 0	Expected: 1
 - Glyph name: O	Contours detected: 0	Expected: 2
 - Glyph name: Q	Contours detected: 0	Expected: 2
 - Glyph name: S	Contours detected: 0	Expected: 1
 - Glyph name: V	Contours detected: 0	Expected: 1
 - Glyph name: W	Contours detected: 0	Expected: 1 or 2
 - Glyph name: a	Contours detected: 0	Expected: 2
 - Glyph name: b	Contours detected: 0	Expected: 2
 - Glyph name: c	Contours detected: 0	Expected: 1
 - Glyph name: d	Contours detected: 0	Expected: 2
 - Glyph name: e	Contours detected: 0	Expected: 2
 - Glyph name: f	Contours detected: 0	Expected: 1
 - Glyph name: g	Contours detected: 0	Expected: 2 or 3
 - Glyph name: h	Contours detected: 0	Expected: 1
 - Glyph name: i	Contours detected: 0	Expected: 2
 - Glyph name: j	Contours detected: 0	Expected: 2
 - Glyph name: k	Contours detected: 0	Expected: 1 or 2
 - Glyph name: l	Contours detected: 0	Expected: 1
 - Glyph name: m	Contours detected: 0	Expected: 1
 - Glyph name: n	Contours detected: 0	Expected: 1
 - Glyph name: o	Contours detected: 0	Expected: 2
 - Glyph name: p	Contours detected: 0	Expected: 2
 - Glyph name: q	Contours detected: 0	Expected: 2
 - Glyph name: r	Contours detected: 0	Expected: 1
 - Glyph name: s	Contours detected: 0	Expected: 1
 - Glyph name: t	Contours detected: 0	Expected: 1
 - Glyph name: u	Contours detected: 0	Expected: 1
 - Glyph name: v	Contours detected: 0	Expected: 1
 - Glyph name: w	Contours detected: 0	Expected: 1
 - Glyph name: x	Contours detected: 0	Expected: 1
 - Glyph name: y	Contours detected: 0	Expected: 1 
 - Glyph name: z	Contours detected: 0	Expected: 1
 [code: contour-count]

</details>
<details>
<summary>⚠ <b>WARN:</b> Checking Vertical Metric Linegaps.</summary>

* [com.google.fonts/check/linegaps](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/hhea.html#com.google.fonts/check/linegaps)

* ⚠ **WARN** OS/2 sTypoLineGap is not equal to 0. [code: OS/2]

</details>
<details>
<summary>⚠ <b>WARN:</b> Are there any misaligned on-curve points?</summary>

* [com.google.fonts/check/outline_alignment_miss](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/<Section: Outline Correctness Checks>.html#com.google.fonts/check/outline_alignment_miss)
<pre>--- Rationale ---
This check heuristically looks for on-curve points which are close to, but do
not sit on, significant boundary coordinates. For example, a point which has a
Y-coordinate of 1 or -1 might be a misplaced baseline point. As well as the
baseline, here we also check for points near the x-height (but only for lower
case Latin letters), cap-height, ascender and descender Y coordinates.
Not all such misaligned curve points are a mistake, and sometimes the design may
call for points in locations near the boundaries. As this check is liable to
generate significant numbers of false positives, it will pass if there are more
than 100 reported misalignments.</pre>

* ⚠ **WARN** The following glyphs have on-curve points which have potentially incorrect y coordinates:
	* G (U+0047): X=294.0,Y=-1.5 (should be at baseline 0?)
	* H (U+0048): X=58.0,Y=-1.0 (should be at baseline 0?)
	* I (U+0049): X=58.0,Y=-1.0 (should be at baseline 0?)
	* J (U+004A): X=54.0,Y=-1.0 (should be at baseline 0?)
	* X (U+0058): X=70.0,Y=-1.0 (should be at baseline 0?)
	* X (U+0058): X=129.0,Y=-1.0 (should be at baseline 0?) and Y (U+0059): X=190.0,Y=-1.0 (should be at baseline 0?) [code: found-misalignments]

</details>
<details>
<summary>⚠ <b>WARN:</b> Are any segments inordinately short?</summary>

* [com.google.fonts/check/outline_short_segments](https://font-bakery.readthedocs.io/en/latest/fontbakery/profiles/<Section: Outline Correctness Checks>.html#com.google.fonts/check/outline_short_segments)
<pre>--- Rationale ---
This check looks for outline segments which seem particularly short (less than
0.6% of the overall path length).
This check is not run for variable fonts, as they may legitimately have short
segments. As this check is liable to generate significant numbers of false
positives, it will pass if there are more than 100 reported short segments.</pre>

* ⚠ **WARN** The following glyphs have segments which seem very short:
	* G (U+0047) contains a short segment B<<376.0,42.0>-<368.0,42.0>-<358.5,35.5>>
	* N (U+004E) contains a short segment B<<196.0,306.0>-<191.0,306.0>-<187.0,302.0>>
	* N (U+004E) contains a short segment B<<187.0,302.0>-<183.0,298.0>-<183.0,286.0>>
	* X (U+0058) contains a short segment B<<222.0,515.0>-<224.0,511.0>-<227.5,506.0>>
	* X (U+0058) contains a short segment B<<227.5,506.0>-<231.0,501.0>-<236.0,501.0>>
	* X (U+0058) contains a short segment B<<236.0,501.0>-<240.0,501.0>-<242.5,506.0>>
	* X (U+0058) contains a short segment B<<242.5,506.0>-<245.0,511.0>-<246.0,516.0>>
	* X (U+0058) contains a short segment B<<256.0,243.0>-<250.0,247.0>-<243.5,253.5>>
	* X (U+0058) contains a short segment B<<243.5,253.5>-<237.0,260.0>-<231.0,259.0>>
	* X (U+0058) contains a short segment B<<231.0,259.0>-<225.0,258.0>-<222.0,252.0>> and 7 more. [code: found-short-segments]

</details>
<br>
</details>

### Summary

| 💔 ERROR | 🔥 FAIL | ⚠ WARN | 💤 SKIP | ℹ INFO | 🍞 PASS | 🔎 DEBUG |
|:-----:|:----:|:----:|:----:|:----:|:----:|:----:|
| 0 | 8 | 7 | 122 | 7 | 76 | 0 |
| 0% | 4% | 3% | 55% | 3% | 35% | 0% |

**Note:** The following loglevels were omitted in this report:
* **SKIP**
* **INFO**
* **PASS**
* **DEBUG**

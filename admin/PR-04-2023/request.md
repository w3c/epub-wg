# Document titles, URLs, estimated publication dates

* EPUB 3.3
  * URL: https://www.w3.org/TR/epub-33/
  * Long URL: https://www.w3.org/TR/2023/PR-epub-33-20230413/
  * Editor's Draft: https://w3c.github.io/epub-specs/epub33/core/
  * Estimated Publication date: 2023-04-13
* EPUB 3.3 Reading Systems
  * URL: https://www.w3.org/TR/epub-rs-33/
  * Long URL: https://www.w3.org/TR/2023/PR-epub-rs-33-20230413/
  * Editor's Draft: https://w3c.github.io/epub-specs/epub33/rs/
  * Estimated Publication date: 2023-04-13
* EPUB Accessibility 1.1
  * URL: https://www.w3.org/TR/epub-a11y-11/
  * Long URL: https://www.w3.org/TR/2023/PR-epub-a11y-11-20230413/
  * Editor's Draft: https://w3c.github.io/epub-specs/epub33/a11y/
  * Estimated Publication date: 2023-04-13

# Abstract

* https://www.w3.org/TR/2023/PR-epub-33-20230413/#abstract
* https://www.w3.org/TR/2023/PR-epub-rs-33-20230413/#abstract
* https://www.w3.org/TR/2023/PR-epub-a11y-11-20230413/#abstract

# Status

* https://www.w3.org/TR/2023/PR-epub-33-20230413/#sotd
* https://www.w3.org/TR/2023/PR-epub-rs-33-20230413/#sotd
* https://www.w3.org/TR/2023/PR-epub-a11y-11-20230413/#sotd

# Will new features be allowed to be incorporated in the Recommendation?

No.

# Link to group's decision to request transition

* https://lists.w3.org/Archives/Public/public-epub-wg/2023Feb/0000.html

# Changes

* https://www.w3.org/TR/2023/PR-epub-33-20230413/#change-log
* https://www.w3.org/TR/2023/PR-epub-rs-33-20230413/#change-log
* https://www.w3.org/TR/2023/PR-epub-a11y-11-20230413/#change-log

# Requirements satisfied
Quoting from the main requirements in the WG charter:

> […] the interoperability of EPUB 3 content, and the conformance of EPUB 3 reading systems, remain a serious issue. There is a need for a more rigorous and comprehensive testing of EPUB 3; this may also mean the need for a further clarification of the standard text itself. […] The EPUB 3 Working Group will advance, refine, and clarify the EPUB 3 standard to ensure its relevance as digital publishing continues to evolve, and specify a comprehensive testing environment for EPUB 3.

The WG has:

* Reviewed, restructured, and updated the former EPUB 3.2 documents and made numerous changes to the texts for clarification, handling possible specification bugs, to make the specifications more precise. Although the change logs show many issues that have been handled (the change logs, together, contain references for over 120 substantial issues, i.e., these do not account for the purely editorial changes) only a handful of those are genuinely new technical features, mostly to answer to internationalization and to security issues.
* The working group has set up a functional testing environment to contribute to the interoperability of EPUB Reading Systems.
* The working group has published test results for 18 implementations.

The WG believes that fully satisfied the requirement for the clarifications needed in the specification, as well as establishing a comprehensive testing environment.

# Dependencies met (or not)

There were no major dependencies.

# Wide Review

Horizontal reviews:

See [horizontal review tracker](https://www.w3.org/PM/horizontal/review.html?shortname=epub).

* A11y Review:
  * [APA approves all three EPUB specifications](https://www.w3.org/2023/01/04-apa-minutes.html)
  * [a11y review issues](https://github.com/w3c/epub-specs/issues?q=is%3Aissue+sort%3Aupdated-desc+label%3Ai18n-tracker) (all closed)
* i18n Review:
  * [mail from Fuqiao](https://lists.w3.org/Archives/Group/group-epub-wg-chairs/2022Mar/0003.html)
  * [i18n-tracker issues](https://github.com/w3c/epub-specs/issues?q=is%3Aissue+author%3Ajasonjgw) (all closed)
  * [i18n-needs-resolution issues](https://github.com/w3c/epub-specs/issues?q=sort%3Aupdated-desc+label%3Ai18n-needs-resolution) (all closed)
* Privacy/Security Review:
  * [Privacy approval of approach](https://lists.w3.org/Archives/Public/public-epub-wg/2022Jun/0002.html)
  * [privacy-tracker issues](https://github.com/w3c/epub-specs/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc+label%3Aprivacy-tracker) (all closed)
  * [privacy issues](https://github.com/w3c/epub-specs/issues?q=is%3Aissue+label%3ACat-Privacy+) (all closed)
  * [security issues](https://github.com/w3c/epub-specs/issues?q=is%3Aissue+label%3ACat-Security+) (all closed)
  
  Note that the latest CR snapshot publication (21st February 2023) resulted in two additional issues: [#2542](https://github.com/w3c/epub-specs/issues/2542) and [#2548](https://github.com/w3c/epub-specs/issues/2548), which turned out to be essentially the same. They resulted in a [non-normative change](https://github.com/w3c/epub-specs/pull/2546) that satisfied the commenters.

* TAG Review:
  * [Issue on the WG repository](https://github.com/w3c/epub-specs/issues?q=is%3Aissue+author%3Arhiaro+)
  * [Issue on the TAG repository](https://github.com/w3ctag/design-reviews/issues/684), [closed by the TAG](https://github.com/w3ctag/design-reviews/issues/684#issuecomment-1091985272)

The WG discussions were conducted through github issues. The group took over the repository used to develop earlier versions of EPUB, and that meant ≈100 open issues at the time the Working Group started (September 2020); some of those were around for years. During the lifetime of the Working Group ≈499 issues were added, coming both from the wider community and the Working Group itself, with the participation of experts outside the group.


# Issues addressed

The change log items listing the substantial changes, i.e.:

* https://www.w3.org/TR/2023/PR-epub-33-20230413/#change-log
* https://www.w3.org/TR/2023/PR-epub-rs-33-20230413/#change-log
* https://www.w3.org/TR/2023/PR-epub-a11y-11-20230413/#change-log

include references to the issues that were addressed by those changes.

# Formal Objections

None.

# Implementation

The exit criteria of the Working Group are described in:

* https://w3c.github.io/epub-specs/epub33/reports/exit_criteria.html

Reports of the testing and implementation results can be found here:

* https://w3c.github.io/epub-specs/epub33/reports/index.html

There are numerous EPUB 3 Reading System implementations on the market, some major ones are represented on the Working Group (Google, Apple, Kobo, EDRLab, VitalSource, Colibrio, etc.). We have received testing results from all of these participants, and more. Also, the group has numerous contacts with Publishers, as well as accessibility organizations, who have contributed to the CR testing of, e.g., vocabularies.

Finally, there is a strong cooperation between the Working Group and the developers of EPUBCheck, that already has a beta version of an EPUB 3.3 checker. (This is particularly important, because epubcheck is used by virtually all publishers before releasing a new publication.) You can find results of EPUBCheck testing here: https://w3c.github.io/epub-structural-tests/

# Patent disclosures

* https://www.w3.org/groups/wg/epub/ipr

# Additional note on PR Transition

The [Working Group's charter](https://www.w3.org/2020/12/epub3-wg-charter.html) has a very strong clause on backwards compatibility:

> Any existing valid EPUB 3.2 should remain valid under EPUB 3.X, unless it relies on features discovered to have serious issues (such as a security bug).

What this means that the usual CR approach, whereby if a feature does not get the right number of implementation per the exit criteria must be removed from the specification, cannot be applied in this case. Instead, the WG has introduced a special category called ["under-implemented features"](https://www.w3.org/TR/epub-33/#under-implemented) to mark those features in the final publication.

Only one feature was found during testing to require this category: https://www.w3.org/TR/epub-33/#attrdef-dir. We have kept this feature in due to its importance for i18n support.

---
layout: default
---

# The practicalities of the self-publishing process for Working Drafts
{: .no_toc}

> **This guide is only valid for the publication of regular Working Drafts. Ie, not for FPWD, nor for Candidate Recommendations snapshots.**

Publishing the group’s Working Drafts is done via a combination of GitHub and a W3C tool called [Echidna](https://github.com/w3c/echidna/wiki). The high-level points to remember are described below.

1. Our repository ([`epub-spec`](https://github.com/w3c/epub-specs/)) contains all the EPUB 3.3 specification. They are all in the `epub33` folder. (The repository has an `archive` folder that contains earlier versions of EPUB 3.) The individual documents are in the various folders within `epub33` (`overview`, `core`, `rs`, `multi-rend`, `a11y`, and `a11y-tech`).
2. These folders can be reached via the “paging” feature of github, yielding the living editors’ drafts. E.g., the editors’ draft of the content document is at the `https://w3c.github.io/epub-specs/epub33/core/` URL.
3. There is a folder called `epub33/snapshot`, which has a a number of sub-folders, one for each document: `epub33/snapshot/epub-overview-33`, `epub33/snapshot/epub-33`, `epub33/snapshot/epub-rs-33`, `epub33/snapshot/epub-multi-rend-11`, `epub33/snapshot/epub-a11y-11`, and `epub33/snapshot/epub-a11y-tech-11`, respectively. These folder contain the final version of the respective documents, as generated from `respec`, plus the dependencies like css files and/or images.
4. There are _6 separate, special, branches_ in the repository: `publish-overview`, `publish-content`, `publish-rs`, `publish-multi-rend`, `publish-a11y`, and `publish-a11-tech`, corresponding to our six documents, respectively.
5. Every time the `main` branch is merged **_into_** one of the special branches (say, `publish_content`) and pushed to the repository, the document is picked up from the `snapshot` (i.e., from `epub33/snapshot/epub-33`), and is automatically published on the W3C site as the “latest version” of the official Working Draft.

What this means in practice is that the group can publish a Working Draft as often as its desires without any human intervention from the W3C staff.

The details of the process are below. (All the examples are on the content document, ie, on the core EPUB 3.3 specification. The other documents are handled the same way.)

* TOC
{:toc}


## Prepare the `respec` source

There is one requirement in the `respecConfig` data structure: the data of each editor _must_ include the `w3cid` field, identifying the person in the W3C database. This number appears on the page of the person’s profile page at W3C; alternatively, the staff contact can find it.

## Generate the final version of the document

The value of [`specStatus`](https://github.com/w3c/respec/wiki/specStatus) should _not_ be changed in the source; it should remain `ED`. Instead, when viewing the editor’s draft, the following URL (or its local equivalent if you use a local server) should be used: [`https://w3c.github.io/epub-specs/epub33/core/?specStatus=WD&publishDate=2021-03-01`](https://w3c.github.io/epub-specs/epub33/core/?specStatus=WD&publishDate=2021-03-01) (setting the publication date as appropriate). Using this URL overwrites the values defined in `respecConfig` and the result uses the right Working Draft format. The standard `respec` mechanism can be used to generate the final HTML to be put into the `snapshot/epub-33` folder.

## Update the Echidna manifest

There is a top level file called ECHIDNA in the snapshot folder, which contains a list of files to be included in the final publication. This file must be modified if new dependencies have been added (or removed) since the last publication. The relevant files themselves (e.g., images) _MUST_ be copied/updated to the snapshot folder manually.

## Check the document

It is _required_ to run the document through the [W3C pubrules’ checker](https://www.w3.org/pubrules/) and _recommended_ to run it through the [W3C link checker](https://validator.w3.org/checklink). For both cases, the URL to the snapshot folder’s content should be used: [`https://w3c.github.io/epub-specs/epub33/snapshot/epub-33/`](https://w3c.github.io/epub-specs/epub33/snapshot/epub-33/).

Note that, if the ECHIDNA file is incomplete (i.e., some resources are _not_ listed) but the corresponding file is present in the folder, the link checker will be successful and, nevertheless, the final publication may miss some links (indeed, the relevant resources are not copied to the target directory on the W3C server). Worth checking the final publication…

## Merge the `main` branch into the corresponding publishing branch (e.g., `publish_content`)

(It is probably a good practice do this on one’s local machine, using a preferred Git(Hub) interface. The changes should then be committed onto GitHub.)

The publication is done; the new version should appear as [`https://www.w3.org/TR/epub-33/`](https://www.w3.org/TR/epub-33/). It is worth checking the [`public-tr-notifications`](https://lists.w3.org/Archives/Public/public-tr-notifications/) mailing list archive to see if everything is o.k.; successful publications or errors are sent to that list.

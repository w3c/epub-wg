---
layout: minutes
date: 2021-04-21
title: EPUB 3 Working Group Virtual Locators Task Force Telco — 2021-04-21
json-ld: |
    {
        "@context": [
            "https://schema.org",
            {
                "resolution": {
                    "@id": "https://w3c.github.io/scribejs/vocab/resolution",
                    "@context": {
                        "@vocab": "https://w3c.github.io/scribejs/vocab/"
                    }
                },
                "irc": {
                    "@id": "https://w3c.github.io/scribejs/vocab/irc"
                }
            }
        ],
        "@type": "CreativeWork",
        "url": "https://www.w3.org/publishing/groups/epub-wg/Meetings/Minutes/2021-04-21-epub-a11y",
        "name": "EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes",
        "about": "EPUB 3 Working Group Virtual Locators Task Force Telco",
        "dateCreated": "2021-04-21",
        "irc": "epub-locators",
        "datePublished": "2021-04-21",
        "genre": "Meeting Minutes",
        "accessMode": "textual",
        "accessModeSufficient": "textual",
        "encodingFormat": "text/html",
        "publisher": {
            "@type": "Organization",
            "name": "World Wide Web Consortium",
            "url": "https://www.w3.org/"
        },
        "inLanguage": "en-US",
        "recordedAt": {
            "@type": "Event",
            "name": "EPUB 3 Working Group Virtual Locators Task Force Telco",
            "startDate": "2021-04-21",
            "endDate": "2021-04-21",
            "location": {
                "@type": "VirtualLocation",
                "description": "Teleconference"
            },
            "attendee": [
                {
                    "@type": "OrganizationRole",
                    "roleName": "chair",
                    "attendee": [
                        {
                            "@type": "Person",
                            "name": "Wendy Reid"
                        }
                    ]
                },
                {
                    "@type": "OrganizationRole",
                    "roleName": "scribe",
                    "attendee": [
                        {
                            "@type": "Person",
                            "name": "Ronnie Seagren"
                        }
                    ]
                },
                {
                    "@type": "Person",
                    "name": "Dave Cramer"
                },
                {
                    "@type": "Person",
                    "name": "Ivan Herman"
                },
                {
                    "@type": "Person",
                    "name": "Brady Duga"
                },
                {
                    "@type": "Person",
                    "name": "Dan Lazin"
                },
                {
                    "@type": "Person",
                    "name": "Ben Schroeter"
                },
                {
                    "@type": "Person",
                    "name": "Pilar Wyman"
                },
                {
                    "@type": "Person",
                    "name": "Charles LaPierre"
                }
            ]
        }
    }

---

# EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes
{: .no_toc}



**Date:** 2021-04-21

See also the [Agenda]() and the [IRC Log](https://www.w3.org/2021/04/21-epub-locators-irc.txt)

## Attendees
{: .no_toc}
**Present:** Dave Cramer, Wendy Reid, Ronnie Seagren, Ivan Herman, Brady Duga, Dan Lazin, Ben Schroeter, Pilar Wyman, Charles LaPierre

**Regrets:** Tzviya Siegman

**Guests:** 

**Chair:** Wendy Reid

**Scribe(s):** Ronnie Seagren

## Content:
{: .no_toc}

* TOC
{:toc}
---


> *Wendy Reid:* See [news about some new, relevant feature in Chrome](https://www.theverge.com/2021/4/17/22389519/google-feature-chrome-90-highlighted-links)

> *Dan Lazin:* So for Wendy's link above, here is what a link-to-text anchor looks like: [https://www.theverge.com/2021/4/17/22389519/google-feature-chrome-90-highlighted-links#:~:text=already-,available,-on](https://www.theverge.com/2021/4/17/22389519/google-feature-chrome-90-highlighted-links#:~:text=already-,available,-on)

**Dan Lazin:** direct-to-text anchor: Chrome 89 or later when you click it, and it appears in yellow. Only on Chrome.  
… Obvious problem of being non-stable, if the text changes, it doesn't work anymore.  

> *Dan Lazin:* [https://www.macrumors.com/how-to/link-to-highlighted-text-webpage-chrome/#:~:text=Unfortunately%2C%20the%20highlight%20links%20that%20Chrome%20generates%20only%20work%20in%20Edge%20and%20Chrome%2C%20therefore%20users%20running%20other%20browsers%20won%27t%20see%20the%20highlighted%20text.%20However%2C%20they%27ll%20still%20be%20sent%20to%20the%20webpage%20in%20question%2C%20so%20the%20link%20isn%27t%20completely%20useless%20to%20Safari%20o[CUT]](https://www.macrumors.com/how-to/link-to-highlighted-text-webpage-chrome/#:~:text=Unfortunately%2C%20the%20highlight%20links%20that%20Chrome%20generates%20only%20work%20in%20Edge%20and%20Chrome%2C%20therefore%20users%20running%20other%20browsers%20won%27t%20see%20the%20highlighted%20text.%20However%2C%20they%27ll%20still%20be%20sent%20to%20the%20webpage%20in%20question%2C%20so%20the%20link%20isn%27t%20completely%20useless%20to%20Safari%20o[CUT])

**Dan Lazin:** This link is from a paragraph.  
… It's quite the URL but it works, but only in Chrome. It might become standardized but not yet  

**Ivan Herman:** It gives the paragraph before in yellow.  

**Dan Lazin:** That might be because of 89; it was announced in 90.  

> *Dave Cramer:* spec: [https://wicg.github.io/scroll-to-text-fragment/](https://wicg.github.io/scroll-to-text-fragment/)

> *Dave Cramer:* Mozilla standards position on this: [https://github.com/mozilla/standards-positions/issues/194](https://github.com/mozilla/standards-positions/issues/194)

> *Dave Cramer:* See [TAG review](https://github.com/w3ctag/design-reviews/issues/392)

**Ivan Herman:** Implementation details still needed. This reminds me of meta-structure to describe anchors in an old annotation WG spec.  

> *Ivan Herman:* See [Selectors, from the Web Annotation spec](https://www.w3.org/TR/selectors-states/)

> *Ivan Herman:* See [Extension Note of selectors for publications](https://www.w3.org/TR/wpub-ann/)

**Ivan Herman:** This is a metastructure that describes various ways you can select things in a resource ... text or something preceded or followed by something, or an SVG window, etc. Giving you a unified JSON structure to select it. And then in this node there's a nonstandard way to turn it into a URL. At least part has been implemented by Hypothes.is, but not the URL part, which is just a thought exercise. In the web publishing WG we added some extra features to access a document within a collection.  
… you want to find a text preceded and followed by something.  

**Wendy Reid:** bottom line: we're not the only people working on this ...  

> *Wendy Reid:* [https://docs.google.com/document/d/1y5JKcwlq1rvGYJ1HoLg0GF-NRiBsBNNZopGuQ0mgHUw/edit](https://docs.google.com/document/d/1y5JKcwlq1rvGYJ1HoLg0GF-NRiBsBNNZopGuQ0mgHUw/edit)

**Ben Schroeter:** there's a page with examples of use cases. It's in the Google Doc above.  

**Wendy Reid:** we looked at all the use cases and divided them into groupings; the bulk fit into one on specific locations - reference one or guide people to that, and offer affordances for a browser of OS to generate them efficiently.  
… so we looked at CFI next  
… couldn't get the list to stop numbering  

**Ivan Herman:** Where do we go from here? We can't solve the general case for the whole web.  

**Dan Lazin:** It's problematic that so many others are working on this at the same time. Chrome is working on it and we have 3 W3 specs here, but none of them fully exists. A nice summary of where we are.  

**Ivan Herman:** We could say "use ePub CFI"  

**Brady Duga:** 3 people are trying to solve a related but different problem. None of them are what we're trying to solve. Fix the fact that there are no anchors. For indexing or sharing info with people in a class - these aren't solved.  
… maybe we should wait, but that's worrisome. I do agree we don't need another spec that won't get adopted.  

**Ben Schroeter:** Is a CFI reading system agnostic?  

**Wendy Reid:** Yes  

**Ben Schroeter:** CFI is unreadable for humans and impossible for authors or indexers to use it because it's unreadable.  
… It's perfectly possible for a reading system to use it internally. But who cares about having it as a standard then?  

**Brady Duga:** CFI has some technical issues, some could be corrected by tooling. CFI's problem is there is no business case for it.  
… Therefore, it hasn't been adopted. Product managers haven't said we really need elaborate indexes to work.  
… Other things take precedence, not technical capacity.  

**Pilar Wyman:** That would be an argument for publishing the use cases  

**Wendy Reid:** It depends on the framing. If you do this you can implement x-platform sharing, allowing book club members to reference the same quote  

**Pilar Wyman:** we need to angle it to how do they make money?  

**Ivan Herman:** What is the implementation level of CFI?  

**Brady Duga:** No one knows, not external.  

**Ivan Herman:** If we have a use case document and we refresh the IDPF document as a note (not a recommendation). There's a hope that might push it to implementation. Or is it a fancy dream  

**Brady Duga:** No one knows how to write CFI, won't do it till the reading systems implement it, and the publishers won't yet ... It's a vicious cycle, hard to evolve till the pieces are implemented.  
… we could do it, but there's no incentive to expose it in the UI and deal with the resulting hassles.  

**Ben Schroeter:** Reading systems use deep linking currently to interface with management systems, from your syllabus you can deep-link to a specific paragraph.  
… Assumed they were using CFIs to do that, but maybe something else. There must be some implementation now that affords that use case.  

**Ivan Herman:** I fully understand Brady's point, but I'm trying to be more optimistic.  
… If the working group refreshes the requirements and publishes it as a note, it draws attention to it and gives the message that it would be good to do it for these reasons.  
… For the time being it's completely forgotten. It's the only thing we have.  

> *Ben Schroeter:* See [Another (IMS) document of interest](https://www.imsglobal.org/spec/lti-dl/v2p0)

**Charles:** Isn't ePub ACE already using CFIs for where the images are and the list of violations?  
… Are we already doing it but don't have a way to access it?  

> *Charles LaPierre:* Here is an example from ACE -  
> `s9ml/chapter01/untitled_page_1.xhtml#epubcfi(/4/2[data-uuid-fb63c7f4d81a47f4a862351ff8e9d269]/8[data-uuid-70aed7f318c045ed8db490083a691b93]/8[data-uuid-e72dd28118af47dea3d815bcb0a85324]/2)`

**Brady Duga:** One problem with CFI is you really want it when you don't control the content. If you control the content to generate an index, just insert spans with anchors used by the index entries.  
… mostly useful when I don't create the content. Most of uses don't matter if I don't have a universal identifier.  
… How much use is there for CFI therefore?  

**Dan Lazin:** Annotate our use cases based on which involve controlling the content. Indexers do. Book club, students, reading system don't.  
… If there are various efforts to solve the problem and we have a partial solution through CFI and make partial progress and defer the rest till there's a clearer answer.  
… CFI has broad usage but not reader-friendly, maybe we could make them more friendly with a dictionary. Let Chrome figure out their anchor thing separately.  

**Wendy Reid:** I like this idea.  

**Dan Lazin:** This feels like offline work on a spreadsheet. The tool at the end of the chain gives the affordances. Indexers are much more at the beginning.  
… Locator provided by reading system or by author, another dimension.  

> *Dan Lazin:* We are basically making a table like this: [https://en.wikipedia.org/wiki/Comparison_of_e-readers#Electronic-paper_displays](https://en.wikipedia.org/wiki/Comparison_of_e-readers#Electronic-paper_displays)

**Ivan Herman:** The stability of the pointers is also another dimension. Books sometimes change slightly. CFI is very bad at that. Whether a tool is stable against change or not is important.  

**Pilar Wyman:** Increasingly ePub texts don't have enough anchors. If you have section numbers or paragraph numbers, but many don't.  

**Ivan Herman:** Technically speaking, that's not enough. If you just have text, you still need anchors for identifiers.  

**Pilar Wyman:** Point taken. Do we have an additional use case, that has section or paragraph numbers but just needs the linking put in? That's different for text without any.  

**Ivan Herman:** The content is in HTML. The real problem is the missing anchors, not the missing structure.  

**Pilar Wyman:** In an index you need the anchor and what you'll call it for the anchors.  

**Wendy Reid:** Do we create an algorithm that numbers the `<p>` tags. But then you need to label it.  

**Dan Lazin:** In a print book index, the label is a page number.  

**Pilar Wyman:** or line numbers in poetry or section for legal text.  

**Dan Lazin:** As discussed on page x, y, z - they don't mean anything in ePub. They work nicely as labels for anchors in text.  

**Brady Duga + Dan Lazin:** What three words is a fine solution. Order numbers are done like that.

**Wendy Reid:** Netlify assigns domains based on that as well.  

**Brady Duga:** Not very international  

**Dan Lazin:** Multiple dictionaries could resolve to the same CFI thing.  

**Brady Duga:** Responding to Ivan. CFI is fairly stable across changes. The path could include all the IDs, text as well. As long as you leave the paragraph IDs in place, it's OK with modifications for the content. It breaks only if you change the IDs. The horrible path could include all the interim IDs.  

**Ivan Herman:** In the CFI itself you encode the path in the doc. If I add a new `<p>` in the middle, all the CFIs pointing to a later paragraph will be wrong.  

**Brady Duga:** Worst case if there are no IDs, but even then you could include text from the target, you could look for it in a neighboring paragraph.  

**Ivan Herman:** That's a runtime implementation. It's not in the spec. There's a way to implementing a redirection, but the original identifier is incorrect in a way.  
… That means if we did a note, we'd have to describe the processing.  

**Brady Duga:** The processing model was considered too risky to include, but there should be one.  

**Ivan Herman:** What's the next step?  

**Wendy Reid:** Identify which use cases intersect at which specific points: control or lack of control; creates and uses the locators.  
… Google Doc isn't good for this, a sheet will work.  

**Pilar Wyman:** If an indexer wants to use the CFIs as targets, how to label them in the index?  
… CFIs don't show up to human reader  

**Ivan Herman:** A URL isn't there for the human reader either.  

**Pilar Wyman:** If the indexer wants to use the embedded index tags, how should they be labelled?  

**Wendy Reid:** Pilar will add this one.  

**Dan Lazin:** We shouldn't prejudge this. But from responsiveness to the original feature request and ePub spec, we won't solve page numbers.  
… We might have a better web focus.  
… We might have a better web solution. We need a way to refer to "page" locators.  

**Pilar Wyman:** Indexers were largely fine with using the paragraph numbers in production, but how long will they last?  

**Ivan Herman:** I have a script that turns W3 recommendations into ePub. No page numbers.  

**Wendy Reid:** w3C recommendations are better prepared, because of section numbering. The audiobook spec can refer to subsections.  
… Two things we want to figure out: 1) how do we make these references? visually to the user, the author, the indexer? 2) also a visual representation of the locators semantically.  
… Breaking up the use cases by control. Also, what could we take from CFI to make it a parsable property?  

**Ivan Herman:** You don't want an average human to see a URL and parse that either.  

**Wendy Reid:** I know a URL means this site, this page  

**Brady Duga:** Sortable feature of CFI. Any label that I can look at and see if it's later is helpful.  

**Pilar Wyman:** Sequential and also size. The equivalent of a page range for a large section or a small subsection.  

**Ivan Herman:** CFI won't get that, only the sort.  

**Pilar Wyman:** Label show a beginning and an ending?  

> *Wendy Reid:* [https://docs.google.com/spreadsheets/d/1KO-HyLGUUw36F-ruAARHNiPO1aUJCCNeTv3zxGtjuHw/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1KO-HyLGUUw36F-ruAARHNiPO1aUJCCNeTv3zxGtjuHw/edit?usp=sharing)

**Wendy Reid:** Page numbers are semantically rich  
… I created a spreadsheet where we can resort the use cases.  

**Pilar Wyman:** I'll add my use case to the Google Doc.  

**Wendy Reid:** We need to make CFI more human readable or to have a more human readable equivalent.  

**Dan Lazin:** Presentation is an issue. We have to thinking about how books work. I was imagining an index where each thing is collapsed by default, you'd see a window to the page that shows the options.  

**Pilar Wyman:** Dan, what you described was in the last ePub spec for indexes.  

---

---
layout: minutes
date: 2021-06-02
title: Virtual Locators TF Telco June 2, 2021 — 2021-06-02
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
        "url": "https://www.w3.org/publishing/groups/epub-wg/Meetings/Minutes/2021-06-02-epub-a11y",
        "name": "Virtual Locators TF Telco June 2, 2021 — Minutes",
        "about": "Virtual Locators TF Telco June 2, 2021",
        "dateCreated": "2021-06-02",
        "irc": "epub-locators",
        "datePublished": "2021-06-03",
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
            "name": "Virtual Locators TF Telco June 2, 2021",
            "startDate": "2021-06-02",
            "endDate": "2021-06-02",
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
                            "name": "Ben Schroeter"
                        }
                    ]
                },
                {
                    "@type": "Person",
                    "name": "Ronnie Seagren"
                },
                {
                    "@type": "Person",
                    "name": "Mary Coe"
                },
                {
                    "@type": "Person",
                    "name": "Dan Lazin"
                }
            ]
        }
    }

---

# Virtual Locators TF Telco June 2, 2021 — Minutes
{: .no_toc}



**Date:** 2021-06-02

See also the [Agenda]() and the [IRC Log](https://www.w3.org/2021/06/02-epub-locators-irc.txt)

## Attendees
{: .no_toc}
**Present:** Wendy Reid, Ronnie Seagren, Ben Schroeter, Mary Coe, Dan Lazin

**Regrets:** 

**Guests:** 

**Chair:** Wendy Reid

**Scribe(s):** Ben Schroeter

## Content:
{: .no_toc}

* TOC
{:toc}
---


> *Wendy Reid:* [https://docs.google.com/spreadsheets/d/1KO-HyLGUUw36F-ruAARHNiPO1aUJCCNeTv3zxGtjuHw/edit#gid=0](https://docs.google.com/spreadsheets/d/1KO-HyLGUUw36F-ruAARHNiPO1aUJCCNeTv3zxGtjuHw/edit#gid=0)

**Wendy Reid:** scoping our use cases  
… two so far:  
… A teacher wants to ask students to go to a certain location in an EPUB which contains no explicit page-list. The students are using different types of reading systems, nevertheless all reach the same page.  
… A student or other academic wants to cite an ebook, including location.  
… we've discounted several original use cases including bookmarking and deep linking as out of scope for this effort  
… What others shall we include?  
… Folks in a book club want to refer to consistent locations in the text. They might be all reading ebooks, because it's 2046, but each user's ebook of course flows somewhat differently.  

**Dan Lazin:** yes if same version/edition of the publication  

**Wendy Reid:** next use case is interesting: A student who is reading "The Lottery" in the Norton Anthology of English Literature wants to refer to a specific location in the text when talking to another student who read the story in The Collected Works of Shirley Jackson (i.e. common locators within a "chapter" instead of a book).  
… this is a "stretch case"  

**Mary Coe:** this goes beyond what can be done today with print  

**Wendy Reid:** yes in this case we might be able to improve upon current print capabilities  

**Ben Schroeter:** I don't see how we can implement this using the techniques discussed, but we don't need to solution here.  

**Wendy Reid:** An indexer wants to link a term in an index to its exact location in the book, not just the top of an artificial page. Note that the term does not necessarily occur on the page verbatim — could be a synonym or concept.  
… for this to work, the indexer would need to provide a hook to the ingestion system of a reading system  

**Ronnie Seagren:** the index entry is marked in the file, so the reading system can find it  

**Dan Lazin:** indexer becomes responsible for adding a page list if there isn't one  

**Wendy Reid:** it would be difficult to ask an ingestion pipeline to process and generate an index  

**Ronnie Seagren:** indexes should be embedded (hotlinked)  

**Wendy Reid:** ok in scope  
… An indexer wants to link an index entry to a range in the book, meaning that the entry refers to the content beginning at the first location and ending at the second location.  

**Mary Coe:** this is aspirational  

**Wendy Reid:** ok might be in scope  
… An indexer is writing and embedding an index for an ebook and needs labels for locator links. (When the ebook includes section numbers, line numbers, or paragraph numbers, they can use those numbers as labels for locator links, but when the text doesn’t have such labels for anchors [CFI or other tagging], they need new labels.)  
… In scope.  
… A machine translation system wants to offer the reader the option of seeing the original source text for a phrase (or, for that matter, tracking consistent "page numbers" across different languages). Note that word order may change between languages, so unlike the lawyer, the translation system cannot just count words; for example, in "I washed my green car" > "J'ai lavé ma voiture verte," the color has moved from word [CUT]  
… out of scope for page numbers but interesting for enhanced cfi's  
… A desktop publishing system like InDesign, or maybe a packaging script, or maybe a reading system, wants to autogenerate locators to ease the pain of authoring EPUBs. (Really, this "use case" is representing the question of where this data is generated. If the RS can do it consistently and automatically, that's best — less work and guaranteed to exist — but also less control.)  
… this use case moves the insertion of locators from the reading system to the authoring tool  
… but the reading system ingestion would have to process these instructions  
… maybe locations get added at the aggregators?  
… for now, let's not get hung up on where this needs to happen.  
… looks like we have our core use cases. I will take the action of putting them into our core document and might alter phrasing to make user stories out of them.  
… next week we can hold them up vs. our proposed virtual locators scheme.  

---

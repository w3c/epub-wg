---
layout: minutes
date: 2021-09-17
title: EPUB 3 Working Group Virtual Locators Task Force Telco — 2021-09-17
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
        "url": "https://www.w3.org/publishing/groups/epub-wg/Meetings/Minutes/2021-09-17-epub-locators",
        "name": "Virtual Locators TF Telco — Minutes",
        "about": "Virtual Locators TF Telco",
        "dateCreated": "2021-09-17",
        "irc": "epub-locators",
        "datePublished": "2021-09-17",
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
            "name": "Virtual Locators TF Telco",
            "startDate": "2021-09-17",
            "endDate": "2021-09-17",
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
                            "name": "Dan Lazin"
                        }
                    ]
                },
                {
                    "@type": "Person",
                    "name": "Pilar Wyman"
                },
                {
                    "@type": "Person",
                    "name": "Tzviya Siegman"
                },
                {
                    "@type": "Person",
                    "name": "Ivan Herman"
                },
                {
                    "@type": "Person",
                    "name": "George Kerscher"
                },
                {
                    "@type": "Person",
                    "name": "Laurent Le Meur"
                }
            ]
        }
    }

---

# EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes
{: .no_toc}



**Date:** 2021-09-17

See also the [Agenda]() and the [IRC Log](https://www.w3.org/2021/09/17-epub-locators-irc.txt)

## Attendees
{: .no_toc}
**Present:** Pilar Wyman, Tzviya Siegman, Wendy Reid, Ivan Herman, George Kerscher, Laurent Le Meur, Dan Lazin

**Regrets:** Brady Duga, Ben Schroeter

**Guests:** 

**Chair:** Wendy Reid

**Scribe(s):** Dan Lazin

## Content:
{: .no_toc}

* TOC
{:toc}
---


**Dan Lazin:** Why didn't this taskforce come around sooner?  
… Why has this problem not been solved in 20 years?  

**Tzviya Siegman:** We've been trying to solve this problem for years, and the indexing specification tried to solve it.  
… This came to be from figuring out which parts of the satellite specifications could be brought into the master spec.  
… Indexes has a lot of useful information but there's nothing normative in the spec.  

**Wendy Reid:** We did a survey and asked people what their interests were and page-numbering came up a lot.  
… Also we have two open issues about page numbers.  

**Ivan Herman:** The whole issue about annotating webpages or pages in a book has been around for 10 or 15 years and browsers never took it seriously.  
… There is a [web annotations recommendation](https://www.w3.org/TR/annotation-model/) that could solve this problem but it is not implemented in browsers.  
… What the task force is doing is saying "the ideal thing is not implemented. What is the suboptimal thing that we can do?"  

> *Tzviya Siegman:* 

**Ivan Herman:** Browsers still require that there be IDs in the document for anchors.  

**George Kerscher:** The problem gets worse with screen readers, because they read from a virtual buffer, not the real HTML.  

**Dan Lazin:** There was also an issue about textbook pages that created this task force ... but I guess it just pushed us over the edge.  

> *Dan Lazin:* Here's what Chrome is doing now: [https://www.macrumors.com/how-to/link-to-highlighted-text-webpage-chrome/](https://www.macrumors.com/how-to/link-to-highlighted-text-webpage-chrome/)

**Wendy Reid:** I spoke to my team of UX designers and one of the problems we've been running into is "what do automatic page numbers look like?"  
… I took screenshots from various applications to see how they handle page numbers ... and everyone does it differently. So we have a long way to go.  
… My team got really into it, but I'm still working on it. Might have a presentation for you next time.  

### 1. Continue work on the Note
{: #section1}

> *Wendy Reid:* [https://docs.google.com/document/d/11GypOjE9xOTaINATl5bxVIA3Mc9jzNBGCr6GT_KNaQ4/edit#heading=h.gbsmtjlkuon](https://docs.google.com/document/d/11GypOjE9xOTaINATl5bxVIA3Mc9jzNBGCr6GT_KNaQ4/edit#heading=h.gbsmtjlkuon)

**Wendy Reid:** So let's continue to write the note.  

**Dan Lazin:** Arbitrarily, let's fill out the Format and Persistence section.  

> *Wendy Reid:* [editing the document]

**Dan Lazin:** (See changes in Google Doc to understand discussion.)  

> *Wendy Reid:* [notes from Readium discussions on this topic]

> *Wendy Reid:* [https://github.com/readium/architecture/issues/123](https://github.com/readium/architecture/issues/123)

> *Wendy Reid:* [https://github.com/readium/r2-streamer-swift/pull/209#issuecomment-859346247](https://github.com/readium/r2-streamer-swift/pull/209#issuecomment-859346247)

---

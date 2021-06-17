---
layout: minutes
date: 2021-06-16
title: EPUB 3 Working Group Virtual Locators Task Force Telco — 2021-06-16
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
        "url": "https://www.w3.org/publishing/groups/epub-wg/Meetings/Minutes/2021-06-16-epub-locators",
        "name": "EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes",
        "about": "EPUB 3 Working Group Virtual Locators Task Force Telco",
        "dateCreated": "2021-06-16",
        "irc": "epub-locators",
        "datePublished": "2021-06-17",
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
            "startDate": "2021-06-16",
            "endDate": "2021-06-16",
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
                            "name": "Pilar Wyman"
                        },
                        {
                            "@type": "Person",
                            "name": "Wendy Reid"
                        }
                    ]
                },
                {
                    "@type": "Person",
                    "name": "Toshiaki Koike"
                },
                {
                    "@type": "Person",
                    "name": "Ben Schroeter"
                },
                {
                    "@type": "Person",
                    "name": "Shinya Takami (高見真也)"
                },
                {
                    "@type": "Person",
                    "name": "Dan Lazin"
                }
            ]
        }
    }

---

# EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes
{: .no_toc}



**Date:** 2021-06-16

See also the [Agenda]() and the [IRC Log](https://www.w3.org/2021/06/16-epub-locators-irc.txt)

## Attendees
{: .no_toc}
**Present:** Wendy Reid, Toshiaki Koike, Pilar Wyman, Ben Schroeter, Shinya Takami (高見真也), Dan Lazin

**Regrets:** 

**Guests:** 

**Chair:** Wendy Reid

**Scribe(s):** Pilar Wyman, Wendy Reid

## Content:
{: .no_toc}

* TOC
{:toc}
---


### 1. Japanese reading system's behaviour
{: #section1}

**Wendy Reid:** summarizing last meeting and noting we are unclear on Japanese reading systems and how they are handling page lists and lack thereof in ebooks. Do they want page #s?  

**Toshiaki Koike:** VOYAGER'S Reading System converts from EPUB to internal format, and to identify the location, use both the number of characters from the beginning and text strings around the location, then if the contents modify a little, Reading System can trace the original location.  
… And about page number, our RS renders all pages when opening the book, resizing window, and resizing font size, then has the index of pages.  

**Wendy Reid:** do pages get rendered again when font changes?  

**Pilar Wyman:** I was asking about the use of the term index, how do you handle ebooks that have an index with listing of page numbers or locations  

**Toshiaki Koike:** sharing screenshot from reading system, position in text (from beginning) is used for indicating location.  

**Wendy Reid:** is this unique? or is it common to other reading systems?  

**Shinya Takami (高見真也):** Voyager is doing its own thing, and other vendors in Japan seem to have each their own system.  

**Wendy Reid:** bookmarking systems all rely on span tags  

### 2. Locator Note
{: #section2}

> *Wendy Reid:* See [current draft of the note](https://w3c.github.io/epub-specs/epub33/locators/)

> *Wendy Reid:* See [reference to the github source](https://github.com/w3c/epub-specs/blob/main/epub33/locators/index.html)

**Dan Lazin:** we can start drafting a note, which will help us focus and move forward. the actual algorithm itself is essentially an appendix.  
… sample note we can follow?  

**Wendy Reid:** similar style to specs, with supportive text, more than usual  
… will be good to say why current options don't work  
… review will not happen, rigor will apply should it be deemed acceptable to go ahead.  

**Pilar Wyman:** My question was about the abstract, it doesn't seem clear  

**Wendy Reid:** common writing program such as Google Docs might be appropriate  

**Dan Lazin:** we will ask page lists be included. algorithm for figuring alternative locators is secondary.  

**Wendy Reid:** google and Adobe have similar approaches for designating where text is in an epub. readium does similar, compressed though.  
… "adobe page numbers"  
… internationalization group should be first reviewers of whatever we draft.  
… fixed-layout has page numbers, page list, but we should consider it as well  

**Dan Lazin:** let's put in outline  

> *Wendy Reid:* [https://docs.google.com/document/d/11GypOjE9xOTaINATl5bxVIA3Mc9jzNBGCr6GT_KNaQ4/edit?usp=sharing](https://docs.google.com/document/d/11GypOjE9xOTaINATl5bxVIA3Mc9jzNBGCr6GT_KNaQ4/edit?usp=sharing)

**Ben Schroeter:** MobileRead wiki discussed all this, but it way out of date  

**Pilar Wyman:** 2 things, being a large number can interfere with index entries  
… readers could get frustrated  
… if the page they're looking for is many "screens"  
… phrasing of "absolute page numbers"  
… we're talking about a page number that doesn't change that's available to readers  

**Ben Schroeter:** structured texts are cool  

**Wendy Reid:** homework is to contribute to the draft note  

---

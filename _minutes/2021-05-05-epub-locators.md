---
layout: minutes
date: 2021-05-05
title: EPUB 3 Working Group Virtual Locators Task Force Telco — 2021-05-05
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
        "url": "https://www.w3.org/publishing/groups/epub-wg/Meetings/Minutes/2021-05-05-epub-a11y",
        "name": "EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes",
        "about": "EPUB 3 Working Group Virtual Locators Task Force Telco",
        "dateCreated": "2021-05-05",
        "irc": "epub-locators",
        "datePublished": "2021-05-06",
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
            "startDate": "2021-05-05",
            "endDate": "2021-05-05",
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
                            "name": "Wendy Reid"
                        }
                    ]
                },
                {
                    "@type": "Person",
                    "name": "Dan Lazin"
                },
                {
                    "@type": "Person",
                    "name": "Pilar Wyman"
                },
                {
                    "@type": "Person",
                    "name": "Marisa DeMeglio"
                },
                {
                    "@type": "Person",
                    "name": "Garth Conboy"
                },
                {
                    "@type": "Person",
                    "name": "Ronnie Seagren"
                }
            ]
        }
    }

---

# EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes
{: .no_toc}



**Date:** 2021-05-05

See also the [Agenda]() and the [IRC Log](https://www.w3.org/2021/05/05-epub-locators-irc.txt)

## Attendees
{: .no_toc}
**Present:** Dan Lazin, Pilar Wyman, Wendy Reid, Marisa DeMeglio, Garth Conboy, Ronnie Seagren

**Regrets:** 

**Guests:** 

**Chair:** Wendy Reid

**Scribe(s):** Wendy Reid

## Content:
{: .no_toc}

* TOC
{:toc}
---


> *Wendy Reid:* [https://docs.google.com/spreadsheets/d/1KO-HyLGUUw36F-ruAARHNiPO1aUJCCNeTv3zxGtjuHw/edit#gid=0](https://docs.google.com/spreadsheets/d/1KO-HyLGUUw36F-ruAARHNiPO1aUJCCNeTv3zxGtjuHw/edit#gid=0)

**all:** reviewing the spreadsheet  
… discussing the challenges of lack of structure within EPUB files and implications for deep linking/ CFI  
… trying to figure out where in the process CFIs/locators need to be applied  
… Garth explains CFIs to all of us  

> *Marisa DeMeglio:* old CFI tests [https://github.com/IDPF/epub-testsuite/tree/d05594654b12fb784682212faf641cba59d2c77d/content/30/epub30-test-0140](https://github.com/IDPF/epub-testsuite/tree/d05594654b12fb784682212faf641cba59d2c77d/content/30/epub30-test-0140)

**all:** difference between a high level locator (like a page number), applied by the authoring tool, and specific locators (like CFIs) used by the reading system  

> *Marisa DeMeglio:* we test print page numbers in EPUB on epubtest.org, e.g. [http://epubtest.org/results/533/#nav-110](http://epubtest.org/results/533/#nav-110)

**all:** Going to continue refining the use cases, with document now in GH we can log issues and make revisions.  

---

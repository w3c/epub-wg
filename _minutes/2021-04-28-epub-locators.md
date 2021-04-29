---
layout: minutes
date: 2021-04-28
title: EPUB 3 Working Group Virtual Locators Task Force Telco — 2021-04-28
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
        "url": "https://www.w3.org/publishing/groups/epub-wg/Meetings/Minutes/2021-04-28-epub-a11y",
        "name": "EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes",
        "about": "EPUB 3 Working Group Virtual Locators Task Force Telco",
        "dateCreated": "2021-04-28",
        "irc": "epub-locators",
        "datePublished": "2021-04-29",
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
            "startDate": "2021-04-28",
            "endDate": "2021-04-28",
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
                    "name": "Marisa DeMeglio"
                },
                {
                    "@type": "Person",
                    "name": "Pilar Wyman"
                },
                {
                    "@type": "Person",
                    "name": "Mary Coe"
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



**Date:** 2021-04-28

See also the [Agenda]() and the [IRC Log](https://www.w3.org/2021/04/28-epub-locators-irc.txt)

## Attendees
{: .no_toc}
**Present:** Wendy Reid, Ben Schroeter, Marisa DeMeglio, Pilar Wyman, Mary Coe, Ronnie Seagren

**Regrets:** Dan Lazin

**Guests:** 

**Chair:** Wendy Reid

**Scribe(s):** Ben Schroeter

## Content:
{: .no_toc}

* TOC
{:toc}
---


> *Wendy Reid:* [https://docs.google.com/spreadsheets/d/1KO-HyLGUUw36F-ruAARHNiPO1aUJCCNeTv3zxGtjuHw/edit#gid=0](https://docs.google.com/spreadsheets/d/1KO-HyLGUUw36F-ruAARHNiPO1aUJCCNeTv3zxGtjuHw/edit#gid=0)


**Wendy Reid:** CFI implementation is often implemented by reading systems or other user agents in the ecosystem  
… how do we make CFIs more "friendly" is still an open question  
… reviewing collected use cases: things like deep linking may be more difficult than things like bookmarks, annotations, etc.  

**Ben Schroeter:** It's a good collection, but there's some overlap  

**Wendy Reid:** CFI currently lives in IDPF... discussing with chairs if we should promote to W3C, maybe as a note so we can start editing  
… then eventually it could be turned into a spec  

**Ronnie Seagren:** Is there anything we can do to make it easier to adopt for indexers and reading systems?  

**Wendy Reid:** yes that's what we are thinking about  

**Pilar Wyman:** In Adobe Acrobat I was updating page numbers (labels) globally - that's what we need for CFIs  

**Wendy Reid:** we've been calling them locators, but labels is interesting  

**Mary Coe:** we need a common language. locator link text? we need terms and definitions that we all can agree on and know what we are talking about  

**Wendy Reid:** CFIs might be massively overpowered for our use cases, which seem to hone in on a paragraph- or line-level locator  
… CFI can be much more precise  

**Pilar Wyman:** that kind of accuracy and precision is great for indexers though  

**Wendy Reid:** at what point does the locator need to be applied, and by whom?  
… we have use cases that indicate we want to point to a section or even a heading  
… and we have use cases where a user, not an author or an indexer, wants to determine a locator  

**Mary Coe:** we are a step ahead of the user - we can monitor their behavior  
… we should be nimble about how we do this because we don't know what the user experience will be ultimately  
… users are still thinking in terms of pages and drift around when you point them to something  

**Marisa DeMeglio:** if someone is using a screen reader, they would go to precisely where they are pointed  

**Pilar Wyman:** is there a way we can apply a highlight or other marker dynamically when the user arrives at the location?  

**Marisa DeMeglio:** the reading system might be able to do so in some cases  

**Wendy Reid:** the reading system takes control of these things - even media overlays can defer to reading system control  

**Marisa DeMeglio:** do we have examples of books with CFIs?  

**Wendy Reid:** Brady might have some Google examples  

**Ronnie Seagren:** what has to be true to implement?  

**Wendy Reid:** publishers have to want it, reading systems have to implement it. Like any tooling.  

**Marisa DeMeglio:** need to be able to translate CFIs into something that is understood by browsers. Maybe also look at selectors and states. Also see if others are considering this  

**Wendy Reid:** a lot of different people are coming at this from different places and through different lenses  
… CFI was designed with books (multi-page, multi-section documents) in mind, which is why we keep coming back to it  

**Marisa DeMeglio:** are we talking about pointing to an element from afar or putting some sort of anchor on an element  

**Ben Schroeter:** You don't put a marker in a book, but you derive it's location, the CFI is a protocol for deriving the location, and can use it to point to it from afar  
… CFI is attractive because it's a way to put a pin in a location with multiple pages/locations, that can be pointed to from multiple places  
… outside the book, from a LMS, from an index  
… but we want to put some human-readable front on it so it can be referenced  

**Ronnie Seagren:** we need to mask it with something human-readable  

**Marisa DeMeglio:** but then the onus is on the tools, which would have to perform that mapping  

**Wendy Reid:** aside from determining what technical improvements, how do we create something human-readable but also understandable for a reading system  
… that's the tricky part  

**Mary Coe:** is money and marketing the crux? does the burden fall with the publisher? it can't fall to the user. it needs to do what they want it to do.  

**Wendy Reid:** the question was considered, why isn't their wider implementation of CFI? the use cases weren't appealing enough, perhaps. If we tout the features we might have wider adoption of digital publications generally.  

**Pilar Wyman:** we tried that with the indexing spec, but it didn't catch on outside book fair settings  

**Marisa DeMeglio:** do we have an explainer?  
… for CFI?  
… it would be valuable to have a better understanding from the creators  

**Wendy Reid:** I propose that before next week we look at the new columns I added to the use case table  
… and determine who is responsible for the locator, who uses the locator, and how specific does the locator need to be  

**Ben Schroeter:** That will give us something to do and perhaps help propel us into the direction of making CFIs more "friendly"

**Ronnie Seagren:** does an ebook always have structure?  

**Wendy Reid:** there are always cases where there are chaotic publications  
… generally publishers try to apply structural semantics though  
… so let's flesh out those use cases and consider if we need more information as well.  
… my homework ill be to see if we can get the document moved from IDPF to Github  

**Ronnie Seagren:** sometimes we want to define a range with a starting and an ending. that would be a different category of locator  

**Wendy Reid:** yeah let's note that use case as well.  

---

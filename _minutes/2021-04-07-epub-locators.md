---
layout: minutes
date: 2021-04-07
title: EPUB 3 Working Group Virtual Locators Task Force Telco — 2021-04-07
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
        "url": "https://www.w3.org/publishing/groups/epub-wg/Meetings/Minutes/2021-04-07-epub-a11y",
        "name": "EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes",
        "about": "EPUB 3 Working Group Virtual Locators Task Force Telco",
        "dateCreated": "2021-04-07",
        "irc": "epub-locators",
        "datePublished": "2021-04-07",
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
            "startDate": "2021-04-07",
            "endDate": "2021-04-07",
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
                            "name": "Matt Garrish"
                        }
                    ]
                },
                {
                    "@type": "Person",
                    "name": "George Kerscher"
                },
                {
                    "@type": "Person",
                    "name": "Avneesh Singh"
                },
                {
                    "@type": "Person",
                    "name": "Ivan Herman"
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
                    "name": "Ben Schroeter"
                },
                {
                    "@type": "Person",
                    "name": "Dan Lazin"
                },
                {
                    "@type": "Person",
                    "name": "Mateus Teixeira"
                },
                {
                    "@type": "Person",
                    "name": "Juan Corona"
                },
                {
                    "@type": "Person",
                    "name": "Pilar Wyman"
                },
                {
                    "@type": "Person",
                    "name": "Ronnie Seagren"
                },
                {
                    "@type": "Person",
                    "name": "Sergey Lobachev"
                }
            ]
        }
    }

---

# EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes
{: .no_toc}



**Date:** 2021-04-07

See also the [Agenda]() and the [IRC Log](https://www.w3.org/2021/04/07-epub-locators-irc.txt)

## Attendees
{: .no_toc}
**Present:** Wendy Reid, George Kerscher, Avneesh Singh, Ivan Herman, Pilar Wyman, Tzviya Siegman, Ben Schroeter, Dan Lazin, Mateus Teixeira, Matt Garrish, Juan Corona

**Regrets:** 

**Guests:** Pilar Wyman, Ronnie Seagren, Sergey Lobachev

**Chair:** Wendy Reid

**Scribe(s):** Matt Garrish

## Content:
{: .no_toc}

* TOC
{:toc}
---


> *Wendy Reid:* [https://github.com/w3c/epub-specs/issues/1542](https://github.com/w3c/epub-specs/issues/1542)

**Dan Lazin:** we should start by laying out the problems we need to solve - we know people want to refer to page numbers from a book - easily link from an index to a place in an epub not necessarily a page  

**Ronnie Seagren:** do we need to be able cover ranges?  

**George Kerscher:** we already have in the spec when an equivalent print page document exists there is page list in the nav doc and the accessibility spec requires the page list be there - options on how to display this in the page  

> *Tzviya Siegman:* See [IDPF Indexing document](http://idpf.org/epub/idx/)

**Tzviya Siegman:** indexes are really important but we should avoid tying page breaks to them - need to figure out what is in scope - indexes specification lists requirements for indexes  

**Dan Lazin:** my impression is that the community group is where new features are supposed to come from and wg is for standardizing - we can't dictate features exist and hope they get coded  

**Ivan Herman:** it is almost true - we do have the possibility to add new features with testing, etc. but we can't realistically add anything too elaborate - question of time  
… the original question is that there are two types of locators - one is relatively fixed like the page list that an epub creator can create and there are others that are completely dynamic - annotations are an example where you want pointers to the location  

**Pilar Wyman:** every epub needs a solid internal structure - locators is the best way to call them - an index uses them but needs to be present  

**Avneesh Singh:** from a process point of view we don't need to get into the details of whether we are creating a new spec but look at the use cases first and then decide what can be done non-normatively - there may also be some things for which we need a new revision but put these for later  

> *Tzviya Siegman:* +1 avneeshsingh

> *Mateus Teixeira:* +1

**George Kerscher:** for background the indexing specification was developed under the idpf which didn't have strict implementation requirements which is why it is not well implemented - under w3c there are more rigorous implementation requirements  

**Ivan Herman:** the elephant in the room is what is the state of epubcfi - is it a tool we can rely on or put into recommendation track?  
… if it is widely implemented perhaps we should consider it again  

> *Juan Corona:* +1 mateus

**Mateus Teixeira:** my sense is that cfi is used silently for many different uses - we use it for deep linking for example and for extracting content within a container  
… a larger implementation of it is in VitalSource bookshelf and for redshelf reader  
… I don't know if anyone loves it but it is the only choice we have - there is potential for improvement  

> *Tzviya Siegman:* +1 to mateus - CFI is broadly used under the hood

**Wendy Reid:** commercial reading systems don't use cfi  

**George Kerscher:** if there was a locator roughly equivalent to a page and was in a publication would that allow us to use xpath to find an offset onto that page using tools that everyone has available to them?  

**Tzviya Siegman:** when we were working on 3.1 Garth Conboy did a survey of google's content and there were no books that included cfi so from an authoring perspective it is not used. It won't be easy to replace and xpath is probably not the best option for longevity  

> *Mateus Teixeira:* +1 tzviya re xpath not being ideal

**Ivan Herman:** xpath is being moved away from and has the problem that it can only point to structure not text - the other community we may want to turn to is Web Annotations - there are some documents coming out of that group that define a general way of addressing content - but may also be more aspirational than practical  
… web devs want dynamic hooks using text before or after but not aware of any tools that would make it practical  

> *Tzviya Siegman:* See [Web Annotation Model](https://www.w3.org/TR/annotation-model/)

> *Mateus Teixeira:* +100 web annotations

> *Juan Corona:* +1 web annotations

**Mateus Teixeira:** web annotation community would be great to involve and I would like to get dynamic locators to locations that change - as soon as you introduce a new section it's hard to ensure you can create persistent urls - hypothes.is has done a lot of work on this with wikipedia and content that changes  
… you need a selector that can point to the text  

> *George Kerscher:* Hypothes.is is planning a big push in Higher Ed.

**Dan Lazin:** one of the biases I bring to this is that ebooks are not as good as they ought to be because publishers don't have the control or time or expertise to ensure quality as they do with print - ebooks just get handed off inhouse or to conversion house - need accessibility for book creators who are not always very technical  
… there is a plugin for InDesign that can add page lists - not widely adopted and a book editor may not be aware of - we need foolproof solutions - for example be able to create a simple hash and use that  
… we'd need to deal with the problem of content and hashes changing but need to drive people in direction of tools being in control  

**Wendy Reid:** need a path forward for this work - what are the use cases so what do we need these locators to do - the indexes spec is a good place to get some from - dynamic content is an example of where we need to explore - I can create a place in github where we can start listing these  
… we need someone to lead the task force as well - keep track of what is going on and drive the work  
… please consider if you would like to and get back to me  

**Dan Lazin:** can we discuss an Australia-friendly time for this meeting?  

**Ivan Herman:** harder when we have people from US west coast and Asia/Australia  

**Dan Lazin:** maybe we could alternate meeting times?  

**Ivan Herman:** early afternoon time in Europe equates to early US time might work  
… maybe 8 or 9AM for US east coast might be 8 or 9PM for Australia  

> *George Kerscher:* it is 1:50 a.m. in Australia right now

**Wendy Reid:** I can send an email to see if we can find another time  

**Mateus Teixeira:** this time collides with the publishing community group  

**Wendy Reid:** try to populate the wiki for the next meeting  

**Ronnie Seagren:** do you want to identify the actor in the use case - is it something an author or indexer would do, etc.  

**Wendy Reid:** yes, typical pattern is that "actor is trying to do X"  

---

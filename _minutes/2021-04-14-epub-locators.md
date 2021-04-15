---
layout: minutes
date: 2021-04-14
title: EPUB 3 Working Group Virtual Locators Task Force Telco — 2021-04-14
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
        "url": "https://www.w3.org/publishing/groups/epub-wg/Meetings/Minutes/2021-04-14-epub-a11y",
        "name": "EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes",
        "about": "EPUB 3 Working Group Virtual Locators Task Force Telco",
        "dateCreated": "2021-04-14",
        "irc": "epub-locators",
        "datePublished": "2021-04-15",
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
            "startDate": "2021-04-14",
            "endDate": "2021-04-14",
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
                            "name": "Brady Duga"
                        }
                    ]
                },
                {
                    "@type": "Person",
                    "name": "Dan Lazin"
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
                    "name": "Ronnie Seagren"
                }
            ]
        }
    }

---

# EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes
{: .no_toc}



**Date:** 2021-04-14

See also the [Agenda]() and the [IRC Log](https://www.w3.org/2021/04/14-epub-locators-irc.txt)

## Attendees
{: .no_toc}
**Present:** Wendy Reid, Brady Duga, Dan Lazin, Marisa DeMeglio

**Regrets:** Tzviya Siegman, Matt Garrish, Ben Schroeter

**Guests:** Pilar Wyman, Ronnie Seagren, Mary

**Chair:** Wendy Reid

**Scribe(s):** Brady Duga

## Content:
{: .no_toc}

* TOC
{:toc}
---


> *Wendy Reid:* [https://docs.google.com/document/d/1y5JKcwlq1rvGYJ1HoLg0GF-NRiBsBNNZopGuQ0mgHUw/edit?ts=607779c8](https://docs.google.com/document/d/1y5JKcwlq1rvGYJ1HoLg0GF-NRiBsBNNZopGuQ0mgHUw/edit?ts=607779c8)

**Wendy Reid:** overview - looking for a solution within epub for locators  
… must work for content creators and RSes  
… may need to change the spec, or may just create a note  
… This is a hard problem, people have looked at it in the past  
… Need to understand the problem space (specific use cases for locators)  
… and what is the range of issues  
… scholarly, trade, etc  
… Asked for use cases, we got a lot back (in a Google doc)  

**Pilar Wyman:** Don't seem to be unique (lots of duplicates/overlaps)  

**Dan Lazin:** Useful to cluster as unique problems  
… probably no single answer that will hit everything  
… grouping problems that might have the same or similar solution may help narrow the scope  

**Wendy Reid:** Ok, let's group them  
… [listing each item]  

**Dan Lazin:** Page numbers important for the first item  
… but that may change over time when we replace page numbers  
… but today we need page numbers  

**Wendy Reid:** Case 2 - book clubs  

**Pilar Wyman:** Good use case, very common if everyone is using ebooks  

**Wendy Reid:** New group since this may not be page numbers  
… Use 3 - deep linking from external source  
… Falls under specific location  

> *Wendy Reid:* [https://docs.google.com/document/d/1y5JKcwlq1rvGYJ1HoLg0GF-NRiBsBNNZopGuQ0mgHUw/edit?ts=607779c8#](https://docs.google.com/document/d/1y5JKcwlq1rvGYJ1HoLg0GF-NRiBsBNNZopGuQ0mgHUw/edit?ts=607779c8#)

**Dan Lazin:** Needs to be open to that location as well as display it  
… Can you deep link now?  

**Brady Duga:** Yes, epubcfi, not used  

**Wendy Reid:** Case 4 - link to exact location, not artificial top of page  
… brings up what to do about footnotes  

**Pilar Wyman:** How do indexes work?  

**Wendy Reid:** Reading index note from the doc being reviewed  

**Mary:** Do we want to talk about embedded indexing in depth now?  

**Dan Lazin:** Maybe group first then come back to indexes  

**Ronnie Seagren:** Is this a point locator (unlike the other uses)?  

**Wendy Reid:** Putting in specific locations for now  
… Case 5 - refer to a range of pages  
… [reading note from the doc]  

**Mary:** People still like page numbers because they are used to them  
… but once they look at the page number, they don't care, or use the range  

**Ronnie Seagren:** A range help tell you how much information you will find (ie it tells you size)  

**Brady Duga:** Indicating size is something we haven't considered before  

**Dan Lazin:** There is an existing model, and we need to keep the information even if we change the model  

**Pilar Wyman:** New standard drops page numbers, uses identifiers  
… people seem to understand sections are large, subsections are small  

**Mary:** Need to understand what readers want  

**Ronnie Seagren:** And there are many different kinds of readers  

**Dan Lazin:** Users are used to ctrl-F (technical readers) so lots of nav not needed for technical web content  
… books are different  

**Wendy Reid:** Is this specific locations?  

**many:** yes  

**Wendy Reid:** Case 6 - RS wants to use real pages or screen pages  
… seems to fall under page numbers  

**Dan Lazin:** Is this the major implementation of page list  

**Wendy Reid:** Maybe  

**Marisa DeMeglio:** Thorium seems to do it  
… but it has been a few years  

**Ronnie Seagren:** This is also the case where a teacher tells students to go to a specific page  

**Wendy Reid:** Case 7 - Reading the same content across different volumes  
… Seems like specific locations  

**Dan Lazin:** True, but it is actually throwing things away.  
… That is it is doesn't matter what the book is, it is relative to the start of content in the particular volume (anthology vs single book, etc)  

**Wendy Reid:** Case 8 - Lawyer wants to reference some precise  
… specific locations  
… case 9 - auto generate locators  
… Depending on where it is done (at creation vs reading time) will make it less general  

**Dan Lazin:** If we put it in the spec how to generate it, then it can be consistent  
… but authors would lose control  

**Wendy Reid:** Page list is a problem for digital first/only  
… Since there is no print version, there may not be a pagelist  
… Is this specific location?  
… Making a new category for this one  
… Case 10 - cross language support  
… translations may move the location  
… it's specific location  

**Dan Lazin:** It is also ranges  

**Mary:** It is also less specific  

**Ronnie Seagren:** May not be the same location as the sentence in the translated version  

**Dan Lazin:** Seemed like arbitrary ranges, but paragraphs kind of solve this  
… There are two versions to the problem  

**Wendy Reid:** Putting it in specific  
… Case 11 - annotations  

**Dan Lazin:** Seems like specific locations  

**Ronnie Seagren:** Once did an index where there could only be a single locator for every entry  
… if there are multiple entries need a new sub entry  
… nice because it was one to one (works well with links)  

**Wendy Reid:** Continuously updated content, but locator that always takes you to the same place  
… as another use case  

**Dan Lazin:** pilarw2000__ mentioned poems, we should call that out explicitly  

**Pilar Wyman:** Similar to translations, using line numbers helps  

**Wendy Reid:** We have them all grouped  
… might be all we can do today  
… Looks like we have at least one large group, tackling that will hit most of the issues  
… May want to concentrate on that (specific locations)  
… might be a bad term  

**Mary:** Nope, I like it. But I guess we could have another name  

**Wendy Reid:** Where to do from here?  

**Pilar Wyman:** Also should look at the last one  
… since software drives how we do things, it would be good to guide the software  

**Wendy Reid:** No one handcodes their epubs  
… lean toward authoring side for doing this, to avoid fragmentation of implementations  

**Pilar Wyman:** When indexes are embedded you get an idea about the document and discussion  
… that gets carried through to the digital side, even if they no longer makes sense (eg page numbers)  

**Mary:** Agreed. People like to see things like page numbers in the index, but once they are in the document they don't care  

**Pilar Wyman:** So I want this use case to stay  
… this use case reflects how the software has changed how we think about this issue  

**Wendy Reid:** Need an implementable solution  

**Ronnie Seagren:** After we have a solution, I never want to see an epub without a linked index  
… whatever we can do to make that a default  

**Wendy Reid:** Not linked indexes are painful  

**Ronnie Seagren:** Still need to convince publishers to add links  

**Mary:** Is there an RS that has an index button (similar to ToC, etc)  

**Wendy Reid:** Index has never been elevated to same level as ToC in the epub metadata  

**Dan Lazin:** Homework - a lot of what we have in specific locations can be solved with CFI  
… Maybe we should go read CFI and figure out what would need to change to make it palatable  
… make sense or is it prejudging the solution  

**Marisa DeMeglio:** Real problem of use cases is "how do we stay webby" (ie solve this in the context of browsers)  

**Wendy Reid:** HW - review CFI, think about where the gaps are, how will this work in a browser  
… adjourned, meeting again next week at some other random time  

---

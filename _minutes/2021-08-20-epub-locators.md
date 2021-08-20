---
layout: minutes
date: 2021-08-20
title: EPUB 3 Working Group Virtual Locators Task Force Telco — 2021-08-20
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
        "url": "https://www.w3.org/publishing/groups/epub-wg/Meetings/Minutes/2021-08-20-epub-locators",
        "name": "EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes",
        "about": "EPUB 3 Working Group Virtual Locators Task Force Telco",
        "dateCreated": "08-20-2021",
        "irc": "epub-locators",
        "datePublished": "2021-08-20",
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
            "startDate": "2021-08-20",
            "endDate": "2021-08-20",
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
                        },
                        {
                            "@type": "Person",
                            "name": "Wendy Reid"
                        }
                    ]
                },
                {
                    "@type": "Person",
                    "name": "Ivan Herman"
                },
                {
                    "@type": "Person",
                    "name": "Avneesh Singh"
                },
                {
                    "@type": "Person",
                    "name": "Hadrien Gardeur"
                },
                {
                    "@type": "Person",
                    "name": "Will Awad"
                },
                {
                    "@type": "Person",
                    "name": "Dan Lazin"
                },
                {
                    "@type": "Person",
                    "name": "Tzviya Siegman"
                }
            ]
        }
    }

---

# EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes
{: .no_toc}



**Date:** 2021-08-20

See also the [Agenda]() and the [IRC Log](https://www.w3.org/2021/08/20-epub-locators-irc.txt)

## Attendees
{: .no_toc}
**Present:** Wendy Reid, Ivan Herman, Avneesh Singh, Brady Duga, Hadrien Gardeur, Will Awad, Dan Lazin, Tzviya Siegman

**Regrets:** 

**Guests:** 

**Chair:** Wendy Reid

**Scribe(s):** Brady Duga, Wendy Reid

## Content:
{: .no_toc}

* TOC
{:toc}
---


> *Wendy Reid:* [https://docs.google.com/document/d/11GypOjE9xOTaINATl5bxVIA3Mc9jzNBGCr6GT_KNaQ4/edit](https://docs.google.com/document/d/11GypOjE9xOTaINATl5bxVIA3Mc9jzNBGCr6GT_KNaQ4/edit)

**Wendy Reid:** Sorry for missing the last meeting  

**Dan Lazin:** Most people that are here today weren't at the last meeting  

### 1. document review
{: #section1}

**Wendy Reid:** Added a better definition of page list  

> *Dan Lazin:* Repost for those who missed the link: [https://docs.google.com/document/d/11GypOjE9xOTaINATl5bxVIA3Mc9jzNBGCr6GT_KNaQ4/edit#heading=h.gbsmtjlkuon](https://docs.google.com/document/d/11GypOjE9xOTaINATl5bxVIA3Mc9jzNBGCr6GT_KNaQ4/edit#heading=h.gbsmtjlkuon)

**Wendy Reid:** [Reviewing comment in the doc]  

**Hadrien Gardeur:** Is the page size calculated or authored?  
… if it is calculated than fine, we can use characters  
… but if it is authored then there can't be a fixed rule  
… calculated vs authored is an important distinction  

**Wendy Reid:** The guiding principle is authors should provide their own list, but in the absence of that we have a calculated alternative  

**Hadrien Gardeur:** If we follow the terminology then page list should only refer to the authored content  
… so this definition is confusing  

**Wendy Reid:** Agreed. Maybe just remove the fixed size reference here  

**Hadrien Gardeur:** I am concerned about using the same term ("page") for two different things  
… they are used in similar ways, but they aren't really the same, so using the same term is confusing  

**Dan Lazin:** So are you saying page is ok in the UI, but we should have different terms for authored page list page and the calculated page  

**Avneesh Singh:** Would be good to have different terms  

**Hadrien Gardeur:** We can look at existing implementations and see what terms have been used  
… In readium they are called positions  
… can have multiple positions on the page  
… used for a lot of things  

**Brady Duga:** We also have positions, and does the same thing. We don't use it when the page list is missing  
… one issue is a page list, but you can also have a list of positions  
… the way we handle a missing page list is to create a fake one  
… it's based on the RMSDK  
… we would create a not-great page list that would be consistent but not as good as an authored oen  

**Hadrien Gardeur:** Calculated positions are in memory and not persisted  
… But may persist for annotations  
… I imagine page and position are complementary and both exist for different purposes  
… One is a non-exhaustive string, the other is exhaustive (no gaps)  
… There will be different use cases  

**Wendy Reid:** Working on this terminology is important, given the discussion  
… Kobo uses position markers, but it is not at all related to page lists  
… Kobo is a locator, need a term for a calculated page  

**Ivan Herman:** Is the difference calculated or not?  
… Annotations, etc, are dynamic and to me that is a position  
… And the other is from the author and is set statically  

**Wendy Reid:** Summarizing. There is page and calculated page, but we want a better name  

**Tzviya Siegman:** What about calculated page?  

**Hadrien Gardeur:** Reviewing the doc at trying to decide if we are creating page lists or position lists  
… Some use case want page, but others work better with positions  
… So the answer to the question of what we really want to make isn't clear  
… it looks like we want both  
… For some, dealing with strings, it will be hard to implement a UI  

**Wendy Reid:** We don't consider UI much, we probably should consider it  

**Tzviya Siegman:** For some it won't matter if it is calculated or not, just so long as they are the same  
… The UI is an important point and is an issue we have had in the past with calculated pagination  
… Images are particularly a problem  

**Hadrien Gardeur:** For use case 1, if there is a string and kids need to enter it they will make mistakes  
… due to typos, etc  
… For the second case, it does matter if it is authored or calculated  
… since you need a reference that works across print and epub  

**Wendy Reid:** Authored and calculated will the terms and I will make an attempt at defining them  
… Maybe review the use cases as homework  
… And think about the desired end product  
… Any thoughts?  

**crickets:** chirp  

**Dan Lazin:** Should note that a calculated page won't exist if there is an authored page (mutually exclusive)  

**Wendy Reid:** Maybe expand the section on persistence  

**Dan Lazin:** I just added that  

**Tzviya Siegman:** Can we add images, math, etc into the process  

**Hadrien Gardeur:** If you are using bytes then mathml just works by magic  
… Depends on what you are counting  
… images less so  
… requires rendering first  

**Ivan Herman:** Going back to what Brady said, the calculated page list is "bad" and is meant as a stick to convince authors to include them  
… So maybe we shouldn't spend too much time worrying about the perfect algorithm  
… This is an absolute fallback  

**Hadrien Gardeur:** There is quite a bit of complexity to manage the algorithm  
… When making the list you will likely have different information available than when you are actually displaying the page  

**all:** general discussion of how hard it is to figure out the size of markup  

**Dan Lazin:** Added a section to the doc just now to cover this  

**Ivan Herman:** What we are talking about here is for the static page list  
… It is not for annotations, etc. Is that correct?  

**Hadrien Gardeur:** You could enhance an annotation with that information  
… the simplest thing you can do for annotations is the original text  
… Then you can add position information to annotation like how far in the doc it is  
… which is good for anchoring  

**Ivan Herman:** I think that backs my claim, there are distinct things here  
… the static and dynamic are both useful  

**Hadrien Gardeur:** The one thing all reading systems need is the position list  
… Why do you need to calculated a page list for any use case  
… Why does GPB calculate the page list?  

---

---
layout: minutes
date: 2021-05-12
title: EPUB 3 Working Group Virtual Locators Task Force Telco — 2021-05-12
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
        "url": "https://www.w3.org/publishing/groups/epub-wg/Meetings/Minutes/2021-05-12-epub-a11y",
        "name": "EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes",
        "about": "EPUB 3 Working Group Virtual Locators Task Force Telco",
        "dateCreated": "2021-05-12",
        "irc": "epub-locators",
        "datePublished": "2021-05-12",
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
            "startDate": "2021-05-12",
            "endDate": "2021-05-12",
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
                        }
                    ]
                },
                {
                    "@type": "Person",
                    "name": "Ben Schroeter"
                },
                {
                    "@type": "Person",
                    "name": "Brady Duga"
                },
                {
                    "@type": "Person",
                    "name": "Garth Conboy"
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
                    "name": "Charles LaPierre"
                }
            ]
        }
    }

---

# EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes
{: .no_toc}



**Date:** 2021-05-12

See also the [IRC Log](https://www.w3.org/2021/05/12-epub-locators-irc.txt)

## Attendees
{: .no_toc}
**Present:** Ben Schroeter, Brady Duga, Garth Conboy, Tzviya Siegman, Wendy Reid, Ivan Herman, Pilar Wyman, George Kerscher, Charles LaPierre

**Regrets:** 

**Guests:** 

**Chair:** Wendy Reid

**Scribe(s):** Pilar Wyman

## Content:
{: .no_toc}

* TOC
{:toc}
---


> *Wendy Reid:* [https://docs.google.com/spreadsheets/d/1KO-HyLGUUw36F-ruAARHNiPO1aUJCCNeTv3zxGtjuHw/edit#gid=0](https://docs.google.com/spreadsheets/d/1KO-HyLGUUw36F-ruAARHNiPO1aUJCCNeTv3zxGtjuHw/edit#gid=0)

**Wendy Reid:** summarized last session, incl use cases review and categorization, per locator creation and use  

**George Kerscher:** authoring tools?  

**Ivan Herman:** text editors are included in authoring tools  

**Wendy Reid:** index use cases  

**Pilar Wyman:** current practices on embedding incl page numbers just because they're available  

**Tzviya Siegman:** same with XML, per embedding  

**Brady Duga:** pre-epub vs epub locators  

**Ivan Herman:** some other tools may be called for  

**Brady Duga:** reading systems incl often authoring tools  

**Wendy Reid:** authoring tools, reading systems vs readers  

**Ben Schroeter:** indexers vs authoring tools  

**Ivan Herman:** who puts locators in epubs? that is the question.  
… ie, pre vs post purchase of the epub  

**Wendy Reid:** authoring tools include indexing tools  

**Charles LaPierre:** what about post-production indexes?  

**Ivan Herman:** that's annotation, a separate use case  

**Wendy Reid:** deep-linking cases, how do they apply?  

**Brady Duga:** deep-linking uses cfi, and book identifiers  
… user-interface issues are beyond what we are doing here  

**Ivan Herman:** it's ugly code, where is the spec for it?  

**Tzviya Siegman:** full code combination for such deep-linking isn't possible yet  

**Ivan Herman:** theoretically we do have it  

**Brady Duga:** disagree. we don't have the URL specifications yet  

**Ivan Herman:** the reading system is the culprit  

**Brady Duga:** yes, it's from the reading systems  

**Wendy Reid:** the how here is the challenge, beyond our scope  

**Ivan Herman:** unless we use CFI  

**Wendy Reid:** we are here to find new alternatives for page numbers  
… cross-reference/annotation use case  

**Ivan Herman:** this is reading system stuff, annotation servers do this, not our responsibility.  
… annotation anchors are separate, and may be our responsibility however  

**Charles LaPierre:** we should invite the Hypothesis people (Dan) who have solved this, regarding annotation anchors  

**Ivan Herman:** the Hypothesis system works nicely but uses a variation of locator references for their anchors, not anything we haven't already discussed.  

**Tzviya Siegman:** I will talk to Benjamin Young (of Wiley), who also worked on it  

**Wendy Reid:** more index cases  
… we return to making locators readable  

**Ivan Herman:** is there a tool that converts EPUB CFIs to something readable? that is what we need  

**Garth Conboy:** not sure EPUB CFI is less readable than other fragment IDs  

**Brady Duga:** this is about labels  

**Wendy Reid:** we need a locator with semantic value to replace printed page numbers. CFI does that, but it's really long  
… how can we convert CFI to something shorter?  

**Tzviya Siegman:** and accessible  
… readers like printed page numbers  

**Brady Duga:** ranges too. page numbers are just so good, and none of this other stuff does that.  

**Wendy Reid:** question to tzviya, what was it that readers didn't like about the non-page number locators?  

**Tzviya Siegman:** they found it confusing  

**Ivan Herman:** wouldn't it be nice if the reading system displayed page numbers per the viewing/reading system device  

**Brady Duga:** religious war over device pages and 'real' pages.  

**George Kerscher:** we are making this too complicated. easy solution is to define fake pages for publishers and we define our hats on those  

**Ivan Herman:** what would be the heuristics?  

**Wendy Reid:** Adobe Digital did that  

**George Kerscher:** it's an authoring thing, not a reading system  

**Tzviya Siegman:** Adobe Digital was based on bit size  

**George Kerscher:** Let's make a golden rule, of so many characters = 1 page  

**Wendy Reid:** internationalization would be complicated  

**Garth Conboy:** internationalization is solvable, though  

**Ivan Herman:** I can be convinced that's the way to go, but we do need non-normative agreement heuristic  

**Brady Duga:** what about page lists? can we just use those page numbers?  

**George Kerscher:** yes  

**Garth Conboy:** if no page list, build one  

**Wendy Reid:** no pages in digital-only  

**Garth Conboy:** make it up  

**George Kerscher:** non-normative, general guideline, let's make it up  

**Wendy Reid:** think about this, limits that define pages, etc.  

---

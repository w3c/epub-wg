---
layout: minutes
date: 2021-05-19
title: EPUB 3 Working Group Virtual Locators — 2021-05-19
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
        "url": "https://www.w3.org/publishing/groups/epub-wg/Meetings/Minutes/2021-05-19-epub-a11y",
        "name": "EPUB 3 Working Group Virtual Locators — Minutes",
        "about": "EPUB 3 Working Group Virtual Locators",
        "dateCreated": "2021-05-19",
        "irc": "epub-locators",
        "datePublished": "2021-05-20",
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
            "name": "EPUB 3 Working Group Virtual Locators",
            "startDate": "2021-05-19",
            "endDate": "2021-05-19",
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
                    "name": "Pilar Wyman"
                },
                {
                    "@type": "Person",
                    "name": "Ben Schroeter"
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

# EPUB 3 Working Group Virtual Locators — Minutes
{: .no_toc}



**Date:** 2021-05-19

See also the [Agenda]() and the [IRC Log](https://www.w3.org/2021/05/19-epub-locators-irc.txt)

## Attendees
{: .no_toc}
**Present:** Pilar Wyman, Brady Duga, Ben Schroeter, Ronnie Seagren, Mary Coe, Dan Lazin

**Regrets:** 

**Guests:** 

**Chair:** Wendy Reid

**Scribe(s):** Brady Duga, Wendy Reid

## Content:
{: .no_toc}

* TOC
{:toc}
---


> *Wendy Reid:* [https://docs.google.com/document/d/1y5JKcwlq1rvGYJ1HoLg0GF-NRiBsBNNZopGuQ0mgHUw/edit?usp=sharing](https://docs.google.com/document/d/1y5JKcwlq1rvGYJ1HoLg0GF-NRiBsBNNZopGuQ0mgHUw/edit?usp=sharing)

**Wendy Reid:** Summary of last week  
… George said let's just use page numbers  
… But there are questions around pagination in reading systems  
… May not be possible to have consistent numbers  
… So let's pick it back up now  

**Ben Schroeter:** Would it make sense to look at the use cases and see what would be handled by page numbers?  
… For instance, ones with a start and end requirement  

**Pilar Wyman:** Wants to put in a plug for page numbers  
… The issue isn't really consistent pagination, that happens already (different sized pages)  
… we understand that for a given volume the numbers are consistent internally  
… The real issue is direct to digital  
… The only place we need to say there must be some pagination is for those non printed books  
… May not be that big of an issue since we already aren't consistent  

**Ben Schroeter:** If the publication doesn't have page numbers, we want to avoid virtual page numbers from reading systems  
… since we want reading system agnostic page numbers  

**Pilar Wyman:** I meant authoring not reading system  

**Brady Duga:** I think George's comment was that we should have a virtual page numbering system that is easy to do without pages  
… google play's secret, we respect the page numbers when provided, or use bytes  
… page 75 is the same regardless of device  
… there's issues for citations on certain devices, encoding changes, might be imprecise  
… might need to be unicode code points instead  
… it's doable and easy for both device, authoring system  
… it feels like a hack  
… but maybe it's ok  

**Dan Lazin:** Was going to suggest what we already do  
… a few points: page numbers are already arbitrary  
… If you have a print book, use it, otherwise we will make something up  
… May be a problem when a digital first appears in print, or various formats  
… We don't have to have a single solution, can use pages, tick things off, then adopt other solutions when needed  
… Maybe we should recommend page lists when at all possible  
… Then suggest a fallback algorithm  
… which is entirely arbitrary  

**Ben Schroeter:** If we don't do it at authoring and rely on reading systems  
… we run the risk of non-identical page numbering  

**Dan Lazin:** Algorithms should be dead simple  
… aim for simplicity  

**Pilar Wyman:** Want to add page numbers are not the only solution  
… There could also be other numbering systems like section numbers  
… The types of content that this will be necessary is fiction  

**Dan Lazin:** Why is fiction different?  

**Pilar Wyman:** Fiction has fewer breakouts  
… Non-fiction has more sectioning  

**Ben Schroeter:** A lot of fiction has no section  

**Pilar Wyman:** Some of our use cases are fiction (or similar)  

**Brady Duga:** Few points, page lists and non-device oriented page numbering can be fraught due to device ideologies, some just prefer certain page numberings  
… differences across devices etc  
… there's entrenched opinions  
… we'll face a challenge convincing some people  
… we might be able to couch it in supplying references/indexes, better ui  

**Dan Lazin:** How does this role out? In the spec?  

**Wendy Reid:** This would probably an extension of the navigation document  
… If we have some fallback algorithm, then we would have to specify  
… And this recommendation would have to go through the whole group  
… and it would be at risk since we need two implementations  

**Dan Lazin:** Is there some other model?  

**Wendy Reid:** We could publish a separate document as a note  
… And see how people react  
… But we could try to get two implementations if we are confident  

**Ben Schroeter:** Matt, what are your thoughts around note vs spec  

**Matt Garrish:** Not really. Whichever you want to do is fine  
… might want to start as a note. Easier to go note to spec than vice versa  

**Ben Schroeter:** There was a perception that not having these citations was a barrier to adoption of epub  

**Ronnie Seagren:** Don't want this to go the way of the indexing standard  
… want this to get adopted  
… Do we have contacts  

**Brady Duga:** We have done notes that have become specs, not an absurd way to go  
… in terms of other reading systems, we have the other bigs, unsure of adoption  
… in terms of people, we have play, kobo, others  
… many of them are also w3c members  

**Wendy Reid:** We have a lot of reading systems vendors listening  

**Matt Garrish:** Some of this will depend on how strongly worded it is in the spec  
… Could be in the spec but not a must  

**Wendy Reid:** Best route is note, lay out the use cases and proposals  
… There is probably still a CFI role  
… Note first is also easier to distribute early  
… Note is way easier to read than the minutes  
… That means going back to the use cases  
… need to narrow down to the core cases  
… for instance, deep linking might not make the cut  
… Then figure out which ones would work with page numbers, and which need something else (eg CFI)  

**Ronnie Seagren:** What about getting some tools (eg InDesign) to adopt this?  

**Wendy Reid:** We can always ask  

> *Wendy Reid:* [https://docs.google.com/spreadsheets/d/1KO-HyLGUUw36F-ruAARHNiPO1aUJCCNeTv3zxGtjuHw/edit#gid=0](https://docs.google.com/spreadsheets/d/1KO-HyLGUUw36F-ruAARHNiPO1aUJCCNeTv3zxGtjuHw/edit#gid=0)

**Wendy Reid:** Added a new column to see if page numbers satisfy the requirement (in the linked spreadsheet)  

**Ben Schroeter:** Do we also want a primary/secondary column?  

**Wendy Reid:** Yes  
… [Reading first entry]  
… [continuing to read through, updating as we go]  

**Dan Lazin:** Can we get a catchy name for the different types of page numbers  
… to make it clear  

**Wendy Reid:** Mary, your research came up. How do people feel about generated page numbers?  

**Mary Coe:** I give them arbitrary page numbers in the index, and people seem to like them  
… they are very familiar  
… Pages, ranges, etc mean something, once they are in the text they no longer care  
… But once in the text they use other markers (eg section numbers)  

> *Ben Schroeter:* virtual folio (catchy name suggestion)

**Ronnie Seagren:** How about the word "page link" [?]  

**Mary Coe:** For now need more testing to see what people think  

**Dan Lazin:** Looking at a reader app  
… Looks like they have changed their page numbering recently  
… Only shows current page when there is a page list  

**Brady Duga:** What happens if you change the font size?  

**Dan Lazin:** Consistent if there is a page list, but not when there is no page list  
… Maybe chunks as a name? Or maybe "screens" vs "pages"? But people may not like that  

**Wendy Reid:** Maybe the name will come to us  
… [back to going through the spreadsheet]  

**Dan Lazin:** Are page level bookmarks good enough?  

**Wendy Reid:** Most reading systems are more granular  
… But maybe RS to RS is good enough?  

**Dan Lazin:** How about metric page numbers?  
… decimal page numbers solve all our cases  
… so subdivide pages into smaller sections  

**Ben Schroeter:** so 1.027 or something?  

**Mary Coe:** Metric might work for some cases (eg annotations or bookmarks)  
… But when giving them a new location requires orientation  
… Not always relevant  

**Dan Lazin:** Could suggest displaying other context when or perhaps recommend ignoring decimal portion when creating eg an index  

**Ben Schroeter:** Same issue with physical books and bookmarks  

**Ronnie Seagren:** A rough location can be better, since the reader needs to understand the context around the reference  

**Dan Lazin:** If I had an indexing system that links somewhere, I would want to go to the page and highlight the specific text  

**Pilar Wyman:** When we embed indexes I link exactly where the target is  
… sometimes you can't even see the top of the page  

**Wendy Reid:** Time is up! Homework - can we mark up the remaining use cases?  
… If you disagree just add a comment and we can discuss  
… My homework will be to set up a note (just a skeleton)  
… Do people prefer html or markdown?  

**Dan Lazin:** Why use html? Markdown is better  

**Wendy Reid:** Ok, will use markdown  

---

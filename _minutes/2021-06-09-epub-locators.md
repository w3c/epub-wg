---
layout: minutes
date: 2021-06-09
title: EPUB 3 Working Group Virtual Locators Task Force Telco — 2021-06-09
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
        "url": "https://www.w3.org/publishing/groups/epub-wg/Meetings/Minutes/2021-06-09-epub-locators",
        "name": "EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes",
        "about": "EPUB 3 Working Group Virtual Locators Task Force Telco",
        "dateCreated": "2021-06-09",
        "irc": "epub-locators",
        "datePublished": "2021-06-09",
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
            "startDate": "2021-06-09",
            "endDate": "2021-06-09",
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
                            "name": "Dave Cramer"
                        }
                    ]
                },
                {
                    "@type": "OrganizationRole",
                    "roleName": "scribe",
                    "attendee": [
                        {
                            "@type": "Person",
                            "name": "Dave Cramer"
                        }
                    ]
                },
                {
                    "@type": "Person",
                    "name": "Avneesh Singh"
                },
                {
                    "@type": "Person",
                    "name": "Pilar Wyman"
                },
                {
                    "@type": "Person",
                    "name": "Dan Lazin"
                },
                {
                    "@type": "Person",
                    "name": "Laurent Le Meur"
                },
                {
                    "@type": "Person",
                    "name": "Ivan Herman"
                }
            ]
        }
    }

---

# EPUB 3 Working Group Virtual Locators Task Force Telco — Minutes
{: .no_toc}



**Date:** 2021-06-09

See also the [Agenda]() and the [IRC Log](https://www.w3.org/2021/06/09-epub-locators-irc.txt)

## Attendees
{: .no_toc}
**Present:** Dave Cramer, Avneesh Singh, Pilar Wyman, Dan Lazin, Laurent Le Meur, Ivan Herman

**Regrets:** Tzviya Siegman

**Guests:** 

**Chair:** Dave Cramer

**Scribe(s):** Dave Cramer

## Content:
{: .no_toc}

* TOC
{:toc}
---


**Dan Lazin:** we're working on what might be reasonable to solve  
… we appear to be heading towards a defined fall-back for page numbers  
… a way to ensure pagelist is always present, even if not defined by the author  
… we do want to encourage a pagelist in all EPUBs  
… but have something to fall back to that is easy to implement  
… Laurent and Hadrien had good comments about page numbers via email  
… we don't think CFI is a bad idea, but we think it's a solution for a different set of problems  
… these problems are around traditional page numbers  

**Avneesh Singh:** CFI is also a problem for future for HTML EPUB  
… these are quite broad use cases  
… did you decide to put some of them out of scope?  

**Dan Lazin:** there's a spreadsheet for the use cases  
… the gdoc is out of date  

> *Dan Lazin:* [https://docs.google.com/spreadsheets/d/1KO-HyLGUUw36F-ruAARHNiPO1aUJCCNeTv3zxGtjuHw/edit#gid=0](https://docs.google.com/spreadsheets/d/1KO-HyLGUUw36F-ruAARHNiPO1aUJCCNeTv3zxGtjuHw/edit#gid=0)

**Dan Lazin:** in column 1 is whether things are in scope  
… those are the page number things  

**Pilar Wyman:** dan, were you there last week?  
… I missed it  
… I did not see in the minutes: Mary and I had been in an indexing conf  
… we asked about terms about what to call page numbers in ebooks that don't have page numbers  
… one suggestion was "pointer"  
… the thing a reader would click on to get to content  
… the thing in the index that might look like a section/page/para number that you click  
… "pointer" is a good word for that  
… we'd talked about translating a CFI into something readable; that would be a pointer  

**Dan Lazin:** don't forget that word :)  
… anything that we name has to be worldwide  
… users are familiar with pages  
… the concept is functionally a page  
… if we were to give it some other name, that might lead to irrelevancy  
… the email said, I'm in favor of calling these things pages  
… and encouraging reading systems to call their auto-numbering "screens"  
… pages don't change as you change font size, but the screens do move  

**Pilar Wyman:** would we call them screen numbers?  

**Dan Lazin:** we would do page numbers, RSs would do screen  

**Laurent Le Meur:** First, we cannot ignore the Kindle  
… which has locations  
… but it's not simple  
… in Readium we call it position  
… we didn't want to call it page  
… I would never speak about screens  
… screens is what you see, it's what's in the viewport  
… no two experiences are the same  
… to find something transportable, screens is not good  
… we could keep the name page but there is confusion with pagelist  
… we have to choose a name that is adequate  

**Dan Lazin:** to clarify, what we're trying to introduce is not dependant on viewport or screen size  
… the problem is that reading systems already have a variable thing, and they won't drop those  
… we do want to call the fixed thing pages  
… for one thing, if there's a pagelist we'll use that  
… and we want the same functionality  
… and we're recognizing there's an existing variable thing  
… I do believe screen is a bad name  
… because a11y  

**Laurent Le Meur:** RMSDK has been using position with a basic calculation  
… size of zipped resource in bytes, divided by 1024  
… because they are using zipped html resource  
… it has no real semantic meaning  
… but it is easy to calculate  
… we are wondering about using zipped vs unzipped HTML resource  
… if we want to keep with RMSDK and the reading toolkits  
… this is simple and adequate--zip divided by 1024  

**Dan Lazin:** brady said Google does something similar, unicode code points divided by 1000  
… once we have a recommendation, we should ask a RS to prototype a few things  

**Laurent Le Meur:** we have tried with uncompressed by 2500 but is about the same as compressed / 1024  
… you won't have interop until we agree  
… if we try we can take everything  

**Dan Lazin:** I think we agree it's arbitrary  
… and we're trying to set a standard  

**Ivan Herman:** Laurent, could your team and google team write down their algo.  
… so we could compare  
… I don't know the result of this task force  
… to have something documented as a first step is good  
… I don't know what other reading systems do  

**Laurent Le Meur:** apple recalculates every time the font size or viewport changes  

**Ivan Herman:** it depends on screen size, font size, etc  
… that's not what we're looking for  

**Laurent Le Meur:** exactly  

**Dan Lazin:** if you provide a pagelist, Apple will use your pagelist and the screen number; you used to be able to toggle  
… it will have both variable and fixed  

**Ivan Herman:** who else can we contact? Kobo?  

**Dave Cramer:** it may even depend on which Kobo implementation  

**Dan Lazin:** I can't get info from Google for a bit, as Brady and Garth are out  

**Laurent Le Meur:** yes, we can write down our heuristic algo  

**Ivan Herman:** perfect  
… what about bluefire?  

**Laurent Le Meur:** old bluefire is RMSDK, new bluefire is Readium  

**Ivan Herman:** can someone ask about Japanese reading systems on Thursday night?  

**Dan Lazin:** with dave and ivan here it's a good time to talk about strategy  
… what should we be producing  
… and how do we get adopted by reading systems?  
… let me lead the discussion  
… maybe it's an experimental thing where we need adoption  
… it's an attempt not a spec  

**Ivan Herman:** there is an intermediate thing  
… if I become administrative  
… a WG can publish WG notes  
… about any subject  
… sometimes it could be a design that is not final  
… in this case my option would be that we have a doc published as w3c note on locator issue in general  
… describing the problems and solutions  
… and talk about the role of EPUB CFI  
… and republish CFI with a note  
… and the same note would document this algo  
… this would not be a w3c recommendation  
… would raise more interest; more people would look at it than a CG doc  

**Pilar Wyman:** that's what Wendy has said  

**Dave Cramer:** this sounds like incubation, and we could sell this  

**Avneesh Singh:** is the ultimate objective the algo?  

**Pilar Wyman:** are we?  

**Dan Lazin:** I think so? It's a part of what we're providing. It's like an appendix.  
… we are striving for an agreement that all RSs should have a fallback  
… we need to decide about backward compatibility  
… should we address all the existing epubs in the world  
… I don't think we need to  
… I think it's acceptable to be an initiative for the future  
… it would be OK for us to handle backwards compat  

**Ivan Herman:** what do. you mean by backward compatibility  
… today, if author provides a page list, it's clear what the RS should do  
… if an EPUB does not have a pagelist, then the RS may do something but there is no incompatibility  

**Dan Lazin:** do we need to support all existing EPUBs?  

> *Dave Cramer:* .. is this in authoring, ingestion, or reading system?

**Ivan Herman:** no author will calculate the bytes in the xip  
… from my perspective, ingestion and RS is identical  

**Dan Lazin:** I think RS makes the most sense  
… you could do it in authoring  
… it could be every 1k character  
… and indesign could implement it  

**Avneesh Singh:** as far as algo is concerned  
… why do we worry about this?  
… if there is an algo, it could be used anywhere  

**Dan Lazin:** some are only practical in RS  

**Avneesh Singh:** there are complexities in vertical writing  
… how would that work?  

**Pilar Wyman:** indexing is done and embedding in doc. that's part of authoring  
… I'm not sure I'd agree it's RS-dependent  

**Dan Lazin:** if you have an index in a book, and the index header is "carrot"  
… 12, 38, 44  
… indexer needs to put links in  

**Pilar Wyman:** it's flipped around  
… I've embedded the index entry in the text  
… and then some process results in the pointer  
… the page number comes after  

**Ivan Herman:** this means that whatever algo we come up wiht  
… should be oblivious to whether it is done in RS or in authoring tool  
… so shouldn't be length of zip file  
… could be number of unicode characters  

**Dan Lazin:** there is another alternative  
… that's hard, though, for reasons avneesh explains  

**Ivan Herman:** I don't think avneeshsingh is right here  
… unicode is there; how they are displayed is a different question  

**Avneesh Singh:** it is different  
… may be a small number of chars between pages  

**Dan Lazin:** you need page numbers for xref or index  
… so we could say  
… the pagelist is primary, algo is fallback  
… you can only do indexing and xrefs with a pagelist  
… that lets algo be deferred to the RS  

**Pilar Wyman:** you're also talking about TOC, endnotes  

**Dan Lazin:** TOC doesn't need page numbers  
… more important for index  

**Ivan Herman:** I'm not sure I follow  
… the term authoring is too broad  

**Pilar Wyman:** I'm working with the book right before it's final  

**Ivan Herman:** the content is already there  

**Dan Lazin:** if Pilar finds a book without a pagelist, I'd expect her to request a new version with a pagelist or make one herself  
… there could be a fallback at authoring time  

**Ivan Herman:** that's the algo doable for both author and RS  

**Dan Lazin:** if Pilar is inserting page numbers, she can use arbitrary numbers  

**Ivan Herman:** if indexing is not there, and RS still does it  
… then you solve the use cases around shared location  
… if the algo covers several use cases that's important  

**Pilar Wyman:** I don't generate the page numbers  
… the publisher creates the page numbers for all the use cases  
… InDesign is great for that  

**Dan Lazin:** I still don't agree  
… there's no problem if we use the same algo but I don't think it's necessary  
… one case is a compiled ebook we don't touch, reading system generates positions  
… the other case is where the page numbers are written into the files  

**Ivan Herman:** is it better if it's the same algo  

**Dan Lazin:** the algo is an implementation of the goals. It is an appendix.  
… we derive the algo from our goals and requirements  
… we want it to be useable at both authoring time and RS time  
… and needs to work for all languages  
… but doesn't need to work identically  

**Avneesh Singh:** should be consistent within a language  

**Pilar Wyman:** as we go from spanish to english  

**Avneesh Singh:** if you have ten books in that language it should work consistently  

**Dan Lazin:** from strategy perspective  
… we need to remember is to reach out to adobe and other authoring systems  
… this will be vastly more useful  
… the best case is for every epub to have a pagelist  
… and for that we need ID and scrivener and Word  

**Ivan Herman:** yeah  
… I have a script that produces EPUBs of W3C docs  
… I start with HTML  
… for me to generate a pagelist doesn't work  
… I'd need a script  

**Dan Lazin:** that's not the primary case  

**Pilar Wyman:** when I'm indexing, instead of using page numbers I have distinct text for every hit under a concept  
… every instance has a unique chunk of text  

**Ivan Herman:** yes  

**Pilar Wyman:** we do need to tell people that's what you should do  

**Dan Lazin:** next time, we should start working on the note  
… we have things to write down  

**Ivan Herman:** is that all?  

**Dan Lazin:** the time for this is arbitrary, we're open to moving it  

**Ivan Herman:** the epub call is 4pm CET / 10AM ET  
… it's simpler for me if that slot is taken by EPUB  

**Dan Lazin:** we are proposing to move to Friday 10AM ET  

**Ivan Herman:** the first would be June 25  

**Dan Lazin:** we'll propose it  

**Pilar Wyman:** are we still doing wednesday nights?  

**Ivan Herman:** yes, but laurent and I can't participate  

**Dan Lazin:** we won't move those  

**Ivan Herman:** we'll try and see what others say  

**Avneesh Singh:** thanks for helping me catch up  

**Dan Lazin:** thanks for coming!  

---

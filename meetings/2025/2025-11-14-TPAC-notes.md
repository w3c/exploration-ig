# **Exploration IG Hybrid, TPAC 2025, 2025-11-14**

* Moderator: Heather Flanagan  
* Scribe: xueyuan  
* IRC channel: \#exploration-ig  
* Slack: \#explorationig

Call-in details: see [https://www.w3.org/groups/ig/exploration/calendar/](https://www.w3.org/groups/ig/exploration/calendar/)

Charter: see [https://www.w3.org/2025/04/exploration-ig-charter.html](https://www.w3.org/2025/04/exploration-ig-charter.html)

## **Agenda**

* Opening & round-table introduction  
* [Consider extending the web to include maps and location as 'native' content types](https://github.com/w3c/exploration-ig/issues/5) \- Peter Rushforth  
* [\[PROPOSAL\]Exploring a group of people having common interest about web content authenticity technology and its use cases \#11](https://github.com/w3c/exploration-ig/issues/11) \- Michiko Kuriyama   
* [IETF DISPATCH process](https://github.com/w3c/exploration-ig/blob/main/meetings/2025/W3C%20TPAC%202025.pdf) \- Heather Flanagan  
* Open discussion

Present: 

* Heather Flanagan (co-chair)  
* Philippe Le Hégaret (W3C)  
* Xueyuan Jia (staff contact)  
* Tomoya ASAI (WebDINO)  
* Kohei Watanabe (WebDINO)  
* Satoru Takagi (KDDI)  
* Wei Ding (Huawei)  
* Peter Rushforth (Natural Resources Canada)  
* Chris Wilson (Google)  
* Michiko Kuriyama (OP)  
* Jay Kishigami (WCAP)  
* Shigeya Suzuki (Keio University, Originator Profile CIP)  
* Kazuhiro Hoya （Originator Profile CIP)  
* 

## Meeting note

### Opening & round-table introduction

Heather: Welcome to the Exploration IG meeting. I’d first like to introduce this Interest Group.  
I’m the co-Chair of the Exploration Interest Group.

\[round-table introduction\]

Heather: we have three items today.

### [Consider extending the web to include maps and location as 'native' content types](https://github.com/w3c/exploration-ig/issues/5)

Slides: [https://peter.rushforth.info/TPAC-2025/MapML/Proposal.html](https://peter.rushforth.info/TPAC-2025/MapML/Proposal.html)

Peter: I'm Peter Rushforth, Maps for HTML CG co-chair. We have a small and dedicated group on the map. We have a proposal of the Map Markup Language (MapML). We are a W3C member, as well as the other presenter who will present a different proposal today.I want to bring this proposal to the consortium and the community. 

This is short video presentation from Satoru Takagi:

Satoru Takagi: we began from maps inside the map, now we imagine the web as a map. We shared the same aspiration as Peter the idea of making the maps as first-class citizen of the web. Our vision differs scales. MapML aims to bring the maps into the web. It enables the map data and map services to be handled in a standardized way within individual web pages or websites. In contrast, the Hyper-Layering Architecture (HLA) aims to map the web itself. we envision the entire web as a single map: one web map. Where all information and services can be connected through the common context of space. This vision as explained earlier arises from a very real and urgent social need today. 

we want to try to tell ourselves with HLA 1.0, also known as SVG map, defining everything inside SVG. it was powerful but it became a closed system, unable to evolve with the web. 

with HLA 2.0, we created layers as web apps, instead of forcing one universal format, each layer is now an independent web app, meaning it can use any data format or API internally. and still be easily combined and interoperable with others. the web should not decide anything, it should have accepted connecting everything. that's the foundation on which sustainable evolution can happen. the aspiration of making the maps first-class citizens of the web is something that Peter and I deeply share. However, there's a difference in the scale of our vision. HLA is not only about how to represent maps within HTML, it aims to understand and connect the entire web itself through the common context of maps. 

I'd like to invite everyone here to embrace the 'One Web Map' vision, where every resource can be linked and seen as one map. It's not about just a format or API, we are shaping the future of the web itself. both the MapML and HLA share similar same goal at the highly abstract level. we agree that the web needs a common Geospatial Canvas, a space for 2D geospatial content, whether that takes the form of the map, element or something new, is automatically a matter of HTML stakeholders of WAHTWG and the HTML WG. we need collaboration and gap analysis between the two models  
... recognizing the distinctions and discussing them openly.

Peter: I'd like to discuss the MapML proposal, the abstraction in common between MapML and HLA. The motivation behind this proposal is to enhance the accessibility and usability of maps on the web, creating simple maps is simple for HTML developers, making complex maps should be possible using standard tools, by making maps simple and accessible for developers, it encourages the better privacy through decentralization.  Centralized platforms dominate map publishing and track users.

The problem is: there are a number of maps, a 2022 research showed that 16% of web pages loaded a JS mapping library. For context, the \<video\> element was measured on 4.1% of page loads at the time. Developers are forced to rely on complex, and in some cases inaccessible JS libraries, due to lack of standard support for maps and location. It means location is a fundamental primitive form of information on the web, akin to text, images, video and audio. Accordingly, maps should be prioritized for implementation by the web platform.

Research from 2020 and 2022 shows that JavaScript maps often have poor and inconsistent accessibility, and a majority of developers lack the tools to create accessible maps. Privacy and surveillance: centralized platforms dominate map publishing and track users, standardizing HTML maps could enable private, decentralized alternatives. 

Map interfaces vary widely across sites, standardizing an accessible map widget would establish a consistent baseline web experience. 

The 2020 Maps workshop and the community co-chair led a research, and documentation of mapping use cases and requirements: [https://maps4html.org/HTML-Map-Element-UseCases-Requirements/](https://maps4html.org/HTML-Map-Element-UseCases-Requirements/)

Use cases categorized by user persona: website visitor, content/map author, application developer. Capabilities identified in those use cases are categorized as requirement, enhancement, impractical or undecided.

The requirements are part of our central hub for MapML in our developer documentation site. It has use cases and requirements section. The requirements section lists all the requirements that fulfill by the particular element.

There is a specification, the MapML Polyfill was the subject of the collaborative research and development by the OGC and W3C community before the 2020 workshop, including the editors of the Web Map and @1 specifications. We have implemented various use cases and requirements, and test them. 

The notion of geospatial canvas, called Tiled Coordinate Reference Systems, describes the content of format to change the state of the application. 

You can see two layers in The Viewer: layers represented in layer control, available to the map user that can be edited through the controls and related controls list attribute…

Heather: We probably better not dive into too much tech details. I want to know what you want to see happen next? 

Peter: we are seeking feedback and collaboration from the W3C community, and especially the browser projects on the our proposal. We invite participation in the Maps for HTML Community Group to help refine and advance the proposal towards standardization. If possible, the Maps for HTML community would prefer to integrate the MapML and HLA 2.0 proposals into a single coherent proposal for standardization and implementation. Please provide your feedback and insights to help us move forward with a unified community-backed proposal.

Heather: The MapML community group can take it, and you can reach out to the Team when you have a consensus within the group, then move forward to the next with WG, etc.

PLH: Did you get the TAG review on this proposal? I’d highly encourage you to get a TAG review first if you haven’t. 

Peter: Not yet. 

Heather: Other comments? Hearing none. 

### Exploring a group of people having common interest about web content authenticity technology and its use cases

Michiko: Originator Profile, a technology verifies the existence of content originators and content itself that has not been tampered with, would like to explore the opportunities of how to enhance the reliability of web content with potential collaboration with this technology.

\[video\] @@

shigeya: our use cases primarily focus on news media and digital advertisement. We are trying to provide some kind of validated information, source @@. 

.. verify the source of the information, to improve the situation in the media of false information. Regarding that context, we are seeking cooperation with C2PA. We are collaborating with other bodies on this matter. 

Heather: What do you look for?

shigeya: we like to start conversions in @@group. We also consider establishing a community group.

PLH: Yes, creating a CG and inviting interested people, getting C2PA’s support on that CG, and maintaining the conversation continuously would be a good approach. 

Heather: How to create the CG?  
Philippe: see [https://www.w3.org/community/about/faq/\#how-do-i-propose-a-group](https://www.w3.org/community/about/faq/#how-do-i-propose-a-group) 

### [IETF DISPATCH process](https://github.com/w3c/exploration-ig/blob/main/meetings/2025/W3C%20TPAC%202025.pdf) 

Heather: at the Exploration IG, we are looking for develop strategic narratives to help the W3C community understand these trends, the relevance of W3C activities, or a gap analysis where there are no current W3C activities; providing a forum for members of the W3C community. 

About IETF ART DISPATCH is chartered to bring on new work in the ART area and provide a conduit for new drafts, ideas and potential WGs. It’s well-understood in the IETF community, well-attended (e.g., 100-200 in the meeting room), their works well-documented on their wiki.

The ART DISPATCH focuses on directing the work to an existing WG, proposing new groups, recommending to hold BOF, publishing as AD-sponsored which you can get document published with editor’s support, recommending additional discussion or community development, finding the work inappropriate for IETF. 

Our Exploration starts to fill a similar role to them. W3C is not the IETF, the Exploration IG is not well-know in W3C and people might not know they can bring discussion to us. It’s unclear to people about how it differs from the WICG. 

Disposition options of the Exploration IG: direct the work to an existing WG; propose a new WG, a WICG project. Any other possibilities of options? 

PLH: For instance, you could also say the Exploration can direct people to workshop, task force, member submission, suggest people with proposals get W3C review, e.g., asking the HTML map proposal to go to TAG review. We can also rename ourselves into the DISPATCH group. 

Shigeya: I noticed that our meetings later during the week have less attendees compared to Monday, as people are leaving on Friday. 

Chris Wilson: when the AB talked about the Exploration IG, we expected the group to explore the new tech topics for W3C. We have this landscape for topics (AI, MapML, etc) and get people’s attention. 

Shigeya: I always spot new topics during TPAC, maybe we can leverage it. 

Jay: The process is important, I’d like to see flexibility for people to bring ideas for exploration, even though only small results could come out eventually. 

Wei Ding: The key difference between the WICG and the Exploration IG is that the WICG focuses on incubating specific, well-defined ideas, whereas the Exploration IG serves as a forum for early-stage, uncertain proposals. Open the Exploration IG more broadly, for example, set up a dedicated meeting at TPAC and open to all attendees. 

PLH: The W3C public mailing list \<[https://lists.w3.org/Archives/Public/public-new-work/](https://lists.w3.org/Archives/Public/public-new-work/)\> and the [TAG review list](https://github.com/w3ctag/design-reviews/issues) could be good places for the group to look into new ideas. In IETF, do people have to go through DISPATCH first when they have ideas?

Heather: No. 

Chris: In IETF, there are multiple levels of directing proposals to groups  @@

Heather: there are some people with proposals without knowing where to go (e.g., the credential issue that the group received) and we direct them to the right groups, the Crendential CG. 

Chris: The problem is how to get correct people to show up and work together at one point when we are in early discussion. The group probably needs W3C Working Group chairs to participate. And we couldn’t get them for a chairs breakfast at TPAC.

Carine: regarding the strategy about group chairs participation @@

Heather: the Exploration IG is currently chartered for 2 years, still an experiment. We might want to discuss about what the strategy needs to be like. 

Wei Ding: we should also further promote this IG, and possibly engage with the strategy team, or get a dispatch. 


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
* [\[PROPOSAL\]Exploring a group of people having common interest about web content authenticity technology and its use cases \#11](https://github.com/w3c/exploration-ig/issues/11) \- Michiko Kuriyama Kuriyama   
* [IETF DISPATCH process](https://github.com/w3c/exploration-ig/blob/main/meetings/2025/W3C%20TPAC%202025.pdf) \- Heather Flanagan  
* Open discussion

Present: 

* Heather Flanagan (co-chair)  
* Philippe Le Hégaret Le Hégaret Le Hégaret (W3C)  
* Xueyuan Jia (staff contact)  
* Tomoya ASAI (WebDINO)  
* Kohei Watanabe (WebDINO)  
* Satoru Takagi (KDDI)  
* Wei Ding (Huawei)  
* Peter Rushforth (Natural Resources Canada)  
* Chris Wilson Wilson (Google)  
* Michiko Kuriyama (Originator Profile CIP)  
* Jay Kishigami (WCAP)  
* Shigeya Suzuki (Keio University, Originator Profile CIP)  
* Kazuhiro Hoya （Originator Profile CIP)  
* 

## Meeting note

### Opening & round-table introduction

Heather Flanagan: Welcome to the Exploration IG meeting. I’d first like to introduce this Interest Group.  
I’m the co-Chair of the Exploration Interest Group.

\[round-table introduction\]

Heather Flanagan: we have three items today.

### [Consider extending the web to include maps and location as 'native' content types](https://github.com/w3c/exploration-ig/issues/5)

Slides: [https://peter.rushforth.info/TPAC-2025/MapML/Proposal.html](https://peter.rushforth.info/TPAC-2025/MapML/Proposal.html)

Peter Rushforth: I'm Peter Rushforth, Maps for HTML CG co-chair. We have a small and dedicated group on the map. We have a proposal of the Map Markup Language (MapML). We are a W3C member, as well as the other presenter who will present a different proposal today. I want to bring this proposal to the consortium and the community. 

This is short video presentation from Satoru Takagi: @@

Satoru Takagi: We began from maps inside the map, now we imagine the web as a map. Let's explore how the Web and Geo worlds can connect on a common ground from 'maps in the web' to 'the web as a map'. We shared the same aspiration as Peter the idea of making the maps as first-class citizen of the web. Our vision differs in scales. MapML aims to bring the maps into the web. It enables the map data and map services to be handled in a standardized way within individual web pages or websites. In contrast, the Hyper-Layering Architecture (HLA) aims to map the web itself. We envision the entire web as a single map: one web map, where all information and services can be connected through the common context of space. This vision arises from a very real and urgent social need today. 

HLA 1.0, also known as SVG map, defines everything inside SVG. It was powerful but it became a closed system, unable to evolve with the web. It often starts with one open format and soon multiplies, and the maintenance burden grows beyond sustainability. 

With HLA 2.0, we created layers as web apps, instead of forcing one universal format, each layer is now an independent web app, meaning it can use any data format or API internally, and still be easily combined and interoperable with others. The web should not decide anything, it should have accepted connecting everything. That's the foundation on which sustainable evolution can happen. The aspiration of making the maps first-class citizens of the web is something that Peter and I deeply share.

However, there's a difference in the scale of our vision. HLA is not only about how to represent maps within HTML, it aims to understand and connect the entire web itself through the common context of maps. 

I'd like to invite everyone here to embrace the 'One Web Map' vision, where every resource can be linked and seen as one map. It's not about just a format or API, we are shaping the future of the web itself. Both the MapML and HLA share similar same goal at the highly abstract level. We agree that the web needs a common Geospatial Canvas, a space for 2D geospatial content, whether that takes the form of the map, element or something new, is automatically a matter of HTML stakeholders of WAHTWG and the HTML WG. We need collaboration and gap analysis between the two models, recognizing the distinctions and discussing them openly.

Peter Rushforth: I'd like to discuss the MapML proposal, the abstraction in common between MapML and HLA. The motivation behind this proposal is to enhance the accessibility and usability of maps on the web. Creating simple maps is simple for HTML developers, making complex maps should be possible using standard tools. It encourages the better privacy through decentralization. 

The problem is: there are a number of maps, a 2022 research showed that 16% of web pages loaded a JS mapping library. For context, the \<video\> element was measured on 4.1% of page loads at the time. Developers are forced to rely on complex, and in some cases inaccessible JS libraries, due to lack of standard support for maps and location. It means location is a fundamental primitive form of information on the web, akin to text, images, video and audio. Accordingly, maps should be prioritized for implementation by the web platform.

Research from 2020 and 2022 shows that JavaScript maps often have poor and inconsistent accessibility, and a majority of developers lack the tools to create accessible maps. 

Privacy and surveillance: centralized platforms dominate map publishing and track users, standardizing HTML maps could enable private, decentralized alternatives. Map interfaces vary widely across sites, standardizing an accessible map widget would establish a consistent baseline web experience. 

The 2020 Maps workshop and the community co-chair led a research, and documentation of mapping use cases and requirements: [https://maps4html.org/HTML-Map-Element-UseCases-Requirements/](https://maps4html.org/HTML-Map-Element-UseCases-Requirements/). Use cases categorized by user persona: website visitor, content/map author, application developer. Capabilities identified in those use cases are categorized as requirement, enhancement, impractical or undecided. The requirements are part of our central hub for MapML in our developer documentation site: [https://maps4html.org/web-map-doc/](https://maps4html.org/web-map-doc/). Its requirements section lists all the requirements that fulfill by the particular element.

There is a specification, the MapML Polyfill was the subject of the collaborative research and development by the OGC and W3C community before the 2020 workshop, including the editors of the Web Map and @1 specifications. We have implemented various use cases and requirements, and test them. 

The notion of geospatial canvas, called Tiled Coordinate Reference Systems, describes the content of format to change the state of the application, coupling between the client and server through a format specification. You can see two layers in the Viewer, represented in layer control, available to the map user that can be edited through the controls and related controls list attribute...

Heather Flanagan: We probably shouldn't get into too many technical details. My question is, what do you want to see happen next?

Peter Rushforth: we are seeking feedback and collaboration from the W3C community, and especially the browser projects on the our proposal. We invite participation in the Maps for HTML Community Group to help refine and advance the proposal towards standardization. If possible, the Maps for HTML community would prefer to integrate the MapML and HLA 2.0 proposals into a single coherent proposal for standardization and implementation. Please provide your feedback and insights to help us move forward with a unified community-backed proposal.

Heather Flanagan: The Maps for HTML Community Group can take this on. Once you have reached a consensus within the group, you can reach out to the W3C Team, and then move forward with a Working Group (WG), etc.

Philippe Le Hégaret: Did you get the TAG review on this proposal? I’d highly encourage you to get a TAG review first if you haven’t. 

Peter Rushforth: Not yet. 

Heather Flanagan: Other comments? Hearing none. 

### Exploring a group of people having common interest about web content authenticity technology and its use cases

Michiko Kuriyama: Originator Profile (OP), a technology verifies the existence of content originators and content itself that has not been tampered with, would like to explore the opportunities of how to enhance the reliability of web content with potential collaboration with this technology.

For users, not only will it be easier to verify the originator/publisher of content, but it will also be easier to identify dis/misinformation, as they can be sure that the information has not been tampered with.

\[video\] @@

Shigeya Suzuki: The OP technology is likely to be used for news from media organizations, advertisements by companies, and information from government agencies, etc. It provides users with two key verifications: The content's source is authentic and unaltered; The originator/publisher has systems to ensure reliability and responsibility in distributing information. OP certifies that the content was published by a responsible company or other entity.

OP has already been gaining adoption to the media ecosystem. However, we believe that it will be effective for gaining more to work with content provenance verification technology like C2PA. We hope to look for the opportunity of potential collaborations with that kind of technology.

Heather Flanagan: What do you look for?

Shigeya Suzuki: we like to start conversions with other W3C Groups. We also consider establishing a Community Group (CG).

Philippe Le Hégaret: Yes, creating a Community Group (CG) to engage interested parties, gaining C2PA's support, and sustaining the conversation is a solid approach.

Heather Flanagan: How to create the CG?  
Philippe Le Hégaret: see [https://www.w3.org/community/about/faq/\#how-do-i-propose-a-group](https://www.w3.org/community/about/faq/#how-do-i-propose-a-group) 

### [IETF DISPATCH process](https://github.com/w3c/exploration-ig/blob/main/meetings/2025/W3C%20TPAC%202025.pdf) 

Slides: [https://github.com/w3c/exploration-ig/blob/main/meetings/2025/W3C%20TPAC%202025.pdf](https://github.com/w3c/exploration-ig/blob/main/meetings/2025/W3C%20TPAC%202025.pdf)

Heather Flanagan: At the Exploration IG, we monitor industry and technology trend and analyze their potential impact on the web. Based on these findings, we develop strategic narratives to help the W3C community understand these trends, the relevance of W3C activities, or a gap analysis where there are no current W3C activities. The IG provides a forum for members of the W3C community to share updates as part of broader strategic discussions, and to seek in-depth strategic input. 

About IETF ART DISPATCH: The DISPATCH WG is chartered to bring on new work in the ART area and provide a conduit for new drafts, ideas and potential WGs. It's like a matchmaker between keen engineers and IETF processes/groups/procedures. It’s well-understood in the IETF community, well-attended (e.g., 100-200 in the meeting room). and their work is well-documented on their wiki.

The ART DISPATCH focuses on directing the work to an existing WG, proposing new groups, recommending to hold a BOF, publishing as AD-sponsored which you can get document published with editor’s support, recommending additional discussion or community development, finding the work inappropriate for IETF. 

Our Exploration starts to fill a similar role to them. However, W3C is not the IETF and the possible solutions are not the same. The Exploration IG is not well-know in W3C and people might not know they can bring discussions to us. It’s unclear to people about how it differs from the WICG. 

The disposition options for the Exploration IG include: directing the work to an existing WG, proposing a new WG/CG or a WICG project. Are there any other potential options to consider?

Philippe Le Hégaret: For instance, the Exploration IG could also direct proposals to a workshop, task force, or member submission. It could also suggest that proposal owners seek W3C review; for example, by asking the HTML Map proposal to undergo a TAG review. Additionally, we can also rename ourselves into the DISPATCH group. 

Shigeya Suzuki: I observed that meeting attendance tends to be lower later in the week compared to Monday. Proactive measures might be needed to increase the group's visibility and participation.

Chris Wilson Wilson: The AB expects the Exploration IG to explore new technological topics for W3C, providing a landscape overview for various areas like AI and MapML and attracting community attention.

Shigeya Suzuki: I consistently identify new topics during TPAC. Perhaps we can leverage this opportunity more systematically to inform the group's exploration work.

Jay: I think the process matters. I'd like to see flexibility for people to bring in ideas for exploration, even if only small results eventually come out of them.

Wei Ding: The key difference between the WICG and the Exploration IG is that the WICG focuses on incubating specific, well-defined ideas, whereas the Exploration IG serves as a forum for early-stage and uncertain proposals. To broaden its reach, the Exploration IG could be opened more widely—for example, by organizing a dedicated meeting at TPAC that is open to all attendees.

Philippe Le Hégaret: The W3C public mailing list \<[https://lists.w3.org/Archives/Public/public-new-work/](https://lists.w3.org/Archives/Public/public-new-work/)\> and the [TAG review list](https://github.com/w3ctag/design-reviews/issues) could be good places for the group to look into new ideas. In IETF, do people have to go through DISPATCH first when they have ideas?

Heather Flanagan: No. 

Chris Wilson: In IETF, there are multiple levels of directing proposals to groups @@

Heather Flanagan: There were cases where individuals had proposals but didn't know where to submit them—for example, the credential issue that this group received. In such situations, we directed them to the appropriate group, which was the Credentials CG.

Chris Wilson: The core challenge is engaging the right participants to collaborate during early-stage discussions. The group would benefit from the participation of W3C Working Group chairs. And we couldn’t get them for a chairs breakfast at TPAC.

Carine: regarding the strategy about group chairs participation @@

Heather Flanagan: The Exploration IG is currently chartered for 2 years, so it's still an experiment. We might want to discuss about what the strategy needs to be like. 

Wei Ding: we should also further promote this IG, and possibly engage with the Strategy team, or get a DISPATCH. 


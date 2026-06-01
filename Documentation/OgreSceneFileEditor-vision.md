<!-- 
Style headers to match original word template.
-->
<style scoped>
h1 {
  text-align: right !important;
  border-bottom: 0;
}
h2 {
  border-bottom: 0;
  text-align: right !important;
}

</style>

# Ogre Scene File Editor #
## Vision ##
## Version ```0.12``` ##

> [!NOTE]
> The purpose of this document is to collect, analyze, and define high-level needs and features of the system/program. It focuses on the capabilities needed by the stakeholders and the target users, and why these needs exist. The details of how the system/program fulfils these needs are detailed in the use-case and supplementary specifications.

### 1.1 Introduction ###
> [!NOTE] 
> The introduction of the Vision document provides an overview of the entire document. It includes the purpose, scope, definitions, acronyms, abbreviations, references, and overview of this Vision document.

This documentation details the ****Ogre Scene File Editor**** from conception to testing and delivery. The document contains references to the **fictional** company Gerkin Hammer Games who have commissioned this software as part of their tools pipeline. 

This document provides the **Vision** for the **Ogre Scene File Editor**, this focuses on the high level requirements, environment and stakeholders of the proposed software. It documents the needs of the stakeholders and why they exist, how these needs will be fulfilled by the **Ogre Scene File Editor** will follow in later sections. 

#### Scope ####
> [!NOTE] 
> A brief description of the scope of this Vision document; what Project(s) it is associated with and anything else that is affected or influenced by this document.

The scope of this document is limited to the **Ogre Scene File Editor**, as the file format is well established (and not part of this project) it is documented elsewhere (Ogre3D, no date). This file format is used by the well established Ogre3D Graphics Engine (current release 14.3) rather than the new Ogre-Next engine (current release 3.0) which is still maturing.

The Ogre3D Graphics Engine which uses this file is also outside the scope of this document, please refer to the [Ogre Documentation](https://www.ogre3d.org/) if further information is required.

#### Definitions, Acronyms, and Abbreviations ####
> [!NOTE] 
> This subsection provides the definitions of all terms, acronyms, and abbreviations required to properly interpret the Vision document. This information may be provided by reference to the project’s Glossary.

| Term | Definition |
| :-- | :-- |
|```.scene``` Files| ```.xml``` files used to store scene information for the Ogre Graphics Engine. |
|GerkinEngine|Current Engine technology at Gerkin Hammer Games, the second generation engine makes use of ```.scene``` files. |


<!--TODO
Glenn: Come back to this at the end.
-->

#### References ####
> [!NOTE] 
> This subsection provides a complete list of all documents referenced elsewhere in the Vision document. Identify each document by title, report number if applicable, date, and publishing organization. Specify the sources from which the references can be obtained. This information may be provided by reference to an appendix or to another document.

Goldberg, M. et al. (no date) Open source 3D graphics engine, OGRE. Available at: https://www.ogre3d.org/ (Accessed: 08 July 2025). 

#### Overview ####
> [!NOTE] This subsection describes what the rest of the Vision document contains and explains how the document is organized.

The remaining sections of the vision document focus on the high level problem the software is designed to solve along with some limited market positioning of the software. 


### 2.0 Positioning ###

### 2.1 Problem Statement ###
> [!NOTE] Provide a statement summarizing the problem being solved by this project. The following format may be used:

|     |     |
| --- | --- |
|The problem of	| viewing, verifying and editing Ogre3D's ```.scene``` files |
|affects | *the stakeholders affected by the problem*|
|the impact of which is	| time lost manually viewing and errors introduced while manual editing scene files |
|a successful solution would be	| a program which allowed a selected scene file to be viewed, edited and verified to ensure they are correctly formatted. |

</div>

### 2.2 Product Position Statement ###
> [!NOTE] 
> Provide an overall statement summarizing, at the highest level, the unique position the product intends to fill in the marketplace. The following format may be used:


|     |     |
| --- | --- |
|For| staff at Gerkin Hammer Games|
|Who| require a tool to view, validate and safely edit Ogre Config Files|
|The **Ogre Scene File Editor** is a | file viewer, validator and editor |
|That| provides a bespoke, cross platform, GUI driven tool, that provides viewing, validation and editing features |
|Unlike| notepad and other text editors |
|Our product| allows only valid edits to be made to the file.|



> [!NOTE] 
> A product position statement communicates the intent of the application and the importance of the project to all concerned personnel.

### 3. Stakeholder Descriptions ###

#### 3.1 Stakeholder Summary ####

<!--
|Name|Description|Responsibilities|
|---|---|---|
*Name the stakeholder type.*|*Briefly describe the stakeholder.*|*Summarize the stakeholder’s key responsibilities with regard to the system being developed; that is, their interest as a stakeholder. For example, this stakeholder: <br> ensures that the system will be maintainable <br> ensures that there will be a market demand for the product’s features <br>monitors the project’s progress <br>approves funding <br> and so forth*| 
-->

|Name|Description|Responsibilities|
|---|---|---|
|Game Designer| Use the GerkinEngine (which uses Ogre Scene Files). | Provides requirements in terms of file editing, display and validation.|
|Game Engine Developer| Works with Ogre3D as part of the GerkinEngine | Provides details on the content of the Ogre3D scene file.|
|Lead Designer|Responsible for a team designing a game using the GerkinEngine. |Instigated the project to reduce time spend resolving issues with the Ogre Scene files.|
|Game Tool Developer|Responsible for the delivery of the tool and its maintenance.|Ensure the tool created meets the requirements, also to ensure that it can be maintained by the development team.|



#### 3.2 User Environment ####
> [!NOTE]
> Detail the working environment of the target user. Here are some suggestions:
> Number of people involved in completing the task? Is this changing?
> 
> How long is a task cycle? Amount of time spent in each activity? Is this changing?
> 
> Any unique environmental constraints: mobile, outdoors, in-flight, and so on?
> 
> Which system platforms are in use today? Future platforms?
> 
> What other applications are in use? Does your application need to integrate with them?
> 
> This is where extracts from the Business Model could be included to outline the task and roles involved, and so on.

Gerkin Hammer Games is a small, independent (and **fictional**) games company, established in 2010 by a group of undergraduate students. Originally based in Cardiff increasing costs and homeworking saw the company move to more remote offices in Gwynfyd Monmouthshire.  The company has an established game engine (GerkinEngine) and a selection of tools, mostly bespoke. 

Operationally there are three teams, the Engine Team includes a small group with responsibility for tool development and maintenance (but no full time tool development team). The Design Team includes both those working on the design and it's implementation in the engine. Finally the loosely labelled Art Team, which includes texture artists, animators and an audio designer (who feels out of place). There is no specialised testing team, testers are occasionally employed buy much of the testing is done in house. 

The software will be used on a stand alone PC, belonging to either a designer/developer or tester to recover or repair their ogre.cfg file.  The application would be used for a few minutes at a time to make and test changes to the ```.scene``` file during development/testing.   

### 4. Product Overview  ###
#### 4.1 Product Perspective ####
> [!NOTE]
> This subsection of the Vision document puts the product in perspective to other related products and the user’s environment. If the product is independent and totally self-contained, state it here. If the product is a component of a larger system, then this subsection needs to relate how these systems interact and needs to identify the relevant interfaces between the systems. One easy way to display the major components of the larger system, interconnections, and external interfaces is with a block diagram.

The software will be independent of other existing tools, while there has been some suggestion that a single large 'all-in-one' tool may improve workflow there has been resistance from those charged with tool maintenance. As a result a minimalist approach is being taken, with just enough tools with just the required features.   

#### 4.2 Assumptions and Dependencies ####
> [!NOTE]
 List each factor that affects the features stated in the Vision document. List assumptions that, if changed, will alter the Vision document. For example, an assumption may state that a specific operating system will be available for the hardware designated for the software product. If the operating system is not available, the Vision document will need to change.

It is assumed that the software will compile for Windows 11, Linux (6.x) and macOS (13.0) and later. Expected dependencies include a suitable XML library and GUI library/framework both must be cross platform as indicated above. 


#### 4.3 Needs and Features ####
> [!NOTE]
 Avoid design. Keep feature descriptions at a general level. Focus on capabilities needed and why (not how)	 they should be implemented.


|Need|Priority|Features|Planned Release|
|---|:-:|---|---|
| Read and display ```.scene``` files | 1. | 1. Prompt user for a file <br> 2. Parse file <br> 3. Display as table/tree for checking <br> | 1.0 |
| Validate a scene file | 1. | Read Scene Files | 1.0 |
| Load Scene file | 1.  | 1. Loading selected scene files <br> 2. Read the scene files <br> 3. Parse the data <br> 4. Loading and displaying the scene | 1.0 |
| Validate the scene data | 1. | 1. Able to check and validate the requried elements and object properties <br> 2. Check the compatibility | 1.0 | 
| Displaying scene data | 1. | 1. Displaying the scene data on screen <br> 2. Displaying the visualisation of the scene | 1.0 |
| Writting the scene file | 1. | 1. Writes any changes you have made to the file <br> | 1.0 |
| Fullscreening the appplication | 2. | 1. Allows you to fullscreen the application | 1.0 |
| Reporting errors | 1. | 1. Able to report parts of the file thts invalid <br> 2. Display the error message <br> 3. Log the error | 1.0 |

<!--TODO add to this, what else needs changing in the file.  -->

#### 4.4 Alternatives and Competition ####
> [!NOTE]
 Identify alternatives the stakeholder perceives as available. These can include buying a competitor’s product, building a homegrown solution, or simply maintaining the status quo. List any known competitive choices that exist or may become available. Include the major strengths and weaknesses of each competitor as perceived by the stakeholder or end user.

  The Ogre3D engine does have and associated GUI which can write a new ```.scene``` file, updates are sporadic (last updated to Ogre 14.4) while this is an option this would tie the toolchain to that of the [Ogitor](https://github.com/OGRECave/ogitor) render engine. 

#### 5. Other Product Requirements ####
> [!NOTE]
> At a high level, list applicable standards, hardware, or platform requirements; performance requirements; and environmental requirements.
> 
> Define the quality ranges for performance, robustness, fault tolerance, usability, and similar characteristics that are not captured in the Feature Set
> 
> Note any design constraints, external constraints, or other dependencies.
> 
> Define any specific documentation requirements, including user manuals, online help, installation, labeling, and packaging requirements.
> 
> Define the priority of these other product requirements. Include, if useful, attributes such as stability, benefit, effort, and risk.



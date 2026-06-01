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

# System/Programme Name #
## Supplementary Specification ##

## Version ```0.12``` ##

>[!NOTE] 
> The Supplementary Specification captures the system requirements that are not readily captured in the use cases of the use-case model. Such requirements include: 
> * Legal and regulatory requirements, including application standards. 
> * Quality attributes of the system to be built, including usability, reliability, performance, and supportability requirements. 
> * Other requirements such as operating systems and environments, compatibility requirements, and design constraints.

### Definitions, Acronyms, and Abbreviations ###

> [!NOTE] 
> This subsection provides the definitions of all terms, acronyms, and abbreviations required to properly interpret the Supplementary Specification. This information may be provided by reference to the project’s Glossary.

 Please refer to the [Glossary](OgreConfigReader-glossary.md).

### References ###

TinyXML, https://www.cs.cmu.edu/~preethi/src/tinyxml/docs/ , Lee Thomason, Yves Berquin , published Jan 25 2006 , accssed 25/02/2026

XML API's, R. Chandrasekaran, F. Asgareinjad, J. Morris and T. Rosing, "Multi-Label Classification With Hyperdimensional Representations," in IEEE Access, vol. 11,

> [!NOTE] 
> This subsection provides a complete list of all documents referenced elsewhere in the Supplementary Specification. Identify each document by title, report number if applicable, date, and publishing organization. Specify the sources from which the references can be obtained. This information may be provided by reference to an appendix or to another document.
> 

### Functionality ###

> [!NOTE] 
> This section describes the functional requirements of the system for those requirements which cannot be expressed as Use Case are expressed in the natural language style. For many applications, this may constitute the bulk of the SRS Package and thought should be given to the organization of this section. This section is typically organized by feature, but alternative organization methods, for example organization by user or organization by subsystem, may also be appropriate. Functional requirements may include feature sets, capabilities, and security.
Where application development tools, such as requirements tools, modelling tools, and so on, are employed to capture the functionality, this section document will refer to the availability of that data, indicating the location and name of the tool used to capture the data.

**Functional Requirement One**

> [!NOTE] 
> The requirement description.

### Usability ###
> [!NOTE] 
> This section should include all of those requirements that affect usability. 
> Examples follow:
> * specify the required training time for a normal users and power users to become productive at particular operations
> * specify measurable task times for typical tasks, or
> * specify requirements to conform to common usability standards, for example, IBM’s CUA standards or Microsoft’s GUI standards


**Usability Requirement One**

Menu options will be limited to those available at the time.

| State | Available Options |
| :-- | --- |
| No file Loaded | Load, Exit |
| File Loaded | Display, Edit, Validate, Exit |
| Loaded content modified | Display, Edit, Validate, Write, Exit |
| File loaded and written | Display, Edit, Validate, Exit |

**Usability Requirement Two**

> [!NOTE] 
> The requirement description.

### Reliability ###
> [!NOTE] 
> Requirements for reliability of the system should be specified here. Suggestions are as follows:
> * Availability – specify percentage of time available ( xx.xx%), hours of use, maintenance access, degraded mode operations, and the like.
> * Mean Time Between Failures (MTBF) – this is usually specified in hours but it could also be specified in terms of days, months or years.
> * Mean Time To Repair (MTTR) – how long is the system allowed to be out of operation after it has failed?
> * Accuracy – specify precision (resolution) and accuracy (by some known standard) that is required in the systems output.
> * Maximum bugs or defect rate – usually expressed in terms of bugs/KLOC (thousands of lines of code), or bugs/function-point.
> * Bugs or defect rate – categorized in terms of minor, significant, and critical bugs: the requirement(s) must define what is meant by a “critical” bug; for example, complete loss of data or complete inability to use certain parts of the functionality of the system.

**Reliability Requirement One**

As the application has no online element, connectivity or safety critical aspects there are few reliability requirements.  Due to the nature of the application minor bugs or limitations are acceptable provided the core functionality of the system is present.

**Reliability Requirement Two**

> [!NOTE] The requirement description.

### Performance ###
> [!NOTE] 
> The performance characteristics of the system should be outlined in this section. Include specific response times. Where applicable, reference related Use Cases by name.
> * Response time for a transaction(average, maximum)
> * Throughput (for example, transactions per second)
> * Capacity (for example, the number of customers or transactions the system can accommodate)
> * Degradation modes (what is the acceptable mode of operation when the system has been degraded in some manner)
> * Resource use: memory, disk, communications, and so forth

There are few performance requirements, the system doesn't allow for multiple users or transactions it has no degraded modes and should use few resources. Based on stakeholder feedback the following have been established.

**Performance Requirement One**

Operations performed by the system should meet the following criteria:

| Operation | Approx. Time (sec). |
| :-- | :-- | 
| Load | 0.2 |
| Write | 0.5 |
| Display | 0.2 |
| Edit | 0.2 |
| Validate | 1.0 |
| Parse | 0.5 |

**Performance Requirement Two**

Startup operation should be completed in around 2.0 sec.

**Performance Requirement Three**

The memory footprint of the application must be less than 40MB at all times. 

**Performance Requirement Four**

> [!NOTE] The requirement description.


### Supportability ### 

> [!NOTE] 
> This section indicates any requirements that will enhance the supportability or maintainability of the system being built, including coding standards, naming conventions, class libraries, maintenance access, maintenance utilities.

**Supportability Requirement One**

The application must conform to the companies coding standard. 

| Element | Standard | Example |
| :-- | :-- | :-- |
| Variables | Headless camel case | ```int myVariable;``` |
| Attributes | Headless camel case | ```int myAttribute;``` |
| Function Names | Headless camel case | ```int myFunction()``` |
| Method Names | Headless camel case | ```int myMethod()``` |
| Constants | Capitals with underscores | ```const int MY_CONSTANT = 10;```|
| Braces | Use BSD style braces | ```if(true)``` <br>```{``` <br>  ```}``` |

**Supportability Requirement Two**

> [!NOTE] The requirement description.

### Design Constraints ###

> [!NOTE] 
> This section needs to indicate any design constraints on the system being built. Design constraints represent design decisions that have been mandated and must be adhered to. Examples include software languages, software process requirements, prescribed use of developmental tools, architectural and design constraints, purchased components, class libraries, and so on.

**Design Constraint One**

Application must be written in the C++ programming language. 

**Design Constraint Two**

Application must have an object orientated design. 

**Design Constraint Three**

Application must require no additional libraries over the C++ standard libraries. 

**Design Constraint Four**

Application should compile and run across all currently supported platforms i.e.  Windows 11, Linux (6.x) and macOS (13.0) and later. 

**Design Constraint Five**

> [!NOTE] The requirement description.
 
### Online User Documentation and Help System Requirements ###

>[!NOTE] 
> Describes the requirements, if any, for on-line user documentation, help systems, help about notices, and so on.

Help is provided via a ```Help``` menu item, this will be located in the ```About``` menu.  The documentation will cover the principle operations of the system and normal order of operations. However, there will not be exhaustive documentation as the system is intended for expert users. 

### Purchased Components ###

> [!NOTE] 
> This section describes any purchased components to be used with the system , any applicable licensing or usage restrictions, and any associated compatibility/interoperability or interface standards.

Not applicable.

### Interfaces ###

> [!NOTE] 
> This section defines the interfaces that must be supported by the application. It should contain adequate specificity, protocols, ports and logical addresses, and so forth, so that the software can be developed and verified against the interface requirements.

Not applicable.

### User Interfaces ###
> [!NOTE] 
> Describe the user interfaces that are to be implemented by the software.
>

A window based GUI is required with the following top level options:

| Menu Option | Argument | Argument Type | Description |
| :-- | :-:| :-: | :-- |
| Load | filename| text | File to be loaded.  |
| Display | None | N/A | Show the file in a suitable format on screen. E.g. a text window, table or tree view. |
| Save | N/A | N/A | Write to an alternative output file |
| Save As | filename | text | Write to an alternative output file | 
| Edit | As required. | As required | Change the appropriate property in memory and update the display. |
| Help | N/A | N/A | Shows the help documentation explaining the options above.|
| About | N/A | N/A | Shows version/build information and product details. |  


**TODO** 
- User interface details (forms/screens)
- Wireframe for application


### Hardware Interfaces ###
> [!NOTE] 
> This section defines any hardware interfaces that are to be supported by the software, including logical structure, physical addresses, expected behaviors, and so on.

Not applicable. 

### Software Interfaces ###
> [!NOTE] 
> This section describes software interfaces to other components of the software system. These may be purchased components, components reused from another application or components being developed for subsystems outside of the scope of this SRS, but with which this software application must interact.

The ```.scene``` file effectively forms an interface between the Ogre Scene File Editor and the Ogre3D graphics engine the complete format is documented only by it's [Document Type Definition (DTD) file](https://www.w3schools.com/xml/xml_dtd.asp) (provided [here](https://github.com/OGRECave/ogre/blob/master/PlugIns/DotScene/misc/dotscene.dtd),) which defines a valid document. Current documentation for the DotScene format is located [here](https://ogrecave.github.io/ogre/api/latest/dotscene_overview.html) along with the following example:

```xml
<scene formatVersion="1.1">
    <nodes>
        <node name="Robot">
            <position x="10.0" y="5" z="10.5" />
            <scale x="1" y="1" z="1" />
            <entity name="Robot" meshFile="robot.mesh"/>
        </node>
        <node name="Omni01">
            <position x="-23" y="49" z="18" />
            <rotation qx="0" qy="0" qz="0" qw="1" />
            <scale x="1" y="1" z="1" />
            <light name="Omni01" type="point">
                <colourDiffuse r="0.4" g="0.4" b="0.5" />
                <colourSpecular r="0.5" g="0.5" b="0.5" />
            </light>
        </node>
    </nodes>
</scene>
```

There are many API's that are availible and suitible to us such as: TinyXML, TintXML2, RapidXML, PugiXML, TinyXML++, Xerces, irrXML and libXML2. A review was carried out to see which one would be the most benificial to use. Majority have a small footprint apart from irrXML and LibXML2. TinyXML was found to have a good amount of documentation behinid it when comparing it to the other API's that are currently part of the review. However the most suitable one to use for this project is TinyXML. Thhis is because it is very strightforward to use and is easy to integrate. It is also smaller than other API's but has everyhting that we need on it (basic features for editing a scene file) which gives it an advantage over the others. After looking through the options fully, TinyXML was the API being used.According to 'IEEE' (Institue of electrical and electronics ennginers), TinyXML is easy to install and because of its small size it will be much easier to understand. 'Thomason' also stated that it is a very efficient C++ parser and that it is compatible with CMake gives it a boost. However it is still stated that there are holdbacks to TinyXML such as, it does not have a second library, and that if the said system requires more complete XML's then TinyXML does not have the cabability to parse XLS's or DTD's.

### Communications Interfaces ###
> [!NOTE] 
> Describe any communications interfaces to other systems or devices such as local area networks, remote serial devices, and so on.

Not applicable. 

### Licensing Requirements ###
> [!NOTE] 
> Defines any licensing enforcement requirements or other usage restriction requirements that are to be exhibited by the software.

The software will be licensed by **Gerkin Hammer Games** for internal use only.  If the Gerkin Engine and tooling is ever licensed to another company this software would have to be included in that licensing agreement. 

### Legal, Copyright, and Other Notices ###
> [!NOTE] 
> This section describes any necessary legal disclaimers, warranties, copyright notices, patent notice, wordmark, trademark, or logo compliance issues for the software.

Ogre3D is licenced by Torus Knot Software Ltd (TKS) based in Guernsey. The software makes no use of their code but does read and write their ```.scene``` files. While the GerkinEngine has to display notices as a result and contributions to the Ogre3D codebase are subject to the Contributor Licence Agreement, this software has no such restrictions. 

<!--

TODO:
 * Add licences for any dependent libraries here!

-->

### Applicable Standards ###
> [!NOTE] 
> This section describes by reference any applicable standards and the specific sections of any such standards that apply to the system being described. For example, this could include legal, quality and regulatory standards, industry standards for usability, interoperability, internationalization, operating system compliance, and so forth.

<!-- TODO 
  * Identify suitable HCI standards.
>

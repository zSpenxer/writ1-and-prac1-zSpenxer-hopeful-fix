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

table, tr, th, td {
    border-width: 1px;
    border-color: black !important;
    border-style: solid;
    border-collapse: collapse;

    /*tr:hover {background-color: coral;}*/
    width: 50%;
    line-height: 1;
}

</style>

# System/Programme Name #
## Use Case Realisation <br> For <Use Case Name / ID> ##

> [!NOTE]  
> This is a template, one of these will be created for each Use Case we realise during the Elaboration phase.  

## Version ```1.0``` ##

### Design Class Diagram ###
> [!NOTE]  
> The design class diagram relevant to this Use Case Realisation, note that in larger systems this may be restricted to the classes involved in this Use Case Realisation rather than the whole class architecture. 

![classdiagram](images/bigclassdiagram.svg)

### System Sequence Diagram ###
> [!NOTE]  
>The system sequence diagram shows the use case as a sequence of interactions with an external actor – the system act as a black box.

![ssd](images/ssd.svg)

### Sequence Diagram ###
> [!NOTE]  
>The Sequence Diagram documents the handling of the messages from the System Sequence Diagram by classes from the Design Class Diagram. GRASP patterns are used here to provide guidance on key design decisions. 

![sd](images/sd.svg)


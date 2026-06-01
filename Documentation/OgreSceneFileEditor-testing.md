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

# Ogre Config File Editor #
## Testing <br> For Ogre Config File Editor ##
## Version ```0.12``` ##

> [!NOTE] 
> This section documents the planned tests for each stage of the software development project. This may include: Unit, Integration or System Testing for the relevant component. Template below can be used for each group of tests. 

| Test Name | Input | State | Expected Output | Expected State | Actual Output | Actual State |
|:-- |:-- |:-- |:-- |:-- |:-- |:-- |

> [!IMPORTANT] These are not complete!

### Unit Testing ###
> [!NOTE] 
> Unit Tests are for very small software elements e.g. a method from a class.  These tests are often automated using Testing Frameworks such as xUnit or Google Test, include any relevant unit tests here.

| Test Name | Input | State | Expected Output | Expected State | Actual Output | Actual State |
|:-- |:-- |:-- |:-- |:-- |:-- |:-- |

### Integration Testing ###
> [!NOTE] 
> Integration Tests are larger than a Unit test and may involve multiple software elements e.g. multiple classes cooperating to perform an action as in the realisation of a low level use case.  These tests also often automated using Testing Frameworks such as xUnit or Google Test, include any relevant integration tests here.
>

| Test Name | Input | State | Expected Output | Expected State | Actual Output | Actual State |
|:-- |:-- |:-- |:-- |:-- |:-- |:-- |
| Load valid scene file	| extendedTest.scene	| Loader constructed	| formatVersion='1.1'	|Scene object populated	|As expected	| Pass| | |
Parse node count	| extendedTest.scene	| Scene parsed	| nodeCount==2	| Nodes list populated	| 2	| Pass | | |
Parse entity mesh name	| extendedTest.scene	| Scene parsed	| meshfile=='robot.mesh'	| Entity populated	| As expected	| Pass| | | 
Open missing file	| does_not_exist.scene	| Loader constructed	| Throws DocumentLoadFailed	| No scene created	| Exception thrown	| Pass | | |


> [!IMPORTANT] These are not complete!

### System Testing ###
> [!NOTE] 
> System tests are typically based on Use Case along with the Supplementary Specification these are essentially tests of the system from the user perspective.  These tests are less often automated and are often manually performed by dedicated teams.

| Test Name | Input | State | Expected Output | Expected State | Actual Output | Actual State |
|:-- |:-- |:-- |:-- |:-- |:-- |:-- |
| Display Scene File Data | Correctly formatted ```.scene``` file | No current scene. | Scene information displayed on screen | Display scene in treeview | Scene file is displayed in treeview | Scene data is displayed |
| Display Scene File Data | Incorrectly formatted ```.scene``` file | No current scene. | "Invalid File Error" is displayed. | Error occours | The application crashes | 
| Display Scene File Data | Correctly formatted ```.scene``` file | A scene is already loaded. | Scene information displayed on screen, replaces existing scene file information. | Displays new scene date | Scene infomation is displayed on scene | Scene data is displayed |

> [!IMPORTANT] These are not complete!
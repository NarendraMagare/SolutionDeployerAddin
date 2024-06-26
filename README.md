# SolutionDeployer
Useful for developers and admins. It helps user to list all unmanaged solutions from given source environment. User can select one solution and deploy it to target environment.
This tool will take care export and import process, if there are any missing dependencies at target environment, this tool will show list of missing components. User can select a missing component and click on Resolve Dependency.

Refer [Planned for future](https://github.com/NarendraMagare/SolutionDeployerAddin/edit/main/README.md#planned-for-future) section for upcomging features

## NOTE
1) Current version of the tool supports resolution of attribute type of components(missing dependency) only.
2) Support for other components is planned in coming releases.
3) Deployes unmanaged version of solution. 

### User Guide

1. Open Solution Deployer addin.

    ![image](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/3caf0837-e353-49ac-a969-70f220759f6e)

2. This will ask for source environment connection. Connect to source organization

    ![SourceConnection](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/127dea5c-65a5-4836-87b3-432f350a761b)

3. Click 'Connect Target'  buttong for target environment connection.

    ![image](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/28cb6b02-ed47-4681-ac37-84cbfb6ebce5)

4. Target environment name will be displayed upon successfull connection

    ![image](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/59dbd8f3-c034-49e6-b03f-1a9c52c31510)

5. Click 'Load Source Solutions' to show list of solutions from source environment.

    ![image](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/c013da87-c6c7-48c1-93b6-9364b6dda766)

    ![image](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/c88a8705-a56e-4adc-a5a3-46792ba85f85)

6. From list of source solutions, select a solution to be deployed to target environment and click 'Deploy Selected Solutin to Target'.

    ![image](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/509d4538-9420-4e25-b3b9-7d0d8ec763d6)

7. This will initiate deployment of selected solution to target environment.
8. If the solution is imported succesfully, below message will be shown. Please publish solution manually (auto publishing is planned for coming releases)

    ![image](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/65b4bc66-009e-43e3-998e-a07123082f8f)

**Component Resolution**
   
12. If there are any dependency errors while importing solution, those errors will be listed in 'Dependencies' grid 

    ![image](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/a2aaab62-1585-42ef-8d3c-62dc5d627f45)

    This grid shows details about Required Component (RC) and component which is dependent on it(DC).
    - Required Components. Columns having header text prefixed with RC_ show information about required component.

        ![image](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/69e464cd-5fc2-421e-a063-f55143704645)
      
    - Dependent Component. Columns having header text prefixed with DC_ show information about dependent component.

        ![image](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/b540d292-27de-4465-b51e-2767af3b9b4a)

    - To resolve component dependency, click on checkbox in Select column (First column)
   
        ![image](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/cc65ad8c-1633-4a99-a3b4-ae67c1f59bca)
  
    - Also note Resolved column value ( Last column) for selected row. Resolved flag indicates if the component is successfully resolved or not.

        ![image](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/e4078c9f-170c-40ea-bb72-c142d7076d84)

    - After component is selected, click 'Resolve Selected Dependency at Source' button. This will initiate component resolution
    - Post completion of the operation, check 'Resolved' flag for the row. This flag turns True if component is successfuly resolved at source solution.

        ![image](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/33167d0a-a1da-4ce6-b947-dcca04308274)

    - Initiate Solution deployment process again by Loading solution and deploy it ( refer step 7 above). 

**Settings file**

Tool maintains settings file "SolutionDeployer.xml" typically located at "AppData\Roaming\MscrmTools\XrmToolBox\Settings\". Currently file contains list of solutions to be restricted the movement from one environment to another. Additional solutions can be added to this list as needed.

![image](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/81febb03-5565-485a-b17b-73109941b536)

**Limitations**

Few dependency errors such as below cant be automate currently. Those should be resolved manually at source.
Few dependencies are 

![image](https://github.com/NarendraMagare/SolutionDeployerAddin/assets/10857505/17d98c06-f38d-4b5c-b6ac-a15673aa7d68)


`Error importing solution
The entity relationship role of the referencing entity is required when creating a new one-to-many entity relationship new_FileAttachment_Account_sdp_test9.`

# Planned for future

1. Support for export as managed solution and versioning.
2. Support for additional component types.
3. Support for filtering rows based on component type in Dependency grid.
4. Support for multiple solution deployments.
5. Option to opt for automatically publishing solution after importing it to target.
6. UI improvements
   
for further details
Check [Project](https://github.com/users/NarendraMagare/projects/4) 
or contact jsgenerate7@gmail.com


# DevOps_Deployment_Strategy
<H1>Summary</H1>
 This article describes, how you can
 
   - Structure your application repositories 
   - Templatize CICD pipelines into stages and steps 
   - Modularize pipelines for better management 
 
 Sharing some if the practices i used while designing my devops strategy. I will happy to accept inputs from all. 

<H1> Strategy Diagram </H1>

![devops logo](https://raw.githubusercontent.com/amtkmr1990/DevOps_Deployment_Strategy/main/DevOpsRepoStructure.drawio.png)

<H2> Repositories </H2>
 You can have seperate repos for API, UI and DBSQL. This can help parallel development and reduce PR conflits. 
 **src/** folder can contain all source code files 
 **pipelines** folder will have our CICD pipelines. This yaml pipeline will call stage templates. Stage templates will call steps templates.

<H2> Stages </H2>
 Stage yaml template will define how to call step template (for each ENV) and pass required service connection and parameter. This makes easy to add or remove any step template and also reduce repetation of steps under each stages (Dev/UAT/PROD).  
 Refer tempaltes under Stages Folder here. 
 
<H2> Steps </H2>
 This folder can have different templates. Each template to achive specific set of tasks. Keeping the template seperate (modules) can help in managing and enhancing for future development. This will modularize templates and reduces repitattion of tasks in each stage.
 

 

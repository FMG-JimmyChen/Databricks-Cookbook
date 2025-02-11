# Databricks-FMG Guide 
This guide draws upon experience coaching teams and working on various projects, as well as insights from the open-source community.

Regarding Databricks, and Spark in particular, the source code is **written once**  by its author but **read and modified multiple times** by numerous engineers. Subsequent modifications can introduce bugs.

Given the nature of Spark's codebase development, we must optimize our own codebase for consistency with Spark's style. This ensures long-term, global readability and maintainability.

**A simple code is the most effective solution.**

## <a name='TOC'>Table of Contents</a>
- [Databricks-FMG Guide](#databricks-fmg-guide)
  - [Table of Contents](#table-of-contents)
  - [Document History](#document-history)
  - [Databrircks, Synapse \& GitHub](#databrircks-synapse--github)
  - [Github Repo Setup on Databricks](#github-repo-setup-on-databricks)
  - [Development Guidance on Databricks/GitHub](#development-guidance-on-databricksgithub)

   
## <a name='history'>Document History</a>
- 18/03/2024: Initial version.

## <a name='shortcut'>Databrircks, Synapse & GitHub</a>
- [Databricks Prod](https://adb-5878762332215882.2.azuredatabricks.net/?o=5878762332215882)
- [Databricks Dev](https://adb-8285578967294844.4.azuredatabricks.net/?o=8285578967294844)
- [Synapse Prod](https://web.azuresynapse.net/en/home?workspace=%2Fsubscriptions%2Ff48f9936-8f2a-4773-aa5e-06c2ac54c51b%2FresourceGroups%2Ffzdatorpdrgp002%2Fproviders%2FMicrosoft.Synapse%2Fworkspaces%2Ffzdatorpdasa002)
- [Synpase Dev](https://web.azuresynapse.net/en/home?workspace=%2Fsubscriptions%2F39c4d95e-080f-4278-8633-ed984324ce10%2FresourceGroups%2Ffzdatornprgp002%2Fproviders%2FMicrosoft.Synapse%2Fworkspaces%2Ffzdatornpasa001)

GitHub repositories are being used:
- [fmgcore/fmg-dataorchestration](https://github.com/fmgcore/fmg-dataorchestration) 
    * Protected Branches:
        * master: equivalent to the current production code<br>
          The ***master branch** tracks **dev-release** only 
        * dev-release: the code in the **dev-release** is deployed to a suitable test environment, tested and any issues are resolved.<br>
          Once the testing is complete and the release is finalized, **dev-release** is merged into **master** for production.
 
**API Reference** for all public PySpark modules, classes, functions and methods:
- [Spark SQL](https://spark.apache.org/docs/latest/api/python/reference/index.html)


## <a name='setup'>Github Repo Setup on Databricks</a>

Follow the process and set up your Databricks
- [Configure Git credentials & connect a remote repo to Databricks](https://docs.databricks.com/en/repos/get-access-tokens-from-git-provider.html#github-personal-access-token)

## <a name='practice'>Development Guidance on Databricks/GitHub</a>
Gitbub practice that FMG follows:
- [The FMG Github flow process](https://farmersmutualgroup.atlassian.net/wiki/spaces/BIS/pages/1534328833/The+FMG+Github+flow+process+a+presentation+for+the+uninitiated)
- [Git& GitHub Best Practice](https://farmersmutualgroup.atlassian.net/wiki/spaces/BIS/pages/6750294/Git+GitHub+Best+Practice)
- [Current methodology: GitHub flow](https://farmersmutualgroup.atlassian.net/wiki/x/VYAKVg)
- [Previous methodology: GitFlow](https://farmersmutualgroup.atlassian.net/wiki/spaces/BIS/pages/1443528730/Previous+methodology+GitFlow)

The Databricks workflow we adopted for solution delivery deviates slightly from FMG's internal guidelines.

The key difference lies in the use of a **dev-release** branch for solution delivery. All intended changes are merged into this branch before being merged into **master**.

Due to the interaction between the Synapse and Databricks repositories, this additional branch (**dev-release**) serves to protect **master** and facilitate rapid development and testing.  This also enables changes to be shared within the development environment.

Key points to be followed on Databricks & Synapse:
1. For Databricks and Synapse development, we should always create branches based on the **dev-release** branch. All intended changes (whether code or pipeline modifications) should be merged into **dev-release** before being merged into **master**.
2. Source data files stored in Azure Data Lake are accessible by Databricks because the Data Lake is mounted to dev/prod Databricks (eg. /mnt/structured/CRM/)
3. 

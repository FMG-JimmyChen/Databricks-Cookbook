# Databricks-FMG Guide 
This guide draws from the experience coaching and various projects as well as the open source community.

On Databricks, specifically speaking, the source code of Spark is **written once**  by its author, but **read and modified multiple times** by lots of engineers which the future modification of the code may subsequently come with bugs.

As of the nature of Spark's codebase development, we need to optimize our codebase to be consistent with Spark to obtain a long-term, global readibility and maintainability. 

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
        * master
        * dev-release

**API Reference** for all public PySpark modules, classes, functions and methods:
- [Spark SQL](https://spark.apache.org/docs/3.1.3/api/python/reference/pyspark.sql.html)


## <a name='setup'>Github Repo Setup on Databricks</a>

Follow the process and set up your Databricks
- [Configure Git credentials & connect a remote repo to Databricks](https://docs.databricks.com/en/repos/get-access-tokens-from-git-provider.html#github-personal-access-token)

## <a name='practice'>Development Guidance on Databricks/GitHub</a>
Gitbub practice that FMG follows:
- [The FMG Github flow process](https://farmersmutualgroup.atlassian.net/wiki/spaces/BIS/pages/1534328833/The+FMG+Github+flow+process+a+presentation+for+the+uninitiated)
- [Git& GitHub Best Practice](https://farmersmutualgroup.atlassian.net/wiki/spaces/BIS/pages/6750294/Git+GitHub+Best+Practice)
- [Current methodology: GitHub flow](https://farmersmutualgroup.atlassian.net/wiki/x/VYAKVg)

The Databricks flow we adopted for delivering solution differs a little bit from FMG’s internal guidelines.

The key difference inhabits in the use of **dev-release** branch for delivering solution in which all intended changes should be merged before **master**.

Due to the interaction with repositories between Synapse and Databricks, an additional barrier (**dev-release**) is made made to protect **master** and allow the development to interate quickly as well as the testing so changes can be shared within the development environment.  

Key points to be followed on Databricks:
1. Always creating branch on the basis of dev-release branch where all intended changes should be merged into before master.
2. 
3. 

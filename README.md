# Databricks-FMG Guide 
This guide draws from the experience coaching and various projects as well as the open source community.

On Databricks, specifically speaking, the source code of Spark is **written once**  by its author, but **read and modified multiple times** by lots of engineers which the future modification of the code may subsequently come with bugs. As of the nature of Spark's codebase development, we need to optimize our codebase to be consistent with Spark to obtain a long-term, global readibility and maintainability. 

**A simple code solution is the most effective approach.**

## <a name='TOC'>Table of Contents</a>
1. [Document History](#history)
2. [Databrircks, Synapse & GitHub](#shortcut)
3. [Github Repo Setup on Databricks](#setup)
4. [Best Practice of Development on Databricks](#practice)
   
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

## <a name='setup'>Github Repo Setup on Databricks</a>

Follow the process and set up your Databricks
- [Configure Git credentials & connect a remote repo to Databricks](https://docs.databricks.com/en/repos/get-access-tokens-from-git-provider.html#github-personal-access-token)

## <a name='practice'>Best Practice of Development on Databricks</a>

The Databricks workflow we adopted follows standard development best practices. The key difference is the platform on which we develop, test, review and release.

Key points to be followed on Databricks:

# Databricks-Cookbook
This guide draws from the experience coaching and various projects as well as the open source community.

In Databricks, specifically speaking, the source code of Spark is **written once**  by its author, but **read and modified multiple times** by lots of engineers which the future modification of the code may subsequently come with bugs. As of the nature of Spark's codebase development, we need to optimize our codebase to be consistent with Spark to obtain a long-term, global readibility and maintainability. 

**A simple code solution is the most effective approach.**

## <a name='TOC'>Table of Contents</a>
1. [Document History](#history)
2. [How We develop in Databrciks at FMG](#structure)
## <a name='history'>Document History</a>
- 18/03/2024: Initial version.
## <a name='structure'>Workflow in Databricks</a>

The Databricks workflow we adopted follows standard development best practices. The key difference is the platform on which we develop, test, review and release.

Follow the process and get your work flow
- [Configure Git credentials & connect a remote repo to Databricks](https://docs.databricks.com/en/repos/get-access-tokens-from-git-provider.html#github-personal-access-token)
- 

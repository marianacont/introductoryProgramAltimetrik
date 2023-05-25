#Git Branch Strategies

Each development team utilizes a different Branch strategy, according to how branches are used in the development process.
There are strategies that adjust better to team sizes, deployment frequency, etc.
A strategy depends on how much work should remain in a branch before getting merged back into main. 

##1 - Trunk Based Development
This is the easiest strategy to apply. In this case, everybody in the team clones the main repository, works on his own and pushes the changes to the main branch. So, there is only one branch in the project.
Before pushing changes you should be sure that everything has been tested and is working.
It is demanding in this type of strategy to use feature toggles, also called features flags. They allow you to enable or disable specific functionality in your software 
without updating the code itself. This way you can continue to deploy from the master branch without making the new features immediately available to users.
In Trunk strategy the team works in continuous deployment.

##2 - Feature Branching || GitHub Flow
There is a mainline, but when we want to work on some feature, we create a new branch. Features are typically split into small pieces, and the delivery cycles are short.
Features toggles are recommended to use. They make it easy to deploy code into main and control when the feature is activated, making it easy to initially deploy the code well before the feature is exposed to end-users. 
Pull requests are a must, not only when work is done, but whenever you need feedback.

##3 - Forking Strategy
Is very similar to Feature Branching, but the major difference is that we don’t create branches from the main branch. Instead we fork the whole repositories, work on the feature, and then create a pull request.
The most common use of this strategy is open-source projects.
The major advantage is that we don’t need to deal with permissions. Only a few people have access to the repository and others can read and fork it.

##4 - Release Branching
It has a branch for each entire release. All changes for the release need to be applied twice: once to the branch and then to the main code line. That implies more work.Release branches can be unwieldy and hard to manage as many people are working on the same branch.
It’s typically associated with low frequency deployments.
This strategy is not recommended as it could have merge conflict, deviations, there is no continuous integration.

##5 - Task Branching
Also known as issue branching, Task Branching directly connects tasks with the source code. Each issue is implemented on its own branch with the issue key included in the branch name. 
Since agile centers around user stories, task branches pair well with agile development. Each user story (or bug fix) lives within its own branch, making it easy to see which issues are in progress and which are ready for release. 

#Git Workflow
A Git workflow is a recipe or recommendation for how to use Git to accomplish work in a consistent and productive manner. Git workflows encourage developers and DevOps teams to leverage Git effectively and consistently.

##Links
- Branching Strategies Explained:  https://www.youtube.com/watch?v=U_IFGpJDbeU&ab_channel=DevOpsToolkit 
- Atlassian guide: Branching Strategy https://www.atlassian.com/agile/software-development/branching 
- https://littlekendra.com/2020/01/10/why-i-like-the-release-flow-branching-strategy-with-git-for-database-devops/ 

## Namespace Controller Selector

This project is forked from the open-source ASP.NET samples located at http://aspnet.codeplex.com/SourceControl/latest. The project is specialized for Namespace versioning and changes from self-hosted to IIS or IIS Express.

### Forking method

To create this repository I cloned the original repository and filtered its history using the following commands:

    PS D:\projects> git clone aspnet webapi-namespaceversioning
    Cloning into 'webapi-namespaceversioning'...
    done.
    Checking out files: 100% (4058/4058), done.
    PS D:\projects> cd webapi*
    PS D:\projects\webapi-namespaceversioning> git remote rm origin
    PS D:\projects\webapi-namespaceversioning> ls

        Directory: D:\projects\webapi-namespaceversioning

    Mode                LastWriteTime         Length Name
    ----                -------------         ------ ----
    d-----        12/3/2015  12:55 PM                Samples
    d-----        12/3/2015  12:56 PM                Tools
    -a----        12/3/2015  12:55 PM            715 .gitattributes
    -a----        12/3/2015  12:55 PM            179 .gitignore

    PS D:\projects\webapi-namespaceversioning> git checkout -b develop
    Switched to a new branch 'develop'

    PS D:\projects\webapi-namespaceversioning> git filter-branch --prune-empty --subdirectory-filter Samples/WebApi/NamespaceControllerSelector -- --all
    Rewrite 6d625e87305b20ed6068d7412fdd2601c2f7899a (8/8)
    Ref 'refs/heads/develop' was rewritten
    PS D:\projects\webapi-namespaceversioning> ls

        Directory: D:\projects\webapi-namespaceversioning

    Mode                LastWriteTime         Length Name
    ----                -------------         ------ ----
    d-----        12/3/2015  12:58 PM                .nuget
    d-----        12/3/2015  12:58 PM                Controllers
    d-----        12/3/2015  12:58 PM                Properties
    -a----        12/3/2015  12:58 PM           1258 App.config
    -a----        12/3/2015  12:58 PM           5568 NamespaceControllerSelector.csproj
    -a----        12/3/2015  12:58 PM           1460 NamespaceControllerSelector.sln
    -a----        12/3/2015  12:58 PM           5413 NamespaceHttpControllerSelector.cs
    -a----        12/3/2015  12:58 PM            822 packages.config
    -a----        12/3/2015  12:58 PM           2786 Program.cs
    -a----        12/3/2015  12:58 PM           1328 ReadMe.txt

As you can see, the new repository is filtered to the contents of the NamespaceControllerSelector folder in the original Codeplex repo.
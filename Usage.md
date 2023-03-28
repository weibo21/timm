如果你想在GitHub上fork别人以前版本的仓库，可以按照以下步骤操作：

打开原始仓库的页面并找到要fork的特定版本的commit或分支。

点击“Clone or download”按钮并复制该仓库的URL。

在GitHub上创建一个新的仓库，命名为你想要的名字，并将其设置为“Public”或“Private”。

在本地终端中使用git clone命令将新的仓库克隆到你的计算机中。

    git clone <新仓库URL>
    
进入新克隆的仓库目录，使用以下命令将原始仓库添加为一个远程仓库：

    git remote add upstream <原始仓库URL>
    
拉取原始仓库的代码并检查出要fork的特定版本的commit或分支：

    git fetch upstream
    git checkout <commit或分支名称>

查询分支：

    git branch
    
将当前状态转换为新分支，然后将其推送到远程仓库。可以使用以下命令创建一个新分支：

    git branch new_branch_name

然后，将HEAD指向该分支：

    git checkout new_branch_name

现在，您可以将新分支推送到远程仓库：

    git push -u origin new_branch_name

### git 
### git分为：工作区、暂存区、历史区
- 工作区：就是你工作的地方(写代码的地方)
- 暂存区：临时存储代码的地方
- 历史区：生成历史版本

### git安装

### git的全局配置
    - 第一次安装成功以后，我们需要在全局环境下配置基本信息
    - git config --global -l(--list) :查看全局的配置信息

    - 配置名字有邮箱
    - git config --global user.name 'xxx'
    - git config --global user.email 'xxx@xxxx'
    - clear:清屏
    - 按上下键，可以查看之前输入过的历史命令

### 创建仓库，完成版本控制
    - git init:在你的电脑上创建一个git仓库
    - 创建完成之后会默认生成一个.git文件，里面存储的是当前仓库的信息

### 在本地编写代码，再把工作区的代码上传到暂存区
    - git add . : 把工作区所有的修改的文件上传到暂存区
    - git add A : 把工作区所有的修改的文件上传到暂存区
    - git add '文件名' ：把工作区指定的修改的文件上传到暂存区
    - git status：查看当前修改的文件在哪个区域

### 把暂存区的代码提交到历史区
    - git commit -m'注释'
    - git log:查看历史版本记录
    - git reflog：查看所有的历史记录

### 回滚指定的历史版本
    - git reset --hard 七位历史版本号

==================================================================
### gitHub
    > https://github.com/

    是一个开源的代码管理平台，用户注册之后，进行登录，然后就可以创建远程仓库了，
1、点击右上角邮箱的下拉三角 -->Settings
    Profile(修改自己的基本信息)
    Account(修改用户名)【慎重】
    User security(修改用户密码)
2、创建项目
    点击左上边绿色的new按钮
        Public 公共的开源项目
        peivate：私有的项目
    
    README：勾选上就会默认创建一个描述项目的md文件，在这里边你可以写一些你的整个项目的描述

    最后点击 create repository 就会生成一个项目

3、把本地仓库的代码提交到远程仓库
    (1):建立本地仓库和远程仓库的连接
        - git remote -v:查看连接状态
        - git remote add origin 远程仓库的地址
        - git remote rm origin 解除关联

    (2)向远程仓库提交代码
        git pull origin master (下拉代码)
        git push origin master (上传代码)

4、克隆项目
    git clone 远程仓库地址
        先创建一个文件夹 
        git init
        git remote add origin xxx
        git pull
        git push

    (1)真实的项目负责人，把远程仓库创建好，(把你添加为协作者)
    (小组成员通过git clone把远程仓库拉取到自己的电脑上)【把远程仓库克隆到自己的电脑上 在你的电脑上创建一个文件夹  git init / git remote add xxx / git push】



    git clone xxx
    新增内容
    git add . 
    git commit -m'注释'
    git push

### 我的补充
   - git branch  查看分支
   - git branch <name>   创建分支
   - git switch <name>   切换分支(或者 git checkout <name> )
   - git switch -c <name>   创建+切换 分支 ( 或者 git checkoout -b <name> )
   - git merge <name>   合并某分支到当前分支
   - git branch -d <name>   删除分支
   - $ git pull origin master:master    后面是本地分支名


    







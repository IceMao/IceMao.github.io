# IceMao.github.io

## config分支

用来保存`hexo`博客相关的配置文件

1. `_config.yml`, `package.json`, `source/`，`scaffolds/`，`themes/`

2. 根目录的`_config.yml`和`themes`文件夹下所使用主题的`_config.yml`需要根据需要修改

## 保存配置文件的方法

通过将相关配置保存在同项目的分支的方法，可以方便以后的项目迁移，方法如下：

#### 1. 新建分支 如：config，并删除新建分支时同步的master中的内容

````
git clone <地址>
git branch -a 查看分支
git checkout config 切换分支

git rm * -r
git commit -m"rm *"
git push
````

#### 2. 在本地hexo 博客根目录 初始化git

````
git init
````

#### 3. 添加远程主机，拉取分支信息并切换分支

````
git remote add origin <地址>
git pull 更新
git checkout config 切换分支
````

#### 4. 将不需要提交的部分通过 `.gitignore`文件忽略，然后将文件提交到远程分支

````
git add . 
git commit -m"message"
git push
````
## 项目迁移

当需要迁移项目时：

0. `clone`分支内容到本地
1. `npm install` 安装依赖项
2. `hexo server` 本地查看是否运行正常
3. `hexo generate` 生成/渲染
4. `hexo deploy` 部署到`github`

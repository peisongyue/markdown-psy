> _src_ 目录结构
![[Pasted image 20230609171459.png]]
> 项目规范
![[1686303885399.png]]
> _git init_

> _npm i husky -D_   
>> `husky是做git相关的一些钩子管理的`

> _npx husky install_  
> >`npx 会在本地环境下查找是否可执行的命令，没有找到的话再从全局查找是否安装对应的模块`
> _npx husky add .husky/pre-commit "npm run lint"_  
> >`在git 提交之前执行一下lint`

> _git init_
> _git add ._
> _git status_
> _git commit -m'first int commit '_

![[1686305400491.png]]

> _npm install -D commitlint @commitlint/config-conventional @commitlint/cli_
> _npx husky add .husky/commit-msg 'npx --no -- commitlint --edit ${1}’_  
>> `git在提交信息时来执行committed, 来校验最新的一条lint,log信息是不是符合要求`
> `{
> 	'extends":["acommitlint/config-conventional"]
> }`
>>`创建.commitlintrc 添加配置文件`

> git add . 
> git commit -m'feat: add commit lint for vue-bilibili'
# ReactComponent_ui
React 组件库
  



git Actions 使用

// 利用git Actions 自动部署到git pages

在项目根目录下创建文件夹.github, 然后在此文件夹下面创建workflows文件夹，github只要发现.github/workflows文件夹下面有.yml文件，就会自动运行该文件
创建github下面的yml 文件





参考： https://juejin.cn/post/6870372475188969479
gitActions 文档: https://docs.github.com/cn/actions/learn-github-actions/understanding-github-actions
https://juejin.cn/post/6931269326339702791

### 配置issuse 项目模版
1. 可以通过github网站项目的setting中设置,这样就会默认在.github.workflows中生成一个ISSUE_TEMPLATE文件夹，里面生成bug_report.yml,也可以自己设置文件夹内容。例如 feature_request.yml
// 文档：https://docs.github.com/cn/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository
2. 如果您愿意在 GitHub 之外接收某些报告，您可以使用 contact_links 将用户引导到外部站点。在ISSUE_TEMPLATE文件夹 内新建一个config.yml文件
// 文档 https://docs.github.com/cn/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository#configuring-the-template-chooser
```
blank_issues_enabled: false
contact_links:
  - name: 自定义外部站点链接
    url: https://github.community/
    about: Please ask and answer questions here.
  - name: GitHub Security Bug Bounty
    url: https://bounty.github.com/
    about: Please report security vulnerabilities here.
```



 ## git Actions 
 >git Actions 如果想要对git仓库做一些操作，可能会没有权限，所以需要在git 上面搞一个token,在git 个人主页里面
 >setting 点击，然后点击Developer setting, 然后点击Personal access tokens , 然后 Generate new token, 之后这个token 就可以被github actions 使用ß 通过token,从仓库中拿到原始代码，安装依赖，打包构建，然后放到服务器中（需要知道服务器账号密码地址端口号等）

 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L

 然后进入到ReactComponent_ui 这个代码库里面，。给当前代码库设置一些环境变量，点击settings,然后点击Secrets，点击New repository secret,
 然后将之前获取到的token 设置成变量。然后继续添加其他的变量，。如服务器地址，服务器用户名，服务器密码，gitactions 连接登陆服务器的端口号一般为22，
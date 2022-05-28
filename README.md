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
1. 可以通过github网站项目的setting中设置,这样就会默认在.github.workflows中生成一个ISSUE_TEMPLATE文件夹，里面生成bug_report.yml
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


2. 也可以
2. 也可以
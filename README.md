---
# 功能
  * 每天凌晨自动签到，不需要手动运行。
  * 支持多人同时打卡，打卡结果分别显示。
  * 在其他平台登录健康平台不影响第二天自动签到。
  * 账号和密码以Secret形式存储，正常使用不会导致泄露。  
---  
# 部署
## 1. 复制项目
   * 点击右上角的`Fork`，将项目复制到自己的仓库中。
   ![fork.PNG](https://i.loli.net/2020/11/24/2hTtGldiZF9B7DX.png)
   * (可略过)点击`Fork`左侧的Watch选项有助于您第一时间获取项目最新消息。如果您对本项目还满意，可以点击`Fork`右侧的`Star`对作者表示激励。  
## 2. 添加账号
   * 点击`Settings`-->`Secrets`-->`New repository secret`，进入新建页面。
   ![secrets.PNG](https://i.loli.net/2020/11/24/mIWLRTzUJxuiMHa.png)
   * 在`Name`栏输入`ACCOUNT`，`Value`栏输入自己的学号和密码(默认身份证后8位)，具体格式为学号,密码(;学号,密码;...)。例如`200001010101,01013769`(单人使用)和`200001010101,01013769;200002010102,02032436;200003040205,09082847`(多人使用)。**注意：格式中标点`,`和`;`均为半角标点，使用全角标点`，`和`；`时即使学号密码正确也会导致打卡失败，请注意输入法的中英文状态。**。
   * 点击`Add secret`。
## 3.启用Actions功能
   * 点击上方的`Actions`，点击绿色按钮确认启用Actions。
   * 所有运行结果可以在`Actions`页面点击`View workflow file`查看报告，项目只保留最近3天的运行报告。
   ![check.PNG](https://i.loli.net/2020/11/24/GUEgdrmpIAxlPW5.png)
**注意：打卡内容发生改变时可能会导致打卡失败，此时平台会自动发送一封邮件至注册邮箱内，用户需要进行一次手动打卡更新打卡内容，即可使打卡功能正常运行。Actions启用后连续60天内项目无更改时，平台会关闭本功能，如有需要可定期对仓库内的项目进行无意义的修改。**  
---
# 更新方法
   * 方法一:点击`Settings`-->`Options`-->`Dangerous Zone`-->`delete this reposity`，按照提示删除本项目，然后重新部署。
   * 方法二:使用git指令,指路[相关教程](https://www.runoob.com/git/git-remote-repo.html)

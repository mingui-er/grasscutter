# grasscutter
The local server server of a two-dimensional game
# 0.解压*Resources.zip*获得*Resources*文件夹
# 1.安装java 16 及以上
*https://www.oracle.com/cn/java/technologies/downloads/*
# 2.安装mongdb mongodb-windows-x86_64-5.0.9  或 以上版本
*https://www.mongodb.com/try/download/community*
# 3.安装fidder
*https://www.telerik.com/download/fiddler*
# 4.启动mongdb服务
# 5.启动Fidder服务
打开后点击fiddlerScript
里面内容全选然后吧下面这些粘进去

*/*Original script by NicknameGG, modified for Grasscutter by contributors. */
*mport System;
*mport System.Windows.Forms;
*mport Fiddler;
*mport System.Text.RegularExpressions;
*ar list = [
    *https://api-os-takumi.mihoyo.com/",
    *https://hk4e-api-os-static.mihoyo.com/",
    *https://hk4e-sdk-os.mihoyo.com/",
    *https://dispatchosglobal.yuanshen.com/",
    *https://osusadispatch.yuanshen.com/",
    *https://account.mihoyo.com/",
    *https://log-upload-os.mihoyo.com/",
    *https://dispatchcntest.yuanshen.com/",
    *https://devlog-upload.mihoyo.com/",
    *https://webstatic.mihoyo.com/",
    *https://log-upload.mihoyo.com/",
    *https://hk4e-sdk.mihoyo.com/",
    *https://api-beta-sdk.mihoyo.com/",
    *https://api-beta-sdk-os.mihoyo.com/",
    *https://cnbeta01dispatch.yuanshen.com/",
    *https://dispatchcnglobal.yuanshen.com/",
    *https://cnbeta02dispatch.yuanshen.com/",
    *https://sdk-os-static.mihoyo.com/",
    *https://webstatic-sea.mihoyo.com/",
    *https://webstatic-sea.hoyoverse.com/",
    *https://hk4e-sdk-os-static.hoyoverse.com/",
    *https://sdk-os-static.hoyoverse.com/",
    *https://api-account-os.hoyoverse.com/",
    *https://hk4e-sdk-os.hoyoverse.com/" // Line 24
   *];
*lass Handlers
*
    *tatic function OnBeforeRequest(oS: Session) {
        *ar active = true;
       *if(active) {
            *f(oS.uriContains("http://overseauspider.yuanshen.com:8888/log")){
                oS.oRequest.FailSession(404, "Blocked", "yourmom");
           *}
           *for(var i = 0; i < 24 ;i++) {
               *if(oS.uriContains(list[i])) {
                   *oS.host = "127.0.0.1"; // This can also be replaced with another IP address.
                   *break;
               *}
          *}
       *}
   *}*
};

# 6.解压grasscutter.zip，启动grasscutter.exe
# 7.启动某个二次元游戏
# 8.输入用户名 密码随便输
# 9.在下面的链接进行下载 指令工具
https://github.com/jie65535/GrasscutterCommandGenerator/releases/tag/v1.10.0

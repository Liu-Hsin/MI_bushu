1.
文件夹是建造一个刷步数的网站用的，里面包含一个HTML文件跟CSS文件。直接上传值网站根目录即可。
2.
压缩包文件是部署在腾讯云的云函数里面的。
步骤如下：
1）下载小米运动，注册小米运动账号进入app，点击我的→第三方接入，进行绑定
2）进入腾讯云函数控制台 https://console.cloud.tencent.com/scf/list 选择函数服务→新建
3）函数名称随意填写，运行环境选择python3.6，选择空白函数
4）提交方法选择 “本地上传zip包”然后选择上传此压缩文件。
5）修改代码，user填写小米运动手机号，password填写小米运动密码，key填写在 https://qmsg.zendee.cn/ 申请到的key（推送消息用），qq填写你自己的qq
![image](https://user-images.githubusercontent.com/57285504/114186338-3e73eb00-9936-11eb-90d3-f48871e0f4cc.png)

6）在函数管理处把 执行超时时间 改到900，防止出现奇怪的bug

7）保存并测试如果qq有消息，恭喜你成功了
![image](https://user-images.githubusercontent.com/57285504/114186519-7bd87880-9936-11eb-8d18-e0e4b9db264c.png)

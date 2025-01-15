一位朋友说他们公司不让使用任何代理工具，但是他又经常需要使用 Gemini，有没有什么好办法。今天就分享一个无需代理使用 Gemini 的方法。

需要准备下载 **Chatbox** ：https://chatboxai.app/zh，并获取 **Gemini 的 API key** ：https://aistudio.google.com/apikey。
![image](https://github.com/user-attachments/assets/5293190a-37a7-431e-90bf-25007c242299)

设置Chatbox模型库
![image](https://github.com/user-attachments/assets/f7ef7abd-a1f6-4c5d-a785-2a374109468d)

现在就可以选择模型，并使用 Gemini 了。
![image](https://github.com/user-attachments/assets/34794f5b-c820-48a2-8bbf-48123167c3fb)

虽然可以用 Chatbox 配置 API key 使用 Gemini，但是会发现必须用代理才可以，没有代理是无法使用的。

现在就分享免代理使用 Gemini的详细操作步骤。

1、打开如下 Github 项目，并 **fork** 到自己账号中
https://github.com/PublicAffairs/openai-gemini

2、项目**Readme**中，可以看到该项目可以利用 **Vercel**、**Netlify** 以及 **CF** 等方式部署
![image](https://github.com/user-attachments/assets/4b72ac69-b59c-4f1f-b21d-8e9462022526)

3、今天就用 **CF** 部署方式进行演示，点击 **Deploy with Workers**，然后**授权**
![image](https://github.com/user-attachments/assets/1c7b55b7-1e2c-4625-bafe-633076b863e1)

4、弹出如下窗口，已有账户，点击 **I havee an account**
![image](https://github.com/user-attachments/assets/13d46345-9ca2-436c-ba06-ab599690a088)

5、弹出如下窗口分别获取 CF **账号 ID** 以及**令牌**
![image](https://github.com/user-attachments/assets/0d714601-1158-480f-99d5-bb8037ac0573)

点击 **Workers Dashboard** 打开 CF 账号就可以看到账号 ID，复制粘贴即可。
![image](https://github.com/user-attachments/assets/124f0588-56ef-4a0b-b6e3-927694b8c4eb)

再点击 **My Profile**，点击**创建令牌**，令牌模板选择编辑 **Cloudflare Workers**

权限选择 **均不改变**，账号资源选择 **所有账户**，区域资源选择**所有区域**，点击最下方的继续以显示摘要，然后**创建令牌**
![image](https://github.com/user-attachments/assets/789a40a3-8da6-4a7b-a61e-0604a8de4a9a)

![image](https://github.com/user-attachments/assets/15773aca-0106-4159-afdb-603cf792f701)

6、将**账户 ID** 和 **API Token** 填好，点击 **Connect account**
![image](https://github.com/user-attachments/assets/5fdd5c0c-1540-4919-b544-63eeaf09dccc)

7、提示 **Fork** 项目（已 fork 就忽略），点击 **Repository - Actions**，选择同意，然后点击 **Workflows enabled**，会弹出如下界面，点击 **Deploy**
![image](https://github.com/user-attachments/assets/7a331473-9b83-4257-944f-169ec671897d)

8、当项目由初始化变成功 **Successful**，就代表项目部署完毕
![image](https://github.com/user-attachments/assets/aa076601-6cfb-4b7d-aa5a-8ba9382eb16e)

9、点击上图的 **Worke dash**，就看到 CF worker 中部署了 gemini，打开这个 worker，到设置中，为这个项目添加一个自定义域名
![image](https://github.com/user-attachments/assets/3278fef9-1188-4988-9529-2da7dfd27dba)

到这里，中转域名就设置完毕。现在我们进入 Chatbox 进行设置

1、打开 Chatbox **设置**，因为设置了中转域名，就可以直接使用 OpenAI 格式，粘贴 Gemini API KEY, 把刚才自己的自定义域名填写上
![image](https://github.com/user-attachments/assets/694e4f52-39a1-4f71-a630-5ed96c941ac9)

2、点击**模型**，点击**自定义模型**，填写模型名 **gemini-2.0-flash-exp**，点击**保存**
![image](https://github.com/user-attachments/assets/66617251-3854-4fe0-af99-1a3c7aeb1e37)
![image](https://github.com/user-attachments/assets/532a5ec1-bff8-495c-83d6-eaa35c7bb5bd)

3、现在就可以关掉所有代理，在无代理模式下自由使用 Gemini 了。





# 加密网络

来源: https://www.eff.org/encrypt-the-web

---

网络已基本从不安全的HTTP协议切换到更安全的HTTPS协议。所有网络服务器都使用这两种协议之一将网页从服务器传输到您的浏览器。HTTP存在严重问题，容易受到窃听和内容劫持的攻击。HTTPS修复了大部分这些问题。这就是为什么EFF和许多志同道合的支持者一直在推动网站默认采用HTTPS。截至2021年，约90%的网页访问使用HTTPS。这是加密和安全方面对每个人的巨大胜利。现在比以往任何时候都更容易默认实施HTTPS，我们正在提供工具来实现这一点。

多年来，网站所有者选择只为少数页面实施HTTPS，比如那些接受密码或信用卡号的页面。然而，在过去十年中，互联网安全社区已经意识到所有网页都需要保护。通过HTTP提供的页面容易受到窃听、内容注入和cookie窃取的攻击，这些攻击可用于接管您的在线账户。

内容注入是指有人向您与HTTP网页的通信中添加数据或代码。例如，GCHQ和NSA就是这样[接管了一家比利时ISP的计算机](https://www.wired.com/2014/03/quantum/)。内容注入也是中国通过大规模DDoS攻击（被称为["大炮"](https://citizenlab.org/2015/04/chinas-great-cannon/)）攻击GitHub的方式。内容注入在ISP中也变得越来越流行。[Verizon向其客户的每个请求注入跟踪头](https://www.eff.org/deeplinks/2014/11/verizon-x-uidh)。Comcast[将弹出窗口注入到不属于它们的网站](https://gizmodo.com/comcast-appears-to-be-injecting-browser-pop-ups-to-upse-1752633484)。所有这些攻击都可以通过HTTPS来阻止，只要它在足够多的网站上实施并设为默认。

## 作为个人你能做什么

你只能在支持HTTPS的网站上使用HTTPS，而且仍然有些网站不会默认将访客发送到HTTPS版本。你现在可以在Chrome、Firefox和Microsoft Edge中强制默认使用HTTPS。

**Firefox**

设置 > 隐私与安全 > 滚动到底部 > 启用仅HTTPS模式

**Chrome**

设置 > 隐私和安全 > 安全 > 滚动到底部 > 打开"始终使用安全连接"

此功能也在标志 chrome://flags/#https-only-mode-setting 下可用。

**Edge**

这在Edge中仍被视为"实验性功能"，但在Edge 92中可用。

- 访问 edge://flags/#edge-automatic-https 并启用自动HTTPS

点击出现的"重启"按钮以重启Microsoft Edge。

EFF的浏览器扩展程序[HTTPS Everywhere](https://www.eff.org/https-everywhere/)将于2022年底退役，因为现在大多数网站无需该扩展程序即可默认使用HTTPS。我们认为这是一个巨大的胜利。HTTPS Everywhere本来就是在更多网络自动加密之前的权宜之计。

## 作为网站所有者你能做什么

我们鼓励每个运营网站的人[提供HTTPS](https://www.eff.org/https-everywhere/deploying-https)并默认将访客重定向到HTTPS。在过去10年中，提供HTTPS[变得便宜多了](https://www.imperialviolet.org/2010/06/25/overclocking-ssl.html)。事实上，提供HTTPS使网站能够实施现代HTTP/2标准，这可以相对于HTTP大大加快网页浏览速度。这也为更新的协议做好了准备，这些协议承诺带来更多性能提升，如[HTTP/3-QUIC](https://www.fastly.com/quic-http-3)。

提供HTTPS需要从证书颁发机构获取证书。过去获取证书既昂贵又复杂，但自2016年以来，一个新的证书颁发机构[Let's Encrypt](https://letsencrypt.org/)使用API向公众提供免费证书，使自动化变得简单。Let's Encrypt是EFF、Mozilla和许多其他赞助商的联合项目。

如果您完全通过网页界面管理您的网站，最简单的方法是让您的托管提供商将Let's Encrypt支持集成为一个可以打开的设置。[许多托管提供商](https://community.letsencrypt.org/t/web-hosting-who-support-lets-encrypt/6920)已经支持Let's Encrypt，而且越来越多的提供商不断添加支持。

如果您在托管提供商那里有shell访问权限，您可以使用[Certbot](https://certbot.eff.org/)，这是EFF开发的工具。Certbot可以为您从Let's Encrypt获取免费证书。它还可以自动配置您的Apache或Nginx服务器以正确使用该证书。

## 作为托管提供商你能做什么

我们鼓励所有托管提供商和CDN默认为其客户提供HTTPS，与其HTTP服务相比不收取额外费用。许多提供商已经这样做了，如Cloudflare、OVH、WordPress.com和SquareSpace。[Let's Encrypt集成指南](https://letsencrypt.org/docs/integration-guide/)提供了有关如何最好地默认实施HTTPS的更多详细信息。我们继续庆祝免费、自动的HTTPS成为网络托管的行业标准。

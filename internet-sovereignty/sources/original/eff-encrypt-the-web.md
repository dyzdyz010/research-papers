# Encrypting the Web

Source: https://www.eff.org/encrypt-the-web

---

The web has largely switched from non-secure HTTP to the more secure HTTPS protocol. All web servers use one of these two protocols to get web pages from the server to your browser. HTTP has serious problems that make it vulnerable to eavesdropping and content hijacking. HTTPS fixes most of these problems. That's why EFF, and many like-minded supporters, have been pushing for web sites to adopt HTTPS by default. As of 2021, about 90% of all web page visits use HTTPS. This is a big win for encryption and security for everyone. It's easier than ever to implement HTTPS by default, and we're providing the tools to do it.

For many years, web site owners chose to only implement HTTPS for a small number of pages, like those that accepted passwords or credit card numbers. However, over the last ten years, the Internet security community has come to realize that all web pages need protection. Pages served over HTTP are vulnerable to eavesdropping, content injection, and cookie stealing, which can be used to take over your online accounts.

Content injection is when someone adds data or code to your communications with an HTTP web page. For example, it's how GCHQ and NSA [took over a Belgian ISP's computers](https://www.wired.com/2014/03/quantum/). Content injection is also how China took down GitHub with a massive DDoS attack, [dubbed "The Great Cannon"](https://citizenlab.org/2015/04/chinas-great-cannon/). Content injection is also becoming popular with ISPs. [Verizon injected tracking headers](https://www.eff.org/deeplinks/2014/11/verizon-x-uidh) into every request made by their customers. And Comcast [injects pop-ups into sites where they don't belong](https://gizmodo.com/comcast-appears-to-be-injecting-browser-pop-ups-to-upse-1752633484). All of these attacks can be stopped by HTTPS, provided it is implemented and made default on enough sites.

## What you can do as an individual

You can only use HTTPS on websites that support it, and there are still sites that don't send visitors to the HTTPS version by default. You can now force HTTPS by default in Chrome, Firefox, and Microsoft Edge.

**Firefox**

Settings > Privacy & Security > Scroll to Bottom > Enable HTTPS-Only Mode

**Chrome**

Settings > Privacy and security > Security > Scroll to bottom > Toggle "Always use secure connections"

This feature is also under the flag chrome://flags/#https-only-mode-setting.

**Edge**

This is still considered an "experimental feature" in Edge, but is available in Edge 92.

- Visit edge://flags/#edge-automatic-https and enable Automatic HTTPS

Hit the "Restart" button that appears to restart Microsoft Edge.

EFF's browser extension, [HTTPS Everywhere](https://www.eff.org/https-everywhere/) will retire at the end of 2022, because default HTTPS is now available on most websites without the extension. We see this as a great victory. HTTPS Everywhere was always meant to be a stopgap solution until more of the web was automatically encrypted.

## What you can do as a web site owner

We're encouraging everyone who runs a web site to [offer HTTPS](https://www.eff.org/https-everywhere/deploying-https) and redirect visitors to HTTPS by default. Offering HTTPS has [gotten a lot cheaper](https://www.imperialviolet.org/2010/06/25/overclocking-ssl.html) in the last 10 years. In fact, offering HTTPS makes it possible for sites to implement the modern HTTP/2 standard, which can dramatically speed up web browsing relative to HTTP. This also future proofs for even more up to date protocols that promise even more performance gains like [HTTP/3-QUIC](https://www.fastly.com/quic-http-3).

Offering HTTPS requires getting a certificate from a certificate authority. It used to be expensive and complicated to get a certificate, but since 2016, a new certificate authority, [Let's Encrypt](https://letsencrypt.org/), offers free certificates to the public using an API that enables easy automation. Let's Encrypt is a joint project of EFF, Mozilla, and many other sponsors.

If you manage your web site entirely through a web interface, the easiest approach is for your hosting provider to integrate Let's Encrypt support as a setting you can turn on. [Many hosting providers](https://community.letsencrypt.org/t/web-hosting-who-support-lets-encrypt/6920) already support Let's Encrypt, and many more add support all the time.

If you have shell access on your hosting provider, you can use [Certbot](https://certbot.eff.org/), a tool developed by EFF. Certbot can get you a free certificate from Let's Encrypt. It can also automatically configure your Apache or Nginx server to correctly use that certificate.

## What you can do as a hosting provider

We encourage all hosting providers and CDNs to offer HTTPS by default for their customers, at no additional cost versus their HTTP services. Many already have, like Cloudflare, OVH, WordPress.com, and SquareSpace. The [Let's Encrypt integration guide](https://letsencrypt.org/docs/integration-guide/) has additional details on how to best implement HTTPS by default. We continue to celebrate free, automatic HTTPS being the industry standard for web hosting.

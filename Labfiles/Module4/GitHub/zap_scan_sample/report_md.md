# ZAP Scanning Report

ZAP by [Checkmarx](https://checkmarx.com/).


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 9 |
| Informational | 9 |




## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- |
| CORS Misconfiguration | Medium | 12 |
| Content Security Policy (CSP) Header Not Set | Medium | 3 |
| Cross-Domain Misconfiguration | Medium | 10 |
| Hidden File Found | Medium | 4 |
| Proxy Disclosure | Medium | 13 |
| Cookie with SameSite Attribute None | Low | 2 |
| Cookie without SameSite Attribute | Low | 2 |
| Cross-Domain JavaScript Source File Inclusion | Low | 6 |
| Dangerous JS Functions | Low | 2 |
| Deprecated Feature Policy Header Set | Low | 7 |
| HTTPS Content Available via HTTP | Low | 7 |
| Insufficient Site Isolation Against Spectre Vulnerability | Low | 6 |
| Strict-Transport-Security Header Not Set | Low | 11 |
| Timestamp Disclosure - Unix | Low | 1 |
| Cookie Slack Detector | Informational | 12 |
| Information Disclosure - Suspicious Comments | Informational | 2 |
| Modern Web Application | Informational | 3 |
| Non-Storable Content | Informational | 1 |
| Re-examine Cache-control Directives | Informational | 4 |
| Session Management Response Identified | Informational | 2 |
| Storable and Cacheable Content | Informational | 1 |
| Storable but Non-Cacheable Content | Informational | 9 |
| User Agent Fuzzer | Informational | 24 |




## Alert Detail



### [ CORS Misconfiguration ](https://www.zaproxy.org/docs/alerts/40040/)



##### Medium (High)

### Description

This CORS misconfiguration could allow an attacker to perform AJAX queries to the vulnerable website from a malicious page loaded by the victim's user agent.
In order to perform authenticated AJAX queries, the server must specify the header "Access-Control-Allow-Credentials: true" and the "Access-Control-Allow-Origin" header must be set to null or the malicious page's domain. Even if this misconfiguration doesn't allow authenticated AJAX requests, unauthenticated sensitive content can still be accessed (e.g intranet websites).
A malicious page can belong to a malicious website but also a trusted website with flaws (e.g XSS, support of HTTP without TLS allowing code injection through MITM, etc).

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: ``
  * Attack: `origin: https://p3CpmdoA.com`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: ``
  * Attack: `origin: https://p3CpmdoA.com`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets
  * Method: `GET`
  * Parameter: ``
  * Attack: `origin: https://p3CpmdoA.com`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public
  * Method: `GET`
  * Parameter: ``
  * Attack: `origin: https://p3CpmdoA.com`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public/favicon_js.ico
  * Method: `GET`
  * Parameter: ``
  * Attack: `origin: https://p3CpmdoA.com`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: `origin: https://p3CpmdoA.com`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/polyfills.js
  * Method: `GET`
  * Parameter: ``
  * Attack: `origin: https://p3CpmdoA.com`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/robots.txt
  * Method: `GET`
  * Parameter: ``
  * Attack: `origin: https://p3CpmdoA.com`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/runtime.js
  * Method: `GET`
  * Parameter: ``
  * Attack: `origin: https://p3CpmdoA.com`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: `origin: https://p3CpmdoA.com`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: `origin: https://p3CpmdoA.com`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/vendor.js
  * Method: `GET`
  * Parameter: ``
  * Attack: `origin: https://p3CpmdoA.com`
  * Evidence: ``
  * Other Info: ``

Instances: 12

### Solution

If a web resource contains sensitive information, the origin should be properly specified in the Access-Control-Allow-Origin header. Only trusted websites needing this resource should be specified in this header, with the most secured protocol supported.

### Reference


* [ https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS ](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
* [ https://portswigger.net/web-security/cors ](https://portswigger.net/web-security/cors)


#### CWE Id: [ 942 ](https://cwe.mitre.org/data/definitions/942.html)


#### WASC Id: 14

#### Source ID: 1

### [ Content Security Policy (CSP) Header Not Set ](https://www.zaproxy.org/docs/alerts/10038/)



##### Medium (High)

### Description

Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``

Instances: 3

### Solution

Ensure that your web server, application server, load balancer, etc. is configured to set the Content-Security-Policy header.

### Reference


* [ https://developer.mozilla.org/en-US/docs/Web/Security/CSP/Introducing_Content_Security_Policy ](https://developer.mozilla.org/en-US/docs/Web/Security/CSP/Introducing_Content_Security_Policy)
* [ https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html ](https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html)
* [ https://www.w3.org/TR/CSP/ ](https://www.w3.org/TR/CSP/)
* [ https://w3c.github.io/webappsec-csp/ ](https://w3c.github.io/webappsec-csp/)
* [ https://web.dev/articles/csp ](https://web.dev/articles/csp)
* [ https://caniuse.com/#feat=contentsecuritypolicy ](https://caniuse.com/#feat=contentsecuritypolicy)
* [ https://content-security-policy.com/ ](https://content-security-policy.com/)


#### CWE Id: [ 693 ](https://cwe.mitre.org/data/definitions/693.html)


#### WASC Id: 15

#### Source ID: 3

### [ Cross-Domain Misconfiguration ](https://www.zaproxy.org/docs/alerts/10098/)



##### Medium (Medium)

### Description

Web browser data loading may be possible, due to a Cross Origin Resource Sharing (CORS) misconfiguration on the web server.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public/favicon_js.ico
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/polyfills.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/robots.txt
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/runtime.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/vendor.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`

Instances: 10

### Solution

Ensure that sensitive data is not available in an unauthenticated manner (using IP address white-listing, for instance).
Configure the "Access-Control-Allow-Origin" HTTP header to a more restrictive set of domains, or remove all CORS headers entirely, to allow the web browser to enforce the Same Origin Policy (SOP) in a more restrictive manner.

### Reference


* [ https://vulncat.fortify.com/en/detail?id=desc.config.dotnet.html5_overly_permissive_cors_policy ](https://vulncat.fortify.com/en/detail?id=desc.config.dotnet.html5_overly_permissive_cors_policy)


#### CWE Id: [ 264 ](https://cwe.mitre.org/data/definitions/264.html)


#### WASC Id: 14

#### Source ID: 3

### [ Hidden File Found ](https://www.zaproxy.org/docs/alerts/40035/)



##### Medium (Low)

### Description

A sensitive file was identified as accessible or available. This may leak administrative, configuration, or credential information which can be leveraged by a malicious individual to further attack the system or conduct social engineering efforts.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/._darcs
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 200 OK`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/.bzr
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 200 OK`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/.hg
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 200 OK`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/BitKeeper
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 200 OK`
  * Other Info: ``

Instances: 4

### Solution

Consider whether or not the component is actually required in production, if it isn't then disable it. If it is then ensure access to it requires appropriate authentication and authorization, or limit exposure to internal systems or specific source IPs, etc.

### Reference


* [ https://blog.hboeck.de/archives/892-Introducing-Snallygaster-a-Tool-to-Scan-for-Secrets-on-Web-Servers.html ](https://blog.hboeck.de/archives/892-Introducing-Snallygaster-a-Tool-to-Scan-for-Secrets-on-Web-Servers.html)


#### CWE Id: [ 538 ](https://cwe.mitre.org/data/definitions/538.html)


#### WASC Id: 13

#### Source ID: 1

### [ Proxy Disclosure ](https://www.zaproxy.org/docs/alerts/40025/)



##### Medium (Medium)

### Description

1 proxy server(s) were detected or fingerprinted. This information helps a potential attacker to determine
- A list of targets for an attack against the application.
 - Potential vulnerabilities on the proxy servers that service the application.
 - The presence or absence of any proxy-based components that might cause attacks against the application to be detected, prevented, or mitigated.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: ``
  * Attack: `TRACE, OPTIONS methods with 'Max-Forwards' header. TRACK method.`
  * Evidence: ``
  * Other Info: `Using the TRACE, OPTIONS, and TRACK methods, the following proxy servers have been identified between ZAP and the application/web server:
- Unknown
The following web/application server has been identified:
- Unknown
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: ``
  * Attack: `TRACE, OPTIONS methods with 'Max-Forwards' header. TRACK method.`
  * Evidence: ``
  * Other Info: `Using the TRACE, OPTIONS, and TRACK methods, the following proxy servers have been identified between ZAP and the application/web server:
- Unknown
The following web/application server has been identified:
- Unknown
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets
  * Method: `GET`
  * Parameter: ``
  * Attack: `TRACE, OPTIONS methods with 'Max-Forwards' header. TRACK method.`
  * Evidence: ``
  * Other Info: `Using the TRACE, OPTIONS, and TRACK methods, the following proxy servers have been identified between ZAP and the application/web server:
- Unknown
The following web/application server has been identified:
- Unknown
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public
  * Method: `GET`
  * Parameter: ``
  * Attack: `TRACE, OPTIONS methods with 'Max-Forwards' header. TRACK method.`
  * Evidence: ``
  * Other Info: `Using the TRACE, OPTIONS, and TRACK methods, the following proxy servers have been identified between ZAP and the application/web server:
- Unknown
The following web/application server has been identified:
- Unknown
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public/favicon_js.ico
  * Method: `GET`
  * Parameter: ``
  * Attack: `TRACE, OPTIONS methods with 'Max-Forwards' header. TRACK method.`
  * Evidence: ``
  * Other Info: `Using the TRACE, OPTIONS, and TRACK methods, the following proxy servers have been identified between ZAP and the application/web server:
- Unknown
The following web/application server has been identified:
- Unknown
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/ftp
  * Method: `GET`
  * Parameter: ``
  * Attack: `TRACE, OPTIONS methods with 'Max-Forwards' header. TRACK method.`
  * Evidence: ``
  * Other Info: `Using the TRACE, OPTIONS, and TRACK methods, the following proxy servers have been identified between ZAP and the application/web server:
- Unknown
The following web/application server has been identified:
- Unknown
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: `TRACE, OPTIONS methods with 'Max-Forwards' header. TRACK method.`
  * Evidence: ``
  * Other Info: `Using the TRACE, OPTIONS, and TRACK methods, the following proxy servers have been identified between ZAP and the application/web server:
- Unknown
The following web/application server has been identified:
- Unknown
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/polyfills.js
  * Method: `GET`
  * Parameter: ``
  * Attack: `TRACE, OPTIONS methods with 'Max-Forwards' header. TRACK method.`
  * Evidence: ``
  * Other Info: `Using the TRACE, OPTIONS, and TRACK methods, the following proxy servers have been identified between ZAP and the application/web server:
- Unknown
The following web/application server has been identified:
- Unknown
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/robots.txt
  * Method: `GET`
  * Parameter: ``
  * Attack: `TRACE, OPTIONS methods with 'Max-Forwards' header. TRACK method.`
  * Evidence: ``
  * Other Info: `Using the TRACE, OPTIONS, and TRACK methods, the following proxy servers have been identified between ZAP and the application/web server:
- Unknown
The following web/application server has been identified:
- Unknown
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/runtime.js
  * Method: `GET`
  * Parameter: ``
  * Attack: `TRACE, OPTIONS methods with 'Max-Forwards' header. TRACK method.`
  * Evidence: ``
  * Other Info: `Using the TRACE, OPTIONS, and TRACK methods, the following proxy servers have been identified between ZAP and the application/web server:
- Unknown
The following web/application server has been identified:
- Unknown
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: `TRACE, OPTIONS methods with 'Max-Forwards' header. TRACK method.`
  * Evidence: ``
  * Other Info: `Using the TRACE, OPTIONS, and TRACK methods, the following proxy servers have been identified between ZAP and the application/web server:
- Unknown
The following web/application server has been identified:
- Unknown
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: `TRACE, OPTIONS methods with 'Max-Forwards' header. TRACK method.`
  * Evidence: ``
  * Other Info: `Using the TRACE, OPTIONS, and TRACK methods, the following proxy servers have been identified between ZAP and the application/web server:
- Unknown
The following web/application server has been identified:
- Unknown
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/vendor.js
  * Method: `GET`
  * Parameter: ``
  * Attack: `TRACE, OPTIONS methods with 'Max-Forwards' header. TRACK method.`
  * Evidence: ``
  * Other Info: `Using the TRACE, OPTIONS, and TRACK methods, the following proxy servers have been identified between ZAP and the application/web server:
- Unknown
The following web/application server has been identified:
- Unknown
`

Instances: 13

### Solution

Disable the 'TRACE' method on the proxy servers, as well as the origin web/application server.
Disable the 'OPTIONS' method on the proxy servers, as well as the origin web/application server, if it is not required for other purposes, such as 'CORS' (Cross Origin Resource Sharing).
Configure the web and application servers with custom error pages, to prevent 'fingerprintable' product-specific error pages being leaked to the user in the event of HTTP errors, such as 'TRACK' requests for non-existent pages.
Configure all proxies, application servers, and web servers to prevent disclosure of the technology and version information in the 'Server' and 'X-Powered-By' HTTP response headers.


### Reference


* [ https://tools.ietf.org/html/rfc7231#section-5.1.2 ](https://tools.ietf.org/html/rfc7231#section-5.1.2)


#### CWE Id: [ 204 ](https://cwe.mitre.org/data/definitions/204.html)


#### WASC Id: 45

#### Source ID: 1

### [ Cookie with SameSite Attribute None ](https://www.zaproxy.org/docs/alerts/10054/)



##### Low (Medium)

### Description

A cookie has been set with its SameSite attribute set to "none", which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: `ARRAffinitySameSite`
  * Attack: ``
  * Evidence: `Set-Cookie: ARRAffinitySameSite`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: `ARRAffinitySameSite`
  * Attack: ``
  * Evidence: `Set-Cookie: ARRAffinitySameSite`
  * Other Info: ``

Instances: 2

### Solution

Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.

### Reference


* [ https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site ](https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site)


#### CWE Id: [ 1275 ](https://cwe.mitre.org/data/definitions/1275.html)


#### WASC Id: 13

#### Source ID: 3

### [ Cookie without SameSite Attribute ](https://www.zaproxy.org/docs/alerts/10054/)



##### Low (Medium)

### Description

A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: `ARRAffinity`
  * Attack: ``
  * Evidence: `Set-Cookie: ARRAffinity`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: `ARRAffinity`
  * Attack: ``
  * Evidence: `Set-Cookie: ARRAffinity`
  * Other Info: ``

Instances: 2

### Solution

Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.

### Reference


* [ https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site ](https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site)


#### CWE Id: [ 1275 ](https://cwe.mitre.org/data/definitions/1275.html)


#### WASC Id: 13

#### Source ID: 3

### [ Cross-Domain JavaScript Source File Inclusion ](https://www.zaproxy.org/docs/alerts/10017/)



##### Low (Medium)

### Description

The page includes one or more script files from a third-party domain.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/sitemap.xml
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/sitemap.xml
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>`
  * Other Info: ``

Instances: 6

### Solution

Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.

### Reference



#### CWE Id: [ 829 ](https://cwe.mitre.org/data/definitions/829.html)


#### WASC Id: 15

#### Source ID: 3

### [ Dangerous JS Functions ](https://www.zaproxy.org/docs/alerts/10110/)



##### Low (Low)

### Description

A dangerous JS function seems to be in use that would leave the site vulnerable.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `bypassSecurityTrustHtml(`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/vendor.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `bypassSecurityTrustHtml(`
  * Other Info: ``

Instances: 2

### Solution

See the references for security advice on the use of these functions.

### Reference


* [ https://angular.io/guide/security ](https://angular.io/guide/security)


#### CWE Id: [ 749 ](https://cwe.mitre.org/data/definitions/749.html)


#### Source ID: 3

### [ Deprecated Feature Policy Header Set ](https://www.zaproxy.org/docs/alerts/10063/)



##### Low (Medium)

### Description

The header has now been renamed to Permissions-Policy.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/polyfills.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/runtime.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/vendor.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``

Instances: 7

### Solution

Ensure that your web server, application server, load balancer, etc. is configured to set the Permissions-Policy header instead of the Feature-Policy header.

### Reference


* [ https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Permissions-Policy ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Permissions-Policy)
* [ https://scotthelme.co.uk/goodbye-feature-policy-and-hello-permissions-policy/ ](https://scotthelme.co.uk/goodbye-feature-policy-and-hello-permissions-policy/)


#### CWE Id: [ 16 ](https://cwe.mitre.org/data/definitions/16.html)


#### WASC Id: 15

#### Source ID: 3

### [ HTTPS Content Available via HTTP ](https://www.zaproxy.org/docs/alerts/10047/)



##### Low (Medium)

### Description

Content which was initially accessed via HTTPS (i.e.: using SSL/TLS encryption) is also accessible via HTTP (without encryption).

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public/favicon_js.ico
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `http://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public/favicon_js.ico`
  * Other Info: `ZAP attempted to connect via: http://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public/favicon_js.ico`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `http://juiceshop-dev-devsecops-47526599.azurewebsites.net/main.js`
  * Other Info: `ZAP attempted to connect via: http://juiceshop-dev-devsecops-47526599.azurewebsites.net/main.js`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/polyfills.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `http://juiceshop-dev-devsecops-47526599.azurewebsites.net/polyfills.js`
  * Other Info: `ZAP attempted to connect via: http://juiceshop-dev-devsecops-47526599.azurewebsites.net/polyfills.js`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/robots.txt
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `http://juiceshop-dev-devsecops-47526599.azurewebsites.net/robots.txt`
  * Other Info: `ZAP attempted to connect via: http://juiceshop-dev-devsecops-47526599.azurewebsites.net/robots.txt`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/runtime.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `http://juiceshop-dev-devsecops-47526599.azurewebsites.net/runtime.js`
  * Other Info: `ZAP attempted to connect via: http://juiceshop-dev-devsecops-47526599.azurewebsites.net/runtime.js`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `http://juiceshop-dev-devsecops-47526599.azurewebsites.net/styles.css`
  * Other Info: `ZAP attempted to connect via: http://juiceshop-dev-devsecops-47526599.azurewebsites.net/styles.css`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/vendor.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `http://juiceshop-dev-devsecops-47526599.azurewebsites.net/vendor.js`
  * Other Info: `ZAP attempted to connect via: http://juiceshop-dev-devsecops-47526599.azurewebsites.net/vendor.js`

Instances: 7

### Solution

Ensure that your web server, application server, load balancer, etc. is configured to only serve such content via HTTPS. Consider implementing HTTP Strict Transport Security.

### Reference


* [ https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html ](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html)
* [ https://owasp.org/www-community/Security_Headers ](https://owasp.org/www-community/Security_Headers)
* [ https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security ](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
* [ https://caniuse.com/stricttransportsecurity ](https://caniuse.com/stricttransportsecurity)
* [ https://datatracker.ietf.org/doc/html/rfc6797 ](https://datatracker.ietf.org/doc/html/rfc6797)


#### CWE Id: [ 311 ](https://cwe.mitre.org/data/definitions/311.html)


#### WASC Id: 4

#### Source ID: 1

### [ Insufficient Site Isolation Against Spectre Vulnerability ](https://www.zaproxy.org/docs/alerts/90004/)



##### Low (Medium)

### Description

Cross-Origin-Embedder-Policy header is a response header that prevents a document from loading any cross-origin resources that don't explicitly grant the document permission (using CORP or CORS).

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: `Cross-Origin-Embedder-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: `Cross-Origin-Embedder-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/sitemap.xml
  * Method: `GET`
  * Parameter: `Cross-Origin-Embedder-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: `Cross-Origin-Opener-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: `Cross-Origin-Opener-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/sitemap.xml
  * Method: `GET`
  * Parameter: `Cross-Origin-Opener-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``

Instances: 6

### Solution

Ensure that the application/web server sets the Cross-Origin-Embedder-Policy header appropriately, and that it sets the Cross-Origin-Embedder-Policy header to 'require-corp' for documents.
If possible, ensure that the end user uses a standards-compliant and modern web browser that supports the Cross-Origin-Embedder-Policy header (https://caniuse.com/mdn-http_headers_cross-origin-embedder-policy).

### Reference


* [ https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cross-Origin-Embedder-Policy ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cross-Origin-Embedder-Policy)


#### CWE Id: [ 693 ](https://cwe.mitre.org/data/definitions/693.html)


#### WASC Id: 14

#### Source ID: 3

### [ Strict-Transport-Security Header Not Set ](https://www.zaproxy.org/docs/alerts/10035/)



##### Low (High)

### Description

HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public/favicon_js.ico
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/ftp
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/polyfills.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/robots.txt
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/runtime.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/vendor.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``

Instances: 11

### Solution

Ensure that your web server, application server, load balancer, etc. is configured to enforce Strict-Transport-Security.

### Reference


* [ https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html ](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html)
* [ https://owasp.org/www-community/Security_Headers ](https://owasp.org/www-community/Security_Headers)
* [ https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security ](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
* [ https://caniuse.com/stricttransportsecurity ](https://caniuse.com/stricttransportsecurity)
* [ https://datatracker.ietf.org/doc/html/rfc6797 ](https://datatracker.ietf.org/doc/html/rfc6797)


#### CWE Id: [ 319 ](https://cwe.mitre.org/data/definitions/319.html)


#### WASC Id: 15

#### Source ID: 3

### [ Timestamp Disclosure - Unix ](https://www.zaproxy.org/docs/alerts/10096/)



##### Low (Low)

### Description

A timestamp was disclosed by the application/web server. - Unix

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1734944650`
  * Other Info: `1734944650, which evaluates to: 2024-12-23 09:04:10.`

Instances: 1

### Solution

Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.

### Reference


* [ https://cwe.mitre.org/data/definitions/200.html ](https://cwe.mitre.org/data/definitions/200.html)


#### CWE Id: [ 200 ](https://cwe.mitre.org/data/definitions/200.html)


#### WASC Id: 13

#### Source ID: 3

### [ Cookie Slack Detector ](https://www.zaproxy.org/docs/alerts/90027/)



##### Informational (Low)

### Description

Repeated GET requests: drop a different cookie each time, followed by normal request with all cookies to stabilize session, compare responses against original baseline GET. This can reveal areas where cookie based authentication/attributes are not actually enforced.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `Cookies that don't have expected effects can reveal flaws in application logic. In the worst case, this can reveal where authentication via cookie token(s) is not actually enforced.
These cookies affected the response: 
These cookies did NOT affect the response: ARRAffinitySameSite,ARRAffinity
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `Cookies that don't have expected effects can reveal flaws in application logic. In the worst case, this can reveal where authentication via cookie token(s) is not actually enforced.
These cookies affected the response: 
These cookies did NOT affect the response: ARRAffinitySameSite,ARRAffinity
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `Cookies that don't have expected effects can reveal flaws in application logic. In the worst case, this can reveal where authentication via cookie token(s) is not actually enforced.
These cookies affected the response: 
These cookies did NOT affect the response: ARRAffinitySameSite,ARRAffinity
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `Cookies that don't have expected effects can reveal flaws in application logic. In the worst case, this can reveal where authentication via cookie token(s) is not actually enforced.
These cookies affected the response: 
These cookies did NOT affect the response: ARRAffinitySameSite,ARRAffinity
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public/favicon_js.ico
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `Cookies that don't have expected effects can reveal flaws in application logic. In the worst case, this can reveal where authentication via cookie token(s) is not actually enforced.
These cookies affected the response: 
These cookies did NOT affect the response: ARRAffinitySameSite,ARRAffinity
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `Cookies that don't have expected effects can reveal flaws in application logic. In the worst case, this can reveal where authentication via cookie token(s) is not actually enforced.
These cookies affected the response: 
These cookies did NOT affect the response: ARRAffinitySameSite,ARRAffinity
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/polyfills.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `Cookies that don't have expected effects can reveal flaws in application logic. In the worst case, this can reveal where authentication via cookie token(s) is not actually enforced.
These cookies affected the response: 
These cookies did NOT affect the response: ARRAffinitySameSite,ARRAffinity
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/robots.txt
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `Cookies that don't have expected effects can reveal flaws in application logic. In the worst case, this can reveal where authentication via cookie token(s) is not actually enforced.
These cookies affected the response: 
These cookies did NOT affect the response: ARRAffinitySameSite,ARRAffinity
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/runtime.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `Cookies that don't have expected effects can reveal flaws in application logic. In the worst case, this can reveal where authentication via cookie token(s) is not actually enforced.
These cookies affected the response: 
These cookies did NOT affect the response: ARRAffinitySameSite,ARRAffinity
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `Cookies that don't have expected effects can reveal flaws in application logic. In the worst case, this can reveal where authentication via cookie token(s) is not actually enforced.
These cookies affected the response: 
These cookies did NOT affect the response: ARRAffinitySameSite,ARRAffinity
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `Cookies that don't have expected effects can reveal flaws in application logic. In the worst case, this can reveal where authentication via cookie token(s) is not actually enforced.
These cookies affected the response: 
These cookies did NOT affect the response: ARRAffinitySameSite,ARRAffinity
`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/vendor.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `Cookies that don't have expected effects can reveal flaws in application logic. In the worst case, this can reveal where authentication via cookie token(s) is not actually enforced.
These cookies affected the response: 
These cookies did NOT affect the response: ARRAffinitySameSite,ARRAffinity
`

Instances: 12

### Solution



### Reference


* [ https://cwe.mitre.org/data/definitions/205.html ](https://cwe.mitre.org/data/definitions/205.html)


#### CWE Id: [ 205 ](https://cwe.mitre.org/data/definitions/205.html)


#### WASC Id: 45

#### Source ID: 1

### [ Information Disclosure - Suspicious Comments ](https://www.zaproxy.org/docs/alerts/10027/)



##### Informational (Low)

### Description

The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `query`
  * Other Info: `The following pattern was used: \bQUERY\b and was detected in the element starting with: ""use strict";(self.webpackChunkfrontend=self.webpackChunkfrontend||[]).push([[179],{4550:(tt,K,c)=>{c.d(K,{e:()=>s});var S=c(234", see evidence field for the suspicious comment/snippet.`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/vendor.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `query`
  * Other Info: `The following pattern was used: \bQUERY\b and was detected in the element starting with: "(self.webpackChunkfrontend=self.webpackChunkfrontend||[]).push([[736],{9187:(Mt,te,u)=>{"use strict";u.d(te,{Xy:()=>J,ne:()=>Be,", see evidence field for the suspicious comment/snippet.`

Instances: 2

### Solution

Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.

### Reference



#### CWE Id: [ 200 ](https://cwe.mitre.org/data/definitions/200.html)


#### WASC Id: 13

#### Source ID: 3

### [ Modern Web Application ](https://www.zaproxy.org/docs/alerts/10109/)



##### Informational (Medium)

### Description

The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`

Instances: 3

### Solution

This is an informational alert and so no changes are required.

### Reference




#### Source ID: 3

### [ Non-Storable Content ](https://www.zaproxy.org/docs/alerts/10049/)



##### Informational (Medium)

### Description

The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/ftp
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `400`
  * Other Info: ``

Instances: 1

### Solution

The content may be marked as storable by ensuring that the following conditions are satisfied:
The request method must be understood by the cache and defined as being cacheable ("GET", "HEAD", and "POST" are currently defined as cacheable)
The response status code must be understood by the cache (one of the 1XX, 2XX, 3XX, 4XX, or 5XX response classes are generally understood)
The "no-store" cache directive must not appear in the request or response header fields
For caching by "shared" caches such as "proxy" caches, the "private" response directive must not appear in the response
For caching by "shared" caches such as "proxy" caches, the "Authorization" header field must not appear in the request, unless the response explicitly allows it (using one of the "must-revalidate", "public", or "s-maxage" Cache-Control response directives)
In addition to the conditions above, at least one of the following conditions must also be satisfied by the response:
It must contain an "Expires" header field
It must contain a "max-age" response directive
For "shared" caches such as "proxy" caches, it must contain a "s-maxage" response directive
It must contain a "Cache Control Extension" that allows it to be cached
It must have a status code that is defined as cacheable by default (200, 203, 204, 206, 300, 301, 404, 405, 410, 414, 501).

### Reference


* [ https://datatracker.ietf.org/doc/html/rfc7234 ](https://datatracker.ietf.org/doc/html/rfc7234)
* [ https://datatracker.ietf.org/doc/html/rfc7231 ](https://datatracker.ietf.org/doc/html/rfc7231)
* [ https://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html ](https://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html)


#### CWE Id: [ 524 ](https://cwe.mitre.org/data/definitions/524.html)


#### WASC Id: 13

#### Source ID: 3

### [ Re-examine Cache-control Directives ](https://www.zaproxy.org/docs/alerts/10015/)



##### Informational (Low)

### Description

The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content. For static assets like css, js, or image files this might be intended, however, the resources should be reviewed to ensure that no sensitive content will be cached.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `public, max-age=0`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `public, max-age=0`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/robots.txt
  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/sitemap.xml
  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `public, max-age=0`
  * Other Info: ``

Instances: 4

### Solution

For secure content, ensure the cache-control HTTP header is set with "no-cache, no-store, must-revalidate". If an asset should be cached consider setting the directives "public, max-age, immutable".

### Reference


* [ https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching ](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching)
* [ https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control)
* [ https://grayduck.mn/2021/09/13/cache-control-recommendations/ ](https://grayduck.mn/2021/09/13/cache-control-recommendations/)


#### CWE Id: [ 525 ](https://cwe.mitre.org/data/definitions/525.html)


#### WASC Id: 13

#### Source ID: 3

### [ Session Management Response Identified ](https://www.zaproxy.org/docs/alerts/10112/)



##### Informational (Medium)

### Description

The given response has been identified as containing a session management token. The 'Other Info' field contains a set of header tokens that can be used in the Header Based Session Management Method. If the request is in a context which has a Session Management Method set to "Auto-Detect" then this rule will change the session management to use the tokens identified.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: `ARRAffinity`
  * Attack: ``
  * Evidence: `39b3b235d6db39cca0a58e9f5a0362f9d8995b97311942645a461a93e86f223d`
  * Other Info: `
cookie:ARRAffinity
cookie:ARRAffinitySameSite`
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: `ARRAffinity`
  * Attack: ``
  * Evidence: `39b3b235d6db39cca0a58e9f5a0362f9d8995b97311942645a461a93e86f223d`
  * Other Info: `
cookie:ARRAffinity
cookie:ARRAffinitySameSite`

Instances: 2

### Solution

This is an informational alert rather than a vulnerability and so there is nothing to fix.

### Reference


* [ https://www.zaproxy.org/docs/desktop/addons/authentication-helper/session-mgmt-id ](https://www.zaproxy.org/docs/desktop/addons/authentication-helper/session-mgmt-id)



#### Source ID: 3

### [ Storable and Cacheable Content ](https://www.zaproxy.org/docs/alerts/10049/)



##### Informational (Medium)

### Description

The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/robots.txt
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `In the absence of an explicitly specified caching lifetime directive in the response, a liberal lifetime heuristic of 1 year was assumed. This is permitted by rfc7234.`

Instances: 1

### Solution

Validate that the response does not contain sensitive, personal or user-specific information. If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:
Cache-Control: no-cache, no-store, must-revalidate, private
Pragma: no-cache
Expires: 0
This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.

### Reference


* [ https://datatracker.ietf.org/doc/html/rfc7234 ](https://datatracker.ietf.org/doc/html/rfc7234)
* [ https://datatracker.ietf.org/doc/html/rfc7231 ](https://datatracker.ietf.org/doc/html/rfc7231)
* [ https://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html ](https://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html)


#### CWE Id: [ 524 ](https://cwe.mitre.org/data/definitions/524.html)


#### WASC Id: 13

#### Source ID: 3

### [ Storable but Non-Cacheable Content ](https://www.zaproxy.org/docs/alerts/10049/)



##### Informational (Medium)

### Description

The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public/favicon_js.ico
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/polyfills.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/runtime.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/vendor.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``

Instances: 9

### Solution



### Reference


* [ https://datatracker.ietf.org/doc/html/rfc7234 ](https://datatracker.ietf.org/doc/html/rfc7234)
* [ https://datatracker.ietf.org/doc/html/rfc7231 ](https://datatracker.ietf.org/doc/html/rfc7231)
* [ https://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html ](https://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html)


#### CWE Id: [ 524 ](https://cwe.mitre.org/data/definitions/524.html)


#### WASC Id: 13

#### Source ID: 3

### [ User Agent Fuzzer ](https://www.zaproxy.org/docs/alerts/10104/)



##### Informational (Medium)

### Description

Check for differences in response based on fuzzed User Agent (eg. mobile sites, access as a Search Engine Crawler). Compares the response statuscode and the hashcode of the response body with the original response.

* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 6.0)`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (Windows NT 10.0; Trident/7.0; rv:11.0) like Gecko`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.3739.0 Safari/537.36 Edg/75.0.109.0`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.124 Safari/537.36`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:93.0) Gecko/20100101 Firefox/91.0`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (compatible; Yahoo! Slurp; http://help.yahoo.com/help/us/ysearch/slurp)`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (iPhone; CPU iPhone OS 8_0_2 like Mac OS X) AppleWebKit/600.1.4 (KHTML, like Gecko) Version/8.0 Mobile/12A366 Safari/600.1.4`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (iPhone; U; CPU iPhone OS 3_0 like Mac OS X; en-us) AppleWebKit/528.18 (KHTML, like Gecko) Version/4.0 Mobile/7A341 Safari/528.16`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `msnbot/1.1 (+http://search.msn.com/msnbot.htm)`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 6.0)`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (Windows NT 10.0; Trident/7.0; rv:11.0) like Gecko`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.3739.0 Safari/537.36 Edg/75.0.109.0`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.124 Safari/537.36`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:93.0) Gecko/20100101 Firefox/91.0`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (compatible; Yahoo! Slurp; http://help.yahoo.com/help/us/ysearch/slurp)`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (iPhone; CPU iPhone OS 8_0_2 like Mac OS X) AppleWebKit/600.1.4 (KHTML, like Gecko) Version/8.0 Mobile/12A366 Safari/600.1.4`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `Mozilla/5.0 (iPhone; U; CPU iPhone OS 3_0 like Mac OS X; en-us) AppleWebKit/528.18 (KHTML, like Gecko) Version/4.0 Mobile/7A341 Safari/528.16`
  * Evidence: ``
  * Other Info: ``
* URL: https://juiceshop-dev-devsecops-47526599.azurewebsites.net/assets/public
  * Method: `GET`
  * Parameter: `Header User-Agent`
  * Attack: `msnbot/1.1 (+http://search.msn.com/msnbot.htm)`
  * Evidence: ``
  * Other Info: ``

Instances: 24

### Solution



### Reference


* [ https://owasp.org/wstg ](https://owasp.org/wstg)



#### Source ID: 1



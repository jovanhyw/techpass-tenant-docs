# Overview of TechPass
## What is TechPass?
TechPass is the Identity & Access Management (IAM) and Single Sign-on (SSO) solution to access Singapore Government Technology Stack (SGTS) services. It provides a seamless login experience across SGTS services and allows centralised user access control.

## Key Concepts
TechPass is powered by [Microsoft Azure AD service](https://azure.microsoft.com/en-us/services/active-directory/). It is built on top of Azure AD to meet specific requirements of public service's development environment.

TechPass allows engineering teams working on SGTS products to develop and roll out their services quickly by simplifying the process needed to implement a new service.

TechPass utilises popular open standards such as [OAuth 2.0](https://oauth.net/2/) / [OpenID Connect(OIDC)](https://openid.net/connect/)
and [Security Assertion Markup Language(SAML) 2.0](http://docs.oasis-open.org/security/saml/Post2.0/sstc-saml-tech-overview-2.0.html), for authentication and authorisation.

?> While OAuth 2.0 SSO setup is available on the [TechPass portal](https://portal.techpass.suite.gov.sg), SAML SSO is available only by request. If you need SAML support for your product and services, submit a [service request](https://go.gov.sg/techpass-sr). We will get back to you within three business days.

Continue reading [here](/concepts/oauth2.md) for a deep dive into OAuth 2.0 setup.


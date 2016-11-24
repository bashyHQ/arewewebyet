---
layout: topic
title: "Authorization/Authentication"

intro: Authorization and Authentication are a big deal for web development. Take OAuth, the most widely used protocol of authentication between services on the web. Such an simple idea, but with so many varying implementations (twitter, facebook, whatever...) and tricky parts in the details – it's almost impossible to get right without a library. But authentication doesn't end there, how do people authorize against your server? How do you authenticate? These are crates helping you to address authentication problems.

level: 4
packages:
 - cookie
 - oauth2
 - oauth-client
 - inth-oauth2
 - yup-oauth2
 - frank_jwt
 - macaroons
 - otpauth
 - rust_accountkit

missing:
 - OAuth-Provider Support

news_tag: auth
---

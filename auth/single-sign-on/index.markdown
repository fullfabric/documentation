---
layout: default
---
    
### Single Sign-On (SSO) with SAML

Security Assertion Markup Language (SAML) is an XML standard that allows secure web domains to exchange user authentication and authorization data. Using SAML, an online service provider can contact a separate online identity provider to authenticate users who are trying to access secure content.

FULL FABRIC offers a SAML-based Single Sign-On (SSO) service that provides universities and other institutions with full control over the authorization of user accounts that can access FULL FABRIC. Using the SAML model, FULL FABRIC acts as the *service provider*, whereas clients act as the *identity provider*. Identity providers control usernames, passwords and other information used to identify and authenticate users.

The FULL FABRIC SSO service is based on the SAML v2.0 specifications. SAML v2.0 is supported by several widely known vendors.

#### SAML-based SSO with FULL FABRIC

The following process explains how a user logs into FULL FABRIC via a SAML-based SSO service.

##### Actors

* IdP - Identity Provider: The university, school or institution
* SP - Service Provider: FULL FABRIC
* User

##### Setup

The IdP must provide FULL FABRIC with:

* the URL for its SSO service
* the public key that FULL FABRIC should use to verify SAML responses

##### Use Case

[http://en.wikipedia.org/wiki/Security_Assertion_Markup_Language#The_SAML_Use_Case](http://en.wikipedia.org/wiki/Security_Assertion_Markup_Language#The_SAML_Use_Case)
---
layout: default
---
    
### Single Sign-On (SSO) with SAML

Security Assertion Markup Language (SAML) is an XML standard that allows secure web domains to exchange user authentication and authorization data. Using SAML, an online service provider can contact a separate online identity provider to authenticate users who are trying to access secure content.

FULL FABRIC offers a SAML-based Single Sign-On (SSO) service that provides universities and other institutions with full control over the authorization of user accounts that can access FULL FABRIC. Using the SAML model, FULL FABRIC acts as the *service provider*, whereas clients act as the *identity provider*. Identity providers control usernames, passwords and other information used to identify and authenticate users.

The FULL FABRIC SSO service is based on the SAML specifications. SAML v2.0 is supported by several widely known vendors.

#### SAML-based SSO with FULL FABRIC

The following process explains how a user logs into FULL FABRIC via a SAML-based SSO service.

##### Actors

* IdP - Identity Provider: The university, school or institution
* SP - Service Provider: FULL FABRIC
* User

##### Setup

The IdP must provide FULL FABRIC with:

* the URL for its SSO service
* the public key used to verify authenticity of SAML responses

The SP details are:

* SP initiation endpoint: `https://*.fullfabric.com/auth/saml`
* SP callback endpoint: `https://*.fullfabric.com/auth/saml/callback`

##### Flow

1. The User attempts to reach the SP
2. SP generates a SAML authentication request
3. SP sends a redirect to the User's browser for the IdP's SSO target endpoint. The redirect URL includes the encoded SAML authentication request that should be submitted to the IdP's SSO service
4. IdP decodes the SAML request and authenticates the User either by asking for valid login credentials or by checking for valid session cookies
5. IdP generates a SAML response that contains the authenticated User's details. In accordance with the SAML 2.0 specification, this response is digitally signed with the IdP's public and private DSA/RSA keys.
6. The partner encodes the SAML response and returns that information to the User's browser. The IdP provides a mechanism so that the browser can forward that information to the SP.
7. SP verifies the SAML response using the IdP's public key. If the response is successfully verified, the SP authenticates the User. If the User does not exist, it is created based on the details provided by the IdP.

##### Use Case

[http://en.wikipedia.org/wiki/SAML_2.0#Web_Browser_SSO_Profile](http://en.wikipedia.org/wiki/SAML_2.0#Web_Browser_SSO_Profile)

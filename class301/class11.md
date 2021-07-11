# What is OAuth?
OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential. In authentication parlance, this is known as secure, third-party, user-agent, delegated authorization.  

### OAuth examples
The simplest example of OAuth is when you go to log onto a website and it offers one or more opportunities to log on using another website’s/service’s logon. You then click on the button linked to the other website, the other website authenticates you, and the website you were originally connecting to logs you on itself afterward using permission gained from the second website.

# Authorization and Authentication flows
Authentication is the process of verifying who a user is, while authorization is the process of verifying what they have access to.  

Authorization code flow is used to obtain an access token to authorize API requests. Authorization code flow is the most flexible of the three supported authorization flows and is the recommended method of obtaining an access token for the API. This authorization flow is best suited to applications that have access to secure, private storage such as web applications deployed on a server.

The flow for authorization is:

- Create a URL to the OAuth authorization service
- Display the authorization user interface, prompting the user to sign in to Mendeley first if necessary
- Capture the authorization code from the user interface response
- Exchange the authorization code for an access token
- Extract the access token from the exchange response

Authentication is the process of verifying identity. A unique identifier is associated with a user which is the username or userid. Traditionally, we use a combination of username and password to authenticate a user. The authentication logic has to be maintained locally so we will term it local authentication. Apart from local authentication, we can use OpenID, Oauth & SAML can also be used as Auth providers.
The most common authentication technique is using a username and password.
The common flow while implementing it is:

- The user registers using an identifier like username/email/mobile;
- The application stores user credentials in the database;
- The application sends a verification email/message to validate the registration;
- Post successful registration, the user enters credentials for logging in;
- On successful authentication, the user is allowed access to specific resources;
- The user state is maintained via Sessions or JWT.  

[Source](https://blog.jscrambler.com/authentication-authorization-in-web-apps/)

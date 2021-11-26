# Session-based Authentication

## Caption

This note is an summary of multiple articles discussing on the general concept, implementation, pros and cons regarding to session-based authentication.

## Introduction

In every web applications, there are operations or resources that are meant for one or few specific users to proceed or have access to, thus that it is important to check if the user has the expected authorization to perform such action or access.

In order to check the authorization state of the user, first we will have to authenticate if the requests are made by the specific user. Since the [HTTP protocol is a stateless protocol][1], which means that some form of user identifier must be stored within each subsequent HTTP requests to indicate the user after the first request of user authentication.

## Reference

[1]: https://datatracker.ietf.org/doc/html/rfc2068
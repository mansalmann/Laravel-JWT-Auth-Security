# Laravel API Security with JSON Web Token for user authentication 

This repository contains a Laravel 10 with JWT authentication boilerplate
using the [tymon/jwt-auth](https://github.com/tymondesigns/jwt-auth) package.

Laravel JWT docs: https://jwt.io/introduction

## Features
- JWT authentication (login, register, password reset, email verification)
- Profile updating
- Password changing
- Product CRUD

## Installation

1. `cp .env.example .env`
2. `composer install`
3. `php artisan jwt:secret` (generate a secret key that will be used to sign your tokens)
4. `php artisan migrate:fresh --seed`

## Authentication

In order to authenticate, you have to log in using valid credentials. User data and an access token will be returned.
You can use this access token to do subsequent requests to the API.

The access token has a TTL of 1 hour until it expires. The access token should be refreshed within this time window to
avoid becoming unauthenticated.

The access token can be refreshed for two weeks. After that, the user has to log in again.

You can use many application to utilize API such as Postman or Insomnia, etc...

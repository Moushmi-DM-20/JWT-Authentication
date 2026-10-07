# 🔐 JWT Authentication — Complete Learning

A structured and practical guide to understanding **JWT (JSON Web Token) Authentication** from the fundamentals to advanced security concepts.

This repository is created as a learning reference to build a strong understanding of how modern API authentication works, how JWTs are structured and validated, and how authentication and authorization are implemented securely.

---

## 📌 About This Repository

JWT Authentication is widely used in modern web applications and APIs for securely identifying users and controlling access to protected resources.

This repository focuses on understanding the concepts **from the ground up**, rather than simply copying implementation code.

The goal is to understand:

* Why authentication is required
* How authentication differs from authorization
* How JWTs work internally
* How tokens are created and validated
* How claims represent user information
* How access and refresh tokens work
* How authorization is performed
* Common JWT security risks and best practices

---

## 🎯 Learning Objectives

By completing this guide, I aim to be able to:

* Understand authentication and authorization clearly
* Explain how JWT Authentication works end-to-end
* Understand the structure of a JWT
* Explain Header, Payload, and Signature
* Understand JWT claims
* Understand digital signatures and secret keys
* Implement token-based authentication
* Protect APIs using authentication and authorization
* Understand roles, claims, and policies
* Understand access tokens and refresh tokens
* Identify common JWT security vulnerabilities
* Understand how JWT relates to OAuth 2.0 and OpenID Connect
* Apply JWT security best practices in real-world applications

---

## 🧠 Topics Covered

### 1. Authentication Fundamentals

* Authentication vs Authorization
* Stateless vs Stateful Authentication
* Sessions
* Cookies
* HTTP Authentication
* Bearer Authentication
* HTTP 401 vs 403

### 2. Cryptography Fundamentals

* Encoding
* Encryption
* Hashing
* Password Hashing
* Salt
* Symmetric Cryptography
* Asymmetric Cryptography
* Digital Signatures
* Secret Keys

### 3. JWT Fundamentals

* What is JWT?
* Why JWT is used
* JWT structure
* Header
* Payload
* Signature
* Base64URL Encoding
* JWT Claims
* JWT Validation

### 4. JWT Claims

* Registered Claims
* `sub`
* `iss`
* `aud`
* `exp`
* `iat`
* `nbf`
* Custom Claims
* Role Claims

### 5. Authentication Flow

```text
User
 │
 │ Login Credentials
 ▼
Authentication Server
 │
 │ Validate Credentials
 ▼
Create JWT
 │
 │ Access Token
 ▼
Client
 │
 │ Authorization: Bearer <token>
 ▼
Protected API
 │
 │ Validate Token
 ▼
Authenticated User
```

### 6. Authorization

* Role-Based Authorization
* Claims-Based Authorization
* Policy-Based Authorization
* Permissions
* Resource-Based Authorization

### 7. Access & Refresh Tokens

* Access Tokens
* Refresh Tokens
* Token Expiration
* Refresh Token Flow
* Refresh Token Rotation
* Token Revocation
* Logout Strategies

### 8. JWT Security

* HTTPS
* Token Storage
* XSS
* CSRF
* CORS
* Token Theft
* Replay Attacks
* Secret Key Protection
* Key Rotation
* Token Expiration
* Sensitive Data in JWT Payload
* Algorithm Security

### 9. ASP.NET Core JWT Authentication

* Authentication Middleware
* `AddAuthentication()`
* `AddJwtBearer()`
* `UseAuthentication()`
* `UseAuthorization()`
* `[Authorize]`
* `[AllowAnonymous]`
* `HttpContext.User`
* Reading Claims
* Role Authorization
* Policy Authorization

### 10. Advanced Concepts

* OAuth 2.0
* OpenID Connect
* Access Token vs ID Token
* Authorization Code Flow
* PKCE
* Single Sign-On
* Identity Providers
* JWT vs Session Authentication
* JWT vs OAuth 2.0
* When JWT may not be the best choice

---

## 🗺️ Learning Roadmap

The concepts are studied progressively:

```text
Authentication Fundamentals
          ↓
Sessions & Cookies
          ↓
Cryptography Basics
          ↓
JWT Fundamentals
          ↓
JWT Structure
          ↓
Claims & Signatures
          ↓
Token Generation
          ↓
Token Validation
          ↓
Authorization
          ↓
Access & Refresh Tokens
          ↓
JWT Security
          ↓
OAuth 2.0 & OpenID Connect
          ↓
Production-Level Authentication
```

---

## 🔑 Important Concepts

### Authentication

> **Who are you?**

Authentication verifies the identity of a user or client.

### Authorization

> **What are you allowed to do?**

Authorization determines what an authenticated user is permitted to access.

### JWT

> **A compact, URL-safe token format used to represent claims between parties.**

JWT itself is not the entire authentication system. It is commonly used as part of token-based authentication and authorization systems.

---

## 🔍 JWT Structure

A JWT consists of three parts:

```text
Header.Payload.Signature
```

For example:

```text
xxxxx.yyyyy.zzzzz
```

### Header

Contains metadata such as the signing algorithm and token type.

### Payload

Contains claims about the subject or token.

### Signature

Used to verify that the token has not been altered and that it was signed by a trusted party.

> **Important:** JWT payloads are encoded, not encrypted by default. Sensitive information should not be placed inside them.

---

## 🛡️ Security Principles

This repository emphasizes secure implementation rather than simply making authentication work.

Important principles include:

* Always use HTTPS
* Never store plain-text passwords
* Protect signing keys
* Keep access tokens short-lived
* Validate token signature
* Validate issuer and audience when applicable
* Validate token expiration
* Avoid putting sensitive information in JWT payloads
* Understand secure browser token storage
* Implement appropriate refresh-token protection
* Apply authorization on the server
* Never trust user-provided identity or role information blindly

---

## 💡 What I Want to Achieve

This repository is part of my continuous learning journey toward becoming a stronger **Software Developer** with a solid understanding of backend development, API security, and modern authentication mechanisms.

The focus is not only on **how to implement JWT Authentication**, but also on understanding:

> **Why it works, how it works, where it can fail, and how to implement it securely.**

---

## 📚 Learning Approach

The concepts in this repository are studied progressively:

**Understand → Implement → Test → Analyze → Improve**

Each topic should be understood conceptually before moving to implementation.

---

## ⭐ Purpose

This repository is maintained as a personal **learning and reference resource** for JWT Authentication and modern API security.

If you are also learning JWT Authentication, feel free to explore the material and use it as a reference while building your own understanding.

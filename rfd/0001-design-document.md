---
authors: Ryan Russell (ryan@ryanrussell.ca)
state: draft
---

# RFD 1 - design document

# What

Proposes the design solution for [Teleport Frontend Application Developer](https://github.com/gravitational/careers/blob/main/challenges/frontend/challenge.md); Implement an application that allows a user to browse directory content on a remote server.

# Why

To allow Telport peers to evaluate skills in the following areas:

* Taking existing high-level requirements and translating them to a functional application
* Writing production level code that does not depend on gigabytes of npm packages
* Communicating with the team when working on the challenge
* Handling feedback

# Details

## Tools

* CSS: SCSS - material-ui
* Frontend: React, React Router - Typescript
* Backend: Node - Typescript
* Testing: Jest
* Version Control: [GitHub](https://github.com/ryan0319/teleport.git) 

## Functional Description

The software will include functionality to:

* View an interface for viewing and browsing directory content.
* Allow user searching on filename and sorting on filename, type, and size within the current directory.
* Serve web assets from a web server.
* For a containerized application using Docker.
* Allow for URL Navigation (URL to maintain state upon page change and refresh).

* Implement an API that allows authenticated users to browse a server directory 1-level deep at a time.
* Add support for session management for login/logout.
* Implement a login screen where an unauthenticated user is automatically redirected to (and then taken back to original URL).
* Include a strong TLS setup.

*Not Implemented*
* File preview is not implemented. Clicking on a file is a no-op.

## Milestones

1. Implement the directory browser with searching on filename and sorting on filename, type, and size. This includes the additional repository setup:
  - React app bootstrap
  - Linter
  - Key component tests

2. Implement the web server to server the assets within a docker container. This includes:
  - Node web server
  - Containerization with Docker
  - URL navigation

3. Implement authentication with features:
  - Move the JSON data to the web server and use as an API
  - Add session management for users
  - Allow user redirected to login and return to original state

4. Add security to the app and web server:
  - Use self-signed certs with assets served through HTTPS
  - Set headers to prevent / allow CORS
  - Set middle for HSTS and CSRF

** All milestone also include
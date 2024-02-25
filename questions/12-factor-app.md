# The Twelve-Factor App

+ [1. Codebase](#1-codebase)
+ [2. Dependencies](#2-dependencies)
+ [3. Config](#3-config)
+ [4. Backing Services](#4-backing-services)
+ [5. Build, Release, Run](#5-build-release-run)
+ [6. Processes](#6-processes)
+ [7. Port Binding](#7-port-binding)
+ [8. Concurrency](#8-concurrency)
+ [9. Disposability](#9-disposability)
+ [10. Dev/prod Parity](#10-devprod-parity)
+ [11. Logs](#11-logs)
+ [12. Admin Processes](#12-admin-processes)

## 1. Codebase
A twelve-factor app is always tracked in a version control system (e.g., Git) and has just one codebase for all environments, though there may be different deployments (staging, production, etc.).

## 2. Dependencies
All dependencies should be declared explicitly through a dependency declaration manifest. This ensures that no implicit dependencies are relied upon in the execution environment.

## 3. Config
Configuration that varies between deployments (such as resource handles, credentials, and per-deployment values) should be stored in the environment. This keeps the app's configuration separate from the code.

## 4. Backing Services
Treat all backing services (databases, messaging/queueing systems, caching systems, etc.) as attached resources, which means the codebase can make no distinction between local and third-party services.

## 5. Build, Release, Run
The codebase is transformed into a deployment through a build process. This creates a build, which is then combined with the deployment's current configuration to create a release. The release is then run in the execution environment.

## 6. Processes
The app executes as one or more stateless processes. Any data that needs to persist must be stored in a stateful backing service, like a database.

## 7. Port Binding
The app is completely self-contained and does not rely on runtime injection of a web server. It exports HTTP as a service by binding to a port and listening to requests.

## 8. Concurrency
The app can scale out horizontally as processes across multiple execution environments, leveraging the cloud's elasticity.

## 9. Disposability
Processes can be started or stopped at a moment's notice. This facilitates robustness and enables rapid elastic scaling, deployment, and development cycle.

## 10. Dev/prod Parity
Strive to keep development, staging, and production as similar as possible. This minimizes bugs introduced by environment discrepancies and facilitates continuous deployment.

## 11. Logs
Logs are treated as event streams. The app should not concern itself with routing or storage of output stream but should write its event stream, unbuffered, to `stdout`.

## 12. Admin Processes
Run administrative/management tasks as one-off processes in an environment identical to the application's regular long-running processes.

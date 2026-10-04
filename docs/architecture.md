# High-Level Architecture

Flutter clients authenticate with AWS Cognito and call the FastAPI backend over HTTPS. FastAPI owns business rules, authorization and orchestration. PostgreSQL stores structured application data. Redis provides caching, short-lived state and Pub/Sub support for live updates. A separate Python/FastAPI AI service isolates recommendation and computer-vision workloads. AWS storage is used for uploaded media where required.

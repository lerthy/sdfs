```mermaid
flowchart LR
  User --> CloudFront
  CloudFront -->|GET site| S3
  User -->|POST form| APIGateway
  APIGateway --> Lambda
  Lambda --> Secrets
  Lambda --> RDS
  Lambda --> CloudWatch
  CloudFront -. Invalidate .-> S3
```

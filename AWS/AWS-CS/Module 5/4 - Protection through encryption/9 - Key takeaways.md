- AWS supports both client-side and server-side encryption
    - CSE: you encrypt your data before sending it to AWS
    - SSE: AWS encrypts data on your behalf after receiving it 
- AWS provides 3 types of SSE:
    - SSE with customer-provided keys (SSE-C)
    - SSE with amazon S3 keys managed keys (SSE-S3)
    - SSE with AWS KMS keys (SSR-KMS)
- AWS KMS can create and control the keys used to encrypt your data
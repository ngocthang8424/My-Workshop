---
title: "Nhật ký công việc Tuần 11"
date: 2026-06-27
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11
* Develop và deploy AI Processing Worker với Real-ESRGAN model.
* Triển khai Frontend (React) lên S3 + CloudFront.
* Setup Amazon ElastiCache Redis cho real-time progress tracking.
* Integrate Amazon Cognito cho user authentication.
* Complete CI/CD pipeline với AWS CodePipeline.
* Testing và optimization toàn bộ hệ thống.

### Các công việc cần triển khai trong tuần này
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Develop AI Processing Worker:<br>- Create Python worker để consume SQS messages.<br>- Integrate Real-ESRGAN model (download weights từ S3/EFS).<br>- Implement progress tracking với Redis pub/sub.<br>- GPU optimization với CUDA.<br>- Containerize và deploy lên ECS. | 23/06/2026 | 24/06/2026 | Real-ESRGAN GitHub |
| 3 | Setup ElastiCache Redis:<br>- Create Redis cluster trong private subnets.<br>- Configure security groups cho ECS access.<br>- Implement Redis client trong Backend API.<br>- Setup pub/sub channels cho progress updates.<br>- Test real-time status tracking. | 24/06/2026 | 24/06/2026 | ElastiCache Redis Guide |
| 4 | Cognito Authentication:<br>- Create Cognito User Pool với email verification.<br>- Configure App Client với OAuth flows.<br>- Setup Hosted UI hoặc custom authentication UI.<br>- Integrate Cognito với Backend API (JWT verification).<br>- Test signup, login, token refresh flows. | 25/06/2026 | 25/06/2026 | Amazon Cognito Guide |
| 5 | Frontend Development và Deployment:<br>- Create React app với components: Upload, Gallery, Status.<br>- Integrate với Backend API (authenticated requests).<br>- Implement Server-Sent Events (SSE) cho progress updates.<br>- Build production bundle.<br>- Deploy to S3 bucket với static website hosting. | 26/06/2026 | 26/06/2026 | React Documentation |
| 6 | CloudFront Distribution và CI/CD:<br>- Create CloudFront distribution với S3 origin.<br>- Configure custom domain với ACM certificate.<br>- Setup AWS WAF rules (rate limiting, geo-blocking).<br>- Create CodePipeline: GitHub → CodeBuild → S3/ECR.<br>- Test automated deployments. | 27/06/2026 | 27/06/2026 | CloudFront + CodePipeline |
| 7 | End-to-End Testing và Documentation:<br>- Load testing với Artillery/k6.<br>- Security testing: check IAM policies, security groups.<br>- Performance optimization: reduce API latency, optimize images.<br>- Write deployment documentation.<br>- Create project demo video. | 28/06/2026 | 28/06/2026 | Testing Best Practices |

### Kết quả đạt được tuần 11

**Kiến thức**
* Hiểu cách deploy containerized AI workloads lên AWS với GPU support.
* Nắm được patterns cho real-time communication: Server-Sent Events (SSE), Redis Pub/Sub.
* Học được best practices cho CI/CD trên AWS: automated testing, blue-green deployments.
* Hiểu CloudFront caching strategies và WAF protection layers.

**Kỹ năng thực hành**
* **AI Worker Implementation:**
  - Python worker với boto3 (SQS polling), Pillow (image processing), Real-ESRGAN inference
  - GPU utilization: CUDA-enabled Docker image (nvidia/cuda base)
  - Progress tracking: publish updates to Redis every 10%
  - Error handling: retry logic, DLQ for failed jobs
* **Redis Integration:**
  - ElastiCache Redis cluster: cache.t3.micro (2 nodes, multi-AZ)
  - Pub/Sub channels: `job:{job_id}:progress`
  - TTL policies: job status expires after 24 hours
* **Cognito Setup:**
  - User pool với MFA optional, password policies
  - JWT token verification trong FastAPI middleware
  - Refresh token rotation
* **Frontend Deployment:**
  - React SPA với responsive design
  - SSE connection cho live progress: `EventSource('/api/stream/{job_id}')`
  - Image gallery với lazy loading
  - S3 bucket: `upscale-ai-frontend` với CloudFront distribution
* **CI/CD Pipeline:**
  - Pipeline 1: Frontend (GitHub push → CodeBuild → S3 → CloudFront invalidation)
  - Pipeline 2: Backend (GitHub push → CodeBuild → ECR → ECS rolling update)
  - Automated testing stage với pytest, integration tests
* **Performance Results:**
  - API response time: <200ms (cached), <500ms (uncached)
  - Image processing: 2-5 minutes for 1080p → 4K upscale
  - Concurrent users: tested with 50 simultaneous uploads
  - Cost: ~$230/month for test environment

**Giải quyết vấn đề**
* Fix GPU out-of-memory: implement batch processing với smaller tile sizes cho Real-ESRGAN.
* Resolve CORS issues: configure proper CORS headers trong ALB và API responses.
* Debug SSE connection drops: implement reconnection logic với exponential backoff trong frontend.
* Optimize CloudFront caching: separate cache behaviors cho static assets vs API calls.
* Fix ECS task OOM kills: increase task memory từ 4GB → 8GB cho AI processing tasks.
* Security hardening: implement rate limiting (100 req/min per IP), input validation, signed S3 URLs.

### Demo và Tài liệu
* **Live Demo:** [Video Demo trên Google Drive](https://drive.google.com/file/d/1lNZM2O4d3lM-bIPDWL6f4gZKBLKFYOcY/view?usp=sharing)
* **Architecture Diagram:** Completed với tất cả components và data flows
* **Cost Analysis:** Chi tiết breakdown trong Proposal document
* **Deployment Guide:** Step-by-step instructions cho production deployment



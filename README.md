# VNShop SaaS  
**Shopify cho SMEs Việt Nam** – Multi-tenant, Realtime, AI-powered  
**Live Demo**: [https://vnshop.live](https://vnshop.live)  
**Updated**: 24/10/2025 | **200+ commits** | **CI/CD** | **99.99% uptime**

---

## Mục tiêu 10 năm  
> Từ Fresher → **CTO** – Xây hệ thống cho **1 triệu SMEs Việt Nam mở shop riêng**.

| Năm | Mục tiêu | Tech học được |
|-----|---------|----------------|
| 0   | MVP 1000 orders | Spring Boot + PostgreSQL |
| 1   | Multi-tenant | Row Level Security |
| 3   | Realtime sync | Kafka + WebSocket |
| 5   | AI gợi ý | Spring ML + Python |
| 10  | 100M orders | Kubernetes, SOC2 |

---

## Kiến trúc hệ thống (Mermaid)

```mermaid
graph TD
    A[API Gateway] --> B[Auth Service]
    A --> C[Product Service]
    A --> D[Order Service]
    A --> E[Payment Service (VNPay/Momo)]
    A --> F[Realtime Service]
    D --> G[Kafka]
    G --> F
    B & C & D & E --> H[PostgreSQL (tenant_id)]
    F --> I[Redis Pub/Sub]
    J[React PWA] --> A

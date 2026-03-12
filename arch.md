# High-Level System Architecture

      Users / Systems
            │
            ▼
      API Gateway / Authentication
            │
            ▼
      Application Services Layer
            │
            ▼
      AI Processing Pipeline
            │
            ▼
      Data Storage Layer
            │
            ▼
      Integration Layer

# Detailed System Architecture

                ┌────────────────────────────┐
                │        Client Layer         │
                │-----------------------------│
                │ Web UI (React)              │
                │ Admin Portal                │
                │ Mobile App (Optional)       │
                │ External Systems (API)      │
                └──────────────┬──────────────┘
                               │
                               ▼
                 ┌──────────────────────────┐
                 │        API Gateway        │
                 │---------------------------│
                 │ Authentication (OAuth2)   │
                 │ Rate Limiting             │
                 │ Request Routing           │
                 └─────────────┬─────────────┘
                               │
                               ▼
         ┌─────────────────────────────────────────┐
         │           Application Services           │
         │------------------------------------------│
         │ Document Service                         │
         │ Workflow Service                         │
         │ User Management Service                  │
         │ Notification Service                     │
         │ Audit Service                            │
         └──────────────┬───────────────────────────┘
                        │
                        ▼
        ┌─────────────────────────────────────────┐
        │        AI Processing Pipeline            │
        │------------------------------------------│
        │ Document Ingestion Service               │
        │ OCR Engine                               │
        │ NLP / LLM Extraction                     │
        │ Classification Model                     │
        │ Validation Engine                        │
        │ Confidence Scoring                       │
        └──────────────┬───────────────────────────┘
                       │
                       ▼
         ┌──────────────────────────────────────┐
         │           Data Layer                  │
         │---------------------------------------│
         │ PostgreSQL (metadata)                 │
         │ Object Storage (documents)            │
         │ Vector Database (embeddings)          │
         │ Redis Cache                           │
         └──────────────┬────────────────────────┘
                        │
                        ▼
           ┌───────────────────────────────────┐
           │       Integration Layer           │
           │-----------------------------------│
           │ ERP Systems                       │
           │ CRM Systems                       │
           │ Email / Messaging                 │
           │ Webhooks                          │
           └───────────────────────────────────┘

# AI Pipeline

            1 Document Upload
                    │
                    ▼
            2 Pre-processing
               - format detection
               - image cleanup
                    │
                    ▼
            3 OCR
               - text extraction
                    │
                    ▼
            4 Classification
               - invoice
               - contract
               - KYC
                    │
                    ▼
            5 Data Extraction
               - AI model extracts fields
                    │
                    ▼
            6 Validation
               - rules engine
               - confidence score
                    │
                    ▼
            7 Human Review (optional)
                    │
                    ▼
            8 Export Structured Data

# Microservices

services/

  api-gateway
  document-service
  workflow-service
  auth-service
  ai-extraction-service
  ocr-service
  classification-service
  validation-service
  notification-service
  integration-service

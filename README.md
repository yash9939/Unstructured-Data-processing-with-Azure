# Azure AI Document Processing System

> A cloud-native solution built on Microsoft Azure that allows users to upload images and documents through a web interface, automatically extracts structured text from them using AI services, and returns results as JSON.

## 🚀 Project Overview

This repository contains a complete solution for an **AI-powered document extraction system** built using Azure technologies. Users upload documents via a web UI; the backend stores them in Azure Blob Storage and triggers an automated processing pipeline that uses **Azure Data Factory** and **Azure AI Document Intelligence** to perform text extraction. The final structured output is stored as JSON and can be downloaded or viewed by users.

---

## 🧠 Key Features

- **Interactive Web UI** for drag & drop document upload
- **Direct Azure Blob Storage Integration**
- **Automated AI Pipeline** using Azure Data Factory
- **Document Intelligence** for OCR and structured extraction
- **Result Polling & JSON Output**
- **Scalable, Serverless Architecture**

---

## 🧩 Architecture

flowchart TD
    subgraph Client
        UI[Web Frontend<br/>(Upload Page)]
    end

    subgraph Backend
        API[Backend Server<br/>(Express/Node.js)]
    end

    subgraph Azure
        RawBlob[(Azure Blob: raw-docs)]
        ADF[Azure Data Factory<br/>(Orchestration)]
        DocIntel[Azure AI Document Intelligence]
        ProcBlob[(Azure Blob: processed)]
    end

    UI -->|Upload file| API
    API -->|Upload to storage| RawBlob
    RawBlob -->|Trigger| ADF
    ADF -->|Invoke AI| DocIntel
    DocIntel -->|JSON output| ProcBlob
    ProcBlob -->|Poll result| UI

    style UI fill:#f9f,stroke:#333,stroke-width:1px
    style API fill:#bbf,stroke:#333,stroke-width:1px
    style RawBlob fill:#fbf,stroke:#333,stroke-width:1px
    style ADF fill:#bfb,stroke:#333,stroke-width:1px
    style DocIntel fill:#ffd,border:2px solid #333
    style ProcBlob fill:#fbf,stroke:#333,stroke-width:1px
    
---

## 🛠️ Tech Stack

| Component | Purpose |
|-----------|---------|
| Azure Blob Storage | Stores raw and processed files |
| Azure Data Factory | Orchestrates document analysis pipeline |
| Azure AI Document Intelligence | Performs OCR and generates structured output |
| Node.js / Express | Backend API to handle uploads |
| Vanilla HTML/CSS/JS | Frontend UI |
| SAS Tokens | Secure upload & access to blobs |

---

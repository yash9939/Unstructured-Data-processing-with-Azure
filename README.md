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
Web Frontend (HTML/JS)
↓
API Backend (Node.js/Express)
↓
Azure Blob Storage (raw-docs container)
↓ (trigger)
Azure Data Factory
↓ (invoke AI)
Azure AI Document Intelligence
↓
Azure Blob Storage (processed container)
↓
Frontend poll → display JSON


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

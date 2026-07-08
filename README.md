# 📊 Marketing Tracker v2.64 — ApotekKu

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Web App Status](https://img.shields.io/badge/Deployment-Static%20Page-success.svg)](#-deployment--hosting)
[![Tech Stack](https://img.shields.io/badge/Stack-Vanilla%20JS%20%7C%20Firebase%20%7C%20Chart.js-orange.svg)](#%EF%B8%8F-architecture--tech-stack)

A robust, ultra-fast, zero-backend single-page static application engineered explicitly for the **ApotekKu Marketing Team**. This repository contains a fully decentralized work management dashboard featuring live Kanban pipelines, recurring campaign engines, time tracking workflows, secure team chat, and client-side S3 object storage utilities.

Because it operates entirely on the client side, it features zero hosting operational costs, scales infinitely, and offers full offline resilience.

## 🚀 Key Features

* **🔒 Secure Client-Side Gate:** Entry protected via secure SHA-256 password validation with flexible, persistent login states (`Remember Me`).
* **📋 Multi-Column Kanban Board:** Group tasks dynamically by custom assignees, targets, or strict execution pipelines (`TODO`, `PROSES`, `DONE`).
* **⏰ Smart Rollover Logic:** Overdue or uncompleted campaign boards automatically shift over to the current calendar date to enforce operational continuity.
* **📣 Integrated Team Communication:** Distributed chat streams with customized auditory feedback (WhatsApp-style notification cues) and fast `@member` mentions.
* **📦 Native S3 Storage Client:** Built-in AWS Signature V4 processor allowing direct binary file uploads, access streams, and 7-day presigned generation directly to an external object storage cluster (e.g., private MinIO) without intermediate proxy endpoints.
* **📈 Rich Interactive Analytics:** Modern metrics breakdown (Workloads, Task Tracks, and Team output ratios) powered by `Chart.js`.
* **📥 Comprehensive Data Portability:** On-demand export pipelines targeting human-readable Markdown templates (`.md`), standard spreadsheets (`.csv`), or multi-sheet workbooks (`.xlsx`) generated using `SheetJS`.


## 🛠️ Architecture & Tech Stack

This project deliberately avoids complex continuous integration servers, compilation dependencies, or backend runtimes. 

* **UI/UX Layer:** Structured HTML5 semantic blocks, custom layouts, and a dedicated ApotekKu corporate design layout styled completely through reactive CSS Variables.
* **Database Infrastructure:** **Firebase JS SDK (v10.13.0)** utilizing Firestore multi-tab offline synchronization (IndexedDB layer) for robust real-time state persistence.
* **Data Vis & Processing:** **Chart.js (v4.4.0)** for processing team output charts and **SheetJS (`xlsx.full.min.js`)** for handling local client spreadsheet processing.
* **Security:** Native **Web Crypto API** used browser-side for rendering deterministic hashes and cryptographically signed AWS S3 network calls.

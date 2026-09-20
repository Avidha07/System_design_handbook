# Chapter 1: Scale From Zero to Millions of Users

## Single Server Setup

In a **Single Server Setup**, everything runs on **one server**:

* Web App
* Database
* Cache
* Business Logic

This is the simplest architecture and a good starting point before scaling.

---

## Architecture

![Single Server Setup](./single-server-setup.png)

---

## Request Flow (4 Steps)

1. **User enters a domain** (`api.mysite.com`).
2. **DNS returns the server IP** (e.g., `15.125.23.214`).
3. **Browser/Mobile sends an HTTP request** to the web server.
4. **Server returns HTML or JSON**.

### Quick Flow

`User → DNS → IP Address → Web Server → HTML/JSON Response`

---

## DNS

* Converts **Domain Name → IP Address**.
* Usually provided by **third-party services** (not hosted on our server).

Example:

`api.mysite.com → 15.125.23.214`

---

## Traffic Sources

### 1. Web Application

Uses:

* **Server-side:** Java, Python, etc.
* **Client-side:** HTML + JavaScript

Responsible for:

* Business logic
* Storage
* UI rendering

### 2. Mobile Application

* Communicates using **HTTP**.
* Receives responses in **JSON** format.

Example:

`Mobile App → HTTP → Web Server → JSON`

---

## HTML vs JSON

| HTML                 | JSON                          |
| -------------------- | ----------------------------- |
| Used by browsers     | Used by APIs                  |
| Renders web pages    | Transfers data                |
| Presentation-focused | Lightweight and easy to parse |

---

## Interview Revision (30 Seconds)

* Everything runs on **one server**.
* **DNS** converts the domain into an **IP address**.
* Browser/Mobile sends an **HTTP request**.
* Server returns **HTML (web)** or **JSON (mobile/API)**.
* Traffic comes from **Web Applications** and **Mobile Applications**.

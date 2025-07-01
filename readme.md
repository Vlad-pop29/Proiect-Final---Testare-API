
# Gomag Clients API Testing – Postman Project

Acest repository conține colecția Postman și fișierele necesare pentru testarea endpointurilor API ale modulului **Clienți** din platforma Gomag.

## 📁 Conținut

- `Clienti.postman_collection.json` – colecția Postman cu testele 
- `TestAPIMethod.postman_environment.json` – variabile pentru testare (token, URL etc.)
- `README.md` – acest fișier, cu instrucțiuni de rulare

---
---------------------------------------------------
## ℹ️ Descriere generală

Acest proiect este dedicat **testării automate a API-ului public Gomag**, cu focus pe secțiunea **Clients (Clienți)**.

**Scopul principal al testării:**  
Validarea funcționalităților API oferite de Gomag pentru gestionarea clienților unui magazin online: creare, modificare, autentificare, recuperare parolă, ștergere etc.

---

## 🏢 Ce este Gomag?

**Gomag** este o platformă SaaS românească care ajută comercianții să își construiască și administreze magazine online. Printre funcționalitățile principale se numără:

- Gestionarea produselor, comenzilor și clienților
- Automatizări și integrări
- Acces programatic la date prin **API REST Public**

---

## 🎯 Obiectivul proiectului de testare

- Validarea conformității API-ului cu cerințele business-ului
- Identificarea defectelor (ex: răspunsuri eronate, lipsă validări, coduri de status incorecte)
- Asigurarea unui minim de calitate pentru endpoint-urile de gestionare clienți

---

## 🧑‍💻 Tehnologii folosite

- **Postman** – pentru definirea și rularea testelor manuale și automate
- **Newman** – pentru rularea testelor Postman din linie de comandă (CLI)
- **JavaScript** – pentru validări și assertions în cadrul testelor Postman
- **Collection Runner** – pentru execuții batch
- **CMD / Terminal** – pentru rularea testelor în mod automatizat

## 📌 Scenarii de testare acoperite

| Scenariu | Tip testare | Tehnică folosită |
|---|---|---|
| Citire listă completă clienți | Funcțională pozitivă | Equivalence Partitioning |
| Verificare listă clienți (nu e goală) | Funcțională pozitivă | Equivalence Partitioning |
| Citire client cu email specificat | Funcțională pozitivă | Equivalence Partitioning |
| Citire client inexistent | Funcțională negativă | Equivalence Partitioning |
| Adăugare client cu date valide | Funcțională pozitivă | Equivalence Partitioning |
| Adăugare client cu email existent | Funcțională negativă | Equivalence Partitioning |
| Modificare client fără email | Funcțională negativă | Validarea câmpurilor obligatorii |
| Login client fără parolă | Funcțională negativă | Boundary Value Analysis |
| Recuperare parolă pentru client inexistent | Funcțională negativă | Equivalence Partitioning |
| Ștergere client valid | Funcțională pozitivă | Equivalence Partitioning |

---

## 🛠️ Detalii despre fiecare test executat

Fiecare test include:

- ✅ Metoda HTTP folosită
- ✅ Endpoint-ul
- ✅ Tipul testării
- ✅ Tehnica de testare aplicată
- ✅ Codul de status HTTP așteptat
- ✅ Capturi de ecran cu request/response în Postman
- ✅ Capturi cu testele JavaScript și rezultatele execuției

  ------------------
-------------------------------

## 🛠️ Instalare Postman

Pentru a putea testa și executa metodele API incluse în acest proiect, este necesar să instalezi aplicația **Postman** – un instrument popular pentru testarea API.

---

### 🔽 Pasul 1: Accesează site-ul oficial

👉 [https://www.postman.com/downloads/](https://www.postman.com/downloads/)

---

### 💻 Pasul 2: Alege sistemul tău de operare

- Windows (x64 / x86)
- macOS
- Linux (Ubuntu, Fedora etc.)

---

### 📦 Pasul 3: Descarcă și instalează aplicația

1. Click pe butonul **Download** corespunzător platformei tale.
2. Rulează fișierul executabil și urmează instrucțiunile de instalare.

---

### 👤 Pasul 4: Creează un cont (opțional)

Este recomandat să creezi un cont Postman pentru a beneficia de:
- sincronizarea automată a colecțiilor,
- acces la Postman Web și spații de lucru.


---

### ✅ Pasul 5: Verificare și import colecții

După instalare:

1. Deschide aplicația Postman.
2. Mergi la butonul **Import**.
3. Selectează fișierele `Clienti.postman_collection.json` și `TestAPIMethod.postman_environment.json` din acest proiect.
4. Rulează colecția prin `Collection Runner` sau `Newman`.

---

----------------

## 🛠️ Instalare Newman (Postman CLI)

Newman este un tool de linie de comandă care permite rularea colecțiilor Postman direct din terminal. Este util pentru testare automată, CI/CD și integrare în pipeline-uri DevOps.

---

### 🔽 Pasul 1: Instalare Newman global

Instalează Newman folosind npm: 
npm install -g newman

---

### 🔎 Pasul 2: Verificare instalare

După instalare, verifică versiunea:
newman -v

---

### ▶️ Pasul 3: Rularea unei colecții Postman

Pentru a rula colecția din proiect:
Comanda introdusa in cmd window: newman run Clienti.postman_collection.json -e TestAPIMethod.postman_environment.json






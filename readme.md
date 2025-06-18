
# Gomag Clients API Testing – Postman Project

Acest repository conține colecția Postman și fișierele necesare pentru testarea endpointurilor API ale modulului **Clienți** din platforma Gomag.

## 📁 Conținut

- `Clienti.postman_collection.json` – colecția Postman cu testele 
- `TestAPIMethod.postman_environment.json` – variabile pentru testare (token, URL etc.)
- `README.md` – acest fișier, cu instrucțiuni de rulare

---
---------------------------------------------------

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






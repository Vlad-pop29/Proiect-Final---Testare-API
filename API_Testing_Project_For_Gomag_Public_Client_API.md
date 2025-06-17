# API Testing Project for Gomag – Clients Module

## ℹ️ Despre Gomag și API-ul public

**Gomag** este o platformă românească de tip SaaS (Software as a Service) pentru **crearea și gestionarea magazinelor online**. Comercianții care își construiesc un magazin pe Gomag pot gestiona produse, comenzi, clienți, integrări și automatizări direct dintr-un panou de administrare.

### 🔗 API-ul Public Gomag

Gomag oferă un **API REST public** ce permite integratorilor și dezvoltatorilor să interacționeze programatic cu datele din magazin: produse, comenzi, stocuri, clienți etc.

Este util pentru:

- Conectarea unui ERP, CRM sau alt sistem extern
- Automatizarea proceselor (ex: import clienți, actualizare date)
- Export și analiză date clienți
- Conectarea cu tool-uri personalizate (raportări, dashboard-uri)

### 📦 Ce face secțiunea de API pentru Clienți?

Modulul **Clients API** din Gomag oferă acces la operațiuni esențiale legate de utilizatorii finali (clienți ai magazinului):

- **Autentificarea clienților** (login cu email/parolă)
- **Listarea tuturor clienților înregistrați**
- **Vizualizarea detaliilor unui client anume**
- **Crearea unui client nou**
- **Editarea unui client existent**
- **Ștergerea unui client**
- **Modificare parola clienti**
- **Recuperare parola clienti**

---

## 🎯 Scop

Testarea funcționalităților API-ului public Gomag pentru gestionarea clienților (`clients`): autentificare, listare, creare, actualizare și ștergere.

---

## 🧰 Tehnologii & Tooling

- Postman
- Newman
- GitHub 

---


<h2>Tests performed</h2>

<ol>
<li>**Nume Request 1**</li>

HTTP method for request: **Inserati aici metoda HTTP a requestului**<br>
Request description: **Inserati o scurta descriere a requestului, conform documentatiei de API**<br>
Test types / techniques used: **Inserati tipurile si tehnicile de testare folosite pentru acest request**<br>
Response status code: **Inserati aici status code-ul pe care l-ati obtinut in urma executiei requestului**<br>

Below you can find a picture of the API request from Postman:<br>

**Inserati aici o poza cu requestul din postman in care sa se observe request method, endpoint, request body si response body**<br>

JavaScript Tests:

**Inserati aici o poza cu testele in java script pe care le-ati definit impreuna cu rezultatele executiei acestora**<br>


<li>**Nume Request 2**</li>

HTTP method for request: **Inserati aici metoda HTTP a requestului**<br>
Request description: **Inserati o scurta descriere a requestului, conform documentatiei de API**<br>
Test types / techniques used: **Inserati tipurile si tehnicile de testare folosite pentru acest request**<br>
Response status code: **Inserati aici status code-ul pe care l-ati obtinut in urma executiei requestului**<br>

Below you can find a picture of the API request from Postman:<br>

**Inserati aici o poza cu requestul din postman in care sa se observe request method, endpoint, request body si response body**<br>

JavaScript Tests:

**Inserati aici o poza cu testele in java script pe care le-ati definit impreuna cu rezultatele executiei acestora**<br>

.............

<li>**Nume Request n**</li>

HTTP method for request: **Inserati aici metoda HTTP a requestului**<br>
Request description: **Inserati o scurta descriere a requestului, conform documentatiei de API**<br>
Test types / techniques used: **Inserati tipurile si tehnicile de testare folosite pentru acest request**<br>
Response status code: **Inserati aici status code-ul pe care l-ati obtinut in urma executiei requestului**<br>

Below you can find a picture of the API request from Postman:<br>

**Inserati aici o poza cu requestul din postman in care sa se observe request method, endpoint, request body si response body**<br>

JavaScript Tests:

**Inserati aici o poza cu testele in java script pe care le-ati definit impreuna cu rezultatele executiei acestora**<br>

</ol>

<h2>Rapoartele de executie pentru metodele API testate </h2>

# 📋 Raport Execuție – Gomag Clients API

- 📅 Data: 2025-06-17
- 🔄 Colecție rulată: `Clienti.postman_collection.json`
- 🌐 Environment: `TestAPIMethod.postman_environment.json`
- ⚙️ Tool: Postman Collection Runner

---

## ✅ Rezumat Execuție

| Metrică           | Valoare     |
|-------------------|-------------|
| Total requests    | 28           |
| Total teste  | 115          |
| Tests passed      | 104          |
| Tests failed      | 11          |
| Durată totală     | 330 ms     |
| Data execuției    | 2025-06-17  |

![image](https://github.com/user-attachments/assets/d8f1a0a9-f01a-414c-820c-952c156c1794)
<br>

Colectia Clienti a fost rulata si prin Newmann direct din terminalul cmd,utilizand comanda:
<br> newman run Clienti.postman_collection.json -e TestAPIMethod.postman_environment.json


si rezultatele se pot vizualiza in cele ce urmeaza <br>

![image](https://github.com/user-attachments/assets/f7386784-ebdc-45dd-9e39-a83fa0e94a28)
<br>

<h2>Bug-uri descoperite</h2>

Au fost decoperite urmatoarele bug-uri pe parcursul testarii API-ului prin Postman<br>
[Raportarea de bug.pdf](https://github.com/user-attachments/files/20781407/Raportarea.de.bug.pdf)




<h2>Concluzii</h2>


## 🔢 Rezumat Execuție

- **Total teste executate:** `115`
- **Rezultate:** ✔️ `104 Passed` | ❌ `11 Failed`
- **Rată de succes:** `~90%`

---

## 📊 Observații Generale

- Grad relativ bun de conformitate cu cerințele inițiale (90% teste trecute).
- Erorile identificate afectează funcționalități critice și ridică riscuri importante în cazul lansării aplicației în producție, în forma actuală.

---

## ⚠️ Risc Major Identificat

❌ **Sistemul permite adăugarea mai multor clienți cu aceeași adresă de email.**  
- Poate duce la:
  - Inconsistență în baze de date
  - Probleme de autentificare
  - Confuzie în managementul clienților

> **Recomandare:** Validare unică a câmpului `email` la creare client (HTTP 409 Conflict).

---

## 📉 Probleme de Implementare Identificate

### 🔄 Statusuri HTTP incorecte

- Se returnează `200 OK` chiar și în cazuri de eroare (ex: duplicate, validări eșuate).
- Exemple de coduri așteptate:
  - `400 Bad Request` – pentru date lipsă/invalide
  - `401 Unauthorized` – acces fără token valid
  - `409 Conflict` – în caz de duplicate
  - `422 Unprocessable Entity` – validări complexe

> **Recomandare:** Alinierea răspunsurilor la standardele REST.

---

## 📄 Documentație API – Probleme Identificate

- Lipsesc detalii despre:
  - Formatele exacte de request/response
  - Codurile de eroare posibile
  - Reguli de validare pentru fiecare câmp
- Unele endpointuri documentate nu corespund implementării reale.

> **Recomandare:** Revizuirea documentației și menținerea ei sincronizată cu comportamentul real al API-ului.

---



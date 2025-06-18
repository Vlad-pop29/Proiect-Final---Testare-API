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
<li>Citire lista de clienti completa</li>

Metoda HTTP pentru request: GET http://te-echipam.gomag.ro/api/v1/customer/read/json<br>
Descriere request: Această metodă API permite citirea informațiilor despre toti clientii înregistrati în magazinul de pe platforma Gomag.<br>
Tipuri si tehnici de testare folosite: Tipurile de testare: testare functionala, pozitiva si de integrare. Tehnicile de testare: Echivalence Partitioning<br>
Response status code: 200 OK<br>

Mai jos este ilustrata o imagine cu API request-ul din Postman:<br>

In imagine se observa metoda de request, endpoint-ul, request body este gol si response body**<br>
![image](https://github.com/user-attachments/assets/bce9ecd1-194f-4054-937f-ec9de0927090)

JavaScript Tests:

Imagine cu testele in java script pe care le-am definit, impreuna cu rezultatele executiei acestora<br>
![image](https://github.com/user-attachments/assets/90c207d7-f999-4ba6-922f-9a03a1d6517b)


<li>Verificam daca lista de clienti nu este goala</li>

Metoda HTTP pentru request: GET:  http://te-echipam.gomag.ro/api/v1/customer/read/json<br>
Descriere request: Această metodă API permite citirea informațiilor despre toti clientii înregistrati în magazinul de pe platforma Gomag.<br>
Tipuri si tehnici de testare folosite: 	Testare funcțională pozitivă. Tehnicile de testare: Echivalence Partitioning (Partitionarea echivalenței (clasă validă de date))<br>
Response status code: 200 OK<br>

Mai jos este ilustrata o imagine cu API request-ul din Postman:<br>

In imagine se observa metoda de request, endpoint-ul, request body este gol si response body**<br>
![image](https://github.com/user-attachments/assets/fbf98009-e0b6-40fa-9aa7-1711b4a356b8)


JavaScript Tests:

Imagine cu testele in java script pe care le-am definit, impreuna cu rezultatele executiei acestora<br>
![image](https://github.com/user-attachments/assets/bc0a82b4-4ff0-477b-801b-0b3cea62ee70)


<li>Citire informatii client cu email specificat</li>

Metoda HTTP pentru request: GET:  http://te-echipam.gomag.ro/api/v1/customer/read/json<br>
Descriere request: Această metodă API permite citirea informațiilor despre anumiti clientii înregistrati în magazinul de pe platforma Gomag, cand se specifica anumiti parametrii<br>
Tipuri si tehnici de testare folosite: 	Testare funcțională pozitivă. Tehnicile de testare: Echivalence Partitioning (Partitionarea echivalenței (clasă validă de date))<br>
Response status code: 200 OK<br>

Mai jos este ilustrata o imagine cu API request-ul din Postman:<br>

In imagine se observa metoda de request, endpoint-ul, request body este gol si response body**<br>
![image](https://github.com/user-attachments/assets/5881ebad-db73-4f98-b959-7922ebfd68e5)

JavaScript Tests:

Imagine cu testele in java script pe care le-am definit, impreuna cu rezultatele executiei acestora<br>
![image](https://github.com/user-attachments/assets/1bc2381f-c5af-4a44-9c7b-2318fc6a65c2)

<li>Citire esuata de informatii pentru un client inexistent</li>

Metoda HTTP pentru request: GET:  http://te-echipam.gomag.ro/api/v1/customer/read/json<br>
Descriere request: Această metodă API permite citirea informațiilor despre toti clientii înregistrati în magazinul de pe platforma Gomag.<br>
Tipuri si tehnici de testare folosite: 	Testare funcțională negativa. Tehnicile de testare: Echivalence Partitioning (Partitionarea echivalenței (clasă invalidă de date))<br>
Response status code: 200 OK<br>

Mai jos este ilustrata o imagine cu API request-ul din Postman:<br>

In imagine se observa metoda de request, endpoint-ul, request body este gol si response body**<br>
![image](https://github.com/user-attachments/assets/e29472ce-2cda-4064-9070-71bfb706f5b7)


JavaScript Tests:

Imagine cu testele in java script pe care le-am definit, impreuna cu rezultatele executiei acestora<br>
![image](https://github.com/user-attachments/assets/4fbe4eeb-77ce-4a46-9849-2a583017b65a)

<li>Adauga un client nou in magazin cu date valide</li>

Metoda HTTP pentru request: POST:  http://te-echipam.gomag.ro/api/v1/customer/add/json<br>
Descriere request: Această metodă permite adăugarea unui client nou în magazinul de pe platforma Gomag, prin trimiterea unui request de tip POST care conține datele clientului în body.<br>
Tipuri si tehnici de testare folosite: 	Testare funcțională pozitivă. Tehnicile de testare: Echivalence Partitioning (Partitionarea echivalenței (clasă validă de date))<br>
Response status code: 200 OK<br>

Mai jos este ilustrata o imagine cu API request-ul din Postman:<br>

In imagine se observa metoda de request, endpoint-ul, request body este gol si response body<br>
![image](https://github.com/user-attachments/assets/a32137aa-4eef-4b78-b85d-e05dd7fb5904)

JavaScript Tests:

Imagine cu testele in java script pe care le-am definit, impreuna cu rezultatele executiei acestora<br>
![image](https://github.com/user-attachments/assets/09e85bf2-6a79-43c1-b392-659fa9888e5f)

<li>Adauga un client nou in magazin cu adrea de email existenta</li>

Metoda HTTP pentru request: POST:  http://te-echipam.gomag.ro/api/v1/customer/add/json<br>
Descriere request: Această metodă permite adăugarea unui client nou în magazinul de pe platforma Gomag, prin trimiterea unui request de tip POST care conține datele clientului în body. Adresa de email specificata in body este asociata deja unui cont de client.<br>
Tipuri si tehnici de testare folosite: 	Testare funcțională negativa. Tehnicile de testare: Echivalence Partitioning (Partitionarea echivalenței (date invalide – email duplicat))<br>
Response status code: 200 OK  - BUG Raport<br>

Mai jos este ilustrata o imagine cu API request-ul din Postman:<br>

In imagine se observa metoda de request, endpoint-ul, request body este gol si response body<br>
![image](https://github.com/user-attachments/assets/a9b83465-2b8a-4634-8f1e-907850a13d24)


JavaScript Tests:

Imagine cu testele in java script pe care le-am definit, impreuna cu rezultatele executiei acestora<br>
![image](https://github.com/user-attachments/assets/0245330d-e5a2-4497-b1dd-1972dcd51d28)


<li>Modificare client fara adresa de email</li>

Metoda HTTP pentru request: POST:  http://te-echipam.gomag.ro/api/v1/customer/update/json<br>
Descriere request: Această metodă permite modificarea informațiilor unui client existent în magazinul de pe platforma Gomag, prin trimiterea unui request de tip POST cu datele actualizate ale clientului. In cazul test-case-ului analizat, in body-request nu e specificata adresa de email.<br>
Tipuri si tehnici de testare folosite: 	Testare funcțională negativa. Tehnicile de testare: Validarea câmpurilor obligatorii<br>
Response status code: 200 OK <br>

Mai jos este ilustrata o imagine cu API request-ul din Postman:<br>

In imagine se observa metoda de request, endpoint-ul, request body este gol si response body<br>
![image](https://github.com/user-attachments/assets/24fdf717-396f-4f9a-98c0-a224002de2ef)



JavaScript Tests:

Imagine cu testele in java script pe care le-am definit, impreuna cu rezultatele executiei acestora<br>
![image](https://github.com/user-attachments/assets/0a109968-35b7-4986-8e0f-e3a7744dc6bb)

<li>Logarea esuata a unui client fara parola specificata</li>

Metoda HTTP pentru request: POST:  http://te-echipam.gomag.ro/api/v1/customer/login/json<br>
Descriere request: Această metodă permite autentificarea clienților existenți în baza de date a magazinului Gomag, prin trimiterea unui request POST cu datele de autentificare. In cazul test-case-ului analizat, in body-request nu e specificata parola clientului.<br>
Tipuri si tehnici de testare folosite: 	Testare funcțională negativa. Tehnicile de testare: Validarea câmpurilor obligatorii / Boundary Value Analysis<br>
Response status code: 200 OK - Bug Raport <br>

Mai jos este ilustrata o imagine cu API request-ul din Postman:<br>

In imagine se observa metoda de request, endpoint-ul, request body este gol si response body<br>
![image](https://github.com/user-attachments/assets/4c921bb7-21f7-46ab-9cb6-bbf402a23b35)


JavaScript Tests:

Imagine cu testele in java script pe care le-am definit, impreuna cu rezultatele executiei acestora<br>
![image](https://github.com/user-attachments/assets/a48dab21-59db-4070-88d5-f974a48853b9)

<li>Recuperare Parola pentru un client inexistent</li>

Metoda HTTP pentru request: POST:  http://te-echipam.gomag.ro/api/v1/customer/passwordrecovery/json<br>
Descriere request: Această metodă permite recuperarea parolei unui client existent în baza de date a magazinului, prin trimiterea unui request POST care conține o adresă de email validă. In cazul test-case-ului analizat, in body-request nu e specificata o adresa de email random.<br>
Tipuri si tehnici de testare folosite: 	Testare funcțională negativa. Tehnicile de testare: Equivalence Partitioning (clasă de echivalență invalidă)<br>
Response status code: 200 OK  <br>

Mai jos este ilustrata o imagine cu API request-ul din Postman:<br>

In imagine se observa metoda de request, endpoint-ul, request body este gol si response body<br>
![image](https://github.com/user-attachments/assets/ac2f4a77-6670-4c0b-9b63-57101bf142d6)

JavaScript Tests:

Imagine cu testele in java script pe care le-am definit, impreuna cu rezultatele executiei acestora<br>
![image](https://github.com/user-attachments/assets/19f115e5-3f35-44d3-af52-69b3d7b9a027)

<li>Stergerea unui client valid</li>

Metoda HTTP pentru request: POST:  http://te-echipam.gomag.ro/api/v1/customer/deleterequest/json<br>
Descriere request: Această metodă permite ștergerea unui client existent din baza de date a magazinului, prin trimiterea unui request POST ce conține ID-ul clientului și adresa de email asociată.<br>
Tipuri si tehnici de testare folosite: 	Testare funcțională pozitiva. Tehnicile de testare: Equivalence Partitioning – clasă de date valide<br>
Response status code: 200 OK  <br>

Mai jos este ilustrata o imagine cu API request-ul din Postman:<br>

In imagine se observa metoda de request, endpoint-ul, request body este gol si response body<br>
![image](https://github.com/user-attachments/assets/4b9342fe-74f0-4781-a39e-457d28f24bca)


JavaScript Tests:

Imagine cu testele in java script pe care le-am definit, impreuna cu rezultatele executiei acestora<br>
![image](https://github.com/user-attachments/assets/835fe99b-d65b-4d47-a0f5-4bbdfa66f175)


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



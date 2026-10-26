# Analysis of AI Usage and Impact on Students and Professionals

* **Autor:** Dora Kovačević
* **Datum:** Listopad 2026.

## O projektu
Ovaj projekt obuhvaća čišćenje, obradu i jednostavno analiziranje skupa podataka o upotrebi alata umjetne inteligencije (AI) među studentima i profesionalcima. Cilj je analize istražiti kako se AI alati koriste u svakodnevnom radu i učenju, koje se aktivnosti najčešće automatiziraju te kako uporaba AI-ja utječe na produktivnost.

## O skupu podataka (Dataset)
Skup podataka sadrži 300 zapisa i 19 stupaca s demografskim podacima, informacijama o korištenim AI alatima, svrsi korištenja te ocjenama zadovoljstva i produktivnosti. Podaci su preuzeti s Kagglea: https://www.kaggle.com/datasets/eishatuzzuhra/ai-usage-and-impact-on-students-and-professionals?resource=download

Glavne značajke skupa podataka uključuju:
* **Demografski podaci:** `Age`, `Gender`, `Country`, `Education_Level`, `Profession`, `Monthly_Income`
* **Korištenje umjetne inteligencije:** `AI_Tool`, `AI_Purpose`, `AI_Usage_Hours_Per_Day`, `Tasks_Performed`, `Monthly_AI_Cost`
* **Utjecaj i ocjene:** `Productivity_Score`, `Accuracy_Rating`, `Satisfaction_Score`, `Time_Saved_Hours_Per_Week`, `Work_or_Study_Hours_Per_Day`, `Would_Recommend`

## Čišćenje i priprema podataka (Data Cleaning)
U sklopu analize provedeno je opsežno predprocesiranje podataka:
1. **Konverzija tipova podataka:** Pretvaranje tekstualnih zapisa u numeričke vrijednosti uklanjanjem jedinica i simbola (npr. uklanjanje "yrs", "$", "hrs").
2. **Standardizacija tekstualnih polja:** 
   * Ujednačavanje zapisa za spol (`Gender`) i države (`Country` – npr. pretvaranje raznih oblika u 'UK', 'USA').
   * Standardizacija stupnja obrazovanja (`Education_Level`).
   * Normalizacija naziva AI alata (npr. ujednačavanje zapisa za ChatGPT, Copilot, Gemini).
3. **Kategorizacija zanimanja i zadaća:** 
   * Grupiranje višejezičnih i raznolikih naziva zanimanja u 9 glavnih kategorija te izdvajanje razine iskustva (`Seniority`).
   * Standardizacija i kategorizacija tekstualnih opisa obavljenih zadataka (`Tasks_Performed`) radi lakše statističke analize.

## Ključni uvidi i vizualizacije
* **Najčešći zadaci:** Identifikacija top 10 zadataka za koje korisnici primjenjuju AI alate (poput automatskog generiranja i korigiranja koda, pregleda literature i analize podataka).
* **Usporedba grupa:** Analiza razlika u načinu korištenja AI-ja između studenata i profesionalaca.
  * *Studenti* primarno koriste AI za pregled literature, sažimanje radova i akademska istraživanja (preko 40% njihovih najčešćih aktivnosti).
  * *Profesionalci* se najviše fokusiraju na generiranje i ispravljanje koda (skoro 40% ispitanih).
* **Utjecaj na produktivnost i zadovoljstvo:** Prikaz i analiza povezanosti između vrsta obavljanih zadataka i ocjena produktivnosti i zadovoljstva (`Productivity_Score`, `Satisfaction_Score`).

## Korištene tehnologije i biblioteke
Provedba analize rađena je u Python okruženju (Jupyter Notebook) uz korištenje sljedećih biblioteka:
* **Pandas** – za učitavanje, čišćenje i manipulaciju podacima
* **NumPy** – za numeričke operacije i uvjetno mapiranje
* **Seaborn** & **Matplotlib** – za vizualizaciju podataka i izradu dijagrama

---
*Projekt je izrađen u sklopu samostalnog rada i učenja / analize podataka.*

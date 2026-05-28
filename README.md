# gym_personlig_coach
Projekt i Datakvalitet
Utförd av Abbe och Vladde
* megaGymDataset.csv - original dataset
* megaGymDataset_ready.csv - slutlig dataset
* data_preprocess.ipynb - python-fil för behandling av data
* RAG_fitness.ipynb - RAG applikation
* requirements.txt - nödvändiga bibliotek i vara venv


Detta projekt är en RAG-applikation (Retrieval-Augmented Generation) som fungerar som en personlig träningscoach. Genom att använda **LangChain** och **Google Gemini** ger vi användaren exakta instruktioner för gymövningar baserat på en kvalitetssäkrad databas istället för generella AI-gissningar.

## Projektets Syfte

Huvudmålet med projektet är att visa hur **datakvalitet** fungerar som bränsle för moderna AI-system. Genom att genomföra en noggrann ETL-process (Extract, Transform, Load) på ett dataset från Kaggle säkerställer vi att assistenten levererar pålitlig information utan hallucinationer.

## Teknisk Stack

* **Språk:** Python
* **Ramverk:** LangChain
* **LLM:** Google Gemini
* **Embeddings:** Google Generative AI (gemini-embedding-001)
* **Vektordatabas:** ChromaDB
* **Datahantering:** Pandas

## Datakvalitet & Pre-processing

Vi har tillämpat kursens principer för datakvalitet genom att städa rådatan i flera steg:

* **Completeness:** Borttagning av rader utan instruktioner och kolumner med hög andel saknade värden (t.ex. Ratings).
* **Accuracy:** Verifiering av instruktionstexter för att säkerställa korrekta guider.
* **Uniqueness:** Eliminering av dubbletter för att optimera sökningen och spara tokens.
* **Consistency:** Standardisering av kategorier som utrustning och muskelgrupper.

## Installation & Körning

1. Klona repositoryt:
```bash
git clone https://github.com/vladde-dm25/gym_person_coach.git

```


2. Installera nödvändiga bibliotek:
```bash
pip install -r requirements.txt

```


3. Lägg till din API-nyckel i en `.env`-fil:
```env
GOOGLE_API_KEY=din_nyckel_här

```


4. Kör `data_preprocess.ipynb` följt av `RAG_fitness.ipynb`.

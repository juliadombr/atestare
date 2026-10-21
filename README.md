# Evaluare 01 — Învățarea supervizată

Analiza setului de date **Human Activity Recognition Using Smartphones (UCI HAR)** într-un notebook Python. Sunt rezolvate toate cele nouă secțiuni, inclusiv exercițiile opționale. Notebookul include rezultatele execuției și graficele.

## Conținut

- Import, verificarea tipurilor și a valorilor lipsă.
- Scatter plot și harta corelațiilor.
- Regresie liniară și metricile MAE, MSE, RMSE și R².
- KNN cu validare încrucișată în 5 folduri.
- Regresie logistică binară, SVM și matrice de confuzie multiclasa.
- Gradient Descent implementat manual.
- Random Forest, AdaBoost, Bagging și Stacking.

## Rulare

1. Instalează Python 3.12 și bibliotecile:

   ```bash
   pip install -r requirements.txt
   ```

2. Pune lângă notebook arhiva `human+activity+recognition+using+smartphones.zip` furnizată pentru evaluare. Aceasta conține arhiva interioară `UCI HAR Dataset.zip`. Prima celulă generează automat `Human_Activity_Recognition_Using_Smartphones_Data.csv`. Alternativ, poți pune direct CSV-ul generat lângă notebook.
3. Deschide `Ro_Evaluare_01_Invatarea_Supervizata_COMPLETAT.ipynb` în Jupyter sau VS Code și rulează celulele în ordine. În Google Colab, încarcă notebookul și arhiva sau CSV-ul.

Datele și mediile virtuale nu sunt incluse în repository. Rezultatele deja salvate în notebook pot fi citite fără rerulare.

## Rezultate

Setul conține 10.299 de observații, 561 de caracteristici, identificatorul persoanei și activitatea. Nu sunt valori lipsă. Împărțirea aleatoare este 80% antrenare / 20% testare, cu `random_state=42`.

| Model de clasificare | Acuratețe pe test |
| --- | ---: |
| KNN | 96,80% |
| Regresie logistică multiclasa | 98,54% |
| SVM | 99,22% |
| Stacking | 99,32% |

Pentru regresie, ținta este o măsurătoare numerică a accelerației; activitatea este folosită separat drept țintă de clasificare. Identificatorul `Subject` este exclus dintre predictori.

Împărțirea aleatoare poate include aceeași persoană în antrenare și testare. Aceste acurateți nu estimează strict generalizarea la persoane noi; aceasta necesită o împărțire după `Subject`.

## Date

Sursa: UCI Machine Learning Repository, *Human Activity Recognition Using Smartphones*, Davide Anguita și colaboratorii, 2012, DOI: `10.24432/C54S4K`. Fișierele folosite provin din arhiva furnizată pentru evaluare.

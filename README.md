#  Téma práce: Detekcia nenávistných komentárov v slovenčine

Tento repozitár obsahuje kód k bakalárskej práci, ktorá sa zameriava na detekciu toxických komentárov v slovenskom jazyku pomocou hlbokého učenia. Cieľom je vytvoriť presný a vysvetliteľný klasifikačný model schopný rozlišovať medzi toxickými a netoxickými komentármi, vrátane implementácie metód XAI (LIME a SHAP).

##  Použité modely
- `bert-base-uncased`
- `SlovakBERT` (gerulata/slovakbert)

##  Datasety
- `Toxic comments in Slovak social networks` 
- `TUKE-KEMT/toxic-sk`

##  Použité technológie a knižnice

Projekt bol implementovaný v **Python 3.10.11**. Pre spracovanie dát, modelovanie a vizualizáciu boli použité nasledujúce knižnice:

| Knižnica | Verzia | Popis |
|----------|--------|-------|
| `pandas` | 2.2.3 | Práca s dátami |
| `numpy` | 1.24.3 | Numerické výpočty |
| `matplotlib` | 3.10.1 | Vizualizácia grafov |
| `seaborn` | 0.13.2 | Vizualizácia (matica zámen a pod.) |
| `torch` | 2.6.0 | Tréning neurónových sietí |
| `transformers` | 4.50.1 | Predpripravené modely BERT a RoBERTa |
| `sklearn` | 1.6.1 | Vyhodnocovanie modelov, metriky |
| `datasets` | 2.14.5 | Načítavanie dátových množín z HuggingFace |
| `unicodedata` | 2.31.0 | Normalizácia unicode textu |
| `re` | 3.10.11 | Regulárne výrazy |
| `requests` | 3.10.11 | Práca s HTTP požiadavkami |

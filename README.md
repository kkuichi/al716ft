# 🎓 Detekcia nenávistných komentárov v slovenčine
**Autor:** Anna Leonenko  
**Fakulta:** FEI TUKE – Katedra kybernetiky a umelej inteligencie  
**Školiteľ:** prof. Ing. Ján Paralič, PhD.  
**Konzultantka:** Ing. Miroslava Matejová

## 📄 Popis projektu
Tento repozitár obsahuje kód k bakalárskej práci, ktorá sa zameriava na detekciu toxických komentárov v slovenskom jazyku pomocou hlbokého učenia. Cieľom je vytvoriť presný a vysvetliteľný klasifikačný model schopný rozlišovať medzi toxickými a netoxickými komentármi, vrátane implementácie metód XAI (LIME a SHAP).

## 🧠 Použité modely
- `bert-base-uncased`
- `SlovakBERT` (gerulata/slovakbert)

## 📦 Dataset
- `Toxic comments in Slovak social networks` (vlastná anotácia)
- `TUKE-KEMT/toxic-sk`

## 🔍 Použité metódy
- Tréning a evaluácia modelu pomocou `PyTorch` a `Transformers`
- Vysvetlenie predikcií pomocou:
  - `LIME` – Lokálne interpretable model-agnostické vysvetlenie
  - `SHAP` – Kvantitatívne príspevky slov podľa teórie kooperatívnych hier

## 📈 Výsledky
- Najlepší model: `SlovakBERT`
- Presnosť: až **92.84 %**
- Miera falošne negatívnych klasifikácií: **7.96 %**
- Vizualizácie ukazujú schopnosť modelu zachytiť expresívne alebo hanlivé výrazy

## 🗂️ Štruktúra repozitára
```
/lime/                 # LIME interpretácie (notebooky + HTML výstupy)
/shap/                 # SHAP analýza (notebooky + grafy)
/training/             # Tréningové skripty pre BERT a SlovakBERT
/data/                 # Spracovanie a príprava datasetov
utils.py               # Pomocné funkcie (tokenizácia, predikcie)
README.md              # Tento súbor
```

## 🚀 Spustenie
1. Klonuj repozitár:
   ```bash
   git clone https://github.com/kkuichi/al716ft.git
   cd al716ft
   ```

2. Nainštaluj závislosti:
   ```bash
   pip install -r requirements.txt
   ```

3. Spusti tréning:
   ```bash
   python training/train_slovakbert.py
   ```

4. Spusti XAI interpretáciu:
   ```bash
   python shap/shap_explainer.py
   ```

## 🧪 Závislosti
- `transformers`
- `torch`
- `sklearn`
- `shap`
- `lime`
- `pandas`, `matplotlib`, `seaborn`

## 🧠 Ukážky výstupov
Nájdeš vo výsledkoch v adresároch `/shap/` a `/lime/` – obsahujú vizualizácie prínosu jednotlivých slov.

## 📚 Viac o práci
Podrobné vysvetlenie teórie, metodiky, datasetov aj vyhodnotenie výsledkov je súčasťou PDF:  
📄 [BP_Leonenko_Anna.pdf](./BP_Leonenko_Anna.pdf)

# 🛡️ DataSwat – Jugaadu AI for UPI Fraud Detection

> "Fraud hone ke baad bank bolta hai — ‘Humse na ho payega.’  
> DataSwat bolta hai — ‘Pehle hi pakad lete hain bhai.’"

---

## 🤯 Kya Hai Ye?

DataSwat is your **gully-level genius AI** that scans your boring CSV files (yes, with those weird `V1–V28` columns), and tells you:

- Bhai, kaun sa transaction **fraud** ho sakta hai
- Kis customer ko **manual review** chahiye
- Aur kaun safe hai — jaane do use

All this, without needing any MBA, Excel macros, ya data science ka dard.  
Just upload your file, dekh lo result, aur kar lo action.

---

## 🧑‍💻 Rohan Ki Kahani (aka Every Indian Merchant Ever)

> “UPI fraud ho gaya. ₹37,000 gayab.  
> Bank bola: Sorry sir, prove karo.”  
> – Rohan, Jaipur (fictional… par real emotion)

- Rohan runs a chhoti si online dukaan.
- Gets monthly CSV from Razorpay-type gateway.
- UPI, GPay, PhonePe sab chalu hai.
- But **fraud ka koi guard nahi**.

**Enter: FraudShield**  
Ek click mein pata chal jaata hai — kaunse transaction suspicious lag rahe hain.

---

## 🤖 Features Jo Actually Kaam Aate Hain

| Feature | Samjhauta-free Breakdown |
|--------|--------------------------|
| 🔐 **CSV Upload** | Drag karo, drop karo, ho gaya |
| 🧠 **ML Model** | Trained on real fraud data, fitted with RandomForest |
| 🚥 **Risk Level** | ✅ Safe, ⚠️ Medium Risk, 🚨 High Risk |
| 📊 **Charts** | For logon jo visuals ke bina digest nahi karte |
| 📁 **Download Option** | Report le jao, boss ko dikhao |

---

## 🔍 Real Use-Case: UPI Scams on the Rise

As per **RBI**, UPI frauds have tripled.  
Par chhote merchants ke paas **zero tools**.  
FraudShield unke liye hai — *Not fancy dashboards. Just utility.*

---

## ⚙️ Tech Stack (Nerds ke liye)

| Layer     | Tools             |
|-----------|-------------------|
| ML Model  | scikit-learn (RandomForest) |
| Preproc   | PCA-transformed data + Scaler |
| App       | Streamlit (simple UI) |
| Export    | Pandas, Numpy, CSV |

---

## 📦 CSV Format (Important, warna model confuse hoga)

- Required Columns: `Time`, `V1–V28`, `Amount`
- Optional: `Class` (0 = legit, 1 = fraud)
- No missing values plz 🙏

---

## 💻 Kaise Use Karein?

1. `streamlit run app.py` chalao
2. CSV upload karo
3. Output table mein dekho:
   - Risk Level
   - Fraud probability
4. Manual review ya escalation karo

---

## 📉 Model Performance (Jitna bola hai, utna deliver karta hai)

| Metric        | Score |
|---------------|-------|
| Recall (fraud)| 76.3% |
| Precision     | 95.7% |
| F1-score      | 84.9% |
| AUC-ROC       | 0.93  |

> Apni taraf se toh full try maara hai.  
> Next upgrade mein XGBoost bhi aa raha hai.

---

## 📘 Fraud Handling Rulebook (Tandoor Garam Tip Type)

| Situation                  | Kya Karna Chahiye             |
|---------------------------|-------------------------------|
| Fraud score > 0.8         | Order hold + escalate karna  |
| High amount > ₹10,000     | Bhai, double check toh banta hai |
| Rapid fire UPI attempts   | Suspicious — alert karo      |
| Weird customer behavior   | Manual review must            |

> Ye rulebook app mein sidebar mein mil jaayega, dhoondhne ki zarurat nahi.

---

## 😂 Why It Stands Out (Other than the sarcasm)

- ✅ Works on **anonymized** PCA data (privacy = ✅)
- ✅ Built for **Rohan**, not Reliance
- ✅ Easy interface — no scary dashboards
- ✅ Gives verdicts, not confusion

---

## 🚧 Honest Confessions (Jhoothi tareef nahi karte yaar)

- ❌ Real-time detection? Nahi, abhi CSV-only hai
- ❌ Raw data support? Aayega, par abhi nahi
- ❌ Login/dashboard? MVP mein nahi, final product mein hoga
- ❌ Alert system? Sirf visual alert hai, no SMS/Email yet
- ❌ No SHAP explainability — par plan mein hai

---

## 🔮 Coming Soon (InshaALLH, ya jab bandwidth mile)

| Feature                    | Status     |
|----------------------------|------------|
| Real-time API              | ⏳ Working on it |
| Raw feature support        | 🔜 In roadmap |
| Explainable AI (SHAP)      | 😇 Patience bhai |
| User auth & dashboard      | 🧑‍💼 Under dev |
| UPI-partner integration    | 🙏 Wishful |

---

## 🔧 Installation Guide (5-minute jugaad)

```bash
# Clone repo
git clone https://github.com/prasannajeet/DataSwat.git
cd DataSwat

# Virtual env banayein
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Dependencies install karo
pip install -r requirements.txt

# Chalu karo Streamlit
streamlit run app.py

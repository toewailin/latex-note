[GitHub link](https://github.com/pmichaillat/latex-paper/tree/main) က Paul Michaillat ရဲ့ **"LaTeX template for academic papers"** ဖြစ်ပါတယ်။ ဒီ template က ရိုးရိုးရှင်းရှင်းနဲ့ အရမ်း Professional ကျလို့ နာမည်ကြီးပါတယ်။ 

---

### ၁။ File တစ်ခုချင်းစီရဲ့ တာဝန်များ (Project Structure)

ဒီ project ကို Overleaf မှာ တင်လိုက်ရင် အဓိက ဒီဖိုင်တွေကို တွေ့ရပါလိမ့်မယ် -

* **`paper.tex` (The Main File):**
    ဒါက အစ်ကို အဓိက ကိုင်ရမယ့်ဖိုင်ပါ။ စာတမ်းရဲ့ ခေါင်းစဉ်၊ နာမည်နဲ့ စာသား (Content) တွေကို ဒီထဲမှာပဲ ရေးရပါတယ်။
* **`paper.sty` (The Designer):**
    ဒါက အရေးကြီးဆုံးဖိုင်ပါ။ LaTeX ရဲ့ margin တွေ၊ font တွေ၊ `\maketitle` ရဲ့ ပုံစံတွေကို ဒီထဲမှာ ကြိုတင် Design ဆွဲထားတာပါ။ အစ်ကိုက `\usepackage{paper}` လို့ ခေါ်လိုက်တာနဲ့ ဒီဖိုင်ထဲက design တွေ အကုန်လုံး အသက်ဝင်လာတာ ဖြစ်ပါတယ်။
* **`paper.bib` (References):**
    ဒါက အကိုကိုးကားမယ့် စာအုပ်တွေ၊ စာတမ်းတွေရဲ့ စာရင်းကို သိမ်းတဲ့နေရာပါ။
* **`figures.pdf`:**
    ဒါကတော့ စာတမ်းထဲမှာ သုံးမယ့် ပုံတွေကို စုထားတဲ့ ဖိုင်ပါ။

---

### ၂။ ဒီ Template ရဲ့ ထူးခြားချက် (The Method)

ဒီ template က **"Separation of Concerns"** ဆိုတဲ့ programming concept ကို သုံးထားပါတယ်။

1.  **Metadata အရင်ပေးရတယ်:** `\title`, `\author`, `\date` စတာတွေကို အရင်သတ်မှတ်ရတယ်။
2.  **Custom Commands:** သူက `\paperurl` လိုမျိုး ကိုယ်ပိုင် command အသစ်တွေ ဖန်တီးထားပါတယ်။ ဒါကြောင့် standard LaTeX ထက်စာရင် ပိုပြီး သပ်ရပ်တာပါ။
3.  **Titlepage Environment:** ခေါင်းစဉ်နဲ့ Abstract ကို `\begin{titlepage} ... \end{titlepage}` ကြားထဲမှာ ထည့်ထားတဲ့အတွက် Compile လုပ်လိုက်ရင် အဲဒီအပိုင်းက စာမျက်နှာ အစမှာပဲ သီးသန့် သပ်သပ်ရပ်ရပ် ပေါ်လာတာ ဖြစ်ပါတယ်။

---

### ၃။ ဘာကြောင့် အစဉ်လိုက် ဖြစ်နေတာလဲ? (Detailed Logic)

အစ်ကို့ code ထဲမှာ `\section{Introduction}` ကို `\maketitle` ရဲ့ အပေါ်မှာ သွားရေးထားရင်တောင် `paper.sty` ထဲက rule တွေကြောင့် LaTeX က ခေါင်းစဉ်ကို အရင်ထုတ်ပေးမှာပါ။

**အလုပ်လုပ်ပုံ အဆင့်ဆင့်:**
1.  **Reading `paper.sty`:** LaTeX က အစ်ကိုသုံးမယ့် design rules တွေကို အရင်ဖတ်ပါတယ်။
2.  **Collecting Data:** `\title` နဲ့ `\author` ထဲက စာသားတွေကို မှတ်သားထားပါတယ်။
3.  **Executing `\maketitle`:** ဒီ command ကို တွေ့တာနဲ့ သူမှတ်ထားတဲ့ Title ကို ပုံစံချပြီး စာမျက်နှာထိပ်မှာ တင်လိုက်ပါတယ်။
4.  **Flowing Content:** အဲဒီနောက်မှာမှ `\section` တွေ၊ `\paragraph` တွေကို တစ်ခုပြီးတစ်ခု စီပေးသွားတာပါ။

LaTeX ရဲ့ ထူးခြားချက်က Code ထဲမှာ ရေးချင်သလို ရေးထားပေမဲ့ Compile လုပ်လိုက်တဲ့အခါ သူသတ်မှတ်ထားတဲ့ ပုံစံအတိုင်း အစဉ်လိုက် ထွက်လာတာပါ။ ဒါကို "Logical Structuring" လို့ ခေါ်ပါတယ်။

---

### ၄။ အစ်ကို့အတွက် အကြံပြုချက်
ဒီ template ကို သုံးမယ်ဆိုရင် -
* `paper.sty` ဖိုင်ကို **သွားမပြင်ပါနဲ့** (အကယ်၍ design ကို အရမ်းကျွမ်းကျင်တာမဟုတ်ရင်)။
* စာသားတွေကို `paper.tex` ထဲမှာပဲ အာရုံစိုက်ရေးပါ။
* အကို့ရဲ့ references တွေကို `paper.bib` ထဲမှာ သွားထည့်ပါ။

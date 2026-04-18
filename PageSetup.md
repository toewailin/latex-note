LaTeX မှာ စာမျက်နှာကို ပုံစံချဖို့အတွက် **`geometry`** ဆိုတဲ့ package က အသုံးအဝင်ဆုံးပါပဲ။ LaTeX ဟာ standard အားဖြင့် margin တွေကို အတော်လေး ကျယ်ကျယ်ထားလေ့ရှိတဲ့အတွက် ကျွန်တော်တို့ စိတ်ကြိုက် ပြန်ပြင်ဖို့ လိုအပ်ပါတယ်။

အောက်မှာ တစ်ခုချင်းစီကို အသေးစိတ် ရှင်းပြပေးပါမယ်။

---

## ၁။ Page Setup & Margins (စာမျက်နှာ အထားအသို)
LaTeX မှာ margin တွေကို ပြင်ချင်ရင် `\documentclass` ရဲ့ အောက် (Preamble) မှာ `geometry` package ကို အခုလို သုံးရပါတယ်။

```latex
\usepackage[
  a4paper,
  left=1in,
  right=1in,
  top=1in,
  bottom=1in
]{geometry}
```
* **Paper Size:** `a4paper`, `letterpaper` စသဖြင့် ပြောင်းလဲနိုင်ပါတယ်။
* **Specific Margins:** ဘယ်၊ ညာ၊ အပေါ်၊ အောက် margin တွေကို `inch`, `cm`, သို့မဟုတ် `mm` နဲ့ သတ်မှတ်နိုင်ပါတယ်။

---

## ၂။ Alignment (စာသားများ အစီအစဉ်)
LaTeX မှာ standard အားဖြင့် စာသားတွေကို **Justified** (ဘယ်ရော ညာရော ညီအောင်) အလိုအလျောက် ညှိပေးပါတယ်။ ဒါကို ပြောင်းချင်ရင် အောက်ပါ commands တွေကို သုံးနိုင်ပါတယ် -

### (က) Block တစ်ခုလုံးအတွက် Environment သုံးခြင်း
* **Center:** `\begin{center} ... \end{center}`
* **Left-aligned:** `\begin{flushleft} ... \end{flushleft}`
* **Right-aligned:** `\begin{flushright} ... \end{flushright}`

### (ခ) စာကြောင်းတစ်ကြောင်းချင်းစီအတွက် Command သုံးခြင်း
* `\centering`: ခေါင်းစဉ်တွေကို အလယ်ပို့ချင်တဲ့အခါ သုံးပါတယ်။
* `\raggedright`: စာသားတွေကို ဘယ်ကပ်ချင်တဲ့အခါ သုံးပါတယ်။

---

## ၃။ Padding & Spacing (အကွာအဝေးများ)
LaTeX မှာ Word လိုမျိုး direct "Padding" ဆိုတဲ့ စကားလုံးထက် **Spacing** လို့ ပိုသုံးပါတယ်။

### (က) စာကြောင်း အကွာအဝေး (Line Spacing)
Line spacing ပြင်ချင်ရင် `setspace` package ကို သုံးရပါတယ်။
```latex
\usepackage{setspace}
\onehalfspacing  % ၁.၅ စာကြောင်းကွာ
\doublespacing   % ၂ စာကြောင်းကွာ
```

### (ခ) အပိုဒ်များကြား အကွာအဝေး (Paragraph Spacing)
အပိုဒ်တွေကြားထဲမှာ space ချင်ရင် ဒါကို preamble ထဲ ထည့်ပါ -
```latex
\setlength{\parskip}{1em} % အပိုဒ်တစ်ခုပြီးတိုင်း 1em (စာလုံးတစ်လုံးစာ) ချန်မည်
```

### (ဂ) အပိုဒ်အစ နေရာချန်ခြင်း (Paragraph Indent)
အပိုဒ်အစမှာ ရှေ့ကို နည်းနည်းတိုးချင်ရင် -
```latex
\setlength{\parindent}{2em} % ၂ စာလုံးစာ အကွာအဝေး ချန်မည်
```

---

## ၄။ Horizontal & Vertical Space (Manual ချိန်ညှိခြင်း)
နေရာလွတ်တွေကို ကိုယ်တိုင် လက်နဲ့ ချိန်ချင်တဲ့အခါ -
* `\hspace{1cm}`: ဘေးတိုက် (Horizontal) နေရာလွတ် ၁ စင်တီမီတာ ချန်ပါတယ်။
* `\vspace{2cm}`: အပေါ်အောက် (Vertical) နေရာလွတ် ၂ စင်တီမီတာ ချန်ပါတယ်။
* `\hfill`: စာသားနှစ်ခုကို ဘယ်အစွန်နဲ့ ညာအစွန်ဆီသို့ တွန်းထုတ်ပေးပါတယ်။

---

## ဥပမာ Project Structure
Overleaf မှာ အခုလို စမ်းရိုက်ကြည့်ပါ -

```latex
\documentclass[12pt, a4paper]{article} % စာရွက်အရွယ်အစားနှင့် စာလုံးအရွယ်အစား သတ်မှတ်ခြင်း
\usepackage[utf8]{inputenc}
\usepackage[a4paper, margin=1in]{geometry} % Margin ချိန်ခြင်း
\usepackage{setspace}
\onehalfspacing % စာကြောင်းကွာ ချိန်ခြင်း

\begin{document}

\begin{center}
    \huge \textbf{Page Setup Test} \\ % Center align လုပ်ခြင်း
    \large Toe Wai Lin
\end{center}

\vspace{1cm} % Space ချန်ခြင်း

\section{First Section}
\raggedright % ဘယ်ဘက်ကို ကပ်ခြင်း
ဒီစာသားတွေကတော့ ဘယ်ဘက်ကို ကပ်နေပါလိမ့်မယ်။ LaTeX ရဲ့ geometry package ကို သုံးထားတဲ့အတွက် margin ကလည်း 1 inch ပဲ ရှိပါတော့တယ်။

\end{document}
```
---

### ၁။ `\documentclass[a4paper]{article}` (Global Option)
ဒါက LaTeX Kernel (အခြေခံစနစ်) ကို "ငါ A4 paper သုံးမယ်" လို့ သတင်းပို့လိုက်တာပါ။

* **အလုပ်လုပ်ပုံ:** LaTeX မှာ ပါပြီးသား standard setting တွေကို သုံးပါတယ်။
* **Margin များ:** LaTeX ရဲ့ standard A4 margin တွေက အရမ်းကျယ်ပါတယ်။ (စာမျက်နှာရဲ့ ဘေးတွေမှာ နေရာလွတ် အများကြီး ကျန်နေပါလိမ့်မယ်)။
* **စာလုံးအရွယ်အစား:** `12pt` လို့ ထည့်ရေးလိုက်ရင် တစ်စာအုပ်လုံးမှာရှိတဲ့ စာသားတွေရဲ့ standard size ကို 12pt ဖြစ်အောင် ပြောင်းပေးပါတယ်။
* **ကန့်သတ်ချက်:** Margin တွေကို ကိုယ်တိုင် လက်နဲ့ စိတ်ကြိုက် ပြင်လို့မရပါဘူး။

---

### ၂။ `\usepackage[a4paper, ...]{geometry}` (Package Option)
ဒါကတော့ **Geometry** ဆိုတဲ့ အထူးပြု Package ကို သုံးပြီး စာမျက်နှာ layout ကို အသေးစိတ် စိတ်ကြိုက် Layout ချတာ ဖြစ်ပါတယ်။

* **အလုပ်လုပ်ပုံ:** LaTeX ရဲ့ standard setting တွေကို ကျော်ဖြတ်ပြီး ကိုယ်ပေးတဲ့ margin အတိုင်း (ဥပမာ- `left=1in`) အတင်းအကျပ် ပြောင်းလဲခိုင်းတာပါ။
* **တိကျမှု:** `left`, `right`, `top`, `bottom` တွေကို စိတ်ကြိုက် စီမံနိုင်ပါတယ်။
* **ဦးစားပေး:** အကယ်၍ `\documentclass` မှာ တစ်မျိုး၊ `geometry` မှာ တစ်မျိုး ရေးထားရင် `geometry` ထဲက တန်ဖိုးကိုပဲ LaTeX က ဦးစားပေး သုံးပါလိမ့်မယ်။

---


### ဘယ်လို သုံးသင့်သလဲ? (Best Practice)
Professional ကျတဲ့ စာတမ်းတွေမှာ နှစ်ခုလုံးကို တွဲသုံးတာ အကောင်းဆုံးပါ။

```latex
\documentclass[12pt, a4paper]{article} % Standard size တွေ သတ်မှတ်တယ်

\usepackage[
  a4paper, 
  margin=1in % စံသတ်မှတ်ချက်အတိုင်း margin ကို 1 inch ပြန်ချုံ့တယ်
]{geometry}
```

**ဘာကြောင့် တွဲသုံးရတာလဲ?**
`\documentclass` မှာ `a4paper` လို့ ထည့်ရေးခြင်းဖြင့် တခြား package တွေ (ဥပမာ- ပုံတွေ ထည့်တဲ့အခါ) က စာမျက်နှာ အကျယ်ကို သိရှိနိုင်မှာ ဖြစ်ပါတယ်။ ဒါပေမဲ့ Margin တွေ လှလှပပ ဖြစ်ဖို့အတွက်တော့ `geometry` ကို မဖြစ်မနေ သုံးရတာ ဖြစ်ပါတယ်။

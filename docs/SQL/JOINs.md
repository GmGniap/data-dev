### Implicit vs Explicit JOINs

- Implicit JOIN ဆိုတာက WHERE statement ပေါ်ပဲ လုံးလုံး မူတည်ပြီး join condition တွေကို ပြုလုပ်တာမျိုးကို ဆိုလိုပါတယ်။ အလွယ်မှတ်မယ် ဆိုရင်တော့ JOIN statement ကို လုံးဝ မသုံးပါဘူး။ 
- Implicit JOIN ကို အောက်ပါ ပုံစံအတိုင်း နမူနာ ကြည့်နိုင်ပါတယ်။
```sql
SELECT col_names
FROM table1, table2
WHERE table1.col_name = table2.col_name
```

- Explicit JOIN ကတော့ ပုံမှန် အသုံးများတဲ့ JOIN statement ကို အသုံးပြုပြီး ပြုလုပ်တာမျိုးပါ။ ဥပမာ အနေနဲ့ 
```sql
SELECT col_names
FROM table1
JOIN table2
ON table1.col_name = table2.col_name
```

- ဒီ ၂ ခု အကြားမှာ performance ကွာခြားမှု မရှိပေမယ့် Explicit JOIN ကိုတော့ standard အနေနဲ့ အသုံးပြုသင့်ပါတယ်။ အရမ်း ရှုပ်ထွေးတဲ့ query တွေမှာ Implicit ပုံစံ ရေးရရင် နားလည်မှု လွဲမှားတာမျိုးတွေ ဖြစ်နိုင်ပါတယ်။
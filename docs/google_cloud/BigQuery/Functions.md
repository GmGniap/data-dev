## Conversion Functions

- `SAFE_CAST`
	- GoogleSQL က `CAST` ကို သုံးတဲ့အခါမှာ ပြောင်းလို့မရတာမျိုးနဲ့ ကြုံရင် query fail ပါတယ်။ ဥပမာ - ဒီ query ဆို error တက်ပါလိမ့်မယ်။
```sql
SELECT CAST("apple" AS INT64) AS not_a_number;
```

အကယ်ရွေ့ Error မတက်ချင်ဘူးဆိုရင် `SAFE_CAST` ကို ပြောင်းသုံးလို့ ရတယ်။ `SAFE_CAST` ရဲ့ အလုပ်လုပ်ပုံက runtime errors တွေကို `NULL` နဲ့ အစားထိုးပေးမှာပါ။ 


## Date Functions
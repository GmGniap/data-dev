Google Cloud က စီစဥ်တဲ့ ဒီ [Youtube Talk](https://www.youtube.com/watch?v=cZgTavxWO2k) ကို နားထောင်ရင်း နားလည်သမျှကို မြန်မာလို note ပြန်ထုတ်ထားခြင်း ဖြစ်ပါတယ်။

Cost Optimization လို့ စဥ်းစားရင် Query Processing နဲ့ Storage အတွက် ဆိုပြီး ၂ ပိုင်း ခွဲပြီး စဥ်းစားသင့်တယ်။

### Query Processing
- On-demand နဲ့ Flat-rate pricing ဆိုပြီး ၂ မျိုး ရှိတယ်။
	- သာမန်အားဖြင့်တော့ On demand ကို default သုံးကြတယ်။ Flat-rate ကကျတော့ Google နဲ့ စာချုပ်ချုပ်ပြီး company တစ်ခုလုံးအတွက် သုံးတာမျိုး။
- On-demand (သုံးသလောက်ပေး စနစ်) အတွက် ငွေ ဖြတ်တဲ့နှုန်းကတော့ အောက်ပါတိုင်း ဖြစ်ပါတယ်။ လတိုင်းမှာတော့ 1TB အခမဲ့ ရတယ်။ အဲဒီ ပမာဏထက် ကျော်လွန်သွားရင်တော့ TB အလိုက် ၊ Region အလိုက် ပိုက်ဆံ ပေးရမှာပါ။
![[Pasted image 20250304175055.png]]

- Query optimizing အတွက်က အကြမ်းဖျဥ်း ဒီ အချက်တွေ ထည့်စဥ်းစားဖို့ လိုပါမယ်။
	- လိုအပ်တဲ့ ဒေတာ columns တွေကိုပဲ ရယူပါ ။ `SELECT *` ကို မလိုအပ်ပဲ မသုံးပါနဲ့။
	- BigQuery Setting ထဲကနေ Cost Control setting ကို ဖွင့်ထားပါ။
	- ဒေတာအတွက် Partitioning / Clustering နည်းလမ်းများကို မှန်ကန်စွာ အသုံးချပါ။
	- မိမိ ရဲ့ BigQuery processing cost က USD $XXk (ဒေါ်လာ သောင်း/သိန်း ကျော်နေပါက) Flat-rate pricing ကို ပြောင်းလဲ အသုံးပြုပါ။

### Optimizing Storage
- Data Retention
	- BigQuery ထဲမှာ create လိုက်တဲ့ ဒေတာ table တွေကို အချိန် ဘယ်လို ကြာကြာ သိမ်းဆည်းမလဲ။ အဲဒီအတွက် Dataset create လုပ်တဲ့အဆင့်မှာ expired date ရွေးလို့ ရပါတယ်။
	- အကယ်ရွေ့ ကိုယ့်ရဲ့ data table (သို့မဟုတ်) partition က ရက် ၉၀ အထိ လုံးဝ edit မပြုလုပ်တော့ဘူးဆိုရင်တော့ storage price ကို 50% လျှော့ချပေးပါတယ်။ 
	- ဒါကြောင့် ဘယ်လို Activity တွေ (ဥပမာ - BigQuery ထဲကို loading , DML)
- Storage Pricing - ![[Pasted image 20250304184125.png]]
- GCP ရဲ့ မတူညီတဲ့ cloud services တွေထဲမှာ Data copies တွေ duplicates ဖြစ်နေတာကို လျှော့ချပါ။
- Streaming inserts - what's that?? :D
- Backup & Recovery
	- ၇ ရက်အတွင်း ဒေတာတွေကို ပြန် read လို့ ရသေးတယ်။
	- Use below query :
```sql
SELECT x,y
FROM dataset.table
FOR SYSTEM_TIME AS OF
	TIMESTAMP_SUB(CURRENT_TIMESTAMP() , INTERVAL 3 DAY)
```

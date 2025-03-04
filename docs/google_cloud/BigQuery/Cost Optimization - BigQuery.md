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
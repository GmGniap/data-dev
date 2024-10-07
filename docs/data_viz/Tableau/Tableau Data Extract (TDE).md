## TDE ဆိုတာ ဘာလဲ? 

Tableau Viz တစ်ခုကို အလျှင်အမြန် render ပြသဖို့အတွက် Disk ထဲမှာ compressed snapshot အနေနဲ့ ဒေတာ သိမ်းဆည်းထားပြီး Memory ထဲကို loaded ပြုလုပ်ထားတာကို Tableau Data Extract လို့ ခေါ်ပါတယ်။ 

## အသုံးချနေရာများ
1. Performance
2. Reduced load
3. Portability
4. Pre-aggregations
5. Materialization of calculated field
6. Publishing to Tableau Public and Tableau Online
## တည်ဆောက်ပုံ - TDE Architectuse
- Tableau Official Documentation - Understanding Data Extracts

TDE design နဲ့ ပတ်သတ်ပြီး စိတ်ဝင်စားစရာ ၂ ခုကတော့ 
1. TDE က columnar store တစ်ခု ဖြစ်ပါတယ်။
2. TDE တည်ဆောက်ပုံ က memory ထဲကို ဘယ်လိုပုံစံ load ပြုလုပ်လိုက်သလဲ ဆိုတာရယ် Tableau အနေနဲ့ အသုံးပြုသလဲ အပေါ်မှာ သက်ရောက်မှုတွေ ရှိပါတယ်။ TDE တွေကို "architecture aware" ဖြစ်ဖို့လိုပါတယ်။ ဆိုလိုတာက TDEs တွေက သင့်ကွန်ပျူတာရဲ့ RAM ကနေ Hard disk အထိ Memory တွေကို အသုံးချသလို တပိုင်းချင်းဆီကိုလဲ ၎င်းရဲ့ characteristics များအတိုင်းလိုအပ်သလို ထည့်သွင်းလုပ်ဆောင်ပါတယ်။ 

2025 DE Zoomcamp curriculum ထဲမှာ ပါတဲ့ `dlt` အကြောင်းကို Study Group မှာ ဆွေးနွေးဖို့အတွက် လေ့လာရင်း မှတ်သားမိသမျှ စိတ်ဝင်စားစရာ အချက်အလက်တွေကို မျှဝေပေးချင်တာပါ။ `dlt` အကြောင်း စလေ့လာတဲ့ အချိန်မှာ ပထမဆုံး အံ့အားသင့်စရာက [Official Documentation](https://dlthub.com/docs/intro) က အင်မတန် သပ်သပ်ရပ်ရပ် နဲ့ ရေးထားပြီး [blog](https://dlthub.com/blog) တွေ ၊ Youtube videos တွေ ၊ dlt အကြောင်း talks တွေ စုံစုံလင်လင် ကို ရှိနေတာပါ။ open source library တစ်ခု ဖြစ်လို့ ဆိုတာထက် 2023 နှစ်စပိုင်းလောက်မှာမှ စတင်တဲ့ tool/library တစ်ခု အနေနဲ့ ဒီလောက် မြန်မြန်ဆန်ဆန် community အရရော ၊ content အရရော တိုးလာတာမျိုးကို ဆိုလိုတာပါ။ ဖတ်စရာ ၊ ကြည့်စရာတွေ များလွန်းတော့ ဒီ မိတ်ဆက်မှာတော့ အတတ်နိုင်ဆုံး အနှစ်ချုပ်ပြီး ရေးသားထားပါတယ်။

## Data Load Tool ဆိုတာ ဘာလဲ။

Data Field မှာ အလုပ်လုပ်နေတဲ့သူတွေအနေနဲ့ Data Pipelines (ETL / ELT) စသဖြင့် ရင်းနှီးပြီးသား ဖြစ်နိုင်ပေမယ့် အခုမှ စတင် လေ့လာမယ့်သူတွေ အနေနဲ့တော့ ဒီမေးခွန်းကို မေးချင်လိမ့်မယ် ထင်တယ်။ အလွယ်ကူဆုံး နဲ့ အမြင်သာဆုံး ဖြစ်အောင် နေ့စဥ် ဘဝမှာ မြင်နေရတဲ့ နမူနာ တစ်ခု နဲ့ ရှင်းပြချင်ပါတယ်။ ဥပမာ - စပါး ကနေ ဆန် ဖြစ်အောင် ပြုလုပ်ရတဲ့ အလုပ် တစ်ခု ဆိုပါစို့ ။ ယေဘုယျအားဖြင့်တော့ ဒီအလုပ်မှာ ပထမဆုံး စပါး စိုက်ရတယ် ။ ရိတ်သိမ်းရတယ်။ နေလှမ်း အခြောက်ခံရတယ်။ သိမ်းဆည်းရတယ်။ ကြိတ်စက်ကို ပို့ရတယ်။ ဆန်ကြိတ်ရတယ်။ စသဖြင့် ရှိမှာပေါ့လေ ။ 

<illustration ပုံ ထည့်ရန် >

ဒေတာ နဲ့ ပတ်သတ်ရင်လဲ အလားတူ အဆင့်ဆင့် ပြောင်းလဲ ၊ ရွေ့ပြောင်းရတဲ့ အဆင့်တွေ ရှိပါတယ်။ ပထမဆုံး Raw Data ကို စုဆောင်းရတယ်။ Data File Format မျိုးစုံ နဲ့ အဆင်ပြေသလို (စနစ် မကျနစွာနဲ့) သိမ်းဆည်းရတယ်။ ရရှိလာတဲ့ Data တွေအားလုံးကို Cleaning လုပ်ရတယ်။ ထွက်လာတဲ့ Cleaned Results - data တွေကို စနစ်တကျ Database System တွေထဲ (ဥပမာ - SQL / NoSQL database) ထပ် သိမ်းရပြန်တယ်။ ဒေတာတွေဆိုတာကလဲ သိမ်းရုံနဲ့ မပြီးဘူး ၊ သုံးနိုင်မှ အဖိုးတန်မှာ ဆိုတော့ ဒီ ဒေတာတွေကို စီးပွားရေးအမြင်ရ ၊ လုပ်ငန်းလိုအပ်ချက်အရ Transformation ပြောင်းလဲမှု တွေ ထပ်လုပ်ရပြန်တယ်။ ပြောင်းလဲမှုဆိုတာမှာ Machine Learning Analysis လုပ်တာတွေ Statistics အရ aggregation လုပ်တာတွေ စသဖြင့် မျိုးစုံ ဖြစ်နိုင်ပါတယ်။ 

<illustration ပုံ ထည့်ရန်>

ဒီလို အဆင့်ဆင့် ပြောင်းလဲ ၊ ရွေ့ပြောင်းရမှုတွေကို Standardize ဖြစ်အောင် ETL / ELT pipelines စသဖြင့် ခေါ်ဝေါ် သတ်မှတ်လာပါတယ်။ ETL ကတော့ **Extract** (ဒေတာ အရင် ဆွဲထုတ်) -> **Transform** (ဒေတာ ကို လိုသလို ပုံပြောင်း) -> **Load** (ကိုယ် သိမ်းချင်တဲ့ Database System ထဲကို ထည့်သွင်း) တဲ့ pipeline ဖြစ်ပါတယ်။ ELT ကတော့ **Extract** -> **Load** (ဒေတာကို Source System ကနေ တိုက်ရိုက်ယူပြီး အရင် သိမ်းဆည်း) -> **Transform** (နောက်ဆုံးမှ ပြောင်းလဲ) တဲ့ pipeline ဖြစ်ပါတယ်။ ETL vs ELT အကြား ကွာခြားချက်တွေ အကြောင်း စိတ်ဝင်စားရင် အင်တာနက်မှာ အသေးစိတ် ထပ်မံ ရှာဖွေ ဖတ်ရှုစေချင်ပါတယ်။

ဒီတော့ Data Load Tool (dlt) ကတော့ ELT pipeline အတွက် အဓိက ရည်ရွယ်ထားတဲ့ Python Library တစ်ခု ဖြစ်ပါတယ်။ Python Programming ပေါ် လုံးဝ အခြေခံထားတာ ဖြစ်တဲ့ အတွက် Python (နည်းနည်းပါးပါး) သိရုံနဲ့တင် `dlt` ကို အသုံးပြုပြီး production-level pipeline တစ်ခု တည်ဆောက်နိုင်ပါတယ်။

`dlt` နဲ့ ပတ်သတ်ပြီး မိတ်ဆက် အကြောင်းတွေ ထပ်သိလိုတယ် ဆိုရင် ဒီ Link / Video တွေကို ကြည့်ရှုဖို့ အကြံပြုလိုပါတယ်။
- Link
- EuroPython 2024 Presentation : "Pandas to Production" - Youtube

### dlt Installation

`pip install dlt` 
## dlt အခြေခံ concepts

`dlt` မှာ အခြေခံအားဖြင့် အောက်ပါ concepts တွေ ကို နားလည်ဖို့ လိုအပ်ပါတယ်။
- Source
- Resource
- Pipeline
- Destination
- Dataset
<img title="dlt-concept by Cruxdata" alt="Credit to Cruxdata" src="https://img.plasmic.app/img-optimizer/v1/img?src=bab69d070db436dbd311dac286ed3eb0.png&f=webp&q=75" width="500" height="250" >

- Source ဆိုတာက ဆွဲထုတ်ယူမယ့် ဒေတာတွေအားလုံးကို ခြုံငုံတဲ့ Logical data group ဖြစ်ပါတယ်။ resources တွေကို ပေါင်းလိုက်ပြီး Source အနေနဲ့ အသုံးပြုတာပါ။
- Resource ဆိုတာကကျ database table တစ်ခုကနေ ဖြစ်ဖြစ် ၊ API endpoint တစ်ခုကနေ ဖြစ်ဖြစ် သီးခြား ဆွဲထုတ်ယူတဲ့ အဆင့် ကို ဆိုလိုတာပါ။
- Transformer ကကျတော့ ဒေတာကို သတ်မှတ်ထားတဲ့ destination ထဲ မထည့်ခင်မှာ ပြောင်းလဲလိုတာတွေ ပြောင်းလဲတဲ့ အဆင့် ပါ။
- Destination ကကျတော့ နောက်ဆုံးမှာ ဒေတာတွေကို အရောက်ပို့ရမယ့် နေရာ ပါပဲ။
- Pipeline ကတော့ ဒီ source / resource သတ်မှတ်တာတွေ ၊ transformation ပြောင်းလဲတာတွေ ၊ destination ထဲ ထည့်တာတွေ အားလုံးကို စုပေါင်းထားတဲ့ collection ကို ဆိုလိုပါတယ်။

### Resource

### Source

### Pipeline

- `pipeline` အတွက် `progress` argument ကို အသုံးပြုပြီး loading process ကို monitor ပြုလုပ်လို့ ရတယ်။ [Ref](https://dlthub.com/docs/general-usage/pipeline#display-the-loading-progress)

### dlt အလုပ်လုပ်ပုံ
`dlt` အနေနဲ့  အဓိက အဆင့် ၃ ဆင့် ပါဝင်တယ်။
- Extract
- Normalize
- Load


### Configuration & Secrets in dlt

`dlt` pipeline တွေမှာ များသောအားဖြင့် configurations နဲ့ credentials တွေ အသုံးပြုဖို့ လိုအပ်ပါတယ်။ ဒီအတွက်ကိုတော့ အောက်ပါ နည်းလမ်းတွေ အတိုင်း set up ပြုလုပ်လို့ ရပါတယ်။

1. Environment variables များကို အသုံးပြုခြင်း။ (production တွင် အသုံးပြုသင့်သည်)
2. `dlt` configuration files တွေ ဖြစ်တဲ့ `secrets.toml` နဲ့ `config.toml` တို့ကို အသုံးပြုခြင်း။ (local dev တွင် အသုံးပြုသင့်သည်)
3. Key managers နဲ့ Vaults များကို အသုံးပြုခြင်း။

ကိုယ်ကသာ naming conventions ကို မှန်မှန်ကန်ကန် ပေးထားမယ်ဆိုရင် `dlt` အနေနဲ့ configuration settings နဲ့ secrets တွေကို အလိုအလျောက် ရယူပါလိမ့်မယ်။ ပြီးတော့ code ထဲက လိုအပ်တဲ့ နေရာတွေကို values တွေ အဖြစ် ထည့်သွင်းသွားပါမှာ။

`dlt.secrets.value` ကို အသုံးပြုပြီးတော့လဲ resources နဲ့ sources တွေအတွက် credentials သတ်မှတ်ပေးလို့ ရပါတယ်။ (Variable Assign ချတဲ့ ပုံစံမျိုးပါ)။ ဒီမှာ အရေးကြီးတာ တစ်ခုက အတတ်နိုင်ဆုံး configurations တွေ credentials တွေ အားလုံးကို `dlt.secrets` (တနည်းအားဖြင့် `secrets.toml`) ထဲမှာ ထည့်သွင်းရပါမယ်။ `dlt.config` (တနည်းအားဖြင့် `config.toml`)မှာ credentials တွေ ထည့်သွင်းလို့ ရမှာ မဟုတ်ပါဘူး။ `dlt` အနေနဲ့က အဲဒီ `config.toml` file ကနေ credentials တွေ ဖတ်မှာ မဟုတ်လို့ပါ။ 

### dlt Write Disposition for Incremental Loading

Write Disposition ဆိုတာက ကိုယ် သိမ်းချင်တဲ့ နေရာ destination မှာ ဒေတာတွေကို ဘယ်လိုပုံစံမျိုး သိမ်းမလဲ (write) ဆိုတာကို `dlt` library အနေနဲ့ သတ်မှတ်ရတာမျိုးကို ဆိုလိုပါတယ်။ `dlt` မှာ အဓိက Write Disposition ၃ ခု ရှိပါတယ်။

1. Append - **default** disposition ဖြစ်ပါတယ်။ Destination မှာ ရှိနေပြီးသား ဒေတာတွေထဲကို ဒေတာအသစ်တွေ ထပ်ပေါင်းထည့်သွားမှာပါ။
2. Full Load (or) Replace - Destination မှာ ရှိနေပြီးသား ဒေတာတွေကို Resource က လာမယ့် ဒေတာတွေနဲ့ အစားထိုး (replace) ပြုလုပ်မှာပါ။ ရှိပြီးသား ဒေတာတွေအားလုံးကို **delete** ပြုလုပ်ပြီး schema ကို **recreate** အသစ် ပြုလုပ်မယ်။ ပြီးမှ ဒေတာတွေကို load ထည့်ပါမယ်။
3. Merge - Destination မှာ ရှိနေပြီးသား ဒေတာတွေကို Resource ကနေ လာမယ့် ဒေတာတွေနဲ့ တူညီတဲ့ အပိုင်းတွေကို merge လုပ်မှာပါ။ ဒီအတွက် Resource မှာ `primary_key` ကို သတ်မှတ်ဖို့ လိုပါတယ်။

အသုံးပြုသင့်တဲ့ Write Disposition ကို ဆုံးဖြတ်နိုင်ဖို့အတွက် ကိုယ့်ကိုယ်ကို ဒီမေးခွန်းကို အရင် မေးရပါလိမ့်မယ်။ "ကိုယ် အသုံးပြုမယ့် ဒေတာက stateful လား stateless လား" ဆိုတာပါ။ Stateful ဆိုတာတော့ တစ်ခုနဲ့ တစ်ခု order of occurance ဆက်စပ်ပြီး ပြောင်းလဲလွယ်တဲ့ အခြေအနေကို ဆိုလိုပါတယ်။ ဥပမာ - Taxi App ငှားစီးတဲ့ အခြေအနေမှာ "booked" ကနေ "cancelled" ပြောင်းသွားတာမျိုး ။ Stateless ဆိုတာကတော့ ပြောင်းပြန် (ဒေတာတွေက order of occurance ပေါ် မူတည်ခြင်း မရှိပဲ) မပြောင်းလဲနိုင်တဲ့ အခြေအနေ - ဥပမာ - IoT sensor ကနေ သိမ်းဆည်းလိုက်တဲ့ logged events dataset မျိုး ကို ဆိုလိုပါတယ်။ အကျယ် ဖတ်ရန် - [Link](https://medium.com/@pradeeppaikateel/stateless-vs-stateful-data-engineering-8f96e0ab4fab), [Link2](https://www.freecodecamp.org/news/stateful-vs-stateless-architectures-explained/)





### Ref - ကိုးကားစာရင်း
- dlt Introduction by Cruxdata.co - [Link](https://cruxdata.co/blog/data_load_tool_dlt_introduction)
- 




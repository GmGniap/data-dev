### What's CI/CD?
- Continuous Integration (CI) ဆိုတာက Project တစ်ခုမှာ လူတိုင်းရဲ့ Pull Requests တွေကို merging မလုပ်ခင် Test စမ်းသပ်မယ့် စနစ် ဖြစ်ပါတယ်။
- Continuous Deployment (CD) ဆိုတာက approved ဖြစ်ပြီးတဲ့ changes တွေကို production ဆီ deploy လုပ်ပေးတဲ့ စနစ် ဖြစ်ပါတယ်။
- dbt project တစ်ခုမှာ CI/CD စနစ်တွေ က dbt pipeline testing နဲ့ deployment ပိုင်းကို automate အလိုအလျောက်ဖြစ်အောင် ပြုလုပ်ပေးပါတယ်။

### What's Slim CI?
အကယ်ရွေ့ သင့်မှာ Models ပေါင်း ရာဂဏန်းရှိတဲ့ dbt project တစ်ခု ရှိတယ် ဆိုပါစို့။ Team Member တစ်ယောက်က Models ၃ ခုနဲ့ သက်ဆိုင်တဲ့ changes တွေကို Pull Request အနေနဲ့ တင်လိုက်ပါတယ်။ သင့်အနေနဲ့ ဒီ အသစ်ပြင်လိုက်တဲ့ Models ၃ ခု နဲ့ သူတို့နဲ့ သက်ဆိုင်တဲ့ dependencies တွေကိုပဲ CI run သင့်တာပါ။ ဒီအခြေအနေမှာ သက်ဆိုင်တာတွေကိုပဲ ရွေးပြီး မသက်ဆိုင်တဲ့ ကျန် Model တွေကို ချန်ထားခဲ့ဖို့ ဘယ်လိုနည်းလမ်းနဲ့ လုပ်ရမလဲ။

Slim CI က ဒီ ပြဿနာကို ဖြေရှင်းပေးနိုင်ပါတယ်။ Slim CI အနေနဲ့က ပြောင်းလဲလိုက်တဲ့ code သီးသန့်ကိုပဲ မူတည် (refer) ပြီး running/testing လုပ်ခြင်းအားဖြင့် မလိုအပ်တဲ့ ကုန်ကျမှုတွေအားလုံးကို လျှော့ချပေးမှာ ဖြစ်ပါတယ်။


### References - ကိုးကားစာရင်း
- https://docs.getdbt.com/docs/deploy/continuous-integration
- https://docs.getdbt.com/blog/slim-ci-cd-with-bitbucket-pipelines
# Blue-Green Deployments
- Martin Fowler စတင်ခဲ့တဲ့ method တစ်ခု ဖြစ်ပါတယ်။ 

1. New code တွေကို production environment (blue) ရဲ့ copy version (green) ထဲကို deploy လုပ်ပါမယ်။
2. Deployed လုပ်လိုက်တဲ့ code ကို copy version (green) ထဲမှာ စိတ်ကျေနပ်တဲ့အထိ Testing လုပ်ပါမယ်။
3. Testing ပြီးဆုံးသွားတဲ့အခါမှာ green -> blue environment ကို ပြောင်းလဲပြီး (router လုပ်တယ်လို့လဲ Martin Fowler က သုံးပါတယ်) new code ကို deploy လုပ်မှာပါ။


အသေးစိတ်တွေကိုတော့ ဒီ Reference Links တွေမှာ ဆက်ဖတ်ရှုနိုင်ပါတယ်။
- https://martinfowler.com/bliki/BlueGreenDeployment.html
- https://datatonic.com/insights/blue-green-deployment-with-dbt-and-snowflake/

## Write-Audit-Publish
- Netflix Engineer Team ကနေ စတင်ခဲ့တဲ့ method တစ်ခု ဖြစ်ပါတယ်။
- [[#Blue-Green Deployments]] ကိုပဲ data ရှုထောင့်ကနေ implement လုပ်တယ်လို့ ပြောလို့ ရပါတယ်။

1. audit table ထဲက partition ထဲကို **Write** လုပ်ပါမယ်။
2. audit table ကို **Test** လုပ်မယ်။
3. ကျေနပ်တဲ့အခါ audit table ထဲက partition ကို production table နဲ့ **Swap** လုပ်ပါမယ်။

### Implementing WAP on BigQuery with dbt
- [[#Write-Audit-Publish]] method ကို BigQuery ပေါ်မှာ implement လုပ်ချင်တဲ့အခါမှာ အတားအဆီးတွေ ရှိပါတယ်။
1. BigQuery မှာ partition swapping လုပ်ပေးတဲ့ feature မရှိပါဘူး။
2. BigQuery မှာ zero-cost clones (ပိုက်ဆံမကုန်တဲ့ clone) မျိုး မရှိပါဘူး။

ဒါကြောင့် dbt ကို အသုံးပြုပြီး BigQuery ပေါ်မှာ WAP ကို fake ပုံစံမျိုး လုပ်ရပါတယ်။
1. **Write** - Audit schema/database ထဲကို ဒေတာထည့်တဲ့ DAG ကို dbt က run ပါမယ်။
2. **Audit** - Audit schema/database ထဲကို ဒေတာထည့်တဲ့ DAG ကို dbt နဲ့ test လုပ်ပါမယ်။
3. **Publish** - test လုပ်ပြီးသွားတဲ့ DAG (လိုအပ်တဲ့ အပိုင်းကိုပဲ) အသုံးပြုပြီး Production schema/database ထဲကို ဒေတာထည့်ဖို့ dbt က run ပါမယ်။
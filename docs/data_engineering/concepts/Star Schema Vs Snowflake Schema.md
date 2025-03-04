Star schema ရဲ့ dimension tables တွေက normalized မဖြစ်ပေမယ့် snowflake schema ရဲ့ dimension တွေကတော့ normalized ဖြစ်တယ်။ (ဒါကြောင့် snowflake schema ကို star schema ရဲ့ extended version လို့လဲ ပြောကြတယ်။ ရှိရင်းစွဲ star schema ရဲ့ dimension တွေကို normalized ဖြစ်အောင် ထပ်လုပ်လိုက်ရင် snowflake schema ရလာတာမျိုးမို့။)

normlized ဖြစ်နေတာမို့ Snowflake schemas တွေက dimension tables တွေကို သိမ်းဆည်းဖို့အတွက် နေရာ (space) သိပ်မလိုဘူး ။ ဒါပေမယ့် table လေးတွေ အများကြီး ဖြစ်နေတော့ လုပ်ကိုင်ရတာ ပိုတော့ ရှုပ်ထွေးတယ်။ ဒါပေမယ့် Snowflake schemas တွေမှာ redundant data (ထပ်ခါ ထပ်ခါ ပါဝင်နေတဲ့ ဒေတာ) တွေ မရှိတဲ့အတွက် ထိန်းသိမ်းဖို့ (Update/Delete/Insert) ပိုမိုလွယ်ကူတယ်။

Star schema တွေကတော့ fact table ကို အခြေခံပြီး dimension tables တွေကို Join လိုက်ရုံပဲဆိုတော့ ပိုပြီး ရိုးရှင်း၊မြန်ဆန်တဲ့ queries တွေ ခေါ်လို့ရတယ်။ 

ယေဘုယျအားဖြင့် Snowflakes schemas တွေက Data Warehouses တွေ  ပိုမိုအသုံးဝင်ပြီး star schemas တွေကတော့ data marts (သို့) reporting တွေမှာ ပိုမိုသင့်တော်တယ်။

### Regression Test
dbt data model တစ်ခု (existing object တစ်ခု) ကို အပြောင်းအလဲ လုပ်တဲ့အခါမှာ ဒီ ပြောင်းလဲမှုကြောင့် သူ့အပေါ် မှီခိုနေတဲ့ downstream objects တွေပေါ်ကို ဘာမှ သက်ရောက်မှု မရှိဘူးဆိုတာကို Test လုပ်တာမျိုးကို ဆိုလိုတာ။ များသောအားဖြင့် Non-Production environment မှာ test လုပ်ပီး ရလာတဲ့ result ပေါ် မူတည်ပီး Production အတွက် ready ဖြစ်/မဖြစ် ဆိုတာ ဆုံးဖြတ်ချက် ပေးနိုင်တယ်။


### Unit Testing Patterns
- dbt unit testing အတွက်က "model-inputs-output" pattern နဲ့ သွားပါတယ်။ သဘောကတော့ ဒီ _model_ ကို run တဲ့အခါမှာ ဒီ test _inputs_ တွေကို လက်ခံပြီး ဒီ _output_ ထွက်လာမယ် ဆိုပြီး မျှော်လင့်တဲ့ ပုံစံမျိုးပါ။
- Example - [Unit Test YAML](https://docs.getdbt.com/blog/announcing-unit-testing#unit-test-yaml)
- dbt မှာ မဟုတ်ပေမယ့် အခြားနေရာတွေမှာ အသုံးပြုလေ့ရှိတဲ့ Unit Testing Patterns တွေကတော့ 
	- Arrange-Act-Assert (AAA)
	- Given-When-Then (GWT)
	- 
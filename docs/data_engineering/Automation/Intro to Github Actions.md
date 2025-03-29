Github Actions ဆိုတာက Github ကနေ အခမဲ့ သုံးလို့ ရတဲ့ CI/CD platform တစ်ခု ဖြစ်ပါတယ်။ ကျနော်တို့ ရေးထားတဲ့ project တွေမှာ build , test နဲ့ deployment တွေ လုပ်တဲ့အခါမှာ အလိုအလျောက် လုပ်ဆောင်နိုင်ဖို့ ကူညီပေးပါတယ်။ [Github Actions](https://docs.github.com/en/actions/about-github-actions/understanding-github-actions) အကြောင်း နဲ့ [Usage Limit](https://docs.github.com/en/actions/administering-github-actions/usage-limits-billing-and-administration) အကြောင်းကို ဆက်ဖတ်ကြည့်စေချင်ပါတယ်။

### Github Actions - Theory

### Github Actions - YAML File
- YAML အကြောင်း [Official Documentation](https://docs.github.com/en/actions/writing-workflows/workflow-syntax-for-github-actions)
- [Learn YAML in Y minutes](https://learnxinyminutes.com/yaml/)

Github Actions တွေကို `.yaml` or `.yml` file ထဲမှာ workflow configuration တွေကို ရေးပါတယ်။ ဒီ YAML file တိုင်းကို project repository ထဲက `.github/workflows` location အောက်မှာ သိမ်းဆည်းရပါမယ်။ YML (or) YAML file တိုင်းမှာ အရေးကြီးတဲ့ Key Elements **၄ ခု** ပါဝင်ပါတယ်။ name, triggers, jobs နဲ့ steps တို့ ဖြစ်ပါတယ်။
- `name` ဆိုတာက ကျနော်တို့ workflow အတွက် နာမည် ကို ဆိုလိုတာပါ။ အကယ်ရွေ့ ကိုယ်က name မကြေညာခဲ့ဖူးဆိုရင် Github က repo file path ကို အခြေခံပြီး workflow filename ကို ဖော်ပြပါလိမ့်မယ်။
- triggers ဆိုတာက `on:` syntax ကို အသုံးပြုပြီး ရေးသားတဲ့ အပိုင်းပါ။ ဘယ်လို events တွေကို အခြေခံပြီး workflow ကို auto trigger လုပ်မလဲဆိုတာကို `on:` နဲ့ ကြေညာတဲ့ သဘောပါ။ Trigger လုပ်ဖို့အတွက် သုံးလို့ ရသမျှ events တွေအကြောင်း ကို ဒီ [official documentation](https://docs.github.com/en/actions/writing-workflows/workflow-syntax-for-github-actions#on) မှာ ဆက်ဖတ်နိုင်ပါတယ်။
	- ဥပမာ အားဖြင့် `push` ကို သုံးရင် new code ကို repo ထဲကို push လုပ်တဲ့အခါတိုင်းမှာ workflow ကို execute လုပ်မှာ ဖြစ်ပါတယ်။
	- `schedule` ဆိုရင်ကျ သတ်မှတ်ထားတဲ့ cron job အတိုင်း Timer ပေးထားသလိုမျိုး သတ်မှတ်ချိန် ရောက်တဲ့အခါမှာ workflow အလုပ်လုပ်ပါမယ်။
	- `workflow_dispatch` ကကျ repo ထဲမှာ button တစ်ခု တည်ဆောက်ပီး manual click နှိပ်ပီး workflow အလုပ်လုပ်လို့ ရအောင်ပါ။
- Workflow တွေ ကို **jobs** တွေနဲ့ တည်ဆောက်ထားပါတယ်။ (YAML ထဲမှာ `jobs:` syntax ကို အသုံးပြုပြီး ရေးသားတဲ့ အပိုင်းပါ။) **Jobs** တွေကိုလဲ **steps** တွေနဲ့ ဖွဲ့စည်းထားပါတယ်။

ဒီတော့ အပေါ်က အားလုံးကို ခြုံပြီး ပြန်ပြောရမယ် ဆိုရင် -
- event တစ်ခုခုကနေ Github Action workflow ကို trigger လုပ်ပါတယ်။ 
- Workflow တွေမှာ တစ်ခု (သို့မဟုတ်) တစ်ခုထက်ပိုတဲ့ Jobs တွေ ပါဝင်နိုင်ပါတယ်။ Jobs တစ်ခုချင်းဆီမှာလဲ sequence လိုက် လုပ်ဆောင်မယ့် steps တွေ ရှိပါတယ်။ 


### Github Actions - Secrets & Variables
- Secrets တွေက encrypted လုပ်ထားပြီး sensitive (လုံခြုံရေး အထူးစိုးရိမ်ရတဲ့) data အတွက် အသုံးပြုတယ်။ `${{ secrets.name }}` နဲ့ access လုပ်တယ်။
- Variables ကတော့ plain text သာ ဖြစ်ပြီး non-sensitive(လုံခြုံရေး ပူစရာမရှိတဲ့) data အတွက် အသုံးပြုတယ်။ variables တွေကို access လုပ်ဖို့အတွက် `vars` context ကို သုံးတယ်။
- Secrets မှာမှ Environment နဲ့ Repository secrets ဆိုပြီး ၂ မျိုး ထပ်ခွဲသေးတယ်။
	- Environment ကတော့ workflow ကို dev / testing / production စသဖြင့် environment ခွဲပြီး အသုံးချဖို့ပါ။ 
	- Repository ကတော့ ဒီ project repo မှာ အသုံးပြုဖို့ပါ။
		- personal repo မှာဆိုရင် repo secrets create လုပ်ဖို့အတွက် owner ဖြစ်ဖို့ လိုပါတယ်
### To Learn
- What's Github actions/checkout? [Link](https://spacelift.io/blog/github-actions-checkout)

### References
- https://innerjoin.bit.io/making-a-simple-data-pipeline-part-4-ci-cd-with-github-actions-733251f211a6
- https://towardsdatascience.com/automating-data-pipelines-with-python-github-actions-c19e2ef9ca90/
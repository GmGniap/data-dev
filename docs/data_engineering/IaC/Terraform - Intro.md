### Terraform Block
- `terraform {}` block မှာ သင်ရဲ့ infrastructure ကို ထောက်ပံ့ဖို့အတွက် လိုအပ်တဲ့ provider တွေအပါအဝင် အခြားသော Terraform setting တွေ ပါဝင်ပါတယ်။ Provider တစ်ခုချင်းဆီမှာ optional hostname, namespace နဲ့ provider type တွေ ပါဝင်တဲ့ `source` attribute ပါဝင်တယ်။
- Terraform အနေနဲ့ provider တွေကို install လုပ်တဲ့အခါမှာ Terraform Registry ကို default အသုံးပြုတယ်။ 
- provider တစ်ခုချင်းဆီအတွက် version constraint သတ်မှတ်ချင်တယ်ဆိုရင် `required_providers` block ကို အသုံးပြုလို့ ရတယ်။ ဒီ `version` attribute က optional ဆိုပေမယ့် အသုံးပြုဖို့ recommand လုပ်ပါတယ်။ ဒါမှသာ Terraform အနေနဲ့ သင့်ရဲ့ configuration နဲ့ မကိုက်ညီတဲ့ version တွေကို install ပြုလုပ်ခြင်းမရှိအောင် ကာကွယ်ပြီးသား ဖြစ်မှာပါ။ အကယ်ရွေ့ version ထောက်ပံ့မပေးထားဘူးဆိုရင် Terraform က နောက်ဆုံးထွက် version ကို အလိုအလျောက် install မှာ ဖြစ်ပါတယ်။

### Provider Block
- `provider {}` block ကတော့ အသုံးပြုမယ့် cloud provider ကို ရွေးချယ်တဲ့နေရာ ဖြစ်ပါတယ်။ Provider တိုင်းက သင်ရဲ့ resources တွေကို create / manage လုပ်ဖို့အတွက် Terrafrom အနေနဲ့ အသုံးချတဲ့ plugin တွေလို့ ပြောလို့ ရပါတယ်။
- မတူညီတဲ့ cloud provider တွေကနေ မတူညီတဲ့ service တွေကို အသုံးပြုဖို့အတွက် Terraform မှာ multiple provider block တွေ များစွာ ဖန်တီးလို့ ရပါတယ်။

### Resources Block
- `resource {}` block ကတော့ သင့်ရဲ့ infrasturcture မှာ အသုံးပြုမယ့် components တွေကို ရွေးချယ်ဖို့ ဖြစ်ပါတယ်။ Resource တစ်ခုက physical (သို့) virtual component (ဥပမာ - AWS EC2 instance) ဖြစ်နိုင်သလို logical component (ဥပမာ - Heroku Application) လဲ ဖြစ်နိုင်ပါတယ်။
- `resource {}` block မှာ resource type နဲ့ resource name ကို ကြေညာတဲ့ string ၂ ခု ပါဝင်ပါတယ်။

### Terraform Command Flow
```YAML
## initialize directory
terraform init

## format and validate terraform configuration
terraform fmt
terraform validate

## create infra
terraform apply

## inspect
terraform show

## destory infra
terraform destory
```


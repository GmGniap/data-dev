Data preparation ပိုင်းကို Python နဲ့ အလုပ်လုပ်မယ်ဆိုရင် regex (Regular Expression) အကြောင်း မဖြစ်မနေ သိထားဖို့ လိုပါတယ်။ 

## Regex Search ()

String တစ်ခုထဲမှာ regex pattern ကို ဖြစ်နိုင်ချေရှိတဲ့ နေရာများအားလုံးကို ရှာဖွေရာမှာ အသုံးပြုတယ်။ ရှာတွေ့တဲ့အခါမှာ ပထမဆုံး match ဖြစ်တာကိုပဲ Match Object အနေနဲ့ return ပြန်မှာ ဖြစ်ပါတယ်။ ဥပမာ - "abbbacca" ဆိုတဲ့ စာလုံးထဲကနေ "a" ကို search function အသုံးပြုပီး ရှာတယ်ဆိုရင် ပထမဆုံး match ဖြစ်တဲ့ "a" တစ်လုံးထဲပဲ return ပြန်လာပါမယ်။ အကယ်ရွေ့ ရှိသမျှ match ဖြစ်သမျှ အားလုံးကို return ပြန်စေချင်တယ်ဆိုရင် re.findall() function မျိုးကို အသုံးပြုလို့ ရပါတယ်။

Search function က string တစ်ခုလုံးကို scan လုပ်သွားပီး regex pattern နဲ့ ကိုက်ညီတဲ့ ပထမဆုံး match ဖြစ်တဲ့ location ကို ရှာတဲ့ ပုံစံမျိုးပါ။ 

### Search Syntax
```
re.search(pattern, string, flags=0)
```





To Find out >>
What's zero-length match? Does it mean not matching at all? 
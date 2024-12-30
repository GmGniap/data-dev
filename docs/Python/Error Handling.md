
Python exception တွေကို အသုံးချဖို့အတွက် Exception classes တွေကို နားလည်ဖို့ လိုပါတယ်။ အဲဒီထဲမှာမှ အရေးကြီးဆုံး ၊ အဓိက အကျဆုံး အသက်သွေးကြော Exception Class ၂ မျိုး ရှိပါတယ်။

BaseException နဲ့ Exception Class တွေ ဖြစ်ပါတယ်။

### BaseException Class
- Python မှာ ရှိတဲ့ exception အားလုံး ရဲ့ base class ဖြစ်ပါတယ်။ 
- BaseExceptions တွေက များသောအားဖြင့် အရေးကြီးတဲ့ ထူးခြားတဲ့ အခြေအနေတွေနဲ့ ပတ်သတ်ပါတယ်။ (အလွယ်အားဖြင့် system control နဲ့ ပတ်သတ်တာမျိုးတွေပါ)
- ဒါကြောင့် မှားယွင်းပီး အသုံးပြုမိရင် program shutdown ဖြစ်တာမျိုးတွေ ၊ တနေရာရာ ချို့ယွင်းတာမျိုးတွေ ဖြစ်နိုင်ပါတယ်။
- BaseException ကနေ inheriting လုပ်ထားတဲ့ Example Exceptions တွေကတော့
	- KeyboardInterrupt
	- SystemExit
	- GeneratorExist

### Exception Class
- user က ကြေညာထားတဲ့ exceptions တွေ နဲ့ Python မှာ built-in ပါတဲ့ exceptions တွေ အားလုံးနီးပါးရဲ့ base class ဖြစ်ပါတယ်။ System (သို့) Interpreter နဲ့ ဘာမှ မသက်ဆိုင်တဲ့ exception တွေ အတွက် ပါ။
- user က custom အသုံးပြု ကြေညာချင်တဲ့ exceptions တွေအားလုံးက Exception Class ကနေ inherit ပြုလုပ်ရပါမယ်။ ([PEP-8](https://peps.python.org/pep-0008/) မှာ recommand ပြုလုပ်ထားပါတယ်။)

# Handling Exceptions 

- Use `try - except - finally` block. 
## Raising Exceptions
- Use `raise <ExceptionName>` block.

# Vertical Scaling

- ဥပမာ အနေနဲ့ ပြောရမယ်ဆိုရင် သင့်မှာ Gaming Desktop Computer တစ်လုံး ရှိတယ်။ အဲဒီ Computer အတွက် အသစ်ထွက်တဲ့ Graphic Card တွေ Cooling System စသဖြင့် ဝယ်ယူပြီး အဟောင်းတွေ အစားထိုး လဲလှယ်တာမျိုး။ ရှိပြီးသား hardware တွေကို ပိုမိုကောင်းမွန်တဲ့ performance ရဖို့အတွက် hardware အသစ်တွေ ၊ ပိုကောင်းတဲ့ အမျိုးအစားတွေနဲ့ အဆင့်မြင့်တင်တာမျိုး။ ဒါမျိုးကို vertical scaling လို့ ခေါ်ပါတယ်။
- Vertical Scaling မှာ Single Node တစ်ခုထဲ ရှိပါလိမ့်မယ်။
- အားသာချက်
	- ရေးရန်
- အားနည်းချက်
	- ရေးရန်

### Vertical Scaling in Docker
Docker မှာဆိုရင် container specification ကို ပြုပြင်ပြောင်းလဲတာမျိုးနဲ့ vertical scaling လုပ်လို့ ရပါတယ်။ ဥပမာ - memory limit (သို့) CPU quota ကို တိုးတာမျိုး ၊ Single Host Machine ထဲကိုမှ container တွေ အများကြီး ထပ်ထည့်တာမျိုး။ 
Docker မှာ run နေတဲ့ container တစ်ခုက memory ပိုလိုလာတဲ့အခါမှာ တိုးလာတဲ့ ဝန်အားကို memory limit မြင့်တင်ပြီး ကိုင်တွယ်လို့ ရပါတယ်။ 
```cmd
docker run --memory=2g <container_name>
```

ဒါပေမယ့် vertical scaling အတွက်လဲ ကန့်သတ်ချက်တွေ ရှိပါတယ်။ ပထမကတော့ Host Machine ရဲ့ ရှိပြီးသား ရင်းမြစ် ကန့်သတ်ချက်ပါ။ အကယ်၍ machine က ၎င်းရဲ့ အမြင့်ဆုံး စွမ်းအား capacity နဲ့ run နေပြီးသား ဖြစ်နေရင် အဲဒီအပေါ်ကို ထပ်ဆောင်း resources တွေ ထည့်ဖို့/upgrade လုပ်ဖို့ဆိုတာ မဖြစ်နိုင်ပါဘူး။ ဒါ့အပြင် စျေးလဲ ကြီးနိုင်ပါတယ်။ ဘာကြောင့်လဲဆိုတော့ ရှိပြီးသား machine အပေါ် ကို ထပ်ခါ ထပ်ခါ upgrade လုပ်ရတာမျိုး ဖြစ်တဲ့အတွက် အချိန်အရရော ငွေကြေးအရပါ ပိုမိုကုန်ကျနိုင်ပါတယ်။

# Horizontal Scaling
- ဥပမာ အနေနဲ့ကတော့ Computer တွေ အများကြီးကို ဝယ်လိုက်တာမျိုးပါပဲ။ ရှိပြီးသား ရင်းမြစ်တွေထဲကို component တွေ လဲရုံ/upgradeလုပ်ရုံ မဟုတ်တော့ပဲ နောက်ထပ် စက်အသစ်တွေ ထပ်ထပ်ပေါင်းတာမျိုးပါ။ ဒါမျိုးကို Horizontal scaling လို့ ခေါ်ပါတယ်။
- Horizontal Scaling မှာတော့ Nodes တွေ အများကြီးရှိပြီး တစ်ခုနဲ့တစ်ခု network ပုံစံ ဆက်သွယ်ထားကြပါတယ်။(Cluster of Nodes လို့ ခေါ်ပါတယ်။)

### Advantages
- အကန့်အသတ်မဲ့ scaling လုပ်နိုင်ခြင်း။ 
- အမှားခံနိုင်ရည် ပိုမို ရှိခြင်း။
- Maintenance ကာလအတွင်းမှာ downtime အချိန် နည်းပါးခြင်း။
- ပိုမိုသေးငယ်တဲ့ system များ ဖြစ်သွားတဲ့အတွက်ကြောင့် ထိန်းသိမ်းရ လွယ်ကူခြင်း။
- အလွယ်တကူ Upgrade ပြုလုပ်နိုင်ခြင်း။
- Vertical Scaling နှင့် ရေရှည် နှိုင်းယှဥ်ရင် ကုန်ကျစရိတ် သက်သာခြင်း။
- Comparison - ![[Pasted image 20241111155408.png]]

### Disadvantages
- Architecture ပိုမို ရှုပ်ထွေးခြင်း။ 
- စက်အများအပြားအတွက် Software , Licensing , Operating ကုန်ကျစရိတ်များ ပိုမိုများပြားခြင်း။
- လုံခြုံရေး 
- Comparison - ![[Pasted image 20241111155508.png]]
### Horizontal Scaling in Docker




# References
- Docker Scaling - Vertical vs Horizontal - [Link](https://medium.com/@tranan.aptech/docker-scaling-vertical-vs-horizontal-d6681f45af04)
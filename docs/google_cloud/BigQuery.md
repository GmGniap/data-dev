
A partitioned table is a table divided to sections by partitions. Dividing a large table into smaller partitions allows for improved performance and reduced costs by controlling the amount of data retrieved from a query.  

Partitioned table ဆိုတာက အကန့်လိုက် အပိုင်းလိုက် ခွဲခြားခံလိုက်ရတဲ့ table ကို ဆိုလိုတယ်။ ကြီးမားတဲ့ table ကို သေးငယ်တဲ့ အစိတ်အပိုင်းလေးတွေ (table အသေးစားလေးတွေ) အဖြစ် ခွဲခြားလိုက်တဲ့အခါမှာ query တစ်ခုဆီကနေ ခေါ်တဲ့ data ပမာဏ ကို ထိန်းချုပ်လို့ ရသွားပီး performance အရရော ၊ cost ကုန်ကျစရိတ်အရရော သက်သာသွားတယ်။
  
Clustering sorts the data based on one or more columns in the table. The order of the clustered columns determines the sort order of the data. Clustering can improve the performance of certain types of queries, such as queries that use filter clauses and queries that aggregate data.

Clustering ဆိုတာကကျတော့ table အတွင်းမှာ ရှိတဲ့ တစ်ခု (သို့) တစ်ခုထက် ပိုတဲ့ columns တွေကို အခြေခံပြီး ဒေတာကို sort (အစီအစဥ်တကျဖြစ်အောင် ပြုလုပ်)လိုက်တာမျိုး။ Clustered columns တွေရဲ့ အစဥ်လိုက် order ကနေ ဒေတာအတွက် sort order ကို ဆုံးဖြတ်ပေးတယ်။ Clustering ပြုလုပ်ခြင်းအားဖြင့် ထူးခြားတဲ့ ဝိသေသရှိတဲ့ queries (ဥပမာ - filter clauses ကို အသုံးပြုတဲ့ queries မျိုး ၊ Aggregate data ကို queries လုပ်တာမျိုး) တွေမှာ performance ပိုကောင်းအောင် လုပ်ပေးနိုင်တယ်။ 
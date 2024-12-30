# Architecture
- Chunk - Hadoop မှာ သိမ်းထားတဲ့ ဒေတာတွေအားလုံးကို သေးငယ်တဲ့ အစိတ်အပိုင်းလေးတွေအဖြစ် ခွဲလိုက်တယ်။ (into smaller 'chunk')
- Chunks တွေကို 'block' လို့လဲ ခေါ်တယ်။ 
- Block size ကို (default အနေနဲ့ ? ) 128MB သတ်မှတ်တယ်။ 
	- အရင် version အဟောင်းတွေမှာက 64MB ဖြစ်နိုင်တယ်။ 
	- Chunks တွေကို ဖိုင်ဆိုဒ် နဲ့ သတ်မှတ်ပြီးခွဲလိုက်တာမျိုး ။ ဒါပေမယ့် ဘယ်ဒေတာက ဘယ် chunk/block ထဲမှာ ပါသွားသလဲ ဆိုတာ ဘယ်လို သိနိုင်သလဲ?
	- များသောအားဖြင့် chunks ခွဲတဲ့နေရာမှာ ၃ ခု ခွဲလေ့ ရှိတယ်။ 

## Master Node
- Metadata တွေပဲ သိမ်းတယ်။
- Data nodes တွေနဲ့ communication လုပ်ဆောင်တယ်။

- ဥပမာ - စာအုပ်တစ်အုပ်အနေနဲ့ စဥ်းစားရင် Table of content မာတိကာ က 'master node' ဖြစ်တယ်။ စာအုပ်ထဲက စာတရွက်ချင်းဆီ 'data node' ဖြစ်တယ်။ စာတရွက်ချင်းဆီမှာပါတဲ့ အကြောင်းအရာ content တွေက 'actual data' ဖြစ်တယ်။ 
![[Pasted image 20241116124907.png]]


## HDFS Write Algorithm

1. Application initiates the write request. Sends file name and data to HDFS Client
2. Client sends a request to master providing the file name and block indexes that need to be written
3. Master responds back with a list of servers where data should be written. Master responds back with 3 nodes. One of them is designated as primary and the other two are secondary nodes
4. Client pushes the data to all 3 nodes of the cluster as provided by the Master node, improving network bandwidth. Each client buffers data
5. Client sends a write command to the primary. Primary breaks the data into a specific sequence
6. Primary informs both secondary HDFS nodes to break their copy of the data using exact same sequence
7. Both secondaries commit the data to their disks and make it persistent. Informs primary
8. After receiving the acknowledgment from both secondaries, primary commits itself and sends a response back to HDFS Client
9. HDFS client in turn informs the application.

Two-Phase Commit Protocol - [Read](https://medium.com/@stoic-programmer/the-two-phase-commit-protocol-ensuring-distributed-transaction-consistency-46d0239761dbhttps://medium.com/@stoic-programmer/the-two-phase-commit-protocol-ensuring-distributed-transaction-consistency-46d0239761db) - it ensures that either all nodes commit or all nodes abort.

HDFS was originally designed based on the following assumptions:

- Hardware failure: Fundamental assumption of cluster designs, as you add more nodes, you increase the chance of failure.
- Streaming Data access: Hadoop HDFS is mainly designed for batch processing (as opposed to interactive usage by users). Focused more on high throughput of data access rather than low latency of data access.
- Large Datasets: A file in HDFS is of size ranging from gigabytes to petabytes. The architecture of HDFS should be design in such a way that it should be best for storing and retrieving huge amounts of data.
- Simple Coherency Model (write once read many): Once the file is created, written, and closed, it should not be changed.
- Moving Computation is cheaper than moving Data: Reading data over a network is slower than disk, and the disk is slower than RAM. Having an application do computations nearer the data increases throughput
- Portability: should be portable from one platform to another
# References
- HDFS Read & Write - [link](https://mukul54.github.io/post/hdfs/)
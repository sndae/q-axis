# Introduction #

裝好機器, 灌好程式後, 打開multiWiiconfig的程式時, 這時根據你用的遙控器廠牌不同, 各搖桿對應的方向跟大小可能會跟multiWii不太一樣, 這裡我們要講一個在時做上比較方便的做法, 來將你的搖桿方向跟大小, 中立點跟multiWii相配合


# Details #

**首先,請將飛控板上的ESC接頭都拔起, 因為在調教時,我們有可能不小心arm了motor,有打傷自己的可能, 請裝接收就好, 使用5V供電, 把系統經由FTDI連上PC的MultiWiiConfig**

**藉由multiWiiConfig的幫助,我們總共有三大件事要做
  1. 搖桿的方向(ch1~ch4)
  1. 中立點
  1. 最高點, 跟最低點**

https://lh6.googleusercontent.com/-1XlnqJTlXEQ/TyaP8WO-x8I/AAAAAAAAA_Y/kW0ijd-8Wys/w405-h288-k/wiiconfig.JPG

# 搖桿的方向 #
> 如何辨別搖桿的方向對不對?拿起遙控器,注意看到multiWiiconfig,上的淡藍色的bar, 搖桿推的方向,**應該要跟bar移動的方向一致....**如果不一樣, 請用遙控器裏的REV function去更改..Aux1跟Aux2可以隨自己的喜好去做....
可以觀察一下, 當搖桿往右(YAW/ROLL)或往上(PITCH/THR)時, 數值是變大的...


# 中立點 #
multiWii裏的code是可以調整中立點的, 但是既然遙控器的\*sub trim**這麼好用, 又何必去改code呢...
請用sub trim 去調整中立點, 讓中立點都在\*1500** 的位置. 最好連Aux1/Aux2也一起調到1500, 因為他的切換有時是三段的, 不調到1500, 容易誤判....

有時數值會在1500附近, 每窯一次搖桿, 數值都不會一樣, 這個沒關係, 也不是你的遙控器壞了, 而是arduino內建的timer設定所造成的誤差...只要數值在1500附近, 多個4us少個4us是沒問題的...

# 最高點跟最低點 #
MultiWii裏, 對油門的最低點是可以由code改的, 不過各channel的最大最小值好像不可以調...所以這裏我們要用\*EndPointAdjustmet**來把各channel(1~6)都調在\*最小值=1095 最大值=1905**

把要調的搖桿推到最大值, 調整你的EPA, 讓他約在1905, 稍微大一點無所謂, 原因跟中立點的值一樣, arduino的timer設定是有約4us的誤差, 我們可以讓值稍大一些...
調整最小值時, 就把搖桿推到最低, 調整EPA,略低於1095也可以

原則上 這三件事做完應該就OK了...
我們可以是是一些組合動作, 來看看是不是有調好....
例如油門到底後, yaw打右到底, 這時LED應該會亮起, 表示motor已經Arm了....
再把yaw打左到底, 這時LED應該會熄, 代表disarm.

MultiWii理有相當多的組合動作, 例如, arm motor, Acc calibation, Gyro calbration, Acc trim...etc. 一開始會覺得相當混亂, 習慣後就覺得非常好用...
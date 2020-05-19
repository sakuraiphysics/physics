# 有効数字

　ここでは，科学において数値を正しく表現するための有効数字について記す．



## 物理量の測定と有効数字の必要性

　まず，物理における値について確認し，それを表現するための有効数字のルールを提示する．



### 測定値

　これを読んでいる君たちの手元に，適度な長さの定規と，糸や紐はあるだろうか．無ければリボン状の紙やテープなどでもよい．それも用意できない，例えば移動中にこれを読んでいるならば，頭の中で実験するイメージをしてみよう．

　ここでは糸があったものとする．その糸を適当な長さに切り，その長さを測ってみよう．切った糸をまっすぐになる程度に引き，テープや重石で固定して定規で長さを測れば，精度よく測定できそうだ．

　私たちが糸の長さや，汲んだ水の質量，部屋の気温や湿度，電池の起電力，音の大きさや高さなど，今ある物理量について**値を知りたければ計測・測定するしかない**．逆を言えば，そのような値が分かっているとすれば，それは測定されたから明らかになっていると考えるべきである．このように測定されて判明した値のことを**測定値**という．

　ちなみに，測定せずとも値が分かっているのは，以下のような場合だけである．

- その値が単位系をつくる定義値である場合．例えば真空中の光速度 $c=299\,792\,458\mathrm{m/s}$ など．
  （その他，プランク定数，ボルツマン定数，電気素量，アボガドロ定数など）
- その値が（主に数学的な）定義から明らかである場合．
  例えば円周率$\pi=3.14159265...$ ，$\sqrt{2}=1.41421356...$ ，三角形の面積を求める際の $\times\frac{1}{2}$ など．



### “意味がある” 桁や位はどこまで？

　一般的に最小目盛が $1\,\mathrm{mm}$ の定規で長さを測るとき，最小目盛の $\frac{1}{10}$ まで読むこととされている．糸の話の続きに戻るが･･･測定の結果，糸の長さは $15\,\mathrm{mm}$ と $15.1\mathrm{mm}$ の間にあり，その隙間を $1:9$ に分かつ点であるように見えたことから， $15.1\,\mathrm{mm}$ と示したとする．しかし，単にそう表したとき，一つ問題が生まれる．数学的には
$$
15.1\,\mathrm{mm}=15.10000000000\cdots\,\mathrm{mm} \tag{1}
$$
である．しかし，実際には小数第二位以下の値は「わからない」はずだ．概念的に表記するなら，
$$
15.1\,\mathrm{mm}=15.1??????????\cdots\,\mathrm{mm} \tag{2}
$$
とするべきであろう．

　さて， $15.1\mathrm{mm}$ と書いたときに，(1)であるか(2)であるか判別できないというのは，測定値を表す上でとっても困る．「小数第2位以降も0だと判明している」と「小数第2位以降はわからない」は，異なる測定事実を意味するからだ．

　だから，物理を含め科学全般では，測定値を (2) のように扱えるルールを採用している．つまり「測定値において $15.1\mathrm{mm}$ と示したら，測定された意味のある数字は15.**1**までで，それ以下の位は分からないものとして取り扱うこと」としている．このような値の扱いを**有効数字**という．有効数字は，測定値および測定値を用いて導かれた計算値を，意味がある桁・位を含めて表すのに必須である．

　**有効数字で $15.1$ とした場合，$15.05$ から $15.15$ の間のどこかであることを意味する．**

　なお，測定値でない場合は，有効数字を考慮する必要はない．定義値は，そもそもその値を基準に単位系が決まっているから不確かさのない値として扱われるし，数学的な定義からくる量も測定などによらず値がはっきりしているため，既知の値を何桁まででも，極端なことを言えば無限に採用してよいことになる．



誤差と不確かさ



### まとめると

- 測定値は，測定条件や測定器によって決まる，ある桁・位までしか分からない．有限桁の値になるよね．
- 測定値や，測定値から導かれた計算値について，末尾がどこまで判明しているのかを一意に示せるようにするために，有効数字を考慮して表現・計算すべきだよ．
- 定義値や数学的な定義からくる量に曖昧さはなく，どこまでも明らかな値として扱うため，有効数字を考慮する必要はないよ．



## 有効数字の扱い方

　次に，有効数字で示された値について有効桁をどこまでとするか，計算後の値について有効桁がどこまでか，細かく確認していく．



### 有効数字における有効桁と科学的記数法

　有効数字における有効桁の扱いは以下の通りである．（傍点を打ってあるところが有効桁）

- $15.1$ であれば $\dot{1}\dot{5}.\dot{1}$， $1.24$ であれば $\dot{1}.\dot{2}\dot{4}$ ，$103$ であれば $\dot{1}\dot{0}\dot{3}$ 
- $5.0$ は $\dot{5}.\dot{0}$ ，$123.000$ は $\dot{1}\dot{2}\dot{3}.\dot{0}\dot{0}\dot{0}$ 
  - 末尾の0はわざわざつける0であり，そこが0であることがわかっていることを意味する有効数字．
- 1未満の値について，$0.54$ であれば $0.\dot{5}\dot{4}$ ，$0.0865$ であれば $0.0\dot{8}\dot{6}\dot{5}$ ，$0.0500$ であれば$0.0\dot{5}\dot{0}\dot{0}$ 
  - 頭に付く0は位取りを表記するための0であり，有効とは考えない．単位変換についても， $0.0\dot{8}\dot{6}\dot{5}\,\mathrm{mm}=0.0000\dot{8}\dot{6}\dot{5}\,\mathrm{m}$ ， $0.0\dot{8}\dot{6}\dot{5}\,\mathrm{mm}=\dot{8}\dot{6}.\dot{5}\,\mathrm{\mu m}$ と考えるべきである．

　では，$1200$ はどうか．$\dot{1}\dot{2}00$ とするか，$\dot{1} \dot{2} \dot{0} \dot{0}$ とするか･･･．注意せよ．**このように末尾に0がつく整数で測定値などを表すのは，曖昧で望ましくない表記なので，やらないことを強く推奨する．**このような場合は，

- $1.2\times10^2$ であれば $\dot{1}\dot{2}00$ 
- $1.200\times10^2$  であれば $\dot{1} \dot{2} \dot{0} \dot{0}$

と書く．このように，有効桁を示した基数と指数の積で表す指数表記で示すことを**科学的記数法**という．



### 有効数字の計算法

（※セミナーp.2～3にも記述あり．そちらも参照すること．）

　全ての物理量が直接測定できるわけではない．そのため，測定値から計算して目的の量を導出する場合がある．有効数字を計算する場合，以下のルールに従う．



#### 1．足し算・引き算

　足し算・引き算の計算結果は，有効桁の末位を，最も末位の高いものに合わせるように丸める．

例）ロープAの長さを測定したら$12.3\,\mathrm{m}$ ，ロープBの長さを測定したら $2.34\,\mathrm{m}$ であった．このロープAとロープBをくっつけた長さを計算する．

　$12.3\,\mathrm{m}+2.34\,\mathrm{m}=14.64\,\mathrm{m}$ 　　Ans. $14.6\,\mathrm{m}$
$$
\begin{align}
12&.3? \\
+\;\;2&.34 \\
\underline{\;\;\;\;\;\;\;\;}&\underline{\;\;\;\;\;\;\;\;} \\
14&.64 \\
&\;\,(?)
\end{align}
$$
　つまり**位を見て，最も大ざっぱな位に合わせる**ということである．値のわからない位は計算後もわからないから，計算結果の $14.64$  において，小数第2位の $4$ は本来わからない位なので，丸めて $14.6$ とする．



#### 2．かけ算・わり算

　かけ算・わり算の計算結果は，有効桁数を，最も有効桁の少ないものに合わせるよう丸める．

例）ある長方形の紙がある．縦の長さを測定したら $21.0\,\mathrm{cm}$ ，横の長さを測定したら $29.7\,\mathrm{cm}$ であった．この紙の片面分の面積を計算する．

　$21\,\mathrm{cm}\times 29.7\,\mathrm{cm}=623.7\,\mathrm{cm^2}$　　Ans. $6.2\times10^2\,\mathrm{cm^2}$

　つまり**桁数を見て，最も少ない桁数に合わせる**ということである．この計算は有効桁数が2桁と3桁のかけ算なので，計算結果の有効桁数は2桁になる．上から2桁を有効として表現すると $620$ となるが，誤解を招く表現なので必ず科学的記数法にして $6.2\times10^2$ と表す．



#### 3．計算過程における丸め

　計算過程において，あまりに桁数が多くても無駄である．結果的に丸められてしまう桁を詳細に計算しても意味がない．

例）ある長方形の紙がある．測定により，縦の長さは $21.0\,\mathrm{cm}$ ，横の長さは $29.7\,\mathrm{cm}$ ，厚さは $0.013\,\mathrm{cm}$ であるとわかった．この紙の体積を計算する．
$$
\begin{align}
21\,\mathrm{cm} \times 29.7\,\mathrm{cm} \times 0.013\,\mathrm{cm}&=623.7\,\mathrm{cm^2}\times 0.013\,\mathrm{cm} \\
&=624\,\mathrm{cm^2}\times 0.013\,\mathrm{cm}\tag{*} \\
&=8.112\,\mathrm{cm^3}
\end{align}
$$
Ans. $8.1\,\mathrm{cm^3}$

(*)とした行に注目してほしい．$21\,\mathrm{cm} \times 29.7\,\mathrm{cm}$ を有効数字を考慮して計算すると有効桁数は2桁となるが，計算途中であるため，1桁多い3桁に丸めている．毎回の計算結果を有効数字まで丸めてしまうと，計算の精度が下がってしまう．そうならないように，一般的に**計算過程においては，有効桁数+1桁まで丸めながら計算を進めてもよい**ことになっている．（もちろん，+2桁でもよいし，関数電卓などが使える環境なら，計算過程での丸めはしないでもよい．）



#### 4．有効数字ではない値との計算

　有効数字でない値は，有効桁数は実質無限であるとしてよいが，やはり桁数がむやみに多くても無駄である．そのため，一般的に**計算する測定値の桁数よりも1桁多くとる**．

例）円形に切り抜かれたアルミニウム円盤がある．表側の面を上にして半径を測ったところ， $9.80\,\mathrm{cm}$ であった．この表側の面積を求めよ．
$$
\begin{align}
S &= \pi r^2 \\
&=3.141 \times (9.80)^2 \\
&=3.141 \times 96.04 \\

&=301.6
\end{align}
$$
Ans. $302\,\mathrm{cm^2}$

この場合，円周率 $\pi$ とかけ算をする数値は有効桁数が3桁であるため，円周率はそれより1桁多い4桁をとり， $\pi=3.141$ として計算する．



#### 5．足し算・引き算による有効桁数の変化

　足し算や引き算では，有効数字のルールに則って計算すると有効桁数が増減することがある．

例1）ブロックAとブロックBがある．それぞれのブロックの幅を金尺で測定したところ，Aの幅は $50.0\,\mathrm{cm}$ ，Bの幅は $60.0\,\mathrm{cm}$ であった．くっつけたときの幅はいくつか．

　$50.0\,\mathrm{cm}+60.0\,\mathrm{cm}=110.0\,\mathrm{cm}$ 　　Ans. $110.0\,\mathrm{cm}$

例2）デジタル温度計で気温を測定したら $20.0\,^\circ\mathrm{C}$ だった．数分後に再測定したら $20.7\,^\circ\mathrm{C}$ だった．温度差は？

　$20.7\,^\circ\mathrm{C}-20.0\,^\circ\mathrm{C}=0.7\,^\circ\mathrm{C}$　　Ans. $0.7\,^\circ\mathrm{C}$

　これらは，正しい有効数字の計算である．例1では，もともと3桁の有効数字であったのが4桁に増加した．しかし例2では，もともと温度が3桁まで分かっていたのに，温度差を計算したら有効桁数が1桁に減少した．特にこのように有効桁が減少することを**桁落ち**という．実験や測定を計画する際には，明らかにしたい値が，桁落ちによって曖昧な計算値しか得られないようなことのないよう，注意して実験法や測定器を選定する必要がある．



#### 6．誤差の伝播を考慮した有効桁数の決定

　不確かさの分析・表記を行わない場合，誤差の伝播を考慮して有効桁数を決めたほうがよいことがある．

例1）試薬瓶からピペットで液体Xを $2.0\,\mathrm{ml}$ だけ測り取り，ビーカーに移す．これを10回繰り返した．ビーカーに取り出された液体Xの体積として正しいのはどちらか．

- 計算法1． $2.0+2.0+2.0+2.0+2.0+2.0+2.0+2.0+2.0+2.0=20.0$ 　　Ans. $20.0\mathrm{ml}$ 

- 計算法2．$2.0 \times 10 = 20$ 　　Ans. $20\,\mathrm{ml}$ 

  　どちらも有効数字の計算ルールは踏襲しているが，正しくは，計算法2で導出された $20\,\mathrm{ml}$ である．1回に移す量が$1.95\,\mathrm{ml} \sim 2.05\,\mathrm{ml}$ であったとすると，10回操作を繰り返した後に取り出された液体Xの体積は最小で $19.5\,\mathrm{ml}$ ，最大で $20.5\,\mathrm{ml}$ である．このように，有効数字で許容している誤差範囲が積み重なっていくことを考慮しないといけない．

例2）試薬瓶からビーカーAに液体Xを10.0mlだけ測り取った．ここにさらに試薬瓶からピペットで液体Xを $2.0\,\mathrm{ml}$ だけ測り取り，ビーカーAに移す．これを5回繰り返した．その後，ビーカーAからピペットで液体Xを $2.0\,\mathrm{ml}$ だけ測り取り，捨てる．これを5回繰り返した．ビーカーAにある液体Xの体積はいくらか．

　答えは $10\,\mathrm{ml}$ である．特に条件のない限り，誤差は両側に現れうると考えるべきである．すなわち，5回入れるときに多く，5回捨てるときに少なく取ってしまった場合に，ビーカーAにある液体Xの体積は最も多いことになる．ビーカーAにある液体Xの量は，最小で $9.5\,\mathrm{ml}$ ，最大で $10.5\,\mathrm{ml}$ と考えるべきである．

　このような理由から，実際に測定方法を選ぶ場合に置いても，できるだけ誤差の伝播が起こらない方法を採用すべきである．例えば，点 A，B，C，D，E，F，G，H，I，J，K の順に一直線に並んでいるとして，点AK間の距離を測定したい時に

- 点 AB，BC，CD，DE，EF，FG，GH，HI，IJ，JK 間の距離をそれぞれ測定し，それを全て足し合わせる
- 点 AK 間の距離を1回で測定する

どちらの方法がより精度よく測定できるだろうか．本項を熟読した諸君にとっては明らかであろう．



#### 7．その他

- 四則演算の計算順は，有効数字の計算においても一般的な計算順に従う．すなわち優先順位は，(  )内，累乗，乗除算，加減算，左から，である．
- 結合法則や分配法則など，同じ値を求めるにも計算の手順が異なる場合があるが，これにより計算結果の末尾の値がずれることがあるが，これは仕方ないことである．



### まとめると

- 有効数字，どこまで有効桁か判断できるようにね．
  つけざるを得ない位取りの $0$ は有効数字に含めず，わざわざつける末尾の $0$ は含めるよ．
- 科学的記数法を心がけようね．末尾に 0 がつく整数で示すのはやめよう．
- 足し算・引き算は**位を見て，最も大ざっぱな位に合わせる**ようにね．
- かけ算・割り算は**桁数を見て，最も少ない桁数に合わせる**ようにね．
- 計算は，少なくとも有効数字+1桁で進めよう．
- 他にも状況によって有効桁数は変化する可能性がある，実際に測定値を分析する際には注意しよう．



## 物理の演習問題等における値の取り扱い

　ここまでに記したとおり，本来は物理において計算である値を明らかにする場合，それがどのような測定に基づいているのかは重要な関心事である．しかし教科書や問題集などの演習問題では，そのあたりの設定は結構大ざっぱであることが多い．実際にある以下の演習問題を見てみよう．

- 軽い糸の一端を天井につけ，他端に重さ $2.0\,\mathrm{N}$ の小球をつなぐ．この小球に，ばね定数 $10\,\mathrm{N/m}$ の軽いばねの一端を取りつけ，他端を水平方向に静かに引いた．糸が鉛直方向と $60^\circ$ の各をなして小球が静止しているとき，ばねの自然の長さからの伸びは何 $\mathrm{m}$ か．（第一学習社　セミナー物理基礎+物理 2020 p.32 基本例題8）
- $x$ 軸状を正の向きに一定の速さ $3.0\,\mathrm{m/s}$ で運動している物体が，時刻 $0\,\mathrm{s}$ に原点Oを通過した．時刻 $0.80\,\mathrm{s}$ での物体の位置を求めよ．また，時刻 $3.0\,\mathrm{s}$ から $5.0\,\mathrm{s}$ までの間の物体の変位を求めよ．（啓林館　物理基礎 改訂版 p. 9 問5）

　1問目には「 重さ $2.0\,\mathrm{N}$ の小球」「ばね定数 $10\,\mathrm{N/m}$ の軽いばね」「糸が鉛直方向と $60^\circ$ の各をなして」，2問目には「一定の速さ $3.0\,\mathrm{m/s}$ で」「時刻 $0\,\mathrm{s}$ に原点Oを通過した」などと，測定値らしきものが記されている．これらの値がなぜ判明しているのかについて記述は無い．あくまで演習問題として作られた架空の設定ということなのだろう．しかし私たちはこれらの問題について「実際に実験したらどうなると予測できるだろうか」という視点を持って解いていくべきである．（そうでなければもはや自然科学ではない．物理ではない．）

　そう考えて読んでいくと，1問目については「 重さ $2.0\,\mathrm{N}$ の小球」は，ニュートン目盛のばねばかりで重さを測定したのかな，「ばね定数 $10\,\mathrm{N/m}$ の軽いばね」も同様に，ばねばかりなどを利用してばね定数を測定したのかな，「糸が鉛直方向と $60^\circ$ の各をなして」というのは分度器か，角度計を使用したのかなと想像できる．事前の測定について省略されているが，これは実際の実験を基にしているか，それに準じて作られた問題であろう．そうであれば，これらの値は測定値であるという想定のもと，有効数字の計算法で解いていくべきである．

　一方，2問目については「一定の速さ $3.0\,\mathrm{m/s}$ で」については，ほぼでもだいたいでもなく，一定の速さで進むものがあるだろうか･･･．また，「時刻 $0\,\mathrm{s}$ に原点Oを通過した」とあるが，時刻 $0\,\mathrm{s}$ はこの問題において定めたものであろう．これは演習問題とするために作られた抽象的な物理イメージ，思考実験，実験モデルの類いであると考えられる．このような場合には，有効数字で考える意義があるのかどうか微妙なところではあるが，やはりできるだけ自然科学の問題として捉えようというならば，「一定の速さ $3.0\,\mathrm{m/s}$ 」は測定値として，有効数字を考慮すべきであろう．ただ，「時刻 $0\,\mathrm{s}$ に原点Oを通過した」については，おそらく原点Oを通過した時点を時刻 $0\,\mathrm{s}$ として定めた（実際の操作としては，その瞬間にストップウォッチなどをスタートさせた）ということであろうから，有効数字を考慮する必要はない．（ストップウォッチを人が操作することによる誤差は，必要に応じて別に考慮・評価する必要はあるだろう．）



### まとめると

- 問題文内で提示した値は，全て有効桁数を考慮して記述された有効数字であるとして解く
- 「0」は題意から，問題の上で定めた0や理論上の0（有効数字でない）か，測定値の0（有効数字1桁）か判断する．（ほとんどの場合，有効数字ではない）
- その他，指示があればそれに従う

以上の原則に従って問題を解いていけばよいでしょう．ただ，実際の実験を想定することを忘れずにね！



## 	補記

### 丸めと四捨五入について

　数値の末尾を処理して，任意の桁までの記述に短縮することを「丸める」という．最も有名な方法は**四捨五入**で，$12.867$ を小数第1位で丸める場合，小数第2位が $6$ だから，四捨五入によって繰り上げて $12.9$ とする．四捨五入は，JIS Z 8401 にて規則Bとして規定され，正しい丸め操作とされている．

　ただ，四捨五入であると，両方の丸め先から等しく近いところにある場合，必ず切り上げ操作を行うことになる．（例えば小数第1位で丸める場合， $1.05$ ， $1.15$ ， $1.25$ ， $1.35$ ， $1.45$ ...や， $1.050$ ， $1.150$ ， $1.250$ ， $1.350$ ， $1.450$ ...は，全て$1.1$ ， $1.2$ ， $1.3$ ， $1.4$ ， $1.5$ ...に切り上げ）これによって測定値の平均や，丸め後の期待値がやや大きい値に偏る可能性がある．そこで，例えばJIS Z 8401 の規則Aでは，このような場合の丸め方法について，**偶数への丸め**を推奨している．

　偶数への丸めとは，両方の丸め先から等しく近いところにある場合，必ず末尾が偶数になるように切り上げまたは切り捨てを行うということである．（前述の $1.05$ ， $1.15$ ， $1.25$ ， $1.35$ ， $1.45$ ...や， $1.050$ ， $1.150$ ， $1.250$ ， $1.350$ ， $1.450$ ...は，$1.0$ ， $1.2$ ， $1.2$ ， $1.4$ ， $1.4$ ...とする．）

　基本的には四捨五入で事足りるが，測定値の有効桁数が不十分な中，四捨五入による誤差が大きく影響しそうな場合には，こういった丸め方を採用するとよい．



### 指数表示について

　例えば長さについて考える．私たちが科学で取り扱う長さには，大きいものから小さいものまで多様である．私たちのいる天の川銀河はおとめ座超銀河団に属するが，その中央にあるおとめ座銀河団と天の川銀河の距離は，およそ $590000000000000000000000\,\mathrm{m}$ であると知られている．翻って，水素原子内の電子が基底状態にある時の軌道半径はボーア半径と呼ばれ，およそ $0.000000000053\mathrm{m}$ であると分かっている．

　しかし，このように0を並べる記法では，読みづらいし書きづらい．物理における値で大事なのはオーダーであり，これが一目でわかるように表記したい．そのため，指数表示を採用する．具体的には，最高位が一の位で表される基数と，10の累乗で表される指数の積として表現する．これにより，先に示した銀河間の距離は $5.9\times 10^{23}\,\mathrm{m}$ ，ボーア半径は $5.3\times 10^{-11}\,\mathrm{m}$ と表される．



### 末尾に0がつく整数の有効桁

　散々やるなと念を押した，末尾に0がつく整数での表記（$1200$ とか）であるが，いざ文書でそれを見つけてしまったら，どう捉えればいいのか．一応，知る限りのことを記す．

- 日本では，教科書によって， $1200$ は $\dot{1} \dot{2} \dot{0} \dot{0}$ とすると記されたものと， $1200$ という書き方はそもそも推奨されないと記されたものがある．
- 日本では，いざ $1200$ に出会ってしまったら， $\dot{1} \dot{2} \dot{0} \dot{0}$ と読むのが多数派．
- $3.0 \times 10^1$ は読みづらいから $30$ と書いたほうがよいとしている教科書もある．
- だが，海外の物理の教科書で「$170 × 1.3 = 220$」と堂々と書いている例もある．
  これは，計算結果の $220$ を $\dot{2} \dot{2} 0$ と読むしかない． 

　以上より，本文内で示した通り，完全にこうだ！ というルールを示せない曖昧な状況であると言えよう．その値が計算結果で，そこまでの計算過程が記されているなら，そこから読み取って解釈もできるだろうが，測定値などでポッと $1200$ が出てきた時には，有効桁の判断のしようがない．



三角比・三角関数の有効桁数

　三角比・三角関数の有効桁数については，以下の通りとするのがよい．

- 基本的に有効数字2桁の角度における三角比・三角関数は，2桁まで有効とする．
  $\sin 30^\circ=0.50$ ，$\sin 45^\circ=0.71$ ，$\sin 60^\circ=0.87$ 
- 基本的に有効数字3桁の角度における三角比・三角関数は，3桁まで有効とする．
  $\sin 30.0^\circ=0.500$ ，$\sin 45.0^\circ=0.707$ ，$\sin 60.0^\circ=0.866$ 
- ただし，角度が $0^\circ$，$90^\circ$ などに近い場合は，有効桁数が変化する可能性があるので，有効数字の示す値の範囲を計算した上で妥当な桁に決定する．
  - 例1）$\sin 1^\circ$ 
    値域は $\sin 0.5^\circ=0.00872653...$ から $\sin 1.5^\circ=0.0261769...$ であり，有効な値を示しづらいが，$\sin 1^\circ=0.001$ と辛うじて言えなくもない．$\sin 1.0^\circ$ であれば， $\sin 0.95^\circ=0.0165798...$ から $\sin 1.05^\circ=0.01832...$ であるから，辛うじて$1.7$と書けるだろうか．
  - 例2）$\sin 89^\circ$ 
    値域は $\sin 88.5^\circ=0.999657...$ から $\sin 89.5^\circ=0.999961...$ であり，これは$0.999$という3桁か，$0.9998$という4桁で表せそうだ．

　三角関数に限らず，有効桁が分からない新しい関数が出てきた場合には，有効数字で示される値域で最小値・最大値を確認して有効桁を決定するのが，より誠実なやり方だろう．
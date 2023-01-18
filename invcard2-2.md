はたらく力を図示して、台Aと物体Bにはたらく力を考える。垂直抗力をNとして考える。

<img src="/Users/pastzwei/Library/Application Support/CleanShot/media/media_uwVN9C4wPi/CleanShot 2023-01-13 at 14.03.41@2x.png" alt="CleanShot 2023-01-13 at 14.03.41@2x" style="zoom:50%;" />

<img src="/Users/pastzwei/Library/Application Support/CleanShot/media/media_TexXDhvpEk/CleanShot 2023-01-13 at 14.05.29@2x.png" alt="CleanShot 2023-01-13 at 14.05.29@2x" style="zoom:50%;" />



台Aにはたらく正味の力は、水平右方向の力$F_A$であるから、台Aの加速度を$A_a$とすると、運動方程式は
$$
Ma_A=N\sin\theta
$$
物体Bにはたらく正味の力は、向きがわからんので、水平方向$F_{Bx}$と鉛直方向$F_{By}$の分力で考える。
$$
ma_{Bx}=N\sin\theta
$$

$$
ma_{By}=mg-N\cos\theta
$$

それぞれの加速度の導出は、これで終わり。

そうは言っても、垂直抗力Nは勝手に決めた文字なので、もう少し話は続く。(1)〜(3)だけでは、Nを求めるための条件が足りない。物体Bが台Aの上からすべり始めてから、台Aの下まで到達するのに$t$秒かかったとして、どのような運動をしたか考える。

<img src="/Users/pastzwei/Library/Application Support/CleanShot/media/media_hGYOBpHdIX/CleanShot 2023-01-13 at 14.06.34@2x.png" alt="CleanShot 2023-01-13 at 14.06.34@2x" style="zoom:50%;" />

その間に台Aが水平方向に移動した距離を$x_A$、物体Bが水平方向に移動した距離を$x_B$、鉛直方向に移動した距離を$y_B$とすると、
$$
\frac{y_B}{x_A+x_B}=\tan\theta
$$
の関係がある。（これが束縛条件）

A、Bにはたらく力は一定であり、両方とも初速度は0であるから
$$
x_A=\frac{1}{2}a_At^2,\;\;x_B=\frac{1}{2}a_{Bx}t^2,\;\;y_B=\frac{1}{2}a_{By}t^2
$$
であるから、(5)を代入すると、(4)の左辺は分母と分子で2分の1と$t^2$が消えて
$$
\frac{y_B}{x_A+x_B} = \frac{a_{By}}{a_{A}+a_{Bx}}
$$
であるから、(4)式は
$$
\frac{a_{By}}{a_{A}+a_{Bx}}=\tan\theta
$$
になる。これをうまいこと解いていきましょう。まず分数だと厄介なので平たくする。
$$
a_{By}=\tan\theta\cdot(a_{A}+a_{Bx})
$$
(1)〜(3)を代入する。
$$
g-\frac{N\cos\theta}{m}=\tan\theta\cdot(\frac{N\sin\theta}{M}+\frac{N\sin\theta}{m})
$$
移項と右辺カッコ内を通分
$$
g=\tan\theta\frac{N\sin\theta(M+m)}{Mm}+\frac{N\cos\theta}{m}
$$
両辺を$\tan\theta$でわる。一番右の項は $\tan\theta=\frac{\sin\theta}{\cos\theta}$を使う。
$$
\frac{g}{\tan\theta}=\frac{N\sin\theta(M+m)}{Mm}+\frac{N\cos^2\theta}{m\sin\theta}
$$
両辺に$Mm\sin\theta$をかける。左辺は $\tan\theta=\frac{\sin\theta}{\cos\theta}$を使う。
$$
Mmg\cos\theta=Nm\sin^2\theta+NM\sin^2\theta+NM\cos^2\theta
$$
右辺をくくって
$$
Mmg\cos\theta=N(m\sin^2\theta+M\sin^2\theta+M\cos^2\theta)
$$
$\sin^2\theta+\cos^2\theta=1$になって
$$
Mmg\cos\theta=N(m\sin^2\theta+M)
$$
だから
$$
N=\frac{Mmg\cos\theta}{m\sin^2\theta+M}
$$
である。Nが導出できたので、改めて(1)〜(3)に代入して加速度を求めると
$$
a_A=\frac{N\sin\theta}{M}=\frac{mg\sin\theta\cos\theta}{m\sin^2\theta+M}
$$

$$
a_{Bx}=\frac{N\sin\theta}{m}=\frac{Mg\sin\theta\cos\theta}{m\sin^2\theta+M}
$$

$$
a_{By}=\frac{mg-N\cos\theta}{m}=g-\frac{Mmg\cos^2\theta}{m^2\sin^2\theta+mM}
$$

ですね。



（別解）慣性力を使って解くと楽っぽい気がする。斜面上の物体Bについて、斜面に対して垂直な方向のつり合いの式を立てられる。
$$
N+ma_A\sin\theta=mg\cos\theta
$$
(1)式$N=\frac{Ma_A}{\sin\theta}$を代入してNを消去
$$
\frac{Ma_A}{\sin\theta}+ma_A\sin\theta=mg\cos\theta
$$
両辺に$\sin\theta$をかけて
$$
Ma_A+ma_A\sin^2\theta=mg\sin\theta\cos\theta
$$
$a_A$について整理すれば
$$
a_A=\frac{mg\sin\theta\cos\theta}{m\sin^2\theta+M}
$$
これは(16)式に同じ。あとは$\frac{M}{m}$かけたり、$\frac{\cos\theta}{\sin\theta}$かけたり、それを$g$から引いたりすれば残りも導出できる。
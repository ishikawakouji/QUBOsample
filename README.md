# Solve 2D equations using PyQUBO
I used to be into CAE field, I am interested in solving big linear equations.
And I want to it should be easier.

When I saw the quantum computing, it tries finite combination values in one time
and brings the best result, I think.

But qbit or spin are just 2 values 0 or 1. It is far from
usual floating point values. It is difficault .....

# Approximation and not perfect
I have an idea. 2-dimensional x and y are following relation.

Mx = y

I replace the result x to array A, vector v and scalar c.

M(cAv) = y

It means some v rotated by A and x are parallel. And 
M(Av) and y are parallel too.

PyQUBO solves maxmizing the dot product of MAv and y.

# How to
I use PyQUBO released by Recruite Communications and google colaboratory.

https://github.com/recruit-communications/pyqubo

PIP is able to install PyQUBO, then we can use it in colaboratory. 

# We can find
some solution of equation systems in the internet.

But it is too difficault for me to understand (ToT)

# PyQUBOで連立方程式
もともとCAE屋さんなので、大きな連立方手式を解くことには
興味がありました。というか、もっとラクになるといいのになぁ、という感じ。

量子コンピュータが出てきたときに、あ、解を同時に無限に試して、一番いいものを
選ぶことができるんじゃないかと漠然と思っていました。

ただし、qbitなりspinなりは、0 or 1の2値なので、通常考えている浮動小数に
結びつけるのはちょっと難しいか、と考えていました。

# 解の近似と完璧を狙わないこと
ここでは、2Dの x, y について

Mx = y

という方程式を考えた時に、解 x を行列Aとベクトルvの積とスカラ係数cで表すこととして

M(cAv) = y

とし、ある v をAで回転させると x と平行になると仮定することに
しました。大きさはcで吸収します。

そうすると、M(Av) と　y　は平行と考えればよく、
内積を取って、これを最大（PyQUBOで解くときは符号を反対にして最小）に
することを考えられそうです。

また、A や v の成分は2進数っぽく表現することにしました。
完全な値は求められないでしょうが、近くまでできれば、これを初期値として
通常の方法である程度早く解けることが期待できるかと考えています。

# 環境
リクルートが公開している PyQUBO と google の colaboratory を
使っています。

https://github.com/recruit-communications/pyqubo

PyQUBOは pip でインストールできるので colaboratory でも簡単にインストールできます。

# 巷では
探せば、なんか出てくるんでしょうが、厳密に求めることを狙いすぎているような気がします。

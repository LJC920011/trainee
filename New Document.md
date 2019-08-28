1.高斯分布：(数据，算法上的运用)——————重点模型
基础公式及性质一遍过:

代码：
	标准正态分布（μ=0，σ=1）:np.random.randn(size)
    正态分布(可以指定μ和σ):np.random.normal(loc, scale, size)


2.指数分布:
基础公式及性质一遍过:
	无记忆性：P( T > (t+s) | T > t ) = P( T > s)   -> 忘记电灯已使用t
	

	f(x) =  λexp{-λx}    x > 0
		0 	       x <= 0

	其中λ>0为常数，则称X服从参数λ的指数分布。
               1                     1
  	期望E（X）=----      方差D（X）=------
               λ                   λ^2
代码:	lambda=0.5
		x = np.arange(0, 15, 0.1)
 		y = lambda*np.exp(-lambda*x)


3.泊松分布：
基础公式及性质一遍过:

             λ^k
	P(X=k)=------ exp{-λ}
              k!
	泊松分布的参数λ是单位时间(或单位面积)内随机事件的平均发生次数。
	泊松分布适合于描述单位时间内随机事件发生的次数。
	泊松分布的期望和方差均为λ

代码:	np.random.poisson(lam, size)
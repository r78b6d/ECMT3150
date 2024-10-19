java c
ECMT3150: Assignment 2 (Semester 2, 2024)
Due: 5pm, 18 October 2024 (Friday)NOTE: Please do not write your final answers in your R-script. You should summarise the outputs (e.g., plots) and include your discussion and final answers in the written response file. Both your written response file and R-script. (i.e., the  .R source Öle, not the screenshot) need to be submitted.[Total:  30 marks  (+ bonus)] Carol is undergoing a series of training at the pricing team in Goldman Sachs.  She is studying a simple financial market consisting of a risk-free money account and a stock called BOB. Here is the single-period model under the risk-neutral probability measure Q:
● Time length of the period is △ .
● In the risk-free market account, a dollar at time 0 will grow into a = er△ at time △ , where r is the continuously compounded risk-free interest rate.
● At time 0, the share price is S0 .  At time △, the share price rises to S△ = S0u with probability q, and drops to S△ = S0 dwith probability 1 - q.
1.  [2 marks] Write down the risk-neutral probability distribution of S△ , the share price at time △ . Express the probability mass function in terms of u; d and q.
2.  [3 marks] Show that q = u-d/a-d .  [Hint:  the discounted share price is a martingale under
Q.]
3.  [3 marks] Find  Var(S△ ), the variance of the share price at time △?  Express your answer in terms of a, u and d.
4.  [3 marks] Let u = eσ √△  and d =  = e-σ√△ .  Show that Var(S△ ) ≈ S0(2)σ 2 △ for small
△ .  [Hint:  ex   ≈ 1 + x if x is close to zero.  The final result is obtained by dropping terms involving higher power of △]Carol wants to construct a binomial tree model for the price of BOB traded in an n- period market, where n is a positive integer.  Here is the binomial tree model under Q (for i = 1; : : : ; n):
● Time length of a period is △ .
● In the risk-free market account, a dollar at time (i — 1)△ will grow into a = er△ at time i△, where r is the continuously compounded risk-free interest rate, which remains constant overtime.
● At time (i — 1)△ , the share price starts at S(i-1)△ . At time i△, the share price rises to S(i-1)△u with probability q, or drops to S(i-1)△dwith probability 1—q. The probability q is as given in question 2, and u and d are as given in question 4 (i.e. u = eσ √△ and d = u/1 = e-σ√△ ). Assume that the price changes are independent across all n periods.
5.  [3 marks] Let j  denote the number of times by which the share price goes up over n per代 写ECMT3150: Assignment 2 (Semester 2, 2024)R
代做程序编程语言iods. What is the probability distribution of j?  For a given j, show that the share price at the end of period n is given by
Sn△ = S0ujdn-j:
6.  [2 marks] Consider a European call option written on a share of BOB at time 0 with strike price X and time-to-maturity T = n△ .  Show that its price is given byC0(bin) = EQ [e-rn△ max(Sn△ — X; 0)]:                                  (1)Suppose we are at time 0, and the current share price of BOB is S0  = 50. Suppose r = 0:02 and σ = 0:3.  Write an R code that simulates 5000 sample paths of share price using the above binomial tree model with the following specifications:  n = 63, △ = 1=252.    While simulating the random numbers, set the random seed to be the last 5 digits of your SID. [Hint:  you may use rbinom(5000,n,p)to generate 5000 random integers from a binomial distribution with parameters n and p.]
7.  [3 marks] Using your code, compute the time-0 price of an at-the-money European call option written on a share of BOB at time 0 with strike price X = S0  = 50 and expiring in 63 days (i.e., T = 63△).  Correct your answer to 3 decimal places.
8.  [3  marks]  Compute analytically the time-0 price of the same call option using the Black-Scholes formula instead.  Correct your answer to 3 decimal places.  Compare it with your answer in question 7.Carol has recently moved to the product design team.   She is  currently designing an exotic option written on a share of BOB at time 0. This option will give the following payoff as a function of the share price ST  at time T

where X1  < X2 . Carol named this exotic option as ''fly-with-BOB,'' after noting that the graph of the payoff function looks like the wings of an aeroplane.
9.  [3 marks] Using your code, compute the time-0 price of a fly-with-BOB option with strike prices X1  = 45, X2  = 55 and expiring in 63 days (i.e., τ = 63△).  Correct your answer to 3 decimal places.
10.  [3 marks] Compute analytically the time-0 price of a fly-with-BOB option using the Black-Scholes formula instead.  Correct your answer to 3 decimal places.  Compare it with your answer in question 9.
11.  [2 marks] What type of investors will be interested in fly-with-BOB?
12.  [Optional question for those who are up to the challenge; bonus marks will be given for correct solutions] Prove mathematically that C0(bin) as defined in question 6 converges to
the Black-Scholes call price as △ → 0 and n → ∞ while τ = n△ remaining constant.

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com

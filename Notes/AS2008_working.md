## 1 Abstract and Intro

# We face inventory risk due to:
    Diffusive nature of stock mid price
    Poisson arrival of market buy and sell orders

# Inventory based strategy compared with native-symmetric strategies about mid-price
    Inventory-aware strategy found to yiel PnL with significantly less variance

# Most common risks facing dealers
    Inventory risk from asset value uncertainty
    Asymmetric information from more informed traders
    (We focus on inventory risk)

# Arrival rate k of orders is crucial
    Arises from econophysics ??
    Reproducing patterns with 'zaro intelligence agents' rather than optimal strategies of optimal agents
    Luckock takes different approach by modelling optimal strats. without utility functions
    Using econophysics literature to infer reasonable arrival rates - size distribution of orders

# Two step procedure to derive optimal bid/ask quotes
    Reservation price (personal indifference)
    Adjustment for probability of filling orders as a function of distance to mid-price


## 2 The model

    dSu = σdWu

    we assume constant volatility

    mid-price used exclusively to calculate asset value at end of horizon

# Optimising with finite horizon
    1) Frozen inventory strategy:
        Hold an inventory q until terminal time T - convex risk measure ??

    Agents value function 
        v(x, s, q, t) = Et[−exp(−γ(x + qST ) 
        can be
        v(x, s, q, t) = −exp(−γx) exp(−γqs) exp[(γ2q2σ2(T −t)/2]

    ?? model chosen over standard to ensure utility functionals remain unbounded ??

# Defining resevation bid and ask
    RESERVATION PRICE OCCURS WHERE A CHANGE IN THE PORTFOLIO MAKES NO DIFFERENCE IN UTILITY

    The average of reservation ask and bid gives reservation price:
        r(s, q, t) = s −qγσ2(T −t)

# Optimizing with infinite horizon (2.3)
    Not worrying too much about this

# Limit Orders
    being 'hit and 'lifted' by market orders ??
    limit order book shape determines priority of execution when large orders get executed
    market buys lift sell limit orders at Poisson rate
    market seels hit buy limit orders at poisson rate
        λa(δa)
    Therefore wealth and inventory are stocahstics and depends on arrival of market orders
    Also notice that the agent has control over the bid ask prices so indirectly influences arrival of orders he recieves. ?? Why do previous sections have less control ??

# The Trading Intensity
    Econophysics tries to describe laws governing microstructure
    Here, focus on addressing Poisson intensity lambda, where a limit order is executed as a function of distance to mid-price
    For this we need:
        i. overall frequency of mkt orders
        ii. distribution of their size
        iii.temporary impact of large orders
    
    size distribution found to obey power law ?? assumtpion:
        proptional to x^-(1 + alpha) for large x
        with varying values of alpha(1.53, 1.4, 1.5) mostly similar - why
    
    market impact less clear in econophys
        some find proportional to Q^(beta) for beta(0.5, 0.76)
        others find propootion to lnQ

    Now with all this info we can derive a lamba function of delta (mid-price distance):
        fig 2.11 (many options based on assumptions / preferences)

    If we use power price impact we get lamba(delta) = B delta^(alpha/beta)
    Alternatively, looking at short-term liquidity, market impact function can be derived by integrating density of the LOB:
        yields the "virtual price impact"
    
## The solution
# Optimal bid and ask quotes
    recall value function of the agent from earlier:
        u(s,x,q,t) = ..
    where optimal half-spreads are time and spread dependent. This type of optimal dealer problem was studied by Ho and Stoll
        Key analysis was use of dynamic programming to show the function u SOLVES HJB EQUATION
    So solution to the nonlinear PDE is continuous in variables s, x, t and depends on discrete values of inventory q.

    ?? not instant intuition or full understanding of last steps to solution

    
    



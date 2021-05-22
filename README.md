# CRUDE.LVRG

# Description
This asset is reward token for bitsharescrude

# Asset Parameters
- Max Supply 999,999,999.000000
- Stealth Supply 0
- Precision 6(0.000001)
- Market Fee Rate 0.1%
- Market Fee Referral Reward 10%
- Max Market Fee 0
# Permissions
- Enable market fee
- Require holders to be white-listed
- Issuer may transfer asset back to himself
- Issuer must approve all transfers
- Disable confidential transactions
# Flags
- Enable market fee
# How It Works
- CRUDE.LVRG is primarily a reward token for contributors to bitsharescrude fund.
- Users who contribute to the tune of 3million CRUDE.LVRG tokens become eligible for rewards.
- 33.33% the funds gotten are locked in the CRUDE.LPT Liquidity Pool Contract.
- 33.33% is converted to bitCNY and stored in the fbn3113104450 reserve wallet.
- all contract funds for CRUDE.LVRG are reflected on the crude-leverage wallet.
- The profits gotten from the pool share distribution will then be used to buy back CRUDE.LVRG from the market.
- This in-turn will reduce the yearly budget supply to holders and increase the value of the token via its locked contract. 

# CRUDE.BTX
This token is a smartcoin backed by CRUDE.LVRG, it represents 5x the price change of bitshares daily, price is fed @ least once
daily and it's taken from the close price of the BTS token.

# HOW IT WORKS
Originally, FTX tokens represent the underlying value of a leveraged asset, however this feature is not present currently on the
Bitshares DEX, rather it requires a trader who is willing to borrow the asset @ an MCR of 5, 
in the hope of selling for more LVRG tokens, while the buyer hopes to accumulate more BTX in order to get more LVRG tokens from Forced Settlement or price increase.
The basic economy is that as the price of bitshares rises, the MCR drops, a 100% rise in the price of bitshares will cause a
500% rise in price and may lead to the margin being called or ultimately global settlement, causing the BTX borrower to lose his margin and CLVRG tokens hence the MCR is set at 5.
However as long as bitshares price continues to go down, the margin is safe and the borrower can add to his position, a price drop below 20% leads to negative price feed (in such a case price cannot be fed
and the asset will have no price feed for the day)
The asset is extremely volatile thus the borrower must always be ready to maintain his position or end up losing his funds.
# PRICE FEED MECHANISM
- STEP 1 CALC THE AVERAGE DAY PRICE BITSHARES USING THE CURRENT OPEN PRICE OF BITSHARES TO THE PREVIOUS OPEN
     (COP + POP)/2 = AVGDP
- STEP 2 CALCULATE THE % PRICE CHANGE  
     ((COP-POP)/POP)*100
- STEP 3 MULTIPLY THE % CHANGE BY 5 = BTX%
- STEP 4 (AVGDP * BTX%/100)+AVGDP = BTX(USD)
- STEP 5 CONVERT THE PRICE TO NAIRA : BTX(USD)/(USD VALUE OF CRUDE.NGN currently @ $0.0015) = BTX(CNGN)
- STEP 6 CONVERT THE PRICE TO BTS = BTX(BTS)
- STEP 7 CORE EXCHANGE RATE (CER) = 1/(BTX(BTS)*5)
- STEP 8 FEED PRICE = CLVRG(NGN)/BTX(NGN) CLVRG(NGN) => 0.0208
- STEP 9 IF BTX(USD) IS NEGATIVE DO NOT FEED PRICE 
     

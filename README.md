# CRUDE.LVRG

# Description
LEVERAGE is the main investment vehicle of bitsharescrude-fund. Its market value is tied to it's liquidity pools. Staking to CRUDE.LVCNY and CRUDE.USDTLP liquidity pools earns users monthly Smartholdem airdrops in the form of CRUDE.STHLP. Added are FTX tokens the first being CRUDE.BTX which is a half-bull BTS smart token that can be borrowed and sold for 1.5 times its amount in bitshares.  Buy, Stake, and earn with LEVERAGE

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
- Issuer must approve all transfers
- Disable confidential transactions
# Flags
- Enable market fee
# How It Works
- CRUDE.LVRG is primarily a reward token for contributors to bitsharescrude fund.
- Users contribute by staking to the stablecoin liqiudity pools of Leverage. Currently there are two stable pools CRUDE.LVCNY and CRUDE.USDTLP.
- Every month CRUDE.STHLP tokens are then distributed to the ten richest wallets holding the assets in their wallets (The assets in order books will not be counted), according to a simple sharing formula where the highest contributor gets more reward.
- all data is displayed on the https://fund.bitsharescrude.i.ng site.

# CRUDE.BTX
This token is a smartcoin backed by CRUDE.LVRG, it represents 1.5x the price change of bitshares daily, price is fed @ least once
daily and it's taken from the close price of the BTS token.

# HOW IT WORKS
Originally, FTX tokens represent the underlying value of a leveraged asset, however this feature is not present currently on the
Bitshares DEX, rather it requires a trader who is willing to borrow the asset @ an MCR of 1.5. 
The basic economy is that as the price of bitshares rises, the MCR drops, a 100% rise in the price of bitshares will cause a
150% rise in price and may lead to the margin being called or ultimately global settlement, causing the BTX borrower to lose his margin and CLVRG tokens hence the MCR is set at 1.5.
However as long as bitshares price continues to go down, the margin is safe and the borrower can add to his position, a price drop below 67% leads to negative price feed (in such a case price cannot be fed
and the asset will have no price feed for the day)
The asset is extremely volatile thus the borrower must always be ready to maintain his position or end up losing his funds.
# PRICE FEED MECHANISM
- STEP 1 CALC THE AVERAGE DAY PRICE BITSHARES USING THE CURRENT OPEN PRICE OF BITSHARES TO THE PREVIOUS OPEN
     (COP + POP)/2 = AVGDP
- STEP 2 CALCULATE THE % PRICE CHANGE  
     ((COP-POP)/POP)*100
- STEP 3 MULTIPLY THE % CHANGE BY 1.5 = BTX%
- STEP 4 (AVGDP * BTX%/100)+AVGDP = BTX_CNY
- STEP 5 CONVERT THE PRICE TO LEVERAGE : BTX_CNY/(CNY VALUE OF CRUDE.LVRG) = BTX_CLVRG
- STEP 6 CONVERT THE PRICE TO BTS = BTX_BTS
- STEP 7 CORE EXCHANGE RATE (CER) = 1/(BTX_BTS)*1.5)
- STEP 8 FEED PRICE = 1/(Price in LEVERAGE)
- STEP 9 IF BTX_CLVRG IS NEGATIVE DO NOT FEED PRICE 
     

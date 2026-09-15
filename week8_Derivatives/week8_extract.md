# Extraction: ../../week8_Derivatives.pptx (59 slides)

## Slide 1  [layout: Title and Caption]
 EF5342 Financial Systems, Markets and InstrumentsSemester B 2025/2026Week 8
 Prof. Weikai Li
  [IMAGE -> figures/slide01_img.jpg]

## Slide 2  [layout: Title and Content]
 Derivatives
 Overview of Derivatives
 Futures and Forwards
 Options
 Hedging and Speculation with Derivatives

## Slide 3  [layout: Title and Content]
 Derivatives
 Securities whose value is derived from the value of some underlying asset or financial instrument
  - Underlying asset can be a stock, T-bill/bond, foreign currency, commodity or even another derivative security
 Generally involve an agreement between two parties to exchange certain quantity of an asset or cash flow at a predetermined price and at a specified date in future
 Types of derivatives
  - Forwards
  - Futures
  - Options
  - Swaps

## Slide 4  [layout: Title and Content]
 Purpose of Trading Derivatives
 To Speculate
  - To profit from expected changes in the underlying asset’s price
  - No position in underlying asset
 To Hedge
  - To minimize or manage risks
  - Have position in underlying asset with the goal to offset risk
 To Arbitrage
  - To take advantage of price discrepancies between underlying asset and its derivatives (e.g., covered interest rate parity arbitrage)
  - Take positions in underlying and derivatives simultaneously
 Note that a derivative contract is a “zero sum game”. How much you gain in a contract is equivalent to how much your counterparty lose.

## Slide 5  [layout: Blank]
 Forwards and Futures
 A spot contract is an agreement to transact involving the immediate exchange of assets and cash
 A forward contract is a non-standardized agreement to buy or sell an asset in the future, with the terms of the contract set today
 Forwards are:
  - customized contracts
  - not traded in secondary market, so participants must perform
  - have potential counterparty risk that the other side fails to perform obligations under the terms of the contract
 A futures contract is a standardized, exchange-traded version of a forward contract

## Slide 6  [layout: Blank]
 Differences between Futures and Forwards
 Futures differ from forwards in the following ways:
  - Futures are liquid, most traders close their position before the delivery date so the underlying delivery may never take place
  - Futures contracts are marked to market daily—i.e., traders’ gains and losses on outstanding futures contracts are realized each day as futures prices change
  - Exchange clearing house stands behind all contracts so there is minimum counterparty default risk
  - Futures have margin requirements
    - margin requirement is a deposit required on futures contract to ensure that the terms of futures contract will be met

## Slide 7  [layout: Blank]
 Futures Contracts
 A long position is the purchase of a futures contract
 A short position is the sale of a futures contract
 Open interest is the total number of the futures contracts outstanding at the beginning of the day
 A clearing house is the unit that oversees trading on the exchange and guarantees all trades made through the exchange
  - Clearing houses act as third parties to all futures and options contracts, as buyers to every clearing member seller, and as sellers to every buyer
  [IMAGE -> figures/slide07_img.png]
  [NOTES: The role of the clearing house is to perform the obligations under the contract agreed between the two counterparties, thereby removing the counterparty risk the parties of the contract had to each other and replacing it with counterparty risk to a highly regulated central counterparty that specializes in managing and mitigating counterparty risk]

## Slide 8  [layout: Blank]
 Futures Contracts
 The underlying asset of future contracts could be T-notes/bonds, currency, commodity, stock index, single stock or even bitcoin.
 Futures contract can be settled in two ways:
  - Physical Delivery: requires the actual underlying asset to be delivered on the specified delivery date
  - Cash Settlement: requires the counterparties to the contract to net out the cash difference in the value of their positions, no actual assets are delivered at the expiration

## Slide 9  [layout: Blank]
 List of Futures Contracts
  [IMAGE -> figures/slide09_img.png]

## Slide 10  [layout: Title and Content]
 http://www.cmegroup.com/trading/energy/crude-oil/light-sweet-crude_contract_specifications.html
 Eg of physically settled contract
 9
  [IMAGE -> figures/slide10_img.png]

## Slide 11  [layout: Title and Content]
 Eg of cash-settled contract
 http://www.cmegroup.com/trading/energy/crude-oil/emini-crude-oil_contract_specifications.html
 10
  [IMAGE -> figures/slide11_img.png]

## Slide 12  [layout: Blank]
 Long position – a commitment to purchase the asset on the delivery date.
 Short position – a commitment to sell the asset on the delivery date.
 Profit to long = Spot price at maturity - Original futures price
 Profit to short = Original futures price - Spot price at maturity
  Long and Short positions profit from opposite price movements.
 The futures contract is a zero-sum game, which means gains and losses net out to zero.
 Long and Short Positions

## Slide 13  [layout: Title and Content]
 Futures/Forward profit profile at maturity
 Profit profile at maturity on a 1-month crude oil futures contract at a futures price of $40.
 $40
 $profits
 Spot Oil price in 1 month
 Long Position
 $40
 $profits
 Spot Oil Price in 1 month
 Short Position
 Important! You must know how to plot profits of a derivative contract at maturity, where the horizontal axis is the spot price of the underlying asset at maturity.

## Slide 14  [layout: Blank]
 Margin Requirement on Futures
 An initial margin is a deposit required on futures trades to ensure that the terms of the contracts will be met
 The maintenance margin is the margin a futures trader must maintain once a futures position is taken
  - if losses occur such that margin account fall below the maintenance margin, the customer receives a margin call and is required to deposit additional funds to bring margin account back to initial margin level and keep the position open
 Brokers can close out customers’ futures position if margin is not maintained
 Margin requirements are set by exchanges and varies across contracts (change over time)

## Slide 15  [layout: Blank]
 Example – Futures Contract Terms
 Contract: 30-year Treasury Bond contract
 Exchange: Chicago Board of Trade (CBOT)
 Delivery Months:	Contract maturity months are March, June, September, December
 Contract Size: Contract calls for delivery of $100,000 face value
 Deliverable Instrument: Treasury bonds that mature for at least 15 years from the date of delivery and mature in no more than 25 years
 IMR: Exchange mandated initial margin requirement to initiate a position (brokers may require a higher margin)
 MMR: Exchange mandated maintenance margin requirement to keep the position open
  [TABLE]
    | Contract | Exchange | Delivery Months | Contract Size | Deliverable Instrument | IMR | MMR |
    | T-Bond | CBOT | M,J,S,D | $   100,000 | See below* | $2,530 | $2,300 |
  [NOTES: Margin requirements as of Spring 2014.  See the CBOT website for updates.  Similar contracts may be available on other exchanges with slightly different terms.
The contract calls for delivery of bonds with a 6% yield and a price adjustment is made if they are not 6% yield.]

## Slide 16  [layout: Blank]
 Long and Short Positions
 If an investor buys or goes “long” one June contract, they are agreeing to buy $100,000 par or face value of T-Bonds at the original futures contract price when the contract expires in June.
 If an investor sells or goes “short” one June contract, they are agreeing to deliver $100,000 par or face value of T-Bonds and receive the original futures contract price when the contract expires in June.
 Each investor must put up the IMR of $2,530 when they initiate the contract.
 Each investor must maintain the MMR of $2,300 in their margin account while the position is open.
  [TABLE]
    | Contract | Exchange | Delivery Months | Contract Size | Deliverable Instrument | IMR | MMR |
    | T-Bond | CBOT | M,J,S,D | $   100,000 | See below* | $2,530 | $2,300 |

## Slide 17  [layout: Blank]
 Mark to Market
 Gains and losses are recognized daily
 IMR = $2,530, MMR = $2,300
 Suppose you buy one June contract at the opening price of 98’16 (98+16/32=98.5), Monday’s settle price is 98’10 (98+10/32=98.3125), and Tuesday’s close is 97’00.  What is in your margin account after Tuesday’s settle?
 Who receives the money taken out of your margin account?
  [TABLE]
    | Long in contract |  |  |  |  |
    | Marking to Market |  |  |  |  |
    |  | Settle | Underlying Value | Price Change | Margin Acct |
    | OPEN |  | $98,500.00 |  | $2,530.00 |
    | Mon. | 98’10 | $98,312.50 | ($187.50) | $2,342.50 |
    | Tues. | 97’00 | $97,000.00 | ($1,312.50) | $1,030.00 |
    | MARGIN CALL (beneath $2,300) add cash = |  |  |  | $1,500.00 |
    |  |  |  |  | $2,530.00 |
  [NOTES: The futures price is effectively updated with daily marking to market.
In this example the IMR is restored when there is a margin call]

## Slide 18  [layout: Title and Content]
 Valuation of Futures
  [IMAGE -> figures/slide18_img.png]
  [NOTES: Convenience yield: benefits from holding the underlying asset, such as to profit from temporary shortages, and the ability to keep a production process running]

## Slide 19  [layout: Title and Content]
 Parity Condition for Futures Price
  [IMAGE -> figures/slide19_img.png]

## Slide 20  [layout: Title and Content]
 Contango vs. Backwardation
  [IMAGE -> figures/slide20_img.png]
  [IMAGE -> figures/slide20_img.jpg]

## Slide 21  [layout: Title and Content]
 Basis
 Basis
 At Maturity
 Spot
 Futures
 Price
 1 month before Maturity
  [IMAGE -> figures/slide21_img.png]

## Slide 22  [layout: Title and Content]
 Arbitrage with Futures
 Investors can make riskless profits when the actual price of futures is different from its theoretically implied futures price according to the futures parity condition.
 Example. If gold costs 2% p.a. to store and interest rate is 1% p.a. The current spot price is $1400/ounce. What should the one-year futures price be?
  - Futures price should be F=1400×(1+0.02+0.01)=$1442.
  - If the actual futures price is too high, e.g., $1450. We should borrow money $1400, buy spot gold now (store for 1 year), and enter into a futures contract maturing in 1 year to sell gold for $1450.
  - Profit (on maturity date) = -$1400*(1+2%+1%)+$1450=$8
  - What if actual futures price is too low, e.g., $1420?

## Slide 23  [layout: Title and Content]
 Risks of Trading Futures
 Market risk
  - Speculators win or lose based on the changing market prices.
  - Hedgers have a position in the underlying asset, and won’t be impacted by contract price volatility, unless they do not have enough cash for margin calls before expiration.
 Basis risk
  - Basis risk is the risk of imperfect correlation between the % changes in the futures price and the % changes in the spot price over the hedging period, resulting in imperfect hedge. (E.g., airlines hedge rising cost of jet fuel using crude oil futures)
 Liquidity risk
  - If a contract is not widely-traded, it is difficult to find a counterparty to close a position before maturity.
 Counterparty risk
  - Forwards have much higher counterparty risk: If the other party in the forward contract defaults, you can suffer large losses.
  - Counterparty risk in futures is mitigated by daily marked-to-market accounting and guarantee by exchange clearing house.

## Slide 24  [layout: Title and Content]
 Options

## Slide 25  [layout: Title and Content]
 Options
 Options give the buyer the right but not the obligation to buy or sell the underlying asset at a pre-specified price (strike price) within a specific period of time.
  - Call option: Right to buy
  - Put option: Right to sell
 Buyer needs to pay a premium to the seller for this option.
 Options differ from futures and forwards in that:
  - You have to pay a premium to buy the option (not free).
  - A buyer of a futures/forward contract has the obligation to make delivery/settlement at maturity. But an option buyer can “walk away” if exercising is not profitable.
  - By not exercising, the option buyer loses only the option premium.

## Slide 26  [layout: Title and Content]
 Calls and Puts
 Seller or writer of the option:
  - Receives the premium upfront
  - Has an obligation to sell (call) or buy (put) the underlying asset if the buyer decides to exercise the option
 European options can be exercised only at maturity date. American options can be exercised anytime before or at the maturity
  - Most of equity options are American options
 If the asset’s spot price is equal to the strike price of the option, we say that the option is “at the money”:
  - “In-the-money” means excising option immediately is profitable
  - “Out-of-the-money” means excising option immediately is not profitable
  - Calls: Spot>Strike, means in the money. Spot<Strike, out of the money
  - Puts: Spot<Strike, means in the money. Spot>Strike, out of the money

## Slide 27  [layout: Title and Content]
 Speculating with Call Options
 BUY A CALL: Speculator thinks the spot price will rise above a particular strike price X and pays a premium for the right but not the obligation to buy the asset at strike price X.
 If the spot price rises above X, the option contract is in-the-money and buyer of the call option would exercise.
 If the spot price does not rise above X, option is out-of-the-money, and buyer does not exercise. Buyer loses the premium paid for the option.
 If exercised at maturity, net profit/loss equals:
  - ̶  Amount of the option premium
  - ̶  Amount paid for the exercising the option (call’s strike price)
  - + Price received for selling the asset in spot market (spot price at maturity)
 If not exercised, net profit/loss at maturity equals:
  - ̶  Amount of the option premium

## Slide 28  [layout: Blank]
 0
 -$4
 Long Call
 You long 1 call option with:
 Strike Price = $25, Call Premium = $4
 $25
 $29
 Profit
 Spot Price at expiration
 Speculating with Call Options

## Slide 29  [layout: Title and Content]
 Speculating with Put Options
 BUY A PUT: Speculator thinks a spot price will drop below a particular strike price X and pays a premium for the right but not the obligation to sell the underlying asset at the strike price X.
 If the spot price drops below X, the option contract is in-the-money and buyer of the put would exercise.
 If the spot price does not drop below X, option is out of the money, and buyer of the put does not exercise. Buyer loses the premium paid for the option.
 If exercised at maturity, net profit/loss equals
  - ̶  Amount of the option premium
  - ̶  Amount paid to buy asset in spot market (spot price at maturity)
  - + Price received for exercising the put (put’s strike price)
 If not exercised, net profit/loss at maturity equals
  - ̶  Amount of the option premium

## Slide 30  [layout: Blank]
 0
 -$4
 Long Put
 $33
 $29
 Profit
 Spot Price at expiration
 You long 1 Put Option with:
 Strike Price = $33, Put Premium = $4
 Speculating with Put Options

## Slide 31  [layout: Title and Content]
 Option profit profiles
 Long Call
 Short Call
 -$Call premium
 Profit
 $0
 Price of underlying asset at maturity
 Strike price
 +$Call premium
 Profit
 $0
 Price of underlying asset at maturity
 Strike price
 Long Put
 -$Put premium
 Profit
 $0
 Price of underlying asset at maturity
 Strike price
 $(Strike Price - Put Premium)
 +$Put premium
 Profit
 $0
 Price of underlying asset at maturity
 Strike price
 -$(Strike Price - Put Premium)
 Short Put
 Payoff Function
 Payoff Function
 Payoff Function

## Slide 32  [layout: Title and Content]
 Option premium has an intrinsic and extrinsic component.
 Intrinsic value is determined by whether the option is in, out, or at-the-money
  - For Calls, intrinsic value = Max {0, S-X}
  - For Puts, intrinsic value = Max {0, X-S}
  - where X = strike price, S = spot price
 Extrinsic component is also called the “time value”.
 Time value = option premium - intrinsic value
  - Option has time value because the intrinsic value could further increase before maturity.
  - Time value depends on characteristics such as volatility of underlying asset, time left to maturity, dividend yield, interest rate.
 Intrinsic Value and Time Value of Option

## Slide 33  [layout: 1_Title and Content]
 Intrinsic and Time Value of Options
 Figure 10–9 The Intrinsic Value versus the Before-Exercise Value of a Call Option
 10-
  [IMAGE -> figures/slide33_img.jpg]

## Slide 34  [layout: Blank]
 The May call is in the money (positive intrinsic value) and the call premium is $3.30
 The intrinsic value of the call (S-X) is ($8.79 - $6.00) = $2.79
 The time value of the call is $3.30 - $2.79 = $0.51
 The May put is out of the money so the put’s intrinsic value is 0
 The May put still has time value, however, equal to $0.45
 Intrinsic and Time Value: example
  [TABLE]
    | AMR |  |  |  | Underlying stock price $8.79 |  |  |  |
    | Expiration |  | Call |  |  | Put |  |  |
    |  | STRIKE | LAST | VOLUME | OPEN INTEREST | LAST | VOLUME | OPEN INTEREST |
    | May | 6.00 | 3.30 | 12 | 578 | 0.45 | 20 | 4175 |
    | Jan | 7.50 | 1.30 | 60 | 17062 | 0.15 | 138 | 58909 |
  [NOTES: An investor would not exercise the May call because that would be throwing away the $51 time value. 
Notice that the closer to the money option has much higher open interest.]

## Slide 35  [layout: Title and Content]
 Determinants of Option Price
 Black and Scholes (1973) derived the formula for determining the price of an option based on observable factors.
 Here are the directional impact of the following factors on total (total=intrinsic plus extrinsic) option premium and the reasoning behind the directional impact.
 Factor influencing option premium
 Call
 Put
 Current price of underlying
 +
 ‒
 Strike price
 ‒
 +
 Yield from holding underlying asset (div)
 ‒
 +
 Time to maturity
 +
 +
 Price volatility of underlying asset
 +
 +
 Interest rate
 +
 ‒
 Intrinsic value, obvious
 Explained in next slide
  [NOTES: The higher the spot price, the more likely call option getting in the money; The higher the strike price, the less likely call option getting in the money;]

## Slide 36  [layout: Two Content]
 The longer the time to maturity, the greater the chance of the option getting in-the-money (applies to both call and put).
 As volatility increases, the chance that the stock will do very well or very poorly increases. Option (both call and put) allows you to profit when price moves favourably but has limited downside risk if price move adversely.
 The greater the interest rate, the more valuable the call. Since you don’t need to pay cash to buy the spot now, you can invest the money at high interest rate. A put is the opposite: If you have the right to sell asset at certain strike price in the future and interest rates are high, the PV of the strike price is lower.
 If underlying asset has an expected dividend, stock price will fall by the dividend amount.
  - While the spot price falls on the ex-dividend date by the dividend amount, the strike price is fixed and doesn’t fall by the dividend amount.
  - Call is less likely getting in-the-money while put is more likely getting in-the-money.
 Determinants of Option Price

## Slide 37  [layout: Two Content]
 Option prices can be used to back out investors’ expectation of market volatility (implied volatility which is forward-looking)
 The VIX is a real-time market index that measures the market's expectations for volatility in the S&P 500 Index (SPX) over the next 30 days
 Widely known as the "fear gauge" or "fear index" because it tends to rise sharply during periods of market stress, uncertainty, or declining stock prices
 The VIX
  [IMAGE -> figures/slide37_img.png]

## Slide 38  [layout: Two Content]
 Bond market's equivalent of the VIX — often called the "VIX for Bonds."
 It measures implied interest rate volatility across U.S. Treasury markets, serving as a key fear gauge for fixed income investors.
 One of the MOVE Index's most useful properties is that it can lead equity market volatility — sometimes signaling stress before it shows up in the VIX.
 ICE BofA MOVE Index
  [IMAGE -> figures/slide38_img.png]

## Slide 39  [layout: Title and Content]
 Hedging and Speculation with Derivatives

## Slide 40  [layout: Title and Content]
 Hedging with Derivatives
 Derivatives allow investors and firms to remove (hedge away) risks that they do not want to face.
 For hedging, we will consider:
  - Hedging with futures/forwards
  - Hedging with options
 In order to know how to use a derivative to hedge, you need to understand what is the underlying position of the investor.
 The next slide contains a very useful way to check what underlying position you have.

## Slide 41  [layout: Title and Content]
 Are you long or short the underlying asset?
 Futures/Forwards can be used for hedging.
 To hedge: Take the opposite position as your underlying spot position in a futures/forward contract.
 But do you have an underlying long or short position on the spot?
 A general rule to check if you are long or short “something” (e.g., foreign currency, stock, real estate, or a commodity).
 LONG: You are happy if the price of that “something” goes _up___.
 SHORT: You are happy if the price of that “something” goes _down_.
 This rule is particularly useful for natural underlying positions arising from business or expected future actions.
  - If you own a car, are you short or long oil?
  - If you are going to buy an apartment in HK next year, are you long or short HK real estate now?
  - A farmer who grows wheat is long or short wheat?
  [NOTES: Short Oil
Short real estate
Short Chinese Yuan
Long wheat]

## Slide 42  [layout: Title, Text, and Content]
 Hedging with Futures/Options Example
 An investor needs to sell a stock in six month’s time in order to make a down-payment for a house. The stock is worth $50 now. (time 0)
 He is exposed to fluctuations in the stock price during the next six months. His profit or loss is uncertain.
 Qn: Is his underlying position long or short the stock? Answer ____________.
 Underlying position
 Stock price at maturity (i.e. in 6mths)
 $50
 Profit based on time 0 price.
 $0

## Slide 43  [layout: Title and Content]
 Futures Hedge
 Suppose the investor can hedge his exposure using the futures contract for this stock.
 He will short a futures contract at the futures price. Assume that the futures price is exactly $50 for simplicity.
  - Recall that theoretical futures price is computed from F=S(1+r-d)
 This hedge completely eliminates price risk of the underlying asset.
 If the stock price goes up, the investor would benefit in the underlying position but lose money in the short futures contract. So the investor gives up potential upside of the stock.
 But he is also sheltered from potential downside. If the stock price goes down, the investor would lose money in the underlying position. But he would make profit in the short futures contract.

## Slide 44  [layout: Title and Content]
 Result of Futures Hedge
 Underlying position
 Stock price at maturity
 Short futures contract
 $50
 Profit
 hedged position, flat line
 $0
 What is the point of doing this? Why not just sell the stock?
  [NOTES: 4 reasons
Cannot sell (restriction, or underlying position)
Costs
It is equivalent, futures parity condition 
More flexibility can adjust futures more easily than spot]

## Slide 45  [layout: Title and Content]
 Basis Risk in Futures Hedging
 The hedges in the example have been almost too good to be true. In practice, hedging is often not quite as straightforward as this:
  - The asset whose price is to be hedged may not be exactly the same as the asset underlying the futures contract.
  - There may be uncertainty as to the exact date when the asset will be bought or sold.
  - The hedge may require the futures contract to be closed out before its delivery month.
 These problems give rise to what is termed basis risk.
  - The spread between the spot price and the futures price may either widen or narrow between the time when a hedging position is initiated and the time when it is liquidated.
 E.g., in the previous example, if the investor had to sell the stock and close the futures positions in three months, and assume spot price is $45 and futures price is $47. The net amount received is:
 $45 + ($50 - $47)=$48, which is less than the expected $50

## Slide 46  [layout: Title and Content]
 Hedging with Options
 Is there a hedge in which the investor can retain some of the upside potential, while limiting its downside risk? Yes, with an options.
 Assume the investor can buy a 6-month put option on the stock with an exercise price K=$50. Suppose put premium is $4.
 The profits at maturity are described below in two scenarios:
  - Stock price $30. The investor loses $20 on the long stock position. But the put option is in the money. He makes money on the long put (=20-4=$16). Total profit=-$4.
  - Stock price $60. The investor earns $10 on the underlying position. The put option is out of the money. But he still incurred the cost of the put premium. Total profit=10-4=$6.

## Slide 47  [layout: Title Only]
 Profits at maturity according to stock price
  [TABLE]
    | Stock price at maturity | Long stock profits | Exercise Put  Option? K=$50 | Option Profits (including premium paid) | Total Profits |
    | 30 | -20 | Y | 20-4 | -4 |
    | 40 | -10 | Y | 10-4 | -4 |
    | 50 | 0 | Indifferent | -4 | -4 |
    | 54 | 4 | N | -4 | 0 |
    | 60 | 10 | N | -4 | 6 |
    | 70 | 20 | N | -4 | 16 |

## Slide 48  [layout: Title and Content]
 Hedging Long Position with a Long Put
 $0
 Stock price at maturity
 (1)+(2)=(3) Options hedge Combined Profit Profile
 Profits
 -$4
 $50
 $54
 Compare to futures hedge (dotted line)
 (1) Underlying position
 Stock price at maturity (6mths)
 $50
 Profit
 $0
 (2) Long Put
 Stock price at maturity (6mths)
 $50
 Profit
 $0
 -$4

## Slide 49  [layout: Title and Content]
 Using Options to Hedge Underlying
 Long call
 Short asset
 Hedge short position with call option
 Combined position
 Profit
 Long call to hedge short asset position
 Long asset
 Long put
 Hedge long position with put option
 Combined position
 Profit
 Long put to hedge long asset position (the previous example)
 Assume option strike price = asset price =K. Put premium=$p, Call Premium=$c
 -p
 Asset price at maturity
 K
 -p
 K
 -c
 K
 -c
 K
 Asset price at maturity
 Asset price at maturity
 Asset price at maturity
 Profit
 Profit
  [NOTES: Put-call parity: S+P=C]

## Slide 50  [layout: Title and Content]
 Speculating with Options
 In addition to being used as hedging instrument, options are particularly suitable for speculators to bet on sophisticated views of future price movement.
 Using futures/forwards, we can only bet on either a rise or fall in the underlying asset’s price
 By using options, we could bet on:
  - A large rise/drop in the price of the underlying security
  - A moderate rise/drop in the price of the underlying security
  - Price of underlying asset will change a lot in either direction
  - Price of underlying asset will change little in either direction

## Slide 51  [layout: Title and Content]
 Bull Spread Using Calls
 K1
  - K2
 Profit
 ST
 Buy a call with strike price K1 and sell a call with strike price K2
 Believe underlying asset’s price will rise (only moderately)
  [IMAGE -> figures/slide51_img.png]
  [IMAGE -> figures/slide51_img1.png]

## Slide 52  [layout: Title and Content]
 Bear Spread Using Puts
 K1
 K2
 Profit
 ST
 Buy a put with strike price K2 and sell a put with strike price K1
 Believe underlying asset’s price will fall (but only moderately)
  [IMAGE -> figures/slide52_img.png]
  [IMAGE -> figures/slide52_img1.png]

## Slide 53  [layout: Title and Content]
 Collar and Straddle
 Long underlying
 Short call
 Long Collar
 Combined position
 Profit
 Long asset. Hedge by selling out-of-money call, buying out-of-money put. (Madoff claimed to use this strategy, see WSJ article).
 Buy put
 Long call
 Long Straddle
 Combined position
 Profit
 Long call and Long put at same strike price with same maturity. (basically long volatility)
 K
 K
 long put
 -(c+p)
 Profit
 Profit
 Asset price at maturity
 Asset price at maturity
 Asset price at maturity
 Asset price at maturity
  [NOTES: https://blogs.wsj.com/marketbeat/2008/12/16/madoffs-not-so-unique-options-strategy/]

## Slide 54  [layout: Title and Content]
 Collar and Straddle
 A collar is an options strategy that brackets the value of asset between two bounds.
  - Buy a protective put to limit downside risk of a position.
  - Fund the put by writing a call, so also limit upside gain.
  - Net outlay for options is approximately zero.
 The straddle is a bet on volatility.
  - To make a profit, the change in stock price must exceed the cost of both options. You need a large change in stock price in either direction.
  - The writer of a straddle is betting the stock price will not change much.
  - Nick Leeson’s short straddle strategy caused collapse of Barings Bank in Jan 1995.

## Slide 55  [layout: Title and Content]
 Put-Call Parity
 The call-plus-bond portfolio (on left) must cost the same as the stock-plus-put portfolio (on right):
 C and P are the price of call and put with the same time to maturity T and the same strike price X
 At the maturity date T, both strategies will generate the same payoff, regardless of the prevailing stock price ST
 If at maturity ST  >X, call option will be exercised and you end up with the stock (on left); the put option is out of the money and you also only have the stock (on right)
 If at maturity ST  <X, call option is out of the money and you end up with X (on left); put option will be exercised and you sell the stock you own at strike price X (on right)
  [IMAGE -> figures/slide55_img.png]

## Slide 56  [layout: Blank]
 Stock Price = 110   Call Price = 17
 Put Price = 5           Risk Free = 5%
 Maturity = 1 yr         X = 105
 17 + 100 > 110 + 5
 Since the right side is less expensive, you will buy the stock and a put option, while simultaneously sell a call option and borrow the PV of strike price X
 Riskless profit of $2 regardless of the stock price at maturity (verify)
 Violation of Put-Call Parity Example
  [IMAGE -> figures/slide56_img.emf]

## Slide 57  [layout: Blank]
 Violation of Put-Call Parity Example
  [TABLE]
    | Position | Immediate | Cash Flow in 1 Year |  |
    |  | Cash Flow | ST < 105 | ST >= 105 |
    | Buy stock | -110 | ST | ST |
    | Borrow $105/1.05=$100 | +100 | -105 | -105 |
    | Sell a call option | +17 | 0 | -(ST-105) |
    | Buy a put option | -5 | 105-ST | 0 |
    | Total | 2 | 0 | 0 |

## Slide 58  [layout: Blank]
 Key Takeaways
 What are Derivatives?
 Securities with value derived from an underlying asset (stock, currency, commodity). Used for speculation, hedging, or arbitrage. Zero-sum game.
 Forwards vs. Futures:
  - Forwards: Customized, OTC, counterparty risk, settled at maturity.
  - Futures: Standardized, exchange-traded, marked-to-market daily, low counterparty risk (clearinghouse), margin requirements.
 Futures Payoffs (at maturity):
  - Long: Profit = Spot – Futures Price (unlimited upside).
  - Short: Profit = Futures Price – Spot (unlimited downside).

## Slide 59  [layout: Blank]
 Key Takeaways
 Options (Rights, not Obligations):
  - Call: Right to buy at strike price. Put: Right to sell at strike price.
  - Buyer: Pays premium; limited loss (premium), unlimited gain.
  - Seller (Writer): Receives premium; limited gain (premium), unlimited loss.
  - Key Determinants of Premium: Underlying price, strike price, time to maturity, volatility (higher volatility = higher premium), interest rates.
 Hedging Strategies:
  - Futures: Take opposite position to underlying exposure. Eliminates risk but also upside.
  - Options: Long put protects long asset (limits downside, retains upside). Long call protects short asset.
  - Put-call Parity:
  - Futures Parity Condition:
  [IMAGE -> figures/slide59_img.png]
  [IMAGE -> figures/slide59_img1.png]

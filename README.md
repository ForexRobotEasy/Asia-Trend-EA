# Asia Trend EA

This code is an expert advisor (EA) developed by the Forex Robot Easy Team. It is designed for trend trading in the Forex market. The EA uses a custom trend indicator to identify the direction of the trend and opens buy or sell positions accordingly. It also incorporates a grid trading strategy to build additional orders at specified price levels.

## Input Parameters

- `IndicatorPeriod` (default: 14): Period for the trend indicator.
- `GridStep` (default: 10): Grid step for building orders.
- `StopLoss` (default: 50): Stop loss in points.
- `Autolot` (default: 1): Autolot option (0 - off, 1 - on).
- `LotMultiplier` (default: 2): Lot multiplier for grid orders.

## Global Variables

- `trendIndicatorHandle`: Trend indicator handle.
- `lotSize`: Lot size for opening positions.

## Custom Indicator Initialization

The `OnInit()` function is responsible for initializing the EA. It creates the trend indicator using the `iCustom()` function and sets the initial lot size based on the account balance and autolot option.

## Custom Indicator Deinitialization

The `OnDeinit()` function is called when the EA is being shut down. It removes the trend indicator using the `ObjectDelete()` function.

## Expert Advisor Start Function

The `OnTick()` function is the main entry point for the EA. It is triggered on each tick of the market. 

1. The current trend is determined using the trend indicator.
2. If the trend is positive (trend value = 1), a buy position is opened. The entry price is set to the current ask price, and the stop loss level is calculated based on the stop loss parameter.
3. If the buy position is successfully opened, a loop is executed to build grid orders at decreasing price levels. Each grid order has a lot size calculated based on the lot multiplier and the iteration index.
4. If the trend is negative (trend value = -1), a sell position is opened. The entry price is set to the current bid price, and the stop loss level is calculated based on the stop loss parameter.
5. If the sell position is successfully opened, a loop is executed to build grid orders at increasing price levels. Each grid order has a lot size calculated based on the lot multiplier and the iteration index.

## Product Description

The Asia Trend EA is an advanced Forex trading software developed by the Forex Robot Easy Team. It is designed to take advantage of trending market conditions and uses a custom indicator to identify profitable trading opportunities. The EA incorporates a grid trading strategy to build additional orders at specific price levels, maximizing the profit potential.

Key Features:
- Trend-based trading: The EA identifies the direction of the trend using a custom indicator and opens positions accordingly.
- Grid trading strategy: The EA builds additional orders at specified price levels, enhancing the profit potential.
- Adjustable parameters: The EA allows users to customize input parameters such as the indicator period, grid step, stop loss, autolot option, and lot multiplier.
- Money management: The EA automatically adjusts the lot size based on the account balance and the autolot option.
- Easy to use: The EA is designed to be user-friendly and can be easily set up on any MetaTrader 5 platform.

Please note that ForexRobotEasy is not the official developer of this product. We only provide sample code that demonstrates the functionality described in this product. To find the official developer and access detailed reviews and trading results, please visit [ForexRobotEasy Asia Trend EA Review](https://forexroboteasy.com/forex-robot-review/asia-trend-ea-review-advanced-forex-software-for-trend-trading/).

For more information and support, please refer to the official documentation and contact the developers through the MQL5 platform.

# Lightness MT5

Lightness MT5 is an innovative forex software developed by the Forex Robot Easy Team. It is designed to trade on the AUDCAD and CADCHF currency pairs. This code serves as a sample implementation of the Lightness MT5 strategy.

## Prerequisites

To run this code, you will need to have the following libraries installed:

- Trade.mqh
- Expert.mqh
- Trend.mqh

## Global Variables

- `CTrade trade` - Trade class object
- `CTrend trend` - Trend indicator class object

## Expert Initialization Function

The `OnInit()` function is called during the initialization of the expert advisor. In this function, we set the EA parameters:

- `trade.SetExpertMagicNumber(123456)` - Set the magic number for trade operations
- `trade.SetExpertStopLoss(50)` - Set the stop loss value in pips
- `trade.SetExpertTakeProfit(100)` - Set the take profit value in pips

We also apply the trend indicator settings:

- `trend.SetPeriod(14)` - Set the period for calculating trend
- `trend.SetMethod(MODE_SMA)` - Set the method for calculating trend

## Expert Deinitialization Function

The `OnDeinit()` function is called during the deinitialization of the expert advisor. It can be used to perform any necessary cleanup.

## Expert Start Function

The `OnTick()` function is called on every tick of the price chart. In this function, we check if the AUDCAD and CADCHF currency pairs are trending using the `trend.iCustom()` function.

- If the trend is up, we enter a long trade on the respective currency pair using the `trade.Buy()` function.
- If the trend is down, we enter a short trade on the respective currency pair using the `trade.Sell()` function.

## Expert Stop Function

The `OnStop()` function is called before the expert advisor stops. It can be used to perform any necessary actions.

For detailed reviews and trading results of the Lightness MT5 product, please visit the official developer's site: [Lightness MT5 - Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/review-lightness-mt5-innovative-forex-software-for-audcad-and-cadchf-trading/)

Please note that ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in the product. To find the official developer of this product, please refer to MQL5.

# Stenvall MK III ReadMe

This ReadMe file provides an overview of the Stenvall MK III code and how it works. Please note that ForexRobotEasy is not the official developer of this product. We are only providing a sample code that can work as described in the product. To find the official developer of this product, please use MQL5.

## Product Description

Stenvall MK III is a proven forex software designed for long-term investment. It is developed by the Forex Robot Easy Team. For detailed reviews and trading results of this product, please visit [here](https://forexroboteasy.com/forex-robot-review/stenvall-mk-iii-review-proven-forex-software-for-long-term-investment/).

## Code Explanation

### Libraries and Global Variables

The code starts by including the necessary libraries and defining global variables. The `Trade.mqh` library is used for trading operations, and the `PositionInfo.mqh` library is used to retrieve information about open positions.

### Inputs

There are three input parameters that can be adjusted according to the user's requirements:
- `lotSize`: Trading lot size
- `stopLoss`: Stop loss level in points
- `takeProfit`: Take profit level in points

### Initialization Function (OnInit)

The `OnInit` function is called during the initialization of the expert advisor. In this function, the initial trade parameters are set using the `trade` object. The expert magic number is set as 123456, and the deviation in points is set as 10.

### Deinitialization Function (OnDeinit)

The `OnDeinit` function is called during the deinitialization of the expert advisor. It is responsible for closing any open positions before the deinitialization.

### Start Function (OnTick)

The `OnTick` function is called on every tick of the market. It checks if there are any open positions using the `positionInfo` object. If there are no open positions, it executes the trend strategy by calling the `ExecuteTrendStrategy` function. If there are open positions, it executes the countertrend strategy by calling the `ExecuteCounterTrendStrategy` function.

### Trend Strategy (ExecuteTrendStrategy)

The `ExecuteTrendStrategy` function is responsible for executing the trend strategy. It places a buy order and a sell order using the `trade` object with the specified lot size, stop loss level, and take profit level.

### Countertrend Strategy (ExecuteCounterTrendStrategy)

The `ExecuteCounterTrendStrategy` function is responsible for executing the countertrend strategy. It closes all open positions using the `trade` object.

### Conclusion (OnDeinit)

The `OnDeinit` function is called again at the end to close any open positions before deinitialization and print a conclusion message indicating that Stenvall MK III has successfully completed its trading operations.

## Note

Please note that this ReadMe file provides a brief explanation of the code and its functionality. For detailed information on how to use and customize the Stenvall MK III expert advisor, please refer to the official developer or documentation available on MQL5.

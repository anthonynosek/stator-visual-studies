## Data Domain: Estate-Position Statistics
Stator AFM (Visual Studies)

### Domain explanation
Stator exposes position (open, close, open and closed) statistics for the four periods as defined on the position statistics screen within Stator.

### Where are canvases for this domain found within Stator?
1. **Estate - Assets - Markets - Statistics**  
   From the main Stator screen open an Estate and select "Assets/Markets" and "Statistics".

### JSON data format
- Date is in yyyy-MM-dd HH:mm:ss format (HH = 24 hour notation).
- Statistics for two periods of analysis are shown.

```json
[
    {
        "AnalysisClosedPositionsExitedAfter": null,
        "AnalysisDateCalculatedFOR": "2012-07-08 13:59:59",
        "AnalysisPeriodDays": 2761,
        "AnalysisPeriodFROM": "2004-12-13 13:00:00",
        "AnalysisPeriodTO": "2012-07-05 14:00:00",
        "AverageClosedEquityPercentDrawdown": null,
        "AverageDaysInAllPositions": 257.694543297746,
        "AverageDaysInLosingPositions": 344.251666666667,
        "AverageDaysInProfitablePositions": 211.015009380863,
        "AverageLosingPercentLosingPositions": -0.318948951068333,
        "AverageLossLosingPositions": -33798.0255943868,
        "AveragePositionCostPerPosition": 927.164781921728,
        "AveragePositionMargin": 92318.396851175,
        "AveragePositionMarketExposure": 91653.9506411599,
        "AveragePositionPercentageReturn": 0.485970477135232,
        "AverageProfitPercentProfitablePositions": 0.948373769687617,
        "AverageProfitPerPosition": 13603.8257482913,
        "AverageProfitProfitablePositions": 40553.7883037411,
        "AverageProfitToAverageLossRatio": 1.1998863126039,
        "AverageRewardRisk": 0,
        "AverageRiskPerPosition": 0,
        "BarsSinceFirstPosition": 1973,
        "CapitalInvestment": 155648817.091081,
        "CompoundAnnualGrowthRate": 0.0183383389791143,
        "CompoundAnnualGrowthRateWithIncome": 0.0214390361848313,
        "DaysSinceFirstPosition": 2761,
        "DollarReturnPerBar": 11624.9620940796,
        "DollarReturnPerDay": 8307.15328200619,
        "DollarReturnStandardDeviation": 89343.5835041032,
        "ExpectancyPerDollarRisked": 0,
        "KellyPercent": 0.32579144718596,
        "LargestLosingPosition": -754179.134208,
        "LargestPositionMargin": 1788797.073312,
        "LargestPositionMarketExposure": 1771195.01,
        "LargestProfitablePosition": 1400000,
        "LargestProfitablePositionsAsPercentOfTotalProfit": 0.0323846644283734,
        "MaximumNumberOfConsecutiveLosingPositions": 23,
        "MaximumNumberOfConsecutiveProfitablePositions": 73,
        "NegativeReturnZValue": -0.168874111830696,
        "NetProfitLoss": 22936050.2116191,
        "NetProfitLossPercent": 0.147357690474433,
        "NormalisedExpectancy": 0.147457098641009,
        "PercentageReturnRangeFrom": -25.112494237,
        "PercentageReturnRangeTo": 92.480309699,
        "PercentageReturnStandardDeviation": 2.87770855974916,
        "PercentageReturnVariance": 8.2812065548536,
        "PessimisticRateOfReturn": 5.33896121003954,
        "ProfitFactor": 2.13179801539293,
        "SharpeRatio": 0.00637254906060146,
        "SmallestPositionMargin": 0,
        "SmallestPositionMarketExposure": 0,
        "SystemExpectancy": 13613.0029508635,
        "SystemQuality": 6.25632579192338,
        "TotalIncomeReceived": 4154593.406154,
        "TotalLoss": -20278815.3566321,
        "TotalNumberOfBreakevenPositions": 20,
        "TotalNumberOfLosingPositions": 600,
        "TotalNumberOfPositions": 1686,
        "TotalNumberOfPositionsWithNOStopLoss": 1686,
        "TotalNumberOfPositionsWithNOStopLossPercentOfTotal": 1,
        "TotalNumberOfPositionsWithStopLoss": 0,
        "TotalNumberOfPositionsWithStopLossPercentOfTotal": 0,
        "TotalNumberOfProfitablePositions": 1066,
        "TotalPositionCosts": 1563199.82232003,
        "TotalProfit": 43230338.331788,
        "TotalTurnover": 331993171.758269
    },
    {
        "AnalysisClosedPositionsExitedAfter": null,
        "AnalysisDateCalculatedFOR": "2013-06-08 13:59:59",
        "AnalysisPeriodDays": 3006,
        "AnalysisPeriodFROM": "2004-12-13 13:00:00",
        "AnalysisPeriodTO": "2013-03-07 13:00:00",
        "AverageClosedEquityPercentDrawdown": null,
        "AverageDaysInAllPositions": 271.988148984199,
        "AverageDaysInLosingPositions": 351.29793977813,
        "AverageDaysInProfitablePositions": 229.834525939177,
        "AverageLosingPercentLosingPositions": -0.318515125408875,
        "AverageLossLosingPositions": -34757.193944019,
        "AveragePositionCostPerPosition": 943.940034603857,
        "AveragePositionMargin": 92850.5166576244,
        "AveragePositionMarketExposure": 92180.3191635299,
        "AveragePositionPercentageReturn": 0.596185597792325,
        "AverageProfitPercentProfitablePositions": 1.12495238541503,
        "AverageProfitPerPosition": 15160.7819236409,
        "AverageProfitProfitablePositions": 43660.5967897178,
        "AverageProfitToAverageLossRatio": 1.25616000129467,
        "AverageRewardRisk": 0,
        "AverageRiskPerPosition": 0,
        "BarsSinceFirstPosition": 2148,
        "CapitalInvestment": 164531115.51731,
        "CompoundAnnualGrowthRate": 0.0185344127587004,
        "CompoundAnnualGrowthRateWithIncome": 0.0212243368807241,
        "DaysSinceFirstPosition": 3006,
        "DollarReturnPerBar": 12506.9392777894,
        "DollarReturnPerDay": 8937.09433422879,
        "DollarReturnStandardDeviation": 92644.890993676,
        "ExpectancyPerDollarRisked": 0,
        "KellyPercent": 0.337113818530744,
        "LargestLosingPosition": -754179.134208,
        "LargestPositionMargin": 1788797.073312,
        "LargestPositionMarketExposure": 1771195.01,
        "LargestProfitablePosition": 1400000,
        "LargestProfitablePositionsAsPercentOfTotalProfit": 0.0286811502368646,
        "MaximumNumberOfConsecutiveLosingPositions": 23,
        "MaximumNumberOfConsecutiveProfitablePositions": 73,
        "NegativeReturnZValue": -0.198664035822948,
        "NetProfitLoss": 26864905.5686917,
        "NetProfitLossPercent": 0.16328161080185,
        "NormalisedExpectancy": 0.163377958921092,
        "PercentageReturnRangeFrom": -25.112494237,
        "PercentageReturnRangeTo": 92.480309699,
        "PercentageReturnStandardDeviation": 3.00097395747892,
        "PercentageReturnVariance": 9.00584469346671,
        "PessimisticRateOfReturn": 6.32225836758467,
        "ProfitFactor": 2.22565274397375,
        "SharpeRatio": 0.00617613248942383,
        "SmallestPositionMargin": 0,
        "SmallestPositionMarketExposure": 0,
        "SystemExpectancy": 15169.7278962915,
        "SystemQuality": 6.89268092893685,
        "TotalIncomeReceived": 4202868.156154,
        "TotalLoss": -21931789.378676,
        "TotalNumberOfBreakevenPositions": 23,
        "TotalNumberOfLosingPositions": 631,
        "TotalNumberOfPositions": 1772,
        "TotalNumberOfPositionsWithNOStopLoss": 1772,
        "TotalNumberOfPositionsWithNOStopLossPercentOfTotal": 1,
        "TotalNumberOfPositionsWithStopLoss": 0,
        "TotalNumberOfPositionsWithStopLossPercentOfTotal": 0,
        "TotalNumberOfProfitablePositions": 1118,
        "TotalPositionCosts": 1672661.74131803,
        "TotalProfit": 48812547.2109045,
        "TotalTurnover": 353551956.6678
    }
]
```

### Accessing the data from a visual study
Inserted code (HTML)
- This code is automatically inserted into the page HTML for single sketch studies only.
- Variable 'dataStatistics' contains the JSON data for position statistics.

```javascript
function getJsonData(url) {
       var data = null;
       $.ajax({
               'url': url,
               'async': false,
               'global': false,
               'dataType': "json",
               'success': function(json) {
                               data = json;
                           }
       });
       return data;
}
</script>

<script>
var dataStatistics = getJsonData('##JSON_DATA_FILE##');
</script>
```

## Visual studies in this repository for this data-domain
<i>None at the time of writing.</i>
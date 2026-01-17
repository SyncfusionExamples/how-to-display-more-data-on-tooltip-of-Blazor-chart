# how-to-display-more-data-on-tooltip-of-Blazor-chart

This article explains how to display more data on tooltip of a Blazor Chart Component.

**Display more information on tooltip in Blazor chart**

In [Blazor Chart](https://www.syncfusion.com/blazor-components/blazor-charts), You can customize the tooltip  to display specific information by using the [TooltipMappingName](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartSeries.html#Syncfusion_Blazor_Charts_ChartSeries_TooltipMappingName) property in the series. By default, the tooltip shows information about the x and y values in data points.

In the following code example illustrates this. 

**Index.razor**

```cshtml

@using Syncfusion.Blazor.Charts

<SfChart Title="Unemployment Rates 1975-2010">

    <ChartSeriesCollection>
        <ChartSeries DataSource="StepChartValues" Type="ChartSeriesType.StepLine" XName="Year" YName="YValue" TooltipMappingName="Text">
            <ChartMarker Visible="true" Width="10" Height="10">
            </ChartMarker>
        </ChartSeries>
    </ChartSeriesCollection>

    <ChartTooltipSettings Enable="true" Format="${point.tooltip}">        
    </ChartTooltipSettings>

</SfChart>

@code {

    public List<StepChartData> StepChartValues = new List<StepChartData>
    {
        new StepChartData { Year = "1975", YValue = 16, Text = "Unemployment rate in 1975 : 16%" },
        new StepChartData { Year = "1980", YValue = 12.5, Text = "Unemployment rate in 1980 : 12.5%" },
        new StepChartData { Year = "1985", YValue = 19, Text = "Unemployment rate in 1985 : 19%" },
        new StepChartData { Year = "1990", YValue = 14.4, Text = "Unemployment rate in 1990 : 14.4%" },
        new StepChartData { Year = "1995", YValue = 11.5, Text = "Unemployment rate in 1995 : 11.5%" },
        new StepChartData { Year = "2000", YValue = 14, Text = "Unemployment rate in 2000 : 14%" },
        new StepChartData { Year = "2005", YValue = 10, Text = "Unemployment rate in 2005 : 10%" },
        new StepChartData { Year = "2010", YValue = 16 , Text = "Unemployment rate in 2010 : 16%"}
    };

    public class StepChartData
    {
        public string Year { get; set; }
        public double YValue { get; set; }
        public string Text{ get; set; }
    }
}

```

The following screenshot illustrates the output of the above code snippet.

**Output:**

![](/tooltip-template.png)

**Conclusion**

I hope you enjoyed learning how to display more data on tooltip of Blazor Chart Component.

You can refer to our [Blazor Chart feature tour](https://www.syncfusion.com/blazor-components/blazor-charts) page to know about its other groundbreaking feature representations and [documentation](https://blazor.syncfusion.com/documentation/chart/getting-started), and how to quickly get started for configuration specifications. You can also explore our [Blazor Chart example](https://blazor.syncfusion.com/demos/chart/line?theme=bootstrap5) to understand how to create and manipulate data.

For current customers, you can check out our components from the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/blazor) to check out our other controls.

If you have any queries or require clarifications, please let us know in the comments section below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [support portal](https://support.syncfusion.com/create), or [feedback portal](https://www.syncfusion.com/feedback/blazor-components?control=charts). We are always happy to assist you!
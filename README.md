# Display More Data in a Syncfusion Blazor Chart Tooltip Using a Custom Template

## Overview

This sample demonstrates how to customize tooltips in Syncfusion [Blazor Charts](https://www.syncfusion.com/blazor-components/blazor-charts) by using the `ChartTooltipSettings.Template` property. Instead of displaying only the default tooltip content, the chart renders custom HTML markup within the tooltip and accesses the selected data point through `ChartTooltipInfo`.

The sample visualizes unemployment-rate data using a step-line chart and displays the corresponding year and value inside a formatted table when users hover over a data point. This approach is useful when applications need to present additional contextual information, custom layouts, branding, or multiple fields beyond the default chart tooltip content.

## Key Features

- Uses the `SfChart` component to render chart data.
- Configures a chart series using:
  - `ChartSeries`
  - `Type="ChartSeriesType.StepLine"`
  - `DataSource="StepChartValues"`
  - `XName="Year"`
  - `YName="YValue"`
- Displays markers for individual data points using:
  - `ChartMarker`
  - `Visible="true"`
  - `Width="10"`
  - `Height="10"`
- Enables tooltip support through:
  - `ChartTooltipSettings`
  - `Enable="true"`
- Customizes tooltip content using:
  - `ChartTooltipSettings.Template`
- Accesses the current tooltip context through:
  - `ChartTooltipInfo`
- Displays point information using:
  - `data.X`
  - `data.Y`
- Uses standard HTML table elements inside the tooltip template to present formatted data.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download this repository.
2. Open the following project file:

   `TooltipTemplate/TooltipTemplate.csproj`

3. Restore NuGet packages.
4. Build the project.
5. Run the application using **Ctrl+F5**.
6. Hover over the chart data points to view the customized tooltip template.

**Visual Studio Code**

1. Clone or download this repository.
2. Open the repository folder in Visual Studio Code.
3. Open the integrated terminal.
4. Navigate to the project directory:

```bash
cd ToolTipTemplate/TooltipTemplate
```

5. Restore NuGet packages:

```bash
dotnet restore
```

6. Run the application:

```bash
dotnet run
```

7. Open the local application URL and hover over the chart points to view the customized tooltip template.

## Project Structure

`Pages/Index.razor` - Implements the `SfChart`, `ChartSeries`, `ChartMarker`, `ChartTooltipSettings`, tooltip template markup, sample data collection, and `StepChartData` model used by the demonstration.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Review the official Syncfusion Blazor Chart tooltip documentation: https://help.syncfusion.com/chart-sdk/blazor/charts/tool-tip

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.
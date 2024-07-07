<!-- TOC start (generated with https://github.com/derlin/bitdowntoc) -->

- [Data Visualization](#data-visualization)
  - [Histograms](#histograms)
    - [Definition](#definition)
    - [Constructing a Histogram](#constructing-a-histogram)
    - [Use Cases](#use-cases)
    - [Examples](#examples)
    - [Best Practices](#best-practices)
    - [Types of Histograms](#types-of-histograms)
  - [Box Plots](#box-plots)
    - [Definition](#definition-1)
    - [Constructing a Boxplot](#constructing-a-boxplot)
    - [Use Cases](#use-cases-1)
    - [Examples](#examples-1)
    - [Best Practices](#best-practices-1)
  - [Scatter Plots](#scatter-plots)
    - [Definition](#definition-2)
    - [Constructing a Scatter Plot](#constructing-a-scatter-plot)
    - [Use Cases](#use-cases-2)
    - [Examples](#examples-2)
    - [Best Practices](#best-practices-2)
  - [Heat Maps](#heat-maps)
    - [Definition](#definition-3)
    - [Use Cases](#use-cases-3)
    - [Examples](#examples-3)
    - [Best Practices](#best-practices-3)
  - [Bubble Charts](#bubble-charts)
    - [Definition](#definition-4)
    - [Constructing a Bubble Chart](#constructing-a-bubble-chart)
    - [Use Cases](#use-cases-4)
    - [Examples](#examples-4)
    - [Best Practices](#best-practices-4)
  - [Bar Charts](#bar-charts)
    - [Definition](#definition-5)
    - [Constructing a Bar Chart](#constructing-a-bar-chart)
    - [Types of Bar Charts](#types-of-bar-charts)
    - [Use Cases](#use-cases-5)
    - [Examples](#examples-5)
    - [Best Practices](#best-practices-5)
  - [Distribution Plot](#distribution-plot)
    - [Purpose](#purpose)
    - [Construction](#construction)
    - [Use Cases](#use-cases-6)
    - [Best Practices](#best-practices-6)
  - [Pair Plot](#pair-plot)
    - [Purpose](#purpose-1)
    - [Construction](#construction-1)
    - [Use Cases](#use-cases-7)
    - [Best Practices](#best-practices-7)
  - [Line Graph](#line-graph)
    - [Purpose](#purpose-2)
    - [Types](#types)
    - [Construction](#construction-2)
    - [Use Cases](#use-cases-8)
    - [Best Practices](#best-practices-8)
  - [Pie Chart](#pie-chart)
    - [Purpose](#purpose-3)
    - [Types](#types-1)
    - [Construction](#construction-3)
    - [Use Cases](#use-cases-9)
    - [Best Practices](#best-practices-9)
  - [Doughnut Chart](#doughnut-chart)
    - [Purpose](#purpose-4)
    - [Types](#types-2)
    - [Construction](#construction-4)
    - [Use Cases](#use-cases-10)
    - [Best Practices](#best-practices-10)
  - [Area Chart](#area-chart)
    - [Purpose](#purpose-5)
    - [Types](#types-3)
    - [Use Cases](#use-cases-11)
    - [Best Practices](#best-practices-11)

<!-- TOC end -->

<!-- TOC --><a name="data-visualization"></a>
# Data Visualization

<!-- TOC --><a name="histograms"></a>
## Histograms

<!-- TOC --><a name="definition"></a>
### Definition
- A histogram visualizes data distribution across continuous classes.
- Represented with rectangular bars:
  - Widths equal to class intervals.
  - Areas proportional to frequencies.
- A graphic of a grouped frequency distribution with continuous classes.
- Provides:
  - Estimate of value distribution.
  - Extremes and gaps.
  - Out-of-the-ordinary numbers.
- Useful for understanding probability distribution.

<!-- TOC --><a name="constructing-a-histogram"></a>
### Constructing a Histogram
- Group data into class intervals ("bins").
- Plot intervals on the x-axis representing the data range.
- Construct rectangles with bases along intervals for each class.
- Height of rectangles (y-axis) represents frequency for each class interval.
- Rectangles are adjacent, covering spaces between class boundaries.

<!-- TOC --><a name="use-cases"></a>
### Use Cases
- Illustrate or compare numerical data distribution across intervals.
- Aid in visualizing key meanings and patterns in large data sets.
- Assist in business or organizational decision-making.

<!-- TOC --><a name="examples"></a>
### Examples
- Distribution of salaries in an organization.
- Distribution of height in a student batch or student performance on an exam.
- Customers by company size.
- Frequency of a product problem.

<!-- TOC --><a name="best-practices"></a>
### Best Practices
- Analyse various data groups by creating multiple histograms.
- Use color to break down compartments, showing a second set of categories.

<!-- TOC --><a name="types-of-histograms"></a>
### Types of Histograms

- **Normal Distribution**
  - Probability of points occurring on either side of the mean is the same.

- **Bimodal Distribution**
  - Two peaks in the distribution.
  - Segment data before analyzing as normal distributions.

- **Right-skewed Distribution**
  - Also known as positively skewed distribution.
  - More data values on the left, fewer on the right.
  - Often results when data have a range boundary on the left side.

- **Left-skewed Distribution**
  - Also known as negatively skewed distribution.
  - More data values on the right, fewer on the left.
  - Often results when data have a range limit on the right side.
  - Alternative name: right-tailed distribution.

- **Random Distribution**
  - Characterized by no clear pattern and multiple peaks.
  - Several distinct data attributes may be blended.
  - Data should be partitioned and investigated independently.

- **Edge Peak Distribution**
  - Additional peak at the edge of the distribution.
  - Often indicates incorrect data plotting or collection.
  - Example: a few extreme views on a survey.

- **Comb Distribution**
  - Resembles a comb with alternating high and low peaks.
  - Can result from rounding off objects.
  - Example: measuring water height to nearest 10 cm, but class width is 5 cm.

<!-- TOC --><a name="box-plots"></a>
## Box Plots

<!-- TOC --><a name="definition-1"></a>
### Definition
- Box-and-whisker plots (boxplots) display data distributions using five summary statistics:
  - Minimum
  - First quartile (Q1)
  - Median
  - Third quartile (Q3)
  - Maximum
- Visual representation of data helps determine:
  - Distribution shape
  - Central value
  - Variability

<!-- TOC --><a name="constructing-a-boxplot"></a>
### Constructing a Boxplot
- **Box**: Shows median, Q1, and Q3.
- **Whiskers**: Extend to minimum and maximum points, or up to 1.5 × IQR (Interquartile Range) from Q1 and Q3.
- **Outliers**: Points beyond 1.5 × IQR can be marked as suspected outliers.

<!-- TOC --><a name="use-cases-1"></a>
### Use Cases
- Demonstrates skewness and potential outliers in a data set.
- Useful for comparing large data sets.

<!-- TOC --><a name="examples-1"></a>
### Examples
- Gas efficiency of vehicles.
- Time spent reading across readers.

<!-- TOC --><a name="best-practices-1"></a>
### Best Practices
- Cover points within the box to highlight outliers.
- Compare box plots across categorical dimensions for quick dataset comparisons.

<!-- TOC --><a name="scatter-plots"></a>
## Scatter Plots

<!-- TOC --><a name="definition-2"></a>
### Definition
- Used to observe relationships between two quantitative variables.
- Identifies possible correlations between data points.
- Shows whether variables are predictors of each other or fluctuate independently.
- Can include trend lines or cluster analysis.

<!-- TOC --><a name="constructing-a-scatter-plot"></a>
### Constructing a Scatter Plot
- Uses Cartesian coordinates.
- Categories represented by circles, with:
  - Colour indicating category.
  - Size indicating numerical volume.
- Can represent additional variables using different colours.

<!-- TOC --><a name="use-cases-2"></a>
### Use Cases
- Display relationships between variables.

<!-- TOC --><a name="examples-2"></a>
### Examples
- Time spent on social media vs. churn rate.
- Salary vs. years spent at a company.

<!-- TOC --><a name="best-practices-2"></a>
### Best Practices
- Analyze clusters to find segments.
- Use highlight actions to identify common characteristics among points.
- Customize individual marks for clarity.

<!-- TOC --><a name="heat-maps"></a>
## Heat Maps

<!-- TOC --><a name="definition-3"></a>
### Definition
- Two-dimensional graphics showing data trends through colour shading.
- Part-to-whole charts with values represented by colours.
- Offers quick visual representation of complex data sets.
- Highlights trends and patterns.

<!-- TOC --><a name="use-cases-3"></a>
### Use Cases
- Show large data set trends.
- Guide users to important data parts.

<!-- TOC --><a name="examples-3"></a>
### Examples
- Average monthly temperatures over years.
- Departments with highest attrition over time.
- Website or product page traffic.
- Population density in a geographical location.

<!-- TOC --><a name="best-practices-3"></a>
### Best Practices
- Select appropriate colour schemes.
- Include a legend to explain colour meanings.

<!-- TOC --><a name="bubble-charts"></a>
## Bubble Charts

<!-- TOC --><a name="definition-4"></a>
### Definition
- Show relationships between variables using bubbles.
- Bubbles represent data points in three dimensions:
  - X-axis, Y-axis, and bubble size.

<!-- TOC --><a name="constructing-a-bubble-chart"></a>
### Constructing a Bubble Chart
- Place bubbles in Cartesian coordinates based on two variables.
- Bubble size represents a third variable.
- Additional data sets can be represented using different bubble colours.

<!-- TOC --><a name="use-cases-4"></a>
### Use Cases
- Compare and show correlations between variables.
- Identify data patterns and trends.

<!-- TOC --><a name="examples-4"></a>
### Examples
- CPC vs. Conversions vs. share of total conversions in AdWords analysis.
- Life expectancy vs. GDP per capita vs. population size.

<!-- TOC --><a name="best-practices-4"></a>
### Best Practices
- Add colour for extra depth.
- Ensure bubble sizes are proportional.
- Overlay bubbles on maps for geographic context.

<!-- TOC --><a name="bar-charts"></a>
## Bar Charts

<!-- TOC --><a name="definition-5"></a>
### Definition
- Graphical depiction of numerical data using rectangles (bars) with equal widths and varied heights.
- Handles data efficiently in statistics.

<!-- TOC --><a name="constructing-a-bar-chart"></a>
### Constructing a Bar Chart
- X-axis: Horizontal line, categories of data items.
- Y-axis: Vertical line, frequency values.
- Determine bar heights based on data values.

<!-- TOC --><a name="types-of-bar-charts"></a>
### Types of Bar Charts
- **Horizontal Bar Charts**: Bars are horizontal, categories on the Y-axis.
- **Vertical Bar Charts**: Bars are vertical, categories on the X-axis.
- **Grouped Bar Charts**: Compare multiple groups, use different colours for each value.
- **Stacked Bar Charts**: Show component parts of data, different colours within bars.

<!-- TOC --><a name="use-cases-5"></a>
### Use Cases
- Display quantitative data relationships.
- Study trends over extended periods.

<!-- TOC --><a name="examples-5"></a>
### Examples
- Show relationships between variables clearly and quickly.
- Efficiently present large data sets.

<!-- TOC --><a name="best-practices-5"></a>
### Best Practices
- Use a common zero-valued baseline.
- Maintain rectangular shapes for bars.
- Order categories thoughtfully and use colour wisely.

<!-- TOC --><a name="distribution-plot"></a>
## Distribution Plot

### Purpose 
- Visually assess the distribution of sample data by contrasting actual data with theoretical values.

### Construction
  - Use 1 or 2 dimensions with one measure.
  - One dimension gives a single line visualization.
  - Two dimensions produce separate lines for each value of the outer dimension.

### Use Cases
  - Height distribution in a population.
  - Income distribution in an economy.
  - Test scores listed by percentile.

### Best Practices
  - Equal class widths.
  - Mutually exclusive, non-overlapping class intervals.
  - Avoid open-ended classes at the lower and upper limits (e.g., <10, >100).

<!-- TOC --><a name="pair-plot"></a>
## Pair Plot

### Purpose 
- Extend histograms and scatter plots to show relationships between variables.

### Construction
  - Create an m x m figure for m attributes.
  - Diagonal subplots: univariate histograms.
  - Off-diagonal subplots: scatter plots for attribute pairs.

### Use Cases
  - Identify distinct clusters or optimal attribute combinations.
  - Socio-economic data analysis.

### Best Practices
  - Use different color palettes.
  - Different markers for each color level.

<!-- TOC --><a name="line-graph"></a>
## Line Graph

### Purpose
- Depict changes over time using points and lines.

### Types
  - Simple Line Graph: Single line.
  - Multiple Line Graph: Several lines on the same axes.
  - Compound Line Graph: Breaks down information into components.

### Construction
- Plot points and connect with lines.

### Use Cases
  - Track changes over time.
  - Compare changes for different groups.

### Best Practices
  - Connect adjacent values only.
  - Use comparable interval sizes.
  - Ensure the baseline makes sense.
  - Use same scales for comparing data sets.

<!-- TOC --><a name="pie-chart"></a>
## Pie Chart

### Purpose
- Summarize nominal data or show values of a single variable.
  
### Types
  - Simple Pie Chart.
  - Exploded Pie Chart.
  - Pie of Pie.
  - Bar of Pie.

### Construction
- Calculate percentage and degrees for each category.
  
### Use Cases
  - Voting preference by age group.
  - Market share of cloud providers.

### Best Practices
  - Limit pie wedges.
  - Use on maps for geographic trends.

<!-- TOC --><a name="doughnut-chart"></a>
## Doughnut Chart

### Purpose
- Simplify reading pie charts with a central hole.

### Types
  - Normal Doughnut Chart.
  - Exploded Doughnut Chart.

### Construction
- Like pie charts, can display multiple data series.

### Use Cases
  - Android OS market share.
  - Monthly sales by channel.

### Best Practices
  - Limit slices to five or less.
  - Use informative labels.
  - Sort slices for clarity.

<!-- TOC --><a name="area-chart"></a>
## Area Chart

### Purpose
- Show the relationship between numerical values and the development of a second variable over time.
  
### Types
  - Overlapping Area Chart: Compare values of different groups.
  - Stacked Area Chart: Track total value and breakdown by groups.
  
### Use Cases
  - Track trends over time (e.g., company revenue, enrollment).
  - Compare contributions of different categories (e.g., department sizes, support tickets).

### Best Practices
  - Start the y-axis at 0.
  - Use translucent, contrasting colors.
  - Place highly variable data at the top during stacking.
  - Use 100% stacked area charts for part-to-whole relationships when the total is unimportant.
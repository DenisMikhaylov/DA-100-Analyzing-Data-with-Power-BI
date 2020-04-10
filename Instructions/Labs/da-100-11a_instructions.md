

### Lab 11A

Data Analysis in Power BI Desktop

# Overview

**The estimated time to complete the lab is 45 minutes**

In this lab, you will create the **Sales Exploration** report.

In this lab, you learn how to:

* Create animated scatter charts

* Use a visual to forecast values

* Work with the decomposition tree visual

* Work with the key influences visual

# Exercise 1: Create the Report

In this exercise, you will create the **Sales Exploration** report.

### Task 1: Create the report

In this task, you will create the **Sales Exploration** report.

1. Open the Power BI Desktop, and dismiss the welcome screen.

	![Picture 2](Linked_image_Files/PowerBI_Lab11A_image1.png)

2. Save the file to the **D:\DA100\MySolution** folder, as **Sales Exploration**.

	![Picture 1](Linked_image_Files/PowerBI_Lab11A_image2.png)

3. Create a live connection to your **Sales Analysis** dataset.

	*Tip: Use the **Get Data** command on the **Home** ribbon tab, and then select **Power BI Datasets***.

	![Picture 6](Linked_image_Files/PowerBI_Lab11A_image3.png)

	*You now create four report pages, and on each page you’ll work with a different visual to analyze and explore data*.

# Exercise 2: Create a Scatter Chart

In this exercise, you will create a scatter chart that can be animated.

### Task 1: Create an animated scatter chart

In this task, you will create a scatter chart that can be animated.

1. Rename **Page 1** as **Scatter Cha****rt**.

	![Picture 67](Linked_image_Files/PowerBI_Lab11A_image4.png)

5. Add a **Scatter Chart** visual to the report page, and then reposition and resize it so it fills the entire page.

	![Picture 37](Linked_image_Files/PowerBI_Lab11A_image5.png)

	![Picture 75](Linked_image_Files/PowerBI_Lab11A_image6.png)

6. Add the following fields to the visual wells:

	* Legend: **Reseller | Business Type**

	* X Axis: **Sales | Sales** 

	* Y Axis: **Sales | Profit Margin**

	* Size: **Sales | Quantity**

	* Play Axis: **Date | Quarter**

	![Picture 39](Linked_image_Files/PowerBI_Lab11A_image7.png)

	*The chart can be animated when a field is added to the **Play Axis** well*.

7. In the **Filters** pane, add the **Product | Category** field to the **Filters On This Page** well.

8. In the filter card, filter by **Bikes**.

	![Picture 40](Linked_image_Files/PowerBI_Lab11A_image8.png)

9. To animate the chart, at the bottom left corner, click **Play**.

	![Picture 41](Linked_image_Files/PowerBI_Lab11A_image9.png)

10. Watch the entire animation cycle from **FY2018 Q1** to **FY2020 Q4**.

	*The scatter chart allows understanding the measure values simultaneously: in this case, order quantity, sales revenue, and profit margin*.

	*Each bubble represents a reseller business type. Changes in the bubble size reflect increased or decreased order quantities. While horizontal movements represent increases/decreases in sales revenue, and vertical movements represent increases/decreases in profitability*.

11. When the animation stops, click one of the bubbles to reveal its tracking over time.

12. Hover the cursor over any bubble to reveal a tooltip describing the measure values for the reseller type at that point in time.

13. In the **Filters** pane, filter by **Clothing** only, and notice that it produces a very different result.

14. Save the Power BI Desktop file.

# Exercise 3: Create a Forecast

In this exercise, you will create a forecast to determine possible future sales revenue.

### Task 1: Create a forecast

In this task, you will create a forecast to determine possible future sales revenue.

1. Add a new page, and then rename the page to **Forecast**.

	![Picture 66](Linked_image_Files/PowerBI_Lab11A_image10.png)

16. Add a **Line Chart** visual to the report page, and then reposition and resize it so it fills the entire page.

	![Picture 45](Linked_image_Files/PowerBI_Lab11A_image11.png)

	![Picture 74](Linked_image_Files/PowerBI_Lab11A_image12.png)

17. Add the following fields to the visual wells:

	* Axis: **Date | Date**

	* Values: **Sales | Sales** 

	![Picture 46](Linked_image_Files/PowerBI_Lab11A_image13.png)

18. In the **Filters** pane, add the **Date | Year** field to the **Filters On This Page** well.

19. In the filter card, filter by two years: **FY2019** and **FY2020**.

	![Picture 47](Linked_image_Files/PowerBI_Lab11A_image14.png)

	*When forecasting over a time line, you will need at least two cycles (years) of data to produce an accurate and stable forecast*.

20. Add also the **Product | Category** field to the **Filters On This Page** well, and filter by **Bikes**.

	![Picture 48](Linked_image_Files/PowerBI_Lab11A_image15.png)

21. To add a forecast, beneath the **Visualizations** pane, select the **Analytics** pane.

	![Picture 49](Linked_image_Files/PowerBI_Lab11A_image16.png)

22. Expand the **Forecast** section.

	![Picture 50](Linked_image_Files/PowerBI_Lab11A_image17.png)

	*If the **Forecast** section is not available, it’s probably because the visual hasn’t been correctly configured. Forecasting is only available when two conditions are met: the axis has a single field of type date, and there’s only one value field*.

23. Click **Add**.

	![Picture 51](Linked_image_Files/PowerBI_Lab11A_image18.png)

24. Configure the following forecast properties:

	* Forecast length: 1 month

	* Confidence interval: 80%

	* Seasonality: 365

25. Click **Apply**.

	![Picture 52](Linked_image_Files/PowerBI_Lab11A_image19.png)

26. In the line visual, notice that the forecast has extended one month beyond the history data.

	*The gray area represents the confidence. The wider the confidence, the less stable—and therefore the less accurate—the forecast is likely to be*.

	*When you know the length of the cycle, in this case annual, you should enter the seasonality points. Sometimes it could be weekly (7), or monthly (30)*.

27. In the **Filters** pane, filter by **Clothing** only, and notice that it produces a different result.

28. Save the Power BI Desktop file.

# Exercise 4: Work with a Decomposition Tree

In this exercise, you will create a decomposition tree to explore the relationships between reseller geography and profit margin.

### Task 1: Work with a decomposition tree

In this task, you will create a decomposition tree to explore the relationships between reseller geography and profit margin.

1. Add a new page, and then rename the page to **Decomposition Tree**.

	![Picture 65](Linked_image_Files/PowerBI_Lab11A_image20.png)

30. On the **Insert** ribbon, from inside the **AI Visuals** group, click **Decomposition Tree**.

	*Tip: The AI visuals are also available in the **Visualizations** pane*.

	![Picture 54](Linked_image_Files/PowerBI_Lab11A_image21.png)

31. Reposition and resize the visual so it fills the entire page.

	![Picture 73](Linked_image_Files/PowerBI_Lab11A_image22.png)

32. Add the following fields to the visual wells:

	* Analyze: **Sales | Profit Margin**

	* Explain By: **Reseller | Geography** (the entire hierarchy)

	![Picture 57](Linked_image_Files/PowerBI_Lab11A_image23.png)

33. In the **Filters** pane, add the **Date | Year** field to the **Filters On This Page** well, and set the filter to **FY2020**.

	![Picture 59](Linked_image_Files/PowerBI_Lab11A_image24.png)

34. In the decomposition tree visual, notice the root of the tree: **Profit Margin** at -0.94%

	![Picture 60](Linked_image_Files/PowerBI_Lab11A_image25.png)

35. Click the plus icon, and in the context menu, select **High Value**.

	![Picture 61](Linked_image_Files/PowerBI_Lab11A_image26.png)

36. Notice that the decision tree presents resellers, ordered from highest profit margin.

37. To remove the level, at the top of visual, beside the **Reseller** label, click **X**.

	![Picture 62](Linked_image_Files/PowerBI_Lab11A_image27.png)

38. Click the plus icon again, and then expand to the **Country-Region** level.

39. Expand from the **United States** to the **State-Province** level.

40. Use the down-arrow located at the bottom of the visual for **State-Province**, and then scroll to the lower profitable states.

41. Notice that **New York** state has negative profitability.

42. Expand from **New York** to the **Reseller** level.

43. Notice that it is easy to isolate root cause.

	![Picture 63](Linked_image_Files/PowerBI_Lab11A_image28.png)

	***United States** is not producing profit in **FY2020**. **New York** is one state not achieving positive profit, and it’s due to four resellers paying less than standard costs for their goods.*

44. Save the Power BI Desktop file.

# Exercise 5: Work with Key Influencers

In this exercise, you will use the Key Influencers AI visual to determine what influences profitability within reseller business types and geography.

### Task 1: Work with key influencers

In this task, you will use the Key Influencers AI visual to determine what influences profitability within reseller business types and geography.

1. Add a new page, and then rename the page to **Key Influencers**.

	![Picture 64](Linked_image_Files/PowerBI_Lab11A_image29.png)

46. On the **Insert** ribbon, from inside the **AI Visuals** group, click **Key Influencers**.

	*Tip: The AI visuals are also available in the **Visualizations** pane*.

	![Picture 71](Linked_image_Files/PowerBI_Lab11A_image30.png)

47. Reposition and resize the visual so it fills the entire page.

	![Picture 72](Linked_image_Files/PowerBI_Lab11A_image31.png)

48. Add the following fields to the visual wells:

	* Analyze: **Sales | Profit Margin**

	* Explain By: **Reseller | Business Type** and **Reseller | Geography** (the entire hierarchy)

	* Expand By: **Sales | Quantity**

	![Picture 3](Linked_image_Files/PowerBI_Lab11A_image32.png)

49. At the top-left of the visual, notice that **Key Influencers** is in focus, and the specific influence is set to understand what includes profit margin to increase.

	![Picture 76](Linked_image_Files/PowerBI_Lab11A_image33.png)

50. Review the result, which is that the city of **Bothel** is more likely to increase.

51. Modify the target to determine what influences profit margin to decrease.

	![Picture 77](Linked_image_Files/PowerBI_Lab11A_image34.png)

52. Review the result.

53. To detect segments, at the top-left, select **Top Segments**.

	![Picture 78](Linked_image_Files/PowerBI_Lab11A_image35.png)

54. Notice that the target is now to determine segments when profit margin is likely to be high.

55. When the visual displays the segments (as circles), click one of them to reveal information about it.

56. Review the segment results.

### Finish up

In this task, you will complete the lab.

1. Save the Power BI Desktop file.

58. Select the **Scatter Chart** page.

59. Publish the file to your **Sales Analysis** workspace.

60. Close Power BI Desktop.

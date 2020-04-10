

### Lab 09A

Designing a Report in Power BI Desktop, Part 2

# Overview

**The estimated time to complete the lab is 45 minutes**

In this lab, you will enhance the **Sales Report** with advanced design features.

In this lab, you learn how to:

* Sync slicers

* Create a drillthrough page

* Apply conditional formatting

* Create and use bookmarks

# Exercise 1: Configure Sync Slicers

In this exercise, you will sync the report page slicers.

### Task 1: Sync slicers

In this task, you will sync the **Year** and **Region** slicers.

*You will continue the development of the report that you commenced designing in **Lab 08A***.

1. In Power BI Desktop, in the **Sales Report** file, on the **Overview** page, set the **Year** slicer to **FY2018**.

2. Go to the **My Performance** page, and then notice that the **Year** slicer is a different value.

	*When slicers aren’t synced, it can contribute to misrepresentation of data and frustration for report users. You’ll now sync the report slicers*.

3. Go to the **Overview** page, and then select the **Year** slicer.

4. On the **View** ribbon tab, from inside the **Show Panes** group, click **Sync Slicers**.

	![Picture 1](Linked_image_Files/PowerBI_Lab09A_image1.png)

5. In the **Sync Slicers** pane (at the left of the **Visualizations** pane), in the second column (which represents syncing), check the checkboxes for the **Overview** and **My Performance** pages.

	![Picture 93](Linked_image_Files/PowerBI_Lab09A_image2.png)

6. On the **Overview** page, select the **Region** slicer.

7. Sync the slicer with the **Overview** and **Profit** pages.

	![Picture 94](Linked_image_Files/PowerBI_Lab09A_image3.png)

8. Test the sync slicers by selecting different filter options, and then verifying that the synced slicers filter by the same options.

9. To close the **Sync Slicer** page, click the **X** located at the top-right of the pane.

	![Picture 98](Linked_image_Files/PowerBI_Lab09A_image4.png)

# Exercise 2: Configure Drill Through

In this exercise, you will create a new page and configure it as a drill through page. When you’ve completed the design, the page will look like the following:  

![Picture 69](Linked_image_Files/PowerBI_Lab09A_image5.png)

### Task 1: Create a drill through page

In this task, you will create a new page and configure it as a drill through page.

1. Add a new report page named **Product Details**.

	![Picture 95](Linked_image_Files/PowerBI_Lab09A_image6.png)

11. Right-click the **Product Details** page tab, and then select **Hide Page**.

	![Picture 97](Linked_image_Files/PowerBI_Lab09A_image7.png)

	*Report users won’t be able to go to the drill through page directly. They’ll need to access it from visuals on other pages. You’ll learn how to drill through to the page in the final exercise of this lab*.

12. Beneath the **Visualizations** pane, in the **Drill Through** section, add the **Product | Category** field to the **Add Drill-Through Fields Here** box.

	![Picture 96](Linked_image_Files/PowerBI_Lab09A_image8.png)

13. To test the drill through page, in the drill through filter card, select **Bikes**.

	![Picture 99](Linked_image_Files/PowerBI_Lab09A_image9.png)

14. At the top-left of the report page, notice the arrow button.

	![Picture 100](Linked_image_Files/PowerBI_Lab09A_image10.png)

	*The button was added automatically. It allows report users to navigate back to the page from which they drilled through*.

15. Add a **Card** visual to the page, and then resize and reposition it so it sits to the right of the button and fills the remaining width of the page.

	![Picture 102](Linked_image_Files/PowerBI_Lab09A_image11.png)

	![Picture 101](Linked_image_Files/PowerBI_Lab09A_image12.png)

16. Drag the **Product | Category** field into the card visual.

17. Configure the format options for the visual, and then turn the **Category Label** property to **Off**.

	![Picture 103](Linked_image_Files/PowerBI_Lab09A_image13.png)

18. Set the **Background Color** property to a light shade of gray.

19. Add a **Table** visual to the page, and then resize and reposition it so it sits beneath the card visual and fills the remaining space on the page.

	![Picture 104](Linked_image_Files/PowerBI_Lab09A_image14.png)

	![Picture 105](Linked_image_Files/PowerBI_Lab09A_image15.png)

20. Add the following fields to the visual:

	* Product | Subcategory

	* Product | Color

	* Sales | Quantity

	* Sales | Sales

	* Sales | Profit Margin

21. Configure the format options for the visual, and in the **Grid** section, set the **Text Size** property to **20pt**.

	*The design of the drill through page is almost complete. In the next exercise, you’ll define conditional formatting*.

# Exercise 3: Add Conditional Formatting

In this exercise, you will enhance the drill through page with conditional formatting. When you’ve completed the design, the page will look like the following:  

![Picture 106](Linked_image_Files/PowerBI_Lab09A_image16.png)

### Task 1: Add conditional formatting

In this task, you will enhance the drill through page with conditional formatting.

1. Select the table visual.

23. In the visual fields pane, for the **Profit Margin** field, click the down-arrow, and then select **Conditional Formatting | Icons**.

	![Picture 107](Linked_image_Files/PowerBI_Lab09A_image17.png)

24. In the **Icons – Profit Margin** window, in the **Icon Layout** dropdown list, select **Right of Data**.

	![Picture 108](Linked_image_Files/PowerBI_Lab09A_image18.png)

25. To delete the middle rule, at the left of the yellow triangle, click **X**.

	![Picture 109](Linked_image_Files/PowerBI_Lab09A_image19.png)

26. Configure the first rule (red diamond) as follows:

	* In the second control, remove the value

	* In the third control, select **Number**

	* In the fifth control, enter **0**

	* In the sixth control, select **Number**

27. Configure the second rule (green circle) as follows:

	* In the second control, enter **0**

	* In the third control, select **Number**

	* In the fifth control, remove the value

	* In the sixth control, select **Number**

	![Picture 110](Linked_image_Files/PowerBI_Lab09A_image20.png)

	*The rules are as follows: display a red diamond if the profit margin value is less than 0; otherwise if the value is great or equal to zero, display the green circle*.

28. Click **OK**.

	![Picture 111](Linked_image_Files/PowerBI_Lab09A_image21.png)

29. In the table visual, verify that the that the correct icons are displayed.

	![Picture 112](Linked_image_Files/PowerBI_Lab09A_image22.png)

30. Configure background color conditional formatting for the **Color** field.

31. In the **Background Color – Color** window, in the **Format By** dropdown list, select **Field Value**.

	![Picture 113](Linked_image_Files/PowerBI_Lab09A_image23.png)

32. In the **Based on Field** dropdown list, select **Product | Formatting | Background Color Format**.

	![Picture 114](Linked_image_Files/PowerBI_Lab09A_image24.png)

33. Click **OK**.

	![Picture 115](Linked_image_Files/PowerBI_Lab09A_image25.png)

34. Repeat the previous steps to configure font color conditional formatting for the **Color** field, using the **Product | Formatting | Font Color Format** field

	*Recall that the background and font colors were source from the **ColorFormats.csv** file in **Lab 02A**, and then integrated with the **Product** query in **Lab 03A***.

# Exercise 4: Add Bookmarks and Buttons

In this exercise, you will enhance the **My Performance** page with buttons, allowing the report user to select the visual type to display. When you’ve completed the design, the page will look like the following:  

![Picture 116](Linked_image_Files/PowerBI_Lab09A_image26.png)

### Task 1: Add bookmarks

In this task, you will add two bookmarks, one to display each of the monthly sales/targets visuals.

1. Go to the **My Performance** page.

36. On the **View** ribbon tab, from inside the **Show Panes** group, click **Bookmarks**.

	![Picture 118](Linked_image_Files/PowerBI_Lab09A_image27.png)

37. On the **View** ribbon tab, from inside the **Show Panes** group, click **Selection**.

	![Picture 119](Linked_image_Files/PowerBI_Lab09A_image28.png)

38. In the **Selection** pane, beside one of the **Sales and Target by Month** items, to hide the visual, click the eye icon.

	![Picture 120](Linked_image_Files/PowerBI_Lab09A_image29.png)

39. In the **Bookmarks** pane, click **Add**.

	![Picture 121](Linked_image_Files/PowerBI_Lab09A_image30.png)

40. To rename the bookmark, double-click the bookmark.

41. If the visible chart is the bar chart, rename the bookmark as **Bar Chart ON**, otherwise rename the bookmark as **Column Chart ON**.

42. In the **Selection** pane, toggle the visibility of the two **Sales and Target by Month** items.

	*In other words, make the visible visual hidden, and make the hidden visual visible*.

	![Picture 122](Linked_image_Files/PowerBI_Lab09A_image31.png)

43. Create a second bookmark, and name it appropriately (either **Column Chart ON** or **Bar Chart ON).**

	![Picture 123](Linked_image_Files/PowerBI_Lab09A_image32.png)

44. In the **Selection** pane, to make both visuals visible, simple show the hidden visual.

45. Resize and reposition both visuals so they fill the page beneath the multi-card visual, and completely overlap one another.

	*Tip: To select the visual that is covered up, select it in the **Selection** pane*.

	![Picture 124](Linked_image_Files/PowerBI_Lab09A_image33.png)

46. In the **Bookmarks** pane, select each of the bookmarks, and notice that only one of the visuals is visible.

	*The next stage of design is to add two buttons to the page, which will allow the report user to select the bookmarks*.

### Task 2: Add buttons

In this task, you will add two buttons, and assign bookmark actions to each.

1. On the **Insert** ribbon, from inside the **Elements** group, click **Button**, and then select **Blank**.

	![Picture 125](Linked_image_Files/PowerBI_Lab09A_image34.png)

48. Reposition the button directly beneath the **Year** slicer.

49. Select the button, and the in the **Visualizations** pane, turn the **Button Text** property to **On**.

	![Picture 126](Linked_image_Files/PowerBI_Lab09A_image35.png)

50. Expand the **Button Text** section, and then in the **Button Text** box, enter **Bar Chart**.

51. Format the background color, using a suitable color.

52. Turn the **Action** property to **On** (located near the bottom of the list).

	![Picture 127](Linked_image_Files/PowerBI_Lab09A_image36.png)

53. Expand the **Action** section, and then set the **Type** dropdown list to **Bookmark**.

54. In the **Bookmark** dropdown list, select **Bar Chart ON**.

	![Picture 128](Linked_image_Files/PowerBI_Lab09A_image37.png)

55. Create a copy of the button by using copy and paste, and then configure the new button as follows:

	* Set the **Button Text** property to **Column Chart**

	* In the **Action** section, set the **Bookmark** dropdown list to **Column Chart ON**

### Task 3: Publish the report

In this task, you will publish the report.

1. Select the **Overview** page.

57. In the **Year** slicer, select **FY2020**.

58. In the **Region** slicer, select **Select All**.

59. Save the Power BI Desktop file.

60. Publish the report to your **Sales Analysis** workspace.

61. When prompted to replace the report, click **Replace**.

	![Picture 129](Linked_image_Files/PowerBI_Lab09A_image38.png)

62. Leave Power BI Desktop open.

	*In the next exercise, you will explore the report in the Power BI service*.

# Exercise 5: Explore the Report

In this exercise, you will explore the **Sales Report** in the Power BI service.

### Task 1: Explore the report

In this task, you will explore the **Sales Report** in the Power BI service.

1. In the Edge, in the Power BI service, open the **Sales Report** report.

64. To test the drill through report, in the **Quantity by Category** visual, right-click the **Clothing** bar, and then select **Drill Through | Product Details**.

	![Picture 130](Linked_image_Files/PowerBI_Lab09A_image39.png)

65. Notice that the **Product Details** page is for **Clothing**.

66. To return to the source page, at the top-left corner, click the arrow button.

67. Select the **My Performance** page.

68. Click each of the buttons, and then notice that a different visual is displayed.

### Finish up

In this task, you will complete the lab.

1. To return to the workspace, in the breadcrumb trail, click your workspace name.

	![Picture 92](Linked_image_Files/PowerBI_Lab09A_image40.png)

70. Leave the Edge browser window open.

71. In Power BI Desktop, go to the **My Performance** page, and in the **Fields** pane, remove the **Salesperson** filter card.

	![Picture 132](Linked_image_Files/PowerBI_Lab09A_image41.png)

72. Select the **Overview** page.

73. Save the Power BI Desktop file, and then republish to the **Sales Analysis** workspace.

74. Close Power BI Desktop.

	*When you share the report in **Lab 12A**, the report will enforce row-level security*.

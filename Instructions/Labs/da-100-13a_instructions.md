

### Lab 13A

Creating a Paginated Report

# Overview

**The estimated time to complete the lab is 45 minutes**

In this lab, you will use Power BI Report Builder to develop a pixel-perfect paginated report layout that sources data from the **AdventureWorksDW2020** SQL Server database. You will create a data source and dataset, and also configure a report parameter. The report layout will allow data to be rendered over multiple pages, and to be exported in PDF and other formats.

The final report will look like the following:  

![Picture 10](Linked_image_Files/PowerBI_Lab13A_image1.png)

In this lab, you learn how to:

* Use Power BI Report Builder

* Design a multi-page report layout

* Define a data source

* Define a dataset

* Create a report parameter

* Export a report to PDF

# Exercise 1: Getting Started

In this exercise, you will open Power BI Report Builder to create and then save a report.

### Task 1: Create the report

In this task, you will open Power BI Report Builder to create and then save a report.

1. To open Power BI Report Builder, on the taskbar, click the **Power BI Report Builder** shortcut.

	![Picture 32](Linked_image_Files/PowerBI_Lab13A_image2.png)

2. In the Power BI Report Builder window, to create a new report, in the **Getting Started** window, click **Blank Report**.

	![Picture 5](Linked_image_Files/PowerBI_Lab13A_image3.png)

3. To save the report, click the **File** tab (located at the top-left), and then select **Save**.

	![C:\Users\PETERM~1\AppData\Local\Temp\SNAGHTML32fddfaf.PNG](Linked_image_Files/PowerBI_Lab13A_image4.png)

4. In the **Save As Report** window, navigate to the **D:\DA100\MySolution** folder.

5. In the **Name** box, enter **Sales Order Report**.

6. Click **Save**.

# Exercise 2: Developing the Report Layout

In this exercise, you will develop the report layout, and explore the final report design.

### Task 1: Configure the report header

In this task, you will configure the report header.

1. In the report designer, notice the default report layout, which consists of a body region and a report footer region.

	![C:\Users\PETERM~1\AppData\Local\Temp\SNAGHTML330700e8.PNG](Linked_image_Files/PowerBI_Lab13A_image5.png)

	*The body contains a single textbox ready for a report title, and the report footer contains a single textbox describing the report execution time*.

	*The default design will render the report title once, in the body, on the first rendered page. However, you will now modify the report design by adding a report header region, and by moving the report title textbox into this region. This way, the report title will repeat on every page. You will also add an image of the company logo*.

8. To add a report header region, on the **Insert** ribbon tab, from inside the **Header &amp; Footer** group, click **Header**, and then select **Add Header**.

	![C:\Users\PETERM~1\AppData\Local\Temp\SNAGHTML33038ea4.PNG](Linked_image_Files/PowerBI_Lab13A_image6.png)

9. In the report designer, notice that a report header region has been added to the report layout.

10. To select the body textbox, click the “Click to add title” textbox.

11. To move the textbox, click the four-headed arrow icon, and then drag it into the header region to then drop it at the very top-left of the report header region.

	![C:\Users\PETERM~1\AppData\Local\Temp\SNAGHTML330925bc.PNG](Linked_image_Files/PowerBI_Lab13A_image7.png)

12. To modify the report title textbox text, click inside the text box, and then enter: **Sales Order Report**

	*To resize the textbox, you will first open the **Properties** pane. For fine-grained control of location and size properties, you will need use the **Properties** pane*.

13. On the **View** ribbon tab, from inside the **Show/Hide** group, check **Properties**.

	![Picture 27](Linked_image_Files/PowerBI_Lab13A_image8.png)

14. To select the report title textbox, first click an area outside the textbox, and then click the textbox again.

	*The textbox is selected when you see the border of the textbox highlighted and resizing handles (small circles) appear on the border*.

15. In the **Properties** pane (located at the right), scroll down the list to locate the **Position** group.

	![Picture 28](Linked_image_Files/PowerBI_Lab13A_image9.png)

	*The **Position** group allows setting exact values for the location and size of report items*.

	*It’s important that you enter the values as directed in this lab. Pixel-perfect layout is required to achieve the page rendering at the end of the lab*.

16. Within the **Position** group, expand the **Location** group, and ensure that the **Left** and **Top** properties are each set to **0in**.

	*The location and size units are in inches because the regional settings of the lab virtual machine is set to the United States. If your region uses metric measurements, centimeters would be the default unit*.

17. Within the **Position** group, expand the **Size** group, and then set the **Width** property to **4**.

	![Picture 35](Linked_image_Files/PowerBI_Lab13A_image10.png)

18. To insert an image, on the **Insert** ribbon tab, from inside the **Report Items** group, click **Image**.

	![Picture 31](Linked_image_Files/PowerBI_Lab13A_image11.png)

19. To add the image to the report design, click inside the report header region, to the right of the report title textbox.

20. In the **Image Properties** window, to import from an image file, click **Import**.

	![Picture 33](Linked_image_Files/PowerBI_Lab13A_image12.png)

21. In the **Open** window, navigate to the **D:\DA100\Data** folder, and then select the **AdventureWorksLogo.jpg** file.

22. Click **Open**.

23. In the **Image Properties** window, click **OK**.

24. In the report designer, notice that the image was added, and is selected.

25. To position and resize the image, in the **Properties** pane, configure the following properties:

	|  Property | Value |   |   |
	|  ------  |  ---- | ---- | ---- |
	|  Position | Location | Left | 5 |
	|  Position | Location | Top | 0 |
	|  Position | Size | Width | 1  |
	|  Position | Size | Height | 1 |


26. To resize the report header region, first select the region by clicking a blank area of the region.

27. In the **Properties** pane, set the **General | Height** property to **1**.

28. Verify that the report header region contains a single textbox and image, and looks like the following:

	![Picture 34](Linked_image_Files/PowerBI_Lab13A_image13.png)

29. To save the report, on the **File** tab, click **Save**.

	*Tip: You can also click the disk icon located at the top-left*.

	![Picture 106](Linked_image_Files/PowerBI_Lab13A_image14.png)

	*You are now ready to configure the report to retrieve a database query result*.

### Task 2: Retrieve data

In this task, you will create a data source and dataset to retrieve a query result from the **AdventureWorksDW2020** SQL Server database.

1. In the **Report Data** pane (located at the left), right-click the **Data Sources** folder, and then select **Add Data Source**.

	![C:\Users\PETERM~1\AppData\Local\Temp\SNAGHTML3367f3d0.PNG](Linked_image_Files/PowerBI_Lab13A_image15.png)

	*It is possible to retrieve data from cloud or on-premises databases, or a Power BI dataset*.

31. In the **Data Source Properties** window, in the **Name** box, replace the text with **AdventureWorksDW2020**.

32. In the **Select Connection Type** dropdown list, notice that **Microsoft SQL Server** is selected.

33. To build the connection string, click **Build**.

	![Picture 1](Linked_image_Files/PowerBI_Lab13A_image16.png)

34. In the **Connection Properties** window, in the **Server Name** box, enter **localhost**.

	*In the labs, you will connect to the SQL Server database by using **localhost**. This isn’t a recommended practice, however, when creating your own solutions. It’s because gateway data sources cannot resolve **localhost***.

35. In the **Select or Enter a Database Name** dropdown list, select the **AdventureWorksDW2020**.

36. Click **OK**.

37. In the **Data Source Properties** window, click **OK**.

38. In the **Report Data** pane, notice the addition of the **AdventureWorksDW2020** data source.

	![Picture 2](Linked_image_Files/PowerBI_Lab13A_image17.png)

39. To create a dataset, in the **Report Data** pane, right-click the **AdventureWorksDW2020** data source, and then select **Add Dataset**.

	![C:\Users\PETERM~1\AppData\Local\Temp\SNAGHTML336e389c.PNG](Linked_image_Files/PowerBI_Lab13A_image18.png)

	*A report dataset is a different in purpose and structure from a Power BI dataset*.

40. In the **Dataset Properties** window, in the **Name** box, replace the text with **SalesOrder**.

41. To import a pre-defined query, click **Import**.

	![Picture 40](Linked_image_Files/PowerBI_Lab13A_image19.png)

42. In the **Import Query** window, navigate to the **D:\DA100\Lab13A\Assets** folder, and then select the **SalesOrder.sql** file.

43. Click **Open**.

44. In the **Query** box, review the query, and be sure to scroll down to the bottom of the query text.

	*It is not important that you understand the details of the query statement. It has been designed to retrieve sales order line details. The WHERE clause includes a predicate to restrict the query result to a single sales order. The ORDER BY clause ensures the rows are returned by line number order*.

45. Notice the use of **@SalesOrderNumber** in the WHERE clause, which represents a query parameter.

	![Picture 3](Linked_image_Files/PowerBI_Lab13A_image20.png)

	*A query parameter is a placeholder for a value that will be passed in at query execution time. You will configure a report parameter to prompt the report user for a single sales order number which will then be passed to the query parameter*.

46. Click **OK**.

47. In the **Report Data** pane, notice the addition of the **SalesOrder** dataset and its fields.

	![Picture 44](Linked_image_Files/PowerBI_Lab13A_image21.png)

	*Fields are used to configure data regions in the report layout. They were derived from the dataset query columns*.

48. Save the report.

### Task 3: Configure the report parameter

In this task, you will configure the report parameter with a default value.

1. In the **Report Data** pane, expand the **Parameters** folder to reveal the **SalesOrderNumber** report parameter.

	![Picture 107](Linked_image_Files/PowerBI_Lab13A_image22.png)

	*The **SalesOrderNumber** report parameter was added automatically when the dataset was created. This is because the dataset query included the **@SalesOrderNumber** query parameter*.

50. To edit the report parameter, right-click the **SalesOrderNumber** report parameter, and then select **Parameter Properties**.

	![Picture 46](Linked_image_Files/PowerBI_Lab13A_image23.png)

51. In the **Report Parameter Properties** window, at the left, select the **Default Values** pages.

	![Picture 48](Linked_image_Files/PowerBI_Lab13A_image24.png)

52. Select the **Specify Values** option.

	![Picture 49](Linked_image_Files/PowerBI_Lab13A_image25.png)

53. To add a default value, click **Add**.

54. In the **Value** dropdown list, replace the text with **43659**.

	![Picture 50](Linked_image_Files/PowerBI_Lab13A_image26.png)

	*Sales order 43659 is the value you will initially use to test the report design*.

55. Click **OK**.

56. Save the report.

	*You will now complete the report header region design by adding textboxes to describe the sales order*.

### Task 4: Finalize the report header layout

In this task, you will finalize the report header region design by adding textboxes.

1. To add a textbox to the report header region, on the **Insert** ribbon tab, from inside the **Report Items** group, click **Text Box**.

	![Picture 51](Linked_image_Files/PowerBI_Lab13A_image27.png)

58. Click inside the report header region, directly beneath the report title textbox.

59. Inside the textbox, enter **Sales Order:** followed by a space.

60. To insert a place holder, immediately after the space just entered, right-click and then select **Create Placeholder**.

	![Picture 109](Linked_image_Files/PowerBI_Lab13A_image28.png)

61. In the **Placeholder Properties** window, at the right of the **Value** dropdown list, click the **fx** button.

	![Picture 53](Linked_image_Files/PowerBI_Lab13A_image29.png)

	*The **fx** button allows entering a custom expression. This expression will be used to return the sales order number*.

62. In the **Expression** window, in the **Category** list, select **Parameters**.

	![Picture 54](Linked_image_Files/PowerBI_Lab13A_image30.png)

63. In the **Values** list, double-click the **SalesOrderNumber** parameter.

64. In the expression box, notice that a programmatic reference to the **SalesOrderNumber** report parameter was added.

	![Picture 55](Linked_image_Files/PowerBI_Lab13A_image31.png)

65. Click **OK**.

66. In the **Placeholder Properties** window, click **OK**.

67. Click a blank area of the report header region, and then select the new textbox.

68. In the **Properties** pane, configure the following position properties:

	|  Property                    |  Value|
	|  :---                        |  :--- |
	|  Position \| Location \| Left|  0    |
	|  Position \| Location \| Top |  0.5  |
	|  Position \| Size \| Width   |  4    |
	|  Position \| Size \| Height  |  0.25 |

69. To format part of the textbox text, inside the new textbox, select only the **Sales Order:** text.

	![Picture 110](Linked_image_Files/PowerBI_Lab13A_image32.png)

70. On the **Home** ribbon tab, from inside the **Font** group, click the **Bold** command.

	![Picture 56](Linked_image_Files/PowerBI_Lab13A_image33.png)

71. Add another textbox to the report header region, and then enter the text **Reseller:** followed by a space.

	*Tip: You can also add a textbox by right-clicking the canvas, and then selected **Insert | Text Box***.

72. After the space, insert a placeholder, and then set the value of the placeholder to use an expression.

73. In the **Expression** window, in the **Category** list, select **Datasets**.

	![Picture 58](Linked_image_Files/PowerBI_Lab13A_image34.png)

74. Base the expression value on **First(Reseller)** value.

75. In the **Properties** pane, configure the following position properties:

	|  Property                    |  Value|
	|  :---                        |  :--- |
	|  Position \| Location \| Left|  0    |
	|  Position \| Location \| Top |  0.75 |
	|  Position \| Size \| Width   |  4    |
	|  Position \| Size \| Height  |  0.25 |
	

76. Format the **Reseller:** text in bold.

77. Add a third (and last) textbox to the report header region, and then enter the text **Order Date:** followed by a space.

78. After the space, insert a placeholder, and set the value of the placeholder to use an expression based on the **Datasets** category, **First(OrderDate)** value.

	![Picture 111](Linked_image_Files/PowerBI_Lab13A_image35.png)

79. To format the date value, in the **Placeholder Properties** window, select the **Number** page.

	![Picture 61](Linked_image_Files/PowerBI_Lab13A_image36.png)

80. In the **Category** list, select **Date**.

	![Picture 62](Linked_image_Files/PowerBI_Lab13A_image37.png)

81. In the **Type** list, select a suitable date format type.

82. In the **Placeholder Properties** window , click **OK**.

83. In the **Properties** pane, configure the following position properties:

	|  Property                    |  Value|
	|  :---                        |  :--- |
	|  Position \| Location \| Left|  0    |
	|  Position \| Location \| Top |  1    |
	|  Position \| Size \| Width   |  4    |
	|  Position \| Size \| Height  |  0.25 |


84. Format the **Order Date:** text in bold.

85. Finally, click a blank area of the report header region.

86. In the **Properties** pane, set the **Height** property to **1.5**.

87. Verify that the report header region looks like the following:

	![Picture 112](Linked_image_Files/PowerBI_Lab13A_image38.png)

88. Save the report.

89. To preview the report, on the **Home** ribbon tab, from inside the **Views** group, click **Run**.

	![Picture 60](Linked_image_Files/PowerBI_Lab13A_image39.png)

	*Running the report renders the report in HTML. As the only report parameter has a default value, the report will run automatically*.

90. Verify that the rendered report looks like the following:

	![Picture 4](Linked_image_Files/PowerBI_Lab13A_image40.png)

91. To return to design view, on the **Run** ribbon tab, from inside the **Views** group, click **Design**.

	![Picture 64](Linked_image_Files/PowerBI_Lab13A_image41.png)

	*You will now add a table to the report body to display a formatted layout of the sales order lines*.

### Task 5: Add a table data region

In this task, you will add a table data region to the report body.

1. On the **Insert** ribbon tab, from inside the **Data Regions** group, click **Table**, and then select **Insert Table**.

	![C:\Users\PETERM~1\AppData\Local\Temp\SNAGHTML33b54257.PNG](Linked_image_Files/PowerBI_Lab13A_image42.png)

93. To add the table, click a blank area inside the report body.

94. In the **Properties** pane, configure the following position properties:

	|  Property                     | Value |
	|  :---                         |  :--- |
	|  Position \| Location \| Left |  0    |
	|  Position \| Location \| Top  |  0    |
	
	*The table will display five columns. By default, the table template includes only three columns*.

95. To add a column to the table, right-click inside any cell of the last column, and then select **Insert Column | Right**.

	![C:\Users\PETERM~1\AppData\Local\Temp\SNAGHTML33b96fbd.PNG](Linked_image_Files/PowerBI_Lab13A_image43.png)

96. Repeat the last step to add a second new column.

97. Hover the cursor over the cell in the second row of the first column to reveal the field picker icon.

	![Picture 67](Linked_image_Files/PowerBI_Lab13A_image44.png)

98. Click the field picker icon, and then select the **Line** field.

	![Picture 113](Linked_image_Files/PowerBI_Lab13A_image45.png)

99. Notice that the table now includes a text value in the first row (header), and a field reference in the detail row.

	![Picture 68](Linked_image_Files/PowerBI_Lab13A_image46.png)

1. Add fields to the next four columns, in order, as follows:

	* Product
	* Quantity
	* UnitPrice
	* Amount

101. Verify that the table design looks like the following:  
	![Picture 69](Linked_image_Files/PowerBI_Lab13A_image47.png)

102. Save the report.

103. Preview the report.    
	![Picture 71](Linked_image_Files/PowerBI_Lab13A_image48.png)  
	![Picture 11](Linked_image_Files/PowerBI_Lab13A_image49.png)  
	*The table includes a header and 12 sales order line rows. There are many improvements that can be made by formatting the table layout*.   
	*In the next task you will*:
		* Format the table header by using a background color and bold font style

		* Modify column widths to remove redundant space and to prevent long text values from wrapping

		* Left-justify the first column values

		* Right-justify the last three column values

		* Format currency values using a currency symbol (for USD)

		* Add and format a total row for the table

### Task 6: Format the table data region

In this task, you will format the table data region.

1. Return to design view.

105. Click any cell in the table to reveal the gray cell guides.  
	![Picture 73](Linked_image_Files/PowerBI_Lab13A_image50.png)  
	*The cell guides are there to help you configure entire rows or columns*.

106. To format the table header, click the header row guide.  
	![C:\Users\PETERM~1\AppData\Local\Temp\SNAGHTML3426409c.PNG](Linked_image_Files/PowerBI_Lab13A_image51.png)  
	*Selecting a row or a column guide selects all cells in the row or column. Each cell is in fact a textbox. Formatting single textbox—or a multi-selection of textboxes—can then be achieved by using the **Properties** pane, or the ribbon commands*.

1. In the **Properties** pane (or the ribbon), configure the following properties:  

	|  Property         | Value     |
	|  :---------       | :-------  |
	|  Fill \| BackgroundColor| DarkGreen (tip: hover the cursor over each color to reveal its name) |
	|  Font \| Color             | White |
	|  Font \| Font \| FontWeight| Bold |


108. Select the first column guide.  
	![C:\Users\PETERM~1\AppData\Local\Temp\SNAGHTML342b0187.PNG](Linked_image_Files/PowerBI_Lab13A_image52.png)

109. In the **Properties** pane, set the **Position | Size | Width** property to **0.5**.

110. Set the width of the second column to **2.5**.

111. While pressing the **Ctrl** key, multi-select the last three column header textboxes (**Quantity**, **Unit Price** and **Amount**).

112. In the **Properties** pane (or ribbon), set the **Alignment | TextAlign** property to **Right**.

113. Set the **Line** detail textbox to left align.  
	![C:\Users\PETERM~1\AppData\Local\Temp\SNAGHTML342fbe1d.PNG](Linked_image_Files/PowerBI_Lab13A_image53.png)

114. On the **Home** ribbon tab, from inside the **Number** group, set the last two detail (not header) textboxes (**UnitPrice** and **Amount**) to format with a currency symbol.  
	![Picture 77](Linked_image_Files/PowerBI_Lab13A_image54.png)

115. To add a total row to the table, right-click the **Quantity** detail textbox, and then select **Add Total**.  
	![Picture 78](Linked_image_Files/PowerBI_Lab13A_image55.png)

116. Notice that a new row, which represents the table footer, has been added, and that the expression will evaluate the sum of **Quantity** values.

117. Repeat the last step to add a total for the **Amount** detail textbox.

118. In the first cell of the table footer row, enter the word **Total**.

119. Format all textboxes in the footer row to format as bold.

120. Verify that the table design looks like the following:  
	![Picture 79](Linked_image_Files/PowerBI_Lab13A_image56.png)

121. To remove any trailing space after the table, hover the cursor over the dashed line between the report body and report footer region, and then drag upwards to touch the bottom of the table.  
	![Picture 84](Linked_image_Files/PowerBI_Lab13A_image57.png)

122. Save the report

123. Preview the report.

124. Verify that the rendered report looks like the following:  
	![Picture 6](Linked_image_Files/PowerBI_Lab13A_image58.png)

125. In the **Sales Order Number** parameter box, replace the value with **51721**.  
	![Picture 81](Linked_image_Files/PowerBI_Lab13A_image59.png)

126. To re-run the report, at the right, click **View Report**.  
	![Picture 82](Linked_image_Files/PowerBI_Lab13A_image60.png)  
	*This sales order has 72 sales order lines, and so the data will render over many pages*.

127. To navigate to the second page of the report, on the **Run** ribbon tab, from inside the **Navigation** group, click **Next**.  
	![Picture 83](Linked_image_Files/PowerBI_Lab13A_image61.png)

128. On page 2, notice that the table header does not appear.  
	*You will address this issue in the next task*.

129. Scroll to the bottom of the page, and then notice that the report footer displays only the execution time.  
	*In the next task, you will improve the footer text by appending the page number*.

### Task 7: Finalize the report design

In this task, you will finalize the report design by ensuring multi-page reports render appropriately.

1. Switch to the design view.

131. To ensure the table header repeats on all pages, first select any textbox of the table.

132. In the **Grouping** pane (located along the bottom of the report designer), at the far right of the **Column Groups**, click the down-arrow, and then select **Advanced Mode**.  
	![C:\Users\PETERM~1\AppData\Local\Temp\SNAGHTML34447bde.PNG](Linked_image_Files/PowerBI_Lab13A_image62.png)

133. In the **Row Groups** section, select the first static group.  
	![Picture 86](Linked_image_Files/PowerBI_Lab13A_image63.png)  
	*This selected the table header row*.

134. In the **Properties** pane, set the **Other | RepeatOnNewPage** property to **True**.  
	*This ensures that the first static group (representing the table header) will repeat on all pages*.

135. In the table footer region, right-click the **ExecutionTime** textbox, and then select **Expression**.  
	![C:\Users\PETERM~1\AppData\Local\Temp\SNAGHTML34484edf.PNG](Linked_image_Files/PowerBI_Lab13A_image64.png)

1. In the **Expression** window, in the expression box, append a space, followed by **&amp; “ | Page “ &amp;**, to produce the following:  
**VB Script**
	```
	=Globals!ExecutionTime & " | Page " &
	```

137. Ensure that a space follows the last ampersand (&).

138. In the **Category** list, select **Built-in Fields**.  
	![Picture 94](Linked_image_Files/PowerBI_Lab13A_image65.png)

139. To inject the page number value into the expression, in the **Item** list, double-click **PageNumber**.

140. Verify that the complete expression reads as follows:  
	![Picture 114](Linked_image_Files/PowerBI_Lab13A_image66.png)

141. Click **OK**.

142. Drag the left side of the textbox to increase the width to the width of the report page.  
	![Picture 104](Linked_image_Files/PowerBI_Lab13A_image67.png)  
	*The design of the report is now complete. Lastly, you will ensure that the page width is set to exactly six inches, and also remove the report parameter default value*.

143. To select the report body, right-click any table textbox, and then select **Select | Body**.  
	![C:\Users\PETERM~1\AppData\Local\Temp\SNAGHTML34507b38.PNG](Linked_image_Files/PowerBI_Lab13A_image68.png)  
	*As the table fills the entire report body, this technique must be used to select the report body*.

144. In the **Properties** pane, ensure that the **Position | Size | Width** property is set to **6**.  
	*It is important the width is not greater than six inches, as rendering to print format would break the table up across multiple pages*.

145. In the **Report Data** pane, open the **SalesOrderNumber** report parameter properties.

146. On the **Default Values** page, select the **No Default Value** option.  
	![Picture 98](Linked_image_Files/PowerBI_Lab13A_image69.png)

147. Click **OK**.

148. Save the report.

### **Task 8: Explore the final report**

In this task, you will view the report in print layout mode.

1. Preview the report.

150. In the **Sales Order Number** parameter box, enter the value with **51721**

151. On the **Run** ribbon tab, from inside the **Print** group, click **Print Layout**.  
	![Picture 7](Linked_image_Files/PowerBI_Lab13A_image70.png)  
	*Print layout mode provides a preview of what the report will look like when printed to the strict page size*.

152. Navigate to pages 2 and 3.  
	*In this lab, you won’t publish the report. Paginated reports can only be rendered in the Power BI service when they are stored in a workspace on dedicated capacity, and when that capacity has the paginated reports workload enabled. These requirements do not exist for the class*.

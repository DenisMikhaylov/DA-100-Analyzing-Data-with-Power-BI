

### Lab 04A

Data Modeling in Power BI Desktop

# Overview

**The estimated time to complete the lab is 45 minutes**

In this lab, you will commence developing the data model. It will involve creating relationships between tables, and then configuring table and column properties to improve the friendliness and usability of the data model. You will also create hierarchies and create quick measures.

In this lab, you learn how to:

* Create model relationships

* Configure table and column properties

* Create hierarchies

* Create quick measures

# Exercise 1: Create Model Relationships

In this exercise, you will create model relationships.

If you’re not confident you completed the previous lab successfully, you can open the previous lab’s solution file, which is found in the **D:\DA100\Lab03A\Solution** folder.

### Task 1: Create model relationships

In this task, you will create model relationships.

1. In Power BI Desktop, at the left, click the **Model** view icon.

	![Picture 1](Linked_image_Files/PowerBI_Lab04A_image1.png)

2. If you do not see all seven tables, scroll horizontally to the right, and then drag and arrange the tables more closely together so they can all be seen at the same time.

	*In Model view, it’s possible to view each table and relationships (connectors between tables). Presently, there are no relationships because in **Lab 02A**, you disabled the data load relationship options*.

3. To return to Report view, at the left, click the **Report** view icon.

	![Picture 327](Linked_image_Files/PowerBI_Lab04A_image2.png)

4. To view all table fields, in the **Fields** pane, right-click an empty area, and then select **Expand All**.

	![Picture 328](Linked_image_Files/PowerBI_Lab04A_image3.png)

5. To create a table visual, in the **Fields** pane, from inside the **Product** table, check the **Category** field.

	![Picture 329](Linked_image_Files/PowerBI_Lab04A_image4.png)

	*From now on, the labs will use a shorthand notation to reference a field. It will look like this: **Product | Category***.

6. To add a column to the table, in the **Fields** pane, check the **Sales | Sales** field.

7. Notice that the table visual lists four product categories, and that the sales value is the same for each, and the same for the total.

	![Picture 330](Linked_image_Files/PowerBI_Lab04A_image5.png)

	*The issue is that the table is based on fields from different tables. The expectation is that each product category displays the sales for that category. However, because there isn’t a model relationship between these tables, the **Sales** table is not filtered. You will now add a relationship to propagate filters between the tables*.

8. On the **Modeling** ribbon tab, from inside the **Relationships** group, click **Manage Relationships**.

	![Picture 331](Linked_image_Files/PowerBI_Lab04A_image6.png)

9. In the **Manage Relationships** window, notice that no relationships are yet defined.

10. To create a relationship, click **New**.

	![Picture 332](Linked_image_Files/PowerBI_Lab04A_image7.png)

11. In the **Create Relationship** window, in the first dropdown list, select the **Product** table.

	![Picture 333](Linked_image_Files/PowerBI_Lab04A_image8.png)

12. In the second dropdown list (beneath the **Product** table grid), select the **Sales** table.

	![Picture 334](Linked_image_Files/PowerBI_Lab04A_image9.png)

13. Notice the **ProductKey** columns in each table have been selected.

	*The columns were automatically selected because they share the same name*.

14. In the **Cardinality** dropdown list, notice that **One To Many** is selected.

	*The cardinality was automatically detected, because Power BI understands that the **ProductKey** column from the **Product** table contains unique values. One-to-many relationships are the most common cardinality, and all relationship you create in this lab will be this type. You will work with a Many-to-many cardinality in **Lab 05A***.

15. In the **Cross Filter Direction** dropdown list, notice that **Single** is selected.

	*Single filter direction means that filters propagate from the “one side” to the “many side”. In this case, it means filters applied to the **Product** table will propagate to the **Sales** table, but not in the other direction. You will work with a bi-directional relationship in **Lab 05A***.

16. Notice that the **Mark This Relationship Active** is checked.

	*Active relationships will propagate filters. It’s possible to mark a relationship as inactive so filters don’t propagate. Inactive relationships can exist when there are multiple relationship paths between tables. In which case, model calculations can use special functions to activate them. You’ll work with an inactive relationship in **Lab 05A***.

17. Click **OK**.

	![Picture 335](Linked_image_Files/PowerBI_Lab04A_image10.png)

18. In the **Manage Relationships** window, notice that the new relationship is listed, and then click **Close**.

	![Picture 336](Linked_image_Files/PowerBI_Lab04A_image11.png)

19. In the report, notice that the table visual has updated to display different values for each product category.

	![Picture 337](Linked_image_Files/PowerBI_Lab04A_image12.png)

20. Filters applied to the **Product** table now propagate to the **Sales** table.

21. Switch to Model view, and then notice there is now a connector between the two tables.

	![Picture 338](Linked_image_Files/PowerBI_Lab04A_image13.png)

22. In the diagram, notice that you can interpret the cardinality which is represented by the **1** and ***** indicators.

	*Filter direction is represented by the arrow head. And, a solid line represents an active relationship; a dashed line represents an inactive relationship*.

23. Hover the cursor over the relationship to reveal the related columns.

	*There’s an easier way to create a relationship. In the model diagram, you can drag and drop columns to create a new relationship*.

24. To create a new relationship, from the **Reseller** table, drag the **ResellerKey** column on to the **ResellerKey** column of the **Sales** table.

	![Picture 339](Linked_image_Files/PowerBI_Lab04A_image14.png)

	*Tip: Sometime a column doesn’t want to be dragged. If this situation arises, select a different column, and then select the column you intend to drag again, and try again*.

25. Create the following two model relationships:

	* **Region | SalesTerritoryKey** to **Sales | SalesTerritoryKey**

	* **Salesperson | EmployeeKey** to **Sales | EmployeeKey**

	*In this lab, the **SalespersonRegion** and **Targets** tables will remain disconnected. There’s a many-to-many relationship between salespeople and regions, you will work this advanced scenario in the next lab*.

26. In the diagram, placing the tables with the **Sales** table in the center, and arranging the related tables about it.

	![Picture 340](Linked_image_Files/PowerBI_Lab04A_image15.png)

27. Save the Power BI Desktop file.

# Exercise 2: Configure Tables

In this exercise, you will configure each table by creating hierarchies, and hiding, formatting, and categorizing columns.

### Task 1: Configure the Product table

In this task, you will configure the **Product** table.

1. In Model view, in the **Fields** pane, if necessary, expand the **Product** table.

29. To create a hierarchy, in the **Fields** pane, right-click the **Category** column, and then select **Create Hierarchy**.

	![Picture 341](Linked_image_Files/PowerBI_Lab04A_image16.png)

30. In the **Properties** pane (to the left of the **Fields** pane), in the **Name** box, replace the text with **Products**.

	![Picture 344](Linked_image_Files/PowerBI_Lab04A_image17.png)

31. To add the second level to the hierarchy, in the **Hierarchy** dropdown list, select **Subcategory**.

32. To add the third level to the hierarchy, in the **Hierarchy** dropdown list, select **Product**.

33. To complete the hierarchy design, click **Apply Level Changes**.

	![Picture 343](Linked_image_Files/PowerBI_Lab04A_image18.png)

	*Tip: Don’t forget to click **Apply Level Changes**—it’s a common mistake to overlook this step*.

34. In the **Fields** pane, notice the **Products** hierarchy.

	![Picture 347](Linked_image_Files/PowerBI_Lab04A_image19.png)

35. To reveal the hierarchy levels, expand the **Products** hierarchy.

	![Picture 346](Linked_image_Files/PowerBI_Lab04A_image20.png)

36. To organize columns into a display folder, in the **Fields** pane, first select the **Background Color Format** column.

37. While pressing the **Ctrl** key, select the **Font Color Format**.

38. In the **Properties** pane, in the **Display Folder** box, enter **Formatting**.

	![Picture 348](Linked_image_Files/PowerBI_Lab04A_image21.png)

39. In the **Fields** pane, notice that the two columns are now inside a folder.

	![Picture 349](Linked_image_Files/PowerBI_Lab04A_image22.png)

	*Display folders are a great way to declutter tables—especially those that contain lots of fields*.

### Task 2: Configure the Region table

In this task, you will configure the **Region** table.

1. In the **Region** table, create a hierarchy named **Regions**, with the following three levels:

	* Group

	* Country

	* Region

	![Picture 350](Linked_image_Files/PowerBI_Lab04A_image23.png)

41. Select the **Country** column (not the **Country** level).

42. In the **Properties** pane, expand the **Advanced** section, and then in the **Data Category** dropdown list, select **Country/Region**.

	![Picture 352](Linked_image_Files/PowerBI_Lab04A_image24.png)

	*Data categorization can provide hints to the report designer. In this case, categorizing the column as country or region, provides more accurate information when rendering a map visualization*.

### Task 3: Configure the Reseller table

In this task, you will configure the **Reseller** table.

1. In the **Reseller** table, create a hierarchy named **Resellers**, with the following two levels:

	* Business Type

	* Reseller

	![Picture 351](Linked_image_Files/PowerBI_Lab04A_image25.png)

44. Create a second hierarchy named **Geography**, with the following four levels:

	* Country-Region

	* State-Province

	* City

	* Reseller

	![Picture 353](Linked_image_Files/PowerBI_Lab04A_image26.png)

45. Categorize the following three columns:

	* **Country-Region** as **Country/Region**

	* **State-Province** as **State or Province**

	* **City** as **City**

### Task 4: Configure the Sales table

In this task, you will configure the **Sales** table.

1. In the **Sales** table, select the **Cost** column.

47. In the **Properties** pane, in the **Description** box, enter: **Based on standard cost**

	![Picture 358](Linked_image_Files/PowerBI_Lab04A_image27.png)

	*Descriptions can be applied to table, columns, hierarchies, or measures. In the **Fields** pane, description text is revealed in a tooltip when a report author hovers their cursor over the field*.

48. Select the **Quantity** column.

49. In the **Properties** pane, from inside the **Formatting** section, slide the **Thousands Separator** property to **On**.

	![Picture 357](Linked_image_Files/PowerBI_Lab04A_image28.png)

50. Select the **Unit Price** column.

51. In the **Properties** pane, from inside the **Formatting** section, slide the **Decimal Places** property to **2**.

52. In the **Advanced** group (you may need to scroll down to locate it), in the **Summarize By** dropdown list, select **Average**.

	![Picture 354](Linked_image_Files/PowerBI_Lab04A_image29.png)

	*By default, numeric columns will summarize by summing values together. This default behavior is not suitable for a column like **Unit Price**, which represents a rate. Setting the default summarization to average will produce a useful and accurate result*.

### Task 5: Bulk update properties

In this task, you will update multiple columns in a single bulk update. You will use this approach to hide columns, and format column values.

1. While pressing the **Ctrl** key, select the following 13 columns (spanning multiple tables):

	* Product | ProductKey

	* Region | SalesTerritoryKey

	* Reseller | ResellerKey

	* Sales | EmployeeKey

	* Sales | ResellerKey

	* Sales | SalesOrderNumber

	* Sales | SalesTerritoryKey

	* Salesperson | EmployeeID

	* Salesperson | EmployeeKey

	* Salesperson | UPN

	* SalespersonRegion | EmployeeKey

	* SalespersonRegion | SalesTerritoryKey

	* Targets | EmployeeID

54. In the **Properties** pane, slide the **Is Hidden** property to **On**.

	![Picture 355](Linked_image_Files/PowerBI_Lab04A_image30.png)

	*The columns were hidden because they are either used by relationships or will be used in row-level security configuration or calculation logic*.

	*You will define row-level security in the next lab using the **UPN** column. You will use the **SalesOrderNumber** in a calculation in **Lab 06A***.

55. Multi-select the following columns:

	* Product | Standard Cost

	* Sales | Cost

	* Sales | Sales

56. In the **Properties** pane, from inside the **Formatting** section, set the **Decimal Places** property to **0** (zero).

	![Picture 356](Linked_image_Files/PowerBI_Lab04A_image31.png)

# Exercise 3: Review the Model Interface

In this exercise, you will switch to Report view, and review the model interface.

### Task 1: Review the model interface

In this task, you will switch to Report view, and review the model interface.

1. Switch to Report view.

58. In the **Fields** pane, notice the following:

	* Columns, hierarchies and their levels are fields, which can be used to configure report visuals

	* Only fields relevant to report authoring are visible

	* The **SalespersonRegion** table is not visible—because all of its fields are hidden

	* Spatial fields in the **Region** and **Reseller** table are adorned with a spatial icon

	* Fields adorned with the sigma symbol (Ʃ) will summarize, by default

	* A tooltip appears when hovering the cursor over the **Sales | Cost** field

59. Expand the **Sales | OrderDate** field, and then notice that it reveals a date hierarchy.

	![Picture 359](Linked_image_Files/PowerBI_Lab04A_image32.png)

	*The **Targets | TargetMonth** presents the same hierarchy. These hierarchies were not created by you. They are created automatically. There is a problem, however. The Adventure Works financial year commences on July 1 of each year. But, the date hierarchy year commences on January 1 of each year*.

	*You will now turn this automatic behavior off. In **Lab 06A**, you will use DAX to create a date table, and configure it define the Adventure Works’ calendar*.

60. To turn off auto/date time, click the **File** ribbon tab to open the backstage view.

61. At the left, select **Options and Settings**, and then select **Options**.

	![Picture 360](Linked_image_Files/PowerBI_Lab04A_image33.png)

62. In the **Options** window, at the left, in the **Current File** group, select **Data Load**.

	![Picture 361](Linked_image_Files/PowerBI_Lab04A_image34.png)

63. In the **Time Intelligence** section, uncheck **Auto Date/Time**.

	![Picture 362](Linked_image_Files/PowerBI_Lab04A_image35.png)

64. Click **OK**.

	![Picture 9](Linked_image_Files/PowerBI_Lab04A_image36.png)

65. In the **Fields** pane, notice that the date hierarchies are no longer available.

	![Picture 363](Linked_image_Files/PowerBI_Lab04A_image37.png)

# Exercise 4: Create Quick Measures

In this exercise, you will create two quick measures.

### Task 1: Create quick measures

In this task, you will create two quick measures to calculate profit and profit margin.

1. In the **Fields** pane, right-click the **Sales** table, and then select **New Quick Measure**.

	![Picture 366](Linked_image_Files/PowerBI_Lab04A_image38.png)

67. In the **Quick Measures** window, in the **Calculation** dropdown list, from inside the **Mathematical Operations** group, select **Subtraction**.

	![Picture 367](Linked_image_Files/PowerBI_Lab04A_image39.png)

68. In the **Fields** pane, expand the **Sales** table.

69. Drag the **Sales** field into the **Base Value** box.

70. Drag the **Cost** field into the **Value to Subtract** box.

	![Picture 368](Linked_image_Files/PowerBI_Lab04A_image40.png)

71. Click **OK**.

	![Picture 369](Linked_image_Files/PowerBI_Lab04A_image41.png)

	*A quick measure creates the calculation for you. They’re easy and fast to create for simple and common calculations. You’ll create measures without this tool using the formula language in **Lab 06A***.

72. In the **Fields** pane, inside the **Sales** table, notice that new measure.

	![Picture 370](Linked_image_Files/PowerBI_Lab04A_image42.png)

	*Measures are adorned with the calculator icon*.

73. To rename the measure, right-click it, and then select **Rename**.

	![Picture 371](Linked_image_Files/PowerBI_Lab04A_image43.png)

	*Tip: To rename a field, you can also double-click it, or select it and press **F2***.

74. Rename the measure to **Profit**, and then press **Enter**.

75. In the **Sales** table, add a second quick measure, based on the following requirements:

	* Use the **Division** mathematical operation

	* Set the **Numerator** to the **Sales | Profit** field

	* Set the **Denominator** to **Sales | Sales** field

	* Rename the measure as **Profit Margin**

	![Picture 372](Linked_image_Files/PowerBI_Lab04A_image44.png)

	![Picture 373](Linked_image_Files/PowerBI_Lab04A_image45.png)

76. Ensure the **Profit Margin** measure is selected, and then on the **Measure Tools** contextual ribbon, set the format to **Percentage**, with two decimal places.

	![Picture 374](Linked_image_Files/PowerBI_Lab04A_image46.png)

77. To test the two measures, first select the table visual on the report page.

78. In the **Fields** pane, check the two measures.

	![Picture 375](Linked_image_Files/PowerBI_Lab04A_image47.png)

79. Click and drag the right guide to widen the table visual.

	![Picture 376](Linked_image_Files/PowerBI_Lab04A_image48.png)

80. Verify that the measures produce reasonable result that are correctly formatted.

	![Picture 378](Linked_image_Files/PowerBI_Lab04A_image49.png)

### Finish up

In this task, you will complete the lab.

1. To remove the table, select the table (by clicking it), and then press the **Delete** key.

82. Save the Power BI Desktop file.

	*In the next lab, you will enhance the data model by configuring a many-to-many relationship, and row-level security*.

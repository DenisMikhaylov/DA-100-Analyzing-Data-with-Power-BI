Перейти к содержанию
Найдите или перейдите к…
Пулл-реквесты
вопросы
Торговая площадка
Исследовать
 
@DenisMikhaylov 
DenisMikhaylov
/
DA-100-Analyzing-Data-with-Power-BI
Public
Code
Issues
Pull requests
Projects
Wiki
Security
Insights
Settings
DA-100-Analyzing-Data-with-Power-BI/Instructions/Labs/01-prepare-data-with-power-query-in-power-bi-desktop.md
@shannonlindsay
shannonlindsay Updating lab instructions
…
Latest commit e33ad56 on 14 Sep 2021
 History
 2 contributors
@shannonlindsay@weslbo
352 lines (178 sloc)  16.1 KB

---
Лабораторная:
    Название: 'Подготовка к  Power BI Desktop'
    Модуль: 'Module 2 - Получение данных в Power BI'
---

# **Подготовка данных в Power BI Desktop**

**Расчетное время выполнения лабораторной работы 45 минут.**

В этом лабораторном занятии вы начнете разработку решения Power BI Desktop для компании Adventure Works. Он включает подключение к исходным данным, предварительный просмотр данных и использование методов предварительного просмотра данных для понимания характеристик и качества исходных данных.


В этой лабораторной работе вы научитесь:

-Открывать Power BI Desktop

- Настраивать параметры Power BI Desktop

- Подключать источники данных

- Смотреть предварительные данные перед их подключением

- Используйте методы предварительного просмотра данных, чтобы лучше понять данные

### **Выполнение лабораторной**


## **Упражнение 1: Подготовка данных**

В этом упражнении вы создадите восемь запросов Power BI Desktop. Шесть запросов будут получать данные из SQL Server, а два — из CSV-файлов.

### **Задача 1: Сохранение файла Power BI Desktop**

In this task you will first save the Power BI Desktop file.

1. В этой задаче вы сначала сохраните файл Power BI Desktop.

 	![Picture 2](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image1.png)

1. Чтобы закрыть окно начала работы, в правом верхнем углу окна щелкните **X**.

 	![Picture 3](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image2.png)

1. Чтобы сохранить файл, щелкните вкладку ленты **Файл**, чтобы открыть представление Backstage..

1. Выберите **Save**.

 	![Picture 4](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image3.png)

1. В окне **Save As**, Выберите папку **D:\DA100\MySolution**.

1. В поле **File Name**, Введите название файла **Sales Analysis**.

 	![Picture 14](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image4.png)

1. Нажмите **Save**.

	![Picture 17](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image5.png)

	Подсказка: Вы также можете сохранить файл, нажав значок **Сохранить**, расположенный в левом верхнем углу.

	![Picture 18](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image6.png)

### **Задача 2: НАстрофка параеметров Power BI Desktop**

В этой задаче вы установите параметры Power BI Desktop.

1. В Power BI Desktop, нажмите **File** на ленте меню.

1. в левой панели, выбирите **Options and Settings**, и выбирите **Options**.

 	![Picture 1](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image7.png)

1. В окне **Options**, слева, в группе **Current File**, выбирите **Data Load**.

    ![Picture 5](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image8.png)

    Параметры **Data Load** для текущего файла позволяют задавать параметры, определяющие поведение по умолчанию при моделировании.

1. В группе **Relationships** ,уберите выбор двух параеметров.

	![Picture 7](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image9.png)

    Хотя включение этих двух параметров может быть полезно при разработке модели данных, вы отключили их ранее для поддержки лабораторного опыта. При создании взаимосвязей в лабораторной работе **Загрузка данных в Power BI Desktop** вы узнаете, почему вы добавляете каждую из них.

1. Нажмите **OK**.

    ![Picture 9](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image10.png)

1. Сохраните файл Power BI Desktop.

### **Задача 3: Получение данных из MS SQL Server**

В этом задании вы создадите запросы на основе таблиц SQL Server.

1. В ленте меню выбирите **Home** , в группе **Data** , нажмите на **SQL Server**.

	![Picture 19](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image11.png)

2. В окне **SQL Server Database**, в поле **Server**, введите **Имя сервера (дополнительно имя инстанса если это есть)** название серевера уточните у преподователя.

	![Picture 21](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image12.png)

	
3. Нажмите **OK**.

	![Picture 22](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image13.png)

4. В окне **Navigator**, в левой части, раскрояте базу данных **AdventureWorksDW2020**.

	![Picture 28](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image17.png)

5. Наэмите на таблицу **DimEmployee**, но не ставьте чекбокс.

	![Picture 29](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image18.png)

6. В правой панели, загрузиться предварительно еотображение данных.

	Данные предварительного просмотра позволяют определить столбцы и выборку строк..

7. Чтобы подключить таблицы, установите флажок рядом со следующими таблицами:

	- DimEmployee

	- DimEmployeeSalesTerritory

	- DimProduct

	- DimReseller

	- DimSalesTerritory

	- FactResellerSales

8. Чтобы преобразовать данные выбранных таблиц, нажмите **Transform Data**.

	Вы не будете преобразовывать данные в этой лаборатории. Задачи этого практического занятия сосредоточены на изучении и профилировании данных в окне **Power Query Editor**.

	![Picture 30](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image19.png)

### **Задача 4: Просмотр запросов MS SQL Server**

В этой задаче вы предварительно просмотрите данные запросов SQL Server. Во-первых, вы узнаете актуальную информацию о данных. Вы также будете использовать инструменты качества столбца, распределения столбца и профиля столбца, чтобы понять данные и оценить качество данных..

1. В окне **Power Query Editor** , В левой части, находиться панель **Queries**.

	![Picture 31](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image20.png)

	Панель **Queries** находятся запросы к данным, один запрос на одну таблицу.

2. Выбирите первый запрос —**DimEmployee**.

	![Picture 33](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image21.png)

	Таблица **DimEmployee** в базе данных SQL Server хранит одну строку для каждого сотрудника. Подмножество строк из этой таблицы представляет продавцов, которые будут иметь отношение к модели, которую вы разработаете.

3. At the bottom left, in the status bar, notice the table statistics—the table has 33 columns, and 296 rows.

	![Picture 36](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image22.png)

4. In the data preview pane, scroll horizontally to review all columns.

5. Notice that the last five columns contain **Table** or **Value** links.

	These five columns represent relationships to other tables in the database. They can be used to join tables together. You’ll join tables in the **Load Data in Power BI Desktop** lab.

6. To assess column quality, on the **View** ribbon tab, from inside the **Data Preview** group, check **Column Quality**.

	![Picture 35](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image23.png)

	The column quality feature allows you to easily determine the percentage of valid, error, or empty values found in columns.

7. For the **Position** column (sixth last column), notice that 94% of rows are empty (null).

	![Picture 38](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image24.png)

8. To assess column distribution, on the **View** ribbon tab, from inside the **Data Preview** group, check **Column Distribution**.

	![Picture 40](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image25.png)

9. Review the **Position** column again, and notice that there are four distinct values, and one unique value.

10. Review the column distribution for the **EmployeeKey** (first) column—there are 296 distinct values, and 296 unique values.

	![Picture 43](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image26.png)

	When the distinct and unique counts are the same, it means the column contains unique values. When modeling, it’s important that some model tables have unique columns. These unique columns can be used to create one-to-many relationships, which you will do in the **Model Data in Power BI Desktop, Part 1** lab.

11. In the **Queries** pane, select the **DimEmployeeSalesTerritory** query.

	![Picture 44](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image27.png)

	The **DimEmployeeSalesTerritory** table stores one row for each employee and the sales territory regions they manage. The table supports relating many regions to a single employee. Some employees manage one, two, or possibly more regions. When you model this data, you’ll need to define a many-to-many relationship, which you’ll do in the **Model Data in Power BI Desktop, Part 2** lab.

12. In the **Queries** pane, select the **DimProduct** query.

	![Picture 46](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image28.png)

	The **DimProduct** table contains one row per product sold by the company.

13. Horizontally scroll to reveal the last columns.

14. Notice the **DimProductSubcategory** column.

	When you add transformations to this query in the **Load Data in Power BI Desktop** lab, you’ll use the **DimProductSubcategory** column to join tables.

15. In the **Queries** pane, select the **DimReseller** query.

	![Picture 49](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image29.png)

	The **DimReseller** table contains one row per reseller. Resellers sell, distribute, or value add to the Adventure Works products.

16. To view column values, on the **View** ribbon tab, from inside the **Data Preview** group, check **Column Profile**.

	![Picture 41](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image30.png)

17. Select the **BusinessType** column header.

18. Notice the new pane beneath the data preview pane.

19. Review the column statistics and value distribution in the data preview pane.

20. Notice the data quality issue: there are two labels for warehouse (**Warehouse**, and the misspelled **Ware House**).

	![Picture 51](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image31.png)

21. Hover the cursor over the **Ware House** bar, and notice that there are five rows with this value.

    You’ll apply a transformation to relabel these five rows in the **Load Data in Power BI Desktop** lab.

22. In the **Queries** pane, select the **DimSalesTerritory** query.

	![Picture 52](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image32.png)

	The **DimSalesTerritory** table contains one row per sales region, including **Corporate HQ** (headquarters). Regions are assigned to a country, and countries are assigned to groups. In the **Model Data in Power BI Desktop, Part 1** lab, you’ll create a hierarchy to support analysis at region, country, or group level.

23. In the **Queries** pane, select the **FactResellerSales** query.

	![Picture 54](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image33.png)

	The **FactResellerSales** table contains one row per sales order line—a sales order contains one or more line items.

24. Review the column quality for the **TotalProductCost** column, and notice that 8% of the rows are empty.

	![Picture 63](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image34.png)

	Missing **TotalProductCost** column values is a data quality issue. To address the issue, in the **Load Data in Power BI Desktop** lab, you’ll apply transformations to fill in missing values by using the product standard cost, which is stored in the related **DimProduct** table.

### **Task 5: Get data from a CSV file**

In this task you will create a query based on a CSV file.

1. To add a new query, in the **Power Query Editor** window, on the **Home** ribbon tab, from inside the **New Query** group, click the **New Source** down-arrow, and then select **Text/CSV**.

	![Picture 70](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image35.png)

2. In the **Open** window, navigate to the **D:\DA100\Resources** folder, and select the **ResellerSalesTargets.csv** file.

3. Click **Open**.

4. In the **ResellerSalesTargets.csv** window, review the preview data.

5. Click **OK**.

	![Picture 71](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image36.png)

  
‎ 

6. In the **Queries** pane, notice the addition of the **ResellerSalesTargets** query.

	![Picture 72](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image37.png)

	The **ResellerSalesTargets** CSV file contains one row per salesperson, per year. Each row records 12 monthly sales targets (expressed in thousands). Note that the business year for the Adventure Works company commences on July 1.

7. Notice that no column contains empty values.

	When there isn’t a monthly sales target, a hyphen character is stored instead.

8. Review the icons in each column header, to the left of the column name.

	![Picture 74](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image38.png)

	The icons represent the column data type. **123** is whole number, and **ABC** is text.

	You’ll apply many transformations to achieve a different shaped result consisting of only three columns: **Date**, **EmployeeKey**, and **TargetAmount** in the **Load Data in Power BI Desktop** lab.

### **Task 6: Get additional data from a CSV file**

In this task you will create an additional query based on a different CSV file.

1. Use the steps in the previous task to create a query based on the **D:\DA100\Resources\ColorFormats.csv** file.

	![Picture 75](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image39.png)

	The **ColorFormats** CSV file contains one row per product color. Each row records the HEX codes to format background and font colors. You’ll integrate this data with the **DimProduct** query data in the **Load Data in Power BI Desktop** lab.

### **Task 7: Finish up**

In this task you will complete the lab.

1. On the **View** ribbon tab, from inside the **Data Preview** group, uncheck the three data preview options that were previously enabled in this lab:

	- Column quality

	- Column distribution

	- Column profile

	![Picture 76](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image40.png)

2. To save the Power BI Desktop file, in the **Power Query Editor** window, on the **File** backstage view, select **Save**.

	![Picture 77](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image41.png)

3. When prompted to apply the queries, click **Apply Later**.

	![Picture 86](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image42.png)

	Applying the queries will load their data to the data model. You’re not ready to do that, as there are many transformations that must be applied first.

4. If you intend to start the next lab, leave Power BI Desktop open.

	You’ll apply various transformations to the queries and then apply the queries to load them to the data model in the **Load Data in Power BI Desktop** lab.
Footer
© 2022 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
DA-100-Analyzing-Data-with-Power-BI/01-prepare-data-with-power-query-in-power-bi-desktop.md at master · DenisMikhaylov/DA-100-Analyzing-Data-with-Power-BI

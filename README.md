# Goudawn-of-dax-function-


Average Promotion = AVERAGE('Onyx Data - DataDNA Dataset Cha'[Promotions])
Avg_Monthly_Salary = AVERAGE('Onyx Data - DataDNA Dataset Cha'[Monthly_Salary])
Total Employee = DISTINCTCOUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID])
Total_Active_Employees = 
CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Resigned] = FALSE)
Total_Resigned_Employees = 
CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Resigned] = TRUE)
Avg_Monthly_Salary_Female = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Monthly_Salary]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female"
)
Avg_Monthly_Salary_Male = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Monthly_Salary]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male"
)
Avg_Monthly_Salary_Other = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Monthly_Salary]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other"
)
Churn_Rate = 
DIVIDE(
    CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Resigned] = TRUE),
    COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]),
    0
)
Avg Work Hours = AVERAGE('Onyx Data - DataDNA Dataset Cha'[Work_Hours_Per_Week])
Avg_Work_Hours_Female = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Work_Hours_Per_Week]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female"
)

Avg_Work_Hours_Male = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Work_Hours_Per_Week]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male"
)

Avg_Work_Hours_Other = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Work_Hours_Per_Week]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other"
)

Avg Years at Company = AVERAGE('Onyx Data - DataDNA Dataset Cha'[Years_At_Company])
Average_Years_At_Company_Female = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Years_At_Company]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female"
)
Average_Years_At_Company_Male = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Years_At_Company]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male"
)
Average_Years_At_Company_Other = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Years_At_Company]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other"
)
Avg_Projects_Handled_Monthly = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Projects_Handled]),
    'Onyx Data - DataDNA Dataset Cha'[Day_of_Week] <> BLANK()
)

Avg_Projects_Handled_Weekly = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Projects_Handled]),
    'Onyx Data - DataDNA Dataset Cha'[Day_of_Week] <> BLANK()
)

Avg_Projects_Per_Year = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Projects_Handled]), 
    VALUES('Onyx Data - DataDNA Dataset Cha'[Year])
)

Avg_Sick_Days_Female = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Sick_Days]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female"
)
Avg_Sick_Days_Male = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Sick_Days]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male"
)

Avg_Sick_Days_Other = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Sick_Days]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other"
)
Churn_Rate = 
DIVIDE(
    CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Resigned] = TRUE),
    COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]),
    0
)

Churn_Rate_Female = 
DIVIDE(
    CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female", 'Onyx Data - DataDNA Dataset Cha'[Resigned] = TRUE),
    CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female"),
    0
)

Churn_Rate_Male = 
DIVIDE(
    CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male", 'Onyx Data - DataDNA Dataset Cha'[Resigned] = TRUE),
    CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male"),
    0
)

Churn_Rate_Other = 
DIVIDE(
    CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other", 'Onyx Data - DataDNA Dataset Cha'[Resigned] = TRUE),
    CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other"),
    0
)

Employee_Growth_Percent = 
DIVIDE(
    [Total_Employees_Selected_Year] - [Total_Employees_Previous_Year],
    [Total_Employees_Previous_Year],
    0
)

Employees_Had_Sick = 
CALCULATE(
    COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    'Onyx Data - DataDNA Dataset Cha'[Sick_Days] > 0
)
Employees_More_Than_One_Promotion = 
CALCULATE(
    COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    'Onyx Data - DataDNA Dataset Cha'[Promotions] > 1
)

Employees_Never_Sick = 
CALCULATE(
    COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    'Onyx Data - DataDNA Dataset Cha'[Sick_Days] = 0
)
Highest_Avg_Work_Hours_Day = 
CALCULATE(
    MAXX(
        SUMMARIZE(
            'Onyx Data - DataDNA Dataset Cha',
            'Onyx Data - DataDNA Dataset Cha'[Day_of_Week],
            "Avg_Work_Hours", AVERAGE('Onyx Data - DataDNA Dataset Cha'[Work_Hours_Per_Week])
        ),
        [Avg_Work_Hours]
    )
)

Highest_Project_Handled = 
MAX('Onyx Data - DataDNA Dataset Cha'[Projects_Handled])

Lowest_Project_Handled = 
CALCULATE(
    MIN('Onyx Data - DataDNA Dataset Cha'[Projects_Handled]),
    'Onyx Data - DataDNA Dataset Cha'[Projects_Handled] > 0
)

Avg_Overtime_Hours = 
AVERAGE('Onyx Data - DataDNA Dataset Cha'[Overtime_Hours])

Avg_Overtime_Hours_Female = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Overtime_Hours]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female"
)

Avg_Overtime_Hours_Male = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Overtime_Hours]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male"
)

Avg_Overtime_Hours_Other = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Overtime_Hours]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other"
)

Percentage_Sick_Days_Female = 
DIVIDE(
    CALCULATE(
        SUM('Onyx Data - DataDNA Dataset Cha'[Sick_Days]),
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female"
    ),
    [Total_Sick_Days],
    0
)
Percentage_Sick_Days_Male = 
DIVIDE(
    CALCULATE(
        SUM('Onyx Data - DataDNA Dataset Cha'[Sick_Days]),
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male"
    ),
    [Total_Sick_Days],
    0
)

Percentage_Sick_Days_Other = 
DIVIDE(
    CALCULATE(
        SUM('Onyx Data - DataDNA Dataset Cha'[Sick_Days]),
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other"
    ),
    [Total_Sick_Days],
    0
)
Average Project Handled = AVERAGE('Onyx Data - DataDNA Dataset Cha'[Projects_Handled])
Promotion_Percentage_Female = 
DIVIDE(
    CALCULATE(
        COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
        'Onyx Data - DataDNA Dataset Cha'[Promotions] > 0,
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female"
    ),
    [Total_Promotions_All],
    0
)

Promotion_Percentage_Male = 
DIVIDE(
    CALCULATE(
        COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
        'Onyx Data - DataDNA Dataset Cha'[Promotions] > 0,
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male"
    ),
    [Total_Promotions_All],
    0
)

Promotion_Percentage_Other = 
DIVIDE(
    CALCULATE(
        COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
        'Onyx Data - DataDNA Dataset Cha'[Promotions] > 0,
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other"
    ),
    [Total_Promotions_All],
    0
)

Promotion_Rate = 
DIVIDE(
    CALCULATE(COUNTROWS('Onyx Data - DataDNA Dataset Cha'), 'Onyx Data - DataDNA Dataset Cha'[Promotions] > 0),
    COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    0
)
Promotion_Rate_Female = 
DIVIDE(
    CALCULATE(
        COUNTROWS('Onyx Data - DataDNA Dataset Cha'), 
        'Onyx Data - DataDNA Dataset Cha'[Promotions] > 0, 
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female"
    ),
    CALCULATE(
        COUNTROWS('Onyx Data - DataDNA Dataset Cha'), 
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female"
    ),
    0
)
Promotion_Rate_Male = 
DIVIDE(
    CALCULATE(
        COUNTROWS('Onyx Data - DataDNA Dataset Cha'), 
        'Onyx Data - DataDNA Dataset Cha'[Promotions] > 0, 
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male"
    ),
    CALCULATE(
        COUNTROWS('Onyx Data - DataDNA Dataset Cha'), 
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male"
    ),
    0
)

Promotion_Rate_Other = 
DIVIDE(
    CALCULATE(
        COUNTROWS('Onyx Data - DataDNA Dataset Cha'), 
        'Onyx Data - DataDNA Dataset Cha'[Promotions] > 0, 
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other"
    ),
    CALCULATE(
        COUNTROWS('Onyx Data - DataDNA Dataset Cha'), 
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other"
    ),
    0
)
Total_Promotions_All = 
CALCULATE(
    COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    'Onyx Data - DataDNA Dataset Cha'[Promotions] > 0
)
Total_Promotions_By_Gender = 
CALCULATE(
    COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    'Onyx Data - DataDNA Dataset Cha'[Promotions] > 0
)

Total_Promotions_Female = 
CALCULATE(
    COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    'Onyx Data - DataDNA Dataset Cha'[Promotions] > 0,
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female"
)

Total_Promotions_Male = 
CALCULATE(
    COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    'Onyx Data - DataDNA Dataset Cha'[Promotions] > 0,
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male"
)

Total_Promotions_Other = 
CALCULATE(
    COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    'Onyx Data - DataDNA Dataset Cha'[Promotions] > 0,
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other"
)

Resignation_Rate = DIVIDE(CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Resigned] = TRUE), COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 0)


Resigned_Female = 
CALCULATE(
    COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female",
    'Onyx Data - DataDNA Dataset Cha'[Resigned] = TRUE
)
Resigned_Female = 
CALCULATE(
    COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female",
    'Onyx Data - DataDNA Dataset Cha'[Resigned] = TRUE
)

Resigned_Male = 
CALCULATE(
    COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male",
    'Onyx Data - DataDNA Dataset Cha'[Resigned] = TRUE
)

Resigned_Other = 
CALCULATE(
    COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other",
    'Onyx Data - DataDNA Dataset Cha'[Resigned] = TRUE
)

Retention_Rate = 
DIVIDE(
    CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Resigned] = FALSE),
    COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]),
    0
) 

Retention_Rate_Female = 
DIVIDE(
    CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female", 'Onyx Data - DataDNA Dataset Cha'[Resigned] = FALSE),
    CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female"),
    0
)

Retention_Rate_Male = 
DIVIDE(
    CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male", 'Onyx Data - DataDNA Dataset Cha'[Resigned] = FALSE),
    CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male"),
    0
)

Retention_Rate_Other = 
DIVIDE(
    CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other", 'Onyx Data - DataDNA Dataset Cha'[Resigned] = FALSE),
    CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other"),
    0
)

Avg_Performance_Score = AVERAGE('Onyx Data - DataDNA Dataset Cha'[Performance_Score])

Avg_Satisfaction_Score = AVERAGE('Onyx Data - DataDNA Dataset Cha'[Employee_Satisfaction_Score])

Avg_Sick_Days = 
AVERAGE('Onyx Data - DataDNA Dataset Cha'[Sick_Days])

Avg_Sick_Days_Per_Year = 
CALCULATE(
    AVERAGE('Onyx Data - DataDNA Dataset Cha'[Sick_Days]),
    ALLEXCEPT('Onyx Data - DataDNA Dataset Cha', 'Onyx Data - DataDNA Dataset Cha'[Year])
)

Sick_Days_Above_7_Percentage = 
DIVIDE(
    COUNTROWS(
        FILTER(
            'Onyx Data - DataDNA Dataset Cha',
            'Onyx Data - DataDNA Dataset Cha'[Sick_Days] > 7
        )
    ),
    COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    0
)

Sick_Days_Percentage = 
DIVIDE(
    SUM('Onyx Data - DataDNA Dataset Cha'[Sick_Days]),
    20 * COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    0
)

Sick_Days_Percentage_New = 
DIVIDE(
    SUM('Onyx Data - DataDNA Dataset Cha'[Sick_Days]),
    COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    0
)

Sick_Days_Percentage_Newest = 
DIVIDE(
    SUM('Onyx Data - DataDNA Dataset Cha'[Sick_Days]),
    240 * COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    0
)

Total Employee = DISTINCTCOUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID])
Total_Employees_Female = 
CALCULATE(
    COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female"
)

Total_Employees_Male = 
CALCULATE(
    COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male"
)

Total_Employees_Other = 
CALCULATE(
    COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other"
)

Total_Projects_Handled = SUM('Onyx Data - DataDNA Dataset Cha'[Projects_Handled])

Total_Resigned_Employees = 
CALCULATE(COUNT('Onyx Data - DataDNA Dataset Cha'[Employee_ID]), 'Onyx Data - DataDNA Dataset Cha'[Resigned] = TRUE)

Total Training Hours = SUM('Onyx Data - DataDNA Dataset Cha'[Training_Hours])
Total_Employees_Previous_Year = 
CALCULATE(
    COUNTROWS('Onyx Data - DataDNA Dataset Cha'),
    PREVIOUSYEAR('Onyx Data - DataDNA Dataset Cha'[Hire_Date])
)

Total_Employees_Selected_Year = 
COUNTROWS('Onyx Data - DataDNA Dataset Cha')

Total_Projects_Female = 
CALCULATE(
    SUM('Onyx Data - DataDNA Dataset Cha'[Projects_Handled]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female"
)

Total_Projects_Male = 
CALCULATE(
    SUM('Onyx Data - DataDNA Dataset Cha'[Projects_Handled]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male"
)

Total_Projects_Other = 
CALCULATE(
    SUM('Onyx Data - DataDNA Dataset Cha'[Projects_Handled]),
    'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other"
)

Total_Sick_Days = 
SUM('Onyx Data - DataDNA Dataset Cha'[Sick_Days])
YoY_Female_Change_Color = 
VAR __PREV_YEAR = 
    CALCULATE(
        [Total Employee], 
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female", 
        DATEADD('Onyx Data - DataDNA Dataset Cha'[Hire_Date].[Date], -1, YEAR)
    )
VAR __YoY_CHANGE = 
    DIVIDE(
        CALCULATE([Total Employee], 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female") - __PREV_YEAR, 
        __PREV_YEAR
    )
RETURN
    IF(
        __YoY_CHANGE > 0, 
        "Green", 
        IF(
            __YoY_CHANGE < 0, 
            "Red", 
            "Gray"  // You can adjust this color if needed for no change
        )
    )

YoY_Female_Employee = 
VAR __PREV_YEAR =
    CALCULATE(
        [Total Employee],
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female",
        DATEADD('Onyx Data - DataDNA Dataset Cha'[Hire_Date].[Date], -1, YEAR)
    )
RETURN
    DIVIDE(
        CALCULATE([Total Employee], 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female") - __PREV_YEAR,
        __PREV_YEAR
    )

YoY_Female_Employee_New = 
VAR __PREV_YEAR = 
    CALCULATE(
        [Total Employee], 
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female", 
        DATEADD('Onyx Data - DataDNA Dataset Cha'[Hire_Date].[Date], -1, YEAR)
    )
VAR __YoY_CHANGE = 
    DIVIDE(
        CALCULATE([Total Employee], 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Female") - __PREV_YEAR, 
        __PREV_YEAR
    )
RETURN
    IF(
        __YoY_CHANGE > 0, 
        FORMAT(__YoY_CHANGE, "0.00%") & " ▲", 
        IF(
            __YoY_CHANGE < 0, 
            FORMAT(__YoY_CHANGE, "0.00%") & " ▼", 
            FORMAT(__YoY_CHANGE, "0.00%") & " --"
        )
    )

YoY_Male_Change_Color = 
VAR __PREV_YEAR = 
    CALCULATE(
        [Total Employee], 
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male", 
        DATEADD('Onyx Data - DataDNA Dataset Cha'[Hire_Date].[Date], -1, YEAR)
    )
VAR __YoY_CHANGE = 
    DIVIDE(
        CALCULATE([Total Employee], 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male") - __PREV_YEAR, 
        __PREV_YEAR
    )
RETURN
    IF(
        __YoY_CHANGE > 0, 
        "Green", 
        IF(
            __YoY_CHANGE < 0, 
            "Red", 
            "Gray"  // You can adjust this color if needed for no change
        )
    )

YoY_Male_Employee = 
VAR __PREV_YEAR =
    CALCULATE(
        [Total Employee],
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male",
        DATEADD('Onyx Data - DataDNA Dataset Cha'[Hire_Date].[Date], -1, YEAR)
    )
RETURN
    DIVIDE(
        CALCULATE([Total Employee], 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male") - __PREV_YEAR,
        __PREV_YEAR
    )

YoY_Male_Employee_New = 
VAR __PREV_YEAR = 
    CALCULATE(
        [Total Employee], 
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male", 
        DATEADD('Onyx Data - DataDNA Dataset Cha'[Hire_Date].[Date], -1, YEAR)
    )
VAR __YoY_CHANGE = 
    DIVIDE(
        CALCULATE([Total Employee], 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Male") - __PREV_YEAR, 
        __PREV_YEAR
    )
RETURN
    IF(
        __YoY_CHANGE > 0, 
        FORMAT(__YoY_CHANGE, "0.00%") & " ▲", 
        IF(
            __YoY_CHANGE < 0, 
            FORMAT(__YoY_CHANGE, "0.00%") & " ▼", 
            FORMAT(__YoY_CHANGE, "0.00%") & " --"
        )
    )

YoY_Other_Change_Color = 
VAR __PREV_YEAR = 
    CALCULATE(
        [Total Employee], 
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other", 
        DATEADD('Onyx Data - DataDNA Dataset Cha'[Hire_Date].[Date], -1, YEAR)
    )
VAR __YoY_CHANGE = 
    DIVIDE(
        CALCULATE([Total Employee], 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other") - __PREV_YEAR, 
        __PREV_YEAR
    )
RETURN
    IF(
        __YoY_CHANGE > 0, 
        "Green", 
        IF(
            __YoY_CHANGE < 0, 
            "Red", 
            "Gray"  // You can adjust this color if needed for no change
        )
    )

YoY_Other_Employee = 
VAR __PREV_YEAR =
    CALCULATE(
        [Total Employee],
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other",
        DATEADD('Onyx Data - DataDNA Dataset Cha'[Hire_Date].[Date], -1, YEAR)
    )
RETURN
    DIVIDE(
        CALCULATE([Total Employee], 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other") - __PREV_YEAR,
        __PREV_YEAR
    )

YoY_Other_Employee_New = 
VAR __PREV_YEAR = 
    CALCULATE(
        [Total Employee], 
        'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other", 
        DATEADD('Onyx Data - DataDNA Dataset Cha'[Hire_Date].[Date], -1, YEAR)
    )
VAR __YoY_CHANGE = 
    DIVIDE(
        CALCULATE([Total Employee], 'Onyx Data - DataDNA Dataset Cha'[Gender] = "Other") - __PREV_YEAR, 
        __PREV_YEAR
    )
RETURN
    IF(
        __YoY_CHANGE > 0, 
        FORMAT(__YoY_CHANGE, "0.00%") & " ▲", 
        IF(
            __YoY_CHANGE < 0, 
            FORMAT(__YoY_CHANGE, "0.00%") & " ▼", 
            FORMAT(__YoY_CHANGE, "0.00%") & " --"
        )
    )
Promotion_Description = 
SWITCH(
    TRUE(),
    'Onyx Data - DataDNA Dataset Cha'[Promotions] = 0, "No Promotion",
    'Onyx Data - DataDNA Dataset Cha'[Promotions] = 1, "Promoted Once",
    'Onyx Data - DataDNA Dataset Cha'[Promotions] > 1, "Promoted More Than Once")
Monthly_Salary_Classification = 
SWITCH(
    TRUE(),
    'Onyx Data - DataDNA Dataset Cha'[Monthly_Salary] <= 4000, "Under 4k",
    'Onyx Data - DataDNA Dataset Cha'[Monthly_Salary] <= 5000, "4k - 5k",
    'Onyx Data - DataDNA Dataset Cha'[Monthly_Salary] <= 6000, "5k - 6k",
    'Onyx Data - DataDNA Dataset Cha'[Monthly_Salary] <= 7000, "6k - 7k",
    'Onyx Data - DataDNA Dataset Cha'[Monthly_Salary] <= 9000, "7k - 9k",
    "Above 9k"
)

Remote_Work_Label = 
SWITCH(
    TRUE(),
    'Onyx Data - DataDNA Dataset Cha'[Remote_Work_Frequency] = 0, "No Remote Work",
    'Onyx Data - DataDNA Dataset Cha'[Remote_Work_Frequency] = 25, "Occasional Remote Work",
    'Onyx Data - DataDNA Dataset Cha'[Remote_Work_Frequency] = 50, "Half Remote Work",
    'Onyx Data - DataDNA Dataset Cha'[Remote_Work_Frequency] = 75, "Mostly Remote Work",
    'Onyx Data - DataDNA Dataset Cha'[Remote_Work_Frequency] = 100, "Fully Remote Work",
    "Unknown"
)
Remote_Work_Status = 
IF(
    'Onyx Data - DataDNA Dataset Cha'[Remote_Work_Frequency] = 0, 
    "No Remote Work", 
    "Remote Work"
)

Satisfaction_Group = IF('Onyx Data - DataDNA Dataset Cha'[Employee_Satisfaction_Score] < 3, "Low", IF('Onyx Data - DataDNA Dataset Cha'[Employee_Satisfaction_Score] < 4, "Medium", "High"))
Sick_Days_Class = 
SWITCH(
    TRUE(),
    'Onyx Data - DataDNA Dataset Cha'[Sick_Days] = 0, "Never Sick",
    'Onyx Data - DataDNA Dataset Cha'[Sick_Days] <= 7, "Under 7 Days Or Equal",
    "Above 7 Days"
)
Team_Size_Group = 
SWITCH(
    TRUE(),
    'Onyx Data - DataDNA Dataset Cha'[Team_Size] >= 1 && 'Onyx Data - DataDNA Dataset Cha'[Team_Size] <= 5, "Small Team (1-5)",
    'Onyx Data - DataDNA Dataset Cha'[Team_Size] >= 6 && 'Onyx Data - DataDNA Dataset Cha'[Team_Size] <= 10, "Medium Team (6-10)",
    'Onyx Data - DataDNA Dataset Cha'[Team_Size] >= 11 && 'Onyx Data - DataDNA Dataset Cha'[Team_Size] <= 15, "Large Team (11-15)",
    'Onyx Data - DataDNA Dataset Cha'[Team_Size] >= 16 && 'Onyx Data - DataDNA Dataset Cha'[Team_Size] <= 19, "Very Large Team (16-19)",
    "Other"
)
Total Employee YoY% = 
IF(
    ISFILTERED('Onyx Data - DataDNA Dataset Cha'[Hire_Date]),
    ERROR("Time intelligence quick measures can only be grouped or filtered by the Power BI-provided date hierarchy or primary date column."),
    VAR __PREV_YEAR =
        CALCULATE(
            [Total Employee],
            DATEADD('Onyx Data - DataDNA Dataset Cha'[Hire_Date].[Date], -1, YEAR)
        )
    RETURN
        DIVIDE([Total Employee] - __PREV_YEAR, __PREV_YEAR)
)
Total Employee YTD = 
IF(
    ISFILTERED('Onyx Data - DataDNA Dataset Cha'[Hire_Date]),
    ERROR("Time intelligence quick measures can only be grouped or filtered by the Power BI-provided date hierarchy or primary date column."),
    TOTALYTD(
        [Total Employee],
        'Onyx Data - DataDNA Dataset Cha'[Hire_Date].[Date]
    )
)
Years_of_Service_Group = 
SWITCH(
    TRUE(),
    'Onyx Data - DataDNA Dataset Cha'[Years_At_Company] <= 1, "0-1 Year",
    'Onyx Data - DataDNA Dataset Cha'[Years_At_Company] <= 5, "2-5 Years",
    'Onyx Data - DataDNA Dataset Cha'[Years_At_Company] <= 10, "6-10 Years",
    "Above 10 Years"
)



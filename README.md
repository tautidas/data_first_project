# data_first_project
First full data science project for learning purposes
-------------------------
1 review and handling data

    load data.
    sample 5 rows.
        review values
        review column names
            find column names descriptions https://www.kaggle.com/datasets/pavlofesenko/titanic-extended
    review each column
        check nan values
        check column type
    drop small value columns.
        PassengerId
        Body
    rename column names according python variable naming convention https://stackoverflow.com/questions/159720/what-is-the-naming-convention-in-python-for-variable-and-function
    count column survived values, include nan values into the output.
    create a new dataset that holds non-null values Survived columns.
    reset new dataset index, use attribute drop=True
    review each column of new dataset
        check nan values
        check column type
    fill nan values.
        age - fill in using median value of age and pclass group.
        cabin
            option 1 [easy]: sample from existing cabins random cabin and assign to a class groups.
            option 2 [hard]: check cabin naming convention with respect to a class. Create new cabin numbers. Assign randomly for class groups. [additional]
        do we need to fill nan in lifeboat?
            if yes fill na, else create a value indicating that a passenged did not use a boat.
    drop rest of the rows that have at least one nan value.
----------------------------------
2 data transformations

    find and remove duplicates
    add a name to column index. name = "features".
    transform embarked column values to port names. Use map function and dictionary.
    compare column "embarked" and "boarded" values. Unify and drop "boarded" column.
    compare column "age" and "age_wiki" values. Unify and drop "age_wiki" column.
    compare column "pclass" and "class" values. Unify and drop "class" column.
    drop column "wikiid"
    use map function to extract town and country from Hometown column. Extracted values save as additional columns df["home_town"], df["home_country"]
    use map function to extract town and country from Hometown column. Extracted values save as additional columns df["destition_town"], df["destination_country"]
    create a column that indicates - is traveler coming home or emigrating. Column name "travel_direction"
    create dummy variables from column "sex".
    create column "age_groups" by puting age column values into bins. 0-12,12-18,18-25,25-35, 35-50,50-65,65+. Use pd.cut function.
    create column "labeled_age_groups" by puting age column values into bins. 0-12,12-18,18-25,25-35, 35-50,50-65,65+. Use pd.cut function. and create labels for every bin.
    create column "fare_quantiles" from column "fare". Use pd.qcut. Print out quantile edge values.
----------------------------------------
3 string manipulation

    create column "initials" using column "name". Initials are Mr., Mrs., etc..
    create column "wiki_initials" using column "name_wiki". Initials are Mr., Mrs., etc..
    compare column "initials" and "wiki_initials" values. Unify and drop "wiki_initials" column.
    create column "first_name" using columns "name" and "name_wiki". If person has more than one name extract all names.
    create column "last_name" using columns "name" and "name_wiki". If person has more than one surname extract all surnames.
    drop columns "name" and "name_wiki"
----------------------------------------
4 EDA
9.1  Plot

    Plot column "survived" values as pie chart and bar plot.
    Plot "sex" column values.
    Split "survived" values by "sex". Plot survived values split by sex.
    create corsstab using columns "survived" and "pclass".
    Split "survived" values by "pclass". Plot survived values split by pclass.
    create crosstab using columns "survived" and keys "pclass" and "sex".
    Draw factorplot using seaboarn. sns.factorplot.
    draw survived plot with respect to "age_groups".
    draw survived plot with respect to "labeled_age_groups".
    draw survived plot with respect to "fare_quantiles".

9.2  Investigate groups

    Find top 5 most common names splitted by class.
    Find top 5 most common names splitted by class and sex.
    Find top 5 most common names splitted by class and age groups.
    Count passengers traveling home or emigrating.
    Count passengers by continents.
    Count passengers by countries.
    Count passengers by cities.
    plot survived column by countries.
    plot survived column by continents.
    what is the distribution of classes with respect to destination country/town?
    what is the distribution of classes with respect to embarked pord?

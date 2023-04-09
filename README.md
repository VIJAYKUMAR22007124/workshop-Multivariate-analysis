# Workshop-Multivariate-analysis

AIM:

    To perform Exploratory Data Analysis in the given data set to understand the operations done on data analysis.
    Perform both the types of EDA(i.e.,Between Numerical & Numerical and Between Numerical & Categorial).
    Use plots like barplot.boxplot,scatterplot,etc.
    
ALGORITHM:  

STEP 1 :

     Upload the Dataset provided in Google Colab
     
STEP 2 :

     Print the data.Use head(),info(),describe(),tail() functions.
     
STEP 3 :  

     Use scatterplots(between Numerical values) to display the informations in graphs.
     
STEP 4 : 

     Use box,barplots(between Numerical and categorial) to display in graphs.
     
STEP 5 : 

    Print the whole page of your operatios done in colab and convert to a pdf.
   
   
CODE:
```
    import pandas as pd 
    import seaborn as sns
    df = pd.read_csv("FlightInformation.csv")
    print(df)
    
    sns.scatterplot(x = df['Price'], y=df['Total_Stops'])
    
    df.info()
    
    df.describe()
    
    sns.barplot(x = "Price",y="Destination",data=df)
    
    sns.barplot(x = "Price",y="Source",data=df)
    
    Decor=df.loc[:,["Source","Price"]]
    Decor=Decor.groupby(by=["Source"]).sum().sort_values(by="Price")
    sns.barplot(x=Decor.index,y="Price",data=Decor)
    
    Decor=df.loc[:,["Airline","Price"]]
    Decor=Decor.groupby(by=["Airline"]).sum().sort_values(by="Price")
    sns.barplot(x=Decor.index,y="Price",data=Decor)
    
    sns.barplot(x = df['Price'], y=df['Source'],hue = df['Airline'])
    
    df.head()
    
    df.tail()

```

OUTPUT:

![Screenshot (290)](https://user-images.githubusercontent.com/119657657/230766411-88c558d1-caad-48bf-825d-742f8832f36a.png)


![Screenshot (291)](https://user-images.githubusercontent.com/119657657/230766434-f667a3e6-c8c5-45fd-81e2-268da5cde66b.png)


![Screenshot (292)](https://user-images.githubusercontent.com/119657657/230766448-a0f73ff6-9d8f-4a39-bfa8-4f624bf10a36.png)


![Screenshot (293)](https://user-images.githubusercontent.com/119657657/230766453-e180f235-baba-46f6-bcbd-8de56ff619f4.png)


![Screenshot (294)](https://user-images.githubusercontent.com/119657657/230766461-9d80238c-1d4c-4c0a-862f-8db89302aca4.png)


![Screenshot (295)](https://user-images.githubusercontent.com/119657657/230766470-9f38c2d5-cf09-43c9-9e6e-44e6304e536c.png)


![Screenshot (296)](https://user-images.githubusercontent.com/119657657/230766478-9da3acaf-5af2-445f-8d45-d24e2715c73a.png)


RESULTS:

      Both the types of the Bivariate/Multivariate Analysis is done using the given dataset and graphs are received as outcomes.





    

# Understanding Suicide
First approach to suicide in Spain. Bivariate analysis of time series and forecasting. Suicide and Unemployment 1998-2017.

May, 2019

## OBJECTIVES

This project has two main questions to solve:

- How do Unemployment and Suicide in Spain behave monthly?
- Is there a relationship between both events?


To try to answer these questions, the following data sources will be used:

- Monthly data of the number of suicides in Spain from 1998 to 2017 (included). The is the 
Statistics National Institute of Spain (INE) -> https://www.ine.es (open data source)
- Monthly data of the number of unemployed in Spain from 1998 to 2017 (included). The source is the
Public Service of State Employment in Spain (SEPE) -> https://www.sepe.es (open data source)

## DATA DESCRIPTION

### *Data of suicide in Spain*
The INE does not collect all the data for this period in the same place or in the same format. For this reason we have been forced to group the data in two periods:
- ![Number of suicides per month from 1998 to 2004 (included)] (http://www.ine.es/jaxi/Tabla.htm?path=/t18/p427/a1998/l0/&file=03013.px) (Spanish).
- ![Number of suicides per month from 2005 to 2017 (included)] (https://www.ine.es/jaxi/Tabla.htm?path=/t15/p417/a2005/l0/&file=05006.px&L=0) (Spanish).

As of 2013, the INE has access to data from the Forensic Anatomy Institute of Madrid and introduces a methodological improvement that has allowed them to more accurately assign the cause of death in deaths with judicial intervention (deaths that were assigned to ill-defined causes they have been reassigned to specific external causes).

### *Data of unemployment in Spain*
In the same way, the SEPE does not collect data for the entire period to be analyzed in the same site or in the same format. This time we are going to group the data in four periods:
- ![Registered unemployment per month from 1996 to 2005 (April)] (https://www.sepe.es/HomeSepe/que-es-el-sepe/estadisticas/empleo.html).
- Registered unemployment per month from 2005 (May) to 2007 (included).
- Registered unemployment per month from 2008 to 2012 (included).
- Registered unemployment per month from 2013 to 2017 (included).

During the realization of this project SEPE has changed its website. Now you can find the monthly summary of the employment data from 
2005 (May) to 2019 here -> https://www.sepe.es/HomeSepe/que-es-el-sepe/estadisticas/datos-avance/datos.html (Spanish)


Since 2005, SEPE use another methodology for data registration (SISPE), so the data from 1996 to mid-2005 are estimates of what the 
values would have been if they had applied this methodology.


All data has been downloaded, grouped and saved in the ![Data](https://github.com/tonilopezrosell/understandingsuicide/tree/master/Data) folder of this repository.


To execute the code it is necessary to download the ![understandingsuicide Github repository] (https://github.com/tonilopezrosell/understandingsuicide). This contains all the necessary directory structure and data files. 


## CODE DESCRIPTION

The code to obtain the final data of the study has been divided into two Python (3.7.3) notebooks and one of R (3.5.1) that are in understandingsuicide/.

To execute the code it will be necessary to have installed in the system Python and R. The study has been done on the Windows 10 OS and the code has been written in Jupyter Notebooks (IRKernel, IPython) of the Anaconda 3 framework.

*You have to execute the scripts in the following order*
### *1.Suicide_Time_Series_Reading_and_Cleansing_Data.ipynb (IPython)*
We load, clean, select and shape all the groups of files that we have collected about the number of suicides per month in Spain from 1998 to 2017 by the INE.

The final result is a csv with a time series with the total number of suicides per month in Spain from 1998 to 2017 (included). That csv will be saved in the 'Data' folder as 'Monthly_suicide_Spain_1998-2017.csv'

The needed libraries are: numpy, pandas and os.

### *2.Unemployment_Time_Series_Reading_and_Cleansing_Data.ipynb (IPython)*

We load, clean, select and shape all the groups of files that we have collected about the number of unemployed per month in Spain from 1998 to 2017 by the SEPE.

The final result is a csv with a time series with the total number of unemployed per month in Spain from 1998 to 2017 (included). That csv will be saved in the 'Data' folder as 'Monthly_unemployment_Spain_1998-2017.csv'.

The needed libraries are: numpy, pandas and os.

### *3.Time_Series_Analysis_Forecasting_and_Cross_Correlation_Suicide_and_Unemployment_in_Spain.ipynb (IRkernel)*

We analyze the time series of suicide and unemployment in Spain from 1998 to 2017, make some forecasts and study the relationship that may exist between both series.

## REPORT AND GRAPHS

## Mini Project1: JSON Based Data Exercise

This mini project takes advantage of a World Bank dataset from a school quality improvement project in Ethiopia to demonstrate the use of JSON files. There are 3 questions asked. The questions, the approach and the final answers are below:

#### Question 1: Find the 10 countries with most projects

Approach:
- Load the JSON data as a PANDAS dataframe
- Group by countryname 
- Aggregate by count, sort by descending count
- Filter the top 10 most frequently appearing country names

```
countryname
People's Republic of China         19
Republic of Indonesia              19
Socialist Republic of Vietnam      17
Republic of India                  16
Republic of Yemen                  13
Nepal                              12
People's Republic of Bangladesh    12
Kingdom of Morocco                 12
Africa                             11
Republic of Mozambique             11
Name: countryname, dtype: int64
```

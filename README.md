## Mini Project1: JSON Based Data Exercise

This mini project takes advantage of a World Bank dataset from a school quality improvement project in Ethiopia to demonstrate the use of JSON files. There are 3 questions asked. The questions, the approach and the final answers are below:

#### Question 1: Find the 10 countries with most projects

**Approach:**
- Load the JSON data as a PANDAS dataframe
- Group by countryname 
- Aggregate by count, sort by descending count
- Filter the top 10 most frequently appearing country names

**Output:**
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

#### Question 2: Find the top 10 major project themes

**Approach:**
- Load the JSON data 
- Normalize by the `mjtheme_namecode` variable and save as a pandas dataframe
- With the same approach as in the last question, list the 10 most frequencty accuring `name`s.

**Output:**
```
name
Environment and natural resources management    223
Rural development                               202
Human development                               197
Public sector governance                        184
Social protection and risk management           158
Financial and private sector development        130
                                                122
Social dev/gender/inclusion                     119
Trade and integration                            72
Urban development                                47
Name: name, dtype: int64
```

#### Question 3: Create a dataframe with the missing names filled in

**Approach:**

- Using the same dataframe created in previous question, make a 2-way tabulation of the values of `code` and `name` to verify that each `code` is either only associated to one value of `name` or the `name` is missing,
- Create a second dataframe of unique `code` and,non missing, `name` values,
- Merge this dataframe with the original dataframe by `code`
- Replace the old `name` column with the new one
- Drop the extra `name` column
- Rename variables to their original names
- Verify there is no missing `name`

**Output:**

```
# Verifying there's no missing name
merged[merged.name=='']


code	name
```

# Step 1: Independent Data Audit
**Dataset overview**
The dataset contains illustrative price observations for four items across two cities, recorded over 12 dates.

Consists of 97 rows and 6 columns, and explicitly states that the observations are not actual Pbs observations.

**Initial inspection**
The dataset was laoded through pandas and examined through basic inspection commands, showing:
97 observations and 6 columns
12 distinct observation dates
four intended item categories
two cities
a missing value in the price column
price column having an object data type instead of numerical
all other columns have complete values

# code used
df.shape
df.head()
df.info()
df.isnull().sum()
df.describe(include='all')

# identifying data quality issues

*issue 1: missing value*
one price observation is missing; pulse c in city 2 on january 1, 2026
*code used:*
df.isnull().sum()
df[df['price'].isnull()]
*decision:*
flag and investigate missing obsrervation. this shouldnt be replaced with a false estimate without sufficient supporting information.

*issue 2: inconsistent data type*
the price column is stored as an object rather than a numeric data type. this is also because of a comma formatted value (1,250)
*code used:*
df.info()
df['price'].value_counts()
*decision:*
standardise numerical formatting and convert valid prices into a numeric data type, saving the original values for comaprison.

*issue 3: duplicate observation*
theres on exact duplicate row; observation for staple a in city 1 on january 8 comes twice.
*code used:*
df.duplicated().sum()
df[df.duplicated(keep=False)]
*decision:*
verify duplicate and remove the additional copy, as it doesnt represent a different observation.

*issue 4: inconsistent category label*
the item label 'oil b' appears in lowercase, while other observations use Oil B.
*code used:*
df.['item'].value_counts()
*decision:*
standardise captialization to Oil B, after confriming that both labels are of the same item.

*issue 5: suspicious price observations*
multiple prices seem to be inconsistent with the surrounding observations;
staple a, cty 2, jan 15, 2026: 1,250
sweetener d, city 1, jan 22, 2026: 9999
oil b, city 1, feb 5, 2026: 108.5
*code used:*
df['price'].value_counts()
df[df'price].astype.str.isin(['1,250', '9999', '108.5'])
*decision:*
flag these for investiagtuion. unusual values shouldnt automatically be treated as errors or deleted witout evidences of the correct values being present.

## dataset hash
**hash algorithm:** SHA-256
**original dataset fingerprint**
5818DAD3807487D4E37F764E5D19CBAA152EDD78FE4DB182EB28B087C8709D35


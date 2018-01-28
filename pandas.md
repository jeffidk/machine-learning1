http://www.gregreda.com/

data school

dronap
dataframe.dropna().head()


rename column name
dataframe_name.columns = dataframe_name.columns.str.replace(‘old’, ‘new’)
dataframe.rename{‘oldcol1’:’newcol1’, ‘oldcol2’:’newcol2’}, axis = ‘columns’)
dataframe.rename{str.upper, , axis = ‘columns’)

axis
axis 0: to apply a method down each column, vertical
axis 1:to apply a method across each row, horizontal

remove cola and colb
dataframe_name.drop([‘cola’,’colb’], axis=1, inplace=True)

remove linea and lineb
dataframe_name.drop([indexa,indexb], axis=0, inplace=True)

sort rows
booleans = []
for iter in dataframe.column:
	if iter > 2:
		boolean.append(True)
	else:
		boolean.append(False)

ismorethan2 = pd.Series(booleans)
dataframe[ismorethan2]

ismorethan2 = dataframe.column >2
dataframe[dataframe.column >2]

select different values in a column
dataframe.column.isin([‘value1', 'value2' ])

groupby
dataframe.groupby(‘colum_with_finite_values’).column.agg([‘min’, ‘max’,’count’])

map (rename the values of a column from a to new_a and b to new_b, create a new column for these new values)
dataframe[‘new_column’] = data frame.col.map({‘a’:new_a, ‘b’:new_b})

apply (apply a function to a Serie)
dataframe['new_column’]=dataframe.column.apply(np.ceil)
dataframe[:,’col1’:’coln'].apply(max, axis=0) #max des colonnes
dataframe[:,’col1’:’coln'].apply(max, axis=1) #max des lignes

applymap (apply to the whole dataset, not column or row)

#remove all non numerical column
dataframe.select_dtypes(include=[np.number]) 

string operation on column
dataframe.column.str.replace(‘from’,’to’).astype(float).mean

somme des valeurs manquantes des colonnes.
dataframe.isnull().sum()

concat 2 dataframes l’un à coté de l’autre
pd.concat([dataframe1, dataframe2], axis=1)

find occurrences of an item in a column
dataframe.column.value_count

find the type of the data in a column
dataframe.dtypes

vlookup
mapping = {‘cat1’:’yes’, ‘cat2’:’no', ‘cat3’:’yes’}
dataframe.col_with_cat.map(mapping)

sort with key
>>> def get_score(nom_et_score):
...     return nom_et_score[1] # retourne le 2nd element du tuple
... 
>>> sorted(scores.items(), key=get_score) # on passe la fonction a key
[('Roger', 1), ('Robert', 2), ('Cunegonde', 3), ('Gertrude', 4)]

import but modify a column (here remove dollar sign)
headers = ['name', 'title', 'department', 'salary']
chicago = pd.read_csv('city-of-chicago-salaries.csv', 
                      header=0,
                      names=headers,
                      converters={'salary': lambda x: float(x.replace('$', ''))})


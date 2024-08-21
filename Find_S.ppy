import pandas as pd
import numpy as np


df = pd.read_csv(r'C:\Users\yuvas\Downloads\archive (4).zip')
print(df)
print(" ")


print("The number of rows and columns:", df.shape)
print(" ")

last_row = np.array(df)[:, :-1]
print("After Removing the last column in the dataset \n", last_row)
print(" ")

print("The number of rows and columns after removing the last column:", last_row.shape)
print(" ")


target = np.array(df)[:, -1]
print("Target concept \n", target)
print(" ")


hypothesis = None


for i, val in enumerate(target):
    if val.lower() == "yes":  
        hypothesis = last_row[i].copy()
        break

print("Initial hypothesis: ", hypothesis)


for i, var in enumerate(last_row):
    if target[i].lower() == "yes":
        for x in range(len(hypothesis)):
            if var[x] != hypothesis[x]:
                hypothesis[x] = '?'  

print("Final hypothesis: ", hypothesis)

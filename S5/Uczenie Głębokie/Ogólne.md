5 osobowy projekt 

najpózniej do 11 tyogdnia semestru

przydatne komendy 
df_train = (df_train - min_) / (max_ - min_) # standaryzacja do [0,1]


####  relu
jak kombinacja ważona sumuje się do czegoś wiecej niż 0 to ją przekazujemy dalej
a jak 0 to usuwa 

wszystkie wyjścia z pierwszej warsty nieujemne 

warstwa ostatnia i przedostatnia tworzy regresje logistyczną 


### Explicación del proceso de Script

# Inicialmente buscaba importar los datos en excel, ya que al pasarlos a csv, quizá por la forma en la que estaba construida la tabla, arrojaba error, por lo que preferí trabajar en excel y al final pasarlo a csv.


import pandas as pd

# Mostrar el excel (cuando lo hago en csv me tira error no entiendo el porqué)
datos = pd.read_excel("/content/drive/MyDrive/Colab Notebooks/Cat-checklist-at-February-2023 (1).xlsx")

## hice este filtro para quitar la posibilidad de dejar afuera variantes que no fuesen "Chile", agregué por lo tanto "CHILE" y "chile", creo que finalmente todos estaban como "Chile", pero lo dejé como parte del proceso. 

# definir el filtro de las formas que se puede escribir chile con mayusculas
chile = "Chile"
chile2 = "CHILE"
chile3 = "chile"

## Aquí cree un data frame que haga el filtro con las formas de escribir Chile en las diferentes columnas

# Filtrar los datos para las variables de búsqueda
datos_chile = datos[datos["Countries"].str.contains(chile) | datos["Countries"].str.contains(chile2) | datos["Countries"].str.contains(chile3)]

## Luego de ese filtro realizado, comenzó el proceso de realizar una nueva base de datos, por lo que investigué y fui metiendo todo a un excel que mantuviese una estructura similar a los datos filtrados previamente para que no hubiera problemas a la hora de unirlos. Específicamente, me preocupé de que en ambos excel estuviese la columna "Scientific name" y que a partir de esa columna se unieran. Ese excel lo cargué y lo uní con inner join: 


# nuevos datos recolectados de diferentes sitios web (base de datos propia, fuentes en la entrega)
datos2 = pd.read_excel("/content/drive/MyDrive/Colab Notebooks/Gatos datos extras.xlsx")

#fusionar datos
fusion_de_datos = datos_chile.merge(datos2, on="Scientific name", how="inner")

# print el resultado
print(fusion_de_datos)


## para cumplir con los requisitos de la entrega pasé todo a csv, en realidad no sabía como hacerlo, entonces google bastante hasta llegar a una solución. Por lo que, con total honestidad, no entiendo muy bien qué hace el codigo de abajo, lo importante es que funciona para lo que lo quería


#pasar a csv y descargar

fusion_de_datos.to_csv("/content/drive/MyDrive/Colab Notebooks/resultados_fusionados.csv", index=False)






Nombre
Explicación de cómo se realizó el proceso de limpieza de datos, cada paso y decisión tomada.
Lista de las fuentes de datos utilizadas y una explicación de por qué las eligieron.
Algunos ejemplos sobre preguntas que se pueden responder su base de datos limpia (3 mínimo).
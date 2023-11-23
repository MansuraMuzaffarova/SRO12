# SRO12
import pandas as pd

finance_data = pd.read_csv("data.csv", header=0, sep=",")

pd.set_option('display.max_columns', None)
pd.set_option('display.max_rows', None)

print(finance_data.describe())

import pandas as pd
import numpy as np

school_grades = {
    'Математика': [90, 85, 92, 78, 88],
    'Русский': [85, 88, 90, 92, 78],
    'Физика': [92, 87, 95, 80, 85],
    'Литература': [78, 80, 85, 90, 88],
    'Химия': [85, 92, 88, 78, 90]
}

grades_df = pd.DataFrame(data=school_grades)

# Используем персентиль 10 для столбца "Физика"
percentile10_physics = np.percentile(grades_df['Физика'], 10)

print("Персентиль 10 для Физики:", percentile10_physics


import pandas as pd
import numpy as np

school_grades = {
    'Математика': [90, 85, 92, 78, 88],
    'Русский': [85, 88, 90, 92, 78],
    'Физика': [92, 87, 95, 80, 85],
    'Литература': [78, 80, 85, 90, 88],
    'Химия': [85, 92, 88, 78, 90]
}

grades_df = pd.DataFrame(data=school_grades)

# Используем столбец "Математика" для вычисления стандартного отклонения
std_math = np.std(grades_df['Математика'])

print("Стандартное отклонение для Математики:", std_math)


import pandas as pd
import numpy as np

univer_data = pd.read_csv("data.csv", header=0, sep=",")

var = np.var(univer_data)

print(var)



import sys
import matplotlib
matplotlib.use('Agg')

import pandas as pd
import matplotlib.pyplot as plt

health_data = pd.read_csv("data.csv", header=0, sep=",")
health_data.plot(x='Height', y='Weight', kind='scatter')

# Показать график
plt.show()
plt.savefig(sys.stdout.buffer)
sys.stdout.flush()


import pandas as pd

full_univer_data = pd.read_csv("data.csv", header=0, sep=",")

Corr_Matrix = round(full_univer_data.corr(),2)

print(Corr_Matrix)



#Three lines to make our compiler able to draw:
import sys
import matplotlib
matplotlib.use('Agg')

import pandas as pd
import matplotlib.pyplot as plt

# Пример с данными о финансах
Income = [5000, 6000, 5500, 7000, 8000, 7500, 9000, 9500, 8500, 10000]
Expenses = [2000, 2500, 2200, 2800, 3000, 2700, 3200, 3500, 3300, 3800]
Profit = [3000, 3500, 3300, 4200, 5000, 4800, 5800, 6000, 5200, 6200]

Finance_Data = {"Income": Income, "Expenses": Expenses, "Profit": Profit}
Finance_DF = pd.DataFrame(data=Finance_Data)

Finance_DF.plot(x="Expenses", y="Income", kind="scatter")
plt.show()

correlation_finance = Finance_DF.corr()
print(correlation_finance)

#Two lines to make our compiler able to draw:
plt.savefig(sys.stdout.buffer)
sys.stdout.flush()



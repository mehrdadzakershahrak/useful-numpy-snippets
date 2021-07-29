# useful-numpy-snippets

__IMPORTS__

    import numpy as np

__IMPORTING/EXPORTING__

    np.loadtxt('file.txt') - From a text file
    # From a CSV file
    np.genfromtxt('file.csv',delimiter=',')
    # Writes to a text file
    np.savetxt('file.txt',arr,delimiter=' ')
    # Writes to a CSV file
    np.savetxt('file.csv',arr,delimiter=',')


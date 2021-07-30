# useful-numpy-snippets

__Imports__

    import numpy as np

__Importing and Exporting__

    np.loadtxt('file.txt') - From a text file
    # From a CSV file
    np.genfromtxt('file.csv',delimiter=',')
    # Writes to a CSV file
    np.savetxt('file.csv',arr,delimiter=',')
    # Writes to a text file
    np.savetxt('file.txt',arr,delimiter=' ')

**Creating Arrays**

    # One dimensional array
    np.array([1,2,3])
    # Two dimensional array
    np.array([(1,2,3),(4,5,6)])
    # 1D array of length 3 all values 0
    np.zeros(3)
    # 3x4 array with all values 1
    np.ones((3,4))
    # 5x5 array (Identity matrix) of 0 with 1 on diagonal
    np.eye(5)
    # Array of 6 evenly divided values from 0 to 100
    np.linspace(0,100,6)
    # Array of values from 0 to less than 10 with step 3 (eg [0,3,6,9])
    np.arange(0,10,3)
    # 2x3 array with all values 8
    np.full((2,3),8)
    # 4x5 array of random floats between 0-1
    np.random.rand(4,5)
    # 6x7 array of random floats between 0-100
    np.random.rand(6,7)*100
    # 2x3 array with random ints between 0-4
    np.random.randint(5,size=(2,3))

__Ispecting Properties__

    # Returns number of elements in arr
    arr.size
    # Returns dimensions of arr (rows, columns)
    arr.shape
    # Returns type of elements in arr
    arr.dtype
    # Convert arr elements to type dtype
    arr.astype(dtype)
    # Convert arr to a Python list
    arr.tolist()
    # View documentation for np.eye
    np.info(np.eye)

__Copying/Sorting/Reshaping__
    # Copies arr to new memory
    np.copy(arr)
    # Creates view of arr elements with type dtype
    arr.view(dtype)
    # Sorts arr
    arr.sort()
    # Sorts specific axis of arr
    arr.sort(axis=0)
    # Flattens 2D array two_d_arr to 1D
    two_d_arr.flatten()


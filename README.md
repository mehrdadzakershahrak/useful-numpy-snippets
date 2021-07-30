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
    # Transposes arr (rows become columns and vice versa)
    arr.T
    # Reshapes arr to 3 rows, 4 columns without changing data
    arr.reshape(3,4) 
    # Changes arr shape to 5x6 and fills new values with 0
    arr.resize((5,6))

__Adding/Removing Elements__

    # Appends values to end of arr
    np.append(arr,values)
    # Inserts values into arr before index 2
    np.insert(arr,2,values)
    # Deletes row on index 3 of arr
    np.delete(arr,3,axis=0)
    # Deletes column on index 4 of arr
    np.delete(arr,4,axis=1)

__Combining/Slitting__

    # Adds arr2 as rows to the end of arr1
    np.concatenate((arr1,arr2),axis=0)
    # Adds arr2 as columns to end of arr1
    np.concatenate((arr1,arr2),axis=1)
    # Splits arr into 3 sub-arrays
    np.split(arr,3)
    # Splits arr horizontally on the 5th index
    np.hsplit(arr,5)

__Indexing/Slicing/Subsetting__

    # Returns the element at index 5
    arr[5]
    # Returns the 2D array element on index[2][5]
    arr[2,5]
    # Assigns array element on index 1 the value 4
    arr[1]=4
    # Assigns array element on index[1][3] the value 10
    arr[1,3]=10
    # Returns the elements at indices 0,1,2 (On a 2D array: returns rows 0,1,2)
    arr[0:3]
    # Returns the elements on rows 0,1,2 at column 4
    arr[0:3,4]
    # Returns the elements at indices 0,1 (On a 2D array: returns rows 0,1)
    arr[:2]
    # Returns the elements at index 1 on all rows
    arr[:,1]
    # Returns an array with boolean values 
    arr<5
    #  Returns an array with boolean values
    (arr1<3) & (arr2>5)
    # Inverts a boolean array
    ~arr
    # Returns array elements smaller than 5
    arr[arr<5]
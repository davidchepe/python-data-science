# Numpy

NumPy is the fundamental package for scientific computing with Python. It contains among other things:

* a powerful N-dimensional array object
* sophisticated (broadcasting) functions
* tools for integrating C/C++ and Fortran code
* useful linear algebra, Fourier transform, and random number capabilities

Besides its obvious scientific uses, NumPy can also be used as an efficient multi-dimensional container of generic data. Arbitrary data-types can be defined. This allows NumPy to seamlessly and speedily integrate with a wide variety of databases.

## Summary

1. [Array Creation, Methods & Printing](#numpy-A)
2. [Basic Operations](#numpy-B)
3. [Universal Functions](#numpy-C)
4. [Indexing, Slicing and Iterating](#numpy-D)
5. [Shape Manipulation](#numpy-E)
6. [Linear Algebra](#numpy-F)
7. [Tricks and Tips](#numpy-G)

<a id='numpy-A'></a>
### Array Creation, Methods & Printing 

numpy.array is not the same as the Standard Python class array.array which only handles one-dimensional arrays and offers less functionality

|        Function         |             Action                |
|:-----------------------:|:---------------------------------:|
| arr_1 = np.array([...]) | Initialize numpy array            |
|      arr_1.ndim         | returns number of dimensions      |
|      arr_1.shape        | returns shape of the array        |
|      arr_1.dytpe        | returns type of elements in array |
|      arr_1.mean()       | returns mean of elements in array |
|      arr_1.sum()        | returns sum of elements in array  |
|      arr_1.min()        | returns min of array              |
|      arr_1.max()        | returns max of array              |
 

Build a two dimensional array (matrix):
```python
np.array([(1.5,2,3), (4,5,6)])
```

Build a matrix with elements of a specific type:
```python
np.array( [ [1,2], [3,4] ], dtype=complex)
```


Often, the elements of an array are originally unknown, but its size is known. Hence, NumPy offers several functions to create arrays with initial placeholder content. These minimize the necessity of growing arrays, an expensive operation.

The function zeros creates an array full of zeros, the function ones creates an array full of ones, and the function empty creates an array whose initial content is random and depends on the state of the memory. By default, the dtype of the created array is float64.

Initialize with 4 zeros:
```python
np.zeros(4)
```

Initialize with 4 zeros along column:
```python
np.zeros((1,4))
[Out] array([[ 0.,  0.,  0.,  0.]])
```

Initialize with ones:
```python
np.ones((1,4))
[Out] array([[ 1.,  1.,  1.,  1.]])
```


```python
#Initialize an empty array:

np.empty(4)
[Out] array([[ 0.,  0.,  0.,  0.]])
```

Initialize an array with a series:
> np.arange(10, 40, 10) #arange(min,max,step)
> 
> array([10, 20, 30])

Initialize with a more sophisticated series:
> np.linspace(10,40,10) #create 10 ticks between 10 and 40
> 
> array([ 10.,  13.33333333,  16.66666667,  20.,23.33333333,  26.66666667,  30.,33.33333333, 36.66666667,40.])

<a id='numpy-B'></a>
### Basic Operations

> a = np.array( [20,30,40,50] )
> 
> b = np.arange( 4 )
> 
> 


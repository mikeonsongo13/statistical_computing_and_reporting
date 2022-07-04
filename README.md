# statistical_computing_and_reporting
assignmet on linear algebra
This git is for learn  and expaining how linear algebra is done in python using numpy and all 



Welcome to the statistical_computing_and_reporting wiki!

# Linear Algebra in python 
This article will show you how to perform some linear algebra calculations using python.
To be specific using the NumPy module.
Numpy is a python module widely used to handle n-dimensional arrays.
Numpy can handle large Multi-dimensional arrays and matrices, along with an extensive collection of mathematical operations to operate on the arrays. It stands for Numerical python.
Arrays occupy less space and are extremely convenient to use as compared to python lists. Also, it has a mechanism for specifying data types.
Numerous problems in science and engineering can be described or approximated by linear relationships. For example, if you combined resistors in a complicated circuit, you will obtain a system of linear relationships.
## Sets
In mathematics, a set is a collection of objects. A set is denoted be braces{} for example t={2,4,6,8,10}
An empty set is denoted by {} empty braces or by  ∅ . Given two sets A and B 
the intersect is denoted by A ∩ B set of all the elements in both A and B.
 the union is denoted by A∪B set of all the elements of A and B.
The colon is used to mean "such that". \ is used to mean the complement of a set. In mathematics, there are various types of sets that are related to numbers real, integers irrational, complex, whole, and rational numbers.
A set is defined as follows 

***
S={(x,y):x,y∈R,x2+y2=1} 
which means S is a set of all real numbers (x,y) such that x2+y2=1



***

## vectors
The set  R^n is the set of all n-tuples of real numbers. In set notation this is R^n={(x1,x2,x3,⋯,xn):x1,x2,x3,⋯,xn∈R}.For example the set R^3 represents the set of real triples (x,y,z) coordinates in the 3D space.
A vecotr in R^n is a n-tuple in R^n. vectros can be written horizontally(row vector) and vertically (column vector).
The normal of a vector is measure of the length of a vector  L2 most common norm "euclidian distance" denoted by||v2||
∥v∥2=√∑iv2i. 

Create a row vector and column vector, and show the shape of the vectors.


In Python, the row vector and column vector are a little bit tricky. You can see from the above in order to get the 1 row and 4 columns or 4 rows and 1 column vectors, we have to use the list of list to specify it. You can define np.array([1,2,3,4]), but you will soon notice that it doesn’t contain information about row or column.
Transpose the row vector we defined above into a column vector and calculate the L1, L2, and L∞ norm of it. Verify that the L∞ norm of a vector is equivalent to the maximum value of the elements in the vector.




Vector addition is defined as the pairwise addition of each of the elements of the added vectors. For example, if v and w are vectors in Rn, then u=v+w is defined as ui=vi+wi.

Vector multiplication can be defined in several ways depending on the context. Scalar multiplication of a vector is the product of a vector and a scalar (i.e., a number in R). Scalar multiplication is defined as the product of each element of the vector by the scalar. More specifically, if α is a scalar and v is a vector, then u=αv is defined as ui=αvi. Note that this is exactly how Python implements scalar multiplication with a vector.

Show that a(v+w)=av+aw (i.e., scalar multiplication of a vector distributes across vector addition).

By vector addition, u=v+w is the vector with ui=vi+wi. By scalar multiplication of a vector, x=αu is the vector with xi=α(vi+wi). Since α,vi, and wi are scalars, multiplication distributes and xi=αvi+αwi. Therefore, a(v+w)=av+aw.
The dot product of two vectors is the sum of the product of the respective elements in each vector and is denoted by ⋅, and v⋅w is read “v dot w.” Therefore for v and w ∈Rn,d=v⋅w is defined as d=∑ni=1viwi. The angle between two vectors, θ, is defined by the formula:

***


v⋅w=∥v∥2∥w∥2cosθ
***
The dot product is a measure of how similarly directed the two vectors are. For example, the vectors (1,1) and (2,2) are parallel. If you compute the angle between them using the dot product, you will find that θ=0. If the angle between the vectors, θ=π/2, then the vectors are said to be perpendicular or orthogonal, and the dot product is 0.

Compute the angle between the vectors v=[10,9,3] and w=[2,5,12].


Finally, the cross product between two vectors, v and w, is written v×w. It is defined by v×w=∥v∥2∥w∥2sin(θ)n, where θ is the angle between the v and w (which can be computed from the dot product) and n is a vector perpendicular to both v and w with unit length (i.e., the length is one). The geometric interpretation of the cross product is a vector perpendicular to both v and w with length equal to the area enclosed by the parallelogram created by the two vectors.

 Given the vectors v=[0,2,0] and w=[3,0,0], use the Numpy function cross to compute the cross product of v and w.



A set is called linearly independent if no object in the set can be written as a linear combination of the other objects in the set. For the purposes of this book, we will only consider the linear independence of a set of vectors. A set of vectors that is not linearly independent is linearly dependent.

Given the row vectors v=[0,3,2], w=[4,1,1], and u=[0,−2,0], write the vector x=[−8,−1,4] as a linear combination of v, w, and u.




## Matrices
An m×n matrix is a rectangular table of numbers consisting of m rows and n columns. The norm of a matrix can be considered as a particular kind of vector norm, if we treat the m×n elements of M are the elements of an mn dimensional vector, then the p-norm of this vector can be write as:

***
∥M∥p=(∑im∑jn|aij|p)

***

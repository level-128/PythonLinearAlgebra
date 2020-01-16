# PythonLinearAlgebra
This code implements part of the algorithm in Gilbert Strang's 
Introduction to Linear Algebra, and it is completely written in Python. 

---
## CATALOG:
1. Introduction
2. Licence
3. Tutorial
4. APIs

---
## INTRODUCTION:
I'm a high school student who is studying Linear Algebra with the 
Professor Gillbert Strang’s MIT OpenCourse. This is the code I used
to practice linear algebra on.

This code includes most linear algebra operations as well as a basic 
interactive command line that allows users to perform computations.

To run this code, a python3 interpreter (3.6 and above) is required. 
And also, no 3rd library is used in this code.

---
## Licence 
This software is licensed under the GNU General Public License v3.0

Copyright (C) 2020  Weizheng Wang

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <https://www.gnu.org/licenses/>.

---
## Tutorial

this code could be imported by other python scripts by using:

    import alice
    # or
    from alice import *
    
or using interactive console:

    this is a basic compute software of linear algebra developed by Wang Weizheng
    For more information, type 'copyright()' or 'about()' in the console.


    >>>

To exit the console (if you are using the console), type exit().
the console could accept python commands (a single line of code).

#### Next step, start compute:
To create matrix or vector:

    # create a matrix
    X = matrix([[1,2,3],[2,3,4],[-1,-1,-1]])
    
    # X =  [ 1    2    3]
    #      [ 2    3    4]
    #      [-1   -1   -1]
    
    # create a vector
    Y = vector([1,2,3])
    
    # Y = 1i_hat + 2j_hat + 3k_hat
    # 
    # or it is same with
    #
    # Y = [1]
    #     [2]
    #     [3]
    
To perform basic operations:

    X*Y  
    # matrix:
    #    [14]
    #    [20]
    #    [-6]
    
    X+X
    # matrix:
    # [2, 4, 6]
    # [4, 6, 8]
    # [-2, -2, -2]
    
    X.transpose()
    # matrix:
    # [1, 2, -1]
    # [2, 3, -1]
    # [3, 4, -1]
    
    X.invert()
    # the matrix is singular. It is uninvertible.
    
    Y.module()
    # 3.7416573867739413
    
    
    
    
To generate a random matrix:

    # generate a 4*4 matrix, from 0 to 10, integer value
    X = matrix.random_matrix(5,6,2,-3,int)
    # matrix:
    # [-3, 2, 0, 0, 1, 1]
    # [0, -3, -3, -2, 2, -2]
    # [-1, 0, -3, 0, 0, 1]
    # [-1, 2, 1, -2, 2, -2]
    # [-2, 0, 0, -2, -1, 0]

    # generate a default 4*4 matrix, from 0 to 10, by default, floating point value
    X = print(matrix.random_matrix(type_ = float))
    # matrix:
    # [3.5043241003, 0.3713558007, 3.7324463516, 5.2982786823]
    # [2.4268259983, 4.8068851973, 9.7347697987, 6.8648311404]
    # [0.189252822, 7.126140657, 5.6800361683, 7.6905833487]
    # [8.1493381191, 7.0644692704, 1.7996603637, 6.6048587747]

    # generate a 3*4 matrix, from 0+0j to 10+10j, by default, integer real and imagine value
    print(matrix.random_matrix(type_ = (complex, int), row = 3))
    # matrix:
    # [(3+2j), (10+3j), 1j, (6+0j)]
    # [(9+5j), 7j, (8+5j), (3+6j)]
    # [(1+4j), (8+4j), (7+8j), (10+9j)]

To perform advanced operations:

    Z = matrix([[1,2,3],[2,3,4],[-1,-1,-1],[3,4,5]])
    
    Z.null_space()
    # [vector:
    # [1.0, -2.0, 1.0]
    # ]
    
    Z.column_space()
    # [vector:
    # [1, 2, -1, 3]
    # , vector:
    # [2, 3, -1, 4]
    # ]
    
    # get the row reduced form of matrix Z
    Z.reduced_echelon_form()
    # matrix:
    # [1.0, 0.0, -1.0]
    # [-0.0, 1.0, 2.0]
    # [0.0, 0.0, 0.0]
    # [0.0, 0.0, 0.0]
    
    matrix.least_square([[1,2],[2,3],[4,4],[5,4]])
    # least square of [[1, 2], [2, 3], [4, 4], [5, 4]] for y = Cx + D:
    # C = 0.5000000000000006, D = 1.749999999999998


### Other methods could be found in the APIs
    
    
    
    
    
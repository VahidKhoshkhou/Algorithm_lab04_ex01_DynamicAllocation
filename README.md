# Algorithm_lab04_ex01_DynamicAllocation
###This is an exercise in Algorithms in C Language :

### Requirements :
A file has the following format:
- the first row contains an integer number n
- the following n rows store a string (each string is terminated
  by a '\n' character).
The longest string included in the file is 100 character long but
the average string length is much smaller (e.g., 10 characters).

A C program receives two file names on the command line (input and
output file names).
The first file has the format previously specified.
The program:
1) reads the content of the first (input) file and stores all strings
   into a dynamic data structure
2) orders the strings in alphabetic order
3) stores the strings in the second (output) file.
   The output file has the same format of the input one.

Write two versions of the program:

- The first one stores all words in an 1D dynamic array of structures
  with dynamic fields.

  The structure should be defined as:
  struct string {
    char *str;
  };

  A first "malloc" allocates the array.
  One more "malloc" for each array element allocates the string space
  to store each string.

- The second one stores all word in a 2D dynamic matrix of characters:

  The dynamic matrix can be defined as:
  char **mat;
  and each string stored on a row of the matrix such that
  mat[i] (or &mat[i][0])
  is the pointer to the first character of the string in position i.

  In this second version, to reorder the strings will be necessary to
  swap strings or sufficient to swap pointers to strings?

Example
-------

The following is an example of a correct input file:
`
10  <br />
this  <br />
is    <br />
an     <br />
example   <br />
of   <br />
file   <br />
used  <br />
to <br />
order <br /> <br /> <br /> <br /> <br />
strings <br /> <br /> <br /> <br />
`
and the following is the corresponding output file:
`
10 <br /> 
an <br /> 
example <br />
file <br />
is <br />
of <br />
order <br />
strings <br />
this <br />
to <br />
used <br />
`

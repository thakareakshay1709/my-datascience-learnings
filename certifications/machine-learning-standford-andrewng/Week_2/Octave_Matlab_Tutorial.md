##Octave and Matlab Tutorial:

1. Suppose I first execute the following in Octave/Matlab:
	A = [1 2; 3 4; 5 6];
	B = [1 2 3; 4 5 6];

Options

A. C = A' + B; (Correct)
B. C = B * A; (Correct)
C. C = A + B; (Incorrect)
D. C = B' * A; (Incorrect)

2. Let A = 
[16 2 3 13
5 11 10 8
9 7 6 12
4 14 15 1]

Which of the following indexing expressions give 
B = 
[6 2
5 11
9 7
4 14]
Options

A. B = A(:, 1:2); (Correct)
B. B = A(1:4, 1:2)(Correct);
C. B = A(0:2, 0:4)(Incorrect)
D. B = A(1:2, 1:4);(Incorrect)

3. Let A be a 10x10 matrix and xx be a 10-element vector. Your friend wants to compute the product AxAx and writes the following code:
	v = zeros(10, 1);
	for i = 1:10
		for j = 1:10
			v(i) = v(i) + A(i, j) * x(j);
		end
	end
	
	How would you vectorize this code to run without any FOR loops? Check all that apply.
	
Options

A. v = A * x;   	(Correct)
B. v = Ax; 			(Incorrect)
C. v = A .* x;  	(Incorrect)
D. v = sum (A * x); (Incorrect)

4. Say you have two column vectors vv and ww, each with 7 elements (i.e., they have dimensions 7x1). Consider the following  code:

z = 0;
for i = 1:7
  z = z + v(i) * w(i)
end

Which of the following vectorizations correctly compute z? Check all that apply.

Options
A. z = sum (v .* w); (Correct)
B. z = w' * v; (Correct)
C. z = v * w; (Incorrect)
D. z = w * v; (Incorrect)


5. In Octave/Matlab, many functions work on single numbers, vectors, and matrices. For example, the sin function when applied to a matrix will return a new matrix with the sin of each element. But you have to be careful, as certain functions have different behavior. Suppose you have an 7x7 matrix XX. You want to compute the log of every element, the square of every element, add 1 to every element, and divide every element by 4. You will store the results in four matrices, A, B, C, DA,B,C,D. One way to do so is the following code:
for i = 1:7
  for j = 1:7
    A(i, j) = log(X(i, j));
    B(i, j) = X(i, j) ^ 2;
    C(i, j) = X(i, j) + 1;
    D(i, j) = X(i, j) / 4;
  end
end

Which of the following correctly compute A, B, C,A,B,C, or DD? Check all that apply. 

Options
A. C = X + 1; (Correct)
B. D = X / 4; (Correct)
C. B = X .^ 2; (Correct)
D. B = X ^ 2; (Incorrect)
Download Link: https://assignmentchef.com/product/solved-midterm-advanced-machine-learning-data442-642
<br>
<strong>Exercise 1 </strong>(10 points)

Show that the <em>`</em><sub>1 </sub>norm is a convex function (as all norms), yet it is not strictly convex. In contrast, show that the squared Euclidean norm is a strictly convex function.

<strong>Exercise 2 </strong>(10 points)

Let the observations resulting from an experiment be <em>x<sub>n</sub></em>, <em>n </em>= 1<em>,</em>2<em>,…,N</em>. Assume that they are independent and that they originate from a Gaussian PDF with mean <em>µ </em>and standard deviation <em>σ</em><sup>2</sup>. Both, the mean and the variance, are unknown. Prove that the maximum likelihood (ML) estimates of these quantities are given by

<strong>Exercise 3 </strong>(15 points)

For the regression model where the noise vector <em>η </em>= [<em>η</em><sub>1</sub><em>,…,η<sub>N</sub></em>]<sup>&gt; </sup>comprises samples from zero mean Gaussian random variable, with covariance matrix <strong>Σ</strong><em><sub>n</sub></em>, show that the Fisher information matrix is given by

<em>,</em>

where <strong>X </strong>is the input matrix.

<strong>Exercise 4 </strong>(20 points) Consider the regression problem described in one of our labs. Read the same audio file, then add white Gaussian noise at a 15 dB level and randomly “hit” 10% of the data samples with outliers (set the outlier values to 80% of the maximum value of the data samples).

<ul>

 <li>Find the reconstructed data samples obtained by the support vector regression. Employthe Gaussian kernel with <em>σ </em>= 0<em>.</em>004 and set 003 and <em>C </em>= 1. Plot the fitted curve of the reconstructed samples together with the data used for training.</li>

 <li>Repeat step (a) using <em>C </em>= 0<em>.</em>05<em>,</em>0<em>.</em>1<em>,</em>0<em>.</em>5<em>,</em>5<em>,</em>10<em>,</em></li>

 <li>Repeat step (a) using<em>.</em></li>

 <li>Repeat step (a) using <em>σ </em>= 0<em>.</em>001<em>,</em>0<em>.</em>002<em>,</em>0<em>.</em>01<em>,</em>0<em>.</em>05<em>,</em>0<em>.</em>1<em>.</em></li>

 <li>Comment on the results.</li>

</ul>

<strong>Exercise 5 </strong>(15 points)

Show, using Lagrange multipliers, that the <em>`</em><sub>2 </sub>minimizer in equation (9.18) from the textbook accepts the closed form solution

<em>θ</em>ˆ = <strong>X</strong>&gt;(<strong>XX</strong>&gt;)−1<em>y</em>

Now, show that for the system <em>y </em>= <strong>X</strong><em>θ </em>with <strong>X </strong>∈ R<em><sup>n</sup></em><sup>×<em>l </em></sup>and <em>n &gt; l </em>the least squares solution is given by

<em>θ</em>ˆ = (<strong>X</strong>&gt;<strong>X</strong>)−1<strong>X</strong>&gt;<em>y</em>

<strong>Exercise 6 </strong>(10 points)

Show that the null space of a full rank <em>N </em>×<em>l </em>matrix <strong>X </strong>is a subspace of imensionality <em>l </em>−<em>N</em>, for <em>N &lt; l</em>.

<strong>Exercise 7 </strong>(20 points)

Generate in Python a sparse vector <em>θ </em>∈ R<em><sup>l</sup>, l </em>= 100, with its first five components taking random values drawn from a normal distribution with mean zero and variance one and the rest being equal to zero. Build, also, a sensing matrix <strong>X </strong>with <em>N </em>= 30 rows having samples normally distributed, with mean zero and variance 1<em>/N</em>, in order to get 30 observations based on the linear regression model <em>y </em>= <strong>X</strong><em>θ</em>. Then perform the following tasks.

<ul>

 <li>Use a LASSO implementation to reconstruct <em>θ </em>from <em>y </em>and <strong>X</strong>.</li>

 <li>Repeat the experiment 500 times, with different realizations of <strong>X</strong>, in order to compute the probability of correct reconstruction (assume the reconstruction is exact when ||<em>y </em>= <strong>X</strong><em>θ</em>|| <em>&lt; </em>10<sup>−8</sup>).</li>

 <li>Repeat the same experiment (500 times) with matrices of the form</li>

</ul>

<em>,      </em>with probability



<strong>X</strong>(<em>i,j</em>) =        0<em>,                 </em>with probability 1

<em>,      </em>with probability

for <em>p </em>equal to 1<em>,</em>9<em>,</em>25<em>,</em>36<em>,</em>64 (make sure that each row and each column of <strong>X </strong>has at least a nonzero component). Give an explanation why the probability of reconstruction falls as <em>p </em>increases (observe that both the sensing matrix and the unknown vector are sparse).
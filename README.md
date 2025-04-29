# syde556---solved
**TO GET THIS SOLUTION VISIT:** [SYDE556 – Solved](https://www.ankitcodinghub.com/product/syde556-solved-4/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;110691&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;SYDE556 -  Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
SYDE 556/750

Simulating Neurobiological Systems

Assignment 1

Important Notes – Please Read Carefully

• Please use Python 3 along with the numpy and matplotlib libraries to solve these assignments.

In particular, fill out this Jupyter Notebook template:

https://github.com/astoeckel/syde556-w20/blob/master/assignments/assignment_01/ syde556_assignment_01_template.ipynb

• Clearly label any plot you produce, including the axes. Provide a legend if there are multiple graphs in the same plot.

• You won’t be judged on the quality of your code, but writing reusable functions will greatly simplify this and future assignments.

• Do not use or refer to any code from Nengo!

1 Representation of Scalars

1.1 Basic encoding and decoding

Implement a neural representation of a scalar value x. For the neuron model, use a rectified linear neuron model, i.e., a = G[J] = max(J,0). Choose the maximum firing amax rates randomly (uniformly distributed between 100Hz and 200Hz at x = 1), and choose the x-intercepts ξ randomly (uniformly distributed between −0.95 and 0.95). Use those values to compute the corresponding α and Jbias parameters for each neuron.

The encoders e are randomly chosen and are either +1 or −1 for each neuron. Go through these steps:

[0.5] a) Computing gain and bias. In general, for a neuron model a = G[J] (and assuming that the inverse J = G−1[a] exists), solve the following system of equations to compute the gain α, and the bias Jbias given a maximum rate amax and an x-intercept ξ.

amax = G[α + Jbias], 0 = G[αξ + Jbias].

Now, simplify these equations for the specific case G[J] = max(J,0).

🖈 The x-intercept ξ is the value of ⟨x,ei⟩ for which the neuron just starts to have a non-zero firing rate. Mathematically, we must inject a current of magnitude Jth into the neuron at the x-intercept, where Jth is defined as

.

This threshold current Jth is the maximum current that results in a zero output rate – currents above the threshold will result in output spikes. In your equations, you can use Jth in place of G−1[0], which is not well-defined for most neuron models.

[0.5] b) Neuron tuning curves. Plot the neuron tuning curves ai(x) for 16 randomly generated neurons following the intercept and maximum rate distributions described above.

📖 See Figure 2.4 in the book for an example, but with a different neuron model and a different range of maximum firing rates.

🖈 Since you can’t compute this for every possible x value between −1 and 1, monotonously sample the x-axis with ∆x = 0.05, i.e. there should be 41 monotonously increasing x values. Use this sampling throughout this question.

[1] c) Computing identity decoders. Compute the optimal identity decoder d for those 16 neurons (as shown in class). Report the value of the individual decoder coefficients. Compute d using the matrix notation mentioned in the course notes. Do not apply any regularization. A is the matrix of activities (the same data used to generate the plot in 1.1b).

(e.g. by calling np.random.seed) to reliably generate tuning curves that do not have this problem.

[1] d) Evaluating decoding errors. Compute and plot xˆ = Pi diai(x). Overlay on the plot the line y = x. Make a separate plot of x − xˆ to see what the error looks like. Report the Root Mean Squared Error (RMSE) value.

📖 See Figure 2.7 for an example.

[1] e) Decoding under noise. Now try decoding under noise. Add random normally distributed noise to A and decode again. The noise is a random variable with mean µ = 0 and standard deviation of σ = 0.2max(A) (where max(A) is the maximum firing rate of all the neurons). Resample this variable for every different x value for every different neuron. Create all the same plots as in part d). Report the RMSE.

[1] f) Accounting for decoder noise. Recompute the decoder d taking noise into account (i.e., apply the appropriate regularization, as shown in class). Show how these decoders behave when decoding both with and without noise added to a by making the same plots as in d) and e). Report the RMSE for all cases.

🖈 As in the previous question, σ = 0.2max(A).

🖈 For this, and all other questions, do not add noise to the A you use for computing the decoders D. Instead, appropriately account for noise through regularization when computing the decoders, as we discussed in class. Use the noisy version of A to test what impact noise has on the quality of the decoded values.

[1] g) Interpretation. Show a 2×2 table of the four RMSE values reported in parts d), e), and f). This should show the effects of adding noise and whether the decoders d are computed taking noise into account. Write a few sentences commenting on what the table shows, i.e., what the effect of adding noise to the activities is with respect to the measured error and why accounting for noise when computing the decoders increases/decreases/does not change the measured RMSE.

1.2 Exploring sources of error

Use the program you wrote in 1.1 to examine the sources of error in the representation.

🖈 Again, do not add noise to A when computing the decoders (see note above).

📖 See Equation 2.9 and Figure 2.6 in the book.

[1] b) Adapting the noise level. Repeat part a) with σ = 0.01max(A).

[1] c) Interpretation. What does the difference between the graphs in a) and b) tell us about the sources of error in neural populations?

1.3 Leaky Integrate-and-Fire neurons

Change the code to use the rate approximation of the LIF neuron model

.

[0.5] a) Computing gain and bias. As in the second part of 1.1a), given a maximum firing rate amax and an x-intercept ξ, write down the equations for computing α and Jbias for this specific neuron model.

[0.5] b) Neuron tuning curves. Generate the same plot as in 1.1b). Use τref = 2ms and τRC = 20ms. Use the same distribution of x-intercepts and maximum firing rates as in 1.1, i.e., choose the maximum firing rates amax as uniformly distributed between 100Hz and 200Hz at x = 1, choose the x-intercepts ξ as uniformly distributed between −0.95 and 0.95, and choose the encoders e as either −1 or +1.

[1.5] c) Impact of noise. Generate the same four plots as in 1.1f) (adding/not adding noise to A, accounting/not accounting for noise when computing d), and report the RMSE both with and without noise.

2 Representation of Vectors

2.1 Vector tuning curves

[1] a) Plotting 2D tuning curves. Plot the tuning curve of an LIF neuron whose 2D preferred direction vector

is at an angle of θ = −π/4, has an x-intercept at the origin (0,0), and has a maximum firing rate of 100Hz.

🖈 Use the parameters τref = 2ms and τRC = 20ms from the previous question.

🖈 Remember that J = α⟨e,x⟩ + Jbias, and both x and e are 2D vectors.

🖈 In general, the maximum firing rate of a neuron is defined to occur when the input is of unit length along its preferred direction, i.e., ⟨e,x⟩ = 1, which, for unit-length e is equivalent to e = x. Of course, if we increase the magnitude of the input vector beyond unit length, neurons would start firing faster than their maximum firing rate. Similarly, here the “maximum firing rate” means the firing rate when x = e. This should allow you to reuse your equations from 1.3a) to compute α and Jbias for a desired maximum firing rate and x-intercept.

🐍 To generate 3D plots in Python, see here.

📖 This is a 3D plot similar to Figure 2.8a in the book.

[1] b) Plotting the 2D tuning curve along the unit circle. Plot the tuning curve for the same neuron as in a),

but only considering the points around the unit circle, i.e., sample the activation for different angles θ.

Fit a curve of the form c1 cos(c2θ + c3) + c4 to the tuning curve and plot it as well.

📖 This will be similar to Figure 2.8b in the book.

🐍 To do curve fitting in Python, see here.

[0.5] c) Discussion. What makes a cosine a good choice for the curve fit in 2.1b? Why does it differ from the ideal curve?

2.2 Vector representation

[1] a) Choosing encoding vectors. Generate a set of 100 random unit vectors uniformly distributed around the unit circle. These will be the encoders e for 100 neurons. Plot these vectors with a quiver or line plot (i.e., not just points, but lines/arrows to the points).

[0.5] b) Computing the identity decoder. Use LIF neurons with the same properties as in question 1.3. When

computing the decoders, take into account noise with σ = 0.2max(A). Plot the decoders in the same way you plotted the encoders.

🖈 The decoder will be a matrix D ∈ R2×100. Each column in D corresponds to a 2D vector.

🖈 In the scalar case, to sample the input space, you used x values between −1 and 1, with ∆x = 0.05. In this case, you can regularly tile the 2D x values ([1,1],[1,0.95],…[−1,−0.95],[−1,1]).

Alternatively, you can just randomly choose 1600 different x values to sample.

[0.5] c) Discussion. How do these decoding vectors compare to the encoding vectors?

[1] d) Testing the decoder. Generate 20 random x values throughout the unit circle (i.e., with different directions and radiuses). For each x value, determine the neural activity ai for each of the 100 neurons. Now decode these values (i.e., compute xˆ = Da) using the decoders from part b). Plot the original and decoded values on the same graph in different colours, and compute the RMSE.

🖈 Technically, the RMSE is not well-defined for non-scalar data. The usual convention is to “flatten” the series, i.e., treat the extra dimensions as scalar datapoints. For N d-dimensional datapoints

RMSE .

🐍 Per default, the np.mean function computes the mean on a “flattened” array.

[1] e) Using encoders as decoders. Repeat part d) but use the encoders as decoders. This is what Georgopoulos used in his original approach to decoding information from populations of neurons. Plot the decoded values and compute the RMSE. In addition, recompute the RMSE in both cases, but ignore the magnitude of the decoded vectors by normalizing before computing the RMSE.

🖈 To rephrase the above, we are only interested in the angular error, not the error in the magnitude of the decoded vectors. To compute the angular error, you have to normalize both the decoded vectors and the target vectors you are comparing to.

[1] f) Discussion. When computing the RMSE on the normalized vectors, using the encoders as decoders should result in a larger, yet still surprisingly small error. Thinking about random unit vectors in high dimensional spaces, why is this the case? What are the relative merits of these two approaches to decoding?

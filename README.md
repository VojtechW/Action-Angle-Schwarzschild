# Action-Angle-Schwarzschild
Mathematica notebooks and .m files accompanying the paper on Action-angle coordinates for bound geodesics in Schwarzschild space-time.

***If you use these notebooks in any way, please cite the accompanying paper:*** 
Witzany, V. (2022). Action-angle coordinates for black-hole geodesics I: Spherically symmetric and Schwarzschild. arXiv:2203.11952
(Submitted to MNRAS, please check later for details on publication in print)

## Description of files

There are a couple of files here:

 - **AA_Spherical.nb** Mathematica notebook that derives all the coefficients needed for the transformation to and from action-angle variables for geodesics in any static, spherically symmetric space-time. Feel free to increase the order and let it run longer if you need higher order coefficients than in the paper.
 - **AA_SchwDarw.** Mathematica notebook that uses the Darwin parametrization of geodesics in Schwarzschild space-time to derive transformations to and from action-angle variables. It also contains a section generating all the plots used in the paper. (Again, feel free to run longer if you need higher order.)
 - **AA_Spher_Storage12.m** Mathematica storage file that contains coefficients needed for transformations to and from action-angle coordinates in general static, spherically symmetric space-time to 6th order in radial action (12th order in eccentricity).
 - **AA_SchwRcEJ20.m** Mathematica storage file that contains coefficients needed for transformations between orbital elements *p,e* and actions to tenth order in the radial action (twentieth order in eccentricity). It also contains coefficients of the expansion of the Hamiltonian wrt the radial action to tenth order.
 - **AA_SchwRcFull8.m** Mathematica storage file that contains the previous information to 4th order in radial actions, but also coefficients needed for transformations to and from angle variables to 4th order in the radial action (8th order in eccentricity).
 - **Pad5Store.m** Mathematica storage file with the coefficients of the Padé approximant for the action Hamiltonian. (Yields sub-percent level errors for the Hamiltonian everywhere in parameter space.)

## Usage

You can open and run any notebook in Mathematica as per usual. The "Spherical" notebook is written with the use of Mathematica Parallelization constructs such as ParallelTable. The "SchwDarw" notebook was written on a machine with Apple Silicone that had issues with Mathematica Parallelization (adjust as needed). If you run the entire notebooks, they will take a long time to finish, read them first and run what you need, or at least adjust the "Ord" parameter to a lower value so that they finish faster.

The Storage files can be loaded using the Get[] Mathematica function. Do note that you may need to use some of the Symbolize[] commands from the Notation package found in the notebooks above, since I like to use symbols involving subscripts and superscripts.

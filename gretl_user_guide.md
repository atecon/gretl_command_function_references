# Gretl User’s Guide

## Gnu Regression, Econometrics and Time-series Library

### Allin Cottrell

### Department of Economics

### Wake Forest University

### Riccardo “Jack” Lucchetti

### Dipartimento di Economia

### Università Politecnica delle Marche

### April, 2025


Permission is granted to copy, distribute and/or modify this document under the terms of the
_GNU Free Documentation License_ , Version 1.1 or any later version published by the Free Software
Foundation (see [http://www.gnu.org/licenses/fdl.html).](http://www.gnu.org/licenses/fdl.html).)


## Contents










- 1 Introduction
   - 1.1 Features at a glance
   - 1.2 Acknowledgements
   - 1.3 Installing the programs
- I Running the program
- 2 Getting started
   - 2.1 Let’s run a regression
   - 2.2 Estimation output
   - 2.3 The main window menus
   - 2.4 Keyboard shortcuts
   - 2.5 The gretl toolbar
- 3 Modes of working
   - 3.1 Command scripts
   - 3.2 Saving script objects
   - 3.3 The gretl console
   - 3.4 The Session concept
- 4 Data files
   - 4.1 Data file formats
   - 4.2 Databases
   - 4.3 Creating a dataset from scratch
   - 4.4 Structuring a dataset
   - 4.5 Panel data specifics
   - 4.6 Missing data values
   - 4.7 Maximum size of data sets
   - 4.8 Data file collections
   - 4.9 Assembling data from multiple sources
- 5 Sub-sampling a dataset
   - 5.1 Introduction
   - 5.2 Setting the sample
   - 5.3 Restricting the sample
   - 5.4 Panel data Contents ii
   - 5.5 Resampling and bootstrapping
- 6 Graphics
   - 6.1 Gnuplot graphs
   - 6.2 Plotting graphs from scripts
   - 6.3 Boxplots
- 7 Joining data sources
   - 7.1 Introduction
   - 7.2 Basic syntax
   - 7.3 Filtering
   - 7.4 Matching with keys
   - 7.5 Aggregation
   - 7.6 String-valued key variables
   - 7.7 Importing multiple series
   - 7.8 A real-world case
   - 7.9 The representation of dates
   - 7.10 Time-series data
   - 7.11 Special handling of time columns
   - 7.12 Panel data
   - 7.13 Memo: join options
- 8 Realtime data
   - 8.1 Introduction
   - 8.2 Atomic format for realtime data
   - 8.3 More on time-related options
   - 8.4 Getting a certain data vintage
   - 8.5 Getting the n -th release for each observation period
   - 8.6 Getting the values at a fixed lag after the observation period
   - 8.7 Getting the revision history for an observation
- 9 Temporal disaggregation
   - 9.1 Introduction
   - 9.2 Notation and design
   - 9.3 Overview of data handling
   - 9.4 Extrapolation
   - 9.5 Function signature
   - 9.6 Handling of deterministic terms
   - 9.7 Some technical details
   - 9.8 The plot option
   - 9.9 Multiple low-frequency series Contents iii
   - 9.10 Examples
- 10 Special functions in genr
   - 10.1 Introduction
   - 10.2 Cumulative densities and p-values
   - 10.3 Retrieving internal variables (dollar accessors)
- 11 Gretl data types
   - 11.1 Introduction
   - 11.2 Series
   - 11.3 Scalars
   - 11.4 Matrices
   - 11.5 Lists
   - 11.6 Strings
   - 11.7 Bundles
   - 11.8 Arrays
   - 11.9 The life cycle of gretl objects
- 12 Discrete variables
   - 12.1 Declaring variables as discrete
   - 12.2 Commands for discrete variables
- 13 Loop constructs
   - 13.1 Introduction
   - 13.2 Loop control variants
   - 13.3 Special controls
   - 13.4 Progressive mode
   - 13.5 Loop examples
- 14 User-defined functions
   - 14.1 Defining a function
   - 14.2 Calling a function
   - 14.3 Deleting a function
   - 14.4 Function programming details
   - 14.5 Function packages
- 15 Named lists and strings
   - 15.1 Named lists
   - 15.2 Named strings
- 16 String-valued series
   - 16.1 Introduction Contents iv
   - 16.2 Creating a string-valued series
   - 16.3 Permitted operations
   - 16.4 String-valued series and functions
   - 16.5 Other import formats
- 17 Matrix manipulation
   - 17.1 Creating matrices
   - 17.2 Empty matrices
   - 17.3 Selecting submatrices
   - 17.4 Deleting rows or columns
   - 17.5 Matrix operators
   - 17.6 Matrix–scalar operators
   - 17.7 Matrix functions
   - 17.8 Matrix accessors
   - 17.9 Namespace issues
   - 17.10 Creating a data series from a matrix
   - 17.11 Matrices and lists
   - 17.12 Deleting a matrix
   - 17.13 Printing a matrix
   - 17.14 Example: OLS using matrices
- 18 Complex matrices
   - 18.1 Introduction
   - 18.2 Creating a complex matrix
   - 18.3 Indexation
   - 18.4 Operators
   - 18.5 Functions
   - 18.6 File input/output
   - 18.7 Backward (in)compatibility
- 19 Calendar dates
   - 19.1 Introduction
   - 19.2 Date and time representations
   - 19.3 Converting between representations
   - 19.4 Epoch day arithmetic
   - 19.5 Other accessors and functions
   - 19.6 Working with pre-Gregorian dates
- 20 Mixed-frequency data
   - 20.1 Basics
   - 20.2 The notion of a “MIDAS list” Contents v
   - 20.3 High-frequency lag lists
   - 20.4 High-frequency first differences
   - 20.5 MIDAS-related plots
   - 20.6 Alternative MIDAS data methods
- 21 Cheat sheet
   - 21.1 Dataset handling
   - 21.2 Creating/modifying variables
   - 21.3 Neat tricks
- II Econometric methods
- 22 Robust covariance matrix estimation
   - 22.1 Introduction
   - 22.2 Cross-sectional data and the HCCME
   - 22.3 Time series data and HAC covariance matrices
   - 22.4 Special issues with panel data
   - 22.5 The cluster-robust estimator
- 23 Panel data
   - 23.1 Estimation of panel models
   - 23.2 Autoregressive panel models
- 24 Dynamic panel models
   - 24.1 Introduction
   - 24.2 Usage
   - 24.3 Replication of DPD results
   - 24.4 Cross-country growth example
   - 24.5 Auxiliary test statistics
   - 24.6 Post-estimation available statistics
   - 24.7 Memo: dpanel options
- 25 Nonlinear least squares
   - 25.1 Introduction and examples
   - 25.2 Initializing the parameters
   - 25.3 NLS dialog window
   - 25.4 Analytical and numerical derivatives
   - 25.5 Advanced use
   - 25.6 Controlling termination
   - 25.7 Details on the code
   - 25.8 Numerical accuracy Contents vi
- 26 Maximum likelihood estimation
   - 26.1 Generic ML estimation with gretl
   - 26.2 Syntax
   - 26.3 Covariance matrix and standard errors
   - 26.4 Gamma estimation
   - 26.5 Stochastic frontier cost function
   - 26.6 GARCH models
   - 26.7 Analytical derivatives
   - 26.8 Debugging ML scripts
   - 26.9 Using functions
   - 26.10 Advanced use of mle: functions, analytical derivatives, algorithm choice
   - 26.11 Estimating constrained models
   - 26.12 Handling non-convergence gracefully
- 27 GMM estimation
   - 27.1 Introduction and terminology
   - 27.2 GMM as Method of Moments
   - 27.3 OLS as GMM
   - 27.4 TSLS as GMM
   - 27.5 Covariance matrix options
   - 27.6 A real example: the Consumption Based Asset Pricing Model
   - 27.7 Caveats
- 28 Model selection criteria
   - 28.1 Introduction
   - 28.2 Information criteria
- 29 Degrees of freedom correction
   - 29.1 Introduction
   - 29.2 Back to basics
   - 29.3 Application to OLS regression
   - 29.4 Beyond OLS
   - 29.5 Consistency and awkward cases
   - 29.6 What gretl does
- 30 Time series filters
   - 30.1 Fractional differencing
   - 30.2 The Hodrick–Prescott filter
   - 30.3 The Baxter and King filter
   - 30.4 The Butterworth filter Contents vii
   - 30.5 The discrete Fourier transform
- 31 Univariate time series models
   - 31.1 Introduction
   - 31.2 ARIMA models
   - 31.3 Unit root tests
   - 31.4 Cointegration test
   - 31.5 ARCH and GARCH
- 32 Vector Autoregressions
   - 32.1 Notation
   - 32.2 Estimation
   - 32.3 Structural VARs
   - 32.4 Residual-based diagnostic tests
- 33 Cointegration and Vector Error Correction Models
   - 33.1 Introduction
   - 33.2 Vector Error Correction Models as representation of a cointegrated system
   - 33.3 Interpretation of the deterministic components
   - 33.4 The Johansen cointegration tests
   - 33.5 Identification of the cointegration vectors
   - 33.6 Over-identifying restrictions
   - 33.7 Numerical solution methods
- 34 Multivariate models
   - 34.1 The system command
   - 34.2 Equation systems within functions
   - 34.3 Restriction and estimation
   - 34.4 System accessors
- 35 Forecasting
   - 35.1 Introduction
   - 35.2 Saving and inspecting fitted values
   - 35.3 The fcast command
   - 35.4 Univariate forecast evaluation statistics
   - 35.5 Forecasts based on VAR models
   - 35.6 Forecasting from simultaneous systems
- 36 State Space Modeling
   - 36.1 Introduction
   - 36.2 Notation Contents viii
   - 36.3 Defining the model as a bundle
   - 36.4 Special features of state-space bundles
   - 36.5 The kfilter function
   - 36.6 The ksmooth function
   - 36.7 The kdsmooth function
   - 36.8 Diffuse initialization of the state vector
   - 36.9 Extensions and refinements
   - 36.10 The ksimul function
   - 36.11 Numerical optimization
   - 36.12 Example scripts
   - 36.13 Graphical interface
- 37 Numerical methods
   - 37.1 Derivative-based optimization methods
   - 37.2 Derivative-free optimization methods
   - 37.3 Numerical differentiation
   - 37.4 Numerical integration
- 38 Discrete and censored dependent variables
   - 38.1 Logit and probit models
   - 38.2 Ordered response models
   - 38.3 Multinomial logit
   - 38.4 Bivariate probit
   - 38.5 Panel estimators
   - 38.6 The Tobit model
   - 38.7 Interval regression
   - 38.8 Sample selection model
   - 38.9 Count data
   - 38.10 Duration models
- 39 Quantile regression
   - 39.1 Introduction
   - 39.2 Basic syntax
   - 39.3 Confidence intervals
   - 39.4 Multiple quantiles
   - 39.5 Large datasets
- 40 Nonparametric methods
   - 40.1 Locally weighted regression (loess)
   - 40.2 The Nadaraya–Watson estimator
- 41 MIDAS models Contents ix
   - 41.1 Parsimonious parameterizations
   - 41.2 Estimating MIDAS models
   - 41.3 Parameterization functions
- III Technical details
- 42 Gretl and ODBC
   - 42.1 ODBC support
   - 42.2 ODBC base concepts
   - 42.3 Syntax
   - 42.4 Examples
   - 42.5 Connectivity details
- 43 Gretl and TEX
   - 43.1 Introduction
   - 43.2 TEX-related menu items
   - 43.3 Fine-tuning typeset output
   - 43.4 Installing and learning TEX
- 44 Gretl and R
   - 44.1 Introduction
   - 44.2 Starting an interactive R session
   - 44.3 Running an R script
   - 44.4 Sending data back and forth
   - 44.5 Interacting with R from the command line
   - 44.6 Performance issues with R
   - 44.7 Further use of the R library
- 45 Gretl and Ox
   - 45.1 Introduction
   - 45.2 Ox support in gretl
   - 45.3 Illustration: replication of DPD model
- 46 Gretl and Octave
   - 46.1 Introduction
   - 46.2 Octave support in gretl
   - 46.3 Illustration: spectral methods
- 47 Gretl and Stata
- 48 Gretl and Python
   - 48.1 Introduction Contents x
   - 48.2 Python support in gretl
   - 48.3 Illustration: linear regression with multicollinearity
- 49 Gretl and Julia
   - 49.1 Introduction
   - 49.2 Julia support in gretl
   - 49.3 Illustration
- 50 Troubleshooting gretl
   - 50.1 Bug reports
   - 50.2 Auxiliary programs
- 51 The command line interface
- IV Appendices
- A Data file details
   - A.1 Basic native format
   - A.2 Binary data file format
   - A.3 Native database format
- B Building gretl
   - B.1 Installing the prerequisites
   - B.2 Getting the source: release or git
   - B.3 Configure the source
   - B.4 Build and install
- C Numerical accuracy
- D Related free software
- E Listing of URLs
- Bibliography


## Chapter 1

Introduction

### 1.1 Features at a glance

Gretl is an econometrics package, including a shared library, a command-line client program and a
graphical user interface.

User-friendly Gretl offers an intuitive user interface; it is very easy to get up and running with
econometric analysis. Thanks to its association with the econometrics textbooks by Ramu
Ramanathan, Jeffrey Wooldridge, and James Stock and Mark Watson, the package offers many
practice data files and command scripts. These are well annotated and accessible. Two other
useful resources for gretl users are the available documentation and the gretl-users mailing
list.

Flexible You can choose your preferred point on the spectrum from interactive point-and-click to
complex scripting, and can easily combine these approaches.

Cross-platform Gretl’s “home” platform is Linux but it is also available for MS Windows and Mac
OS X, and should work on any unix-like system that has the appropriate basic libraries (see
Appendix B).

Open source The full source code for gretl is available to anyone who wants to critique it, patch it,
or extend it. See Appendix B.

Sophisticated Gretl offers a full range of least-squares based estimators, either for single equations
and for systems, including vector autoregressions and vector error correction models. Sev-
eral specific maximum likelihood estimators (e.g. probit, ARIMA, GARCH) are also provided
natively; more advanced estimation methods can be implemented by the user via generic
maximum likelihood or nonlinear GMM.

Extensible Users can enhance gretl by writing their own functions and procedures in gretl’s script-
ing language, which includes a wide range of matrix functions.

Accurate Gretl has been thoroughly tested on several benchmarks, among which the NIST refer-
ence datasets. See Appendix C.

Internet ready Gretl can fetch materials such databases, collections of textbook datafiles and add-
on packages over the internet.

International Gretl will produce its output in English, French, Italian, Spanish, Polish, Portuguese,
German, Basque, Turkish, Russian, Albanian or Greek depending on your computer’s native
language setting.

### 1.2 Acknowledgements

The gretl code base originally derived from the program ESL (“Econometrics Software Library”),
written by Professor Ramu Ramanathan of the University of California, San Diego. We are much in
debt to Professor Ramanathan for making this code available under the GNU General Public Licence
and for helping to steer gretl’s early development.

#### 1


Chapter 1. Introduction 2

We are also grateful to the authors of several econometrics textbooks for permission to package for
gretl various datasets associated with their texts. This list currently includes William Greene, au-
thor of _Econometric Analysis_ ; Jeffrey Wooldridge ( _Introductory Econometrics: A Modern Approach_ );
James Stock and Mark Watson ( _Introduction to Econometrics_ ); Damodar Gujarati ( _Basic Economet-
rics_ ); Russell Davidson and James MacKinnon ( _Econometric Theory and Methods_ ); and Marno Ver-
beek ( _A Guide to Modern Econometrics_ ).

GARCH estimation in gretl is based on code deposited in the archive of the _Journal of Applied
Econometrics_ by Professors Fiorentini, Calzolari and Panattoni, and the code to generate _p_ -values
for Dickey–Fuller tests is due to James MacKinnon. In each case we are grateful to the authors for
permission to use their work.

With regard to the internationalization of gretl, thanks go to Ignacio Díaz-Emparanza (Spanish),
Michel Robitaille and Florent Bresson (French), Cristian Rigamonti (Italian), Tadeusz Kufel and Pawel
Kufel (Polish), Markus Hahn and Sven Schreiber (German), Hélio Guilherme and Henrique Andrade
(Portuguese), Susan Orbe (Basque), Talha Yalta (Turkish) and Alexander Gedranovich (Russian).

Gretl has benefitted greatly from the work of numerous developers of free, open-source software:
for specifics please see Appendix B. Our thanks are due to Richard Stallman of the Free Software
Foundation, for his support of free software in general and for agreeing to “adopt” gretl as a GNU
program in particular.

Many users of gretl have submitted useful suggestions and bug reports. In this connection par-
ticular thanks are due to Ignacio Díaz-Emparanza, Tadeusz Kufel, Pawel Kufel, Alan Isaac, Cri
Rigamonti, Sven Schreiber, Talha Yalta, Andreas Rosenblad, and Dirk Eddelbuettel, who maintains
the gretl package for Debian GNU/Linux.

### 1.3 Installing the programs

Linux

On the Linux^1 platform you have the choice of compiling the gretl code yourself or making use of a
pre-built package. Building gretl from the source is necessary if you want to access the development
version or customize gretl to your needs, but this takes quite a few skills; most users will want to
go for a pre-built package.

Some Linux distributions feature gretl as part of their standard offering: Debian, Ubuntu and Fe-
dora, for example. If this is the case, all you need to do is install gretl through your package
manager of choice. In addition the gretl webpage at [http://gretl.sourceforge.net](http://gretl.sourceforge.net) offers a
“generic” package in rpm format for modern Linux systems.

If you prefer to compile your own (or are using a unix system for which pre-built packages are not
available), instructions on building gretl can be found in Appendix B.

MS Windows

The MS Windows version comes as a self-extracting executable. Installation is just a matter of
downloading gretl_install.exe and running this program. You will be prompted for a location
to install the package.

Mac OS X

The Mac version comes as a gzipped disk image. Installation is a matter of downloading the image
file, opening it in the Finder, and dragging Gretl.app to the Applications folder. However, when
installing for the first time two prerequisite packages must be put in place first; details are given
on the gretl website.

(^1) In this manual we use “Linux” as shorthand to refer to the GNU/Linux operating system. What is said herein about
Linux mostly applies to other unix-type systems too, though some local modifications may be needed.


## Part I

# Running the program

#### 3


## Chapter 2

Getting started

### 2.1 Let’s run a regression

This introduction is mostly angled towards the graphical client program; please see Chapter 51
below and the _Gretl Command Reference_ for details on the command-line program, gretlcli.

You can supply the name of a data file to open as an argument to gretl, but for the moment let’s
not do that: just fire up the program.^1 You should see a main window (which will hold information
on the data set but which is at first blank) and various menus, some of them disabled at first.

What can you do at this point? You can browse the supplied data files (or databases), open a data
file, create a new data file, read the help items, or open a command script. For now let’s browse the
supplied data files. Under the File menu choose “Open data, Sample file”. A second notebook-type
window will open, presenting the sets of data files supplied with the package (see Figure 2.1). Select
the first tab, “Ramanathan”. The numbering of the files in this section corresponds to the chapter
organization of Ramanathan (2002), which contains discussion of the analysis of these data. The
data will be useful for practice purposes even without the text.

```
Figure 2.1: Practice data files window
```
If you select a row in this window and click on “Info” this opens a window showing information on
the data set in question (for example, on the sources and definitions of the variables). If you find
a file that is of interest, you may open it by clicking on “Open”, or just double-clicking on the file
name. For the moment let’s open data3-6.

☞ In gretl windows containing lists, double-clicking on a line launches a default action for the associated list
entry: e.g. displaying the values of a data series, opening a file.

(^1) For convenience we refer to the graphical client program simply as gretl in this manual. Note, however, that the
specific name of the program differs according to the computer platform. On Linux it is called gretl_x11 while on
MS Windows it is gretl.exe. On Linux systems a wrapper script named gretl is also installed — see also the _Gretl
Command Reference_.

#### 4


Chapter 2. Getting started 5

This file contains data pertaining to a classic econometric “chestnut”, the consumption function.
The data window should now display the name of the current data file, the overall data range and
sample range, and the names of the variables along with brief descriptive tags — see Figure 2.2.

```
Figure 2.2: Main window, with a practice data file open
```
OK, what can we do now? Hopefully the various menu options should be fairly self explanatory. For
now we’ll dip into the Model menu; a brief tour of all the main window menus is given in Section 2.
below.

Gretl’s Model menu offers numerous various econometric estimation routines. The simplest and
most standard is Ordinary Least Squares (OLS). Selecting OLS pops up a dialog box calling for a
_model specification_ — see Figure 2.3.

```
Figure 2.3: Model specification dialog
```
To select the dependent variable, highlight the variable you want in the list on the left and click
the arrow that points to the Dependent variable slot. If you check the “Set as default” box this
variable will be pre-selected as dependent when you next open the model dialog box. Shortcut:
double-clicking on a variable on the left selects it as dependent and also sets it as the default. To
select independent variables, highlight them on the left and click the green arrow (or right-click the


Chapter 2. Getting started 6

highlighted variable); to remove variables from the selected list, use the rad arrow. To select several
variable in the list box, drag the mouse over them; to select several non-contiguous variables, hold
down the Ctrl key and click on the variables you want. To run a regression with consumption as
the dependent variable and income as independent, click Ct into the Dependent slot and add Yt to
the Independent variables list.

### 2.2 Estimation output

Once you’ve specified a model, a window displaying the regression output will appear. The output
is reasonably comprehensive and in a standard format (Figure 2.4).

```
Figure 2.4: Model output window
```
The output window contains menus that allow you to inspect or graph the residuals and fitted
values, and to run various diagnostic tests on the model.

For most models there is also an option to print the regression output in LATEX format. See Chap-
ter 43 for details.

To import gretl output into a word processor, you may copy and paste from an output window,
using its Edit menu (or Copy button, in some contexts) to the target program. Many (not all) gretl
windows offer the option of copying in RTF (Microsoft’s “Rich Text Format”) or as LATEX. If you are
pasting into a word processor, RTF may be a good option because the tabular formatting of the
output is preserved.^2 Alternatively, you can save the output to a (plain text) file then import the
file into the target program. When you finish a gretl session you are given the option of saving all
the output from the session to a single file.

Note that on the gnome desktop and under MS Windows, the File menu includes a command to
send the output directly to a printer.

☞ When pasting or importing plain text gretl output into a word processor, select a monospaced or typewriter-
style font (e.g. Courier) to preserve the output’s tabular formatting. Select a small font (10-point Courier
should do) to prevent the output lines from being broken in the wrong place.

(^2) Note that when you copy as RTF under MS Windows, Windows will only allow you to paste the material into ap-
plications that “understand” RTF. Thus you will be able to paste into MS Word, but not into notepad. Note also that
there appears to be a bug in some versions of Windows, whereby the paste will not work properly unless the “target”
application (e.g. MS Word) is already running prior to copying the material in question.


Chapter 2. Getting started 7

### 2.3 The main window menus

Reading left to right along the main window’s menu bar, we find the File, Tools, Data, View, Add,
Sample, Variable, Model and Help menus.

- File menu
    - Open data: Open a native gretl data file or import from other formats. See Chapter 4.
    - Append data: Add data to the current working data set, from a gretl data file, a comma-
       separated values file or a spreadsheet file.
    - Save data: Save the currently open native gretl data file.
    - Save data as: Write out the current data set in native format, with the option of using
       gzip data compression. See Chapter 4.
    - Export data: Write out the current data set in Comma Separated Values (CSV) format, or
       the formats of GNU R or GNU Octave. See Chapter 4 and also Appendix D.
    - Send to: Send the current data set as an e-mail attachment.
    - New data set: Allows you to create a blank data set, ready for typing in values or for
       importing series from a database. See below for more on databases.
    - Clear data set: Clear the current data set out of memory. Generally you don’t have to do
       this (since opening a new data file automatically clears the old one) but sometimes it’s
       useful.
    - Working directory: Change the current working directory (or “workdir”) and specify re-
       lated options. For an explanation of the role of the workdir click the Help button in the
       dialog window which is presented, or refer to the documentation of the set command
       with the workdir option in the command reference.
    - Script files: A “script” is a file containing a sequence of gretl commands. This item
       contains entries that let you open a script you have created previously (“User file”), open
       a sample script, or open an editor window in which you can create a new script.
    - Session files: A “session” file contains a snapshot of a previous gretl session, including
       the data set used and any models or graphs that you saved. Under this item you can
       open a saved session or save the current session.
    - Databases: Allows you to browse various large databases, either on your own computer
       or, if you are connected to the internet, on the gretl database server. See Section 4.2 for
       details.
    - Function packages: Manage user-contributed function packages that extend gretl’s capa-
       bilities. To learn more about such packages written in gretl’s built-in matrix and scripting
       language “hansl”, please refer to the “Packages” entry in Help menu.
    - Resource from addon: Access example scripts and datafiles that are shipped as part of
       gretl’s official “addons”. (Addons are function packages that are more tightly integrated
       with the gretl program than standard user-contributed packages.)
    - Exit: Quit the program. You’ll be prompted to save any unsaved work.
- Tools menu
    - Statistical tables: Look up critical values for commonly used distributions (normal or
       Gaussian, _t_ , chi-square, _F_ and Durbin–Watson).
    - P-value finder: Look up p-values from the Gaussian, _t_ , chi-square, _F_ , gamma, binomial or
       Poisson distributions. See also the pvalue command in the _Gretl Command Reference_.


Chapter 2. Getting started 8

- Distribution graphs: Produce graphs of various probability distributions. In the resulting
    graph window, the pop-up menu includes an item “Add another curve”, which enables
    you to superimpose a further plot (for example, you can draw the _t_ distribution with
    various different degrees of freedom).
- Test statistic calculator: Calculate test statistics and p-values for a range of common hy-
    pothesis tests (population mean, variance and proportion; difference of means, variances
    and proportions).
- Nonparametric tests: Calculate test statistics for various nonparametric tests (Sign test,
    Wilcoxon rank sum test, Wilcoxon signed rank test, Runs test).
- Seed for random numbers: Set the seed for the random number generator (by default
    this is set based on the system time when the program is started).
- Command log: Open a window containing a record of the commands executed so far.
- Gretl console: Open a “console” window into which you can type commands as you would
    using the command-line program, gretlcli (as opposed to using point-and-click).
- Start Gnu R: Start R (if it is installed on your system), and load a copy of the data set
    currently open in gretl. See Appendix D.
- Sort variables: Rearrange the listing of variables in the main window, either by ID number
    or alphabetically by name.
- Function packages: Handles “function packages” (see Section 14.5), which allow you to
    access functions written by other users and share the ones written by you.
- NIST test suite: Check the numerical accuracy of gretl against the reference results for
    linear regression made available by the (US) National Institute of Standards and Technol-
    ogy.
- Preferences: Set the paths to various files gretl needs to access. Choose the font in which
    gretl displays text output. Activate or suppress gretl’s messaging about the availability
    of program updates, and so on. See the _Gretl Command Reference_ for further details.
- Data menu
- Select all: Several menu items act upon those variables that are currently selected in the
main window. This item lets you select all the variables.
- Display values: Pops up a window with a simple (not editable) printout of the values of
the selected variable or variables.
- Edit values: Opens a spreadsheet window where you can edit the values of the selected
variables.
- Add observations: Gives a dialog box in which you can choose a number of observations
to add at the end of the current dataset; for use with forecasting.
- Remove extra observations: Active only if extra observations have been added automati-
cally in the process of forecasting; deletes these extra observations.
- Read info, Edit info: “Read info” just displays the summary information for the current
data file; “Edit info” allows you to make changes to it (if you have permission to do so).
- Print description: Opens a window containing a full account of the current dataset, in-
cluding the summary information and any specific information on each of the variables.
- Add case markers: Prompts for the name of a text file containing “case markers” (short
strings identifying the individual observations) and adds this information to the data set.
See Chapter 4.
- Remove case markers: Active only if the dataset has case markers identifying the obser-
vations; removes these case markers.


Chapter 2. Getting started 9

- Dataset structure: invokes a series of dialog boxes which allow you to change the struc-
    tural interpretation of the current dataset. For example, if data were read in as a cross
    section you can get the program to interpret them as time series or as a panel. See also
    section 4.4.
- Compact data: For time-series data of higher than annual frequency, gives you the option
    of compacting the data to a lower frequency, using one of four compaction methods
    (average, sum, start of period or end of period).
- Expand data: For time-series data, gives you the option of expanding the data to a higher
    frequency.
- Transpose data: Turn each observation into a variable and vice versa (or in other words,
    each row of the data matrix becomes a column in the modified data matrix); can be useful
    with imported data that have been read in “sideways”.
- View menu
- Icon view: Opens a window showing the content of the current session as a set of icons;
see section 3.4.
- Graph specified vars: Gives a choice between a time series plot, a regular X–Y scatter
plot, an X–Y plot using impulses (vertical bars), an X–Y plot “with factor separation” (i.e.
with the points colored differently depending to the value of a given dummy variable),
boxplots, and a 3-D graph. Serves up a dialog box where you specify the variables to
graph. See Chapter 6 for details.
- Multiple graphs: Allows you to compose a set of up to six small graphs, either pairwise
scatter-plots or time-series graphs. These are displayed together in a single window.
- Summary statistics: Shows a full set of descriptive statistics for the variables selected in
the main window.
- Correlation matrix: Shows the pairwise correlation coefficients for the selected variables.
- Cross Tabulation: Shows a cross-tabulation of the selected variables. This works only if
at least two variables in the data set have been marked as discrete (see Chapter 12).
- Principal components: Produces a Principal Components Analysis for the selected vari-
ables.
- Mahalanobis distances: Computes the Mahalanobis distance of each observation from
the centroid of the selected set of variables.
- Cross-correlogram: Computes and graphs the cross-correlogram for two selected vari-
ables.
- Add menu Offers various standard transformations of variables (logs, lags, squares, etc.) that
you may wish to add to the data set. Also gives the option of adding random variables, and
(for time-series data) adding seasonal dummy variables (e.g. quarterly dummy variables for
quarterly data).
- Sample menu
- Set range: Select a different starting and/or ending point for the current sample, within
the range of data available.
- Restore full range: self-explanatory.
- Define, based on dummy: Given a dummy (indicator) variable with values 0 or 1, this
drops from the current sample all observations for which the dummy variable has value
0.
- Restrict, based on criterion: Similar to the item above, except that you don’t need a pre-
defined variable: you supply a Boolean expression (e.g. sqft > 1400) and the sample is
restricted to observations satisfying that condition. See the entry for genr in the _Gretl
Command Reference_ for details on the Boolean operators that can be used.


Chapter 2. Getting started 10

- Random sub-sample: Draw a random sample from the full dataset.
- Drop all obs with missing values: Drop from the current sample all observations for
    which at least one variable has a missing value (see Section 4.6).
- Count missing values: Give a report on observations where data values are missing. May
    be useful in examining a panel data set, where it’s quite common to encounter missing
    values.
- Set missing value code: Set a numerical value that will be interpreted as “missing” or “not
    available”. This is intended for use with imported data, when gretl has not recognized
    the missing-value code used.
- Variable menu Most items under here operate on a single variable at a time. The “active”
variable is set by highlighting it (clicking on its row) in the main data window. Most options
will be self-explanatory. Note that you can rename a variable and can edit its descriptive label
under “Edit attributes”. You can also “Define a new variable” via a formula (e.g. involving
some function of one or more existing variables). For the syntax of such formulae, look at the
online help for “Generate variable syntax” or see the genr command in the _Gretl Command
Reference_. One simple example:

```
foo = x1 * x2
```
```
will create a new variable foo as the product of the existing variables x1 and x2. In these
formulae, variables must be referenced by name, not number.
```
- Model menu For details on the various estimators offered under this menu please consult the
    _Gretl Command Reference_. Also see Chapter 25 regarding the estimation of nonlinear models.
- Help menu Please use this as needed! It gives details on the syntax required in various dialog
    entries.

### 2.4 Keyboard shortcuts

When working in the main gretl window, some common operations may be performed using the
keyboard, as shown in the table below.

```
Return Opens a window displaying the values of the currently selected variables: it is
the same as selecting “Data, Display Values”.
Delete Pressing this key has the effect of deleting the selected variables. A confirma-
tion is required, to prevent accidental deletions.
e Has the same effect as selecting “Edit attributes” from the “Variable” menu.
F2 Same as “e”. Included for compatibility with other programs.
g Has the same effect as selecting “Define new variable” from the “Variable”
menu (which maps onto the genr command).
h Opens a help window for gretl commands.
F1 Same as “h”. Included for compatibility with other programs.
r Refreshes the variable list in the main window.
t Graphs the selected variable; a line graph is used for time-series datasets,
whereas a distribution plot is used for cross-sectional data.
```
### 2.5 The gretl toolbar

At the bottom left of the main window sits the toolbar.


Chapter 2. Getting started 11

The icons have the following functions, reading from left to right:

1. Launch a calculator program. A convenience function in case you want quick access to a
    calculator when you’re working in gretl. The default program is calc.exe under MS Win-
    dows, or xcalc under the X window system. You can change the program under the “Tools,
    Preferences, General” menu, “Programs” tab.
2. Start a new script. Opens an editor window in which you can type a series of commands to be
    sent to the program as a batch.
3. Open the gretl console. A shortcut to the “Gretl console” menu item (Section 2.3 above).
4. Open the session icon window.
5. Open a window displaying available gretl function packages.
6. Open this manual in PDF format.
7. Open the help item for script commands syntax (i.e. a listing with details of all available
    commands).
8. Open the dialog box for defining a graph.
9. Open the dialog box for estimating a model using ordinary least squares.
10. Open a window listing the sample datasets supplied with gretl, and any other data file collec-
tions that have been installed.


## Chapter 3

Modes of working

### 3.1 Command scripts

As you execute commands in gretl, using the GUI and filling in dialog entries, those commands are
recorded in the form of a “script” or batch file. Such scripts can be edited and re-run, using either
gretl or the command-line client, gretlcli.

To view the current state of the script at any point in a gretl session, choose “Command log” under
the Tools menu. This log file is called session.inp and it is overwritten whenever you start a new
session. To preserve it, save the script under a different name. Script files will be found most easily,
using the GUI file selector, if you name them with the extension “.inp”.

To open a script you have written independently, use the “File, Script files” menu item; to create a
script from scratch use the “File, Script files, New script” item or the “new script” toolbar button.
In either case a script window will open (see Figure 3.1).

```
Figure 3.1: Script window, editing a command file
```
The toolbar at the top of the script window offers the following functions (left to right): (1) Save
the file; (2) Save the file under a specified name; (3) Print the file (this option is not available on all
platforms); (4) Execute the commands in the file; (5) Copy selected text; (6) Paste the selected text;
(7) Find and replace text; (8) Undo the last Paste or Replace action; (9) Help (if you place the cursor
in a command word and press the question mark you will get help on that command); (10) Close
the window.

When you execute the script, by clicking on the Execute icon or by pressing Ctrl-r, all output is
directed to a single window, where it can be edited, saved or copied to the clipboard. To learn
more about the possibilities of scripting, take a look at the gretl Help item “Command reference,”

#### 12


Chapter 3. Modes of working 13

or start up the command-line program gretlcli and consult its help, or consult the _Gretl Command
Reference_.

If you run the script when part of it is highlighted, gretl will only run that portion. Moreover, if you
want to run just the current line, you can do so by pressing Ctrl-Enter.^1

Clicking the right mouse button in the script editor window produces a pop-up menu. This gives
you the option of executing either the line on which the cursor is located, or the selected region of
the script if there’s a selection in place. If the script is editable, this menu also gives the option of
adding or removing comment markers from the start of the line or lines.

The gretl package includes over 70 example scripts. Many of these relate to Ramanathan (2002),
but they may also be used as a free-standing introduction to scripting in gretl and to various points
of econometric theory. You can explore the example files under “File, Script files, Example scripts”
There you will find a listing of the files along with a brief description of the points they illustrate
and the data they employ. Open any file and run it to see the output. Note that long commands in
a script can be broken over two or more lines, using backslash as a continuation character.

You can, if you wish, use the GUI controls and the scripting approach in tandem, exploiting each
method where it offers greater convenience. Here are two suggestions.

- Open a data file in the GUI. Explore the data — generate graphs, run regressions, perform tests.
    Then open the Command log, edit out any redundant commands, and save it under a specific
    name. Run the script to generate a single file containing a concise record of your work.
- Start by establishing a new script file. Type in any commands that may be required to set
    up transformations of the data (see the genr command in the _Gretl Command Reference_ ).
    Typically this sort of thing can be accomplished more efficiently via commands assembled
    with forethought rather than point-and-click. Then save and run the script: the GUI data
    window will be updated accordingly. Now you can carry out further exploration of the data
    via the GUI. To revisit the data at a later point, open and rerun the “preparatory” script first.

Scripts and data files

One common way of doing econometric research with gretl is as follows: compose a script; execute
the script; inspect the output; modify the script; run it again — with the last three steps repeated as
many times as necessary. In this context, note that when you open a data file this clears out most
of gretl’s internal state. It’s therefore probably a good idea to have your script start with an open
command: the data file will be re-opened each time, and you can be confident you’re getting “fresh”
results.

One further point should be noted. When you go to open a new data file via the graphical interface,
you are always prompted: opening a new data file will lose any unsaved work, do you really want
to do this? When you execute a script that opens a data file, however, you are _not_ prompted. The
assumption is that in this case you’re not going to lose any work, because the work is embodied
in the script itself (and it would be annoying to be prompted at each iteration of the work cycle
described above).

This means you should be careful if you’ve done work using the graphical interface and then decide
to run a script: the current data file will be replaced without any questions asked, and it’s your
responsibility to save any changes to your data first.

(^1) This feature is not unique to gretl; other econometric packages offer the same facility. However, experience shows
that while this can be remarkably useful, it can also lead to writing dinosaur scripts that are never meant to be executed
all at once, but rather used as a chaotic repository to cherry-pick snippets from. Since gretl allows you to have several
script windows open at the same time, you may want to keep your scripts tidy and reasonably small.


Chapter 3. Modes of working 14

### 3.2 Saving script objects

When you estimate a model using point-and-click, the model results are displayed in a separate
window, offering menus which let you perform tests, draw graphs, save data from the model, and
so on. Ordinarily, when you estimate a model using a script you just get a non-interactive printout
of the results. You can, however, arrange for models estimated in a script to be “captured”, so that
you can examine them interactively when the script is finished. Here is an example of the syntax
for achieving this effect:

```
Model1 <- ols Ct 0 Yt
```
That is, you type a name for the model to be saved under, then a back-pointing “assignment arrow”,
then the model command. The assignment arrow is composed of the less-than sign followed by a
dash; it must be separated by spaces from both the preceding name and the following command.
The name for a saved object may include spaces, but in that case it must be wrapped in double
quotes:

```
"Model 1" <- ols Ct 0 Yt
```
Models saved in this way will appear as icons in the gretl icon view window (see Section 3.4) after
the script is executed. In addition, you can arrange to have a named model displayed (in its own
window) automatically as follows:

```
Model1.show
```
Again, if the name contains spaces it must be quoted:

```
"Model 1".show
```
The same facility can be used for graphs. For example the following will create a plot of Ct against
Yt, save it under the name “CrossPlot” (it will appear under this name in the icon view window),
and have it displayed:

```
CrossPlot <- gnuplot Ct Yt
CrossPlot.show
```
You can also save the output from selected commands as named pieces of text (again, these will
appear in the session icon window, from where you can open them later). For example this com-
mand sends the output from an augmented Dickey–Fuller test to a “text object” named ADF1 and
displays it in a window:

```
ADF1 <- adf 2 x1
ADF1.show
```
Objects saved in this way (whether models, graphs or pieces of text output) can be destroyed using
the command .free appended to the name of the object, as in ADF1.free.

### 3.3 The gretl console

A further option is available for your computing convenience. Under gretl’s “Tools” menu you will
find the item “Gretl console” (there is also an “open gretl console” button on the toolbar in the
main window). This opens up a window in which you can type commands and execute them one
by one (by pressing the Enter key) interactively. This is essentially the same as gretlcli’s mode of
operation, except that the GUI is updated based on commands executed from the console, enabling
you to work back and forth as you wish.


Chapter 3. Modes of working 15

In the console, you have “command history”; that is, you can use the up and down arrow keys to
navigate the list of command you have entered to date. You can retrieve, edit and then re-enter a
previous command. In console mode, you can create, display and free objects (models, graphs or
text) as described above for script mode.

```
Figure 3.2: Main window including console
```
Optionally, the console can be shown not as a separate window, but as a side pane to the main
window, as in Figure 3.2. Some people prefer this arrangement, that is vaguely reminiscent of
other programs such as Rstudio or the Octave GUI interface. In order to activate the “split panes”
interface, go to the Tools menu, select “Preferences” and tick the “Main window includes console”
box.

### 3.4 The Session concept

Gretl offers the idea of a “session” as a way of keeping track of your work and revisiting it later.
The basic idea is to provide an iconic space containing various objects pertaining to your current
working session (see Figure 3.3). You can add objects (represented by icons) to this space as you
go along. If you save the session, these added objects should be available again if you re-open the
session later.

```
Figure 3.3: Icon view: one model and one graph have been added to the default icons
```

Chapter 3. Modes of working 16

If you start gretl and open a data set, then select “Icon view” from the View menu, you should see
the basic default set of icons: these give you quick access to information on the data set (if any),
correlation matrix (“Correlations”) and descriptive summary statistics (“Summary”). All of these
are activated by double-clicking the relevant icon. The “Data set” icon is a little more complex:
double-clicking opens up the data in the built-in spreadsheet, but you can also right-click on the
icon for a menu of other actions.

To add a model to the Icon view, first estimate it using the Model menu. Then pull down the File
menu in the model window and select “Save to session as icon... ” or “Save as icon and close”.
Simply hitting the S key over the model window is a shortcut to the latter action.

To add a graph, first create it (under the View menu, “Graph specified vars”, or via one of gretl’s
other graph-generating commands). Click on the graph window to bring up the graph menu, and
select “Save to session as icon”.

Once a model or graph is added its icon will appear in the Icon view window. Double-clicking on the
icon redisplays the object, while right-clicking brings up a menu which lets you display or delete
the object. This popup menu also gives you the option of editing graphs.

The model table

In econometric research it is common to estimate several models with a common dependent
variable — the models differing in respect of which independent variables are included, or per-
haps in respect of the estimator used. In this situation it is convenient to present the regression
results in the form of a table, where each column contains the results (coefficient estimates and
standard errors) for a given model, and each row contains the estimates for a given variable across
the models. Note that some estimation methods are not compatible with the straightforward model
table format, therefore gretl will not let those models be added to the model table. These meth-
ods include non-linear least squares (nls), generic maximum-likelihood estimators (mle), generic
GMM (gmm), dynamic panel models (dpanel), interval regressions (intreg), bivariate probit models
(biprobit), AR(I)MA models (arima or arma), and (G)ARCH models (garch and arch).

In the Icon view window gretl provides a means of constructing such a table (and copying it in plain
text, LATEX or Rich Text Format). The procedure is outlined below. (The model table can also be built
non-interactively, in script mode — see the entry for modeltab in the _Gretl Command Reference_ .)

1. Estimate a model which you wish to include in the table, and in the model display window,
    under the File menu, select “Save to session as icon” or “Save as icon and close”.
2. Repeat step 1 for the other models to be included in the table (up to a total of six models).
3. When you are done estimating the models, open the icon view of your gretl session, by se-
    lecting “Icon view” under the View menu in the main gretl window, or by clicking the “session
    icon view” icon on the gretl toolbar.
4. In the Icon view, there is an icon labeled “Model table”. Decide which model you wish to
    appear in the left-most column of the model table and add it to the table, either by dragging
    its icon onto the Model table icon, or by right-clicking on the model icon and selecting “Add
    to model table” from the pop-up menu.
5. Repeat step 4 for the other models you wish to include in the table. The second model selected
    will appear in the second column from the left, and so on.
6. When you are finished composing the model table, display it by double-clicking on its icon.
    Under the Edit menu in the window which appears, you have the option of copying the table
    to the clipboard in various formats.
7. If the ordering of the models in the table is not what you wanted, right-click on the model
    table icon and select “Clear table”. Then go back to step 4 above and try again.

A simple instance of gretl’s model table is shown in Figure 3.4.


Chapter 3. Modes of working 17

```
Figure 3.4: Example of model table
```
The graph page

The “graph page” icon in the session window offers a means of putting together several graphs
for printing on a single page. This facility will work only if you have the LATEX typesetting system
installed, and are able to generate and view either PDF or PostScript output. The output format
is controlled by your choice of program for compiling TEX files, which can be found under the
“Programs” tab in the Preferences dialog box (under the “Tools” menu in the main window). Usually
this should be pdflatex for PDF output or latex for PostScript. In the latter case you must have a
working set-up for handling PostScript, which will usually include dvips, ghostscript and a viewer
such as gv, ggv or kghostview.

In the Icon view window, you can drag up to eight graphs onto the graph page icon. When you
double-click on the icon (or right-click and select “Display”), a page containing the selected graphs
(in PDF or EPS format) will be composed and opened in your viewer. From there you should be able
to print the page.

To clear the graph page, right-click on its icon and select “Clear”.

As with the model table, it is also possible to manipulate the graph page via commands in script or
console mode — see the entry for the graphpg command in the _Gretl Command Reference_.

Saving and re-opening sessions

If you create models or graphs that you think you may wish to re-examine later, then before quitting
gretl select “Session files, Save session” from the File menu and give a name under which to save
the session. To re-open the session later, either

- Start gretl then re-open the session file by going to the “File, Session files, Open session”, or
- From the command line, type gretl -r _sessionfile_ , where _sessionfile_ is the name under which
    the session was saved, or
- Drag the icon representing a session file onto gretl.


## Chapter 4

Data files

### 4.1 Data file formats

Gretl has its own native format for data files. Most users will probably not want to read or write
such files outside of gretl itself, but occasionally this may be useful and details on the file formats
are given in Appendix A. The program can also import data from a variety of other formats. In
the GUI program this can be done via the “File, Open Data, User file” menu — note the drop-down
list of acceptable file types. In script mode, simply use the open command. The supported import
formats are as follows.

- Plain text files (comma-separated or “CSV” being the most common type). For details on what
    gretl expects of such files, see Section 4.3.
- Spreadsheets: MS Excel, Gnumeric and Open Document (ODS). The requirements for such files
    are given in Section 4.3.
- Stata data files (.dta).
- SPSS data files (.sav).
- SAS “xport” files (.xpt).
- Eviews workfiles (.wf1).^1
- JMulTi data files.

When you import data from a plain text format, gretl opens a “diagnostic” window, reporting on its
progress in reading the data. If you encounter a problem with ill-formatted data, the messages in
this window should give you a handle on fixing the problem.

Note that gretl has a facility for writing out data in the native formats of GNU R, Octave, JMulTi and
PcGive (see Appendix D). In the GUI client this option is found under the “File, Export data” menu;
in the command-line client use the store command with the appropriate option flag.

### 4.2 Databases

For working with large amounts of data gretl is supplied with a database-handling routine. A
_database_ , as opposed to a _data file_ , is not read directly into the program’s workspace. A database
can contain series of mixed frequencies and sample ranges. You open the database and select
series to import into the working dataset. You can then save those series in a native format data
file if you wish. Databases can be accessed via the menu item “File, Databases”.

For details on the format of gretl databases, see Appendix A.

(^1) See [http://users.wfu.edu/cottrell/eviews_format/.](http://users.wfu.edu/cottrell/eviews_format/.)

#### 18


Chapter 4. Data files 19

Online access to databases

Several gretl databases are available from Wake Forest University. Your computer must be con-
nected to the internet for this option to work. Please see the description of the “data” command
under the Help menu.

☞ Visit the gretl data page for details and updates on available data.

Foreign database formats

Thanks to Thomas Doan of _Estima_ , who made available the specification of the database format
used by RATS 4 (Regression Analysis of Time Series), gretl can handle such databases — or at least,
a subset of same, namely time-series databases containing monthly and quarterly series.

Gretl can also import data from PcGive databases. These take the form of a pair of files, one
containing the actual data (with suffix .bn7) and one containing supplementary information (.in7).

In addition, gretl offers ODBC connectivity. Be warned: this feature is meant for somewhat ad-
vanced users; there is currently no graphical interface. Interested readers will find more info in
appendix 42.

### 4.3 Creating a dataset from scratch

There are several ways of doing this:

1. Find, or create using a text editor, a plain text data file and open it via “Import”.
2. Use your favorite spreadsheet to establish the data file, save it in comma-separated format if
    necessary (this may not be necessary if the spreadsheet format is MS Excel, Gnumeric or Open
    Document), then use one of the “Import” options.
3. Use gretl’s built-in spreadsheet.
4. Select data series from a suitable database.
5. Use your favorite text editor or other software tools to a create data file in gretl format inde-
    pendently.

Here are a few comments and details on these methods.

Common points on imported data

Options (1) and (2) involve using gretl’s “import” mechanism. For the program to read such data
successfully, certain general conditions must be satisfied:

- The first row must contain valid variable names. A valid variable name is of 31 characters
    maximum; starts with a letter; and contains nothing but letters, numbers and the underscore
    character, _. (Longer variable names will be truncated to 31 characters.) Qualifications to the
    above: First, in the case of an plain text import, if the file contains no row with variable names
    the program will automatically add names, v1, v2 and so on. Second, by “the first row” is
    meant the first _relevant_ row. In the case of plain text imports, blank rows and rows beginning
    with a hash mark, #, are ignored. In the case of Excel, Gnumeric and ODS imports, you are
    presented with a dialog box where you can select an offset into the spreadsheet, so that gretl
    will ignore a specified number of rows and/or columns.
- Data values: these should constitute a rectangular block, with one variable per column (and
    one observation per row). The number of variables (data columns) must match the number
    of variable names given. See also section 4.6. Numeric data are expected, but in the case of


Chapter 4. Data files 20

```
importing from plain text, the program offers limited handling of character (string) data: if
a given column contains character data only, consecutive numeric codes are substituted for
the strings, and once the import is complete a table is printed showing the correspondence
between the strings and the codes.
```
- Dates (or observation labels): Optionally, the _first_ column may contain strings such as dates,
    or labels for cross-sectional observations. Such strings have a maximum of 15 characters (as
    with variable names, longer strings will be truncated). A column of this sort should be headed
    with the string obs or date, or the first row entry may be left blank.
    For dates to be recognized as such, the date strings should adhere to one or other of a set of
    specific formats, as follows. For _annual_ data: 4-digit years. For _quarterly_ data: a 4-digit year,
    followed by a separator (either a period, a colon, or the letter Q), followed by a 1-digit quarter.
    Examples: 1997.1, 2002:3, 1947Q1. For _monthly_ data: a 4-digit year, followed by a period or
    a colon, followed by a two-digit month. Examples: 1997.01, 2002:10.

Plain text (“CSV”) files can use comma, space, tab or semicolon as the column separator. When you
open such a file via the GUI you are given the option of specifying the separator, though in most
cases it should be detected automatically.

If you use a spreadsheet to prepare your data you are able to carry out various transformations of
the “raw” data with ease (adding things up, taking percentages or whatever): note, however, that
you can also do this sort of thing easily — perhaps more easily — within gretl, by using the tools
under the “Add” menu.

Appending imported data

You may wish to establish a dataset piece by piece, by incremental importation of data from other
sources. This is supported via the “File, Append data” menu items: gretl will check the new data for
conformability with the existing dataset and, if everything seems OK, will merge the data. You can
add new variables in this way, provided the data frequency matches that of the existing dataset. Or
you can append new observations for data series that are already present; in this case the variable
names must match up correctly. Note that by default (that is, if you choose “Open data” rather
than “Append data”), opening a new data file closes the current one.

Using the built-in spreadsheet

Under the “File, New data set” menu you can choose the sort of dataset you want to establish (e.g.
quarterly time series, cross-sectional). You will then be prompted for starting and ending dates (or
observation numbers) and the name of the first variable to add to the dataset. After supplying this
information you will be faced with a simple spreadsheet into which you can type data values. In
the spreadsheet window, clicking the right mouse button will invoke a popup menu which enables
you to add a new variable (column), to add an observation (append a row at the foot of the sheet),
or to insert an observation at the selected point (move the data down and insert a blank row.)

Once you have entered data into the spreadsheet you import these into gretl’s workspace using the
spreadsheet’s “Apply changes” button.

Please note that gretl’s spreadsheet is quite basic and has no support for functions or formulas.
Data transformations are done via the “Add” or “Variable” menus in the main window.

Selecting from a database

Another alternative is to establish your dataset by selecting variables from a database.

Begin with the “File, Databases” menu item. This has four forks: “Gretl native”, “RATS 4”, “PcGive”
and “On database server”. You should be able to find the file fedstl.bin in the file selector that


Chapter 4. Data files 21

opens if you choose the “Gretl native” option since this file, which contains a large collection of US
macroeconomic time series, is supplied with the distribution.

You won’t find anything under “RATS 4” unless you have purchased RATS data.^2 If you do possess
RATS data you should go into the “Tools, Preferences, General” dialog, select the Databases tab,
and fill in the correct path to your RATS files.

If your computer is connected to the internet you should find several databases (at Wake Forest
University) under “On database server”. You can browse these remotely; you also have the option
of installing them onto your own computer. The initial remote databases window has an item
showing, for each file, whether it is already installed locally (and if so, if the local version is up to
date with the version at Wake Forest).

Assuming you have managed to open a database you can import selected series into gretl’s workspace
by using the “Series, Import” menu item in the database window, or via the popup menu that ap-
pears if you click the right mouse button, or by dragging the series into the program’s main window.

Creating a gretl data file independently

It is possible to create a data file in one or other of gretl’s own formats using a text editor or
software tools such as awk, sed or perl. This may be a good choice if you have large amounts
of data already in machine readable form. You will, of course, need to study these data formats
(XML-based or “traditional”) as described in Appendix A.

### 4.4 Structuring a dataset

Once your data are read by gretl, it may be necessary to supply some information on the nature of
the data. We distinguish between three kinds of datasets:

1. Cross section
2. Time series
3. Panel data

The primary tool for doing this is the “Data, Dataset structure” menu entry in the graphical inter-
face, or the setobs command for scripts and the command-line interface.

Cross sectional data

By a cross section we mean observations on a set of “units” (which may be firms, countries, indi-
viduals, or whatever) at a common point in time. This is the default interpretation for a data file:
if there is insufficient information to interpret data as time-series or panel data, they are automat-
ically interpreted as a cross section. In the unlikely event that cross-sectional data are wrongly
interpreted as time series, you can correct this by selecting the “Data, Dataset structure” menu
item. Click the “cross-sectional” radio button in the dialog box that appears, then click “Forward”.
Click “OK” to confirm your selection.

Time series data

When you import data from a spreadsheet or plain text file, gretl will make fairly strenuous efforts
to glean time-series information from the first column of the data, if it looks at all plausible that
such information may be present. If time-series structure is present but not recognized, again you
can use the “Data, Dataset structure” menu item. Select “Time series” and click “Forward”; select the
appropriate data frequency and click “Forward” again; then select or enter the starting observation

(^2) See [http://www.estima.com](http://www.estima.com)


Chapter 4. Data files 22

and click “Forward” once more. Finally, click “OK” to confirm the time-series interpretation if it is
correct (or click “Back” to make adjustments if need be).

Besides the basic business of getting a data set interpreted as time series, further issues may arise
relating to the frequency of time-series data. In a gretl time-series data set, all the series must
have the same frequency. Suppose you wish to make a combined dataset using series that, in their
original state, are not all of the same frequency. For example, some series are monthly and some
are quarterly.

Your first step is to formulate a strategy: Do you want to end up with a quarterly or a monthly data
set? A basic point to note here is that “compacting” data from a higher frequency (e.g. monthly) to
a lower frequency (e.g. quarterly) is usually unproblematic. You lose information in doing so, but
in general it is perfectly legitimate to take (say) the average of three monthly observations to create
a quarterly observation. On the other hand, “expanding” data from a lower to a higher frequency is
not, in general, a valid operation.

In most cases, then, the best strategy is to start by creating a data set of the _lower_ frequency, and
then to compact the higher frequency data to match. When you import higher-frequency data from
a database into the current data set, you are given a choice of compaction method (average, sum,
start of period, or end of period). In most instances “average” is likely to be appropriate.

You _can_ also import lower-frequency data into a high-frequency data set, but this is generally not
recommended. What gretl does in this case is simply replicate the values of the lower-frequency
series as many times as required. For example, suppose we have a quarterly series with the value
35.5 in 1990:1, the first quarter of 1990. On expansion to monthly, the value 35.5 will be assigned
to the observations for January, February and March of 1990. The expanded variable is therefore
useless for fine-grained time-series analysis, outside of the special case where you know that the
variable in question does in fact remain constant over the sub-periods.

When the current data frequency is appropriate, gretl offers both “Compact data” and “Expand
data” options under the “Data” menu. These options operate on the whole data set, compacting or
exanding all series. They should be considered “expert” options and should be used with caution.

Panel data

Panel data are inherently three dimensional — the dimensions being variable, cross-sectional unit,
and time-period. For example, a particular number in a panel data set might be identified as the
observation on capital stock for General Motors in 1980. (A note on terminology: we use the
terms “cross-sectional unit”, “unit” and “group” interchangeably below to refer to the entities that
compose the cross-sectional dimension of the panel. These might, for instance, be firms, countries
or persons.)

For representation in a textual computer file (and also for gretl’s internal calculations) the three
dimensions must somehow be flattened into two. This “flattening” involves taking layers of the
data that would naturally stack in a third dimension, and stacking them in the vertical dimension.

gretl always expects data to be arranged “by observation”, that is, such that each row represents an
observation (and each variable occupies one and only one column). In this context the flattening of
a panel data set can be done in either of two ways:

- Stacked time series: the successive vertical blocks each comprise a time series for a given
    unit.
- Stacked cross sections: the successive vertical blocks each comprise a cross-section for a
    given period.

You may input data in whichever arrangement is more convenient. Internally, however, gretl always
stores panel data in the form of stacked time series.


Chapter 4. Data files 23

### 4.5 Panel data specifics

When you import panel data into gretl from a spreadsheet or comma separated format, the panel
nature of the data will not be recognized automatically (most likely the data will be treated as
“undated”). A panel interpretation can be imposed on the data using the graphical interface or via
the setobs command.

In the graphical interface, use the menu item “Data, Dataset structure”. In the first dialog box
that appears, select “Panel”. In the next dialog you have a three-way choice. The first two options,
“Stacked time series” and “Stacked cross sections” are applicable if the data set is already organized
in one of these two ways. If you select either of these options, the next step is to specify the number
of cross-sectional units in the data set. The third option, “Use index variables”, is applicable if the
data set contains two variables that index the units and the time periods respectively; the next step
is then to select those variables. For example, a data file might contain a country code variable and
a variable representing the year of the observation. In that case gretl can reconstruct the panel
structure of the data regardless of how the observation rows are organized.

The setobs command has options that parallel those in the graphical interface. If suitable index
variables are available you can do, for example

```
setobs unitvar timevar --panel-vars
```
where unitvar is a variable that indexes the units and timevar is a variable indexing the periods.
Alternatively you can use the form setobs _freq_ 1:1 _structure_ , where _freq_ is replaced by the “block
size” of the data (that is, the number of periods in the case of stacked time series, or the number
of units in the case of stacked cross-sections) and structure is either --stacked-time-series or
--stacked-cross-section. Two examples are given below: the first is suitable for a panel in
the form of stacked time series with observations from 20 periods; the second for stacked cross
sections with 5 units.

```
setobs 20 1:1 --stacked-time-series
setobs 5 1:1 --stacked-cross-section
```
Panel data arranged by variable

Publicly available panel data sometimes come arranged “by variable.” Suppose we have data on two
variables, x1 and x2, for each of 50 states in each of 5 years (giving a total of 250 observations
per variable). One textual representation of such a data set would start with a block for x1, with
50 rows corresponding to the states and 5 columns corresponding to the years. This would be
followed, vertically, by a block with the same structure for variable x2. A fragment of such a data
file is shown below, with quinquennial observations 1965–1985. Imagine the table continued for
48 more states, followed by another 50 rows for variable x2.

```
x1
1965 1970 1975 1980 1985
AR 100.0 110.5 118.7 131.2 160.4
AZ 100.0 104.3 113.8 120.9 140.6
```
If a datafile with this sort of structure is read into gretl,^3 the program will interpret the columns as
distinct variables, so the data will not be usable “as is.” But there is a mechanism for correcting the
situation, namely the stack function.

Consider the first data column in the fragment above: the first 50 rows of this column constitute a
cross-section for the variable x1 in the year 1965. If we could create a new series by stacking the

(^3) Note that you will have to modify such a datafile slightly before it can be read at all. The line containing the variable
name (in this example x1) will have to be removed, and so will the initial row containing the years, otherwise they will be
taken as numerical data.


Chapter 4. Data files 24

first 50 entries in the second column underneath the first 50 entries in the first, we would be on the
way to making a data set “by observation” (in the first of the two forms mentioned above, stacked
cross-sections). That is, we’d have a column comprising a cross-section for x1 in 1965, followed by
a cross-section for the same variable in 1970.

The following gretl script illustrates how we can accomplish the stacking, for both x1 and x2. We
assume that the original data file is called panel.txt, and that in this file the columns are headed
with “variable names” v1, v2,... , v5. (The columns are not really variables, but in the first instance
we “pretend” that they are.)

```
open panel.txt
series x1 = stack(v1..v5, 50)
series x2 = stack(v1..v5, 50, 50)
setobs 50 1:1 --stacked-cross-section
store panel.gdt x1 x2
```
The second and third lines illustrate the syntax of the stack function, which has this signature:

```
series stack(list L, scalar length, scalar offset)
```
- L: a list of series on which to operate.
- length: an integer giving the number of observations to take from each series.
- offset: an integer giving the offset from the top of the dataset at which to start taking values
    (optional, defaults to 0).

The “..” syntax in the example above constructs a list of the 5 contiguous series to be stacked.
More generally, you can define a named list of series and pass that as the first argument to stack
(see chapter 15). In this example we’re supposing that the full data set contains 100 rows, and that
in the stacking of variable x1 we wish to read only the first 50 rows from each column, so we give
50 as the second argument.

On line 3 we do the stacking for variable x2. Again we want a length of 50 for the components of
the stacked series, but this time we want to start reading from the 50th row of the original data,
and so we add a third offset argument of 50. Line 4 then imposes a panel interpretation on the
data. Finally, we save the stacked data to file, with the panel interpretation.

The illustrative script above is appropriate when the number of variables to be processed is small.
When then are many variables in the dataset it will be more convenient to use a loop to accomplish
the stacking, as shown in the following script. The setup is presumed to be the same as in the
previous case (50 units, 5 periods), but with 20 variables rather than 2.

```
open panel.txt
list L = v1..v5 # predefine a list of series
scalar length = 50
loop i=1..20
scalar offset = (i - 1) * length
series x$i = stack(L, length, offset)
endloop
setobs 50 1.01 --stacked-cross-section
store panel.gdt x1..x20
```
Side-by-side time series

There’s a second sort of data that you may wish to convert to gretl’s panel format, namely side-
by-side time series for a number of cross-sectional units. For example, a data file might contain
separate GDP series of common length _T_ for each of _N_ countries. To turn these into a single stacked


Chapter 4. Data files 25

time series the stack function can again be used. An example follows, where we suppose the
original data source is a comma-separated file named GDP.csv, containing GDP data for countries
from Austria (GDP_AT) to Zimbabwe (GDP_ZW) in consecutive columns.

```
open GDP.csv
scalar T = $nobs # the number of periods
list L = GDP_AT..GDP_ZW
series GDP = stack(L, T)
setobs T 1:01 --stacked-time-series
store panel.gdt GDP
```
The resulting data file, panel.gdt, will contain a single series of length _NT_ where _N_ is the number
of countries and _T_ is the length of the original dataset. One could insert revised variants of lines
3 and 4 of the script if the original file contained additional side-by-side per-country series for
investment, consumption or whatever.

Relatively simple cases of this transformation can be handled via gretl’s graphical interface. The
“simplicity” requirements are:

- The dataset contains exactly _M_ · _N_ time series, arranged in _M_ ≥ 1 blocks each having _N_ ≥ 2
    contiguous members.
- In each block, the _N_ series represent measures of a single variable (e.g. GDP) for a set of _N_
    cross-sectional units, and in each block these units appear in the same order.

The relevant GUI apparatus can be accessed via the item Dataset structure under the Data menu in
the main window. On selecting this item one of the options is Panel; choose this option and the
next step offers “Convert from side-by-side time series”. This leads to steps where you specify _M_
or _N_ ; give a name for the panel series; then confirm that the specified transformation is what you
want. The end result is the same as executing a series of commands on the pattern shown above,
using the stack function, then executing the additional command open panel.gdt.

Panel data marker strings

It can be helpful with panel data to have the observations identified by mnemonic markers. A
special function in the genr command is available for this purpose.

In the example under the heading “Panel data arranged by variable” above, suppose all the states
are identified by two-letter codes in the left-most column of the original datafile. When the stack
function is invoked as shown, these codes will be stacked along with the data values. If the first row
is marked AR for Arkansas, then the marker AR will end up being shown on each row containing an
observation for Arkansas. That’s all very well, but these markers don’t tell us anything about the
date of the observation. To rectify this we could do:

```
genr time
series year = 1960 + (5 * time)
genr markers = "%s:%d", marker, year
```
The first line generates a 1-based index representing the period of each observation, and the second
line uses the time variable to generate a variable representing the year of the observation. The
third line contains this special feature: if (and only if) the name of the new “variable” to generate is
markers, the portion of the command following the equals sign is taken as a C-style format string
(which must be wrapped in double quotes), followed by a comma-separated list of arguments.
The arguments will be printed according to the given format to create a new set of observation
markers. Valid arguments are either the names of variables in the dataset, or the string marker
which denotes the pre-existing observation marker. The format specifiers which are likely to be


Chapter 4. Data files 26

useful in this context are %s for a string and %d for an integer. Strings can be truncated: for
example %.3s will use just the first three characters of the string. To chop initial characters off
an existing observation marker when constructing a new one, you can use the syntax marker + n,
where n is a positive integer: in the case the first n characters will be skipped.

After the commands above are processed, then, the observation markers will look like, for example,
AR:1965, where the two-letter state code and the year of the observation are spliced together with
a colon.

Panel dummy variables

In a panel study you may wish to construct dummy variables of one or both of the following sorts:
(a) dummies as unique identifiers for the units or groups, and (b) dummies as unique identifiers for
the time periods. The former may be used to allow the intercept of the regression to differ across
the units, the latter to allow the intercept to differ across periods.

Two special functions are available to create such dummies. These are found under the “Add”
menu in the GUI, or under the genr command in script mode or gretlcli.

1. “unit dummies” (script command genr unitdum). This command creates a set of dummy
    variables identifying the cross-sectional units. The variable du_1 will have value 1 in each
    row corresponding to a unit 1 observation, 0 otherwise; du_2 will have value 1 in each row
    corresponding to a unit 2 observation, 0 otherwise; and so on.
2. “time dummies” (script command genr timedum). This command creates a set of dummy
    variables identifying the periods. The variable dt_1 will have value 1 in each row correspond-
    ing to a period 1 observation, 0 otherwise; dt_2 will have value 1 in each row corresponding
    to a period 2 observation, 0 otherwise; and so on.

If a panel data set has the YEAR of the observation entered as one of the variables you can create a
periodic dummy to pick out a particular year, e.g. genr dum = (YEAR==1960). You can also create
periodic dummy variables using the modulus operator, %. For instance, to create a dummy with
value 1 for the first observation and every thirtieth observation thereafter, 0 otherwise, do

```
genr index
series dum = ((index-1) % 30) == 0
```
Lags, differences, trends

If the time periods are evenly spaced you may want to use lagged values of variables in a panel
regression (but see also chapter 24); you may also wish to construct first differences of variables of
interest.

Once a dataset is identified as a panel, gretl will handle the generation of such variables correctly.
For example the command genr x1_1 = x1(-1) will create a variable that contains the first lag
of x1 where available, and the missing value code where the lag is not available (e.g. at the start of
the time series for each group). When you run a regression using such variables, the program will
automatically skip the missing observations.

When a panel data set has a fairly substantial time dimension, you may wish to include a trend in
the analysis. The command genr time creates a variable named time which runs from 1 to _T_ for
each unit, where _T_ is the length of the time-series dimension of the panel. If you want to create an
index that runs consecutively from 1 to _m_ × _T_ , where _m_ is the number of units in the panel, use
genr index.


Chapter 4. Data files 27

Basic statistics by unit

gretl contains functions which can be used to generate basic descriptive statistics for a given vari-
able, on a per-unit basis; these are pnobs() (number of valid cases), pmin() and pmax() (minimum
and maximum) and pmean() and psd() (mean and standard deviation).

As a brief illustration, suppose we have a panel data set comprising 8 time-series observations on
each of _N_ units or groups. Then the command

```
series pmx = pmean(x)
```
creates a series of this form: the first 8 values (corresponding to unit 1) contain the mean of x for
unit 1, the next 8 values contain the mean for unit 2, and so on. The psd() function works in a
similar manner. The sample standard deviation for group _i_ is computed as

```
si =
```
```
sP
(x − x ̄ i)^2
Ti − 1
```
where _Ti_ denotes the number of valid observations on x for the given unit, _x_ ̄ _i_ denotes the group
mean, and the summation is across valid observations for the group. If _Ti<_ 2, however, the
standard deviation is recorded as 0.

One particular use of psd() may be worth noting. If you want to form a sub-sample of a panel that
contains only those units for which the variable x is time-varying, you can either use

```
smpl pmin(x) < pmax(x) --restrict
```
or

```
smpl psd(x) > 0 --restrict
```
### 4.6 Missing data values

Representation and handling

Missing values are represented internally as NaN (“not a number”), as defined in the IEEE 754
floating-point standard. In a native-format data file they should be represented as NA. When im-
porting CSV data gretl accepts several common representations of missing values including −999,
the string NA (in upper or lower case), a single dot, or simply a blank cell. Blank cells should, of
course, be properly delimited, e.g. 120.6,,5.38, in which the middle value is presumed missing.

As for handling of missing values in the course of statistical analysis, gretl does the following:

- In calculating descriptive statistics (mean, standard deviation, etc.) under the summary com-
    mand, missing values are simply skipped and the sample size adjusted appropriately.
- In running regressions gretl first adjusts the beginning and end of the sample range, trun-
    cating the sample if need be. Missing values at the beginning of the sample are common in
    time series work due to the inclusion of lags, first differences and so on; missing values at the
    end of the range are not uncommon due to differential updating of series and possibly the
    inclusion of leads.

If gretl detects any missing values “inside” the (possibly truncated) sample range for a regression,
the result depends on the character of the dataset and the estimator chosen. In many cases, the
program will automatically skip the missing observations when calculating the regression results.
In this situation a message is printed stating how many observations were dropped. On the other
hand, the skipping of missing observations is not supported for all procedures: exceptions include


Chapter 4. Data files 28

all autoregressive estimators, system estimators such as SUR, and nonlinear least squares. In the
case of panel data, the skipping of missing observations is supported only if their omission leaves
a balanced panel. If missing observations are found in cases where they are not supported, gretl
gives an error message and refuses to produce estimates.

Manipulating missing values

Some special functions are available for the handling of missing values. The Boolean function
missing() takes the name of a variable as its single argument; it returns a series with value 1 for
each observation at which the given variable has a missing value, and value 0 otherwise (that is, if
the given variable has a valid value at that observation). The function ok() is complementary to
missing; it is just a shorthand for !missing (where! is the Boolean NOT operator). For example,
one can count the missing values for variable x using

```
scalar nmiss_x = sum(missing(x))
```
The function zeromiss(), which again takes a single series as its argument, returns a series where
all zero values are set to the missing code. This should be used with caution — one does not want
to confuse missing values and zeros — but it can be useful in some contexts. For example, one can
determine the first valid observation for a variable x using

```
genr time
scalar x0 = min(zeromiss(time * ok(x)))
```
The function misszero() does the opposite of zeromiss, that is, it converts all missing values to
zero.

If missing values get involved in calculations, they propagate according to the IEEE rules: notably,
if one of the operands to an arithmetical operation is a NaN, the result will also be NaN.

### 4.7 Maximum size of data sets

Basically, the size of data sets (both the number of variables and the number of observations per
variable) is limited only by the characteristics of your computer. Gretl allocates memory dynami-
cally, and will ask the operating system for as much memory as your data require. Obviously, then,
you are ultimately limited by the size of RAM.

Aside from the multiple-precision OLS option, gretl uses double-precision floating-point numbers
throughout. The size of such numbers in bytes depends on the computer platform, but is typically
eight. To give a rough notion of magnitudes, suppose we have a data set with 10,000 observations
on 500 variables. That’s 5 million floating-point numbers or 40 million bytes. If we define the
megabyte (MB) as 1024× 1024 bytes, as is standard in talking about RAM, it’s slightly over 38 MB.
The program needs additional memory for workspace, but even so, handling a data set of this size
should be quite feasible on a current PC, which at the time of writing is likely to have at least 256
MB of RAM.

If RAM is not an issue, there is one further limitation on data size (though it’s very unlikely to
be a binding constraint). That is, variables and observations are indexed by signed integers, and
on a typical PC these will be 32-bit values, capable of representing a maximum positive value of
231 − 1 = 2 _,_ 147 _,_ 483 _,_ 647.

The limits mentioned above apply to gretl’s “native” functionality. There are tighter limits with
regard to two third-party programs that are available as add-ons to gretl for certain sorts of time-
series analysis including seasonal adjustment, namely TRAMO/SEATS and X-12-ARIMA. These pro-
grams employ a fixed-size memory allocation, and can’t handle series of more than 600 observa-
tions.


Chapter 4. Data files 29

### 4.8 Data file collections

If you’re using gretl in a teaching context you may be interested in adding a collection of data files
and/or scripts that relate specifically to your course, in such a way that students can browse and
access them easily.

There are three ways to access such collections of files:

- For data files: select the menu item “File, Open data, Sample file”, or click on the folder icon
    on the gretl toolbar.
- For script files: select the menu item “File, Script files, Example scripts”.

When a user selects one of the items:

- The data or script files included in the gretl distribution are automatically shown (this includes
    files relating to Ramanathan’s _Introductory Econometrics_ and Greene’s _Econometric Analysis_ ).
- The program looks for certain known collections of data files available as optional extras,
    for instance the datafiles from various econometrics textbooks (Davidson and MacKinnon,
    Gujarati, Stock and Watson, Verbeek, Wooldridge) and the Penn World Table (PWT 5.6). (See
    the data page at the gretl website for information on these collections.) If the additional files
    are found, they are added to the selection windows.
- The program then searches for valid file collections (not necessarily known in advance) in
    these places: the “system” data directory, the system script directory, the user directory,
    and all first-level subdirectories of these. For reference, typical values for these directories
    are shown in Table 4.1. (Note that PERSONAL is a placeholder that is expanded by Windows,
    corresponding to “My Documents” on English-language systems.)

```
Linux MS Windows
system data dir /usr/share/gretl/data c:\Program Files\gretl\data
system script dir /usr/share/gretl/scripts c:\Program Files\gretl\scripts
user dir $HOME/gretl PERSONAL\gretl
```
```
Table 4.1: Typical locations for file collections
```
Any valid collections will be added to the selection windows. So what constitutes a valid file collec-
tion? This comprises either a set of data files in gretl XML format (with the .gdt suffix) or a set of
script files containing gretl commands (with .inp suffix), in each case accompanied by a “master
file” or catalog. The gretl distribution contains several example catalog files, for instance the file
descriptions in the misc sub-directory of the gretl data directory and ps_descriptions in the
misc sub-directory of the scripts directory.

If you are adding your own collection, data catalogs should be named descriptions and script
catalogs should be be named ps_descriptions (in each case, with no suffix). The catalog file
should be placed (along with the associated data or script files) in its own sub-directory (e.g. /usr/
share/gretl/data/mydata or c:\Program Files\gretl\data\mydata).

The catalog files are plain text (encoded as UTF-8 if they contain any non-ASCII characters). The
syntax of such files is straightforward. Here, for example, are the first few lines of gretl’s “misc”
data catalog:

```
# Gretl: various illustrative datafiles
"abdata","Arellano and Bond (1991) panel data","panel, T=9 N=140"
"anscombe","Anscombe’s Quartet (artificial data)","cross section, n=11"
"arma","Artificial data for ARMA script example","time series, T=624"
"australia","Johansen’s Australian macroeconomic data","time series, T=77"
```

Chapter 4. Data files 30

The first line, which must start with a hash mark followed by a space, contains a short name (not
to exceed 23 bytes) — here Gretl — which will appear as the label for this collection’s tab in the
data browser window, terminated by a colon and optionally followed by a brief description of the
collection as a whole.

Each subsequent line should contain three elements, wrapped in upright double quotes and sepa-
rated by commas, as follows:

1. The name of a data file, not to exceed 23 characters (leave off the .gdt suffix here).
2. A short description of the content of the datafile, not to exceed 79 bytes.
3. A stylized record of the structure (cross section, time series or panel) and length of the dataset
    (see the examples from the Gretl collection above).

There should be one such line for each data file in the collection.

A script catalog file looks very similar. Again there are three fields in the per-file lines: a filename
(without its .inp suffix); a brief account of the econometric point illustrated in the script; and a
brief indication of the nature of the data used. Again, here are the first few lines of the supplied
“misc” script catalog:

```
# Gretl: various sample scripts
"arbond91","Dynamic panel model (GMM-DIF)","UK employment data"
"armaloop","ARMA using command loop","artificial data"
"auto_arima","Automatic ARIMA model selection","artificial data"
"bbond98","Dynamic panel model (GMM-SYS)","UK employment data"
"biprobit","Bivariate probit (William Greene)","credit rating"
```
If you want to make your own data collection available to users, these are the steps:

1. Assemble the data, in whatever format is convenient.
2. Convert the data to gretl format and save as gdt files. It is probably easiest to convert the data
    by importing them into the program from plain text, CSV, or a spreadsheet format (MS Excel
    or Gnumeric) then saving them. You may wish to add descriptions of the individual variables
    (the “Variable, Edit attributes” menu item), and add information on the source of the data (the
    “Data, Dataset info” menu item).
3. Write a catalog file for the collection using a text editor.
4. Put the data files plus the catalog file in a subdirectory of the gretl data directory (or per-user
    directory).
5. If the collection is to be distributed to other people, package the data files and catalog in some
    suitable manner, e.g. as a zipfile.

If you assemble such a collection, and the data are not proprietary, we would encourage you to
submit the collection for packaging as a gretl optional extra.

### 4.9 Assembling data from multiple sources

In many contexts researchers need to bring together data from multiple source files, and in some
cases these sources are not organized such that the data can simply be “stuck together” by append-
ing rows or columns to a base dataset. In gretl, the join command can be used for this purpose;
this command is discussed in detail in chapter 7.


## Chapter 5

Sub-sampling a dataset

### 5.1 Introduction

Some subtle issues can arise here; this chapter attempts to explain the issues.

A sub-sample may be defined in relation to a full dataset in two different ways: we will refer to these
as “setting” the sample and “restricting” the sample; these methods are discussed in sections 5.2
and 5.3 respectively. In addition section 5.4 discusses some special issues relating to panel data,
and section 5.5 covers resampling with replacement, which is useful in the context of bootstrapping
test statistics.

The following discussion focuses on the command-line approach. But you can also invoke the
methods outlined here via the items under the Sample menu in the GUI program.

### 5.2 Setting the sample

By “setting” the sample we mean defining a sub-sample simply by means of adjusting the starting
and/or ending point of the current sample range. This is likely to be most relevant for time-series
data. For example, one has quarterly data from 1960:1 to 2003:4, and one wants to run a regression
using only data from the 1970s. A suitable command is then

```
smpl 1970:1 1979:4
```
Or one wishes to set aside a block of observations at the end of the data period for out-of-sample
forecasting. In that case one might do

```
smpl ; 2000:4
```
where the semicolon is shorthand for “leave the starting observation unchanged”. (The semicolon
may also be used in place of the second parameter, to mean that the ending observation should be
unchanged.) By “unchanged” here, we mean unchanged relative to the last smpl setting, or relative
to the full dataset if no sub-sample has been defined up to this point. For example, after

```
smpl 1970:1 2003:4
smpl ; 2000:4
```
the sample range will be 1970:1 to 2000:4.

An incremental or relative form of setting the sample range is also supported. In this case a relative
offset should be given, in the form of a signed integer (or a semicolon to indicate no change), for
both the starting and ending point. For example

```
smpl +1 ;
```
will advance the starting observation by one while preserving the ending observation, and

```
smpl +2 -1
```
#### 31


Chapter 5. Sub-sampling a dataset 32

will both advance the starting observation by two and retard the ending observation by one.

An important feature of “setting” the sample as described above is that it necessarily results in
the selection of a subset of observations that are contiguous in the full dataset. The structure of
the dataset is therefore unaffected (for example, if it is a quarterly time series before setting the
sample, it remains a quarterly time series afterwards).

### 5.3 Restricting the sample

By “restricting” the sample we mean selecting observations on the basis of some Boolean (logical)
criterion, or by means of a random number generator. This is likely to be most relevant for cross-
sectional or panel data.

Suppose we have data on a cross-section of individuals, recording their gender, income and other
characteristics. We wish to select for analysis only the women. If we have a male dummy variable
with value 1 for men and 0 for women we could do

```
smpl male==0 --restrict
```
to this effect. Or suppose we want to restrict the sample to respondents with incomes over $50,000.
Then we could use

```
smpl income>50000 --restrict
```
A question arises: if we issue the two commands above in sequence, what do we end up with in
our sub-sample: all cases with income over 50000, or just women with income over 50000? By
default, the answer is the latter: women with income over 50000. The second restriction augments
the first, or in other words the final restriction is the logical product of the new restriction and any
restriction that is already in place. If you want a new restriction to replace any existing restrictions
you can first recreate the full dataset using

```
smpl --full
```
Alternatively, you can add the replace option to the smpl command:

```
smpl income>50000 --restrict --replace
```
This option has the effect of automatically re-establishing the full dataset before applying the new
restriction.

Unlike a simple “setting” of the sample, “restricting” the sample may result in selection of non-
contiguous observations from the full data set. It may therefore change the structure of the data
set.

This can be seen in the case of panel data. Say we have a panel of five firms (indexed by the variable
firm) observed in each of several years (identified by the variable year). Then the restriction

```
smpl year==1995 --restrict
```
produces a dataset that is not a panel, but a cross-section for the year 1995. Similarly

```
smpl firm==3 --restrict
```
produces a time-series dataset for firm number 3.

For these reasons (possible non-contiguity in the observations, possible change in the structure of
the data), gretl acts differently when you “restrict” the sample as opposed to simply “setting” it. In


Chapter 5. Sub-sampling a dataset 33

the case of setting, the program merely records the starting and ending observations and uses these
as parameters to the various commands calling for the estimation of models, the computation of
statistics, and so on. In the case of restriction, the program makes a reduced copy of the dataset
and by default treats this reduced copy as a simple, undated cross-section — but see the further
discussion of panel data in section 5.4.

If you wish to re-impose a time-series interpretation of the reduced dataset you can do so using the
setobs command, or the GUI menu item “Data, Dataset structure”.

The fact that “restricting” the sample results in the creation of a reduced copy of the original
dataset may raise an issue when the dataset is very large. With such a dataset in memory, the
creation of a copy may lead to a situation where the computer runs low on memory for calculating
regression results. You can work around this as follows:

1. Open the full data set, and impose the sample restriction.
2. Save a copy of the reduced data set to disk.
3. Close the full dataset and open the reduced one.
4. Proceed with your analysis.

Random sub-sampling

Besides restricting the sample on some deterministic criterion, it may sometimes be useful (when
working with very large datasets, or perhaps to study the properties of an estimator) to draw a
random sub-sample from the full dataset. This can be done using, for example,

```
smpl 100 --random
```
to select 100 cases. If you want the sample to be reproducible, you should set the seed for the
random number generator first, using the set command. This sort of sampling falls under the
“restriction” category: a reduced copy of the dataset is made.

### 5.4 Panel data

Consider for concreteness the Arellano–Bond dataset supplied with gretl (abdata.gdt). This com-
prises data on 140 firms _(n_ = 140) observed over the years 1976–1984 _(T_ = 9 _)_. The dataset is
“nominally balanced” in the sense that that the time-series length is the same for all countries (this
being a requirement for a dataset to count as a panel in gretl), but in fact there are many missing
values (NAs).

You may want to sub-sample such a dataset in either the cross-sectional dimension (limit the sam-
ple to a subset of firms) or the time dimension (e.g. use data from the 1980s only). One way to
sub-sample on firms keys off the notation used by gretl for panel observations. The full data range
is printed as 1:1 (firm 1, period 1) to 140:9 (firm 140, period 9). The effect of

```
smpl 1:1 80:9
```
is to limit the sample to the first 80 firms. Note that if you instead tried smpl 1:1 80:4 this would
provoke an error: you cannot use this syntax to sub-sample in the time dimension of the panel.
Alternatively, and perhaps more naturally, you can use the --unit option with the smpl command
to limit the sample in the cross-sectional dimension, as in

```
smpl 1 80 --unit
```
The firms in the Arellano–Bond dataset are anonymous, but suppose you had a panel with five
named countries. With such a panel you can inform gretl of the names of the groups using the
setobs command. For example, given


Chapter 5. Sub-sampling a dataset 34

```
string cstr = "Portugal Italy Ireland Greece Spain"
setobs country cstr --panel-groups
```
gretl creates a string-valued series named country with group names taken from the variable cstr.
Then, to include only Italy and Spain you could do

```
smpl country=="Italy" || country=="Spain" --restrict
```
or to exclude one country,

```
smpl country!="Ireland" --restrict
```
Sub-sampling a panel in the time dimension can be done via --restrict. For example, the
Arellano–Bond dataset contains a variable named YEAR that records the year of the observations
and if one wanted to omit the first two years of data one could do

```
smpl YEAR >= 1978 --restrict
```
If a dataset does not already incude a suitable variable for this purpose one can use the command
genr time to create a simple 1-based time index.

Another way to sub-sample in the time dimension of a panel starts with a specification of time via
the setobs command, as in

```
setobs 1 1976 --panel-time
```
This tells gretl that panel-time is annual (frequency 1), starting in 1976. (In fact this is already done
for abdata.gdt.) Then to restrict the sample range to 1979–1982 you can do

```
smpl 1979 1982 --time
```
Note that if you apply a sample restriction that just selects certain units (firms, countries or what-
ever), or selects certain contiguous time-periods — such that _n >_ 1, _T >_ 1 and the time-series length
is still the same across all included units — your sub-sample will still be interpreted by gretl as a
panel.

Unbalancing restrictions

In some cases one wants to sub-sample according to a criterion that “cuts across the grain” of
a panel dataset. For instance, suppose you have a micro dataset with thousands of individuals
observed over several years and you want to restrict the sample to observations on employed
women.

If we simply extracted from the total _nT_ rows of the dataset those that pertain to women who were
employed at time _t (t_ = 1 _,...,T)_ we would likely end up with a dataset that doesn’t count as a
panel in gretl (because the specific time-series length, _Ti_ , would differ across individuals). In some
contexts it might be OK that gretl doesn’t take your sub-sample to be a panel, but if you want to
apply panel-specific methods this is a problem. You can solve it by giving the --preserve-panel
option with smpl. For example, supposing your dataset contained dummy variables gender (with
the value 1 coding for women) and employed, you could do

```
smpl gender==1 && employed==1 --restrict --preserve-panel
```
What exactly does this do? Well, let’s say the years of your data are 2000, 2005 and 2010, and
that some women were employed in all of those years, giving a maximum _Ti_ value of 3. But in-
dividual 526 is a woman who was employed only in the year 2000 ( _Ti_ = 1). The effect of the
--preserve-panel option is then to insert “padding rows” of NAs for the years 2005 and 2010 for
individual 526, and similarly for all individuals with 0 _< Ti<_ 3. Your sub-sample then qualifies as
a panel.


Chapter 5. Sub-sampling a dataset 35

### 5.5 Resampling and bootstrapping

Given an original data series x, the command

```
series xr = resample(x)
```
creates a new series each of whose elements is drawn at random from the elements of x. If the
original series has 100 observations, each element of x is selected with probability 1 _/_ 100 at each
drawing. Thus the effect is to “shuffle” the elements of x, with the twist that each element of x may
appear more than once, or not at all, in xr.

The primary use of this function is in the construction of bootstrap confidence intervals or p-values.
Here is a simple example. Suppose we estimate a simple regression of _y_ on _x_ via OLS and find that
the slope coefficient has a reported _t_ -ratio of _t_ 0 with _ν_ degrees of freedom. A two-tailed p-value
for the null hypothesis that the slope parameter equals zero can then be found using the _t(ν)_
distribution. Depending on the context, however, we may doubt whether the ratio of coefficient to
standard error truly follows the _t(ν)_ distribution. In that case we could derive a bootstrap p-value
as shown in Listing 5.1.

Under the null hypothesis that the slope with respect to _x_ is zero, _y_ is simply equal to its mean plus
an error term. We simulate _y_ by resampling the residuals from the initial OLS and re-estimate the
model. We repeat this procedure a large number of times, and record the number of cases where
the absolute value of the _t_ -ratio is greater than _t_ 0 : the proportion of such cases is our bootstrap
p-value. For a good discussion of simulation-based tests and bootstrapping, see Davidson and
MacKinnon (2004, chapter 4); Davidson and Flachaire (2001) is also instructive.

```
Listing 5.1: Calculation of bootstrap p-value [Download▼]
```
nulldata 50
set seed 54321
series x = normal()
series y = 10 + x + 2*normal()
ols y 0 x
# the reported t-stat
t0 = abs($coeff[2] / $stderr[2])
# save the residuals
series u = $uhat
scalar ybar = mean(y)
# number of replications for bootstrap
scalar B = 1000
scalar tcount = 0
series ysim
loop B
# generate simulated y by resampling
ysim = ybar + resample(u)
ols ysim 0 x --quiet
scalar tsim = abs($coeff[2] / $stderr[2])
tcount += (tsim > t0)
endloop
printf "proportion of cases with |t| > %.3f = %g\n", t0, tcount / B


## Chapter 6

Graphics

### 6.1 Gnuplot graphs

A separate program, gnuplot, is called to generate graphs. Gnuplot is a very full-featured graphing
program with myriad options. It is available from [http://www.gnuplot.info](http://www.gnuplot.info) (but note that a suitable copy
of gnuplot is bundled with the packaged versions of gretl for MS Windows and Mac OS X). Gretl
gives you direct access, via a graphical interface, to a subset of gnuplot’s options and it tries to
choose sensible values for you; it also allows you to take complete control over graph details if you
wish.

With a graph displayed, you can right-click on the graph window (or use the “hamburger” toolbar
button) for a pop-up menu with the following options.

- Save as PNG: Save the graph in Portable Network Graphics format (the same format that you
    see on screen).
- Save as postscript (EPS): Save in encapsulated postscript format.
- Save as PDF: Save in PDF format.
- Save as Windows metafile: Save in Enhanced Metafile (EMF) format (with color and monochrome
    options).
- Copy to clipboard: with color and monochrome options.
- Save to session as icon: The graph will appear in iconic form when you select “Icon view” from
    the View menu.
- Zoom: Lets you select an area within the graph for closer inspection (not available for all
    graphs).
- Display PDF: view a PDF version of the graph.
- Edit: Opens a controller for the plot which lets you adjust many aspects of its appearance.
- Close: Closes the graph window.

If you select Save as postscript or Save as PDF you get a dialog box that lets you adjust several
aspects of the graph, and also preview the result.

Displaying data labels

For simple X-Y scatter plots, some further options are available if the dataset includes “case mark-
ers” (that is, labels identifying each observation).^1 With a scatter plot displayed, when you move
the mouse pointer over a data point its label is shown on the graph. By default these labels are
transient: they do not appear in the printed or copied version of the graph. They can be removed by
selecting “Clear data labels” from the graph pop-up menu. If you want the labels to be affixed per-
manently (so they will show up when the graph is printed or copied), select the option “Freeze data

(^1) For an example of such a dataset, see the Ramanathan file data4-10: this contains data on private school enrollment
for the 50 states of the USA plus Washington, DC; the case markers are the two-letter codes for the states.

#### 36


Chapter 6. Graphics 37

labels” from the pop-up menu; “Clear data labels” cancels this operation. The other label-related
option, “All data labels”, requests that case markers be shown for all observations. At present the
display of case markers is disabled for graphs containing more than 250 data points.

GUI plot editor

Selecting the Edit option in the graph popup menu opens an editing dialog box, shown in Figure 6.1.
Notice that there are several tabs, allowing you to adjust many aspects of a graph’s appearance:
font, title, axis scaling, line colors and types, and so on. You can also add lines or descriptive labels
to a graph (under the Lines and Labels tabs). The “Apply” button applies your changes without
closing the editor; “OK” applies the changes and closes the dialog.

```
Figure 6.1: gretl’s plot controller
```
Publication-quality graphics: advanced options

The GUI plot editor has two limitations. First, it cannot represent all the myriad options that
gnuplot offers. Users who are sufficiently familiar with gnuplot to know what they’re missing in
the plot editor presumably don’t need much help from gretl, so long as they can get hold of the
gnuplot command file that gretl has put together. Second, even if the plot editor meets your needs,
in terms of fine-tuning the graph you see on screen, a few details may need further work in order
to get optimal results for publication.

Either way, the first step in advanced tweaking of a graph is to get access to the graph command
file.

- In the graph display window, right-click and choose “Save to session as icon”.


Chapter 6. Graphics 38

- If it’s not already open, open the icon view window — either via the menu item View/Icon view,
    or by clicking the “session icon view” button on the main-window toolbar.
- Right-click on the icon representing the newly added graph and select “Edit plot commands”
    from the pop-up menu.
- You get a window displaying the plot file (Figure 6.2).

```
Figure 6.2: Plot commands editor
```
Here are the basic things you can do in this window. Obviously, you can edit the file you just
opened. You can also send it for processing by gnuplot, by clicking the “Execute” (cogwheel) icon
in the toolbar. Or you can use the “Save as” button to save a copy for editing and processing as you
wish. And please note that the Help button on the toolbar (a lifebelt in Figure 6.2) gives you access
to the gnuplot manual.

One relatively simple editorial job would be to set a chosen driver (or “terminal” in gnuplot par-
lance) and output filename. For example, to get PDF output you could insert lines like the following
at the top:

```
# PDF, slightly amended (the default size is 5in x 3in)
set term pdfcairo font "Sans,6" size 5in,3.5in
set output ’mygraph1.pdf’
# or small size
set term pdfcairo font "Sans,5" size 3in,2in
set output ’mygraph2.pdf’
# or with size given in centimeters
set term pdfcairo font "Sans,6" size 6cm,4.2cm
set output ’mygraph3.pdf’
```

Chapter 6. Graphics 39

Or substitute epscairo for pdfcairo (and change the filenames) if you want EPS output. However,
such changes may be more easily made via the Save as PDF and Save as postscript options in the
plot menu.^2

The real payoff to editing the plot code can be obtained if you dive into the details and employ
gnuplot features that are not accessible via gretl, and/or use one of the terminal types not directly
supported by gretl, such as context (ConTeXt), mp (MetaPost), lua (Lua) or pslatex (LATEX picture
environment with PostScript specials). The lua terminal with the tikz option is especially useful
for LATEX users, because it produces a tikzpicture environment, which offers almost unlimited
customization possibilities (note that in order to use plots produced in this way you’ll also need
the gnuplot-lua-tikz LATEX package).

To find out more about gnuplot visit gnuplot.sourceforge.net. This site has documentation for the
current version of the program in various formats along with a large collection of demonstration
plots.

Additional tips

To be written. Line widths, enhanced text. Show a “before and after” example.

### 6.2 Plotting graphs from scripts

When working with scripts, you may want to have a graph shown onto your display or saved into a
file. In fact, if in your usual workflow you find yourself creating similar graphs over and over again,
you might want to consider the option of writing a script which automates this process for you.
gretl gives you two main tools for doing this: one is a command called gnuplot, whose main use
is to create standard plot quickly. The other one is the plot command block, which has a more
elaborate syntax but offers you more control on output.

The **gnuplot** command

The gnuplot command is described at length in the _Gretl Command Reference_ and the online help
system. Here, we just summarize its main features: basically, it consists of the gnuplot keyword,
followed by a list of items, telling the command _what_ you want plotted and a list of options, telling
it _how_ you want it plotted.

For example, the line

```
gnuplot y1 y2 x
```
will give you a basic XY plot of the two series y1 and y2 on the vertical axis versus the series x on
the horizontal axis. In general, the arguments to the gnuplot command is a list of series, the last
of which goes on the x-axis, while all the other ones go onto the y-axis. By default, the gnuplot
command gives you a scatterplot. If you just have one variable on the y-axis, then gretl will also
draw a the OLS interpolation, if the fit is good enough.^3

Several aspects of the behavior described above can be modified. You do this by appending options
to the command. Most options can be broadly grouped in three categories:

1. Plot styles: we support points (the default choice), lines, lines and points together, and im-
    pulses (vertical lines).
2. Algorithm for the fitted line: here you can choose between linear, quadratic and cubic inter-
    polation, but also more exotic choices, such as semi-log, inverse or loess (non-parametric). Of
    course, you can also turn this feature off.

(^2) A “traditional” postscript terminal may also be available in gnuplot, with an eps option. The defaults in this case
are quite different from epscairo, and to make use of the alternative you’ll have to consult the gnuplot manual.
(^3) The technical condition for this is that the two-tailed _p_ -value for the slope coefficient should be under 10%.


Chapter 6. Graphics 40

```
Listing 6.1: Plotting macroeconomic data
```
open AWM.gdt --quiet

# --- consumption and income, different styles ------------

gnuplot PCR YER
gnuplot PCR YER --output=display
gnuplot PCR YER --output=display --time-series
gnuplot PCR YER --output=display --time-series --with-lines

# --- Phillips’ curve, different fitted lines -------------

gnuplot INFQ URX --output=display
gnuplot INFQ URX --fit=none --output=display
gnuplot INFQ URX --fit=inverse --output=display
gnuplot INFQ URX --fit=loess --output=display

3. Input and output: you can choose whether you want your graph on your computer screen
    (and possibly use the in-built graphical widget to further customize it — see above, page 37),
    or rather save it to a file. We support several graphical formats, among which PNG and PDF,
    to make it easy to incorporate your plots into text documents.

Listing 6.1 shows examples of some traditional plots in macroeconomics, using time series from
the “area-wide model” dataset produced by the European Central Bank, which is shipped with gretl
in the file AWM.gdt. PCR is aggregate private real consumption and YER is real GDP.

The first command line in the listing plots consumption against income as a kind of Keynesian
consumption function. More precisely, it produces a simple scatter plot with an automatically
linear fitted line. If this is executed in the gretl console the plot will be directly shown in a new
window, but if this line is contained in a script then instead a file with the plot commands will be
saved for later execution. The second example line changes this behavior for a script command
and forces the plot to be shown directly.

The third line instead asks for a plot of the two variables as two separate curves against time on
the x-axis. Each observation point is drawn separately with a certain symbol determined by gnuplot
defaults. If you add the option --with-lines the points will be connected with a continuous line
and the symbols omitted.

The second batch of examples demonstrate how the fitted line in the scatter plot can be controlled
from gretl’s side. The option --fit=none overrides gnuplot’s default to draw a line if it deems the
fit to be “good enough”. The effect of --fit=inverse is to consider the variable on the y-axis as a
function of 1 _/X_ instead of _X_ and draw the corresponding hyperbolic branch. For the workings of
a Loess fit (locally-weighted polynomial regression) please refer to the documentation of the loess
function.

For more detail, consult the _Gretl Command Reference_.

The **plot** command block

The plot environment is a way to pass information to Gnuplot in a more structured way, so that
customization of basic plots becomes easier. It has the following characteristics:

The block starts with the plot keyword, followed by a required parameter: the name of a list, a
single series or a matrix. This parameter specifies the data to be plotted. The starting line may be


Chapter 6. Graphics 41

prefixed with the savename <- apparatus to save a plot as an icon in the GUI program. The block
ends with end plot.

Inside the block you have zero or more lines of these types, identified by an initial keyword:

option: specify a single option (details below)

options: specify multiple options on a single line; if more than one option is given on a line, the
options should be separated by spaces.

literal: a command to be passed to gnuplot literally

printf: a printf statement whose result will be passed to gnuplot literally; this allows the use of
string variables without having to resort to @-style string substitution.

The options available are basically those of the current gnuplot command, but with a few dif-
ferences. For one thing you don’t need the leading double-dash in an "option" (or "options") line.
Besides that,

- You can’t use the option --matrix=whatever with plot: that possibility is handled by pro-
    viding the name of a matrix on the initial plot line.
- The --input=filename option is not supported: use gnuplot for the case where you’re
    supplying the entire plot specification yourself.
- The several options pertaining to the presence and type of a fitted line, are replaced in plot
    by a single option fit which requires a parameter. Supported values for the parameter are:
    none, linear, quadratic, cubic, inverse, semilog and loess. Example:

```
option fit=quadratic
```
As with gnuplot, the default is to show a linear fit in an X-Y scatter if it’s significant at the 10
percent level.

Here’s a simple example, the plot specification from the “bandplot” package, which shows how
to achieve the same result via the gnuplot command and a plot block, respectively — the latter
occupies a few more lines but is clearer

```
gnuplot 1 2 3 4 --with-lines --matrix=plotmat \
--fit=none --output=display \
{ set linetype 3 lc rgb "#0000ff"; set title "@title"; \
set nokey; set xlabel "@xname"; }
```
```
plot plotmat
options with-lines fit=none
literal set linetype 3 lc rgb "#0000ff"
literal set nokey
printf "set title \"%s\"", title
printf "set xlabel \"%s\"", xname
end plot --output=display
```
Note that --output=display is appended to end plot; also note that if you give a matrix to plot
it’s assumed you want to plot all the columns. In addition, if you give a single series and the dataset
is time series, it’s assumed you want a time-series plot.


Chapter 6. Graphics 42

```
Listing 6.2: Plotting the log wage from the Mroz example dataset [Download▼]
```
set verbose off
open mroz87.gdt --quiet

series lWW = log(WW)
scalar m = mean(lWW)
scalar s = sd(lWW)

###
### prepare matrix with data for plot
###

# number of valid observations
scalar n = nobs(lWW)
# discretize log wage
scalar k = 4
series disc_lWW = round(lWW*k)/k
# get frequencies
matrix f = aggregate(null, disc_lWW)
# add density
phi = dnorm((f[,1] - m)/s) / (s*k)
# put columns together and add labels
plotmat = f[,2]./n ~ phi ~ f[,1]
strings cnames = defarray("frequency", "density", "log wage")
cnameset(plotmat, cnames)

###
### create plot
###

plot plotmat
# move legend
literal set key outside rmargin
# set line style
literal set linetype 2 dashtype 2 linewidth 2
# set histogram color
literal set linetype 1 lc rgb "#777777"
# set histogram style
literal set style fill solid 0.25 border
# set histogram width
printf "set boxwidth %4.2f\n", 0.5/k
options with-lines=2 with-boxes=1
end plot --output=display


Chapter 6. Graphics 43

_Example: Plotting an histogram together with a density_

Listing 6.2 contains a slightly more elaborate example: here we load the Mroz example dataset and
calculate the log of the individual’s wage. Then, we match the histogram of a discretized version
of the same variable (obtained via the aggregate() function) versus the theoretical density if data
were Gaussian.

There are a few points to note:

- The data for the plot are passed through a matrix in which we set column names via the
    cnameset function; those names are then automatically used by the plot environment.
- In this example, we make extensive use of the set literal construct for refining the plot by
    passing instruction to gnuplot; the power of gnuplot is impossible to overstate. We encourage
    you to visit the “demos” version of gnuplot’s website (http://gnuplot.sourceforge.net/)
    and revel in amazement.
- In the plot environment you can use all the quantities you have in your script. This is the
    way we calibrate the histogram width (try setting the scalar k in the script to different values).
    Note that the printf command has a special meaning inside a plot environment.
- The script displays the plot on your screen. If you want to save it to a file instead, replace
    --output=display at the end with --output= _filename_.
- It’s OK to insert comments in the plot environment; actually, it’s a rather good idea to com-
    ment as much as possible (as always)!

The output from the script is shown in Figure 6.3.

```
0
```
```
0.02
```
```
0.04
```
```
0.06
```
```
0.08
```
```
0.1
```
```
0.12
```
```
0.14
```
```
0.16
```
```
0.18
```
```
-2 -1 0 1 2 3
log wage
```
```
frequency
density
```
```
Figure 6.3: Output from listing 6.2
```
_Example: Plotting Student’s t densities_

The power of the printf statement in a plot block becomes apparent when used jointly with
user-defined functions, as exemplified in Listing 6.3, in which we create a plot showing the den-
sity functions of Student’s _t_ distribution for three different settings of the “degrees of freedom”


Chapter 6. Graphics 44

```
Listing 6.3: Plotting t densities for varying degrees of freedom [Download▼]
```
set verbose off

function string tplot(scalar m)
return sprintf("stud(x,%d) title \"t(%d)\"", m, m)
end function

matrix dfs = {2, 4, 16}

plot
literal set xrange [-4.5:4.5]
literal set yrange [0:0.45]
literal Binv(p,q) = exp(lgamma(p+q)-lgamma(p)-lgamma(q))
literal stud(x,m) = Binv(0.5*m,0.5)/sqrt(m)*(1.0+(x*x)/m)**(-0.5*(m+1.0))
printf "plot %s, %s, %s", tplot(dfs[1]), tplot(dfs[2]), tplot(dfs[3])
end plot --output=display

parameter (note that plotting a _t_ density is very easy to do from the GUI: just go to the _Tools >
Distribution graphs_ menu).

First we define a user function called tplot, which returns a string with the ingredients to pass
to the gnuplot plot statement, as a function of a scalar parameter (the degrees of freedom in our
case). Next, this function is used within the plot block to plot the appropriate density. Note that
most of the statements to mathematically define the function to plot are outsourced to gnuplot via
the literal command.

The output from the script is shown in Figure 6.4.

```
0
```
```
0.05
```
```
0.1
```
```
0.15
```
```
0.2
```
```
0.25
```
```
0.3
```
```
0.35
```
```
0.4
```
```
0.45
```
```
-4 -3 -2 -1 0 1 2 3 4
```
```
t(2)
t(4)
t(16)
```
```
Figure 6.4: Output from listing 6.3
```

Chapter 6. Graphics 45

### 6.3 Boxplots

These plots (after Tukey and Chambers) display the distribution of a variable. Its shape depends
on a few quantities, defined as follows:

```
x min sample minimum
Q 1 first quartile
m median
x ̄ mean
Q 3 third quartile
x max sample maximum
R = Q 3 − Q 1 interquartile range
```
The central box encloses the middle 50 percent of the data, i.e. goes from _Q_ 1 to _Q_ 3 ; therefore, its
height equals _R_. A line is drawn across the box at the median _m_ and a “+” sign identifies the mean
_x_ ̄.

The length of the “whiskers” depends on the presence of outliers. The top whisker extends from
the top of the box up to a maximum of 1.5 times the interquartile range, but can be shorter if the
sample maximum is lower than that value; that is, it reaches min _[x_ max _,Q_ 3 + 1_._ 5 _R]_. Observations
larger than _Q_ 3 + 1_._ 5 _R_ , if any, are considered outliers and represented individually via dots.^4 The
bottom whisker obeys the same logic, with obvious adjustments. Figure 6.5 provides an example
of all this by using the variable FAMINC from the sample dataset mroz87.

#### 0

#### 20000

#### 40000

#### 60000

#### 80000

#### FAMINC

```
Q 3 x ̄
```
#### Q 1

```
m
```
```
x min
```
```
x max
```
```
outliers
```
```
Figure 6.5: Sample boxplot
```
In the case of boxplots with confidence intervals, dotted lines show the limits of an approximate 90

(^4) To give you an intuitive idea, if a variable is normally distributed, the chances of picking an outlier by this definition
are slightly below 0.7%.


Chapter 6. Graphics 46

percent confidence interval for the median. This is obtained by the bootstrap method, which can
take a while if the data series is very long. For details on constructing boxplots, see the entry for
boxplot in the _Gretl Command Reference_ or use the Help button that appears when you select one
of the boxplot items under the menu item “View, Graph specified vars” in the main gretl window.

Factorized boxplots

A nice feature which is quite useful for data visualization is the conditional, or factorized boxplot.
This type of plot allows you to examine the distribution of a variable conditional on the value of
some discrete factor.

As an example, we’ll use one of the datasets supplied with gretl, that is rac3d, which contains an
example taken from Cameron and Trivedi (2013) on the health conditions of 5190 people. The
script below compares the unconditional (marginal) distribution of the number of illnesses in the
past 2 weeks with the distribution of the same variable, conditional on age classes.

open rac3d.gdt
# unconditional boxplot
boxplot ILLNESS --output=display
# create a discrete variable for age class:
# 0 = below 20, 1 = between 20 and 39, etc
series age_class = floor(AGE/0.2)
# conditional boxplot
boxplot ILLNESS age_class --factorized --output=display

After running the code above, you should see two graphs similar to Figure 6.6. By comparing the
marginal plot to the factorized one, the effect of age on the mean number of illnesses is quite
evident: by joining the green crosses you get what is technically known as the conditional mean
function, or regression function if you prefer.

```
0
```
```
1
```
```
2
```
```
3
```
```
4
```
```
5
```
```
ILLNESS
```
```
0
```
```
1
```
```
2
```
```
3
```
```
4
```
```
5
```
```
0 1 2 3
```
```
ILLNESS
```
```
age_class
```
```
Distribution of ILLNESS by age_class
```
```
Figure 6.6: Conditional and unconditional distribution of illnesses
```

## Chapter 7

Joining data sources

### 7.1 Introduction

Gretl provides two commands for adding data from file to an existing dataset in the program’s
workspace, namely append and join. The append command, which has been available for a long
time, is relatively simple and is described in the _Gretl Command Reference_. Here we focus on the
join command, which is much more flexible and sophisticated. This chapter gives an overview
of the functionality of join along with a detailed account of its syntax and options. We provide
several toy examples and discuss one real-world case at length.

First, a note on terminology: in the following we use the terms “left-hand” and “inner” to refer
to the dataset that is already in memory, and the terms “right-hand” and “outer” to refer to the
dataset in the file from which additional data are to be drawn.

Two main features of join are worth emphasizing at the outset:

- “Key” variables can be used to match specific observations (rows) in the inner and outer
    datasets, and this match need not be 1 to 1.
- A row filter may be applied to screen out unwanted observations in the outer dataset.

As will be explained below, these features support rather complex concatenation and manipulation
of data from different sources.

A further aspect of join should be noted — one that makes this command particularly useful when
dealing with very large data files. That is, when gretl executes a join operation it does not, in gen-
eral, read into memory the entire content of the right-hand side dataset. Only those columns that
are actually needed for the operation are read in full. This makes join faster and less demanding
of computer memory than the methods available in most other software. On the other hand, gretl’s
asymmetrical treatment of the “inner” and “outer” datasets in join may require some getting used
to, for users of other packages.

### 7.2 Basic syntax

The minimal invocation of join is

```
join filename varname
```
where _filename_ is the name of a data file and _varname_ is the name of a series to be imported.
Only two sorts of data file are supported at present: delimited text files (where the delimiter may
be comma, space, tab or semicolon) and “native” gretl data files (gdt or gdtb). A series named
_varname_ may already be present in the left-hand dataset, but that is not required. The series to be
imported may be numerical or string-valued. For most of the discussion below we assume that just
a single series is imported by each join command, but see section 7.7 for an account of multiple
imports.

The effect of the minimal version of join is this: gretl looks for a data column labeled _varname_ in
the specified file; if such a column is found and the number of observations on the right matches
the number of observations in the current sample range on the left, then the values from the right
are copied into the relevant range of observations on the left. If _varname_ does not already exist

#### 47


Chapter 7. Joining data sources 48

on the left, any observations outside of the current sample are set to NA; if it exists already then
observations outside of the current sample are left unchanged.

The case where you want to rename a series on import is handled by the --data option. This option
has one required argument, the name by which the series is known on the right. At this point we
need to explain something about right-hand variable names (column headings).

Right-hand names

We accept on input arbitrary column heading strings, but if these strings do not qualify as valid
gretl identifiers they are automatically converted, and in the context of join you must use the
converted names. A gretl identifier must start with a letter, contain nothing but (ASCII) letters,
digits and the underscore character, and must not exceed 31 characters. The rules used in name
conversion are:

1. Skip any leading non-letters.
2. Until the 31-character is reached or the input is exhausted: transcribe “legal” characters; skip
    “illegal” characters apart from spaces; and replace one or more consecutive spaces with an
    underscore, unless the last character transcribed is an underscore in which case space is
    skipped.

In the unlikely event that this policy yields an empty string, we replace the original with col _n_ ,
where _n_ is replaced by the 1-based index of the column in question among those used in the
join operation. If you are in doubt regarding the converted name of a given column, the function
fixname() can be used as a check: it takes the original string as an argument and returns the
converted name. Examples:

```
? eval fixname("valid_identifier")
valid_identifier
? eval fixname("12. Some name")
Some_name
```
Returning to the use of the --data option, suppose we have a column headed "12. Some name"
on the right and wish to import it as x. After figuring how the right-hand name converts, we can do

```
join foo.csv x --data="Some_name"
```
No right-hand names?

Some data files have no column headings; they jump straight into the data (and you need to deter-
mine from accompanying documentation what the columns represent). Since gretl expects column
headings, you have to take steps to get the importation right. It is generally a good idea to insert a
suitable header row into the data file. However, if for some reason that’s not practical, you should
give the --no-header option, in which case gretl will name the columns on the right as col1, col2
and so on. If you do not do either of these things you will likely lose the first row of data, since
gretl will attempt to make variable names out of it, as described above.

### 7.3 Filtering

Rows from the _outer_ dataset can be filtered using the --filter option. The required parameter
for this option is a Boolean condition, that is, an expression which evaluates to non-zero (true,
include the row) or zero (false, skip the row) for each of the outer rows. The filter expression may
include any of the following terms: up to three “right-hand” series (under their converted names as


Chapter 7. Joining data sources 49

explained above); scalar or string variables defined “on the left”; any of the operators and functions
available in gretl (including user-defined functions); and numeric or string constants.

Here are a few simple examples of potentially valid filter options (assuming that the specified right-
hand side columns are found):

```
# 1. relationship between two right-hand variables
--filter="x15<=x17"
```
```
# 2. comparison of right-hand variable with constant
--filter="nkids>2"
```
```
# 3. comparison of string-valued right-hand variable with string constant
--filter="SEX==\"F\""
```
```
# 4. filter on valid values of a right-hand variable
--filter=!missing(income)
```
```
# 5. compound condition
--filter="x < 100 && (x > 0 || y > 0)"
```
Note that if you are comparing against a string constant (as in example 3 above) it is necessary
to put the string in “escaped” double-quotes (each double-quote preceded by a backslash) so the
interpreter knows that F is not supposed to be the name of a variable.

It is safest to enclose the whole filter expression in double quotes, however this is not strictly
required unless the expression contains spaces or the equals sign.

In general, an error is flagged if a missing value is encountered in a series referenced in a filter
expression, because the condition then becomes indeterminate. In example 2 above, if the nkids
value is NA on any given row we are not in a position to evaluate the condition nkids>2. However,
you can use the missing() function — or ok(), which is a shorthand for !missing() — if you need
a filter that keys off the missing or non-missing status of a variable.

### 7.4 Matching with keys

Things get interesting when we come to key-matching. The purpose of this facility is perhaps best
introduced by example. Suppose that (as with many survey and census-based datasets) we have a
dataset that is composed of two or more related files, each having a different unit of observation;
for example we have a “persons” data file and a “households” data file. Table 7.1 shows a simple,
artificial case. The file people.csv contains a unique identifier for the individuals, pid. The
households file, hholds.csv, contains the unique household identifier hid, which is also present
in the persons file.

As a first example of join with keys, let’s add the household-level variable xh to the persons
dataset:

```
open people.csv --quiet
join hholds.csv xh --ikey=hid
print --byobs
```
The basic key option is named ikey; this indicates “inner key”, that is, the key variable found in the
left-hand or inner dataset. By default it is assumed that the right-hand dataset contains a column of
the same name, though as we’ll see below that assumption can be overridden. The join command
above says, find a series named xh in the right-hand dataset and add it to the left-hand one, using
the values of hid to match rows. Looking at the data in Table 7.1 we can see how this should
work. Persons 1 and 2 are both members of household 1, so they should both get values of 1 for
xh; persons 3 and 4 are members of household 2, so that xh = 4; and so on. Note that the order


Chapter 7. Joining data sources 50

in which the key values occur on the right-hand side does not matter. The gretl output from the
print command is shown in the lower panel of Table 7.1.

```
people.csv hholds.csv
```
```
pid,hid,gender,age,xp hid,country,xh
1,1,M,50,1 1,US,1
2,1,F,40,2 6,IT,12
3,2,M,30,3 3,UK,6
4,2,F,25,2 4,IT,8
5,3,M,40,3 2,US,4
6,4,F,35,4 5,IT,10
7,4,M,70,3
8,4,F,60,3
9,5,F,20,4
10,6,M,40,4
```
```
pid hid xh
```
```
1 1 1
2 1 1
3 2 4
4 2 4
5 3 6
6 4 8
7 4 8
8 4 8
9 5 10
10 6 12
```
```
Table 7.1: Two linked CSV data files, and the effect of a join
```
Note that key variables are treated conceptually as integers. If a specified key contains fractional
values these are truncated.

Two extensions of the basic key mechanism are available.

- If the outer dataset contains a relevant key variable but it goes under a different name from
    the inner key, you can use the --okey option to specify the outer key. (As with other right-
    hand names, this does not have to be a valid gretl identifier.) So, for example, if hholds.csv
    contained the hid information, but under the name HHOLD, the join command above could
    be modified as

```
join hholds.csv xh --ikey=hid --okey=HHOLD
```
- If a single key is not sufficient to generate the matches you want, you can specify a double key
    in the form of two series names separated by a comma; in this case the importation of data is
    restricted to those rows on which both keys match. The syntax here is, for example
       join foo.csv x --ikey=key1,key2

```
Again, the --okey option may be used if the corresponding right-hand columns are named
differently. The same number of keys must be given on the left and the right, but when a
```

Chapter 7. Joining data sources 51

```
double key is used and only one of the key names differs on the right, the name that is in
common may be omitted (although the comma separator must be retained). For example, the
second of the following lines is acceptable shorthand for the first:
```
```
join foo.csv x --ikey=key1,Lkey2 --okey=key1,Rkey2
join foo.csv x --ikey=key1,Lkey2 --okey=,Rkey2
```
The number of key-matches

The example shown in Table 7.1 is an instance of a 1 to 1 match: applying the matching criterion
produces exactly one value of the variable xh corresponding to each row of the inner dataset. Three
other possibilities arise:

- Some rows on the left have multiple matches on the right (“1 to _n_ matching”).
- Some rows on the right have multiple matches on the left (“ _n_ to 1 matching”).
- Some rows in the inner dataset have no match on the right.

The 1-to- _n_ case is addressed in detail in the next section; here we discuss the others.

The _n_ to 1 case is straightforward. If a particular key value (or combination of key values) occurs at
each of _n >_ 1 observations on the left but at a single observation on the right, then the right-hand
value is entered at each of the matching slots on the left.

Treatment of the case where there’s _no_ match on the right depends on whether the join operation
is adding a new series to the inner dataset or modifying an existing one. When adding a new series,
unmatched rows automatically get NA for the imported data. However, if join is pulling in values
for a series already present on the left only matched rows will be updated. In other words we do
_not_ overwite an existing value on the left with NA when there’s no match on the right.

These default policies may not produce the desired results in every case but gretl provides the
means to modify the effect if need be. We will illustrate with two scenarios.

First consider adding a new series recording “number of hours worked” when the inner dataset
contains individuals and the outer file contains data on jobs. If an individual does not appear in
the jobs file (no match on the right) the default policy means that her hours worked will be recorded
as NA. If in context you wish to set hours worked to zero rather than NA for such individuals, gretl’s
misszero() function can be used to turn NA into 0 in the imported series.

Second, consider updating an existing series via join when the outer file is presumed to contain all
available updated values, such that “no match” should be taken as an implicit NA. In that case we
want the (presumably out-of-date) values on any unmatched rows to be overwritten with NA. Let the
series in question be called x (both on the left and the right) and let the common key be called pid.
The solution is then

```
join update.csv tmpvar --data=x --ikey=pid
x = tmpvar
```
where tmpvar does not already exist in the inner dataset. As a new series, tmpvar will get NA for
all unmatched rows; we then transcribe its values into x. In a more complicated case one might use
the smpl command to limit the sample range before assigning tmpvar to x, or use the conditional
assignment operator ?:.

One further point: given some missing values in an imported series you may want to know whether
(a) the NAs were explicitly represented in the outer data file or (b) they arose due to “no match”. You
can find this out by using a method described in the following section, namely the count variant of
the aggregation option: this will give you a series with 0 values for all and only unmatched rows.


Chapter 7. Joining data sources 52

### 7.5 Aggregation

In the case of 1 to _n_ matching of rows ( _n >_ 1) the user must specify an “aggregation method”; that
is, a method for mapping from _n_ rows down to one. This is handled by the --aggr option which
requires a single argument from the following list:

```
Code Value returned
```
```
count count of matches
avg mean of matching values
sum sum of matching values
min minimum of matching values
max maximum of matching values
seq: i the i thmatching value (e.g. seq:2)
min( aux ) minimum of matching values of auxiliary variable
max( aux ) maximum of matching values of auxiliary variable
```
Note that the count aggregation method is special, in that there is no need for a “data series” on
the right; the imported series is simply a function of the specified key(s). All the other methods
require that “actual data” are found on the right. Also note that when count is used, the value
returned when no match is found is (as one might expect) zero rather than NA.

The basic use of the seq method is shown above: following the colon you give a positive integer rep-
resenting the (1-based) position of the observation in the sequence of matched rows. Alternatively,
a negative integer can be used to count down from the last match (seq:-1 selects the last match,
seq:-2 the second-last match, and so on). If the specified sequence number is out of bounds for a
given observation this method returns NA.

Referring again to the data in Table 7.1, suppose we want to import data from the persons file into
a dataset established at household level. Here’s an example where we use the individual age data
from people.csv to add the average and minimum age of household members.

```
open hholds.csv --quiet
join people.csv avgage --ikey=hid --data=age --aggr=avg
join people.csv minage --ikey=hid --data=age --aggr=min
```
Here’s a further example where we add to the household data the sum of the personal data xp, with
the twist that we apply filters to get the sum specifically for household members under the age of
40, and for women.

```
open hholds.csv --quiet
join people.csv young_xp --ikey=hid --filter="age<40" --data=xp --aggr=sum
join people.csv female_xp --ikey=hid --filter="gender==\"F\"" --data=xp --aggr=sum
```
The possibility of using an auxiliary variable with the min and max modes of aggregation gives extra
flexibility. For example, suppose we want for each household the income of its oldest member:

```
open hholds.csv --quiet
join people.csv oldest_xp --ikey=hid --data=xp --aggr=max(age)
```
### 7.6 String-valued key variables

The examples above use numerical variables (household and individual ID numbers) in the match-
ing process. It is also possible to use string-valued variables, in which case a match means that the
string values of the key variables compare equal (with case sensitivity). When using double keys,


Chapter 7. Joining data sources 53

you can mix numerical and string keys, but naturally you cannot mix a string variable on the left
(via ikey) with a numerical one on the right (via okey), or vice versa.

Here’s a simple example. Suppose that alongside hholds.csv we have a file countries.csv with
the following content:

```
country,GDP
UK,100
US,500
IT,150
FR,180
```
The variable country, which is also found in hholds.csv, is string-valued. We can pull the GDP of
the country in which the household resides into our households dataset with

```
open hholds.csv -q
join countries.csv GDP --ikey=country
```
which gives

```
hid country GDP
```
```
1 1 1 500
2 6 2 150
3 3 3 100
4 4 2 150
5 2 1 500
6 5 2 150
```
### 7.7 Importing multiple series

The examples given so far have been limited in one respect. While several columns in the outer data
file may be referenced (as keys, or in filtering or aggregation) only one column has actually provided
data — and correspondingly only one series in the inner dataset has been created or modified — per
invocation of join. However, join can handle the importation of several series at once. This
section gives an account of the required syntax along with certain restrictions that apply to the
multiple-import case.

There are two ways to specify more than one series for importation:

1. The _varname_ field in the command can take the form of a space-separated list of names rather
    than a single name.
2. Alternatively, you can give the name of an array of strings in place of _varname_ : the elements
    of this array should be the names of the series to import.

Here are the limitations:

1. The --data option, which permits the renaming of a series on import, is not available. When
    importing multiple series you are obliged to accept their “outer” names, fixed up as described
    in section 7.2.
2. While the other join options are available, they necessarily apply uniformly to all the series
    imported via a given command. This means that if you want to import several series but using
    different keys, filters or aggregation methods you must use a sequence of commands.

Here are a couple of examples of multiple imports.


Chapter 7. Joining data sources 54

```
# open base datafile containing keys
open PUMSdata.gdt
```
```
# join using a list of import names
join ss13pnc.csv SCHL WAGP WKHP --ikey=SERIALNO,SPORDER
```
```
# using a strings array: may be worthwhile if the array
# will be used for more than one purpose
strings S = defarray("SCHL", "WAGP", "WKHP")
join ss13pnc.csv S --ikey=SERIALNO,SPORDER
```
### 7.8 A real-world case

For a real use-case for join with cross-sectional data, we turn to the Bank of Italy’s _Survey on House-
hold Income and Wealth_ (SHIW).^1 In ASCII form the 2010 survey results comprise 47 MB of data in
29 files. In this exercise we will draw on five of the SHIW files to construct a replica of the dataset
used in Thomas Mroz’s famous paper (Mroz, 1987) on women’s labor force participation, which
contains data on married women between the age of 30 and 60 along with certain characteristics
of their households and husbands.

Our general strategy is as follows: we create a “core” dataset by opening the file carcom10.csv,
which contains basic data on the individuals. After dropping unwanted individuals (all but married
women), we use the resulting dataset as a base for pulling in further data via the join command.

The complete script to do the job is given in the Appendix to this chapter; here we walk through
the script with comments interspersed. We assume that all the relevant files from the Bank of Italy
survey are contained in a subdirectory called SHIW.

Starting with carcom10.csv, we use the --cols option to the open command to import specific
series, namely NQUEST (household ID number), NORD (sequence number for individuals within each
household), SEX (male = 1, female = 2), PARENT (status in household: 1 = head of household, 2 =
spouse of head, etc.), STACIV (marital status: married = 1), STUDIO (educational level, coded from
1 to 8), ETA (age in years) and ACOM4C (size of town).

```
open SHIW/carcom10.csv --cols=1,2,3,4,9,10,29,41
```
We then restrict the sample to married women from 30 to 60 years of age, and additionally restrict
the sample of women to those who are either heads of households or spouses of the head.

```
smpl SEX==2 && ETA>=30 && ETA<=60 && STACIV==1 --restrict
smpl PARENT<3 --restrict
```
For compatibility with the Mroz dataset as presented in the gretl data file mroz87.gdt, we rename
the age and education variables as WA and WE respectively, we compute the CIT dummy and finally
we store the reduced base dataset in gretl format.

```
rename ETA WA
rename STUDIO WE
series CIT = (ACOM4C > 2)
```
```
store mroz_rep.gdt
```
The next step will be to get data on working hours from the jobs file allb1.csv. There’s a com-
plication here. We need the total hours worked over the course of the year (for both the women

(^1) Details of the survey can be found at [http://www.bancaditalia.it/statistiche/indcamp/bilfait/dismicro.](http://www.bancaditalia.it/statistiche/indcamp/bilfait/dismicro.)
The ASCII (CSV) data files for the 2010 survey are available at [http://www.bancaditalia.it/statistiche/indcamp/](http://www.bancaditalia.it/statistiche/indcamp/)
bilfait/dismicro/annuale/ascii/ind10_ascii.zip.


Chapter 7. Joining data sources 55

and their husbands). This is not available as such, but the variables ORETOT and MESILAV give,
respectively, average hours worked per week and the number of months worked in 2010, each on a
per-job basis. If each person held at most one job over the year we could compute his or her annual
hours as

```
HRS = ORETOT * 52 * MESILAV/12
```
However, some people had more than one job, and in this case what we want is the sum of annual
hours across their jobs. We could use join with the seq aggregation method to construct this sum,
but it is probably more straightforward to read the allb1 data, compute the HRS values per job as
shown above, and save the results to a temporary CSV file.

```
open SHIW/allb1.csv --cols=1,2,8,11 --quiet
series HRS = misszero(ORETOT) * 52 * misszero(MESILAV)/12
store HRS.csv NQUEST NORD HRS
```
Now we can reopen the base dataset and join the hours variable from HRS.csv. Note that we need
a double key here: the women are uniquely identified by the combination of NQUEST and NORD. We
don’t need an okey specification since these keys go under the same names in the right-hand file.
We define labor force participation, LFP, based on hours.

```
open mroz_rep.gdt
join HRS.csv WHRS --ikey=NQUEST,NORD --data=HRS --aggr=sum
WHRS = misszero(WHRS)
LFP = WHRS > 0
```
For reference, here’s how we could have used seq to avoid writing a temporary file:

```
join SHIW/allb1.csv njobs --ikey=NQUEST,NORD --data=ORETOT --aggr=count
series WHRS = 0
loop i=1..max(njobs)
join SHIW/allb1.csv htmp --ikey=NQUEST,NORD --data=ORETOT --aggr="seq:$i"
join SHIW/allb1.csv mtmp --ikey=NQUEST,NORD --data=MESILAV --aggr="seq:$i"
WHRS += misszero(htmp) * 52 * misszero(mtmp)/12
endloop
```
To generate the work experience variable, AX, we use the file lavoro.csv: this contains a variable
named ETALAV which records the age at which the person first started work.

```
join SHIW/lavoro.csv ETALAV --ikey=NQUEST,NORD
series AX = misszero(WA - ETALAV)
```
We compute the woman’s hourly wage, WW, as the ratio of total employment income to annual
working hours. This requires drawing the series YL (payroll income) and YM (net self-employment
income) from the persons file rper10.csv.

```
join SHIW/rper10.csv YL YM --ikey=NQUEST,NORD --aggr=sum
series WW = LFP? (YL + YM)/WHRS : 0
```
The family’s net disposable income is available as Y in the file rfam10.csv; we import this as
FAMINC.

```
join SHIW/rfam10.csv FAMINC --ikey=NQUEST --data=Y
```
Data on number of children are now obtained by applying the count method. For the Mroz repli-
cation we want the number of children under the age of 6, and also the number aged 6 to 18.


Chapter 7. Joining data sources 56

```
join SHIW/carcom10.csv KIDS --ikey=NQUEST --aggr=count --filter="ETA<=18"
join SHIW/carcom10.csv KL6 --ikey=NQUEST --aggr=count --filter=ETA<6
series K618 = KIDS - KL6
```
We want to add data on the women’s husbands, but how do we find them? To do this we create an
additional inner key which we’ll call H_ID (husband ID), by sub-sampling in turn on the observations
falling into each of two classes: (a) those where the woman is recorded as head of household and
(b) those where the husband has that status. In each case we want the individual ID (NORD) of the
household member whose status is complementary to that of the woman in question. So for case
(a) we subsample using PARENT==1 (head of household) and filter the join using PARENT==2 (spouse
of head); in case (b) we do the converse. We thus construct H_ID piece-wise.

```
# for women who are household heads
smpl PARENT==1 --restrict --replace
join SHIW/carcom10.csv H_ID --ikey=NQUEST --data=NORD --filter="PARENT==2"
# for women who are not household heads
smpl PARENT==2 --restrict --replace
join SHIW/carcom10.csv H_ID --ikey=NQUEST --data=NORD --filter="PARENT==1"
smpl full
```
Now we can use our new inner key to retrieve the husbands’ data, matching H_ID on the left with
NORD on the right within each household.

```
join SHIW/carcom10.csv HA --ikey=NQUEST,H_ID --okey=NQUEST,NORD --data=ETA
join SHIW/carcom10.csv HE --ikey=NQUEST,H_ID --okey=NQUEST,NORD --data=STUDIO
join HRS.csv HHRS --ikey=NQUEST,H_ID --okey=NQUEST,NORD --data=HRS --aggr=sum
HHRS = misszero(HHRS)
```
The remainder of the script is straightforward and does not require discussion here: we recode
the education variables for compatibility; delete some intermediate series that are not needed any
more; add informative labels; and save the final product. See the Appendix for details.

To compare the results from this dataset with those from the earlier US data used by Mroz, one can
copy the input file heckit.inp (supplied with the gretl package) and substitute mroz_rep.gdt for
mroz87.gdt. It turns out that the results are qualitatively very similar.

### 7.9 The representation of dates

Up to this point all the data we have considered have been cross-sectional. In the following sections
we discuss data that have a time dimension, and before proceeding it may be useful to say some-
thing about the representation of dates. Gretl takes the ISO 8601 standard as its reference point
but provides mean of converting dates provided in other formats; it also offers a set of calendrical
functions for manipulating dates (isodate, isoconv, epochday and others).

ISO 8601 recognizes two formats for daily dates, “extended” and “basic”. In both formats dates
are given as 4-digit year, 2-digit month and 2-digit day, in that order. In extended format a dash
is inserted between the fields — as in 2013-10-21 or more generally YYYY-MM-DD — while in basic
format the fields are run together (YYYYMMDD). Extended format is more easily parsed by human
readers while basic format is more suitable for computer processing, since one can apply ordinary
arithmetic to compare dates as equal, earlier or later. The standard also recognizes YYYY-MM as
representing year and month, e.g. 2010-11 for November 2010,^2 as well as a plain four-digit number
for year alone.

One problem for economists is that the “quarter” is not a period covered by ISO 8601. This could
be presented by YYYY-Q (with only one digit following the dash) but in gretl output we in fact use a
colon, as in 2013:2 for the second quarter of 2013. (For printed output of months gretl also uses

(^2) The form YYYYMM is _not_ recognized for year and month.


Chapter 7. Joining data sources 57

a colon, as in 2013:06. A difficulty with following ISO here is that in a statistical context a string
such as 1980-10 may look more like a subtraction than a date.) Anyway, at present we are more
interested in the parsing of dates on input rather than in what gretl prints. And in that context note
that “excess precision” is acceptable: a month may be represented by its first day (e.g. 2005-05-01
for May, 2005), and a quarter may be represented by its first month and day (2005-07-01 for the
third quarter of 2005).

Some additional points regarding dates will be taken up as they become relevant in practical cases
of joining data.

### 7.10 Time-series data

Suppose our left-hand dataset is recognized by gretl as time series with a supported frequency
(annual, quarterly, monthly, weekly, daily or hourly). This will be the case if the original data were
read from a file that contained suitable time or date information, or if a time-series interpretation
has been imposed using either the setobs command or its GUI equivalent. Then — apart, perhaps,
from some very special cases — joining additional data is bound to involve matching observations
by time-period. In this case, contrary to the cross-sectional case, the inner dataset has a natural
ordering of which gretl is aware; hence, no “inner key” is required.

If, in addition, the file from data which are to be joined is in native gretl format and contains time-
series information, keys are not needed at all. Three cases can arise: the frequency of the outer
dataset may be the same, lower or higher than that of the inner dataset. In the first two cases
join should work without any special apparatus; lower-frequency values will be repeated for each
high-frequency period. In the third case, however, an aggregation method must be specified: gretl
needs to know how to map higher-frequency data into the existing dataset (by averaging, summing,
or whatever).

If the outer data file is _not_ in native gretl format we need a means of identifying the period of each
observation on the right, an outer key which we’ll call a “time key”. The join command provides
a simple (but limited) default for extracting period information from the outer data file, plus an
option that can be used if the default is not applicable, as follows.

- The default assumptions are: (1) the time key appears in the first column; (2) the heading
    of this column is either left blank or is one of obs, date, year, period, observation, or
    observation_date (on a case-insensitive comparison); and (3) the time format conforms
    to ISO 8601 where applicable (“extended” daily date format YYYY-MM-DD, monthly format
    YYYY-MM, or annual format YYYY).
- If dates do not appear in the first column of the outer file, or if the column heading or format
    is not as just described, the --tkey option can be used to indicate which column should be
    used and/or what format should be assumed.

Setting the time-key column and/or format

The --tkey option requires a parameter holding the name of the column in which the time key
is located and/or a string specifying the format in which dates/times are written in the time-key
column. This parameter should be enclosed in double-quotes. If both elements are present they
should be separated by a comma; if only a format is given it should be preceded by a comma. Some
examples:

```
--tkey="Period,%m/%d/%Y"
--tkey="Period"
--tkey="obsperiod"
--tkey=",%Ym%m"
```

Chapter 7. Joining data sources 58

The first of these applies if Period is not the first column on the right, and dates are given in the
US format of month, day, year, separated by slashes. The second implies that although Period is
not the first column, the date format is ISO 8601. The third again implies that the date format is
OK; here the name is required even if obsperiod is the first column since this heading is not one
recognized by gretl’s heuristic. The last example implies that dates are in the first column (with
one of the recognized headings), but are given in the non-standard format year, “m”, month.

The date format string should be composed using the codes employed by the POSIX function
strptime; Table 7.2 contains a list of the most relevant codes.^3

```
Code Meaning
%% The % character.
%b The month name according to the current locale, either abbreviated
or in full.
%C The century number (0–99).
%d The day of month (1–31).
%D Equivalent to %m/%d/%y. (This is the American style date, very con-
fusing to non-Americans, especially since %d/%m/%y is widely used in
Europe. The ISO 8601 standard format is %Y-%m-%d.)
%H The hour (0–23).
%j The day number in the year (1–366).
%m The month number (1–12).
%n Arbitrary whitespace.
%q The quarter (1–4).
%w The weekday number (0–6) with Sunday = 0.
%y The year within century (0–99). When a century is not otherwise spec-
ified, values in the range 69–99 refer to years in the twentieth century
(1969–1999); values in the range 00–68 refer to years in the twenty-
first century (2000–2068).
%Y The year, including century (for example, 1991).
```
```
Table 7.2: Date format codes
```
Example: daily stock prices

We show below the first few lines of a file named IBM.csv containing stock-price data for IBM
corporation.

```
Date,Open,High,Low,Close,Volume,Adj Close
2013-08-02,195.50,195.50,193.22,195.16,3861000,195.16
2013-08-01,196.65,197.17,195.41,195.81,2856900,195.81
2013-07-31,194.49,196.91,194.49,195.04,3810000,195.04
```
Note that the data are in reverse time-series order — that won’t matter to join, the data can appear
in any order. Also note that the first column is headed Date and holds daily dates as ISO 8601
extended. That means we can pull the data into gretl very easily. In the following fragment we
create a suitably dimensioned empty daily dataset then rely on the default behavior of join with
time-series data to import the closing stock price.

```
nulldata 500
setobs 5 2012-01-01
join IBM.csv Close
```
(^3) The %q code for quarter is not present in strptime; it is added for use with join since quarterly data are common
in macroeconomics.


Chapter 7. Joining data sources 59

To make explicit what we’re doing, we could accomplish exactly the same using the --tkey option:

```
join IBM.csv Close --tkey="Date,%Y-%m-%d"
```
Example: OECD quarterly data

Table 7.3 shows an excerpt from a CSV file provided by the OECD statistical site (stat.oecd.org)
in response to a request for GDP at constant prices for several countries.^4

```
Frequency,Period,Country,Value,Flags
"Quarterly","Q1-1960","France",463876.148126845,E
"Quarterly","Q1-1960","Germany",768802.119278467,E
"Quarterly","Q1-1960","Italy",414629.791450547,E
"Quarterly","Q1-1960","United Kingdom",578437.090291889,E
"Quarterly","Q2-1960","France",465618.977328614,E
"Quarterly","Q2-1960","Germany",782484.138122549,E
"Quarterly","Q2-1960","Italy",420714.910290157,E
"Quarterly","Q2-1960","United Kingdom",572853.474696578,E
"Quarterly","Q3-1960","France",469104.41925852,E
"Quarterly","Q3-1960","Germany",809532.161494483,E
"Quarterly","Q3-1960","Italy",426893.675840156,E
"Quarterly","Q3-1960","United Kingdom",581252.066618986,E
"Quarterly","Q4-1960","France",474664.327992619,E
"Quarterly","Q4-1960","Germany",817806.132384948,E
"Quarterly","Q4-1960","Italy",427221.338414114,E
...
```
```
Table 7.3: Example of CSV file as provided by the OECD statistical website
```
This is an instance of data in what we call _atomic format_ , that is, a format in which each line of the
outer file contains a single data-point and extracting data mainly requires filtering the appropriate
lines. The outer time key is under the Period heading, and has the format Q _<quarter>-<year>_.
Assuming that the file in Table 7.3 has the name oecd.csv, the following script reconstructs the
time series of Gross Domestic Product for several countries:

nulldata 220
setobs 4 1960:1

join oecd.csv FRA --tkey="Period,Q%q-%Y" --data=Value --filter="Country==\"France\""
join oecd.csv GER --tkey="Period,Q%q-%Y" --data=Value --filter="Country==\"Germany\""
join oecd.csv ITA --tkey="Period,Q%q-%Y" --data=Value --filter="Country==\"Italy\""
join oecd.csv UK --tkey="Period,Q%q-%Y" --data=Value --filter="Country==\"United Kingdom\""

Note the use of the format codes %q for the quarter and %Y for the 4-digit year. A touch of elegance
could have been added by storing the invariant options to join using the setopt command, as in

setopt join persist --tkey="Period,Q%q-%Y" --data=Value
join oecd.csv FRA --filter="Country==\"France\""
join oecd.csv GER --filter="Country==\"Germany\""
join oecd.csv ITA --filter="Country==\"Italy\""
join oecd.csv UK --filter="Country==\"United Kingdom\""
setopt join clear

If one were importing a large number of such series it might be worth rewriting the sequence of
joins as a loop, as in

(^4) Retrieved 2013-08-05. The OECD files in fact contain two leading columns with very long labels; these are irrelevant
to the present example and can be omitted without altering the sample script.


Chapter 7. Joining data sources 60

strings countries = defarray("France", "Germany", "Italy", "United Kingdom")
strings vnames = defarray("FRA", "GER", "ITA", "UK")
setopt join persist --tkey="Period,Q%q-%Y" --data=Value

loop foreach i countries
vname = vnames[i]
join oecd.csv @vname --filter="Country==\"$i\""
endloop
setopt join clear

### 7.11 Special handling of time columns

When dealing with straight time series data the tkey mechanism described above should suffice
in almost all cases. In some contexts, however, time enters the picture in a more complex way;
examples include panel data (see section 7.12) and so-called realtime data (see chapter 8). To handle
such cases join provides the --tconvert option. This can be used to select certain columns in
the right-hand data file for special treatment: strings representing dates in these columns will be
converted to numerical values: 8-digit numbers on the pattern YYYYMMDD (ISO basic daily format).
Once dates are in this form it is easy to use them in key-matching or filtering.

By default it is assumed that the strings in the selected columns are in ISO extended format,
YYYY-MM-DD. If that is not the case you can supply a time-format string using the --tconv-fmt
option. The format string should be written using the codes shown in Table 7.2.

Here are some examples:

```
# select one column for treatment
--tconvert=start_date
```
```
# select two columns for treatment
--tconvert="start_date,end_date"
```
```
# specify US-style daily date format
--tconv-fmt="%m/%d/%Y"
```
```
# specify quarterly date-strings (as in 2004q1)
--tconv-fmt="%Yq%q"
```
Some points to note:

- If a specified column is not selected for a substantive role in the join operation (as data to be
    imported, as a key, or as an auxiliary variable for use in aggregation) the column in question
    is not read and so no conversion is carried out.
- If a specified column contains numerical rather than string values, no conversion is carried
    out.
- If a string value in a selected column fails parsing using the relevant time format (user-
    specified or default), the converted value is NA.
- On successful conversion, the output is always in daily-date form as stated above. If you
    specify a monthly or quarterly time format, the converted date is the first day of the month
    or quarter.

### 7.12 Panel data

In section 7.10 we gave an example of reading quarterly GDP data for several countries from an
OECD file. In that context we imported each country’s data as a distinct time-series variable. Now


Chapter 7. Joining data sources 61

suppose we want the GDP data in panel format instead (stacked time series). How can we do this
with join?

As a reminder, here’s what the OECD data look like:

```
Frequency,Period,Country,Value,Flags
"Quarterly","Q1-1960","France",463876.148126845,E
"Quarterly","Q1-1960","Germany",768802.119278467,E
"Quarterly","Q1-1960","Italy",414629.791450547,E
"Quarterly","Q1-1960","United Kingdom",578437.090291889,E
"Quarterly","Q2-1960","France",465618.977328614,E
```
and so on. If we have four countries and quarterly observations running from 1960:1 to 2013:2 ( _T_
= 214 quarters) we might set up our panel workspace like this:

```
scalar N = 4
scalar T = 214
scalar NT = N*T
nulldata NT --preserve
setobs T 1.1 --stacked-time-series
```
The relevant outer keys are obvious: Country for the country and Period for the time period. Our
task is now to construct matching keys in the inner dataset. This can be done via two panel-specific
options to the setobs command. Let’s work on the time dimension first:

```
setobs 4 1960:1 --panel-time
series quarter = $obsdate
```
This variant of setobs allows us to tell gretl that time in our panel is quarterly, starting in the
first quarter of 1960. Having set that, the accessor $obsdate will give us a series of 8-digit dates
representing the first day of each quarter — 19600101, 19600401, 19600701, and so on, repeating
for each country. As we explained in section 7.11, we can use the --tconvert option on the outer
series Period to get exactly matching values (in this case using a format of Q%q-%Y for parsing the
Period values).

Now for the country names:

```
string cstrs = sprintf("France Germany Italy \"United Kingdom\"")
setobs country cstrs --panel-groups
```
Here we write into the string cstrs the names of the countries, using escaped double-quotes to
handle the space in “United Kingdom”, then pass this string to setobs with the --panel-groups
option, preceded by the identifier country. This asks gretl to construct a string-valued series
named country, in which each name will repeat _T_ times.

We’re now ready to join. Assuming the OECD file is named oecd.csv we do

```
join oecd.csv GDP --data=Value \
--ikey=country,quarter --okey=Country,Period \
--tconvert=Period --tconv-fmt="Q%q-%Y"
```
Other input formats

The OECD file discussed above is in the most convenient format for join, with one data-point per
line. But sometimes we may want to make a panel from a data file structured like this:

```
# Real GDP
Period,France,Germany,Italy,"United Kingdom"
```

Chapter 7. Joining data sources 62

#### "Q1-1960",463863,768757,414630,578437

#### "Q2-1960",465605,782438,420715,572853

#### "Q3-1960",469091,809484,426894,581252

#### "Q4-1960",474651,817758,427221,584779

#### "Q1-1961",482285,826031,442528,594684

Call this file side_by_side.csv. Assuming the same initial set-up as above, we can panelize the
data by setting the sample to each country’s time series in turn and importing the relevant column.
The only point to watch here is that the string “United Kingdom”, being a column heading, will
become United_Kingdom on importing (see section 7.2) so we’ll need a slightly different set of
country strings.

```
strings cstrs = defarray("France", "Germany", "Italy", "United_Kingdom")
setobs country cstrs --panel-groups
loop foreach i cstrs
smpl country=="$i" --restrict --replace
join side_by_side.csv GDP --data=$i \
--ikey=quarter --okey=Period \
--tconvert=Period --tconv-fmt="Q%q-%Y"
endloop
smpl full
```
If our working dataset and the outer data file are dimensioned such that there are just as many
time-series observations on the right as there are time slots on the left — and the observations
on the right are contiguous, in chronological order, and start on the same date as the working
dataset — we could dispense with the key apparatus and just use the first line of the join command
shown above. However, in general it is safer to use keys to ensure that the data end up in correct
registration.

### 7.13 Memo: join options

Basic syntax: join _filename varname(s)_ [ _options_ ]

```
flag effect
```
```
--data Give the name of the data column on the right, in case it differs from
varname (7.2); single import only
--filter Specify a condition for filtering data rows (7.3)
--ikey Specify up to two keys for matching data rows (7.4)
--okey Specify outer key name(s) in case they differ the inner ones (7.4)
--aggr Select an aggregation method for 1 to n joins (7.5)
--tkey Specify right-hand time key (7.10)
--tconvert Select outer date columns for conversion to numeric form (7.11)
--tconv-fmt Specify a format for use with tconvert (7.11)
--no-header Treat the first row on the right as data (7.2)
--verbose Report on progress in reading the outer data
```

Chapter 7. Joining data sources 63

### Appendix: the full Mroz data script

```
# start with everybody; get gender, age and a few other variables
# directly while we’re at it
open SHIW/carcom10.csv --cols=1,2,3,4,9,10,29,41
```
```
# subsample on married women between the ages of 30 and 60
smpl SEX==2 && ETA>=30 && ETA<=60 && STACIV==1 --restrict
# for simplicity, restrict to heads of households and their spouses
smpl PARENT<3 --restrict
```
```
# rename the age and education variables for compatibility; compute
# the "city" dummy and finally save the reduced base dataset
rename ETA WA
rename STUDIO WE
series CIT = (ACOM4C>2)
store mroz_rep.gdt
```
```
# make a temp file holding annual hours worked per job
open SHIW/allb1.csv --cols=1,2,8,11 --quiet
series HRS = misszero(ORETOT) * 52 * misszero(MESILAV)/12
store HRS.csv NQUEST NORD HRS
```
```
# reopen the base dataset and begin drawing assorted data in
open mroz_rep.gdt
```
```
# women’s annual hours (summed across jobs)
join HRS.csv WHRS --ikey=NQUEST,NORD --data=HRS --aggr=sum
WHRS = misszero(WHRS)
```
```
# labor force participation
LFP = WHRS > 0
```
```
# work experience: ETALAV = age when started first job
join SHIW/lavoro.csv ETALAV --ikey=NQUEST,NORD
series AX = misszero(WA - ETALAV)
```
```
# women’s hourly wages
join SHIW/rper10.csv YL YM --ikey=NQUEST,NORD --aggr=sum
series WW = LFP? (YL + YM)/WHRS : 0
```
```
# family income (Y = net disposable income)
join SHIW/rfam10.csv FAMINC --ikey=NQUEST --data=Y
```
```
# get data on children using the "count" method
join SHIW/carcom10.csv KIDS --ikey=NQUEST --aggr=count --filter="ETA<=18"
join SHIW/carcom10.csv KL6 --ikey=NQUEST --aggr=count --filter=ETA<6
series K618 = KIDS - KL6
```
```
# data on husbands: we first construct an auxiliary inner key for
# husbands, using the little trick of subsampling the inner dataset
#
# for women who are household heads
smpl PARENT==1 --restrict --replace
join SHIW/carcom10.csv H_ID --ikey=NQUEST --data=NORD --filter="PARENT==2"
# for women who are not household heads
smpl PARENT==2 --restrict --replace
join SHIW/carcom10.csv H_ID --ikey=NQUEST --data=NORD --filter="PARENT==1"
smpl full
```

Chapter 7. Joining data sources 64

```
# add husbands’ data via the newly-added secondary inner key
join SHIW/carcom10.csv HA --ikey=NQUEST,H_ID --okey=NQUEST,NORD --data=ETA
join SHIW/carcom10.csv HE --ikey=NQUEST,H_ID --okey=NQUEST,NORD --data=STUDIO
join HRS.csv HHRS --ikey=NQUEST,H_ID --okey=NQUEST,NORD --data=HRS --aggr=sum
HHRS = misszero(HHRS)
```
```
# final cleanup begins
```
```
# recode educational attainment as years of education
matrix eduyrs = {0, 5, 8, 11, 13, 16, 18, 21}
series WE = replace(WE, seq(1,8), eduyrs)
series HE = replace(HE, seq(1,8), eduyrs)
```
```
# cut some cruft
delete SEX STACIV KIDS YL YM PARENT H_ID ETALAV
```
```
# add some labels for the series
setinfo LFP -d "1 if woman worked in 2010"
setinfo WHRS -d "Wife’s hours of work in 2010"
setinfo KL6 -d "Number of children less than 6 years old in household"
setinfo K618 -d "Number of children between ages 6 and 18 in household"
setinfo WA -d "Wife’s age"
setinfo WE -d "Wife’s educational attainment, in years"
setinfo WW -d "Wife’s average hourly earnings, in 2010 euros"
setinfo HHRS -d "Husband’s hours worked in 2010"
setinfo HA -d "Husband’s age"
setinfo HE -d "Husband’s educational attainment, in years"
setinfo FAMINC -d "Family income, in 2010 euros"
setinfo AX -d "Actual years of wife’s previous labor market experience"
setinfo CIT -d "1 if live in large city"
```
```
# save the final product
store mroz_rep.gdt
```

## Chapter 8

Realtime data

### 8.1 Introduction

The join command in gretl (see chapter 7) deals in a fairly straightforward manner with so-called
realtime datasets. Such datasets contain information on when the observations in a time series
were actually published by the relevant statistical agency and how they have been revised over time.
Probably the most popular sources of such data are the “Alfred” online database at the St. Louis Fed
(http://alfred.stlouisfed.org/) and the OECD’s StatExtracts site, [http://stats.oecd.org/.](http://stats.oecd.org/.)
The examples in this chapter deal with files downloaded from these sources, but should be easy to
adapt to files with a slightly different format.

As already stated, join requires a column-oriented plain text file, where the columns may be sepa-
rated by commas, tabs, spaces or semicolons. Alfred and the OECD provide the option to download
realtime data in this format (tab-delimited files from Alfred, comma-delimited from the OECD). If
you have a realtime dataset in a spreadsheet file you must export it to a delimited text file before
using it with join.

Representing revision histories is more complex than just storing a standard time series, because
for each observation period you have in general more than one published value over time, along
with the information on when each of these values were valid or current. Sometimes this is repre-
sented in spreadsheets with two time axes, one for the observation period and another one for the
publication date or “vintage”. The filled cells then form an upper triangle (or a “guillotine blade”
shape, if the publication dates do not reach back far enough to complete the triangle). This format
can be useful for giving a human reader an overview of realtime data, but it is not optimal for
automatic processing; for that purpose “atomic” format is best.

### 8.2 Atomic format for realtime data

What we are calling atomic format is exactly the format used by Alfred if you choose the option
“Observations by Real-Time Period”, and by the OECD if you select all editions of a series for
download as plain text (CSV).^1 A file in this format contains one actual data-point per line, together
with associated metadata. This is illustrated in Table 8.1, where we show the first three lines from
an Alfred file and an OECD file (slightly modified).^2

Consider the first data line in the Alfred file: in the observation_date column we find 1960-01-01,
indicating that the data-point on this line, namely 112.0, is an observation or measurement (in this
case, of the US index of industrial production) that refers to the period starting on January 1st

1960. The realtime_start_date value of 1960-02-16 tells us that this value was published on
February 16th 1960, and the realtime_end_date value says that this vintage remained current
through March 15th 1960. On the next day (as we can see from the following line) this data-point
was revised slightly downward to 111.0.

Daily dates in Alfred files are given in ISO extended format, YYYY-MM-DD, but below we describe
how to deal with differently formatted dates. Note that daily dates are appropriate for the last two

(^1) If you choose to download in Excel format from OECD you get a file in the triangular or guillotine format mentioned
above.
(^2) In the Alfred file we have used commas rather than tabs as the column delimiter; in the OECD example we have
shortened the name in the Variable column.

#### 65


Chapter 8. Realtime data 66

```
Alfred: monthly US industrial production
```
```
observation_date,INDPRO,realtime_start_date,realtime_end_date
1960-01-01,112.0000,1960-02-16,1960-03-15
1960-01-01,111.0000,1960-03-16,1961-10-15
```
```
OECD: monthly UK industrial production
```
```
Country,Variable,Frequency,Time,Edition,Value,Flags
"United Kingdom","INDPRO","Monthly","Jan-1990","February 1999",100,
"United Kingdom","INDPRO","Monthly","Feb-1990","February 1999",99.3,
```
```
Table 8.1: Variant atomic formats for realtime data
```
columns, which jointly record the interval over which a given data vintage was current. Daily dates
might, however, be considered overly precise for the first column, since the data period may well
be the year, quarter or month. However, following Alfred’s practice it is acceptable to specify a
daily date, indicating the first day of the period, even for non-daily data.^3

Compare the first data line of the OECD example. There’s a greater amount of leading metadata,
which is left implicit in the Alfred file. Here Time is the equivalent of Alfred’s observation_date,
and Edition the equivalent of Alfred’s realtime_start_date. So we read that in February 1999
a value of 100 was current for the UK index of industrial production for January 1990, and from
the next line we see that in the same vintage month a value of 99.3 was current for industrial
production in February 1990.

Besides the different names and ordering of the columns, there are a few more substantive differ-
ences between Alfred and OECD files, most of which are irrelevant for join but some of which are
(possibly) relevant.

The first (irrelevant) difference is the ordering of the lines. It appears (though we’re not sure how
consistent this is) that in Alfred files the lines are sorted by observation date first and then by
publication date — so that all revisions of a given observation are grouped together — while OECD
files are sorted first by revision date (Edition) and then by observation date (Time). If we want the
next revision of UK industrial production for January 1990 in the OECD file we have to scan down
several lines until we find

```
"United Kingdom","INDPRO","Monthly","Jan-1990","March 1999",100,
```
This difference in format is basically irrelevant because join can handle the case where the lines
appear in random order, although some operations can be coded more conveniently if we’re able
to assume chronological ordering (either on the Alfred or the OECD pattern, it doesn’t matter).

The second (also irrelevant) difference is that the OECD seems to include periodic “Edition” lines
even when there is no change from the previous value (as illustrated above, where the UK industrial
production index for January 1990 is reported as 100 as of March 1999, the same value that we saw
to be current in February 1999), while Alfred reports a new value only when it differs from what
was previously current.

A third difference lies in the dating of the revisions or editions. As we have seen, Alfred gives
a specific daily date while (in the UK industrial production file at any rate), the OECD just dates
each edition to a month. This is not necessarily relevant for join, but it does raise the question of
whether the OECD might date revisions to a finer granularity in some of their files, in which case
one would have to be on the lookout for a different date format.

The final difference is that Alfred supplies an “end date” for each data vintage while the OECD

(^3) Notice that this implies that in the Alfred example it is not clear without further information whether the observation
period is the first quarter of 1960, the month January 1960, or the day January 1st 1960. However, we assume that this
information is always available in context.


Chapter 8. Realtime data 67

supplies only a starting date. But there is less to this difference than meets the eye: according to
the Alfred webmaster, “by design, a new vintage must start immediately following (the day after)
the lapse of the old vintage” — so the end date conveys no independent information.^4

### 8.3 More on time-related options

Before we get properly started it is worth saying a little more about the --tkey and --tconvert
options to join (introduced in section 7.11), as they apply in the case of realtime data.

When you’re working with regular time series data tkey is likely to be useful while tconvert is
unlikely to be applicable (see section 7.10). On the other hand, when you’re working with panel data
tkey is definitely not applicable but tconvert may well be helpful (section 7.12). When working
with realtime data, however, depending on the task in hand both options may be useful. You will
likely need tkey; you may well wish to select at least one column for tconvert treatment; and in
fact you may want to name a given column in both contexts — that is, include the tkey variable
among the tconvert columns.

Why might this make sense? Well, think of the --tconvert option as a “preprocessing” directive:
it asks gretl to convert date strings to numerical values (8-digit ISO basic dates) “at source”, as they
are read from the outer datafile. The --tkey option, on the other hand, singles out a column as
the one to use for matching rows with the inner dataset. So you would want to name a column in
both roles if (a) it should be used for matching periods and also (b) it is desirable to have the values
from this column in numerical form, most likely for use in filtering.

As we have seen, you can supply specific formats in connection with both tkey and tconvert (in
the latter case via the companion option --tconv-fmt) to handle the case where the date strings on
the right are not ISO-friendly at source. This raises the question of how the format specifications
work if a given column is named under both options. Here are the rules that gretl applies:

1. If a format is given with the --tkey option it always applies to the tkey column alone; and
    for that column it overrides any format given via the --tconv-fmt option.
2. If a format is given via tconv-fmt it is assumed to apply to all the tconvert columns, unless
    this assumption is preempted by rule 1.

### 8.4 Getting a certain data vintage

The most common application of realtime data is to “travel back in time” and retrieve the data that
were current as of a certain date in the past. This would enable you to replicate a forecast or other
statistical result that could have been produced at that date.

For example, suppose we are interested in a variable of monthly frequency named INDPRO, realtime
data on which is stored in an Alfred file named INDPRO.txt, and we want to check the status quo
as of June 15th 2011.

If we don’t already have a suitable dataset into which to import the INDPRO data, our first steps will
be to create an appropriately dimensioned empty dataset using the nulldata command and then
specify its time-series character via setobs, as in

```
nulldata 132
setobs 12 2004:01
```
For convenience we can put the name of our realtime file into a string variable. On Windows this
might look like

(^4) Email received from Travis May of the Federal Reserve Bank of St. Louis, 2013-10-17. This closes off the possibility
that a given vintage could lapse or expire some time before the next vintage becomes available, hence giving rise to a
“hole” in an Alfred realtime file.


Chapter 8. Realtime data 68

```
string fname = "C:/Users/yourname/Downloads/INDPRO.txt"
```
We can then import the data vintage 2011-06-15 using join, arbitrarily choosing the (hopefully)
self-explanatory identifier ip_asof_20110615.

```
join @fname ip_asof_20110615 --tkey=observation_date --data=INDPRO \
--tconvert="realtime_start_date" \
--filter="realtime_start_date<=20110615" --aggr=max(realtime_start_date)
```
Here some detailed explanations of the various options are warranted:

- The --tkey option specifies the column which should be treated as holding the observation
    period identifiers to be matched against the periods in the current gretl dataset.^5 The more
    general form of this option is --tkey="colname,format" (note the double quotes here), so
    if the dates do not come in standard format, we can tell gretl how to parse them by using
    the appropriate conversion specifiers as shown in Table 7.2. For example, here we could have
    written --tkey="observation_date,%Y-%m-%d".
- Next, --data=INDPRO tells gretl that we want to retrieve the entries stored in the column
    named INDPRO.
- As explained in section 7.11 the --tconvert option selects certain columns in the right-hand
    data file for conversion from date strings to 8-digit numbers on the pattern YYYYMMDD. We’ll
    need this for the next step, filtering, since the transformation to numerical values makes
    it possible to perform basic arithmetic on dates. Note that since date strings in Alfred files
    conform to gretl’s default assumption it is not necessary to use the --tconv-fmt option here.
- The --filter option specification in combination with the subsequent --aggr aggregation
    treatment is the central piece of our data retrieval; notice how we use the date constant
    20110615 in ISO basic form to do numerical comparisons, and how we perform the numerical
    max operation on the converted column realtime_start_date. It would also have been
    possible to predefine a scalar variable, as in

```
vintage = 20110615
```
```
and then use vintage in the join command instead. Here we tell join that we only want to
extract those publications that (1) already appeared before (and including) June 15th 2011,
and (2) were not yet obsoleted by a newer release.^6
```
As a result, your dataset will now contain a time series named ip_asof_20110615 with the values
that a researcher would have had available on June 15th 2011. Of course, all values for the observa-
tions after June 2011 will be missing (and probably a few before that, too), because they only have
become available later on.

### 8.5 Getting the n -th release for each observation period

For some purposes it may be useful to retrieve the _n_ -th published value of each observation, where
_n_ is a fixed positive integer, irrespective of _when_ each of these _n_ -th releases was published. Sup-
pose we are interested in the third release, then the relevant join command becomes:

```
join @fname ip_3rdpub --tkey=observation_date --data=INDPRO --aggr="seq:3"
```
(^5) Strictly speaking, using --tkey is unnecessary in this example because we could just have relied on the default,
which is to use the first column in the source file for the periods. However, being explicit is often a good idea.
(^6) By implementing the second condition through the max aggregation on the realtime_start_date column alone,
without using the realtime_end_date column, we make use of the fact that Alfred files cannot have “holes” as explained
before.


Chapter 8. Realtime data 69

Since we do not need the realtime_start_date information for this retrieval, we have dropped
the --tconvert option here. Note that this formulation assumes that the source file is ordered
chronologically, otherwise using the option --aggr="seq:3", which retrieves the third value from
each sequence of matches, could have yielded a result different from the one intended. However,
this assumption holds for Alfred files and is probably rather safe in general.

The values of the variable imported as ip_3rdpub in this way were published at different dates,
so the variable is effectively a mix of different vintages. Depending on the type of variable, this
may also imply drastic jumps in the values; for example, index numbers are regularly re-based
to different base periods. This problem also carries over to inflation-adjusted economic variables,
where the base period of the price index changes over time. Mixing vintages in general also means
mixing different scales in the output, with which you would have to deal appropriately.^7

### 8.6 Getting the values at a fixed lag after the observation period

New data releases may take place on any day of the month, and as we have seen the specific day
of each release is recorded in realtime files from Alfred. However, if you are working with, say,
monthly or quarterly data you may sometimes want to adjust the granularity of your realtime axis
to a monthly or quarterly frequency. For example, in order to analyse the data revision process for
monthly industrial production you might be interested in the extent of revisions between the data
available two and three months after each observation period.

This is a relatively complicated task and there is more than one way of accomplishing it. Either you
have to make several passes through the outer dataset or you need a sophisticated filter, written
as a hansl function. Either way you will want to make use of some of gretl’s built-in calendrical
functions.

We’ll assume that a suitably dimensioned workspace has been set up as described above. Given
that, the key ingredients of the join are a filtering function which we’ll call rel_ok (for “release is
OK”) and the join command which calls it. Here’s the function:

```
function series rel_ok (const series obsdate, const series reldate, int p)
series y_obs, m_obs, y_rel, m_rel
# get year and month from observation date
isoconv(obsdate, &y_obs, &m_obs)
# get year and month from release date
isoconv(reldate, &y_rel, &m_rel)
# find the delta in months
series dm = (12*y_rel + m_rel) - (12*y_obs + m_obs)
# and implement the filter
return dm <= p
end function
```
Note that the series arguments to rel_ok are marked as const so that they’re simply shared with
the function rather than being copied (since they’re not being modified; see chapter 14). And here’s
the command:

```
scalar lag = 3 # choose your fixed lag here
join @fname ip_plus3 --data=INDPRO --tkey=observation_date \
--tconvert="observation_date,realtime_start_date" \
--filter="rel_ok(observation_date, realtime_start_date, lag)" \
--aggr=max(realtime_start_date)
```
(^7) Some user-contributed functions may be available that address this issue, but it is beyond our scope here. Another
even more complicated issue in the realtime context is that of “benchmark revisions” applied by statistical agencies,
where the underlying definition or composition of a variable changes on some date, which goes beyond a mere rescaling.
However, this type of structural change is not, in principle, a feature of realtime data alone, but applies to any time-series
data.


Chapter 8. Realtime data 70

Note that we use --tconvert to convert both the observation date and the realtime start date (or
release date) to 8-digit numerical values. Both of these series are passed to the filter, which uses the
built-in function isoconv to extract year and month. We can then calculate dm, the “delta months”
since the observation date, for each release. The filter condition is that this delta should be no
greater than the specified lag, _p_.^8

This filter condition may be satisfied by more than one release, but only the latest of those will
actually be the vintage that was current at the end of the _n_ -th month after the observation period,
so we add the option --aggr=max(realtime_start_date). If instead you want to target the
release at the _beginning_ of the _n_ -th month you would have to use a slightly more complicated filter
function.

An illustration

Figure 8.1 shows four time series for the monthly index of US industrial production from October
2005 to June 2009: the value as of first publication plus the values current 3, 6 and 12 months out
from the observation date.^9 From visual inspection it would seem that over much of this period
the Federal reserve was fairly consistently overestimating industrial production at first release and
shortly thereafter, relative to the figure they arrived at with a lag of a year.

The script that produced this Figure is shown in full in Listing 8.1.

☞ To replicate the examples in Listings 8.1 and 8.2 below you’ll need the Alfred file INDPRO.txt, which is
available as https://gretl.sf.net/gretldata/INDPRO.txt.

```
94
```
```
96
```
```
98
```
```
100
```
```
102
```
```
104
```
```
106
```
```
108
```
```
110
```
```
112
```
```
114
```
```
116
```
```
2006 2007 2008 2009
```
```
First publication
Plus 3 months
Plus 6 months
Plus 12 months
```
```
Figure 8.1: Successive revisions to US industrial production
```
### 8.7 Getting the revision history for an observation

For our final example we show how to retrieve the revision history for a given observation (again
using Alfred data on US industrial production). In this exercise we are switching the time axis: the
observation period is a fixed point and time is “vintage time”.

(^8) The filter is written on the assumption that the lag is expressed in months; on that understanding it could be used
with annual or quarterly data as well as monthly. The idea could be generalized to cover weekly or daily data without
much difficulty.
(^9) Why not a longer series? Because if we try to extend it in either direction we immediately run into the index re-basing
problem mentioned in section 8.5, with big (staggered) leaps downward in all the series.


Chapter 8. Realtime data 71

```
Listing 8.1: Retrieving successive realtime lags of US industrial production [Download▼]
```
function series rel_ok (const series obsdate, const series reldate, int p)
series y_obs, m_obs, d_obs, y_rel, m_rel, d_rel
isoconv(obsdate, &y_obs, &m_obs, &d_obs)
isoconv(reldate, &y_rel, &m_rel, &d_rel)
series dm = (12*y_rel + m_rel) - (12*y_obs + m_obs)
return dm < p || (dm == p && d_rel <= d_obs)
end function

nulldata 45
setobs 12 2005:10

string fname = "INDPRO.txt"

# initial published values
join @fname firstpub --data=INDPRO --tkey=observation_date \
--tconvert=realtime_start_date --aggr=min(realtime_start_date)

# plus 3 months
join @fname plus3 --data=INDPRO --tkey=observation_date \
--tconvert="observation_date,realtime_start_date" \
--filter="rel_ok(observation_date, realtime_start_date, 3)" \
--aggr=max(realtime_start_date)

# plus 6 months
join @fname plus6 --data=INDPRO --tkey=observation_date \
--tconvert="observation_date,realtime_start_date" \
--filter="rel_ok(observation_date, realtime_start_date, 6)" \
--aggr=max(realtime_start_date)

# plus 12 months
join @fname plus12 --data=INDPRO --tkey=observation_date \
--tconvert="observation_date,realtime_start_date" \
--filter="rel_ok(observation_date, realtime_start_date, 12)" \
--aggr=max(realtime_start_date)

setinfo firstpub --graph-name="First publication"
setinfo plus3 --graph-name="Plus 3 months"
setinfo plus6 --graph-name="Plus 6 months"
setinfo plus12 --graph-name="Plus 12 months"

# set --output=realtime.pdf for PDF
gnuplot firstpub plus3 plus6 plus12 --time --with-lines \
--output=display { set key left bottom; }


Chapter 8. Realtime data 72

A suitable script is shown in Listing 8.2. We first select an observation to track (January 1970). We
start the clock in the following month, when a data-point for this period was first published, and let
it run to the end of the vintage history (in this file, March 2013). Our outer time key is the realtime
start date and we filter on observation date; we name the imported INDPRO values as ip_jan70.
Since it sometimes happens that more than one revision occurs in a given month we need to select
an aggregation method: here we choose to take the last revision in the month.

Recall from section 8.2 that Alfred records a new revision only when the data-point in question
actually changes. This means that our imported series will contain missing values for all months
when no real revision took place. However, we can apply a simple autoregressive rule to fill in the
blanks: each missing value equals the prior non-missing value.

Figure 8.2 displays the revision history. Over this sample period the periodic re-basing of the index
overshadows amendments due to accrual of new information.

```
Listing 8.2: Retrieving a revision history [Download▼]
```
# choose the observation to track here (YYYYMMDD)
scalar target = 19700101

nulldata 518 --preserve
setobs 12 1970:02

join INDPRO.txt ip_jan70 --data=INDPRO --tkey=realtime_start_date \
--tconvert=observation_date \
--filter="observation_date==target" --aggr=seq:-1

ip_jan70 = ok(ip_jan70)? ip_jan70 : ip_jan70(-1)
gnuplot ip_jan70 --time --with-lines --output=display

```
20
```
```
40
```
```
60
```
```
80
```
```
100
```
```
120
```
```
140
```
```
160
```
```
180
```
```
1970 1975 1980 1985 1990 1995 2000 2005 2010
```
```
ip_jan70
```
```
Figure 8.2: Vintages of the index of US industrial production for January 1970
```

## Chapter 9

Temporal disaggregation

### 9.1 Introduction

This chapter describes and explains the facility for temporal disaggregation in gretl.^1 This is im-
plemented by the tdisagg function, which supports three variants of the method of Chow and Lin
(1971); the method of Fernández (1981); and two variants of the method of Denton (1971) as modi-
fied by Cholette (1984). Given the analytical similarities between them, the three Chow–Lin variants
and the Fernández method will be grouped in the discussion below as “Chow–Lin methods”.

The balance of this section provides a gentle introduction to the idea of temporal disaggregation;
experts may wish to skip to the next section.

Basically, temporal disaggregation is the business of taking time-series data observed at some given
frequency (say, annually) and producing a counterpart series at a higher frequency (say, quarterly).
The term “disaggregation” indicates the inverse operation of aggregation, and to understand tem-
poral disaggregation it’s helpful first to understand temporal aggregation. In aggregating a high
frequency series to a lower frequency there are three basic methods, the appropriate method de-
pending on the nature of the data. Here are some illustrative examples.

- GDP: say we have quarterly GDP data and wish to produce an annual series. This is a _flow_
    _variable_ and the annual flow will be the _sum_ of the quarterly values (unless the quarterly
    values are annualized, in which case we would aggregate by taking their mean).
- Industrial Production: this takes the form of an _index_ reporting the level of production over
    some period relative to that in a base period in which the index is by construction 100. To
    aggregate from (for example) monthly to quarterly we should take the _average_ of the monthly
    values. (The sum would give a nonsense result.) The same goes for price indices, and also for
    ratios of stocks to flows or vice versa (inventory to sales, debt to GDP, capacity utilization).
- Money stock: this is typically reported as an _end-of-period_ value, so in aggregating from
    monthly to quarterly we’d take the value from the final month of each quarter. In case a
    stock variable is reported as a _start-of-period_ value, the aggregated version would be that of
    the first month of the quarter.

A central idea in temporal disaggregation is that the high frequency series must respect both the
given low frequency data and the aggregation method. So for example, whatever numbers we come
up with for quarterly GDP, given an annual series as starting point, our numbers must sum to
the annual total. If money stock is measured at the end of the period then whatever numbers
we come up with for monthly money stock, given quarterly data, the figure for the last month of
the quarter must match that for the quarter as a whole. This is why temporal disaggregation is
sometimes called “benchmarking”: the given low frequency data constitute a benchmark which the
constructed high frequency data must match, in a well defined sense that depends on the nature
of the data.

Colloquially, we might describe temporal disaggregation as “interpolation,” but strictly speaking
interpolation applies only to stock variables. We have a known end-of-quarter value (say), which is
also the value at the end of the last month of the quarter, and we’re trying to figure out what the

(^1) We are grateful to Tommaso Di Fonzo, Professor of Statistical Science at the University of Padua, for detailed and
precise comments on earlier drafts. Any remaining errors are, of course, our responsibility.

#### 73


Chapter 9. Temporal disaggregation 74

value might have been at the end of months 1 and 2. We’re filling in the blanks, or interpolating.
In the GDP case, however, the procedure is _distribution_ rather than interpolation. We have a given
annual total and we’re trying to figure out how it should be distributed over the quarters. We’re
also doing distribution for variables taking the form of indices or ratios, except in this case we’re
seeking plausible values whose mean equals the given low-frequency value.

While matching the low frequency benchmark is an important constraint, it obviously does not
tie down the high frequency values. That is a job for either regression-based methods such as
Chow–Lin or non-regression methods such as Denton. Details are provided in section 9.7.

### 9.2 Notation and design

Some notation first: the two main ingredients in temporal disaggregation are

- a _T_ × _g_ matrix Y (holding the series to be disaggregated) and
- a matrix X with _k_ columns and _(s_ · _T_ + _m)_ rows (to aid in the disaggregation).

The idea is that Y contains time series data sampled at some frequency _f_ , while each column
of X contains time series data at a higher frequency, _sf_. So for each observation _Yt_ we have _s_
corresponding rows in X. The object is to produce a transformation of Y to frequency _sf_ , with
the help of X (whose columns are typically called “related series” or “indicators” in the temporal
disaggregation literature), via either distribution or interpolation depending on the nature of the
data. For most of this document we will assume that _g_ = 1, or in other words we are performing
temporal disaggregation on a single low-frequency series, but tdisagg supports “batch processing”
of several series and we return to this point in section 9.9.

If the _m_ in _(s_ · _T_ + _m)_ is greater than zero, that implies that there are some “extra” high-frequency
observations available for extrapolation — see section 9.4 for details.

We need to say something more about what goes into X. Under the Denton methods this must be a
single series, generally known as the “preliminary series”.^2 For the Chow–Lin methods, X can hold
a combination of deterministic terms (e.g. constant, trend) and stochastic series. Naturally, suitable
candidates for the role of preliminary series or indicator will be variables that are correlated with Y
(and in particular, might be expected to share short-run dynamics with Y). However, it is possible
to carry out disaggregation using deterministic terms only — in the simplest case, with X containing
nothing but a constant. Experts in the field tend to frown on this, with reason: in the absence of
any genuine high-frequency information disaggregation just amounts to a “mechanical” smoothing.
But some people may have a use for such smoothing, and it’s permitted by tdisagg.

We should draw attention to a design decision in tdisagg: we have separated the specification of
indicators in X from certain standard deterministic terms that might be wanted, namely, a constant,
linear trend or quadratic trend. If you want a disaggregation _without_ stochastic indicators, you can
omit (or set to null) the argument corresponding to X. In that case a constant (only) will be
employed automatically, but for the Chow–Lin methods one can adjust the deterministic terms
used via an option named det, described below. In other words the content of X becomes implicit.
See section 9.6 for more detail.

Here’s an important point to note when X is given explicitly: although this matrix may contain
extra observations “at the end” we assume that Y and X are _correctly aligned at the start_. Take
for example the annual to quarterly case: if the first observation in annual Y is for 1980 then the
first observation in quarterly X must be for the first quarter of 1980. Ensuring this is the user’s
responsibility. We will have some more to say about this in the following section.

(^2) There’s nothing to stop a user from _constructing_ such a series using several primary series as input — by taking the
first principal component or some other means — but that possibility is beyond our scope here.


Chapter 9. Temporal disaggregation 75

### 9.3 Overview of data handling

The tdisagg function has three basic arguments, representing Y, X and _s_ respectively (plus several
options; see below). The first two arguments can be given either in matrix form as such, or as
“dataset objects” — that is, a series for Y and a series or list of series for X. Or, as mentioned above,
X can be omitted (left implicit). This gives rise to five cases; which is most convenient will depend
on the user’s workflow.

1. Both Y and X are matrices. In this case, the size and periodicity of the currently open dataset
    (if any) are irrelevant. If Y has _T_ rows X must, of course, have at least _s_ · _T_ rows; if that
    condition is not satisfied an “Invalid argument” error will be flagged.
2. Y is a series (or list) and X a matrix. In this case we assume that the periodicity of the
    currently open dataset is the _lower_ one, and _T_ will be taken as equal to $nobs (the number of
    observations in the current sample range). Again, X must have at least _s_ · _T_ rows.
3. Y is a matrix and X a series or list. We then assume that the periodicity of the currently open
    dataset is the _higher_ one, so that $nobs defines ( _s_ · _T_ + _m_ ). And Y is supposed to be at the
    lower frequency, so its number of rows gives _T_. We should then be able to find _m_ as $nobs
    minus _s_ · _T_ ; if _m <_ 0 an error is flagged.
4. Both Y and X are “dataset objects”. We have two sub-cases here.
    (a) If X is a series, or an ordinary list of series, the periodicity of the currently open dataset is
       taken to be the _higher_ one. The series (or list) containing Y should hold the appropriate
       entries _everys elements_. For example, if _s_ = 4, _Y_ 1 will be taken from the first observation,
       _Y_ 2 from the fifth, _Y_ 3 from the ninth, and so on. In practical terms, series of this sort are
       likely to be composed by repeating each element of a low-frequency variable _s_ times.
(b) Alternatively, X could be a “MIDAS list”. The concept of a MIDAS list is fully explained in
chapter 20 but for example, in a quarterly dataset a MIDAS list would be a list of three
series, for the third, second and first month (note the ordering). In this case, the current
periodicity is taken to be the _lower_ one and X will contain one column, corresponding to
the high-frequency representation of the MIDAS list.
5. X is omitted. If Y is given as a matrix it is taken to have _T_ rows. Otherwise the interpretation
    is determined heuristically: if the Y series is recognized by gretl as composed of repeated
    low-frequency observations, or if a series result is requested, it is taken as having length _sT_ ,
    otherwise its length is taken to be _T_.

In the previous section we flagged the importance of correct alignment of X and Y at the start of the
data; we’re now in a position to say a little more about this. If either X or Y are given in matrix form
alignment is truly the user’s responsibility. But if they are dataset objects gretl can be more helpful.
We automatically advance the start of the sample range to exclude any leading missing values, and
retard the end of the sample ranges for X and Y to exclude trailing missing values (allowing for the
possibility that X may extend beyond Y). In addition we further advance the sample start if this is
required to ensure that the X data begin in the first high-frequency sub-period (e.g. the first quarter
of a year or the first month of a quarter). But please note: when gretl automatically excludes leading
or trailing missing values, intra-sample missing values will still provoke an error.

### 9.4 Extrapolation

As mentioned above, if X holds covariate data which extend beyond the range of the original series
to be disaggregated then extrapolation is supported. But this is inherently risky, and becomes
riskier the longer the horizon over which it is attempted. In tdisagg extrapolation is by default
limited to one low-frequency period (= _s_ high-frequency periods) beyond the end of the original
data. The user can adjust this behavior via the extmax member of the opts bundle passed to
tdisagg, described in the next section.


Chapter 9. Temporal disaggregation 76

### 9.5 Function signature

The signature of tdisagg is:

```
matrix tdisagg(Y0, [X], int s, [bundle opts], [bundle results])
```
where square brackets indicate optional arguments. Note that while the return value is a matrix, if
Y0 contains a single column or series it can be assigned to a series as in

```
series ys = tdisagg(Y0, ...)
```
provided it’s of the right length to match the current dataset, or the current sample range. Details
on the arguments follow.

Y0 : Y, as a matrix, series or list.

X (optional): X as a matrix, series or list. This should _not_ contain standard deterministic terms,
since they are handled separately (see det under opts below). If this matrix is omitted, then
disaggregation will be performed using deterministic terms only.

s (int): The temporal expansion factor, for example 3 for quarterly to monthly, 4 for annual to
quarterly or 12 for annual to monthly. We do not support cases such as monthly to weekly or
monthly to daily, where _s_ is not a fixed integer value common to all observations; otherwise,
anything goes.

opts (bundle, optional): a bundle holding additional options. The recognized keys are (in alpha-
betical order):

```
aggtype (string): Specifies the type of temporal aggregation appropriate to the series in ques-
tion. The value must be one of sum (each low-frequency value is a sum of s high-frequency
values, the default); avg (each low-frequency value is the average of s high frequency val-
ues); or last or first, indicating respectively that each low-frequency value is the last
or first of s high frequency values.
det (int): Relevant only when one of the Chow–Lin methods is selected. This is a numeric
code for the deterministic terms to be included in the regressions: 0 means none; 1,
constant only; 2, constant and linear trend; 3, constant and quadratic trend. The default
is 1.
extmax (int): the maximum number of high-frequency periods over which extrapolation should
be carried out, conditional on the availability of covariate data. A zero value means no
extrapolation; a value of −1 means as many periods as possible; and a positive value
limits extrapolation to the specified number of periods. See section 9.4 for a statement
of the default value.
method (string): Selects the method of disaggregation (see the listing below). Note that the
Chow–Lin methods employ an autoregression coefficient, ρ , which captures the persis-
tence of the target series at the higher frequency and is used in GLS estimation of the
parameters linking X to Y.
```
- chow-lin (the default) is modeled on the original method proposed by Chow and
    Lin. It uses a value of _ρ_ computed as the transformation of a maximum-likelihood
    estimate of the low-frequency autocorrelation coefficient.
- chow-lin-mle is equivalent to the method called chow-lin-maxlog in the tempdis-
    agg package for R; _ρ_ is estimated by iterated GLS using the loglikelihood as criterion,
    as recommended by Bournay and Laroque (1979). (The BFGS algorithm is used inter-
    nally).
- chow-lin-ssr is equivalent to the method called chow-lin-minrss-quilis in tem-
    pdisagg; _ρ_ is estimated by iterated GLS using the sum of squared GLS residuals as
    criterion (L-BFGS is used internally).


Chapter 9. Temporal disaggregation 77

- fernandez is basically “Chow–Lin with _ρ_ = 1”. It is suitable if the target series has a
    unit root, and is not cointegrated with the indicator series.
- denton-pfd is the proportional first differences variant of Denton, as modified by
    Cholette. See Di Fonzo and Marini (2012) for details.
- denton-afd is the additive first differences variant of Denton (again, as modified by
    Cholette). In contrast to the Chow–Lin methods, neither Denton procedure involves
    regression.
plot (int): If a non-zero value is given, a simple plot is displayed by way of a “sanity check”
on the final series. See section 9.8 for details.
rho (scalar): Relevant only when one of the Chow–Lin methods is selected. If the method
is chow-lin, then rho is treated as a fixed value for _ρ_ , thus enabling the user to by-
pass the default estimation procedure altogether. If the method is chow-lin-mle or
chow-lin-ssr, on the other hand, the supplied _ρ_ value is used to initialize the numeri-
cal optimization algorithm.
verbose (int): Controls the verbosity of Chow–Lin or Fernández output. If 0 (the default)
nothing is printed unless an error occurs; if 1, summary output from the relevant regres-
sion is shown; if 2, in addition output from the optimizer for the iterated GLS procedure
is shown, if applicable.

results (bundle, optional): If present, this argument must be a previously defined bundle. Upon
successful completion of any of the methods other than denton it contains details of the
disaggregation under the following keys:

```
method : the method employed
rho : the value of ρ used
lnl : loglikelihood (maximized by the chow-lin-mle method)
SSR : sum of squared residuals (minimized by the chow-lin-ssr method)
coeff : the GLS (or OLS) coefficients
stderr : standard errors for the coefficients
```
```
If ρ is set to zero — either by specification of the user or because the estimate ρ ˆ turned out
to be non-positive — then estimation of the coefficients is via OLS. In that case the lnl and
SSR values are calculated using the OLS residuals (which will be on a different scale from the
weighted residuals in GLS).
```
### 9.6 Handling of deterministic terms

It may be helpful to set out clearly, in one place, how deterministic terms are handled by tdisagg.

- If X is given explicitly: No deterministic term is added when the Denton method is used (since
    a single preliminary series is wanted) but a constant is added when one of the Chow–Lin
    methods is selected. The latter default can be overridden (i.e. the constant removed, or a
    trend added) by means of the det entry in the options bundle.
- If X is omitted: By default a constant is used for all methods. Again, for Chow–Lin this can be
    overridden by specifying a det value. If for some reason you wanted Denton with just a trend
    you would have to supply X containing a trend.

### 9.7 Some technical details

In this section we provide some technical details on the methods used by tdisagg. We will refer to
the version of Y converted to the high frequency _sf_ as the “final series”.


Chapter 9. Temporal disaggregation 78

As regards the Cholette-modified Denton methods, for the proportional first difference variant we
calculate the final series using the solution described by Di Fonzo and Marini (2012), specifically
equation (4) on page 5, and for the additive variant we draw on Di Fonzo (2003), pages 3 and 5 in
particular. Note that these procedures require the construction and inversion of a matrix of order
_(s_ + 1 _)T_. If both _s_ and _T_ are large it can therefore take some time, and be quite demanding of RAM.

As regards Chow–Lin, let _ρ_ 0 indicate the rho value passed via the options bundle (if applicable). We
then take these steps:

1. If _ρ_ 0 _>_ 0 set _ρ_ = _ρ_ 0 and go to step 6 if the method is chow-lin or step 7 otherwise. But if
    _ρ_ 0 _<_ 0 set _ρ_ 0 = 0.
2. Estimate via OLS a regression of Y on CX,^3 where C is the appropriate aggregation matrix. Let
    _β_ ˆOLSequal the coefficients from this regression. If _ρ_ 0 = 0 and the method is chow-lin go to
    step 8.
3. Calculate the (low frequency) first order autocorrelation of the OLS residuals, _ρ_ ˆ _L_. If _ρ_ ˆ _L_ ≥ 10 −^6
    go to step 4. Otherwise, if the method is chow-lin set _ρ_ = 0 and go to step 8, else set _ρ_ = 0_._ 5
    and go to step 7.
4. Refine the positive estimate of _ρ_ ˆ _L_ via Maximum Likelihood estimation of the AR(1) specifica-
    tion as described in Davidson and MacKinnon (2004).
5. If _ρ_ ˆ _L<_ 0_._ 999, set _ρ_ to the high-frequency counterpart of _ρ_ ˆ _L_ using the approach given in Chow
    and Lin (1971). Otherwise set _ρ_ = 0_._ 999. If the method is chow-lin, go to step 6, otherwise
    go to step 7.
6. Perform GLS with the given value of _ρ_ , store the coefficients as _β_ ˆGLSand go to step 9.
7. Perform iterated GLS starting from the prior value of _ρ_ , adjusting _ρ_ with the goal of either
    maximizing the loglikelihood (method chow-lin-mle) or minimizing the sum of squared GLS
    residuals (chow-lin-ssr); set _β_ ˆGLSto the final coefficient estimates; and go to step 9.
8. Calculate the final series as X _β_ ˆOLS+ C′ _(_ CC′ _)_ −^1 _u_ ˆOLS, where _u_ ˆOLSindicates the OLS residuals,
    and stop.
9. Calculate the final series as X _β_ ˆGLS+ VC′ _(_ CVC′ _)_ −^1 _u_ ˆGLS, where _u_ ˆGLSindicates the GLS residuals
    and V is the estimated high-frequency covariance matrix.

A few notes on our Chow–Lin algorithm follow.

- One might question the value of performing steps 2 to 5 when the method is one that calls
    for GLS iteration (chow-lin-mle or chow-lin-ssr), but our testing indicates that it can be
    helpful to have a reasonably good estimate of _ρ_ in hand before embarking on these iterations.
- Conversely, one might wonder why we bother with GLS iterations if we find _ρ_ ˆ _L<_ 10 −^6. But
    this allows for the possibility (most likely associated with small sample size) that iteration
    will lead to _ρ >_ 0 even when the estimate based on the intial OLS residuals is zero or negative.
- Note that in all cases we are discarding an estimate of _ρ <_ 0 (truncating to 0), which we take
    to be standard in this field. In our iterated GLS we achieve this by having the optimizer pick
    values _x_ in _[_ −∞ _,_ +∞ _]_ which are translated to _[_ 0 _,_ 1 _]_ via the logistic CDF, _ρ_ = 1 _/(_ 1 + exp _(_ − _x))_.
    To be precise, that’s the case with chow-lin-mle. But we find that the chow-lin-ssr method
    is liable to overestimate _ρ_ and proceed to values arbitrarily close to 1, resulting in numerical
    problems. We therefore bound this method to _x_ in _[_ − 20 _,_ + 6_._ 9 _]_ , corresponding to _ρ_ values
    between near-zero and approximately 0.999.^4

(^3) Strictly speaking, CX uses only the first _sT_ rows of X if _m >_ 0.
(^4) It may be worth noting that the tempdisagg package for R limits both methods to a maximum _ρ_ of 0.999. We find,
however, that the ML method can “look after itself”, and does not require the fixed upper bound short of 1.0.


Chapter 9. Temporal disaggregation 79

```
1600
```
```
1700
```
```
1800
```
```
1900
```
```
2000
```
```
2100
```
```
2200
```
```
2300
```
```
2400
```
```
1955 1956 1957 1958 1959 1960 1961 1962 1963 1964 1965
```
```
Temporal disaggregation (chow-lin)
```
```
original data
final series * 4
```
Figure 9.1: Example output from plot option, showing annual GNP (red) and quarterly final series (blue) using
quarterly industrial production as indicator.

As for the Fernández method, this is quite straightforward. The place of the high-frequency co-
variance matrix V in Chow–Lin is taken by _(_ D′D _)_ −^1 , where D is the approximate first-differencing
matrix, with 1 on the diagonal and−1 on the first sub-diagonal. For efficient computation, however,
we store neither D nor D′D as such, and do not perform any explicit inversion. The special struc-
ture of _(_ D′D _)_ −^1 makes it possible to produce the effect of pre-multiplication by this matrix with
_O(T_^2 _)_ floating-point operations. Estimation of _ρ_ is not an issue since it equals 1 by assumption.

### 9.8 The plot option

The semantics of this option may be enriched in future but for now it’s a simple boolean switch. The
effect is to produce a time series plot of the final series along with the original low-frequency series,
shown in “step” form. If aggregation is by sum the final series is multiplied by _s_ for comparability
with the original. If the disaggregation has been successful these two series should track closely
together, with the final series showing plausible short-run dynamics. An example is shown in
Figure 9.1.

If there are many observations, the two lines may appear virtually coincident. In that case one
can see what’s going on in more detail by exploiting the “Zoom” functionality of the plot, which is
accessed via the right-click menu in the plot window.

### 9.9 Multiple low-frequency series

We now return to a point mentioned in section 9.2, namely, that Y may be given as a _T_ × _g_ matrix
with _g >_ 1, or a list of _g_ series. This means that a single call to tdisagg can be used to process
several input series (“batch processing”), in which case the return value is a matrix with _(s_ · _T_ + _m)_
rows and _g_ columns.

There are some restrictions. First and most obviously, a single call to tdisagg implies a single
selection of “indicators” or “related series” (X) and a single selection of options (aggregation type
of the data, deterministic terms, disaggregation method, and so on). So this possibility will be
relevant only if you have several series that “want the same treatment.” In addition, if _g >_ 1 the
plot and verbose options are ignored and the results bundle is not filled; if you need those
features you should supply a single series or vector in Y.


Chapter 9. Temporal disaggregation 80

The advantage of batch processing lies in the spreading of fixed computational cost, leading to
shorter execution time. However, the relative importance of the fixed cost differs substantially
according to the disaggregation method. For the Chow–Lin methods the fixed cost is relatively
small and so little speed-up can be expected, but for the Denton methods it dominates, and (in our
testing) you can process _g >_ 1 series in little more time than it takes to process a single series.

As they say, “Your mileage may vary,” but if you have a large number of series to be disaggregated
via one of the Denton methods you may well find it much faster to use the batch facility of tdisagg.

### 9.10 Examples

Listing 9.1 shows an example of usage and its output. The data are drawn from the St Louis
Fed; we disaggregate quarterly GDP to monthly with the help of industrial production and payroll
employment, using the default Chow–Lin method.

Several other example scripts are available from [http://gretl.sourceforge.net/tdisagg/.](http://gretl.sourceforge.net/tdisagg/.)


Chapter 9. Temporal disaggregation 81

```
Listing 9.1: Example of tdisagg usage [Download▼]
```
### Traditional Chow-Lin: y is a series with repetition
### and X is a list of series. This corresponds to case 4(a)
### as described in section 9.3 of the documentation above.
###

# ensure that no data are in place
clear
# open gretl’s St Louis Fed database
open fedstl.bin
# import two monthly series
data indpro payems
# import quarterly GDP (values are repeated)
data gdpc1

# restrict sample to complete data
smpl --no-missing

# disaggregate GDP from quarterly to monthly, using
# industrial production and payroll employment as indicators
scalar s = 3
list X = indpro payems
series gdpm = tdisagg(gdpc1, X, s, _(verbose=1, aggtype="sum"))

Output:

Aggregation type sum
GLS estimates (chow-lin) T = 294
Dependent variable: gdpc1

```
coefficient std. error t-ratio p-value
----------------------------------------------------------
const 312.394 263.372 1.186 0.2365
indpro 10.9158 1.75785 6.210 1.83e-09 ***
payems 0.0242860 0.00171935 14.13 7.39e-35 ***
```
```
rho = 0.999, SSR = 51543.9, lnl = -1604.98
```
Generated series gdpm (ID 4)


## Chapter 10

Special functions in genr

### 10.1 Introduction

The genr command provides a flexible means of defining new variables. At the same time, the
somewhat paradoxical situation is that the “genr” keyword is almost never visible in gretl scripts.
For example, it is not really recommended to write a line such as genr b = 2.5, because there are
the following alternatives:

- scalar b = 2.5, which also invokes the genr apparatus in gretl, but provides explicit type
    information about the variable b, which is usually preferable. (gretl’s language hansl is stati-
    cally typed, so b cannot switch from scalar to string or matrix, for example.)
- b = 2.5, leaving it to gretl to infer the admissible or most “natural” type for the new object,
    which would again be a scalar in this case.
- matrix b = {2.5}: This formulation is required if b is going to be expanded with additional
    rows or columns later on. Otherwise, gretl’s static typing would not allow b to be promoted
    from scalar to matrix, so it must be a matrix right from the start, even if it is of dimension
    1 × 1 initially. (This definition could also be written as matrix b = 2.5, but the more explicit
    form is recommended.)

In addition to scalar or matrix, other type keywords that can be used to substitute the generic
genr term are those enumerated in the following chapter 11. In the case of an array the concrete
specification should be used, so one of matrices, strings, lists, bundles.^1

Therefore, there’s only a handful of special cases where it is really necessary to use the “genr”
keyword:

- genr time — Creates a time trend variable (1,2,3,... ) under the name time. Note that within
    an appropriately defined panel dataset this variable honors the panel structure and is a true
    time index. (In a cross-sectional dataset, the command will still work and produces the same
    result as genr index below, but of course no temporal meaning exists.)
- genr index — Creates an observation variable named index, running from 1 to the sample
    size.
- genr unitdum — In the context of panel data, creates a set of dummies for the panel groups
    or “units”. These are named du_1, du_2, and so forth. Actually, this particular genr usage is
    not strictly necessary, because a list of group dummies can also be obtained as:

```
series gr = $unit
list groupdums = dummify(gr, NA)
```
```
(The NA argument to the dummify function has the effect of not skipping any unit as the
reference group, thus producing the full set of dummies.)
```
(^1) A recently added advanced datatype is an array of arrays, with the associated type specifier arrays.

#### 82


Chapter 10. Special functions in genr 83

- genr timedum — Again for panel data, creates a set of dummies for the time periods, named
    dt_1, dt_2,.... And again, a list-producing variant without genr exists, using the special
    accessor $obsminor which indexes time in the panel context and can be used as a substitute
    for time from above:

```
series tindex = $obsminor
list timedums = dummify(tindex, NA)
```
- genr markers — See section 4.5 for an explanation and example of this panel-related feature.

Finally, there also exists genr dummy, which produces a set of seasonal dummies. However, it is
recommended to use the seasonals() function instead, which can also return centered dummies.

The rest of this chapter discusses other special function aspects.

### 10.2 Cumulative densities and p-values

The two functions cdf and pvalue provide complementary means of examining values from 17
probability distributions (as of July 2021), among which the most important ones: standard normal,
Student’s _t_ , _χ_^2 , _F_ , gamma, and binomial. The syntax of these functions is set out in the _Gretl
Command Reference_ ; here we expand on some subtleties.

The cumulative density function or CDF for a random variable is the integral of the variable’s
density from its lower limit (typically either −∞ or 0) to any specified value _x_. The p-value (at
least the one-tailed, right-hand p-value as returned by the pvalue function) is the complementary
probability, the integral from _x_ to the upper limit of the distribution, typically +∞.

In principle, therefore, there is no need for two distinct functions: given a CDF value _p_ 0 you could
easily find the corresponding p-value as 1− _p_ 0 (or vice versa). In practice, with finite-precision com-
puter arithmetic, the two functions are not redundant. This requires a little explanation. In gretl,
as in most statistical programs, floating point numbers are represented as “doubles” — double-
precision values that typically have a storage size of eight bytes or 64 bits. Since there are only so
many bits available, only so many floating-point numbers can be represented: _doubles do not model
the real line_. Typically doubles can represent numbers over the range (roughly) ± 1_._ 7977 × 10308 ,
but only to about 15 digits of precision.

Suppose you’re interested in the left tail of the _χ_^2 distribution with 50 degrees of freedom: you’d
like to know the CDF value for _x_ = 0_._ 9. Take a look at the following interactive session:

```
? scalar p1 = cdf(X, 50, 0.9)
Generated scalar p1 = 8.94977e-35
? scalar p2 = pvalue(X, 50, 0.9)
Generated scalar p2 = 1
? scalar test = 1 - p2
Generated scalar test = 0
```
The cdf function has produced an accurate value, but the pvalue function gives an answer of 1,
from which it is not possible to retrieve the answer to the CDF question. This may seem surprising
at first, but consider: if the value of p1 above is correct, then the correct value for p2 is 1− 8_._ 94977 ×
10 −^35. But there’s no way that value can be represented as a double: that would require over 30
digits of precision.

Of course this is an extreme example. If the _x_ in question is not too far off into one or other tail
of the distribution, the cdf and pvalue functions will in fact produce complementary answers, as
shown below:

```
? scalar p1 = cdf(X, 50, 30)
Generated scalar p1 = 0.0111648
```

Chapter 10. Special functions in genr 84

```
? scalar p2 = pvalue(X, 50, 30)
Generated scalar p2 = 0.988835
? scalar test = 1 - p2
Generated scalar test = 0.0111648
```
But the moral is that if you want to examine extreme values you should be careful in selecting the
function you need, in the knowledge that values very close to zero can be represented as doubles
while values very close to 1 cannot.

### 10.3 Retrieving internal variables (dollar accessors)

A very useful feature is to retrieve in a script various values calculated by gretl in the course of
estimating models or testing hypotheses. Since they all start with a literal $ character, they are
called “dollar accessors”. The variables that can be retrieved in this way are listed in the _Gretl
Command Reference_ or in the built-in function help under the Help menu. The dollar accessors
can be used like other gretl objects in script assignments or statements. Some of those accessors
are actually independent of any estimation or test and describe, for example, the context of the
running gretl program. But here we say a bit more about the special variables $test and $pvalue.

These variables hold, respectively, the value of the last test statistic calculated using an explicit
testing command and the p-value for that test statistic. If no such test has been performed at the
time when these variables are referenced, they will produce the missing value code. Some “explicit
testing commands” that work in this way are as follows (among others): add (joint test for the sig-
nificance of variables added to a model); adf (Augmented Dickey–Fuller test, see below); arch (test
for ARCH); chow (Chow test for a structural break); coeffsum (test for the sum of specified coef-
ficients); coint (Engle-Granger cointegration test); cusum (the Harvey–Collier _t_ -statistic); difftest
(test for a difference of two groups); kpss (KPSS stationarity test, no p-value available); modtest
(see below); meantest (test for difference of means); omit (joint test for the significance of vari-
ables omitted from a model); reset (Ramsey’s RESET); restrict (general linear restriction); runs
(runs test for randomness); and vartest (test for difference of variances). In most cases both a
$test and a $pvalue are stored; the exception is the KPSS test, for which a p-value is not currently
available.

The modtest command (which must follow an estimation command) offers several diagnostic tests;
the particular test performed depends on the option flag provided. Please see the _Gretl Command
Reference_ and for example chapters 32 and 31 of this _Guide_ for details.

An important point to notice about this mechanism is that the internal variables $test and $pvalue
are over-written each time one of the tests listed above is performed. If you want to reference these
values, you must do so at the correct point in the sequence of gretl commands.


## Chapter 11

Gretl data types

### 11.1 Introduction

Gretl offers the following data types:

```
scalar holds a single numerical value
series holds n numerical values, where n is the number of observations in the current
dataset
matrix holds a rectangular array of numerical values, of any (two) dimensions
list holds the ID numbers of a set of series
string holds an array of characters
bundle holds zero or more objects of various types
array holds zero or more objects of a given type
```
The “numerical values” mentioned above are all double-precision floating point numbers.

In this chapter we give a run-down of the basic characteristics of each of these types and also
explain their “life cycle” (creation, modification and destruction). The list and matrix types, whose
uses are relatively complex, are discussed at greater length in chapters 15 and 17 respectively.

### 11.2 Series

We begin with the series type, which is the oldest and in a sense the most basic type in gretl. When
you open a data file in the gretl GUI, what you see in the main window are the ID numbers, names
(and descriptions, if available) of the series read from the file. All the series existing at any point in
a gretl session are of the same length, although some may have missing values. The variables that
can be added via the items under the Add menu in the main window (logs, squares and so on) are
also series.

For a gretl session to contain any series, a common series length must be established. This is
usually achieved by opening a data file, or importing a series from a database, in which case the
length is set by the first import. But one can also use the nulldata command, which takes as it
single argument the desired length, a positive integer.

Each series has these basic attributes: an ID number, a name, and of course _n_ numerical values.
A series may also have a description (which is shown in the main window and is also accessible
via the labels command), a “display name” for use in graphs, a record of the compaction method
used in reducing the variable’s frequency (for time-series data only) and flags marking the variable
as discrete and/or as a numeric encoding of a qualitative characteristic. These attributes can be
edited in the GUI by choosing Edit Attributes (either under the Variable menu or via right-click), or
by means of the setinfo command.

In the context of most commands you are able to reference series by name or by ID number as you
wish. The main exception is the definition or modification of variables via a formula; here you must
use names since ID numbers would get confused with numerical constants.

Note that series ID numbers are always consecutive, and the ID number for a given series will change
if you delete a lower-numbered series. In some contexts, where gretl is liable to get confused by

#### 85


Chapter 11. Gretl data types 86

such changes, deletion of low-numbered series is disallowed.

Discrete series

It is possible to mark variables of the series type as _discrete_. The meaning and uses of this facility
are explained in chapter 12.

String-valued series

It is generally expected that series in gretl will be “properly numeric” (on a ratio or at least an
ordinal scale), or the sort of numerical indicator variables (0/1 “dummies”) that are traditional in
econometrics. However, “string-valued” series are also supported — see chapter 16 for details.

### 11.3 Scalars

The scalar type is relatively simple: just a convenient named holder for a single numerical value.
Scalars have none of the additional attributes pertaining to series, do not have ID numbers, and
must be referenced by name. A common use of scalar variables is to record information made
available by gretl commands for further processing, as in scalar s2 = $sigmaˆ2 to record the
square of the standard error of the regression following an estimation command such as ols.

You can define and work with scalars in gretl without having any dataset in place.

In the gretl GUI, scalar variables can be inspected and their values edited via the “Icon view” (see
the View menu in the main window).

### 11.4 Matrices

Matrices in gretl work much as in other mathematical software (e.g. MATLAB, Octave). Like scalars
they have no ID numbers and must be referenced by name, and they can be used without any
dataset in place. Matrix indexing is 1-based: the top-left element of matrix A is A[1,1]. Matrices
are discussed at length in chapter 17; advanced users of gretl will want to study this chapter in
detail.

Matrices have two optional attribute beyond their numerical content: they may have column and/or
row names attached; these are displayed when the matrix is printed. See the cnameset and
rnameset functions for details.

In the gretl GUI, matrices can be inspected, analysed and edited via the Icon view item under the
View menu in the main window: each currently defined matrix is represented by an icon.

### 11.5 Lists

As with matrices, lists merit an explication of their own (see chapter 15). Briefly, named lists can
(and should!) be used to make command scripts less verbose and repetitious, and more easily
modifiable. Since lists are in fact lists of series ID numbers they can be used only when a dataset is
in place.

In the gretl GUI, named lists can be inspected and edited under the Data menu in the main window,
via the item Define or edit list.

### 11.6 Strings

String variables may be used for labeling, or for constructing commands. They are discussed in
chapter 15. They must be referenced by name; they can be defined in the absence of a dataset.


Chapter 11. Gretl data types 87

Such variables can be created and modified via the command-line in the gretl console or via script;
there is no means of editing them via the gretl GUI.

### 11.7 Bundles

A bundle is a container or wrapper for various sorts of objects — primarily scalars, matrices,
strings, arrays and bundles. (Yes, a bundle can contain other bundles). Secondarily, series and
lists can be placed in bundles but this is subject to important qualifications noted below.

A bundle takes the form of a hash table or associative array: each item placed in the bundle is
associated with a key which can used to retrieve it subsequently. We begin by explaining the
mechanics of bundles then offer some thoughts on what they are good for.

There are several ways of creating a bundle. Here are the first two:

- Just “declare” it, as in

```
bundle foo
```
- or define an empty bundle using the defbundle function without any arguments:
    bundle foo = defbundle()

These formulations are basically equivalent, in that they both create an empty bundle. The differ-
ence is that the second variant may be reused — if a bundle named foo already exists the effect is
to empty it — while the first may only be used once in a given gretl session; it is an error to attempt
to declare a variable that already exists.

To create a bundle and add contents in one go, you can use the defbundle function with some
arguments. For example:

```
bundle foo = defbundle("x", 13, "mat", I(3), "str", "some string")
```
The arguments must be given in pairs — a key followed by the object to be associated with the key —
with all terms comma-separated. However, you may prefer to use one or other of the alternative
idioms introduced in gretl 2021a. The first of these looks like this:

```
bundle foo = _(x = 13, mat = I(3), str = "some string")
```
It’s more streamlined than defbundle but not quite so flexible. You don’t have to quote the keys,
but that also means that you can’t give the name of a key as a string variable; it’s always taken as a
string literal. Yet more streamlined but also less flexible is this variant:

```
bundle foo = _(x, mat, str)
```
which works if and only if there are existing objects x, mat and str in scope and you want to add
them to the bundle under keys equal to their own names.

For more on the defbundle function, see the _Gretl Command Reference_ or the Function Reference
under Help in the GUI program.

To add an object to a bundle you assign to a compound left-hand value: the name of the bundle
followed by the key. Two forms of syntax are acceptable in this context. The recommended syntax
(for most uses) is _bundlename_. _key_ ; that is, the name of the bundle followed by a dot, then the key.
Both the bundle name and the key must be valid gretl identifiers.^1 For example, the statement

```
foo.matrix1 = m
```
(^1) As a reminder: 31 characters maximum, starting with a letter and composed of just letters, numbers or underscore.


Chapter 11. Gretl data types 88

adds an object called m (presumably a matrix) to bundle foo under the key matrix1. If you wish to
make it explicit that m is supposed to be a matrix you can use the form

```
matrix foo.matrix1 = m
```
Alternatively, a bundle key may be given as a string enclosed in square brackets, as in

```
foo["matrix1"] = m
```
This syntax offers greater flexibility in that the key string does not have to be a valid identifier (for
example it can include spaces). In addition, when using the square bracket syntax it is possible to
use a string variable to define or access the key in question. For example:

```
string s = "matrix 1"
foo[s] = m # matrix is added under key "matrix 1"
```
To get an item out of a bundle, again use the name of the bundle followed by the key, as in

```
matrix bm = foo.matrix1
# or using the alternative notation
matrix bm = foo["matrix1"]
# or using a string variable
matrix bm = foo[s]
```
Note that the key identifying an object within a given bundle is necessarily unique. If you reuse an
existing key in a new assignment, the effect is to replace the object which was previously stored
under the given key. In this context it is not required that the type of the replacement object is the
same as that of the original.

Also note that when you add an object to a bundle, what in fact happens is that the bundle acquires
a _copy_ of the object. The external object retains its own identity and is unaffected if the bundled
object is replaced by another. Consider the following script fragment:

```
bundle foo
matrix m = I(3)
foo.mykey = m
scalar x = 20
foo.mykey = x
```
After the above commands are completed bundle foo does not contain a matrix under mykey, but
the original matrix m is still in good health.

To delete an object from a bundle use the delete command, with the bundle/key combination, as
in

```
delete foo.mykey
```
This destroys the object associated with mykey and removes the key from the hash table.

To determine whether a bundle contains an object associated with a given key, use the inbundle()
function. This takes two arguments: the name of the bundle and the key string. The value returned
by this function is an integer which codes for the type of the object (0 for no match, 1 for scalar, 2
for series, 3 for matrix, 4 for string, 5 for bundle and 6 for array). The function typestr() may be
used to get the string corresponding to this code. For example:

```
scalar type = inbundle(foo, x)
if type == 0
```

Chapter 11. Gretl data types 89

```
print "x: no such object"
else
printf "x is of type %s\n", typestr(type)
endif
```
Besides adding, accessing, replacing and deleting individual items, the other operations that are
supported for bundles are union, printing and deletion. As regards union, if bundles b1 and b2 are
defined you can say

```
bundle b3 = b1 + b2
```
to create a new bundle that is the union of the two others. The algorithm is: create a new bundle
that is a copy of b1, then add any items from b2 whose keys are not already present in the new
bundle. (This means that bundle union is not commutative if the bundles have one or more key
strings in common.)

If b is a bundle and you say print b, you get a listing of the bundle’s keys along with the types of
the corresponding objects, as in

```
? print b
bundle b:
x (scalar)
mat (matrix)
inside (bundle)
```
Note that in the example above the bundle b nests a bundle named inside. If you want to see
what’s inside nested bundles (with a single command) you can append the --tree option to the
print command.

Series and lists as bundle members

It is possible to add both series and lists to a bundle, as in

```
open data4-10
list X = const CATHOL INCOME
bundle b
b.y = ENROLL
b.X = X
eval b.y
eval b.X
```
However, it is important to bear in mind the following limitations.

- A series, as such, is inherently a member of a dataset, and a bundle can “survive” the replace-
    ment or destruction of the dataset from which a series was added. It may then be impossible
    (or, even if possible, meaningless) to extract a bundled series _as a series_. However it’s always
    possible to retrieve the values of the series in the form of a matrix (column vector).
- In gretl commands that call for series arguments you cannot give a bundled series without
    first extracting it. In the little example above the series ENROLL was added to bundle b under
    the key y, but b.y is not itself a series (member of a dataset), it’s just an anonymous array
    of values. It therefore cannot be given as, say, the dependent variable in a call to gretl’s ols
    command.
- A gretl list is just an array of ID numbers of series in a given dataset, a “macro” if you like.
    So as with series, there’s no guarantee that a bundled list can be extracted _as a list_ (though it
    can always be extracted as a row vector).


Chapter 11. Gretl data types 90

The points made above are illustrated in Listing 11.1. In “Case 1” we open a little dataset with just
14 cross-sectional observations and put a series into a bundle. We then open a time-series dataset
with 64 observations, while preserving the bundle, and extract the bundled series. This instance is
_legal_ , since the stored series does not overflow the length of the new dataset (it gets written into
the first 14 observations), but it’s probably not meaningful. It’s up to the user to decide if such
operations make sense.

In “Case 2” a similar sequence of statements leads to an error (trapped by catch) because this time
the stored series will not fit into the new dataset. We can nonetheless grab the data as a vector.

In “Case 3” we put a list of three series into a bundle. This does not put any actual data values into
the bundle, just the ID numbers of the specified series, which happen to be 4, 5 and 6. We then
switch to a dataset that contains just 4 series, so the list cannot be extracted as such (IDs 5 and 6
are out of bounds). Once again, however, we can retrieve the ID numbers in matrix form if we want.

In some cases putting a gretl list as such into a bundle may be appropriate, but in others you are
better off adding the _content_ of the list, in matrix form, as in

```
open data4-10
list X = const CATHOL INCOME
bundle b
matrix b.X = {X}
```
In this case we’re adding a matrix with three columns and as many rows as there are in the dataset;
we have the actual data, not just a reference to the data that might “go bad”. See chapter 17 for
more on this.

What are bundles good for?

Bundles are unlikely to be of interest in the context of standalone gretl scripts, but they can be
very useful in the context of complex function packages where a good deal of information has to
be passed around between the component functions (see Cottrell and Lucchetti, 2016). Instead of
using a lengthy list of individual arguments, function _A_ can bundle up the required data and pass
it to functions _B_ and _C_ , where relevant information can be extracted via a mnemonic key.

In this context bundles should be passed in “pointer” form (see chapter 14) as illustrated in the fol-
lowing trivial example, where a bundle is created at one level then filled out by a separate function.

```
# modification of bundle (pointer) by user function
```
```
function void fill_out_bundle (bundle *b)
b.mat = I(3)
b.str = "foo"
b.x = 32
end function
```
```
bundle my_bundle
fill_out_bundle(&my_bundle)
```
The bundle type can also be used to advantage as the _return value_ from a packaged function, in
cases where a package writer wants to give the user the option of accessing various results. In
the gretl GUI, function packages that return a bundle are treated specially: the output window that
displays the printed results acquires a menu showing the bundled items (their names and types),
from which the user can save items of interest. For example, a function package that estimates a
model might return a bundle containing a vector of parameter estimates, a residual series and a
covariance matrix for the parameter estimates, among other possibilities.

When offering a bundle as the return value from a function it’s important to keep in mind the
limitation noted above, concerning the inclusion of lists in bundles. Once again: a list is just an
array of series ID numbers. Consider the following would-be function code.


Chapter 11. Gretl data types 91

```
Listing 11.1: Series and lists in bundles [Download▼]
```
# Case 1: store and retrieve series, OK?
open data4-1
bundle b
series b.x = sqft
open data9-7 --preserve
series x = b.x
print x --byobs

# Case 2: store and retrieve series: gives an error,
# but the data can be retrieved in matrix form
open data9-7
bundle b
series b.x = QNC
open data4-1 --preserve
catch series x = b.x # wrong, won’t fit!
if $error
matrix mx = b.x
print mx
else
print x
endif

# Case 3: store and retrieve list: gives an error,
# but the ID numbers in the list can be retrieved
# as a row vector
open data9-7
list L = PRIME UNEMP STOCK
bundle b
list b.L = L
open data4-1 --preserve
catch list L = b.L
if $error
matrix mL = b.L
print mL # prints "4 5 6"
endif


Chapter 11. Gretl data types 92

```
function bundle bunlist (const series y)
series y2 = y^2
series y3 = y^3
bundle ret
# don’t do this!
list ret.L = y2 y3
return ret
end function
```
If the intent is to give the caller a list containing two new series this will _not_ work. Suppose that
when this function is called, the caller has in place a dataset with two series (besides the built-in
const), with ID numbers 1 and 2. Then the series y2 and y3 will be given IDs 3 and 4, which will
be duly recorded in ret.L. But these series are local to the function; at caller level there will be no
series answering to IDs 3 and 4, and the “list” therefore turns into the useless vector { 3 _,_ 4 }. If you
want to return multiple series your options are (a) return a list _directly_ — in which case gretl adds
the specified series to the caller’s dataset — or (b) turn the list into a a matrix, as in

```
list L = y2 y3
matrix Y = {L}
```
This matrix can be returned in its own right, or can be packed into a bundle if the function is
to return something else besides; either way the caller can reconstitute a list using the mat2list
function.

You might be wondering, if the direct return of a list works as mentioned above, why doesn’t a
bundled list work in the same way? That’s basically because of the “encapsulation” policy: func-
tions should not have any unexpected side effects. If a caller assigns the return value of a function
that advertises a list return, it should be clear that the caller’s dataset may be modified — it’s all
“above board”. If a function that advertises a bundle return value has the side effect of modify-
ing the caller’s dataset, because the bundle happens to contain a list, that would seem to break
encapsulation.

For completeness, it’s worth noting that there are cases where a function _can_ successfully return a
list in a bundle, without breaking encapsulation: the requirement is just that the series IDs in the
list are defined at caller level. Listing 11.2 gives an example. A list argument L is examined and
the return value is a bundle containing a list and a vector. The bundled list includes the IDs of just
those series in L that are discrete, and the vector gives the number of distinct values for each of
these series.

Adding annotations

As a refinement to support the use of bundles as a function return type, the setnote function can
be used to add a brief explanatory note to a bundled item — such notes will then be shown in the
GUI menu. This function takes three arguments: the name of a bundle, a key string, and the note.
For example

```
setnote(b, "vcv", "covariance matrix")
```
After this, the object under the key vcv in bundle b will be shown as “covariance matrix” in a GUI
menu.

### 11.8 Arrays

The gretl array type is intended for scripting use. Arrays have no GUI representation and they’re
unlikely to acquire one.^2

(^2) However, it’s possible to save arrays “invisibly” in the context of a GUI session, by virtue of the fact that they can be
packed into bundles (see below), and bundles can be saved as part of a “session”.


Chapter 11. Gretl data types 93

```
Listing 11.2: Returning a list in a bundle [Download▼]
```
set verbose off

function bundle discrete_check (const list L)
list dlist
matrix nvals = {}
bundle b
loop i=1..nelem(L)
b = getinfo(L[i])
if b.discrete
dlist += L[i]
nvals ~= nelem(values(L[i]))
endif
endloop
return _(dlist, nvals)
end function

open mroz87.gdt --quiet
list L = dataset
bundle b = discrete_check(L)
list print b.dlist

A gretl array is, as you might expect, a container which can hold zero or more objects of a certain
type, indexed by consecutive integers starting at 1. It is one-dimensional. This type is implemented
by a quite “generic” back-end. The types of object that can be put into arrays are strings, matrices,
lists, bundles and arrays.^3

Of gretl’s “primary” types, then, neither scalars nor series are supported by the array mechanism.
There would be little point in supporting arrays of scalars as such since the matrix type already
plays that role, and more flexibly. As for series, they have a special status as elements of a dataset
(which is in a sense an “array of series” already) and in addition we have the list type which already
functions as a sort of array for subsets of the series in a dataset.

Creating an array

An array can be brought into existence in any of three ways: bare declaration or using one of the
functions array() or defarray(). In each case one of the specific type-words strings, matrices,
lists, bundles or arrays must be used. Here are some examples:

```
# declare an empty array of strings
strings S
# make an empty array of matrices
matrices M = array(0)
# make an array with space for four bundles
bundles B = array(4)
# make an array with three specified strings
strings P = defarray("foo", "bar", "baz")
```
The “bare declaration” form and the function form with array(0) have the same effect of creating
an empty array, but the second can be used in contexts where bare declaration is not allowed
(and it can also be used to destroy the content of an existing array and reduce it to size zero).

(^3) It was not possible to nest arrays prior to version 2019d of gretl.


Chapter 11. Gretl data types 94

The array() function expects a non-negative integer argument and can be used to create an array
of pre-given size; in this case the elements are initialized appropriately as empty strings, empty
matrices, empty lists, empty bundles or empty arrays. The defarray() function takes a variable
number of arguments (one or more), each of which may be the name of a variable of the appropriate
type or an expression which evaluates to an object of the appropriate type.

Setting and getting elements

There are two ways to set the value of an array element: you can set a particular element using the
array index, or you can append an element using the += operator:

```
# first case
strings S = array(3)
S[2] = "string the second"
# alternative
matrices M = array(0)
M += mnormal(T,k)
```
In the first method the index must (of course) be within bounds; that is, greater than zero and
no greater than the current length of the array. When the second method is used it automatically
extends the length of the array by 1.

To get hold of an element, the array index must be used:

```
# for S an array of strings
string s = S[5]
# for M an array of matrices
printf "\n%#12.5g\n", M[1]
```
Removing elements

There’s a counterpart to the += operator mentioned above: -= can be used to remove one or more
elements specified by _content_ from an array of strings. Note that -= works on all matching ele-
ments, so after the following statements

```
strings S = defarray("a", "a", "b", "a")
S -= "a"
```
S becomes a one-element array holding only the original third element.

More generally, a negative index can be used to remove a specified element from an array of any
type, as in

```
strings S = defarray("a", "a", "b", "a")
S = S[-1]
```
where only the first element is removed. See chapter 17 for more on the semantics of negative
indices.

Operations on whole arrays

Three operators are applicable to whole arrays, but only one to arrays of arbitrary type (the other
two being restricted to arrays of strings). The generally available operation is appending. You can
do, for example

```
# for M1 and M2 both arrays of matrices
matrices BigM = M1 + M2
# or if you wish to augment M1
M1 += M2
```

Chapter 11. Gretl data types 95

In each case the result is an array of matrices whose length is the sum of the lengths of M1 and
M2 — and similarly for the other supported types.

The operators specific to strings are union, via ||, and intersection, via &&. Given the following
code, for S1 and S2 both arrays of strings,

```
strings Su = S1 || S2
strings Si = S1 && S2
```
the array Su will contain all the strings in S1 plus any in S2 that are not in S1, while Si will contain
all and only the strings that appear in both S1 and S2.

Arrays as function arguments

One can write hansl functions that take as arguments any of the array types, and it is possible to
pass arrays as function arguments in “pointerized” form. In addition hansl functions may return
any of the array types. Here is a trivial example for strings:

```
function void printstrings (strings *S)
loop i=1..nelem(S)
printf "element %d: ’%s’\n", i, S[i]
endloop
end function
```
```
function strings mkstrs (int n)
strings S = array(n)
loop i=1..n
S[i] = sprintf("member %d", i)
endloop
return S
end function
```
```
strings Foo = mkstrs(5)
print Foo
printstrings(&Foo)
```
A couple of points are worth noting here. First, the nelem() function works to give the number of
elements in any of the “container” types (lists, arrays, bundles, matrices). Second, if you do “print
Foo” for Foo an array, you’ll see something like:

```
? print Foo
Array of strings, length 5
```
Nesting arrays

While gretl’s array structure is in itself one-dimensional you can add extra dimensions by nesting.
For example, the code below creates an array holding _n_ arrays of _m_ bundles.

```
arrays BB = array(n)
loop i=1..n
bundles BB[i] = array(m)
endloop
```
The syntax for setting or accessing any of the _n_ × _m_ bundles (or their members) is then on the
following pattern:

```
BB[i][j].m = I(3)
eval BB[i][j]
eval BB[i][j].m # or eval BB[i][j]["m"]
```

Chapter 11. Gretl data types 96

where the respective array subscripts are each put into square brackets.

The elements of an array of arrays must (obviously) all be arrays, but it’s not required that they
have a common content-type. For example, the following code creates an array holding an array of
matrices plus an array of strings.

```
arrays AA = array(2)
matrices AA[1] = array(3)
strings AA[2] = array(3)
```
Arrays and bundles

As mentioned, the bundle type is supported by the array mechanism. In addition, arrays (of what-
ever type) can be put into bundles:

```
matrices M = array(8)
# set values of M[i] here...
bundle b
b.M = M
```
The mutual “packability” of bundles and arrays means that it’s possible to go quite far down the
rabbit-hole... users are advised not to get carried away.

### 11.9 The life cycle of gretl objects

Creation

The most basic way to create a new variable of any type is by _declaration_ , where one states the type
followed by the name of the variable to create, as in

```
scalar x
series y
matrix A
```
and so forth. In that case the object in question is given a default initialization, as follows: a new
scalar has value NA (missing); a new series is filled with NAs; a new matrix is empty (zero rows
and columns); a new string is empty; a new list has no members, new bundles and new arrays are
empty.

Declaration can be supplemented by a definite initialization, as in

```
scalar x = pi
series y = log(x)
matrix A = zeros(10,4)
```
The type of a new variable can be left implicit, as in

```
x = y/100
z = 3.5
```
Here the type of x will be determined automatically depending on the context. If y is a scalar,
a series or a matrix x will inherit y’s type (otherwise an error will be generated, since division is
applicable to these types only). The new variable z will “naturally” be of scalar type.

In general, however, we recommend that you state the type of a new variable explicitly. This makes
the intent clearer to a reader of the script and also guards against errors that might otherwise be
difficult to understand (i.e. a certain variable turns out to be of the wrong type for some subsequent
calculation, but you don’t notice at first because you didn’t say what type you wanted). Exceptions
to this rule might reasonably be granted for clear and simple cases where there’s little possibility
of confusion.


Chapter 11. Gretl data types 97

Modification

Typically, the values of variables of all types are modified by assignment, using the = operator with
the name of the variable on the left and a suitable value or formula on the right:

```
z = normal()
x = 100 * log(y) - log(y(-1))
M = qform(a, X)
```
By a “suitable” value we mean one that is conformable for the type in question. A gretl variable
acquires its type when it is first created and this cannot be changed via assignment; for example, if
you have a matrix A and later want a string A, you will have to delete the matrix first.

☞ One point to watch out for in gretl scripting is type conflicts having to do with the names of series brought
in from a data file. For example, in setting up a command loop (see chapter 13) it is very common to call
the loop index i. Now a loop index is a scalar (typically incremented each time round the loop). If you open
a data file that happens to contain a series named i you will get a type error (“Types not conformable for
operation”) when you try to use i as a loop index.

Although the type of an existing variable cannot be changed on the fly, gretl nonetheless tries to be
as “understanding” as possible. For example if x is an existing series and you say

```
x = 100
```
gretl will give the series a constant value of 100 rather than complaining that you are trying to
assign a scalar to a series. This issue is particularly relevant for the matrix type — see chapter 17
for details.

Besides using the regular assignment operator you also have the option of using an “inflected”
equals sign, as in the C programming language. This is shorthand for the case where the new value
of the variable is a function of the old value. For example,

```
x += 100 # in longhand: x = x + 100
x *= 100 # in longhand: x = x * 100
```
For scalar variables you can use a more condensed shorthand for simple increment or decrement
by 1, namely trailing ++ or -- respectively:

```
x = 100
x-- # x now equals 99
x++ # x now equals 100
```
In the case of objects holding more than one value — series, matrices and bundles — you can mod-
ify particular values within the object using an expression within square brackets to identify the
elements to access. We have discussed this above for the bundle type and chapter 17 goes into
details for matrices. As for series, there are two ways to specify particular values for modification:
you can use a simple 1-based index, or if the dataset is a time series or panel (or if it has marker
strings that identify the observations) you can use an appropriate observation string. Such strings
are displayed by gretl when you print data with the --byobs flag. Examples:

```
x[13] = 100 # simple index: the 13th observation
x[1995:4] = 100 # date: quarterly time series
x[2003:08] = 100 # date: monthly time series
x["AZ"] = 100 # the observation with marker string "AZ"
x[3:15] = 100 # panel: the 15th observation for the 3rd unit
```

Chapter 11. Gretl data types 98

Note that with quarterly or monthly time series there is no ambiguity between a simple index
number and a date, since dates always contain a colon. With annual time-series data, however,
such ambiguity exists and it is resolved by the rule that a number in brackets is always read as a
simple index: x[1905] means the nineteen-hundred and fifth observation, _not_ the observation for
the year 1905. You can specify a year by quotation, as in x["1905"].

Destruction

Objects of the types discussed above, _with the important exception of named lists_ , are all destroyed
using the delete command: delete _objectname_.

Lists are an exception for this reason: in the context of gretl commands, a named list expands to
the ID numbers of the member series, so if you say

```
delete L
```
for L a list, the effect is to delete all the series in L; the list itself is not destroyed, but ends up
empty. To delete the list itself (without deleting the member series) you must invert the command
and use the list keyword:

```
list L delete
```
Note that the delete command cannot be used within a loop construct (see chapter 13).


## Chapter 12

Discrete variables

When a variable can take only a finite, typically small, number of values, then it is said to be _discrete_.
In gretl, variables of the series type (only) can be marked as discrete. (When we speak of “variables”
below this should be understood as referring to series.) Some gretl commands act in a slightly
different way when applied to discrete variables; moreover, gretl provides a few commands that
only apply to discrete variables. Specifically, the dummify and xtab commands (see below) are
available only for discrete variables, while the freq (frequency distribution) command produces
different output for discrete variables.

### 12.1 Declaring variables as discrete

Gretl uses a simple heuristic to judge whether a given variable should be treated as discrete, but
you also have the option of explicitly marking a variable as discrete, in which case the heuristic
check is bypassed.

The heuristic is as follows: First, are all the values of the variable “reasonably round”, where this
is taken to mean that they are all integer multiples of 0.25? If this criterion is met, we then ask
whether the variable takes on a “fairly small” set of distinct values, where “fairly small” is defined
as less than or equal to 8. If both conditions are satisfied, the variable is automatically considered
discrete.

To mark a variable as discrete you have two options.

1. From the graphical interface, select “Variable, Edit Attributes” from the menu. A dialog box
    will appear and, if the variable seems suitable, you will see a tick box labeled “Treat this
    variable as discrete”. This dialog box can also be invoked via the context menu (right-click on
    a variable) or by pressing the F2 key.
2. From the command-line interface, via the discrete command. The command takes one or
    more arguments, which can be either variables or list of variables. For example:
       list xlist = x1 x2 x3
       discrete z1 xlist z2

```
This syntax makes it possible to declare as discrete many variables at once, which cannot
presently be done via the graphical interface. The switch --reverse reverses the declaration
of a variable as discrete, or in other words marks it as continuous. For example:
discrete foo
# now foo is discrete
discrete foo --reverse
# now foo is continuous
```
The command-line variant is more powerful, in that you can mark a variable as discrete even if it
does not seem to be suitable for this treatment.

Note that marking a variable as discrete does not affect its content. It is the user’s responsibility
to make sure that marking a variable as discrete is a sensible thing to do. Note that if you want to
recode a continuous variable into classes, you can use gretl’s arithmetical functionality, as in the
following example:

#### 99


Chapter 12. Discrete variables 100

```
nulldata 100
# generate a series with mean 2 and variance 1
series x = normal() + 2
# split into 4 classes
series z = (x>0) + (x>2) + (x>4)
# now declare z as discrete
discrete z
```
Once a variable is marked as discrete, this setting is remembered when you save the data file.

### 12.2 Commands for discrete variables

The **dummify** command

The dummify command takes as argument a series _x_ and creates dummy variables for each distinct
value present in _x_ , which must have already been declared as discrete. Example:

```
open greene22_2
discrete Z5 # mark Z5 as discrete
dummify Z5
```
The effect of the above command is to generate 5 new dummy variables, labeled DZ5_1 through
DZ5_5, which correspond to the different values in Z5. Hence, the variable DZ5_4 is 1 if Z5 equals
4 and 0 otherwise. This functionality is also available through the graphical interface by selecting
the menu item “Add, Dummies for selected discrete variables”.

The dummify command can also be used with the following syntax:

```
list dlist = dummify(x)
```
This not only creates the dummy variables, but also a named list (see section 15.1) that can be used
afterwards. The following example computes summary statistics for the variable Y for each value
of Z5:

```
open greene22_2
discrete Z5 # mark Z5 as discrete
list foo = dummify(Z5)
loop foreach i foo
smpl $i --restrict --replace
summary Y
endloop
smpl --full
```
Since dummify generates a list, it can be used directly in commands that call for a list as input, such
as ols. For example:

```
open greene22_2
discrete Z5 # mark Z5 as discrete
ols Y 0 dummify(Z5)
```
The **freq** command

The freq command displays absolute and relative frequencies for a given variable. The way fre-
quencies are counted depends on whether the variable is continuous or discrete. This command is
also available via the graphical interface by selecting the “Variable, Frequency distribution” menu
entry.


Chapter 12. Discrete variables 101

For discrete variables, frequencies are counted for each distinct value that the variable takes. For
continuous variables, values are grouped into “bins” and then the frequencies are counted for each
bin. The number of bins, by default, is computed as a function of the number of valid observations
in the currently selected sample via the rule shown in Table 12.1. However, when the command is
invoked through the menu item “Variable, Frequency Plot”, this default can be overridden by the
user.

```
Observations Bins
8 ≤ n < 16 5
16 ≤ n < 50 7
50 ≤ n ≤ 850 ⌈
```
#### √

```
n ⌉
n > 850 29
```
```
Table 12.1: Number of bins for various sample sizes
```
For example, the following code

```
open greene19_1
freq TUCE
discrete TUCE # mark TUCE as discrete
freq TUCE
```
yields

```
Read datafile /usr/local/share/gretl/data/greene/greene19_1.gdt
periodicity: 1, maxobs: 32,
observations range: 1-32
```
```
Listing 5 variables:
0) const 1) GPA 2) TUCE 3) PSI 4) GRADE
```
```
? freq TUCE
```
```
Frequency distribution for TUCE, obs 1-32
number of bins = 7, mean = 21.9375, sd = 3.90151
```
```
interval midpt frequency rel. cum.
```
```
< 13.417 12.000 1 3.12% 3.12% *
13.417 - 16.250 14.833 1 3.12% 6.25% *
16.250 - 19.083 17.667 6 18.75% 25.00% ******
19.083 - 21.917 20.500 6 18.75% 43.75% ******
21.917 - 24.750 23.333 9 28.12% 71.88% **********
24.750 - 27.583 26.167 7 21.88% 93.75% *******
>= 27.583 29.000 2 6.25% 100.00% **
```
```
Test for null hypothesis of normal distribution:
Chi-square(2) = 1.872 with p-value 0.39211
? discrete TUCE # mark TUCE as discrete
? freq TUCE
```
```
Frequency distribution for TUCE, obs 1-32
```
```
frequency rel. cum.
```
```
12 1 3.12% 3.12% *
14 1 3.12% 6.25% *
17 3 9.38% 15.62% ***
```

Chapter 12. Discrete variables 102

#### 19 3 9.38% 25.00% ***

#### 20 2 6.25% 31.25% **

#### 21 4 12.50% 43.75% ****

#### 22 2 6.25% 50.00% **

#### 23 4 12.50% 62.50% ****

#### 24 3 9.38% 71.88% ***

#### 25 4 12.50% 84.38% ****

#### 26 2 6.25% 90.62% **

#### 27 1 3.12% 93.75% *

#### 28 1 3.12% 96.88% *

#### 29 1 3.12% 100.00% *

```
Test for null hypothesis of normal distribution:
Chi-square(2) = 1.872 with p-value 0.39211
```
As can be seen from the sample output, a Doornik–Hansen test for normality is computed auto-
matically. This test is suppressed for discrete variables where the number of distinct values is less
than 10.

This command accepts two options: --quiet, to avoid generation of the histogram when invoked
from the command line and --gamma, for replacing the normality test with Locke’s nonparametric
test, whose null hypothesis is that the data follow a Gamma distribution.

If the distinct values of a discrete variable need to be saved, the values() matrix construct can be
used (see chapter 17).

The **xtab** command

The xtab command cab be invoked in either of the following ways. First,

```
xtab ylist ; xlist
```
where ylist and xlist are lists of discrete variables. This produces cross-tabulations (two-way
frequencies) of each of the variables in ylist (by row) against each of the variables in xlist (by
column). Or second,

```
xtab xlist
```
In the second case a full set of cross-tabulations is generated; that is, each variable in xlist is tabu-
lated against each other variable in the list. In the graphical interface, this command is represented
by the “Cross Tabulation” item under the View menu, which is active if at least two variables are
selected.

Here is an example of use:

```
open greene22_2
discrete Z* # mark Z1-Z8 as discrete
xtab Z1 Z4 ; Z5 Z6
```
which produces

```
Cross-tabulation of Z1 (rows) against Z5 (columns)
```
```
[ 1][ 2][ 3][ 4][ 5] TOT.
```
```
[ 0] 20 91 75 93 36 315
[ 1] 28 73 54 97 34 286
```
```
TOTAL 48 164 129 190 70 601
```

Chapter 12. Discrete variables 103

```
Pearson chi-square test = 5.48233 (4 df, p-value = 0.241287)
```
```
Cross-tabulation of Z1 (rows) against Z6 (columns)
```
```
[ 9][ 12][ 14][ 16][ 17][ 18][ 20] TOT.
```
```
[ 0] 4 36 106 70 52 45 2 315
[ 1] 3 8 48 45 37 67 78 286
```
```
TOTAL 7 44 154 115 89 112 80 601
```
```
Pearson chi-square test = 123.177 (6 df, p-value = 3.50375e-24)
```
```
Cross-tabulation of Z4 (rows) against Z5 (columns)
```
```
[ 1][ 2][ 3][ 4][ 5] TOT.
```
```
[ 0] 17 60 35 45 14 171
[ 1] 31 104 94 145 56 430
```
```
TOTAL 48 164 129 190 70 601
```
```
Pearson chi-square test = 11.1615 (4 df, p-value = 0.0248074)
```
```
Cross-tabulation of Z4 (rows) against Z6 (columns)
```
```
[ 9][ 12][ 14][ 16][ 17][ 18][ 20] TOT.
```
```
[ 0] 1 8 39 47 30 32 14 171
[ 1] 6 36 115 68 59 80 66 430
```
```
TOTAL 7 44 154 115 89 112 80 601
```
```
Pearson chi-square test = 18.3426 (6 df, p-value = 0.0054306)
```
Pearson’s _χ_^2 test for independence is automatically displayed, provided that all cells have expected
frequencies under independence greater than 10−^7. However, a common rule of thumb states that
this statistic is valid only if the expected frequency is 5 or greater for at least 80 percent of the
cells. If this condition is not met a warning is printed.

Additionally, the --row or --column options can be given: in this case, the output displays row or
column percentages, respectively.

If you want to cut and paste the output of xtab to some other program, e.g. a spreadsheet, you
may want to use the --zeros option; this option causes cells with zero frequency to display the
number 0 instead of being empty.


## Chapter 13

Loop constructs

### 13.1 Introduction

The command loop opens a special mode in which gretl accepts a block of commands to be re-
peated zero or more times. This feature may be useful for, among other things, Monte Carlo
simulations, bootstrapping of test statistics and iterative estimation procedures. The general form
of a loop is:

```
loop control-expression [ --progressive | --verbose ]
loop body
endloop
```
Five forms of control-expression are available, as explained in section 13.2.

Not all gretl commands are available within loops; the commands that are not presently accepted
in this context are shown in Table 13.1.

```
Table 13.1: Commands not usable in loops
```
```
function include nulldata quit run setmiss
```
By default, the genr command operates quietly in the context of a loop (without printing informa-
tion on the variable generated). To force the printing of feedback you may specify the --verbose
option to loop.

The --progressive option to loop modifies the behavior of the commands print and store,
and certain estimation commands, in a manner that may be useful with Monte Carlo analyses (see
Section 13.4).

The following sections explain the various forms of the loop control expression and provide some
examples of use of loops.

☞ If you are carrying out a substantial Monte Carlo analysis with many thousands of repetitions, memory
capacity and processing time may be an issue. To minimize the use of computer resources, run your script
using the command-line program, gretlcli, with output redirected to a file.

### 13.2 Loop control variants

Count loop

The simplest form of loop control is a direct specification of the number of times the loop should
be repeated. We refer to this as a “count loop”. The number of repetitions may be a numerical
constant, as in loop 1000, or may be read from a scalar variable, as in loop replics.

In the case where the loop count is given by a variable, say replics, in concept replics is an
integer; if the value is not integral, it is converted to an integer by truncation. Note that replics is
evaluated only once, when the loop is initially compiled.

#### 104


Chapter 13. Loop constructs 105

While loop

A second sort of control expression takes the form of the keyword while followed by a Boolean
expression. For example,

```
loop while essdiff > .00001
```
Execution of the commands within the loop will continue so long as (a) the specified condition
evaluates as true and (b) the number of iterations does not exceed the value of the internal variable
loop_maxiter. By default this equals 100000, but you can specify a different value (or remove the
limit) via the set command (see the _Gretl Command Reference_ ).

Index loop

A third form of loop control uses an index variable, for example i.^1 In this case you specify starting
and ending values for the index, as in loop i=1..20.

The index variable may be a pre-existing scalar; if this is not the case, the variable is created
automatically and is destroyed on exit from the loop.

The index may be used within the loop body in either of two ways: you can access the integer value
of i or you can use its string representation, $i.

The starting and ending values for the index can be given in numerical form, by reference to pre-
defined scalar variables, or as expressions that evaluate to scalars. In the latter two cases the
variables are evaluated once, at the start of the loop. In addition, with time series data you can give
the starting and ending values in the form of dates, as in loop i=1950:1..1999:4 for quarterly
data.

This form of loop control is intended to be quick and easy, and as such it is subject to certain
limitations. In particular, standard behavior is to increment the index variable by one at each
iteration. So, for example, if you have

```
loop i=m..n
```
where m and n are scalar variables with values m _>_ n at the time of execution, the index will not be
decremented; rather, the loop will simply be bypassed.

One modification of this behavior is supported, via the option flag --decr (or -d for short). This
causes the index to be decremented by one at each iteration. For example,

```
loop i=m..n --decr
```
In this case the loop will be bypassed if m _<_ n. If you need more flexible control, see the “for” form
below.

The index loop is particularly useful in conjunction with the values() matrix function when some
operation must be carried out for each value of some discrete variable (see chapter 12). Consider
the following example:

```
open greene22_2
discrete Z8
v8 = values(Z8)
loop i=1..rows(v8)
scalar xi = v8[i]
smpl Z8==xi --restrict --replace
printf "mean(Y | Z8 = %g) = %8.5f, sd(Y | Z8 = %g) = %g\n", \
xi, mean(Y), xi, sd(Y)
endloop
```
(^1) It is common programming practice to use simple, one-character names for such variables.


Chapter 13. Loop constructs 106

In this case, we evaluate the conditional mean and standard deviation of the variable Y for each
value of Z8.

Foreach loop

The fourth form of loop control also uses an index variable, in this case to index a specified set
of strings. The loop is executed once for each string in the list. This can be useful for performing
repetitive operations on a list of variables. Here is an example of the syntax:

```
loop foreach i peach pear plum
print "$i"
endloop
```
This loop will execute three times, printing out “peach”, “pear” and “plum” on the respective itera-
tions. The numerical value of the index starts at 1 and is incremented by 1 at each iteration.

If you wish to loop across a list of variables that are contiguous in the dataset, you can give the
names of the first and last variables in the list, separated by “..”, rather than having to type all
the names. For example, say we have 50 variables AK, AL,... , WY, containing income levels for the
states of the US. To run a regression of income on time for each of the states we could do:

```
genr time
loop foreach i AL..WY
ols $i const time
endloop
```
This loop variant can also be used for looping across the elements in a _named list_ (see chapter 15).
For example:

```
list ylist = y1 y2 y3
loop foreach i ylist
ols $i const x1 x2
endloop
```
Note that if you use this idiom inside a function (see chapter 14), looping across a list that has been
supplied to the function as an argument, it is necessary to use the syntax _listname_ .$i to reference
the list-member variables. In the context of the example above, this would mean replacing the third
line with

```
ols ylist.$i const x1 x2
```
Two other cases are supported: the target of foreach can be a named array of strings or a bundle
(see chapter 11). In the array case, $i gets (naturally) the string at position i in the array, from
1 to the number of elements; in the bundle case it gets the key-strings of all bundle members (in
no particular order). For a bundle b, the command “print b” gives a fairly terse account of the
bundle’s membership; for a full account you can do:

```
loop foreach i b
print "$i:"
eval b["$i"]
endloop
```
For loop

The final form of loop control emulates the for statement in the C programming language. The
syntax is loop for, followed by three component expressions, separated by semicolons and sur-
rounded by parentheses. The three components are as follows:


Chapter 13. Loop constructs 107

1. Initialization: This is evaluated only once, at the start of the loop. Common example: setting
    a scalar control variable to some starting value.
2. Continuation condition: this is evaluated at the top of each iteration (including the first). If
    the expression evaluates as true (non-zero), iteration continues, otherwise it stops. Common
    example: an inequality expressing a bound on a control variable.
3. Modifier: an expression which modifies the value of some variable. This is evaluated prior
    to checking the continuation condition, on each iteration after the first. Common example: a
    control variable is incremented or decremented.

Here’s a simple example:

```
loop for (r=0.01; r<.991; r+=.01)
```
In this example the variable r will take on the values 0.01, 0.02,... , 0.99 across the 99 iterations.
Note that due to the finite precision of floating point arithmetic on computers it may be necessary
to use a continuation condition such as the above, r<.991, rather than the more “natural” r<=.99.
(Using double-precision numbers on an x86 processor, at the point where you would expect r to
equal 0.99 it may in fact have value 0.990000000000001.)

Any or all of the three expressions governing a for loop may be omitted — the minimal form is
(;;). If the continuation test is omitted it is implicitly true, so you have an infinite loop unless you
arrange for some other way out, such as a break statement (see section 13.3 below).

If the initialization expression in a for loop takes the common form of setting a scalar variable to
a given value, the string representation of that scalar’s value is made available within the loop via
the accessor $ _varname_.

### 13.3 Special controls

Besides the control afforded by the governing expression at the top of a loop, the flow of execution
can be adjusted via the keywords break and continue.

The break keyword terminates execution of the current loop immediately, while continue has the
effect of skipping any subsequent statements within the loop on the current iteration; execution
will proceed to the next iteration if the condition for continuation is still satisfied.

### 13.4 Progressive mode

If the --progressive option is given for a command loop, special behavior is invoked for certain
commands, namely, print, store and simple estimation commands. By “simple” here we mean
commands which (a) estimate a single equation (as opposed to a system of equations) and (b) do
so by means of a single command statement (as opposed to a block of statements, as with nls and
mle). The paradigm is ols; other possibilities include tsls, wls, logit and so on.

The special behavior is as follows.

Estimators: The results from each individual iteration of the estimator are not printed. Instead,
after the loop is completed you get a printout of (a) the mean value of each estimated coefficient
across all the repetitions, (b) the standard deviation of those coefficient estimates, (c) the mean
value of the estimated standard error for each coefficient, and (d) the standard deviation of the
estimated standard errors. Note that this is useful only if there is some random input at each step.

print: When this command is used to print the value of a variable, its value is not printed each
time round the loop. Rather, when the loop is terminated you get a printout of the mean and
standard deviation of the variable, across the repetitions of the loop. This mode is intended for use


Chapter 13. Loop constructs 108

with variables that have a scalar value at each iteration, for example the sum of squared residuals
from a regression. Series cannot be printed in this way, and neither can matrices.

store: This command writes out the values of the specified scalars, from each time round the
loop, to a specified file. Thus it keeps a complete record of their values across the iterations. For
example, coefficient estimates could be saved in this way so as to permit subsequent examination
of their frequency distribution. Only one such store can be used in a given loop.

### 13.5 Loop examples

Monte Carlo example

A simple example of a Monte Carlo loop in “progressive” mode is shown in Listing 13.1.

```
Listing 13.1: Simple Monte Carlo loop [Download▼]
```
nulldata 50
set seed 547
series x = 100 * uniform()
# open a "progressive" loop, to be repeated 100 times
loop 100 --progressive
series u = 10 * normal()
# construct the dependent variable
series y = 10*x + u
# run OLS regression
ols y const x
# grab the coefficient estimates and R-squared
scalar a = $coeff(const)
scalar b = $coeff(x)
scalar r2 = $rsq
# arrange for printing of stats on these
print a b r2
# and save the coefficients to file
store coeffs.gdt a b
endloop

This loop will print out summary statistics for the a and b estimates and _R_^2 across the 100 rep-
etitions. After running the loop, coeffs.gdt, which contains the individual coefficient estimates
from all the runs, can be opened in gretl to examine the frequency distribution of the estimates in
detail.

The nulldata command is useful for Monte Carlo work. Instead of opening a “real” data set,
nulldata 50 (for instance) creates an artificial dataset, containing just a constant and an index
variable, with 50 observations. Constructed variables can then be added. See the set command for
information on generating repeatable pseudo-random series.

Iterated least squares

Listing 13.2 uses a “while” loop to replicate the estimation of a nonlinear consumption function of
the form
_C_ = _α_ + _βYγ_ + _ε_

as presented in Greene (2000), Example 11.3. This script is included in the gretl distribution under
the name greene11_3.inp; you can find it in gretl under the menu item “File, Script files, Example
scripts, Greene...”.


Chapter 13. Loop constructs 109

The option --print-final for the ols command arranges matters so that the regression results
will not be printed each time round the loop, but the results from the regression on the last iteration
will be printed when the loop terminates.

```
Listing 13.2: Nonlinear consumption function [Download▼]
```
open greene11_3.gdt
# run initial OLS
ols C 0 Y
scalar essbak = $ess
scalar essdiff = 1
scalar beta = $coeff(Y)
scalar gamma = 1

# iterate OLS till the error sum of squares converges
loop while essdiff > .00001
# form the linearized variables
series C0 = C + gamma * beta * Y^gamma * log(Y)
series x1 = Y^gamma
series x2 = beta * Y^gamma * log(Y)
# run OLS
ols C0 0 x1 x2 --print-final --no-df-corr --vcv
beta = $coeff[2]
gamma = $coeff[3]
ess = $ess
essdiff = abs(ess - essbak)/essbak
essbak = ess
endloop

# print parameter estimates using their "proper names"
printf "alpha = %g\n", $coeff[1]
printf "beta = %g\n", beta
printf "gamma = %g\n", gamma

Listing 13.3 shows how a loop can be used to estimate an ARMA model, exploiting the “outer
product of the gradient” (OPG) regression discussed by Davidson and MacKinnon (1993).

Further examples of loop usage that may be of interest can be found in chapter 21.


Chapter 13. Loop constructs 110

```
Listing 13.3: ARMA 1, 1 [Download▼]
```
# Estimation of an ARMA(1,1) model "manually", using a loop

open arma.gdt

scalar c = 0
scalar a = 0.1
scalar m = 0.1

series e = 0.0
series de_c = e
series de_a = e
series de_m = e

scalar crit = 1

loop while crit > 1.0e-9
# one-step forecast errors
e = y - c - a*y(-1) - m*e(-1)

```
# log-likelihood
scalar loglik = -0.5 * sum(e^2)
print loglik
```
```
# partials of e with respect to c, a, and m
de_c = -1 - m * de_c(-1)
de_a = -y(-1) -m * de_a(-1)
de_m = -e(-1) -m * de_m(-1)
```
```
# partials of l with respect to c, a and m
series sc_c = -de_c * e
series sc_a = -de_a * e
series sc_m = -de_m * e
```
```
# OPG regression
ols const sc_c sc_a sc_m --print-final --no-df-corr --vcv
```
```
# Update the parameters
c += $coeff[1]
a += $coeff[2]
m += $coeff[3]
```
```
# show progress
printf " constant = %.8g (gradient %#.6g)\n", c, $coeff[1]
printf " ar1 coefficient = %.8g (gradient %#.6g)\n", a, $coeff[2]
printf " ma1 coefficient = %.8g (gradient %#.6g)\n", m, $coeff[3]
```
crit = $T - $ess
print crit
endloop

scalar se_c = $stderr[1]
scalar se_a = $stderr[2]
scalar se_m = $stderr[3]

printf "\n"
printf "constant = %.8g (se = %#.6g, t = %.4f)\n", c, se_c, c/se_c
printf "ar1 coefficient = %.8g (se = %#.6g, t = %.4f)\n", a, se_a, a/se_a
printf "ma1 coefficient = %.8g (se = %#.6g, t = %.4f)\n", m, se_m, m/se_m


## Chapter 14

User-defined functions

### 14.1 Defining a function

Gretl offers a mechanism for defining functions, which may be called via the command line, in
the context of a script, or (if packaged appropriately, see section 14.5) via the program’s graphical
interface.

The syntax for defining a function looks like this:

function _type funcname_ ( _parameters_ )
_function body_
end function

The opening line of a function definition contains these elements, in strict order:

1. The keyword function.
2. _type_ , which states the type of value returned by the function, if any. This must be one of void
    (if the function does not return anything), scalar, series, matrix, list, string, bundle or
    one of gretl’s array types, matrices, bundles, strings (see section 11.8).
3. _funcname_ , the unique identifier for the function. Function names have a maximum length of
    31 characters; they must start with a letter and can contain only letters, numerals and the
    underscore character. You will get an error if you try to define a function having the same
    name as an existing gretl command.
4. The function’s _parameters_ , in the form of a comma-separated list enclosed in parentheses.
    This may be run into the function name, or separated by white space as shown. In case the
    function takes no arguments (unusual, but acceptable) this should be indicated by placing the
    keyword void between the parameter-list parentheses.

Function parameters can be of any of the types shown below.^1

```
Type Description
bool scalar variable acting as a Boolean switch
int scalar variable acting as an integer
scalar scalar variable
series data series
list named list of series
matrix matrix or vector
string string variable or string literal
bundle all-purpose container (see section 11.7)
matrices array of matrices (see section 11.8)
bundles array of bundles
strings array of strings
```
(^1) An additional parameter type is available for GUI use, namely obs; this is equivalent to int except for the way it is
represented in the graphical interface for calling a function.

#### 111


Chapter 14. User-defined functions 112

Each element in the listing of parameters must include two terms: a type specifier, and the name
by which the parameter shall be known within the function. An example follows:

```
function scalar myfunc (series y, list xvars, bool verbose)
```
Each of the type-specifiers, with the exception of list and string, may be modified by prepending
an asterisk to the associated parameter name, as in

```
function scalar myfunc (series *y, scalar *b)
```
The meaning of this modification is explained below (see section 14.4); it is related to the use of
pointer arguments in the C programming language.

Function parameters: optional refinements

Besides the required elements mentioned above, the specification of a function parameter may
include some additional fields, as follows:

- The const modifier.
- For scalar or int parameters: minimum, maximum and/or default values; or for bool pa-
    rameters, just a default value. And in addition for scalar parameters, a step size.
- For optional arguments other than scalar, int and bool, the special default value null.
- For all parameters, a descriptive string.
- For int parameters with minimum and maximum values specified, a set of strings to associate
    with the allowed numerical values (that is, value labels).

The first three of these options may be useful in many contexts; the last two may be helpful if a
function is to be packaged for use in the gretl GUI (but probably not otherwise). We now expand on
each of the options.

- The const modifier: must be given as a prefix to the basic parameter specification, as in

```
const matrix M
```
```
This constitutes a promise that the corresponding argument will not be modified within the
function; gretl will flag an error if the function attempts to modify the argument.
```
- Minimum, maximum and default values for scalar or int types: These values should di-
    rectly follow the name of the parameter, enclosed in square brackets and with the individual
    elements separated by colons. For example, suppose we have an integer parameter order for
    which we wish to specify a minimum of 1, a maximum of 12, and a default of 4. We can write

```
int order[1:12:4]
```
```
If you wish to omit any of the three specifiers, leave the corresponding field empty. For
example [1::4] would specify a minimum of 1 and a default of 4 while leaving the maximum
unlimited. However, as a special case, it is acceptable to give just one value, with no colons,
in which case the value is interpreted as a default. So for example
```
```
int k[0]
```
```
designates a default value of 0 for the parameter k, with no minimum or maximum specified.
If you wished to specify a minimum of zero with no maximum or default you would have to
write
```

Chapter 14. User-defined functions 113

```
int k[0::]
```
```
For a parameter of type bool (whose values are just zero or non-zero), you can specify a
default of 1 (true) or 0 (false), as in
```
```
bool verbose[0]
```
- Descriptive string: This will show up as an aid to the user if the function is packaged (see
    section 14.5 below) and called via gretl’s graphical interface. The string should be enclosed
    in double quotes and separated from the preceding elements of the parameter specification
    with a space, as in

```
series y "dependent variable"
```
- Value labels: These may be used only with int parameters for which minimum and maximum
    values have been specified (so that there is a fixed number of admissible values) and the
    number of labels must match the number of values. They will show up in the graphical
    interface in the form of a drop-down list, making the function writer’s intent clearer when an
    integer argument represents a categorical selection. A set of value labels must be enclosed in
    braces, and the individual labels must be enclosed in double quotes and separated by commas
    or spaces. For example:

```
int case[1:3:1] {"Fixed effects", "Between model", "Random effects"}
```
- Step size: This is only supported only for real-valued scalar parameters. It is relevant only
    in the graphical interface, and must be combined with specification of minimum, maximum
    and default values. The effect is that the argument selector takes the form of a “spin button”:
    clicking on the up- or down-buttons in the selector changes the value by the specified step.
    Otherwise the selector for such a parameter simply appears as an entry box into which a
    number should be typed. For example, the following could be used to stipulate that a scalar
    argument should have a minimum of 1, a maximum of 10, a default of 4 and a step size of
    0_._ 1:
       scalar x[1:10:4:0.1]

If two or more of the trailing optional fields are given in a parameter specification, they must be
given in the order shown above: min/max/default, description, value labels. Note that there is
no facility for “escaping” characters within descriptive strings or value labels; these may contain
spaces but they cannot contain the double-quote character.

Here is an example of a well-formed function specification using all the elements mentioned above:

```
function matrix myfunc (series y "dependent variable",
list X "regressors",
int p[0::1] "lag order",
int c[1:2:1] "criterion" {"AIC", "BIC"},
bool quiet[0])
```
One advantage of specifying default values for parameters, where applicable, is that in script or
command-line mode users may omit trailing arguments that have defaults. For example, myfunc
above could be invoked with just two arguments, corresponding to y and X; implicitly p = 1, c = 1
and quiet is false.

Functions taking no parameters

You may define a function that has no parameters (these are called “routines” in some programming
languages). In this case, use the keyword void in place of the listing of parameters:

```
function matrix myfunc2 (void)
```

Chapter 14. User-defined functions 114

The function body

The _function body_ is composed of gretl commands, or calls to user-defined functions (that is,
function calls may be nested). A function may call itself (that is, functions may be recursive). While
the function body may contain function calls, it may not contain function definitions. That is, you
cannot define a function inside another function. For further details, see section 14.4.

### 14.2 Calling a function

A user function is called by typing its name followed by zero or more arguments enclosed in
parentheses. If there are two or more arguments they must be separated by commas.

There are automatic checks in place to ensure that the number of arguments given in a function
call matches the number of parameters, and that the types of the given arguments match the types
specified in the definition of the function. An error is flagged if either of these conditions is violated.
One qualification: allowance is made for omitting arguments at the end of the list, provided that
default values are specified in the function definition. To be precise, the check is that the number
of arguments is at least equal to the number of _required_ parameters, and is no greater than the
total number of parameters.

In general, an argument to a function may be given either as the name of a pre-existing variable or
as an expression which evaluates to a variable of the appropriate type.

The following trivial example illustrates a function call that correctly matches the corresponding
function definition.

```
# function definition
function scalar ols_ess (series y, list xvars)
ols y 0 xvars --quiet
printf "ESS = %g\n", $ess
return $ess
end function
```
```
# main script
open data4-1
list xlist = 2 3 4
# function call (the return value is ignored here)
ols_ess(price, xlist)
```
The function call gives two arguments: the first is a data series specified by name and the second is
a named list of regressors. Note that while the function offers the Error Sum of Squares as a return
value, it is ignored by the caller in this instance. (As a side note here, if you want a function to
calculate some value having to do with a regression, but are not interested in the full results of the
regression, you may wish to use the --quiet flag with the estimation command as shown above.)

A second example shows how to write a function call that assigns a return value to a variable in the
caller:

```
# function definition
function series get_uhat (series y, list xvars)
ols y 0 xvars --quiet
return $uhat
end function
```
```
# main script
open data4-1
list xlist = 2 3 4
# function call
series resid = get_uhat(price, xlist)
```

Chapter 14. User-defined functions 115

### 14.3 Deleting a function

If you have defined a function and subsequently wish to clear it out of memory, you can do so using
the keywords delete or clear, as in

```
function myfunc delete
function get_uhat clear
```
Note, however, that if myfunc is already a defined function, providing a new definition automatically
overwrites the previous one, so it should rarely be necessary to delete functions explicitly.

### 14.4 Function programming details

Variables versus pointers

Most arguments to functions can be passed in two ways: “as they are”, or via pointers (the exception
is the list type, which cannot be passed as a pointer). First consider the following rather artificial
example:

```
function series triple1 (series x)
return 3*x
end function
```
```
function void triple2 (series *x)
x *= 3
end function
```
```
nulldata 10
series y = normal()
series y3 = triple1(y)
print y3
triple2(&y)
print y
```
These two functions produce essentially the same result — the two print statements in the caller
will show the same values — but in quite different ways. The first explicitly returns a modified
version of its input (which must be a plain series): after the call to triple1, y is unaltered; it
would have been altered only if the return value were assigned back to y rather than y3. The
second function modifies its input (given as a pointer to a series) in place without actually _returning_
anything.

It’s worth noting that triple2 as it stands would _not_ be considered idiomatic as a gretl function
(although it’s formally OK). The point here is just to illustrate the distinction between passing an
argument in the default way and in pointer form.

Why make this distinction? There are two main reasons for doing so: modularity and performance.

By modularity we mean the insulation of a function from the rest of the script which calls it. One of
the many benefits of this approach is that your functions are easily reusable in other contexts. To
achieve modularity, _variables created within a function are local to that function, and are destroyed
when the function exits_ , unless they are made available as return values and these values are “picked
up” or assigned by the caller. In addition, functions do not have access to variables in “outer scope”
(that is, variables that exist in the script from which the function is called) except insofar as these
are explicitly passed to the function as arguments.

By default, when a variable is passed to a function as an argument, what the function actually “gets”
is a _copy_ of the outer variable, which means that the value of the outer variable is not modified by
anything that goes on inside the function. This means that you can pass arguments to a function


Chapter 14. User-defined functions 116

without worrying about possible side effects; at the same time the function writer can use argument
variables as workspace without fear of disruptive effects at the level of the caller.

The use of pointers, however, allows a function and its caller to cooperate such that an outer
variable _can_ be modified by the function. In effect, this allows a function to “return” more than one
value (although only one variable can be returned directly — see below). To indicate that a particular
object is to be passed as a pointer, the parameter in question is marked with a prefix of * in the
function definition, and the corresponding argument is marked with the complementary prefix & in
the caller. For example,

```
function series get_uhat_and_ess(series y, list xvars, scalar *ess)
ols y 0 xvars --quiet
ess = $ess
series uh = $uhat
return uh
end function
```
```
open data4-1
list xlist = 2 3 4
scalar SSR
series resid = get_uhat_and_ess(price, xlist, &SSR)
```
In the above, we may say that the function is given the _address_ of the scalar variable SSR, and it
assigns a value to that variable (under the local name ess). (For anyone used to programming in C:
note that it is not necessary, or even possible, to “dereference” the variable in question within the
function using the * operator. Unadorned use of the name of the variable is sufficient to access the
variable in outer scope.)

An “address” parameter of this sort can be used as a means of offering optional information to the
caller. (That is, the corresponding argument is not strictly needed, but will be used if present). In
that case the parameter should be given a default value of null and the the function should test to
see if the caller supplied a corresponding argument or not, using the built-in function exists().
For example, here is the simple function shown above, modified to make the filling out of the ess
value optional.

```
function series get_uhat_and_ess(series y, list xvars, scalar *ess[null])
ols y 0 xvars --quiet
if exists(ess)
ess = $ess
endif
return $uhat
end function
```
If the caller does not care to get the ess value, it can use null in place of a real argument:

```
series resid = get_uhat_and_ess(price, xlist, null)
```
Alternatively, trailing function arguments that have default values may be omitted, so the following
would also be a valid call:

```
series resid = get_uhat_and_ess(price, xlist)
```
One limitation on the use of pointer-type arguments should be noted: you cannot supply a given
variable as a pointer argument more than once in any given function call. For example, suppose we
have a function that takes two matrix-pointer arguments,

```
function scalar pointfunc (matrix *a, matrix *b)
```

Chapter 14. User-defined functions 117

And suppose we have two matrices, x and y, at the caller level. The call

```
pointfunc(&x, &y)
```
is OK, but the call

```
pointfunc(&x, &x) # will not work
```
will generate an error. That’s because the situation inside the function would become too confusing,
with the same object present under two different names.

Const parameters

Pointer-type arguments may also be useful for optimizing performance. Even if a variable is not
modified inside the function, it may be a good idea to pass it as a pointer if it occupies a lot of
memory. Otherwise, the time gretl spends transcribing the value of the variable to the local copy
may be non-negligible compared to the time the function spends doing the job it was written for.

Listing 14.1 takes this to the extreme. We define two functions which return the number of rows
of a matrix (a pretty fast operation). The first gets a matrix as argument while the second gets a
pointer to a matrix. The functions are evaluated 500 times on a matrix with 2000 rows and 2000
columns; on a typical system floating-point numbers take 8 bytes of memory, so the total size of
the matrix is roughly 32 megabytes.

Running the code in example 14.1 will produce output similar to the following (the actual numbers
of course depend on the machine you’re using):

```
Elapsed time:
without pointers (copy) = 2.47197 seconds,
with pointers (no copy) = 0.00378627 seconds
```
If a pointer argument is used for this sort of purpose — and the object to which the pointer points
is not modified (is treated as read-only) by the function — one can signal this to the user by adding
the const qualifier, as shown for function rowcount2 in Listing 14.1. When a pointer argument is
qualified in this way, any attempt to modify the object within the function will generate an error.

However, combining the const flag with the pointer mechanism is technically redundant for the
following reason: if you mark a matrix argument as const then gretl will in fact pass it in pointer
mode internally (since it can’t be modified within the function there’s no downside to simply mak-
ing it available to the function rather than copying it). So in the example above we could revise the
signature of the second function as

```
function scalar rowcount2a (const matrix X)
```
and call it with r = rowcount2a(X), for the same speed-up relative to rowcount1.

From the caller’s point of view the second option — using the const modifier _without_ pointer
notation — is preferable, as it allows the caller to pass an object created “on the fly”. Suppose
the caller has two matrices, A and B, in scope, and wishes to pass their vertical concatenation as an
argument. The following call would work fine:

```
r = rowcount2a(A|B)
```
To use rowcount2, on the other hand, the caller would have to create a named variable first (since
you cannot give the “address” of a anonymous object such as A|B):

```
matrix AB = A|B
r = rowcount2(&AB)
```

Chapter 14. User-defined functions 118

```
Listing 14.1: Performance comparison: values versus pointer [Download▼]
```
function scalar rowcount1 (matrix X)
return rows(X)
end function

function scalar rowcount2 (const matrix *X)
return rows(X)
end function

set verbose off
X = zeros(2000,2000)
scalar r

set stopwatch
loop 500
r = rowcount1(X)
endloop
e1 = $stopwatch

set stopwatch
loop 500
r = rowcount2(&X)
endloop
e2 = $stopwatch

printf "Elapsed time:\n\
without pointers (copy) = %g seconds,\n \
with pointers (no copy) = %g seconds\n", e1, e2


Chapter 14. User-defined functions 119

This requires an extra line of code, and leaves AB occupying memory after the call.

We have illustrated using a matrix parameter, but the const modifier may be used with the same
effect — namely, the argument is passed directly, without being copied, but is protected against
modification within the function — for all the types that support the pointer apparatus.

List arguments

The use of a named list as an argument to a function gives a means of supplying a function with
a set of variables whose number is unknown when the function is written — for example, sets of
regressors or instruments. Within the function, the list can be passed on to commands such as
ols.

A list argument can also be “unpacked” using a foreach loop construct, but this requires some
care. For example, suppose you have a list X and want to calculate the standard deviation of each
variable in the list. You can do:

```
loop foreach i X
scalar sd_$i = sd(X.$i)
endloop
```
_Please note_ : a special piece of syntax is needed in this context. If we wanted to perform the above
task on a list in a regular script (not inside a function), we could do

```
loop foreach i X
scalar sd_$i = sd($i)
endloop
```
where $i gets the name of the variable at position _i_ in the list, and sd($i) gets its standard
deviation. But inside a function, working on a list supplied as an argument, if we want to reference
an individual variable in the list we must use the syntax _listname.varname_. Hence in the example
above we write sd(X.$i).

This is necessary to avoid possible collisions between the name-space of the function and the name-
space of the caller script. For example, suppose we have a function that takes a list argument, and
that defines a local variable called y. Now suppose that this function is passed a list containing
a variable named y. If the two name-spaces were not separated either we’d get an error, or the
external variable y would be silently over-written by the local one. It is important, therefore, that
list-argument variables should not be “visible” by name within functions. To “get hold of” such
variables you need to use the form of identification just mentioned: the name of the list, followed
by a dot, followed by the name of the variable.

Constancy of list arguments When a named list of variables is passed to a function, the function
is actually provided with a copy of the list. The function may modify this copy (for instance, adding
or removing members), but the original list at the level of the caller is not modified.

Optional list arguments If a list argument to a function is optional, this should be indicated by
appending a default value of null, as in

```
function scalar myfunc (scalar y, list X[null])
```
In that case, if the caller gives null as the list argument (or simply omits the last argument) the
named list X inside the function will be empty. This possibility can be detected using the nelem()
function, which returns 0 for an empty list.


Chapter 14. User-defined functions 120

String arguments

String arguments can be used, for example, to provide flexibility in the naming of variables created
within a function. In the following example the function mavg returns a list containing two moving
averages constructed from an input series, with the names of the newly created variables governed
by the string argument.

```
function list mavg (series y, string vname)
list retlist = deflist()
string newname = sprintf("%s_2", vname)
retlist += genseries(newname, (y+y(-1)) / 2)
newname = sprintf("%s_4", vname)
retlist += genseries(newname, (y+y(-1)+y(-2)+y(-3)) / 4)
return retlist
end function
```
```
open data9-9
list malist = mavg(nocars, "nocars")
print malist --byobs
```
The last line of the script will print two variables named nocars_2 and nocars_4. For details on
the handling of named strings, see chapter 15.

If a string argument is considered optional, it may be given a null default value, as in

```
function scalar foo (series y, string vname[null])
```
Retrieving the names of arguments

The variables given as arguments to a function are known inside the function by the names of the
corresponding parameters. For example, within the function whose signature is

```
function void somefun (series y)
```
we have the series known as y. It may be useful, however, to be able to determine the names of
the variables provided as arguments. This can be done using the function argname, which takes
the name of a function parameter as its single argument and returns a string. Here is a simple
illustration:

```
function void namefun (series y)
printf "the series given as ’y’ was named %s\n", argname(y)
end function
```
```
open data9-7
namefun(QNC)
```
This produces the output

```
the series given as ’y’ was named QNC
```
Please note that this will not always work: the arguments given to functions may be anonymous
variables, created on the fly, as in somefun(log(QNC)) or somefun(CPI/100). In that case the
argname function returns an empty string. Function writers who wish to make use of this facility
should check the return from argname using the strlen() function: if this returns 0, no name was
found.


Chapter 14. User-defined functions 121

Return values

Functions can return nothing (just printing a result, perhaps), or they can return a single variable.
The return value, if any, is specified via a statement within the function body beginning with the
keyword return, followed by either the name of a variable (which must be of the type announced
on the first line of the function definition) or an expression which produces a value of the correct
type.

Having a function return a list, bundle or array (see Chapter 11) is a way of permitting the “return”
of more than one variable. For example, you can define several series inside a function and package
them as a list; in this case they are not destroyed when the function exits. Here is a simple example,
which also illustrates the possibility of setting the descriptive labels for variables generated in a
function.

```
function list make_cubes (list xlist)
list cubes = deflist()
loop foreach i xlist
series $i3 = (xlist.$i)^3
setinfo $i3 -d "cube of $i"
list cubes += $i3
endloop
return cubes
end function
```
```
open data4-1
list xlist = price sqft
list cubelist = make_cubes(xlist)
print xlist cubelist --byobs
labels
```
For details about the case of returning a bundle, see Section 11.7, in particular the sub-sections
titled “Series and lists as bundle members” and “What are bundles good for?”.

A return statement causes the function to return (exit) at the point where it appears within the
body of the function. A function may also exit when (a) the end of the function code is reached (in
the case of a function with no return value), (b) a gretl error occurs, or (c) a funcerr statement is
reached.

The funcerr keyword — which may be followed by a string enclosed in double quotes, or the name
of a string variable, or nothing — causes a function to exit with an error flagged. If a string is
provided (either literally or via a variable), this is printed on exit, otherwise a generic error message
is printed. This mechanism enables the author of a function to pre-empt an ordinary execution
error and/or offer a more specific and helpful error message. For example,

```
if nelem(xlist) == 0
funcerr "xlist must not be empty"
endif
```
A function may contain more than one return statement, as in

```
function scalar multi (bool s)
if s
return 1000
else
return 10
endif
end function
```
However, it is recommended programming practice to have a single return point from a function
unless this is very inconvenient. The simple example above would be better written as


Chapter 14. User-defined functions 122

```
function scalar multi (bool s)
return s? 1000 : 10
end function
```
Overloading

You may have noticed that several built-in functions in gretl are “overloaded” — that is, a given
argument slot may accept more than one type of argument, and the return value may depend on
the type of the argument in question. For instance, the argument _x_ for the pdf() function may be
a scalar, series or matrix and the return type will match that choice on the caller’s part.

Since gretl-2021b this possibility also exists for user-defined functions. The meta-type numeric
can be used in place of a specific type to accept a scalar, series or matrix argument, and similarly
the return-type of a function can be marked as numeric.

As a function writer you can choose to be more restrictive than the default (which allows scalar,
series or matrix for any numeric argument). For instance, if you write a function in which two
arguments, _x_ and _y_ , are specified as numeric you might decide to disallow the case where _x_ is
a matrix and _y_ a series, or vice versa, as too complicated. You can use the typeof() function
to determine what types of arguments were supplied, and the funcerr command or errorif()
function to reject an unsupported combination.

If your function is going to return a certain specific type (say, matrix) regardless of the type of the
input, then the return value should be labeled accordingly: use numeric for the return only if it’s
truly unknown in advance.

Listing 14.2 offers an (admittedly artificial) example: its numeric inputs can be scalars, series or
column vectors but they must be of a single type.

Naturally, if your overloaded function is intended for public use you should state clearly in its
documentation what is supported and what is not.

Error checking

When gretl first reads and “compiles” a function definition there is minimal error-checking: the
only checks are that the function name is acceptable, and, so far as the body is concerned, that you
are not trying to define a function inside a function (see Section 14.1). Otherwise, if the function
body contains invalid commands this will become apparent only when the function is called and
its commands are executed.

Debugging

The usual mechanism whereby gretl echoes commands and reports on the creation of new variables
is by default suppressed when a function is being executed. If you want more verbose output from
a particular function you can use either or both of the following commands within the function:

```
set echo on
set messages on
```
Alternatively, you can achieve this effect for all functions via the command set debug 1. Usually
when you set the value of a state variable using the set command, the effect applies only to the
current level of function execution. For instance, if you do set messages on within function f1,
which in turn calls function f2, then messages will be printed for f1 but not f2. The debug variable,
however, acts globally; all functions become verbose regardless of their level.

Further, you can do set debug 2: in addition to command echo and the printing of messages, this
is equivalent to setting max_verbose (which produces verbose output from the BFGS maximizer) at
all levels of function execution.


Chapter 14. User-defined functions 123

```
Listing 14.2: Example of overloaded function [Download▼]
```
function numeric x_plus_b_y (numeric x, scalar b, numeric y)
errorif(typeof(x) != typeof(y), "x and y must be of the same type")
if typeof(x) <= 2 # scalar or series
return x + b*y
elif rows(x) == rows(y) && cols(x) == 1 && cols(y) == 1
return x + b*y
else
funcerr "x and y should be column vectors"
endif
end function

set seed 12345

# call 1: x and y are scalars
eval x_plus_b_y(10, 3, 2)

# call 2: x and y are vectors
matrix x = mnormal(10, 1)
matrix y = mnormal(10, 1)
eval x_plus_b_y(x, 2, y)

open data4-1
# call 3: x and y are series
series bb = x_plus_b_y(bedrms, 0.5, baths)
print bb --byobs


Chapter 14. User-defined functions 124

### 14.5 Function packages

At various points above we have alluded to function packages, and the use of these via the gretl
GUI. This topic is covered in depth by the _Gretl Function Package Guide_. If you’re running gretl you
can find this under the Help menu. Alternatively you may download it from

https://sourceforge.net/projects/gretl/files/manual/


## Chapter 15

Named lists and strings

### 15.1 Named lists

Many gretl commands take one or more lists of series as arguments. To make this easier to handle
in the context of command scripts, and in particular within user-defined functions, gretl offers the
possibility of _named lists_.

Creating and modifying named lists

A named list is created using the keyword list, followed by the name of the list, an equals sign,
and an expression that forms a list. The most basic sort of expression that works in this context is
a space-separated list of variables, given either by name or by ID number. For example,

```
list xlist = 1 2 3 4
list reglist = income price
```
Note that the variables in question must be of the series type.

Two abbreviations are available in defining lists:

- You can use the wildcard character, “*”, to create a list of variables by name. For example,
    dum* can be used to indicate all variables whose names begin with dum.
- You can use two dots to indicate a range of variables. For example income..price indicates
    the set of variables whose ID numbers are greater than or equal to that of income and less
    than or equal to that of price.

In addition there are two special forms:

- If you use the keyword null on the right-hand side, you get an empty list.
- If you use the keyword dataset on the right, you get a list containing all the series in the
    current dataset (except the pre-defined const).

The name of the list must start with a letter, and must be composed entirely of letters, numbers
or the underscore character. The maximum length of the name is 31 characters; list names cannot
contain spaces.

Once a named list has been created, it will be “remembered” for the duration of the gretl session
(unless you delete it), and can be used in the context of any gretl command where a list of variables
is expected. One simple example is the specification of a list of regressors:

```
list xlist = x1 x2 x3 x4
ols y 0 xlist
```
To get rid of a list, you use the following syntax:

```
list xlist delete
```
#### 125


Chapter 15. Named lists and strings 126

Be careful: delete xlist will delete the series contained in the list, so it implies data loss (which
may not be what you want). On the other hand, list xlist delete will simply “undefine” the
xlist identifier; the series themselves will not be affected.

Similarly, to print the names of the members of a list you have to invert the usual print command,
as in

```
list xlist print
```
If you just say print xlist the list will be expanded and the values of all the member series will
be printed.

Lists can be modified in various ways. To _redefine_ an existing list altogether, use the same syntax
as for creating a list. For example

```
list xlist = 1 2 3
xlist = 4 5 6
```
After the second assignment, xlist contains just variables 4, 5 and 6.

To _append_ or _prepend_ variables to an existing list, we can make use of the fact that a named list
stands in for a “longhand” list. For example, we can do

```
list xlist = xlist 5 6 7
xlist = 9 10 xlist 11 12
```
Another option for appending a term (or a list) to an existing list is to use +=, as in

```
xlist += cpi
```
To drop a variable from a list, use -=:

```
xlist -= cpi
```
In most contexts where lists are used in gretl, it is expected that they do not contain any duplicated
elements. If you form a new list by simple concatenation, as in list L3 = L1 L2 (where L1 and
L2 are existing lists), it’s possible that the result may contain duplicates. To guard against this you
can form a new list as the union of two existing ones:

```
list L3 = L1 || L2
```
The result is a list that contains all the members of L1, plus any members of L2 that are not already
in L1.

In the same vein, you can construct a new list as the intersection of two existing ones:

```
list L3 = L1 && L2
```
Here L3 contains all the elements that are present in both L1 and L2.

You can also subtract one list from another:

```
list L3 = L1 - L2
```
The result contains all the elements of L1 that are not present in L2.

Indexing into a defined list is also possible, as if it were a vector:

```
list L2 = L1[1:4]
```
This leaves L2 with the first four members of L1. Notice that the ordering of list members is
path-dependent.


Chapter 15. Named lists and strings 127

Lists and matrices

There are two ways one can think of lists and matrices being interchangeable: either you think of
a list as a collection of references to series, or you may consider the rectangle of data given by the
series that the list contains.

In the former case, a list may be translated into (or created from) a one-dimensional matrix, that is
a vector. Therefore, the matrix in question must be interpretable as a vector containing ID numbers
of data series. It may be either a row or a column vector, and each of its elements must have an
integer part that is no greater than the number of variables in the data set. For example:

```
matrix m = {1,2,3,4}
list L = m
```
The above is OK provided the data set contains at least 4 variables. Conversely, the command

```
matrix m = L
```
will create a row vector with the ID numbers of the series referenced by L.

The latter case occurs when the matrix is assumed to contain valid data. To create a matrix from
the list, simply assing to a matrix the list name surrounded by curly brackets, as in

```
matrix m = { L }
```
Note the difference with the above: without the curly brackets, matrix m would have been just a
vector. Also note that any row corresponding to one or more missing entries will be dropped,
unless the skip_missing set variable is set to on.

For the reverse operation, gretl provides the mat2list function, which takes a matrix (say, X) as
argument and creates new series as well as a list containing them. The row dimension of X must
equal either the length of the current dataset or the number of observations in the current sample
range.

The naming of the series in the returned list proceeds as follows. First, if the optional prefix
argument is supplied, the series created from column _i_ of X is named by appending i to the given
string. Otherwise, if X has column names set these names are used. Finally, if neither of the above
conditions is satisfied, the names are column1, column2 and so on.

For example,

```
matrix X = mnormal($nobs, 8)
list L = mat2list(X, "xnorm")
```
will add to the dataset eight full-length series named xnorm1, xnorm2 and so on.

Querying a list

You can determine the number of variables or elements in a list using the function nelem().

```
list xlist = 1 2 3
nl = nelem(xlist)
```
The (scalar) variable nl will be assigned a value of 3 since xlist contains 3 members.

You can determine whether a given series is a member of a specified list using the function
inlist(), as in

```
scalar k = inlist(L, y)
```
where L is a list and y a series. The series may be specified by name or ID number. The return value
is the (1-based) position of the series in the list, or zero if the series is not present in the list.


Chapter 15. Named lists and strings 128

Generating lists of transformed variables

Given a named list of series, you are able to generate lists of transformations of these series using
the functions log, lags, diff, ldiff, sdiff or dummify. For example

```
list xlist = x1 x2 x3
list lxlist = log(xlist)
list difflist = diff(xlist)
```
When generating a list of _lags_ in this way, you specify the maximum lag order inside the parenthe-
ses, before the list name and separated by a comma. For example

```
list xlist = x1 x2 x3
list laglist = lags(2, xlist)
```
or

```
scalar order = 4
list laglist = lags(order, xlist)
```
These commands will populate laglist with the specified number of lags of the variables in xlist.
You can give the name of a single series in place of a list as the second argument to lags: this is
equivalent to giving a list with just one member.

The dummify function creates a set of dummy variables coding for all but one of the distinct values
taken on by the original variable, which should be discrete. (The smallest value is taken as the
omitted catgory.) Like lags, this function returns a list even if the input is a single series.

Another useful operation you can perform with lists is creating _interaction_ variables. Suppose you
have a discrete variable _xi_ , taking values from 1 to _n_ and a variable _zi_ , which could be continuous
or discrete. In many cases, you want to “split” _zi_ into a set of _n_ variables via the rule

```
z
(j)
i =
```
#### (

```
zi when xi = j
0 otherwise;
```
in practice, you create dummies for the _xi_ variable first and then you multiply them all by _zi_ ; these
are commonly called the _interactions_ between _xi_ and _zi_. In gretl you can do

```
list H = D ^ Z
```
where D is a list of discrete series (or a single discrete series), Z is a list (or a single series)^1 ; all the
interactions will be created and listed together under the name H.

An example is provided in Listing 15.1.

Generating series from lists

There are various ways of retrieving or generating individual series from a named list. The most
basic method is indexing into the list. For example,

```
series x3 = Xlist[3]
```
will retrieve the third element of the list Xlist under the name x3 (or will generate an error if
Xlist has less then three members).

(^1) This construct does _not_ work if neither D nor Z are of the list type. However, a simple workaround is to turn D into a
one-element list in this case, by writing deflist(D) ^ Z.


Chapter 15. Named lists and strings 129

Listing 15.1: Usage of interaction lists [Download▼]
Input:

open mroz87.gdt --quiet

# the coding below makes it so that
# KIDS = 0 -> no kids
# KIDS = 1 -> young kids only
# KIDS = 2 -> young or older kids

series KIDS = (KL6 > 0) + ((KL6 > 0) || (K618 > 0))

list D = CIT KIDS # interaction discrete variables
list X = WE WA # variables to "split"
list INTER = D ^ X

smpl 1 6

print D X INTER -o

Output (selected portions):

```
CIT KIDS WE WA WE_CIT_0
```
1 0 2 12 32 12
2 1 1 12 30 0
3 0 2 12 35 12
4 0 1 12 34 12
5 1 2 14 31 0
6 1 0 12 54 0

```
WE_CIT_1 WA_CIT_0 WA_CIT_1 WE_KIDS_0 WE_KIDS_1
```
1 0 32 0 0 0
2 12 0 30 0 12
3 0 35 0 0 0
4 0 34 0 0 12
5 14 0 31 0 0
6 12 0 54 12 0

```
WE_KIDS_2 WA_KIDS_0 WA_KIDS_1 WA_KIDS_2
```
1 12 0 0 32
2 0 0 30 0
3 12 0 0 35
4 0 0 34 0
5 14 0 0 31
6 0 54 0 0

In addition gretl offers several functions that apply to a list and return a series. In most cases,
these functions also apply to single series and behave as natural extensions when applied to lists,
but this is not always the case.

For recognizing and handling missing values, gretl offers several functions (see the _Gretl Command
Reference_ for details). In this context, it is worth remarking that the ok() function can be used


Chapter 15. Named lists and strings 130

```
YpcFR YpcGE YpcIT NFR NGE NIT
```
```
1997 114.9 124.6 119.3 59830.635 82034.771 56890.372
1998 115.3 122.7 120.0 60046.709 82047.195 56906.744
1999 115.0 122.4 117.8 60348.255 82100.243 56916.317
2000 115.6 118.8 117.2 60750.876 82211.508 56942.108
2001 116.0 116.9 118.1 61181.560 82349.925 56977.217
2002 116.3 115.5 112.2 61615.562 82488.495 57157.406
2003 112.1 116.9 111.0 62041.798 82534.176 57604.658
2004 110.3 116.6 106.9 62444.707 82516.260 58175.310
2005 112.4 115.1 105.1 62818.185 82469.422 58607.043
2006 111.9 114.2 103.3 63195.457 82376.451 58941.499
```
```
Table 15.1: GDP per capita and population in 3 European countries (Source: Eurostat)
```
with a list argument. For example,

```
list xlist = x1 x2 x3
series xok = ok(xlist)
```
After these commands, the series xok will have value 1 for observations where none of x1, x2, or
x3 has a missing value, and value 0 for any observations where this condition is not met.

The functions max, min, mean, sd, sum and var behave “horizontally” rather than “vertically” when
their argument is a list. For instance, the following commands

```
list Xlist = x1 x2 x3
series m = mean(Xlist)
```
produce a series m whose _i_ -th element is the average of _x_ 1 _,i,x_ 2 _,i_ and _x_ 3 _,i_ ; missing values, if any, are
implicitly discarded.

In addition, gretl provides three functions for weighted operations: wmean, wsd and wvar. Consider
as an illustration Table 15.1: the first three columns are GDP per capita for France, Germany and
Italy; columns 4 to 6 contain the population for each country. If we want to compute an aggregate
indicator of per capita GDP, all we have to do is

```
list Ypc = YpcFR YpcGE YpcIT
list N = NFR NGE NIT
y = wmean(Ypc, N)
```
so for example

```
y 1996 =
```
#### 114. 9 × 59830. 635 + 124. 6 × 82034. 771 + 119. 3 × 56890. 372

#### 59830. 635 + 82034. 771 + 56890. 372

#### = 120. 163

See the _Gretl Command Reference_ for more details.

### 15.2 Named strings

For some purposes it may be useful to save a string (that is, a sequence of characters) as a named
variable that can be reused.

Some examples of the definition of a string variable are shown below.


Chapter 15. Named lists and strings 131

```
string s1 = "some stuff I want to save"
string s2 = getenv("HOME")
string s3 = s1 + 11
```
The first field after the type-name string is the name under which the string should be saved, then
comes an equals sign, then comes a specification of the string to be saved. This may take any of
the following forms:

- a string literal (enclosed in double quotes); or
- the name of an existing string variable; or
- a function that returns a string (see below); or
- any of the above followed by + and an integer offset.

The role of the integer offset is to use a substring of the preceding element, starting at the given
character offset. An empty string is returned if the offset is greater than the length of the string in
question.

To add to the end of an existing string you can use the operator ~=, as in

```
string s1 = "some stuff I want to "
string s1 ~= "save"
```
or you can use the ~ operator to join two or more strings, as in

```
string s1 = "sweet"
string s2 = "Home, " ~ s1 ~ " home."
```
Note that when you define a string variable using a string literal, only a single “escape” sequence is
recognized: if a backslash is immediately followed by a double-quote character this is interpreted
as an embedded quote. Otherwise all characters are treated literally. If you wish to use backslash-
escapes to denote newlines, tabs and so on, use the sprintf function instead (see the printf
command for an account of the escape-characters). This function can also be used to produce a
string variable whose definition involves the values of other variables, as in

```
scalar x = 8
foo = sprintf("var%d", x) # produces "var8"
```
String variables and string substitution

String variables can be used in two ways in scripting: the name of the variable can be typed “as
is”, or it may be preceded by the “at” sign, @. In the first variant the named string is treated as a
variable in its own right, while the second calls for “string substitution”. The context determines
which of these variants is appropriate.

In the following contexts the names of string variables should be given in plain form (without the
“at” sign):

- When such a variable appears among the arguments to the printf command or sprintf
    function.
- When such a variable is given as the argument to a function.
- On the right-hand side of a string assignment.

Here is an illustration of the use of a named string argument with printf:


Chapter 15. Named lists and strings 132

```
? string vstr = "variance"
Generated string vstr
? printf "vstr: %12s\n", vstr
vstr: variance
```
String substitution can be used in contexts where a string variable is not acceptable as such. If
gretl encounters the symbol @ followed directly by the name of a string variable, this notation is
treated as a “macro”: the value of the variable is sustituted literally into the command line before
the regular parsing of the command is carried out.

One common use of string substitution is when you want to construct and use the name of a series
programatically. For example, suppose you want to create 10 random normal series named norm1
to norm10. This can be accomplished as follows.

```
string sname
loop i=1..10
sname = sprintf("norm%d", i)
series @sname = normal()
endloop
```
Note that plain sname could not be used in the second line within the loop: the effect would be
to attempt to overwrite the string variable named sname with a series of the same name. What
we want is for the current _value_ of sname to be dumped directly into the command that defines a
series, and the “@” notation achieves that.

Another typical use of string substitution is when you want the options used with a particular
command to vary depending on some condition. For example,

```
function void use_optstr (series y, list xlist, int verbose)
string optstr = verbose? "" : "--simple-print"
ols y xlist @optstr
end function
```
```
open data4-1
list X = const sqft
use_optstr(price, X, 1)
use_optstr(price, X, 0)
```
When printing the value of a string variable using the print command, the plain variable name
should generally be used, as in

```
string s = "Just testing"
print s
```
The following variant is equivalent, though clumsy.

```
string s = "Just testing"
print "@s"
```
But note that this next variant does something quite different.

```
string s = "Just testing"
print @s
```
After string substitution, the print command reads

```
print Just testing
```
which attempts to print the values of two variables, Just and testing.


Chapter 15. Named lists and strings 133

Built-in strings

Apart from any strings that the user may define, some string variables are defined by gretl itself.
These may be useful for people writing functions that include shell commands. The built-in strings
are as shown in Table 15.2.

```
gretldir the gretl installation directory
workdir user’s current gretl working directory
dotdir the directory gretl uses for temporary files
gnuplot path to, or name of, the gnuplot executable
tramo path to, or name of, the tramo executable
x12a path to, or name of, the x-12-arima executable
tramodir tramo data directory
x12adir x-12-arima data directory
```
```
Table 15.2: Built-in string variables
```
To access these as ordinary string variables, prepend a dollar sign (as in $dotdir); to use them in
string-substitution mode, prepend the at-sign (@dotdir).

Reading strings from the environment

It is possible to read into gretl’s named strings, values that are defined in the external environment.
To do this you use the function getenv, which takes the name of an environment variable as its
argument. For example:

```
? string user = getenv("USER")
Generated string user
? string home = getenv("HOME")
Generated string home
? printf "%s’s home directory is %s\n", user, home
cottrell’s home directory is /home/cottrell
```
To check whether you got a non-empty value from a given call to getenv, you can use the function
strlen, which retrieves the length of the string, as in

```
? string temp = getenv("TEMP")
Generated string temp
? scalar x = strlen(temp)
Generated scalar x = 0
```
Capturing strings via the shell

If shell commands are enabled in gretl, you can capture the output from such commands using the
syntax

string _stringname_ = $( _shellcommand_ )

That is, you enclose a shell command in parentheses, preceded by a dollar sign.

Reading from a file into a string

You can read the content of a file into a string variable using the syntax

string _stringname_ = readfile( _filename_ )

The _filename_ field may be given as a string variable. For example


Chapter 15. Named lists and strings 134

```
? fname = sprintf("%s/QNC.rts", $x12adir)
Generated string fname
? string foo = readfile(fname)
Generated string foo
```
More string functions

Gretl offers several functions for creating or manipulating strings. You can find these listed and
explained in the _Function Reference_ under the category Strings.


## Chapter 16

String-valued series

### 16.1 Introduction

By a string-valued series we mean a series whose primary values are strings (though internally such
series comprise an integer coding plus a “dictionary” mapping from the integer values to strings).
This chapter explains how to create such series and describes the operations that are supported
for them.

### 16.2 Creating a string-valued series

This can be done in three ways:

- by reading such a series from a suitable source file;
- by taking a suitable numerical series within gretl and adding string values using the stringify()
    function; and
- by direct assignment to a series from an array of strings.

In each case string values will be preserved when such a series is saved in a gretl-native data file.

Reading string-valued series

The primary “suitable source” for string-valued series is a delimited text data file (but see sec-
tion 16.5 below). Here’s a little example. The following is the content of a file named gc.csv:

```
city,year
"Bilbao",2009
"Toru ́n",2011
"Oklahoma City",2013
"Berlin",2015
"Athens",2017
"Naples",2019
```
A script to read this file and its output are shown in Listing 16.1, from which we can see a few
things.

- By default the print command shows us the string values of the series city, and it han-
    dles non-ASCII characters provided they’re in UTF-8 (but it doesn’t handle longer strings very
    elegantly).
- The --numeric option to print exposes the integer codes for a string-valued series.
- The syntax seriesname[obs] yields a string when a series is string-valued.

If you want to access the numeric code for a particular string-valued observation you can get it by
“casting” the series in question to a vector (by wrapping the identifier in curly brackets). So, for
example,

#### 135


Chapter 16. String-valued series 136

Listing 16.1: Working with a string-valued series
Input:

open gc.csv --quiet
print --byobs
print city --byobs --numeric
printf "The third gretl conference took place in %s.\n", city[3]

Output:

? print --byobs

```
city year
```
1 Bilbao 2009
2 Toru ́n 2011
3 Oklahoma C.. 2013
4 Berlin 2015
5 Athens 2017
6 Naples 2019

? print city --byobs --numeric

```
city
```
1 1
2 2
3 3
4 4
5 5
6 6

The third gretl conference took place in Oklahoma City.


Chapter 16. String-valued series 137

```
printf "The code for ’%s’ is %d.\n", city[3], {city}[3]
```
gives

```
The code for ’Oklahoma City’ is 3.
```
The numeric codes for string-valued series are always assigned thus: reading the data file row by
row, the first string value is assigned 1, the next _distinct_ string value is assigned 2, and so on.

Assigning string values to a numeric series

This is done via the stringify() function, which takes two arguments, the name of a series and
an array of strings. For this to work two conditions must be met:

1. The series must have only integer values and the smallest value must be 1 or greater.
2. The array of strings must have at least _n_ distinct members, where _n_ is the largest value found
    in the series.

The logic of these conditions is that we’re looking to create a mapping as described above, from
a 1-based sequence of integers to a set of strings. However, we’re allowing for the possibility that
the series in question is an incomplete sample from an associated population. Suppose we have a
series that goes 2, 3, 5, 9, 10. This is taken to be a sample from a population that has at least 10
discrete values, 1, 2,... , 10, and so requires at least 10 value-strings.

Here’s (a simplified version of) an example that one of the authors has had cause to use: deriving
US-style “letter grades” from a series containing percentage scores for students. Call the percentage
series _x_ , and say we want to create a series with values A for _x_ ≥ 90, B for 80 ≤ _x <_ 90, and so on
down to F for _x <_ 60. Then we can do:

```
series grade = 1 # F, the least value
grade += x >= 60 # D
grade += x >= 70 # C
grade += x >= 80 # B
grade += x >= 90 # A
stringify(grade, strsplit("F D C B A"))
```
The way the grade series is constructed is not the most compact, but it’s nice and explicit, and
easy to amend if one wants to adjust the threshold values. Note the use of strsplit() to create
an on-the-fly array of strings from a string literal; this is convenient when the array contains a
moderate number of elements with no embedded spaces. An alternative way to get the same result
is to define the array of strings via the defarray() function, as in

```
stringify(grade, defarray("F","D","C","B","A"))
```
The inverse operation of stringify() is performed by the strvals() function: this retrieves the
array of distinct string values from a series (or returns an empty array if the series is not string-
valued).

Assigning from an array of strings

Given an array of strings whose length matches the full length of the current dataset you can assign
directly to a series result, provided these conditions are satisfied: the dataset is not sub-sampled,
and if the assignment is to a pre-existing series it is not already string-valued.

Here’s a trivial example:


Chapter 16. String-valued series 138

```
nulldata 6
strings S = defarray("a", "b", "c", "b", "a", "d")
series sx = S
print sx --byobs
```
Here’s a second example where we create a string-valued series using the “observation markers”
from the current dataset, after grabbing them as an array via the markers command:

```
open data4-10
markers --to-array=S
series state = S
print state --byobs
```
And here’s a third example where we construct the array of strings by reading from a text file:

```
nulldata 8
series sv = strsplit(readfile("ABCD.txt"))
print sv --byobs
```
This will work fine if the content of ABCD.txt is something like

```
A B C D D C B A
```
(containing 8 space-separated values, with or without line breaks). If the strings in question contain
embedded spaces you would have to make use of the optional second argument to strsplit.

### 16.3 Permitted operations

One question that arises with string-valued series is, what exactly are you allowed to do with them?
The optimal policy may be debatable, but here we set out the current state of things.

Setting values per observation

You can set particular values in a string-valued series either by string or numeric code. For example,
suppose (in relation to the example in section 16.2) that for some reason student number 31 with
a percentage score of 88 nonetheless merits an A grade. We could do

```
grade[31] = "A"
```
or, if we’re confident about the mapping,

```
grade[31] = 5
```
Or to raise the student’s grade by one letter:

```
grade[31] += 1
```
What you’re _not_ allowed to do here is make a numerical adjustment that would put the value out
of bounds in relation to the set of string values. For example, if we tried grade[31] = 6 we’d get
an error.

On the other hand, you _can_ implicitly extend the set of string values. This wouldn’t make sense for
the letter grades example but it might for, say, city names. Returning to the example in section 16.2
suppose we try


Chapter 16. String-valued series 139

```
dataset addobs 1
year[7] = 2023
city[7] = "Gda ́nsk"
```
This will work: we’re implicitly adding another member to the string table for city; the associated
numeric code will be the next available integer.^1

Logical product of two string-valued series

The operator ^ can be used to produce what we might call the logical product of two string-valued
series, as in

```
series sv3 = sv1 ^ sv2
```
The result is another string-valued series with value _si.sj_ at observations where sv1 has value _si_
and sv2 has value _sj_. For example, if at a given observation sv1 has value “A” and sv2 has value
“X”, then sv3 will have value “A.X”. The set of strings attached to the resulting series will include
all such string combinations even if they are not all represented in the given sample.

Assignment to a string-valued series

In an assignment statement where the left-hand side (LHS) term is an existing string-valued series
two general conditions must be met. First, the right-hand side (RHS) term must be a series (ei-
ther numeric or string-valued) and second, the assignment operator must be plain “=”; inflected
operators such as += and *= are not supported.

When the RHS series is numeric, all its values must be either integers between 1 and the number of
strings attached to the LHS series, or NA. This is required to preserve the integrity of the LHS. When
the RHS series is itself string-valued there are two cases to consider: there’s no sample restriction
in place, or there is such a restriction. In the unrestricted case the LHS series is in effect destroyed
and replaced by a clone of the RHS. Otherwise string values on the RHS are written into the LHS only
within the current sample range. If an RHS string is already present on the left its numerical code
is adjusted if necessary to match the LHS string table; if it is not present on the left it is appended
to the LHS string table.

Missing values

We support one exception to the general rule, never break the mapping between strings and nu-
meric codes for string-valued series: you can mark particular observations as missing. This is done
in the usual way, e.g.,

```
grade[31] = NA
```
Note, however, that on importing a string series from a delimited text file any non-blank strings (in-
cluding “NA”) will be interpreted as valid values; any missing values in such a file should therefore
be represented by blank cells.

Copying a string-valued series

If you make a copy of a string-valued series, as in

```
series foo = city
```
the string values are _not_ copied over: you get a purely numerical series holding the codes of the
original series. But if you want a full copy with the string values that can easily be arranged:

(^1) So please be careful: one may inadvertently add a new string value by mistyping a string that’s already present.


Chapter 16. String-valued series 140

```
series citycopy = city
stringify(citycopy, strvals(city))
```
String-valued series in other contexts

String-valued series can be used on the right-hand side of assignment statements at will, and in
that context their numerical values are taken. For example,

```
series y = sqrt(city)
```
will elicit no complaint and generate a numerical series 1, 1.41421,.... It’s up to the user to judge
whether this sort of thing makes any sense.

Similarly, it’s up to the user to decide if it makes sense to use a string-valued series “as is” in a
regression model, whether as regressand or regressor — again, the numerical values of the series
are taken. Often this will not make sense, but sometimes it may: the numerical values may by
design form an ordinal, or even a cardinal, scale (as in the “grade” example in section 16.2).

More likely, one would want to use dummify on a string-valued series before using it in statistical
modeling. In that context gretl’s series labels are suitably informative. For example, suppose we
have a series race with numerical values 1, 2 and 3 and associated strings “White”, “Black” and
“Other”. Then the hansl code

```
list D = dummify(race)
labels
```
will show these labels:

```
Drace_2: dummy for race = ’Black’
Drace_3: dummy for race = ’Other’
```
Given a series such as race you can use its string values in a sample restriction, as in

```
smpl race == "Black" --restrict
```
(although race == 2 would also be acceptable).

Accessing string values

We have mentioned above two ways of accessing string values from a given series: via the syntax

```
seriesname[obs]
```
to obtain a single such value; and via the strvals() function to obtain an array holding all its
distinct values. Here we note a third option: direct assignment from a string-valued series to an
array of strings, as in

```
strings S = sv
```
where sv is a suitable series. In this case you get an array holding _all_ the sv strings for observations
in the current sample range, not just the distinct values as with strvals.

### 16.4 String-valued series and functions

We first offer a few words on built-in functions that can be applied to string-valued series. The
five functions substr, strsub, regsub, tolower and toupper all perform transformations on


Chapter 16. String-valued series 141

strings — respectively, extraction of a substring, replacement of a substring, replacement via regular
expression, conversion to all lower-case and to all upper-case (see the _Gretl Command Reference_
for details). These functions work on single strings, arrays of strings and also string-valued series.
Note that when applied to a string-valued series these functions may reduce the number of distinct
strings attached to the series. For example, some string values that are originally distinct may
“collapse” into identity when converted to all lower-case. This possibility is handled by adjustment
of the integer codes as needed.

A special case is presented by the built-in strvsort function: this does not return a modified
string-valued series but rather modifies such a series in place. It puts the string values into alpha-
betical order and recalculates the integer codes so as to preserve the original association between
observation number and string. If, for example, the first observation had a string value of “X”,
coded as 1, it will still have value “X” but its code will reflect the position of “X” in the alphabet-
ized ordering. This can be particularly useful if a dataset comprises several series having the same
string values, but occurring in various orders. The effect of running strvsort on such series will
be to impose a common numerical encoding.

User-defined hansl functions can also deal with string-valued series. If you supply such a series as
an argument to a hansl function its string values will be accessible within the function. One can
test whether a given series arg is string-valued as follows:

```
if nelem(strvals(arg)) > 0
# yes
else
# no
endif
```
It’s also possible, since gretl version 2023c, to put something like the code that generated the grade
series in section 16.2 into a function, and return the stringified series, as in the following (where
we assume that x contains percentage scores):

```
function series letter_grade (series x)
series grade
# define grade based on x and stringify it, as shown above
return grade
end function
```
An alternative means of achieving the same effect — and the only means available prior to gretl
2023c — is to to define grade as a series at the level of the caller and pass it in “pointer” form to
letter_grade(), as in

```
function void letter_grade (series x, series *grade)
# define grade based on x and stringify it
end function
```
```
# caller
...
series grade
letter_grade(x, &grade)
```
As you’ll see from the account above, we don’t offer any very fancy facilities for string-valued
series. We’ll read them from suitable sources and we’ll create them natively via stringify — and
we’ll try to ensure that they retain their integrity — but we don’t, for example, take the specification
of a string-valued series as a regressor as an implicit request to include the dummification of its
distinct values.


Chapter 16. String-valued series 142

### 16.5 Other import formats

In section 16.2 we illustrated the reading of string-valued series with reference to a delimited text
data file. Gretl can also handle several other sources of string-valued data, including the spread-
sheet formats xls, xlsx, gnumeric and ods and (to a degree) the formats of Stata, SAS and SPSS.

Stata files

Stata supports two relevant sorts of variables: (1) those that are of “string type” and (2) variables
of one or other numeric type that have “value labels” defined. Neither of these is exactly equivalent
to what we call a “string-valued series” in gretl.

Stata variables of string type have no numeric representation; their values are literally strings, and
that’s all. Stata’s numeric variables with value labels do not have to be integer-valued and their
least value does not have to be 1; however, you can’t define a label for a value that is not an integer.
Thus in Stata you can have a series that comprises both integer and non-integer values, but only
the integer values can be labeled.^2

This means that on import to gretl we can readily handle variables of string type from Stata’s dta
files. We give them a 1-based numeric encoding; this is arbitrary but does not conflict with any
information in the dta file. On the other hand, in general we’re not able to handle Stata’s numeric
variables with value labels; currently we report the value labels to the user but do not attempt to
store them in the gretl dataset. We could check such variables and import them as string-valued
series if they satisfy the criteria stated in section 16.2 but we don’t at present.

SAS and SPSS files

Gretl is able to read and preserve string values associated with variables from SAS “export” (xpt)
files, and also from SPSS sav files. Such variables seem to be on the same pattern as Stata variables
of string type.

(^2) Verified in Stata 12.


## Chapter 17

Matrix manipulation

Together with the other two basic types of data (series and scalars), gretl offers a quite compre-
hensive array of matrix methods. This chapter illustrates the peculiarities of matrix syntax and
discusses briefly some of the more advanced matrix functions. For a full listing of matrix functions
and a comprehensive account of their syntax, please refer to the _Gretl Command Reference_.

In this chapter we’re concerned with real matrices; most of the points made here also apply to
complex matrices but see the following chapter for additional specifics on the complex case.

### 17.1 Creating matrices

Matrices can be created using any of these methods:

1. By direct specification of the scalar values that compose the matrix — either in numerical form,
    or by reference to pre-existing scalar variables, or using computed values.
2. By providing a list of data series.
3. By providing a _named list_ of series.
4. Via a suitable expression that references existing matrices and/or scalars, or via some special
    functions.

To specify a matrix _directly in terms of scalars_ , the syntax is, for example:

```
matrix A = {1, 2, 3 ; 4, 5, 6}
```
The matrix is defined by rows; the elements on each row are separated by commas and the rows
are separated by semi-colons. The whole expression must be wrapped in braces. Spaces within the
braces are not significant. The above expression defines a 2× 3 matrix. Each element should be a
numerical value, the name of a scalar variable, or an expression that evaluates to a scalar. Directly
after the closing brace you can append a single quote (’) to obtain the transpose.

To specify a matrix _in terms of data series_ the syntax is, for example,

```
matrix A = {x1, x2, x3}
```
where the names of the series are separated by commas. Besides names of existing series, you can
use expressions that yield a series result. For example, given a series x you could do

```
matrix A = {x, x^2}
```
Each series occupies a column (and there can only be one series per column). The semicolon
cannot be used as a row separator in this case: if you want the series arranged in rows, append the
transpose symbol. The range of data values included in the matrix depends on the current setting
of the sample range.

Instead of giving an explicit list of series, you may instead provide the _name of a saved list_ (see
Chapter 15), as in

#### 143


Chapter 17. Matrix manipulation 144

```
list xlist = x1 x2 x3
matrix A = {xlist}
```
When you provide a named list, the data series are by default placed in columns, as is natural in an
econometric context: if you want them in rows, append the transpose symbol.

As a special case of constructing a matrix from a list of series, you can say

```
matrix A = {dataset}
```
This builds a matrix using all the series in the current dataset, apart from the constant (series 0).
When this dummy list is used, it must be the sole element in the matrix definition {...}. You
can, however, create a matrix that includes the constant along with all other series using horizontal
concatenation (see below), as in

```
matrix A = {const}~{dataset}
```
By default, when you build a matrix from series that include missing values any observations (rows)
that contain NAs are skipped. This behavior can be modified via the command set skip_missing
off. In that case missing values are represented in the matrix as NaN (“Not a Number”). Note
that as per the IEEE standard, arithmetic operations involving one or more NaNs always produce a
NaN result. Alternatively, you can take greater control over the observations (data rows) that are
included in the matrix using the “set” variable matrix_mask, as in

```
set matrix_mask msk
```
where msk is the name of a series. Subsequent commands that form matrices from series or lists will
include only observations for which msk has non-zero (and non-missing) values. You can remove
this mask via the command set matrix_mask null.

☞ Names of matrices must satisfy the same requirements as names of gretl variables in general: the name
can be no longer than 31 characters, must start with a letter, and must be composed of nothing but letters,
numbers and the underscore character.

### 17.2 Empty matrices

The syntax

```
matrix A = {}
```
creates an empty matrix — a matrix with zero rows and zero columns.

The main purpose of this construct is to allow the user to define a starting point for subsequent
concatenation operations. For instance, if X is an already defined matrix of any size, the commands

```
matrix A = {}
matrix B = A ~ X
```
produce a matrix B that is identical to X.

From an algebraic point of view, one can make sense of the idea of an empty matrix in terms of
vector spaces: if a matrix is an ordered set of vectors, then A={} is the empty set. As a consequence,
operations involving addition and multiplications don’t have any clear meaning (arguably, they have
none at all), but operations involving the cardinality of this set (that is, the dimension of the space
spanned by A) are meaningful.

Legal function calls with an empty matrix argument are listed in Table 17.1; other matrix functions
generate an error if given an empty argument. In line with the above interpretation, the functions


Chapter 17. Matrix manipulation 145

```
Function Return value Function Return value
A’, transp(A) A rows(A) 0
cols(A) 0 rank(A) 0
det(A) NA ldet(A) NA
tr(A) NA onenorm(A) NA
infnorm(A) NA rcond(A) NA
diag(A) {} vec(A) {}
vech(A) {} unvech(A) {}
```
```
Table 17.1: Valid functions on an empty matrix, A
```
I, ones, zeros, mnormal and muniform return an empty matrix when or more of the arguments is
0, as well as the function nullspace when its argument is of full column rank.

While the 0× 0 matrix produced by {} is the most common sort of empty matrix, matrices with one
zero and one positive dimension are also supported. For example, the call

```
matrix A = zeros(3,0)
```
produces a 3× 0 matrix, as does

```
matrix A = zeros(3,1)
A = A[,-1] # delete column 1 (see below)
```
The handling of such matrices by gretl is very similar to that in Matlab.

### 17.3 Selecting submatrices

You can select submatrices of a given matrix using the syntax

```
A[ rows , cols ]
```
where _rows_ can take any of these forms:

1. empty selects all rows
2. a single integer selects the single specified row
3. two integers separated by a colon selects a range of rows
4. the name of a matrix selects the specified rows

With regard to option 2, the integer value can be given numerically, as the name of an existing
scalar variable, or as an expression that evaluates to a scalar. With option 4, the index matrix given
in the _rows_ field must be either _p_ × 1 or 1× _p_ , and should contain integer values in the range 1 to
_n_ , where _n_ is the number of rows in the matrix from which the selection is to be made.

The _cols_ specification works in the same way, _mutatis mutandis_. Here are some examples.

```
matrix B = A[1,]
matrix B = A[2:3,3:5]
matrix B = A[2,2]
matrix idx = {1, 2, 6}
matrix B = A[idx,]
```
The first example selects row 1 from matrix A; the second selects a 2×3 submatrix; the third selects
a scalar; and the fourth selects rows 1, 2, and 6 from matrix A.


Chapter 17. Matrix manipulation 146

If the matrix in question is _n_ × 1 or 1× _m_ , it is OK to give just one index specifier and omit the
comma. For example, A[2] selects the second element of A if A is a vector. Otherwise the comma
is mandatory.

In addition there are some predefined index specifications, represented by the keywords diag,
lower, upper, real, imag and end. With the exception of end, these keywords imply specific row
_and_ column selections, and therefore cannot be combined with any additional, comma-separated
term.

- The diag specification selects the principal diagonal of a matrix.
- lower and upper select, respectively, the elements of a matrix below and those above the
    principal diagonal.
- real and imag are specific to complex matrices and are described in chapter 18.
- end selects the last element in a given row or column. It can be employed in arithmetical
    expressions, so for example end-1 accesses the second-last element in a row or column.

Submatrix selections cane be used on either the right-hand side of a matrix-generating formula or
the left. Here is an example of use of a selection on the right, to extract a 2× 2 submatrix _B_ from a
3 × 3 matrix _A_ , then the lower triangle of _A_ :

```
matrix A = {1, 2, 3; 4, 5, 6; 7, 8, 9}
matrix B = A[1:2,2:3]
matrix C = A[lower]
```
And here are examples of selection on the left. The second line below writes a 2× 2 identity matrix
into the bottom right corner of the 3× 3 matrix _A_. The fourth line replaces the diagonal of _A_ with
1s.

```
matrix A = {1, 2, 3; 4, 5, 6; 7, 8, 9}
matrix A[2:3,2:3] = I(2)
matrix d = {1, 1, 1}
matrix A[diag] = d
```
When the lower and upper selections are used on the right, they yield a vector holding the elements
in their scope. The ordering of the elements is column-major in both cases, as illustrated below for
the 4× 4 case.

```
d 1 2 4
1 d 3 5
2 4 d 6
3 5 6 d
```
This means that lower and upper do not produce the same result for symmetric matrices bigger
than 3× 3, which may seem unfortunate, but it gives the user a degree of flexibility in respect of the
ordering of the elements. Suppose you have a non-symmetric matrix _M_ and you’d like to extract
the infradiagonal elements in _row_ -major order: (M’)[upper] will do the job.

When lower and upper are used on the left, the replacement must be either (a) a vector of length
equal to the number of elements in the selection or (b) a scalar value. In case (a) the elements of
the target matrix are filled in column-major order; in case (b) they are all set using the scalar.

One possible use of these tools is taking (say) a lower triangular matrix and rendering it symmetric
by copying the elements from beneath the diagonal to above. The way to get this right (assuming
you have a lower triangular matrix L) is

```
L[upper] = (L’)[upper] # note: not L[upper] = L[lower]
```

Chapter 17. Matrix manipulation 147

### 17.4 Deleting rows or columns

A variant of submatrix notation is available for convenience in dropping specified rows and/or
columns from a matrix, namely giving negative values for the indices. Here is a simple example,

```
matrix A = {1, 2, 3; 4, 5, 6; 7, 8, 9}
matrix B = A[-2,-3]
```
which creates B as a 2× 2 matrix which drops row 2 and column 3 from A. Negative indices can also
be given in the form of an index vector:

```
matrix rdrop = {-1,-3,-5}
matrix B = A[rdrop,]
```
In this case B is formed by dropping rows 1, 3 and 5 from A (which must have at least 5 rows), but
retaining the column dimension of A.

There are two limitations on the use of negative indices. First, the from:to range syntax described
in the previous section is not available, but you can use the seq function to achieve an equivalent
effect, as in

```
matrix A = muniform(1, 10)
matrix B = A[,-seq(3,7)]
```
where B drops columns 3 to 7 from A. Second, use of negative indices is valid only on the right-hand
side of a matrix calculation; there is no “negative index” equivalent of assignment to a submatrix,
as in

```
A[1:3,] = ones(3, cols(A))
```
### 17.5 Matrix operators

The following binary operators are available for matrices:

```
+ addition
```
- subtraction
* ordinary matrix multiplication
’ pre-multiplication by transpose
\ matrix “left division” (see below)
/ matrix “right division” (see below)
~ column-wise concatenation
| row-wise concatenation
** Kronecker product
== test for equality
!= test for inequality

In addition, the following operators (“dot” operators) apply on an element-by-element basis:

#### .+ .- .* ./ .^ .= .> .< .>= .<= .!=

Here are explanations of the less obvious cases.

For matrix addition and subtraction, in general the two matrices have to be of the same dimensions
but an exception to this rule is granted if one of the operands is a 1× 1 matrix or scalar. The scalar


Chapter 17. Matrix manipulation 148

is implicitly promoted to the status of a matrix of the correct dimensions, all of whose elements
are equal to the given scalar value. For example, if _A_ is an _m_ × _n_ matrix and _k_ a scalar, then the
commands

```
matrix C = A + k
matrix D = A - k
```
both produce _m_ × _n_ matrices, with elements _cij_ = _aij_ + _k_ and _dij_ = _aij_ − _k_ respectively.

By “pre-multiplication by transpose” we mean, for example, that

```
matrix C = X’Y
```
produces the product of _X_ -transpose and _Y_. In effect, the expression X’Y is shorthand for X’*Y,
which is also valid syntax. In the special case _X_ = _Y_ , however, the two are not exactly equivalent.
The former expression uses a specialized algorithm with two advantages: it is more efficient com-
putationally, and ensures that the result is free of machine precision artifacts that may render it
numerically non-symmetric. This, however, is unlikely to be an issue unless your _X_ matrix is rather
large (at least several hundreds rows/columns).

In matrix “left division”, the statement

```
matrix X = A \ B
```
is interpreted as a request to find the matrix _X_ that solves _AX_ = _B_ , so _A_ and _B_ must have the same
number of rows. If _A_ is a square matrix, this is in principle equivalent to _A_ −^1 _B_ , which fails if _A_
is singular; the numerical method employed here is the LU decomposition. If _A_ is a _T_ × _k_ matrix
with _T > k_ , then _X_ is the least-squares solution, _X_ = _(A_ ′ _A)_ −^1 _A_ ′ _B_ , which fails if _A_ ′ _A_ is singular; the
numerical method is the QR decomposition. Otherwise, the operation fails.

For matrix “right division”, as in X = A / B, _X_ is the matrix that solves _XB_ = _A_ , so _A_ and _B_ must
have the same number of columns. If _B_ is non-singular this is in principle equivalent to _AB_ −^1 ,
otherwise _X_ is the least-squares solution.

In “dot” operations a binary operation is applied element by element; the result of this operation
is obvious if the matrices are of the same size. However, there are several other cases where such
operators may be applied. For example, if we write

```
matrix C = A .- B
```
then the result _C_ depends on the dimensions of _A_ and _B_. Let _A_ be an _m_ × _n_ matrix and let _B_ be
_p_ × _q_ ; the result is as follows:

```
Case Result
Dimensions match ( m = p and n = q ) cij = aij − bij
A is a column vector; rows match ( m = p ; n = 1) cij = ai − bij
B is a column vector; rows match ( m = p ; q = 1) cij = aij − bi
A is a row vector; columns match ( m = 1; n = q ) cij = aj − bij
B is a row vector; columns match ( m = p ; q = 1) cij = aij − bj
A is a column vector; B is a row vector ( n = 1; p = 1) cij = ai − bj
A is a row vector; B is a column vector ( m = 1; q = 1) cij = aj − bi
A is a scalar ( m = 1 and n = 1) cij = a − bij
B is a scalar ( p = 1 and q = 1) cij = aij − b
```
If none of the above conditions are satisfied the result is undefined and an error is flagged.


Chapter 17. Matrix manipulation 149

Note that this convention makes it unnecessary, in most cases, to use diagonal matrices to perform
transformations by means of ordinary matrix multiplication: if _Y_ = _XV_ , where _V_ is diagonal, it is
computationally much more convenient to obtain _Y_ via the instruction

```
matrix Y = X .* v
```
where v is a row vector containing the diagonal of _V_.

Concatenation

In _column-wise concatenation_ of an _m_ × _n_ matrix _A_ and an _m_ × _p_ matrix _B_ , the result is an _m_ × _(n_ + _p)_
matrix. That is,

```
matrix C = A ~ B
```
produces _C_ =

```
h
A B
```
```
i
```
_Row-wise concatenation_ of an _m_ × _n_ matrix _A_ and an _p_ × _n_ matrix _B_ produces an _(m_ + _p)_ × _n_
matrix. That is,

```
matrix C = A | B
```
produces _C_ =

#### "

#### A

#### B

#### #

In general the two matrix operands must be conformable, as indicated above. But as a special case
for convenience, a scalar or 1× 1 matrix can be concatenated with a matrix of any size; the single
value is automatically repeated, if necessary, to form a row or column vector of length conformable
with the matrix in question. So for example

```
matrix A = {1, 2, 3}
matrix B = A | 1
```
produces _B_ =

#### "

#### 1 2 3

#### 1 1 1

#### #

### 17.6 Matrix–scalar operators

For matrix _A_ and scalar _k_ , the operators shown in Table 17.2 are available. (Addition and subtrac-
tion were discussed in section 17.5 but we include them in the table for completeness.) In addition,
for square _A_ and scalar _x_ , B = A^x produces a matrix _B_ which is _A_ raised to the power _x_ , but only
if either of two conditions are satisfied. First, if _x_ is a non-negative integer then Golub and Van
Loan’s “Binary Powering” Algorithm 11.2.2 is used — see Golub and Van Loan (1996) — and _A_ can
then be a generic square matrix. Second, if _A_ is positive semidefinite the power is computed via its
eigen-decomposition and _x_ can be a real number, subject to the constraint that _x_ can be negative
only if _A_ is invertible.

### 17.7 Matrix functions

Most of the functions available for scalars and series also apply to matrices on an element-by-
element basis. This is the case for log, exp, sqrt, sin and many others. For example, if a matrix A
is already defined, then

```
matrix B = sqrt(A)
```

Chapter 17. Matrix manipulation 150

```
Expression Effect
matrix B = A * k bij = kaij
matrix B = A / k bij = aij/k
matrix B = k / A bij = k/aij
matrix B = A + k bij = aij + k
matrix B = A - k bij = aij − k
matrix B = k - A bij = k − aij
matrix B = A % k bij = aij modulo k
```
```
Table 17.2: Matrix–scalar operators
```
generates a matrix such that _bij_ =

#### √

_aij_. All such functions require a single matrix as argument, or
an expression which evaluates to a single matrix.^1

In this section, we review some aspects of functions that apply specifically to matrices. A full
account of each function is available in the _Gretl Command Reference_.

Matrix manipulation
bin2dec cnameset cols dec2bin diag diagcat
halton I lower mlag mnormal mrandgen
mreverse mshape msortby msplitby muniform ones
rnameset rows selifc selifr seq trimr
unvech upper vec vech zeros

Matrix algebra
cholesky cnumber commute conv2d det eigen
eigensym eigsolve fft ffti ginv hdprod
infnorm inv invpd ldet Lsolve mexp
mlog nullspace onenorm psdroot qform qrdecomp
rank rcond svd toepsolv tr transp

Statistics/transformations
aggregate bkw corr corresp cov ecdf
fcstats ghk gini imaxc imaxr iminc
iminr kpsscrit max maxc maxr mcorr
mcov mcovg meanc meanr min minc
minr mols mpols mrls mxtab normtest
npcorr princomp prodc prodr quadtable quantile
ranking resample sdc sphericorrsst sumc
sumr uniq values

Numerical methods
BFGSmax BFGScmax fdjac fzero GSSmax NMmax
NRmax numhess simann

```
Table 17.3: Matrix functions by category
```
(^1) Note that to find the “matrix square root” you need the cholesky function (see below). And since the exp function
computes the exponential element by element, it does _not_ return the matrix exponential unless the matrix is diagonal.
To get the matrix exponential, use mexp.


Chapter 17. Matrix manipulation 151

Matrix reshaping

In addition to the methods discussed in sections 17.1 and 17.3, a matrix can also be created by
re-arranging the elements of a pre-existing matrix. This is accomplished via the mshape function.
It takes three arguments: the input matrix, _A_ , and the rows and columns of the target matrix, _r_
and _c_ respectively. Elements are read from _A_ and written to the target in column-major order. If _A_
contains fewer elements than _n_ = _r_ × _c_ , they are repeated cyclically; if _A_ has more elements, only
the first _n_ are used.

For example:

```
matrix a = mnormal(2,3)
a
matrix b = mshape(a,3,1)
b
matrix b = mshape(a,5,2)
b
```
produces

```
? a
a
```
```
1.2323 0.99714 -0.39078
0.54363 0.43928 -0.48467
```
```
? matrix b = mshape(a,3,1)
Generated matrix b
? b
b
```
```
1.2323
0.54363
0.99714
```
```
? matrix b = mshape(a,5,2)
Replaced matrix b
? b
b
```
```
1.2323 -0.48467
0.54363 1.2323
0.99714 0.54363
0.43928 0.99714
-0.39078 0.43928
```
Multiple returns and the **null** keyword

The functions listed below take one or more matrices as arguments and compute one or more
matrices.

```
eigensym Eigen-analysis of symmetric matrix
eigen Eigen-analysis of general matrix
mols Matrix OLS
qrdecomp QR decomposition
svd Singular value decomposition (SVD)
```

Chapter 17. Matrix manipulation 152

The “main” result of the function is always returned as the result proper. Auxiliary returns, if
wanted, are retrieved using pre-existing matrices, passed to the function in “pointer” form (Sec-
tion 14.4). If such values are not needed, the pointer may be substituted with the keyword null.

The syntax for qrdecomp and eigensym is of the form

```
matrix B = func(A, &C)
```
The first argument, A, represents the input data, that is, the matrix whose decomposition or analysis
is required. The second argument must be either the name of an existing matrix preceded by & (to
indicate the “address” of the matrix in question), in which case an auxiliary result is written to that
matrix, or the keyword null, in which case the auxiliary result is not produced.

In case a non-null second argument is given, the specified matrix will be over-written with the
auxiliary result. (It is not required that the existing matrix be of the right dimensions to receive the
result.)

The function eigensym computes the eigenvalues, and optionally the right eigenvectors, of a sym-
metric _n_ × _n_ matrix. The eigenvalues are returned directly in a column vector of length _n_ ; if the
eigenvectors are required, they are returned in an _n_ × _n_ matrix. For example:

```
matrix V = {}
matrix E = eigensym(M, &V)
matrix E = eigensym(M, null)
```
In the first case E holds the eigenvalues of M and V holds the eigenvectors. In the second, E holds
the eigenvalues but the eigenvectors are not computed.

The function eigen computes the eigenvalues, and optionally the right and/or left eigenvectors,
of a general _n_ × _n_ matrix. Following the input matrix argument there are two slots for matrix-
addresses, the first to retrieve the right eigenvectors and the second for the left. Calls to this
function should therefore conform to one of the following patterns.

```
# get the eigenvalues only
matrix E = eigen(M)
```
```
# get the right eigenvectors as well
matrix V = {}
matrix E = eigen(M, &V)
```
```
# get both sets of eigenvectors
matrix V = {}
matrix W = {}
matrix E = eigen(M, &V, &W)
```
```
# get the left eigenvectors but not the right
matrix W = {}
matrix E = eigen(M, null, &W)
```
The eigenvalues are returned directly in a complex _n_ -vector. If the eigenvectors are wanted they
are returned in a _n_ × _n_ complex matrix.

The qrdecomp function computes the QR decomposition of an _m_ × _n_ matrix _A_ : _A_ = _QR_ , where _Q_
is an _m_ × _n_ orthogonal matrix and _R_ is an _n_ × _n_ upper triangular matrix. The matrix _Q_ is returned
directly, while _R_ can be retrieved via the second argument. Here are two examples:

```
matrix R
matrix Q = qrdecomp(M, &R)
matrix Q = qrdecomp(M, null)
```

Chapter 17. Matrix manipulation 153

In the first example, the triangular _R_ is saved as R; in the second, _R_ is discarded. The first line
above shows an example of a “simple declaration” of a matrix: R is declared to be a matrix but is
not given any explicit value. The result is that it is automatically initialized as an empty matrix (see
Section 17.2).

The syntax for svd is

```
matrix B = func(A, &C, &D)
```
The function svd computes all or part of the singular value decomposition of the real _m_ × _n_ matrix
_A_. Let _k_ = min _(m,n)_. The decomposition is

```
A = U Σ V ′
```
where _U_ is an _m_ × _k_ orthogonal matrix, Σ is an _k_ × _k_ diagonal matrix, and _V_ is an _k_ × _n_ orthogonal
matrix.^2 The diagonal elements of Σ are the singular values of _A_ ; they are real and non-negative,
and are returned in descending order. The first _k_ columns of _U_ and _V_ are the left and right singular
vectors of _A_.

The svd function returns the singular values, in a vector of length _k_. The left and/or right singu-
lar vectors may be obtained by supplying non-null values for the second and/or third arguments
respectively. For example:

```
matrix s = svd(A, &U, &V)
matrix s = svd(A, null, null)
matrix s = svd(A, null, &V)
```
In the first case both sets of singular vectors are obtained, in the second case only the singular
values are obtained; and in the third, the right singular vectors are obtained but _U_ is not computed.
_Please note_ : when the third argument is non-null, it is actually _V_ ′that is provided. To reconstitute
the original matrix from its SVD, one can do:

```
matrix s = svd(A, &U, &V)
matrix B = (U.*s)*V
```
Finally, the syntax for mols is

```
matrix B = mols(Y, X, &U)
```
This function returns the OLS estimates obtained by regressing the _T_ × _n_ matrix _Y_ on the _T_ × _k_
matrix _X_ , that is, a _k_ × _n_ matrix holding _(X_ ′ _X)_ −^1 _X_ ′ _Y_. The Cholesky decomposition is used. The
matrix _U_ , if not null, is used to store the residuals.

Reading and writing matrices from/to text files

The two functions mread and mwrite can be used for basic matrix input/output. This can be useful
to enable gretl to exchange data with other programs.

The mread function accepts one string parameter: the name of the (plain text) file from which the
matrix is to be read. The file in question may start with any number of comment lines, defined
as lines that start with the hash mark, “#”; such lines are ignored. Beyond that, the content must
conform to the following rules:

1. The first non-comment line must contain two integers, separated by a space or a tab, indicat-
    ing the number of rows and columns, respectively.

(^2) This is not the only definition of the SVD: some writers define _U_ as _m_ × _m_ , Σ as _m_ × _n_ (with _k_ non-zero diagonal
elements) and _V_ as _n_ × _n_.


Chapter 17. Matrix manipulation 154

2. The columns must be separated by spaces or tab characters.
3. The decimal separator must be the dot “.” character.

Should an error occur (such as the file being badly formatted or inaccessible), an empty matrix (see
section 17.2) is returned.

The complementary function mwrite produces text files formatted as described above. The column
separator is the tab character, so import into spreadsheets should be straightforward. Usage is
illustrated in Listing 17.1. Matrices stored via the mwrite command can be easily read by other
programs; the following table summarizes the appropriate commands for reading a matrix A from
a file called a.mat in some widely-used programs.^3 Note that the Python example requires that the
numpy module is loaded.

```
Program Sample code
GAUSS tmp[] = load a.mat;
A = reshape(tmp[3:rows(tmp)],tmp[1],tmp[2]);
Octave fd = fopen("a.mat");
[r,c] = fscanf(fd, "%d %d", "C");
A = reshape(fscanf(fd, "%g", r*c),c,r)’;
fclose(fd);
Ox decl A = loadmat("a.mat");
R A <- as.matrix(read.table("a.mat", skip=1))
Python A = numpy.loadtxt(’a.mat’, skiprows=1)
Julia A = readdlm("a.mat", skipstart=1)
```
Optionally, the mwrite and mread functions can use gzip compression: this is invoked if the name
of the matrix file has the suffix “.gz.” In this case the elements of the matrix are written in a single
column. Note, however, that compression should not be applied when writing matrices for reading
by third-party software unless you are sure that the software can handle compressed data.

### 17.8 Matrix accessors

In addition to the matrix functions discussed above, various “accessor” strings allow you to create
copies of internal matrices associated with models previously estimated. These are set out in
Table 17.4.

Many of the accessors in Table 17.4 behave somewhat differently depending on the sort of model
that is referenced, as follows:

- Single-equation models: $sigma gets a scalar (the standard error of the regression); $coeff
    and $stderr get column vectors; $uhat and $yhat get series.
- System estimators: $sigma gets the cross-equation residual covariance matrix; $uhat and
    $yhat get matrices with one column per equation. The format of $coeff and $stderr de-
    pends on the nature of the system: for VARs and VECMs (where the matrix of regressors is
    the same for all equations) these return matrices with one column per equation, but for other
    system estimators they return a big column vector.
- VARs and VECMs: $vcv is not available, but _X_ ′ _X_ −^1 (where _X_ is the common matrix of regres-
    sors) is available as $xtxinv, such that for VARs and VECMs (without restrictions on _α_ ) a vcv
    equivalent can be easily and efficiently constructed as $sigma ** $xtxinv.

(^3) Matlab users may find the Octave example helpful, since the two programs are mostly compatible with one another.


Chapter 17. Matrix manipulation 155

```
Listing 17.1: Matrix input/output via text files [Download▼]
```
nulldata 64
scalar n = 3
string f1 = "a.csv"
string f2 = "b.csv"

matrix a = mnormal(n,n)
matrix b = inv(a)

err = mwrite(a, f1)

if err != 0
fprintf "Failed to write %s\n", f1
else
err = mwrite(b, f2)
endif

if err != 0
fprintf "Failed to write %s\n", f2
else
c = mread(f1)
d = mread(f2)
a = c*d
printf "The following matrix should be an identity matrix\n"
print a
endif

```
$coeff matrix of estimated coefficients
$compan companion matrix (after VAR or VECM estimation)
$jalpha matrix α (loadings) from Johansen’s procedure
$jbeta matrix β (cointegration vectors) from Johansen’s procedure
$jvbeta covariance matrix for the unrestricted elements of β from Johansen’s procedure
$rho autoregressive coefficients for error process
$sigma residual covariance matrix
$stderr matrix of estimated standard errors
$uhat matrix of residuals
$vcv covariance matrix of parameter estimates
$vma VMA matrices in stacked form (see section 32.2)
$yhat matrix of fitted values
```
```
Table 17.4: Matrix accessors for model data
```

Chapter 17. Matrix manipulation 156

If the accessors are given without any prefix, they retrieve results from the last model estimated, if
any. Alternatively, they may be prefixed with the name of a saved model plus a period (.), in which
case they retrieve results from the specified model. Here are some examples:

```
matrix u = $uhat
matrix b = m1.$coeff
matrix v2 = m1.$vcv[1:2,1:2]
```
The first command grabs the residuals from the last model; the second grabs the coefficient vector
from model m1; and the third (which uses the mechanism of submatrix selection described above)
grabs a portion of the covariance matrix from model m1.

If the model in question a VAR or VECM (only) $compan and $vma return the companion matrix and
the VMA matrices in stacked form, respectively (see section 32.2 for details). After a vector error
correction model is estimated via Johansen’s procedure, the matrices $jalpha and $jbeta are also
available. These have a number of columns equal to the chosen cointegration rank; therefore, the
product

```
matrix Pi = $jalpha * $jbeta’
```
returns the reduced-rank estimate of _A(_ 1 _)_. Since _β_ is automatically identified via the Phillips nor-
malization (see section 33.5), its unrestricted elements do have a proper covariance matrix, which
can be retrieved through the $jvbeta accessor.

### 17.9 Namespace issues

Matrices share a common namespace with data series and scalar variables. In other words, no two
objects of any of these types can have the same name. It is an error to attempt to change the type
of an existing variable, for example:

```
scalar x = 3
matrix x = ones(2,2) # wrong!
```
It is possible, however, to delete or rename an existing variable then reuse the name for a variable
of a different type:

```
scalar x = 3
delete x
matrix x = ones(2,2) # OK
```
### 17.10 Creating a data series from a matrix

Section 17.1 above describes how to create a matrix from a data series or set of series. You may
sometimes wish to go in the opposite direction, that is, to copy values from a matrix into a regular
data series. The syntax for this operation is

series _sname_ = _mspec_

where _sname_ is the name of the series to create and _mspec_ is the name of the matrix to copy from,
possibly followed by a matrix selection expression. Here are two examples.

```
series s = x
series u1 = U[,1]
```
It is assumed that x and U are pre-existing matrices. In the second example the series u1 is formed
from the first column of the matrix U.


Chapter 17. Matrix manipulation 157

For this operation to work, the matrix (or matrix selection) must be a vector with length equal to
either the full length of the current dataset, _n_ , or the length of the current sample range, _n_ ′. If
_n_ ′ _< n_ then only _n_ ′elements are drawn from the matrix; if the matrix or selection comprises _n_
elements, the _n_ ′values starting at element _t_ 1 are used, where _t_ 1 represents the starting observation
of the sample range. Any values in the series that are not assigned from the matrix are set to the
missing code.

### 17.11 Matrices and lists

To facilitate the manipulation of named lists of series (see Chapter 15), it is possible to convert
between matrices and lists. In section 17.1 above we mentioned the facility for creating a matrix
from a list of variables, as in

```
matrix M = { listname }
```
That formulation, with the name of the list enclosed in braces, builds a matrix whose columns hold
the series referenced in the list. What we are now describing is a different matter: if we say

```
matrix M = listname
```
(without the braces), we get a row vector whose elements are the ID numbers of the series in the
list. This special case of matrix generation cannot be embedded in a compound expression. The
syntax must be as shown above, namely simple assignment of a list to a matrix.

To go in the other direction, you can include a matrix on the right-hand side of an expression that
defines a list, as in

```
list Xl = M
```
where M is a matrix. The matrix must be suitable for conversion; that is, it must be a row or column
vector containing non-negative integer values, none of which exceeds the highest ID number of a
series in the current dataset.

Listing 17.2 illustrates the use of this sort of conversion to “normalize” a list, moving the constant
(variable 0) to first position.

### 17.12 Deleting a matrix

To delete a matrix, just write

```
delete M
```
where M is the name of the matrix to be deleted.

### 17.13 Printing a matrix

To print a matrix, the easiest way is to give the name of the matrix in question on a line by itself,
which is equivalent to using the print command:

```
matrix M = mnormal(100,2)
M
print M
```
You can get finer control on the formatting of output by using the printf command, as illustrated
in the interactive session below:


Chapter 17. Matrix manipulation 158

```
Listing 17.2: Manipulating a list [Download▼]
```
function void normalize_list (matrix *x)
# If the matrix (representing a list) contains var 0,
# but not in first position, move it to first position
if (x[1] != 0)
scalar k = cols(x)
loop for (i=2; i<=k; i++)
if (x[i] == 0)
x[i] = x[1]
x[1] = 0
break
endif
endloop
endif
end function

open data9-7
list Xl = 2 3 0 4
matrix x = Xl
normalize_list(&x)
list Xl = x
list Xl print

```
? matrix Id = I(2)
matrix Id = I(2)
Generated matrix Id
? print Id
print Id
Id (2 x 2)
```
```
1 0
0 1
```
```
? printf "%10.3f", Id
1.000 0.000
0.000 1.000
```
For presentation purposes you may wish to give titles to the columns of a matrix. For this you can
use the function cnameset. The first argument to this function is a matrix and the second can take
any of three forms: a string that contains as many space-separated substrings as the matrix has
columns; an array of strings (see Section 11.8) of the right length; or a named list of series, whose
names will be used as headings. For example,

```
? matrix M = mnormal(3,3)
? cnameset(M, "foo bar baz")
? print M
M (3 x 3)
```
```
foo bar baz
1.7102 -0.76072 0.089406
-0.99780 -1.9003 -0.25123
-0.91762 -0.39237 -1.6114
```
Row names may be added via the function rnameset, which works in the same way.


Chapter 17. Matrix manipulation 159

### 17.14 Example: OLS using matrices

Listing 17.3 shows how matrix methods can be used to replicate gretl’s built-in OLS functionality.

```
Listing 17.3: OLS via matrix methods [Download▼]
```
open data4-1
matrix X = { const, sqft }
matrix y = { price }
matrix b = invpd(X’X) * X’y
print "estimated coefficient vector"
b
matrix u = y - X*b
scalar SSR = u’u
scalar s2 = SSR / (rows(X) - rows(b))
matrix V = s2 * inv(X’X)
V
matrix se = sqrt(diag(V))
print "estimated standard errors"
se
# compare with built-in function
ols price const sqft --vcv


## Chapter 18

Complex matrices

### 18.1 Introduction

Native support for complex matrices was added to gretl in version 2019d.^1 Not all of hansl’s
matrix functions accept complex input, but we have enabled a sizable subset of these functions
which should suffice for most econometric purposes.

Complex numbers are not used in most areas of econometrics, but there are a few notable ex-
ceptions: among these, complex numbers allow for an elegant treatment of univariate spectral
analysis of time series, and become indispensable if you consider multivariate spectral analysis —
see for example Shumway and Stoffer (2017). A more recent example is the numerical solution of
linear models with rational expectations, which are widely used in modern macroeconomics, for
which the complex Schur factorization has become the tool of choice (Klein, 2000).

A first point to note is that complex values are treated as a special case of the hansl matrix type;
there’s no complex type as such. Complex scalars fall under the matrix type as 1× 1 matrices; the
hansl scalar type is only for real values (as is the series type). A 1× 1 complex matrix should do
any work you might require of a complex scalar.

Before we proceed to the details of complex matrices in gretl, here’s a brief reminder of the relevant
concepts and notation. Complex numbers are pairs of the form _a_ + _bi_ where _a_ and _b_ are real
numbers and _i_ is defined as the square root of −1: _a_ is the real part and _b_ the imaginary part.
One can specify a complex number either via _a_ and _b_ or in “polar” form. The latter pertains to the
complex plane, which has the real component on the horizontal axis and the imaginary component
on the vertical. The polar representation of a complex number is composed of the length _r_ of
the ray from the origin to the point in question and the angle _θ_ subtended between the positive
real axis and this ray, measured counter-clockwise in radians. In polar form the complex number
_z_ = _a_ + _bi_ can be written as
_z_ =| _z_ | _(_ cos _θ_ + _i_ sin _θ)_ =| _z_ | _eiθ_

where | _z_ | = _r_ =

#### √

_a_^2 + _b_^2 and _θ_ = tan−^1 _(b/a)_. The quantity | _z_ | is known as the modulus of _z_ ,
and _θ_ as its complex “argument” (or sometimes “phase”). The notation ̄ _z_ is used for the complex
conjugate of _z_ : if _z_ = _a_ + _bi_ , then _z_ ̄ = _a_ − _bi_.

### 18.2 Creating a complex matrix

The standard constructor for complex matrices is the complex() function. This takes two argu-
ments, giving the real and imaginary parts respectively, and sticks them together, as in

```
C = complex(A, B)
```
Four cases are supported, as follows.

- A and B are both _m_ × _n_ real matrices Then C is an _m_ × _n_ complex matrix such that _ckj_ =
    _akj_ + _bkji_.
- A and B are both scalars: C is a 1× 1 complex matrix such that _c_ = _a_ + _bi_.

(^1) Prior to that release gretl offered improvised support for some complex functionality; see section 18.7 for details.

#### 160


Chapter 18. Complex matrices 161

- A is an _m_ × _n_ real matrix and B is a scalar: C is an _m_ × _n_ matrix such that _ckj_ = _akj_ + _bi_.
- A is a scalar and B is an _m_ × _n_ real matrix: C is an _m_ × _n_ matrix such that _ckj_ = _a_ + _bkji_.

In addition, complex matrices may naturally arise as the result of certain computations.

With both real and complex matrices in circulation, one may wish to determine whether a particular
matrix is complex. The function iscomplex() can tell you. Passed an identifier, it returns non-zero
if it names a complex matrix, 0 if it names a real matrix, or NA otherwise. The non-zero return value
is either 1 or 2, with the following interpretation:

- 1 indicates that the matrix is “nominally complex” (each element is represented as having a
    real part and an imaginary part) but all imaginary parts are zero.
- 2 indicates that at least one element has a non-zero imaginary part.

The following code snippet illustrates the point.

```
matrix z1 = complex(1,0)
scalar a = iscomplex(z1)
matrix z2 = complex(1,1)
scalar b = iscomplex(z2)
printf "a = %d, b = %d\n", a, b
```
The code above gives

```
a = 1, b = 2
```
### 18.3 Indexation

Indexation of complex matrices works as with real matrices, on the understanding that each ele-
ment of a complex matrix is a complex pair. So for example C[i,j] gets you the complex pair at
row i, column j of C, in the form of a 1× 1 complex matrix.

If you wish to access just the real or imaginary part of a given element, or range of elements, you
can use the functions Re() or Im(), as in

```
scalar rij = Re(C[i,j])
```
which gets you the real part of _cij_.

In addition the dummy selectors real and imag can be used to assign to just the real or imaginary
component of a complex matrix. Here are two examples:

```
# replace the real part of C with random normals
C[real] = mnormal(rows(C), cols(C))
```
```
# set the imaginary part of C to all zeros
C[imag] = 0
```
The replacement must be either a real matrix of the same dimensions as the target, or a scalar.

Further, the real and imag selectors may be combined with regular selectors to access specific
portions of a complex matrix for either reading or writing. Examples:

```
# retrieve the real part of a submatrix of C
matrix R = C[1:2,1:2][real]
```
```
# set the imaginary part of C[3,3] to y
C[3,3][imag] = y
```

Chapter 18. Complex matrices 162

### 18.4 Operators

Most of the operators available for working with real matrices are also available for complex ones;
this includes the “dot-operators” which work element-wise or by “broadcasting” vectors. Moreover,
mixed operands are accepted, as in D = C + A where C is complex and A real; the result, D, will be
complex. In such cases the real operand is treated as a complex matrix with an all-zero imaginary
part.

The operators _not_ defined for complex values are:

- Those that include the inequality tests “>” or “<”, since complex values as such cannot be
    compared as greater or lesser (though they can be compared as equal or not equal).
- The (real) modulus operator (percent sign), as in x % y which gives the remainder on division
    of x by y.

As for real matrices, the transposition operator “’” is available in both unary form, as in B = A’,
and binary form, as in C = A’B (transpose-multiply). But note that for complex A this means the
conjugate transpose, _A_ H. If you need the non-conjugated transpose you can use transp().

You may wish to note: although none of gretl’s explicit regression functions (or commands) accept
complex input you can calculate parameter estimates for a least-squares regression of complex _Y_
( _T_ × 1) on complex _X_ ( _T_ × _k_ ) via B = X \ Y.

### 18.5 Functions

To give an idea of what works, and what doesn’t, for complex matrices, we’ll walk through the hansl
function-space using the categories employed in gretl’s online “Function reference” (under the Help
menu in the GUI program).

Linear algebra

The functions that accept complex arguments are: cholesky, det, ldet, eigen, eigensym (for
Hermitian matrices), fft, ffti, inv, ginv, hdprod, mexp, mlog, qrdecomp, rank, svd, tr, and
transp. Note, however, that mexp and mlog require that the input matrix be diagonalizable, and
cholesky requires a positive definite Hermitian matrix.

In addition there are the complex-only functions ctrans, which gives the conjugate transpose,^2
and schur for the Schur factorization.

Matrix building

Given what was said in section 18.2 above, several of the functions in this category should be
thought of as applying to the real or imaginary part of a complex matrix (for example, ones and
mnormal), and are of course usable in that way. However, some of these functions can be applied
to complex matrices as such, namely, diag, diagcat, lower, upper, vec, vech and unvech.

Please note: when unvech is applied to a suitable real vector it produces a symmetric matrix, but
when applied to a complex vector it produces a Hermitian matrix.

The only functions _not_ available for complex matrices are cnameset and rnameset. That is, you
cannot name the columns or rows of such matrices (although this restriction could probably be
lifted without great difficulty).

(^2) The transp function gives the straight (non-conjugated) transpose of a complex matrix.


Chapter 18. Complex matrices 163

Matrix shaping

The functions that accept complex input are: cols, rows, mreverse, mshape, selifc, selifr and
trimr.

The functions msortby, sort and dsort are excluded for the reason mentioned in section 18.4.

Statistical

Supported for complex input: meanc, meanr, sumc, sumr, prodc and prodr. And that’s all.

Mathematical

In the matrix context, these are functions that are applied element by element. For complex input
the following are supported: log, exp and sqrt, plus all of the trigonometric functions with the
exception of atan2.

In addition there are the complex-only functions cmod (complex modulus, also accessible via abs),
carg (complex argument), conj (complex conjugate), Re (real part) and Im (imaginary part). Note
that carg _(z)_ = atan2 _(y,x)_ for _z_ = _x_ + _yi_. Listing 18.1 illustrates usage of cmod and carg.

Transformations

In this category only two functions can be applied to complex matrices, namely cum and diff.

### 18.6 File input/output

Complex matrices are stored and retrieved correctly in the XML serialization used for gretl session
files (*.gretl).

The functions mwrite and mread work in two modes: binary mode if the filename ends with “.bin”
and text mode otherwise. Both modes handle complex matrices correctly if both the writing and
the reading are to be done by gretl, but for exchange of data with “foreign” programs text mode
will _not_ work for complex matrices as a whole. The options are:

- In text mode, use mwrite and mread on the two parts of a complex matrix separately, and
    reassemble the matrix in the target program.
- Use binary mode (on the whole matrix), if this is supported for the given foreign program.

At present binary mode transfer of complex matrices is supported for octave, python and julia.
Listing 18.2 shows some examples: we export a complex matrix to each of these programs in turn;
calculate its inverse in the foreign program; then verify that the result as imported back into gretl
is the same as that calculated in gretl.

### 18.7 Backward (in)compatibility

Prior to version 2019d gretl did not provide native support for complex matrices. It did, however,
offer an improvised representation of such matrices for certain restricted purposes, taking the
form of an expanded regular gretl matrix with real values and imaginary parts in odd- and even-
numbered columns, respectively. The functions fft, eigengen and polroots returned matrices in
this special form, and the functions cmult and cdiv operated on such matrices.

As of version 2022b, fft and polroots have been redefined to work with “proper” complex ma-
trices as described above. The other affected functions are deprecated and will be removed or
redefined in a subsequent release. If you have any hansl code using the legacy representation the
following brief porting guide may be helpful.


Chapter 18. Complex matrices 164

Listing 18.1: Variant representations of complex numbers. We picked 8 points on the unit circle in the
complex plane, so their modulus is constant and equal to 1. The Polar matrix below shows that the complex
argument is expressed in radians; multiplying by 180/ _π_ gives degrees. The chk matrix verifies that we can
retrieve the orginal representation of the complex values from the polar form in either of the two ways
mentioned at the start of the chapter: _z_ =| _z_ | _(_ cos _θ_ + _i_ sin _θ)_ or _z_ =| _z_ | _eiθ_. [Download▼]

# complex values in a + b*i form
scalar rp5 = sqrt(0.5)
matrix A = {1, rp5, 0, -rp5, -1, -rp5, 0, rp5}’
matrix B = {0, rp5, 1, rp5, 0, -rp5, -1, -rp5}’
matrix Z = complex(A, B)

# calculate modulus and argument
matrix zmod = cmod(Z)
matrix theta = carg(Z)
matrix Polar = zmod ~ theta ~ (theta * 180/$pi)
cnameset(Polar, "modulus radians degrees")
printf "%12.4f\n", Polar

# reconstitute the original Z matrix in two ways
matrix Z1 = zmod .* complex(cos(theta), sin(theta))
matrix Z2 = zmod .* exp(complex(0, theta))
matrix chk = Z ~ Z1 ~ Z2
print chk

Printing of Polar and chk

```
modulus radians degrees
1.0000 0.0000 0.0000
1.0000 0.7854 45.0000
1.0000 1.5708 90.0000
1.0000 2.3562 135.0000
1.0000 3.1416 180.0000
1.0000 -2.3562 -135.0000
1.0000 -1.5708 -90.0000
1.0000 -0.7854 -45.0000
```
1.00000 + 0.00000i 1.00000 + 0.00000i 1.00000 + 0.00000i
0.70711 + 0.70711i 0.70711 + 0.70711i 0.70711 + 0.70711i
0.00000 + 1.00000i 0.00000 + 1.00000i 0.00000 + 1.00000i
-0.70711 + 0.70711i -0.70711 + 0.70711i -0.70711 + 0.70711i
-1.00000 + 0.00000i -1.00000 + 0.00000i -1.00000 + 0.00000i
-0.70711 - 0.70711i -0.70711 - 0.70711i -0.70711 - 0.70711i
0.00000 - 1.00000i 0.00000 - 1.00000i 0.00000 - 1.00000i
0.70711 - 0.70711i 0.70711 - 0.70711i 0.70711 - 0.70711i


Chapter 18. Complex matrices 165

```
Listing 18.2: Exporting and importing complex matrices [Download▼]
```
set seed 34756
matrix C = complex(mnormal(3,3), mnormal(3,3))
D = inv(C)

mwrite(C, "C.bin", 1)

foreign language=octave
C = gretl_loadmat(’C.bin’);
gretl_export(inv(C), ’oct_D.bin’);
end foreign

oct_D = mread("oct_D.bin", 1)
eval D - oct_D

foreign language=python
import numpy as np
C = gretl_loadmat(’C.bin’)
gretl_export(np.linalg.inv(C), ’py_D.bin’)
end foreign

py_D = mread("py_D.bin", 1)
eval D - py_D

foreign language=julia
C = gretl_loadmat("C.bin")
gretl_export(inv(C), "jl_D.bin")
end foreign

jl_D = mread("jl_D.bin", 1)
eval D - jl_D


Chapter 18. Complex matrices 166

Porting old complex code

cmult and cdiv: These functions performed element-wise multiplication and division of complex
column vectors in the old two-column form. The statements

```
# old element-wise operations
c1 = cmult(a1, b1)
d1 = cdiv(a1, b1)
```
can be updated as

```
# new element-wise operations
c2 = a2 .* b2
d2 = a2 ./ b2
```
(where a2 and b2 are new-style complex vectors or matrices). The following statements

```
c3 = a2 * b2
d3 = a2 / b2
```
are also valid but have different effects, the first performing standard (rather than element-wise)
multiplication of matrices (complex or real) and the second performing “right division”, equivalent
to a2 * inv(b2). Note that while the return value from cmult and cdiv could be either a real
vector or a (two column) complex vector, the new-style operations yield a nominally complex result
if at least one of the operands is complex, even if the result has an all-zero imaginary part.

A piece of code that appears in some contexts (such as calculation of a periodogram) is as follows:
given a complex vector, v, compute a vector w holding the squared moduli of the elements of v.
The old-style code to accomplish this was

```
# legacy: v has two columns
w = sumr(v.^2)
```
and the new replacement is

```
# current: v has a single complex column
w = abs(v).^2
```
where abs gives the complex modulus.

eigengen: Most uses of this legacy function simply retrieve the eigenvalues of a general (that is,
not symmetric) matrix, and do not exploit the option of retrieving eigenvectors. In that context it is
straightforward to substitute a call to the new function eigen. The only point to note is that eigen
returns a new-style complex vector; if you have need to convert this to the legacy representation
you can use the cswitch function, which is documented in the _Gretl Command Reference_. In brief,
the following code gives you the legacy equivalent of a new-style complex vector v: newvec.

```
if v[imag] == 0
oldv = v[real]
else
oldv = cswitch(v, 2)
endif
```
polroots: This function now returns a new-style complex vector. As with eigengen, you can use
cswitch to convert the vector if necessary.


## Chapter 19

Calendar dates

### 19.1 Introduction

Any software that aims to handle dates and times must have a good built-in calendar. Gretl of-
fers several functions to handle date and time information, which are documented in the _Gretl
Command Reference_. To facilitate their effective use this chapter lists the various possibilities for
storing dates and times and discusses ways of converting between variant representations. Our
main focus in this chapter is dates as such (year, month and day) but we add some discussion
of time-of-day where relevant. A final section addresses the somewhat arcane issue of handling
historical dates on the Julian calendar.

First of all it may be useful to distinguish two contexts:

- You have a time-series dataset in place, or a panel dataset with a well-defined time dimension.
- You have no such dataset in place, or perhaps no dataset at all.

While you can work with dates in the second case, in the first case you have extra resources.

You probably know that if you open a dataset that is in fact time series but gretl has not immedi-
ately recognized that fact, you can rectify matters by use of the setobs command, or via the menu
item /Data/Dataset structure in the gretl GUI. You may also know that with a panel dataset you
can impose a definite dating and frequency in its time dimension (if appropriate) — again, via the
setobs command but with the --panel-time option.

In what follows we state if a relevant function or accessor requires a time-series dataset or well-
defined panel-data time; otherwise you can assume it does not carry such a requirement.

### 19.2 Date and time representations

In gretl there is more than one way to encode a date such as “May 26th, 1993”. Some are more
intuitive, some less obvious from a human viewpoint but easier to handle for an algorithm. The
basic representations we discuss here are:

1. the three-numbers approach
2. date as string
3. the ISO 8601 standard
4. the epoch day
5. Unix time (seconds)

We first explain what these representations are, then explain how to convert between them.

The three-numbers approach

Since a date (without regard to intra-day detail) basically consists of three numbers, it can obviously
be encoded in precisely that way. For example the date “May 26th, 1993” can be stored as

#### 167


Chapter 19. Calendar dates 168

```
scalar y = 1993
scalar m = 5
scalar d = 26
```
Gretl’s multiple-element objects can be used to extend this approach, for example by using a 3-
element vector for year, month and day, or a 3-column matrix for storing as many dates as desired.
If you wish to store dates as series in your dataset this approach would lead you to use three series,
possibly grouping them into a list, as in

```
nulldata 60
setobs 7 2020-01-01
series y = $obsmajor
series m = $obsminor
series d = $obsmicro
list DATE = y m d
```
This example above will generate daily dates for January and February 2020. Note that use of the
$obsm* accessors requires a time-series dataset, and $obsmicro in particular requires daily data.
See Section 19.5 for details.

Some CSV files represent dates in this sort of broken-down format, with various conventions on
the ordering of the three components.

Date as string

To a human being, this may seem the most natural choice. The string “26/6/1953” is pretty much
unambiguous. But using such a format for machine processing can be problematic due to differing
conventions regarding the separators between day, month and year, as well as the order in which
the three pieces of information are arranged. For example, “2/6/1953” is _not_ unambiguous: it
will “naturally” be read differently by Europeans and Americans. This can be a problem with CSV
files found “in the wild”, containing arbitrarily formatted dates. Therefore gretl provides fairly
comprehensive functionality for converting dates of this sort into more manageable formats.

The ISO 8601 standard

Among other things, the ISO 8601 standard provides two representations for a daily date: the
“basic” representation, which uses an 8-digit integer, and the “extended” representation, which
uses a 10-character string.

In the basic version the first four digits represent the year, the middle two the month and the
rightmost two the day, so that for example 20170219 indicates February 19th, 2017. The extended
representation is similar except that the date is a string in which the items are separated by hy-
phens, so the same date would be represented as “2017-02-19”.

In several contexts ISO 8601 dates are privileged by gretl: the ISO format as taken as the default
and you need to supply an additional function argument or take extra steps if the representation
is non-standard.

Using series and/or matrices to store ISO 8601 basic dates is perfectly straightforward.

Epoch days

In gretl an “epoch day” is an unsigned 32-bit integer which represents a date as the number of
days since January 1, 1 AD (that is, the first day of the Common Era), on the proleptic Gregorian
calendar.^1 For example, 1993-05-26 corresponds to 727709.^2

(^1) The term “proleptic,” as applied to a calendar, indicates that it is extrapolated backwards or forwards relative to its
period of actual historical use.
(^2) This representation derives from the astronomers’ “Julian day” which is also a count of days since a benchmark,
namely January 1, 4713 BC, at which time certain astronomical cycles were aligned.


Chapter 19. Calendar dates 169

This is the convention used by the GLib library, on which gretl depends for much of its calendrical
calculation. Since an epoch day is an unsigned integer, neither GLib nor gretl supports dates “BC”,
or prior to the Common Era.

This representation has several advantages. Like ISO 8601 basic, it lends itself naturally to storing
dates as series. Compared to ISO 8601, it has the disadvantage of not being readily understandable
by humans, but to compensate for that it makes it very easy to determine the length of a range of
dates. ISO basic dates can be used for comparison (which of two dates, on a given calendar, refers
to a later day?) but with epoch days one can carry out fully-fledged “dates arithmetic.” Epoch days
are always consecutive by construction, but 8-digit basic dates are consecutive only within a given
month.^3 For more on arithmetic with epoch days see Section 19.4.

Unix seconds

In this representation — the cornerstone of date and time handling on Unix-like systems — time is
the number of seconds since midnight at the start of 1970 according to Coordinated Universal Time
(UTC).^4 This format is therefore ideal for storing fine-grained information, including time of day as
well as date.

This representation is not transparent to humans (for example, the number 123456789 corre-
sponds to the start of Thursday, 29 Nov 1973) but again it lends itself naturally to calculation.
Since Unix seconds are hard-wired to UTC a given value will correspond to different times, and
possibly different dates, if evaluated in different time zones; we expand on this point below.

### 19.3 Converting between representations

To support conversion between different representations, gretl provides several dedicated func-
tions, although in some cases conversion can be carried out by using general-purpose functions.
Figure 19.1 displays a summary: solid lines represent dedicated functions, while dashed lines in-
dicate that no special function is needed. Numerical formats are depicted as boxes and string
formats as ovals. For a full description of the functions referenced in the figure, see the _Gretl Com-
mand Reference_. In the rest of this section we discuss several cases of conversion with the help of
examples.

Strings and three-number dates

As indicated in Figure 19.1, converting between date strings and the three-number representation
does not require date-specific functions. The two “generic” functions that can be used for this
purpose are printf and sscanf. Here’s how: suppose you encode a date via the three scalars
d=30, m=10 and y=1983. You can use printf to turn it into a date string rather easily, as in

```
eu_s = printf("%d/%m/%y", d, m, y)
us_s = printf("%m/%d/%y", m, d, y)
```
where the two strings follow the European and US conventions, respectively.

The reverse operation, using the sscanf function, is a little trickier (see the _Gretl Command Ref-
erence_ for a full illustration). The string s=“1983-10-30” can be broken down into three scalars
as

```
scalar d m y
n = sscanf(s, "%d-%d-%d", y, m, d)
```
(^3) In fact, they advance by 101 minus the number of days in the previous month at the start of each month other than
January, and by 8870 at the start of each year.
(^4) UTC is, to a first approximation, the time such that the Sun is at its highest point at noon over the prime meridian,
the line of 0° longitude, which as a matter of historical contingency runs through Greenwich, England.


Chapter 19. Calendar dates 170

```
epochday
```
```
ISO integer
```
```
isodate
```
```
ISO extended
```
```
isodate
```
```
list (dmy)
```
```
epochday
```
```
genr
```
```
Generic string
```
```
printf printf
```
```
epochday
```
```
isoconv
```
```
Unix seconds
```
```
strpday/strfday
```
```
sscanf
```
```
strptime/strftime
```
```
strpday/strfday
```
```
sscanf
```
```
substr + atof
```
```
strptime/strftime
```
```
Figure 19.1: Conversions between different date formats
```
Note that in this case “%d” in the format specification does not mean “day”, but rather “decimal
integer”, which is why there are three instances. Alternatively, one could have used a 3-element
vector, as in

```
matrix date = zeros(1,3)
n = sscanf(s, "%d-%d-%d", &date[1], &date[2], &date[3])
```
Decomposing a series of “basic” dates

To generate from a series of dates in ISO 8601 basic format distinct series holding year, month and
day, the function isoconv can be used. This function should be passed the original series followed
by “pointers to” the series to be filled out. For example, if we have a series named dates in the
prescribed format we might do

```
series y, m, d
isoconv(dates, &y, &m, &d)
```
This is mostly just a convenience function: provided the dates input is valid on the (possibly
proleptic) Gregorian calendar it is equivalent to:

```
series y = floor(dates/10000)
series m = floor((dates-10000*y)/100)
series d = dates - 10000*y - 100*m
```
However, there is some “value added”: isoconv checks the validity of the dates input. If the
implied year, month and day for any dates observation do not correspond to a valid date, then all
the derived series will have value NA at that observation.

The inverse operation is trivial:


Chapter 19. Calendar dates 171

```
series dates = 10000 * y + 100 * m + d
```
The use of series here means that such operations require that a dataset is in place, but although
they would most naturally occur in the context of a time-series dataset they could equally well
occur with an undated dataset, since an ISO 8601 basic value is just a numeric value (with some
restrictions) and such values do not have to appear in chronological order.

String/numeric conversions: dedicated functions

The primary means of converting between string and scalar numeric representations of dates and
times is provided by two pairs of functions, strptime/strftime and strpday/strfday. The first
of each pair takes string input and outputs a numeric value, and the second performs the inverse
operation, as shown in Table 19.1. With the first pair, the numeric value is Unix seconds; with
the second it’s an epoch day. Numeric values are always relative to UTC, and string values are (by
default, at least) always relative to local time.

```
function input output
```
```
strptime date/time string + format Unix seconds
strftime Unix seconds + format date/time string
strpday date string + format epoch day
strfday epoch day + format date string
```
```
Table 19.1: String ←→ numeric date/time conversions
```
Before moving on, let’s be clear on what we mean by “local time”. Generically, this is time according
to the local time zone (with or without a “Daylight saving” or “Summer” adjustment depending on
the time of year). In a computing context we have to be more specific: the “local” time zone
is whatever is set as such via the operating system (and possibly adjusted via an environment
variable) on the host computer. It will usually be the same as the geographically local zone but
there’s nothing to stop a user making a different setting.

Dates as string-valued series

It often happens that CSV files contain date information stored as strings. Take for example a file
containing earthquake data like the following:^5

```
Date Time Latitude Longitude Magnitude
"01/02/1965" "13:44:18" 19.246 145.616 6.0
"01/04/1965" "11:29:49" 1.863 127.352 5.8
"01/05/1965" "18:05:58" -20.579 -173.972 6.2
"01/08/1965" "18:49:43" -59.076 -23.557 5.8
"01/09/1965" "13:32:50" 11.938 126.427 5.8
"01/10/1965" "13:36:32" -13.405 166.629 6.7
"01/12/1965" "13:32:25" 27.357 87.867 5.9
"01/15/1965" "23:17:42" -13.309 166.212 6.0
```
Suppose we want to convert the Date column to epoch days. Note that the date format follows
the American convention month/day/year. The simplest way to accomplish the task is shown
in Listing 19.1, where we assume that the data file is named earthquakes.csv. Note that the
--all-cols option is wanted here, so that gretl treats Dates as a string-valued series rather than
just a source of time-series information. For good measure we show how to add an ISO 8601 date
series.

(^5) See https://www.kaggle.com/datasets/usgs/earthquake-database for the dataset of which this is an extract.


Chapter 19. Calendar dates 172

```
Listing 19.1: Converting a string-valued date series to epoch day
```
open earthquakes.csv --all-cols
series eday = strpday(Date, "%m/%d/%Y")
series isodates = strfday(eday, "%Y-%m-%d")
print Date eday isodates -o

Output:

```
Date eday isodates
```
1 01/02/1965 717338 1965-01-02
2 01/04/1965 717340 1965-01-04
3 01/05/1965 717341 1965-01-05
4 01/08/1965 717344 1965-01-08
5 01/09/1965 717345 1965-01-09
6 01/10/1965 717346 1965-01-10
7 01/12/1965 717348 1965-01-12
8 01/15/1965 717351 1965-01-15

Alternatively, one might like to convert the Date and Time columns jointly to Unix seconds. This
can be done by sticking the two strings together at each observation and calling strptime with a
suitable format, as follows:

```
series usecs # Unix seconds
loop i=1..$nobs
usecs[i] = strptime(Date[i] ~ Time[i], "%m/%d/%Y%H:%M:%S")
endloop
```
Unix seconds and time zones

At 8:46 in the morning of September 11, 2001, an airliner crashed into the North Tower of the
World Trade Center in New York. Relative to what time zone is that statement correct? Eastern
Daylight Time (EDT), of course. Unless we have special reason to do otherwise we report the time
of an event relative to the time zone in which it occurred; and if we do otherwise we need to state
the metric we’re using (for example, one might say that this event occurred at 2001-09-11 12:46
UTC).

Now consider the following script:

```
date = "2001-09-11 08:46"
format = "%Y-%m-%d %H:%M"
usecs = strptime(date, format)
check = strftime(usecs, format)
printf "Unix time %d\n", usecs
printf "original: %s\n", date
printf "recovered: %s\n", check
```
Run this script in any time zone you like and the last line of output will read

```
recovered: 2001-09-11 08:46
```
The usecs value will differ by time zone — for example it’ll be 1000212360 under Eastern Daylight
Time but 1000194360 under Central European Time — but this difference “cancels out” in recover-
ing the original time via strftime.

So far, so good. But suppose I write a script in which I store the date as Unix seconds, with my
laptop’s clock set to EDT:


Chapter 19. Calendar dates 173

```
usecs = 1000212360
date = strftime(usecs, "%Y-%m-%d %H:%M")
print date
```
Running this script under EDT will again print out “2001-09-11 08:46”, but if I take my laptop to
Italy in June, set its clock to the local time, and rerun the script, I’ll get

```
2001-09-11 14:46
```
Is that a problem? Well, 14:46 is indeed the time in Italy when it’s 08:46 in New York (with both
zones in their Summer variants); it’s a problem only if you want to preserve the locality of the
original time. To do that you need to give time-zone information to both strptime and strftime.
This is illustrated in Listing 19.2.

```
Listing 19.2: Date/time invariance with respect to current time zone
```
string date = "2001-09-11 08:46 -0400"
string format = "%Y-%m-%d %H:%M %z"
usecs = strptime(date, format)
printf "Unix time %d\n", usecs

In the code above we specify the time zone in date using -0400, meaning 4 hours behind UTC,
which is correct when Daylight Saving time is in force in the Eastern US. And we match this with
the “%z” specifier in format. As a result, regardless of the time zone in which the code is run the
Unix time value will be 1000212360. Then we come to unpacking that value:

date = strftime(1000212360, "%Y-%m-%d %H:%M %z", -4*3600)
print date

Here we use the third, optional argument to strftime to supply the offset in seconds of EDT
relative to UTC. Having told strptime the time zone, why do we need this? Well, remember that
Unix time is just a scalar value, always relative to UTC: it cannot store time-zone information.
Anyway, the result is that this code will print 2001-09-11 08:46 -0400 regardless of where and
when it is executed.

Some additional comments are in order. First, spaces matter in parsing the strptime arguments:
they must match between the date and format strings. In the example above we inserted spaces
before -0400 and %z. We could have omitted both spaces, but not just one of them. Second, the
C standard does not require that strptime and strftime know anything about time zones; the
extensions used in this example are supported by GLib functionality.

### 19.4 Epoch day arithmetic

Given the way epoch days are defined, they provide a useful tool for checking whether daily data are
complete. Suppose we have what purport to be 7-day daily data with a starting date of 2015-01-01
and an ending date of 2016-12-31. How many observations should there be?

```
ed1 = epochday(2015,1,1)
ed2 = epochday(2016,12,31)
n = ed2 - ed1 + 1
```
We find that there should be n = 731 observations; if there are fewer there’s something missing.
If the data are supposed to be on a 5-day week (skipping Saturday and Sunday) or 6-day week
(skipping Sunday alone) the calculation is more complicated; in this case we can use the dayspan
function, providing as arguments the epoch-day values for the first and last dates and the number
of days per week:


Chapter 19. Calendar dates 174

```
ed1 = epochday(2015,1,1)
ed2 = epochday(2016,12,30)
n = dayspan(ed1, ed2, 5)
```
We discover that there were n = 522 weekdays in this period.

The dayspan function can also be helpful if you wish to construct a suitably sized “empty” daily
dataset prior to importing data from a third-party database (for example, stock prices from Yahoo).
Say the data to be imported are on a 5-day week and you want the range to be from 2000-01-03
(the first weekday in 2000) to 2020-12-30 (a Wednesday). Here’s how one could initialize a suitable
“host” dataset:

```
ed1 = epochday(2000,1,3)
ed2 = epochday(2020,12,30)
n = dayspan(ed1, ed2, 5)
nulldata n
setobs 5 2000-01-03
```
Another use of arithmetic using epoch days is constructing a sequence of dates of non-standard
frequency. Suppose you want a biweekly series including alternate Saturdays in 2023. Here’s a
solution:

```
nulldata 26
setobs 1 1 --special-time-series
series eday
eday[1] = epochday(20230107) # the first Saturday
loop i=2..$nobs
eday[i] = eday[i-1] + 14
endloop
series dates = strfday(eday, "%Y-%m-%d")
```
### 19.5 Other accessors and functions

Accessors

Gretl offers various accessors for generating dates. One is $now, which returns the current date/time
as a 2-element vector. The first element is Unix seconds and the second an epoch day (see Section
19.2). This is always available regardless of the presence or absence of a dataset.

When a time-series dataset is open, up to four accessors are available to retrieve observation dates
as numeric series. First there is $obsdate, which returns ISO 8601 basic dates. If the frequency
is annual, quarterly or monthly these dates represent the first day of the period in question; if
the frequency is hourly this accessor is not available. Then there’s a set of up to three accessors,
$obsmajor, $obsminor and $obsmicro. The availability and interpretation of these values depends
on the character of the dataset, as shown in Table 19.2. For reference, the “constructor” column
shows the argument that should be supplied to the setobs command to impose each frequency on
a dataset, assuming it starts on January 1, 1990.

The hourly frequency is not fully supported by gretl’s calendrical apparatus. But an epoch day
value can be used to set the starting day for an hourly time series, as exemplified in Table 19.2
(726468 for 1990-01-01). One could then construct a string-valued hourly date/time series in this
way:

```
series day = strptime(isodate($obsmajor))
series usecs = day + 3600 * ($obsminor - 1) # Unix seconds
series tstrs = strftime(usecs, "%Y-%m-%d %H:%M")
```
When a panel dataset is open and its time dimension is specified (see Section 19.1 and the docu-
mentation for the setobs command), $obsdate works as described for time-series datasets. But


Chapter 19. Calendar dates 175

```
frequency description constructor $obsmajor $obsminor $obsmicro
1 annual 1 1990 year – –
4 quarterly 4 1990:1 year quarter –
12 monthly 12 1990:01 year month –
5, 6, 7 daily n 1990-01-01 year month day
52 weekly 52 1990-01-01 year month day
24 hourly 24 726468:01 day hour –
```
```
Table 19.2: Calendrical frequencies and accessors
```
$obsmajor and $obsminor do not refer to the time dimension; rather they give the 1-based indices
of the individuals and time periods, respectively. And $obsmicro is not available.

Miscellaneous functions

Besides conversion, several other calendrical functions are available:

monthlen given month and year, returns the length of the month in days (optionally ignoring
weekends).

weekday given a date as year, month and day (or ISO 8601 basic), returns a number from 0 (Sun-
day) to 6 (Saturday) corresponding to day of the week.

juldate given an epoch day, returns the corresponding date on the Julian calendar (see Section 19.6
below).

dayspan given two epoch days, calculates their distance, optionally taking weekends into account.

easterday given the year, returns the date of Easter on the Gregorian calendar.

isoweek given a date as year, month and day, returns the progressive number of the week within
that year as per the ISO 8601 specification.

### 19.6 Working with pre-Gregorian dates

Working with dates is fairly straightforward in the current era, with the Gregorian calendar used
universally for the dating of socioeconomic observations. It is not so straightforward, however,
when dealing with historical data recorded prior to the adoption of the Gregorian calendar in place
of the Julian, an event which first occurred in the principal Catholic countries in 1582 but which
took place at different dates in different countries over a span of several centuries.

Gretl, like most data-oriented software, uses the Gregorian calendar by default for all dates, thereby
ensuring that dates are all consecutive (the latter being a requirement of the ISO 8601 standard for
dates and times).

As readers probably know, the Julian calendar adds a leap day (February 29) on each year that is
divisible by 4 with no remainder. But this over-compensates for the fact that a 365-day year is too
short to keep the calendar synchronized with the seasons. The Gregorian calendar introduced a
more complex rule which maintains better synchronization, namely, each year divisible by 4 with
no remainder is a leap year _unless_ it’s a centurial year (e.g. 1900) in which case it’s a leap year only
if it is divisible by 400 with no remainder. So the years 1600 and 2000 were leap years on both
calendars, but 1700, 1800, and 1900 were leap years only on the Julian calendar. While the average
length of a Julian year is 365.25 days, the Gregorian average is 365.2425 days.

The fact that the Julian calendar inserts leap days more frequently means that the Julian date
progressively (although very slowly) falls behind the Gregorian date. For example, February 18


Chapter 19. Calendar dates 176

2017 (Gregorian) is February 5 2017 on the Julian calendar. On adoption of the Gregorian calendar
it was therefore necessary to skip several days. In England, where the transition occurred in 1752,
Wednesday September 2 was directly followed by Thursday September 14.

In comparing calendars one wants to refer to a given day in terms that are not specific to either
calendar — but how to define a “given day”? This is accomplished by a count of days following some
definite temporal benchmark. As described in Section 19.2, gretl uses days since the start of 1 AD,
which we call epoch days.

In this section we address the problem of constructing within gretl a calendar which agrees with
the actual historical calendar prior to the switch to Gregorian dating. Most people will have no
use for this, but researchers working with archival data may find it helpful: it would be tricky and
error-prone to enter on the Gregorian calendar data whose dates are given on the Julian at source.

In order to represent Julian dates, Gretl uses two basic tools: one is the juldate function, which
converts a Gregorian epoch day into an ISO8601-like integer and the convention that for some
functions, a negative value where a year is expected acts as a “Julian calendar flag”.

So, for example, the following code fragment,

```
edg = epochday(1700,1,1)
edj = epochday(-1700,1,1)
```
produces edg = 620548 and edj = 620558, indicating that the two calendars differed by 10 days at
the point in time known as January 1, 1700, on the proleptic Gregorian calendar.

Taken together with the isodate and juldate functions (which each take an epoch day argument
and return an ISO 8601 basic date on, respectively, the Gregorian and Julian calendars), epochday
can be used to convert between the two calendars. For example, what was the date in England (still
on the Julian calendar) on the day known to Italians as June 26, 1740 (Italy having been on the
Gregorian calendar since October 1582)?

```
ed = epochday(1740,6,26)
english_date = juldate(ed)
printf "%d\n", english_date
```
We find that the English date was 17400615 , the 15th of June. Working in the other direction, what
Italian date corresponded to the 5th of November, 1740, in England?

```
ed = epochday(-1740,11,5)
italian_date = isodate(ed)
printf "%d\n", italian_date
```
Answer: 17401116 ; Guy Fawkes night in 1740 occurred on November 16 from the Italian point of
view.

We’ll now consider the trickiest case, namely a calendar which includes the day on which the Julian
to Gregorian switch occurred. If we can handle this, it should be relatively simple to handle a purely
Julian calendar. Our illustration will be England in 1752 (a similar analysis could be done for Spain
in 1582 or Greece in 1923). A solution is presented in Listing 19.3.

The first step is to find the epoch day corresponding to the Julian date 1752-01-01 (which turns
out to be 639551). Then we can create a series of epoch days, from which we get both Julian and
Gregorian dates for 355 days starting on epoch day 639551. Note, 355 days because this was a
short year: it was a leap year, but 11 days were skipped in September in making the transition to
the Gregorian calendar. We can then construct a series, hcal, which switches calendar at the right
historical point.

Notice that although the series hcal contains the correct historical calendar (in “basic” form), the
observation labels (in the first column of the output) are still just index numbers. It may be prefer-
able to have historical dates in that role. To achieve this we can decompose the hcal series into


Chapter 19. Calendar dates 177

```
Listing 19.3: Historical calendar for Britain in 1752 [Download▼]
```
# 1752 was a short year on the British calendar!
nulldata 355
# give a negative year to indicate Julian date
ed0 = epochday(-1752,1,1)
# consistent series of epoch day values
series ed = ed0 + index - 1
# Julian dates as YYYYMMDD
series jdate = juldate(ed)
# Gregorian dates as YYYYMMDD
series gdate = isodate(ed)
# Historical: cut-over in September
series hcal = ed > epochday(-1752,9,2)? gdate : jdate
# And let’s take a look
print ed jdate gdate hcal -o

Partial output:

```
ed jdate gdate hcal
```
1 639551 17520101 17520112 17520101
2 639552 17520102 17520113 17520102
...
245 639795 17520901 17520912 17520901
246 639796 17520902 17520913 17520902
247 639797 17520903 17520914 17520914
248 639798 17520904 17520915 17520915
...
355 639905 17521220 17521231 17521231


Chapter 19. Calendar dates 178

year, month and day, then use the genr markers apparatus (see chapter 4). Here’s additional code
to do this job and show the result.

```
series y, m, d
isoconv(hcal, &y, &m, &d)
genr markers = "%04d-%02d-%02d", y, m, d
print ed jdate gdate hcal -o
```
Year numbering

A further complication in dealing with archival data is that the year number has not always been
advanced on January 1; for example in Britain prior to 1752, March 25 was taken as the start of
the new year. On gretl’s calendar (whether Julian or Gregorian) the year number _always_ advances
on January 1, but it’s possible to construct observation markers following the old scheme. This is
illustrated for the year 1751 (as we would now call it) in Listing 19.4.

```
Listing 19.4: Historical calendar for England in 1751 [Download▼]
```
nulldata 365 # a common year
ed0 = epochday(-1751,1,1)
ed1 = epochday(-1751,3,25)
series ed = ed0 + index - 1
series jdate = juldate(ed)
series y, m, d
isoconv(jdate, &y, &m, &d)
y = ed < ed1? y-1 : y
genr markers = "%04d-%02d-%02d", y, m, d
print index -o

Partial output:

1750-01-01 1
1750-01-02 2
1750-01-03 3
...
1750-03-23 82
1750-03-24 83
1751-03-25 84
1751-03-26 85
...
1751-12-31 365

Day of week and length of month

Two of the functions described in Section 19.5, that by default operate on the Gregorian calendar,
can be induced to work on the Julian by the trick mentioned above, namely giving the negative of
the year. These are weekday (which takes arguments year, month and day) and monthlen (which
takes arguments month, year and days per week). Thus for example

```
eval weekday(-1700,2,29)
```
gives 4, indicating that Julian February 29, 1700 was a Thursday. And

```
eval monthlen(2,-1900,5)
```

Chapter 19. Calendar dates 179

gives 21, indicating that there were 21 weekdays in Julian February 1900.


## Chapter 20

Mixed-frequency data

### 20.1 Basics

In some cases one may want to handle data that are observed at different frequencies, a facility
known as “MIDAS” (Mixed Data Sampling). A common pairing includes GDP, usually available quar-
terly, and industrial production, often available monthly. The most common context when this
feature is required is specification and estimation of MIDAS models (see Chapter 41), but other
cases are possible.

A gretl dataset formally handles only a single data frequency, but we have adopted a straightfor-
ward means of representing nested frequencies: a higher frequency series _xH_ is represented by a
set of _m_ series, each holding the value of _xH_ in a sub-period of the “base” (lower-frequency) period
(where _m_ is the ratio of the higher frequency to the lower).

This is most easily understood by means of an example. Suppose our base frequency is quarterly
and we wish to include a monthly series in the analysis. Then a relevant fragment of the gretl
dataset might look as shown in Table 20.1. Here, gdpc96 is a quarterly series while indpro is
monthly, so _m_ = 12 _/_ 4 = 3 and the per-month values of indpro are identified by the suffix _m _n_ ,
_n_ = 3 _,_ 2 _,_ 1.

```
gdpc96 indpro_m3 indpro_m2 indpro_m1
```
```
1947:1 1934.47 14.3650 14.2811 14.1973
1947:2 1932.28 14.3091 14.3091 14.2532
1947:3 1930.31 14.4209 14.3091 14.2253
1947:4 1960.70 14.8121 14.7562 14.5606
1948:1 1989.54 14.7563 14.9240 14.8960
1948:2 2021.85 15.2313 15.0357 14.7842
```
```
Table 20.1: A slice of MIDAS data
```
To recover the actual monthly time series for indpro one must read the three relevant series right-
to-left by row. At first glance this may seem perverse, but in fact it is the most convenient setup
for MIDAS analysis. In such models, the high-frequency variables are represented by lists of lags,
and of course in econometrics it is standard to give the most recent lag first _(xt_ − 1 _,xt_ − 2 _,...)_.

One can construct such a dataset manually from “raw” sources using hansl’s matrix-handling meth-
ods or the join command (see Section 20.6 for illustrations), but we have added native support for
the common cases shown below.

```
base frequency higher frequency
```
```
annual quarterly or monthly
quarterly monthly or daily
monthly daily
```
The examples below mostly pertain to the case of quarterly plus monthly data. Section 20.6 has
details on handling of daily data.

#### 180


Chapter 20. Mixed-frequency data 181

A mixed-frequency dataset can be created in either of two ways: by selective importation of series
from a database, or by creating two datasets of different frequencies then merging them.

Importation from a database

Here’s a simple example, in which we draw from the fedstl (St Louis Fed) database which is
supplied in the gretl distribution:

```
clear
open fedstl.bin
data gdpc96
data indpro --compact=spread
store gdp_indpro.gdt
```
Since gdpc96 is a quarterly series, its importation via the data command establishes a quarterly
dataset. Then the MIDAS work is done by the option --compact=spread for the second invocation
of data. This “spreads” the series indpro — which is monthly at source — into three quarterly
series, exactly as shown in Table 20.1.

Merging two datasets

In this case we consider an Excel file provided by Eric Ghysels in his MIDAS Matlab Toolbox,^1
namely mydata.xlsx. This contains quarterly real GDP in Sheet1 and monthly non-farm payroll
employment in Sheet2. A hansl script to build a MIDAS-style file named gdp_payroll_midas.gdt
is shown in Listing 20.1.

```
Listing 20.1: Building a gretl MIDAS dataset via merger
```
# sheet 2 contains monthly employment data
open MIDASv2.2/mydata.xlsx --sheet=2
rename VALUE payems
dataset compact 4 spread
# limit to the sample range of the GDP data
smpl 1947:1 2011:2
setinfo payems_m3 --description="Non-farm payroll employment, month 3 of quarter"
setinfo payems_m2 --description="Non-farm payroll employment, month 2 of quarter"
setinfo payems_m1 --description="Non-farm payroll employment, month 1 of quarter"
store payroll_midas.gdt

# sheet 1 contains quarterly GDP data
open MIDASv2.2/mydata.xlsx --sheet=1
rename VALUE qgdp
setinfo qgdp --description="Real quarterly US GDP"
append payroll_midas.gdt
store gdp_payroll_midas.gdt

Note that both series are simply named VALUE in the source file, so we use gretl’s rename command
to set distinct and meaningful names. The heavy lifting is done here by the line

```
dataset compact 4 spread
```
(^1) See [http://eghysels.web.unc.edu/](http://eghysels.web.unc.edu/) for links.


Chapter 20. Mixed-frequency data 182

which tells gretl to compact an entire dataset (in this case, as it happens, just containing one
series) to quarterly frequency using the “spread” method. Once this is done, it is straightforward
to append the compacted data to the quarterly GDP dataset.

We will put an extended version of this dataset (supplied with gretl, and named gdp_midas.gdt)
to use in subsequent sections.

### 20.2 The notion of a “MIDAS list”

In the following two sections we’ll describe functions that (rather easily) do the right thing if you
wish to create lists of lags or first differences of high-frequency series. However, we should first
be clear about the correct domain for such functions, since they could produce the most diabolical
mash-up of your data if applied to the wrong sort of list argument — for instance, a regular list
containing distinct series, all observed at the “base frequency” of the dataset.

So let us define a MIDAS list: this is a list of _m_ series holding per-period values of a _single_ high-
frequency series, arranged in the order of most recent first, as illustrated above. Given the dataset
shown in Table 20.1, an example of a correctly formulated MIDAS list would be

```
list INDPRO = indpro_m3 indpro_m2 indpro_m1
```
Or, since the monthly observations are already in the required order, we could define the list by
means of a “wildcard”:

```
list INDPRO = indpro_m*
```
Having created such a list, one can use the setinfo command to tell gretl that it’s a _bona fide_
MIDAS list:

```
setinfo INDPRO --midas
```
This will spare you some warnings that gretl would otherwise emit when you call some of the
functions described below. This step should not be necessary, however, if the series in question
are the product of a compact operation with the spread parameter.

Inspecting high-frequency data

The layout of high-frequency data shown in Table 20.1 is convenient for running regressions, but
not very convenient for inspecting and checking such data. We therefore provide some methods
for displaying MIDAS data at their “natural” frequency. Figure 20.1 shows the gretl main window
with the gdp_midas dataset loaded, along with the menu that pops up if you right-click with the
payems series highlighted. The items “Display values” and “Time series plot” show the data on
their original monthly calendar, while the “Display components” item shows the three component
series on a quarterly calendar, as in Table 20.1.

These methods are also available via the command line. For example, the commands

```
list PAYEMS = payems_*
print PAYEMS --byobs --midas
hfplot PAYEMS --with-lines --output=display
```
produce a monthly printout of the payroll employment data, followed by a monthly time-series
plot. (See section 20.5 for more on hfplot.)


Chapter 20. Mixed-frequency data 183

```
Figure 20.1: MIDAS data menu
```
### 20.3 High-frequency lag lists

A basic requirement of MIDAS is the creation of lists of high-frequency lags for use on the right-
hand side of a regression specification. This is possible, but not very convenient, using the gretl’s
lags function; it is made easier by a dedicated variant of that function described below.

For illustration we’ll consider an example presented in Ghysels’ Matlab implementation of MIDAS:
this uses 9 monthly lags of payroll employment, starting at lag 3, in a model for quarterly GDP.
The estimation period for this model starts in 1985Q1. At this observation, the stipulation that we
start at lag 3 means that the first (most recent) lag is employment for October 1984,^2 and the 9-lag
window means that we need to include monthly lags back to February 1984. Let the per-month
employment series be called x_m3, x_m2 and x_m1, and let (quarterly) lags be represented by (-1),
(-2) and so on. Then the terms we want are (reading left-to-right by row):

.. x_m1(-1)
x_m3(-2) x_m2(-2) x_m1(-2)
x_m3(-3) x_m2(-3) x_m1(-3)
x_m3(-4) x_m2(-4).

We could construct such a list in gretl using the following standard syntax. (Note that the third
argument of 1 to lags below tells gretl that we want the terms ordered “by lag” rather than “by
variable”; this is required to respect the order of the terms shown above.)

```
list X = x_m*
# create lags for 4 quarters, "by lag"
list XL = lags(4,X,1)
# convert the list to a matrix
matrix tmp = XL
# trim off the first two elements, and the last
tmp = tmp[3:11]
```
(^2) That is what Ghysels means, but see the sub-section on “Leads and nowcasting” below for a possible ambiguity in
this regard.


Chapter 20. Mixed-frequency data 184

```
# and convert back to a list
XL = tmp
```
However, the following specialized syntax is more convenient:

```
list X = x_m*
setinfo X --midas
# create high-frequency lags 3 to 11
list XL = hflags(3, 11, X)
```
In the case of hflags the length of the list given as the third argument defines the “compaction
ratio” ( _m_ = 3 in this example); we can (in fact, must) specify the lags we want in high-frequency
terms; and ordering of the generated series by lag is automatic.

Word to the wise: do not use hflags on anything other than a MIDAS list as defined in section 20.2,
unless perhaps you have some special project in mind and really know what you are doing.

Leads and nowcasting

Before leaving the topic of lags, it is worth commenting on the question of leads and so-called
“nowcasting” — that is, prediction of the current value of a lower-frequency variable before its mea-
surement becomes available.

In a regular dataset where all series are of the same frequency, lag 1 means the observation from
the previous period, lag 0 is equivalent to the current observation, and lag −1 (or lead 1) is the
observation for the next period into the relative future.

When considering high-frequency lags in the MIDAS context, however, there is no uniquely deter-
mined high-frequency sub-period which is temporally coincident with a given low-frequency period.
The placement of high-frequency lag 0 therefore has to be a matter of convention. Unfortunately,
there are two incompatible conventions in currently available MIDAS software, as follows.

- High-frequency lag 0 corresponds to the _first_ sub-period within the current low-frequency
    period. This is what we find in Eric Ghysels’ MIDAS Matlab Toolbox; it’s also clearly stated and
    explained in Armesto _et al._ (2010).
- High-frequency lag 0 corresponds to the _last_ sub-period in the current low-frequency period.
    This convention is employed in the midasr package for R.^3

Consider, for example, the quarterly/monthly case. In Matlab, high-frequency (HF) lag 0 is the first
month of the current quarter, HF lag 1 is the last month of the prior quarter, and so on. In midasr,
however, HF lag 0 is the last month of the current quarter, HF lag 1 the middle month of the quarter,
and HF lag 3 is the first one to take you “back in time” relative to the start of the current quarter,
namely to the last month of the prior quarter.

In gretl we have chosen to employ the first of these conventions. So lag 1 points to the most
recent sub-period in the previous base-frequency period, lag 0 points to the first sub-period in the
current period, and lag −1 to the second sub-period within the current period. Continuing with
the quarterly/monthly case, monthly observations for lags 0 and −1 are likely to become available
before a measurement for the quarterly variable is published (possibly also a monthly value for lag
−2). The first “truly future” lead does not occur until lag −3.

The hflags function supports negative lags. Suppose one wanted to use 9 lags of a high-frequency
variable, − 1 _,_ 0 _,_ 1 _,...,_ 7, for nowcasting. Given a suitable MIDAS list, X, the following would do the
job:

```
list XLnow = hflags(-1, 7, X)
```
(^3) See [http://cran.r-project.org/web/packages/midasr/,](http://cran.r-project.org/web/packages/midasr/,) and for documentation https://github.com/
mpiktas/midasr-user-guide/raw/master/midasr-user-guide.pdf.


Chapter 20. Mixed-frequency data 185

This means that one could generate a forecast for the current low-frequency period (which is not
yet completed and for which no observation is available) using data from two sub-periods into the
low-frequency period (e.g. the first two months of the quarter).

### 20.4 High-frequency first differences

When working with non-stationary data one may wish to take first differences, and in the MIDAS
context that probably means high-frequency differences of the high-frequency data. Note that the
ordinary gretl functions diff and ldiff will _not_ do what is wanted for series such as indpro, as
shown in Table 20.1: these functions will give per-month _quarterly_ differences of the data (month
3 of the current quarter minus month 3 of the previous quarter, and so on).

To get the desired result one could create the differences before compacting the high-frequency
data but this may not be convenient, and it’s not compatible with the method of constructing a
MIDAS dataset shown in section 20.1. The alternative is to employ the specialized differencing
function hfdiff. This takes one required argument, a MIDAS list as defined in section 20.2. A
second, optional argument is a scalar multiplier (with default value 1.0); this permits scaling the
output series by a constant. There’s also an hfldiff function for creating high-frequency log
differences; this has the same syntax as hfdiff.

So for example, the following creates a list of high-frequency percentage changes (100 times log-
difference) then a list of high-frequency lags of the changes.

```
list X = indpro_*
setinfo X --midas
list dX = hfldiff(X, 100)
list dXL = hflags(3, 11, dX)
```
If you only need the series in the list dXL, however, you can nest these two function calls:

```
list dXL = hflags(3, 11, hfldiff(X, 100))
```
### 20.5 MIDAS-related plots

In the context of MIDAS analysis one may wish to produce time-series plots which show high- and
low-frequency data in correct registration (as in Figures 1 and 2 in Armesto _et al._ , 2010). This can
be done using the hfplot command, which has the following syntax:

hfplot _midas-list_ [; _lflist_ ] _options_

The required argument is a MIDAS list, as defined above. Optionally, one or more lower-frequency
series ( _lflist_ ) can be added to the plot following a semicolon. Supported options are --with-lines,
--time-series and --output. These have the same effects as with the gretl’s gnuplot command.

An example based on Figure 1 in Armesto _et al._ (2010) is shown in Listing 20.2 and Figure 20.2.

### 20.6 Alternative MIDAS data methods

Importation via a column vector

Listing 20.3 illustrates how one can construct via hansl a MIDAS list from a matrix (column vector)
holding data of a higher frequency than the given dataset. In practice one would probably read
high frequency data from file using the mread function, but here we just construct an artificial
sequential vector.

Note the check in the high_freq_list function: we determine the current sample size, T, and
insist that the input matrix is suitably dimensioned, with a single column of length equal to T times
the compaction factor (here 3, for monthly to quarterly).


Chapter 20. Mixed-frequency data 186

```
Listing 20.2: Replication of a plot from Armesto et al [Download▼]
```
open gdp_midas.gdt

# form and label the dependent variable
series dy = log(qgdp/qgdp(-1))*400
setinfo dy --graph-name="GDP"

# form list of annualized HF differences
list X = payems*
list dX = hfldiff(X, 1200)
setinfo dX --graph-name="Payroll Employment"

smpl 1980:1 2009:1
hfplot dX ; dy --with-lines --time-series --output=display

```
-10
```
```
-5
```
```
0
```
```
5
```
```
10
```
```
15
```
```
20
```
```
1980 1985 1990 1995 2000 2005
```
```
Payroll Employment
GDP
```
```
Figure 20.2: Quarterly GDP and monthly Payroll Employment, annualized percentage changes
```

Chapter 20. Mixed-frequency data 187

```
Listing 20.3: Create a midas list from a matrix [Download▼]
```
function list high_freq_list (const matrix x, int compfac, string vname)
list ret = deflist()
scalar T = $nobs
if rows(x) != compfac*T || cols(x) != 1
funcerr "Invalid x matrix"
endif
matrix m = mreverse(mshape(x, compfac, T))’
loop i=1..compfac
scalar k = compfac + 1 - i
ret += genseries(sprintf("%s%d", vname, k), m[,i])
endloop
setinfo ret --midas
return ret
end function

# construct a little "quarterly" dataset
nulldata 12
setobs 4 1980:1

# generate "monthly" data, 1,2,...,36
matrix x = seq(1,3*$nobs)’
print x
# turn into midas list
list H = high_freq_list(x, 3, "test_m")
print H --byobs


Chapter 20. Mixed-frequency data 188

The final command in the script should produce

```
test_m3 test_m2 test_m1
```
1980:1 3 2 1
1980:2 6 5 4
1980:3 9 8 7
...

This functionality is available in the built-in function hflist, which has the same signature as the
hansl prototype above.

Importation via **join**

The join command provides a general and flexible framework for importing data from external
files (see chapter 7).

In order to handle multiple-frequency data, it supports the “spreading” of high-frequency series to
a MIDAS list in a single operation. This requires use of the --aggr option with parameter spread.
There are two acceptable forms of usage, illustrated below. Note that AWM is a quarterly dataset
while hamilton is monthly. First case:

```
open AWM.gdt
join hamilton.gdt PC6IT --aggr=spread
```
and second case:

```
open AWM.gdt
join hamilton.gdt PCI --data=PC6IT --aggr=spread
```
In the first case MIDAS series PC6IT_m3, PC6IT_m2 and PC6IT_m1 are added to the working dataset.
In the second case “PCI” is used as the base name for the imports, giving PCI_m3, PCI_m2 and
PCI_m1 as the names of the per-month series.

Note that only one high-frequency series can be imported in a given join invocation with the
option --aggr=spread, which already implies the writing of multiple series in the lower frequency
dataset.

An important point to note is that the --aggr=spread mechanism (where we map from one higher-
frequency series to a set of lower-frequency ones) relies on finding a known, reliable time-series
structure in the “outer” data file. Native gretl time-series data files will have such a structure, and
also well-formed gretl-friendly CSV files, but not arbitrary comma-separated files. So if you have
difficulty importing data MIDAS-style from a given CSV file using --aggr=spread you might want
to drop back to a more agnostic, piece-wise approach (agnostic in the sense of assuming less about
gretl’s ability to detect any time-series structure that might be present). Here’s an example:

```
open hamilton.gdt
# create month-of-quarter series for filtering
series mofq = ($obsminor - 1) % 3 + 1
# write example CSV file: the first column holds, e.g. "1973M01"
store test.csv PC6IT mofq
open AWM.gdt -q
# import monthly components one at a time, using a filter
join test.csv PCI_m3 --data=PC6IT --tkey=",%YM%m" --filter="mofq==3"
join test.csv PCI_m2 --data=PC6IT --tkey=",%YM%m" --filter="mofq==2"
join test.csv PCI_m1 --data=PC6IT --tkey=",%YM%m" --filter="mofq==1"
list PCI = PCI_*
setinfo PCI --midas
print PCI_m* --byobs
```

Chapter 20. Mixed-frequency data 189

The example is artificial in that a time-series CSV file of suitable frequency written by gretl itself
should work without special treatment. But you may have to add “helper” columns (such as the
mofq series above) to a third-party CSV file to enable a piece-wise MIDAS join via filtering.

Daily data

Daily data (commonly financial-market data) are often used in practical applications of the MIDAS
methodology. It’s therefore important that gretl support use of such data, but there are special
issues arising from the fact that the number of days in a month, quarter or year is not a constant.

It seems to us that it’s necessary to stipulate a fixed, conventional number of days per lower-
frequency period (that is, in practice, per month or quarter, since for the moment we’re ignoring
the week as a basic temporal unit and we’re not yet attempting to support the combination of
annual and daily data). But matters are further complicated by the fact that daily data come in (at
least) three sorts: 5 days per week (as in financial-market data), 6-day (some commercial data which
skip Sunday) and 7-day.

That said, we currently support — via compact=spread, as described in section 20.1 — the following
conversions:

- Daily to monthly: If the daily data are 5-days per week, we impose 22 days per month. This is
    the median, and also the mode, of weekdays per month, although some months have as few
    as 20 weekdays and some have 23. If the daily data are 6-day we impose 26 days per month,
    and in the 7-day case, 30 days per month.
- Daily to quarterly: In this case the stipulated days per quarter are simply 3 times the days-
    per-month values specified above.

So, given a daily dataset, you can say

```
dataset compact 12 spread
```
to convert MIDAS-wise to monthly (or substitute 4 for 12 for a quarterly target). And this is sup-
posed to work whether the number of days per week is 5, 6 or 7.

That leaves the question of how we handle cases where the actual number of days in the calendar
month or quarter falls short of, or exceeds, the stipulated number. We’ll talk this through with
reference to the conversion of 5-day daily data to monthly; all other cases are essentially the same,
_mutatis mutandis_.^4

We start at “day 1,” namely the first relevant daily date within the calendar period (so the first
weekday, with 5-day data). From that point on we fill up to 22 slots with relevant daily observations
(including, not skipping, NAs due to holidays or whatever). If at the end we have daily observations
left over, we ignore them. If we’re short we fill the empty slots with the arithmetic mean of the
valid, used observations;^5 and we fill in any missing values in the same way.

This means that lags 1 to 22 of 5-day daily data in a monthly dataset are always observations from
days within the prior month (or in some cases “padding” that substitutes for such observations);
lag 23 takes you back to the most recent day in the month before that.

Clearly, we _could_ get a good deal fancier in our handling of daily data: for example, letting the
user determine the number of days per month or quarter, and/or offering more elaborate means
of filling in missing and non-existent daily values. It’s not clear that this would be worthwhile, but
it’s open to discussion.

A little daily-to-monthly example is shown in Listing 20.4 and Figure 20.3. The example exercises
the hfplot command (see section 20.5).

(^4) Or should be! We’re not ready to guarantee that just yet.
(^5) This is the procedure followed in some example programs in the MIDAS Matlab Toolbox.


Chapter 20. Mixed-frequency data 190

```
Listing 20.4: Monthly plus daily data [Download▼]
```
# open a daily dataset
open djclose.gdt

# spread the data to monthly
dataset compact 12 spread
list DJ = djc*

# import an actual monthly series
open fedstl.bin
data indpro

# high-frequency plot (set --output=daily.pdf for PDF)
hfplot DJ ; indpro --with-lines --output=display \
{set key top left;}

```
500
```
```
1000
```
```
1500
```
```
2000
```
```
2500
```
```
3000
```
```
1980 1982 1984 1986 1988 1990
```
```
48
```
```
50
```
```
52
```
```
54
```
```
56
```
```
58
```
```
60
```
```
62
```
```
64
```
```
66
djclose (left)
indpro (right)
```
```
Figure 20.3: Monthly industrial production and daily Dow Jones close
```

## Chapter 21

Cheat sheet

This chapter explains how to perform some common — and some not so common — tasks in gretl’s
scripting language, hansl. Some but not all of the techniques listed here are also available through
the graphical interface. Although the graphical interface may be more intuitive and less intimidat-
ing at first, we encourage users to take advantage of the power of gretl’s scripting language as soon
as they feel comfortable with the program.

### 21.1 Dataset handling

“Weird” periodicities

_Problem:_ You have data sampled each 3 minutes from 9am onwards; you’ll probably want to specify
the hour as 20 periods.

_Solution:_

```
setobs 20 9:1 --special
```
_Comment:_ Now functions like sdiff() (“seasonal” difference) or estimation methods like seasonal
ARIMA will work as expected.

Generating a panel dataset of given dimensions

_Problem:_ You want to generate via nulldata a panel dataset and specify in advance the number of
units and the time length of your series via two scalar variables.

_Solution:_

```
scalar n_units = 100
scalar T = 12
scalar NT = T * n_units
```
```
nulldata NT --preserve
setobs T 1:1 --stacked-time-series
```
_Comment:_ The essential ingredient that we use here is the --preserve option: it protects existing
scalars (and matrices, for that matter) from being trashed by nulldata, thus making it possible to
use the scalar _T_ in the setobs command.

Help, my data are backwards!

_Problem:_ Gretl expects time series data to be in chronological order (most recent observation last),
but you have imported third-party data that are in reverse order (most recent first).

_Solution:_

```
setobs 1 1 --cross-section
series sortkey = -obs
dataset sortby sortkey
setobs 1 1950 --time-series
```
#### 191


Chapter 21. Cheat sheet 192

_Comment:_ The first line is required only if the data currently have a time series interpretation: it
removes that interpretation, because (for fairly obvious reasons) the dataset sortby operation is
not allowed for time series data. The following two lines reverse the data, using the negative of the
built-in index variable obs. The last line is just illustrative: it establishes the data as annual time
series, starting in 1950.

If you have a dataset that is mostly the right way round, but a particular variable is wrong, you can
reverse that variable as follows:

```
x = sortby(-obs, x)
```
Dropping missing observations selectively

_Problem:_ You have a dataset with many variables and want to restrict the sample to those observa-
tions for which there are no missing observations for the variables x1, x2 and x3.

_Solution:_

```
list X = x1 x2 x3
smpl --no-missing X
```
_Comment:_ You can save the file via a store command to preserve a subsampled version of the
dataset. Alternative solutions based on the ok function, such as

```
list X = x1 x2 x3
series sel = ok(X)
smpl sel --restrict
```
are perhaps less obvious, but more flexible. Pick your poison.

“By” operations

_Problem:_ You have a discrete variable d and you want to run some commands (for example, estimate
a model) by splitting the sample according to the values of d.

_Solution:_

```
matrix vd = values(d)
m = rows(vd)
loop i=1..m
scalar sel = vd[i]
smpl d==sel --restrict --replace
ols y const x
endloop
smpl --full
```
_Comment:_ The main ingredient here is a loop. You can have gretl perform as many instructions as
you want for each value of d, as long as they are allowed inside a loop. Note, however, that if all
you want is descriptive statistics, the summary command does have a --by option.

Adding a time series to a panel

_Problem:_ You have a panel dataset (comprising observations of _n_ indidivuals in each of _T_ periods)
and you want to add a variable which is available in straight time-series form. For example, you
want to add annual CPI data to a panel in order to deflate nominal income figures.

In gretl a panel is represented in stacked time-series format, so in effect the task is to create a new
variable which holds _n_ stacked copies of the original time series. Let’s say the panel comprises 500
individuals observed in the years 1990, 1995 and 2000 ( _n_ = 500, _T_ = 3), and we have these CPI
data in the ASCII file cpi.txt:


Chapter 21. Cheat sheet 193

```
date cpi
1990 130.658
1995 152.383
2000 172.192
```
What we need is for the CPI variable in the panel to repeat these three values 500 times.

_Solution:_ Simple! With the panel dataset open in gretl,

```
append cpi.txt
```
_Comment:_ If the length of the time series is the same as the length of the time dimension in the
panel (3 in this example), gretl will perform the stacking automatically. Rather than using the
append command you could use the “Append data” item under the File menu in the GUI program.

If the length of your time series does not exactly match the _T_ dimension of your panel dataset,
append will not work but you can use the join command, which is able to pick just the observations
with matching time periods. On selecting “Append data” in the GUI you are given a choice between
plain “append” and “join” modes, and if you choose the latter you get a dialog window allowing you
to specify the key(s) for the join operation. For native gretl data files you can use built-in series that
identify the time periods, such as $obsmajor, for your outer key to match the dates. In the example
above, if the CPI data were in gretl format $obsmajor would give you the year of the observations.

Time averaging of panel datasets

_Problem:_ You have a panel dataset (comprising observations of _n_ indidivuals in each of _T_ periods)
and you want to lower the time frequency by averaging. This is commonly done in empirical growth
economics, where annual data are turned into 3- or 4- or 5-year averages (see for example Islam,
1995).

_Solution:_ In a panel dataset, gretl functions that deal with time are aware of the panel structure,
so they will automatically “do the right thing”. Therefore, all you have to do is use the movavg()
function for computing moving averages and then just drop the years you don’t need. An example
with the Grunfeld dataset follows:

```
open grunfeld
```
```
# how many periods (here: years) to average
ave = 4
```
```
# a dummy for endpoints of each time block
# (using the modulo operator)
series endpoint = ($time % ave == 0)
```
```
list X = invest value kstock # time-varying variables
```
```
# compute averages
loop foreach i X
series $i = movavg($i, ave)
endloop
```
```
# drop extra observations
smpl endpoint --dummy --permanent
```
```
# restore panel structure
setobs firm year --panel-vars
print firm year X -o
```
Running the above script produces (among other output):


Chapter 21. Cheat sheet 194

```
? print firm year X -o
firm year invest value kstock
```
```
1:1 1 1938 344.425 3979.875 105.375
1:2 1 1942 438.000 4188.100 242.375
1:3 1 1946 574.100 4543.700 283.225
1:4 1 1950 574.025 3559.250 950.750
1:5 1 1954 1109.550 5398.300 1660.450
2:1 2 1938 324.350 1911.925 120.650
2:2 2 1942 377.600 2177.325 281.750
2:3 2 1946 332.200 1929.225 231.825
2:4 2 1950 434.725 1691.725 320.150
2:5 2 1954 583.500 2148.925 519.900
...
9:1 9 1938 25.390 290.675 179.250
9:2 9 1942 30.000 281.875 228.250
9:3 9 1946 51.858 364.250 293.500
9:4 9 1950 42.717 285.150 359.500
9:5 9 1954 59.480 446.300 429.000
10:1 10 1938 2.180 74.943 4.585
10:2 10 1942 1.960 76.713 4.135
10:3 10 1946 1.427 64.863 3.382
10:4 10 1950 4.275 68.315 6.352
10:5 10 1954 5.580 69.772 11.253
```
Turning observation-marker strings into a series

_Problem:_ Here’s one that might turn up in the context of the join command (see chapter 7).
The current dataset contains a string-valued series that you’d like to use as a key for matching
observations, perhaps the two-letter codes for the names of US states. The file from which you wish
to add data contains that same information, but _not_ in the form of a string-valued series, rather it
exists in the form of “observation markers”. Such markers cannot be used as a key directly, but is
there a way to parlay them into a string-valued series? Why, of course there is!

_Solution:_ We’ll illustrate with the Ramanathan data file data4-10.gdt, which contains private
school enrollment data and covariates for the 50 US states plus Washington, D.C. ( _n_ = 51).

```
open data4-10.gdt
markers --to-array="state_codes"
genr index
stringify(index, state_codes)
store joindata.gdt
```
_Comment:_ The markers command saves the observation markers to an array of strings. The com-
mand genr index creates a series that goes 1, 2, 3,... , and we attach the state codes to this series
via stringify(). After saving the result we have a datafile that contains a series, index, that can
be matched with whatever series holds the state code strings in the target dataset.

Suppose the relevant string-valued key series in the target dataset is called state. We might prefer
to avoid the need to specify a distinct “outer” key (again see chapter 7). In that case, in place of

```
genr index
stringify(index, state_codes)
```
we could do

```
genr index
series state = index
stringify(state, state_codes)
```

Chapter 21. Cheat sheet 195

and the two datafiles will contain a comparable string-valued state series.

### 21.2 Creating/modifying variables

Generating a dummy variable for a specific observation

_Problem:_ Generate _dt_ = 0 for all observations but one, for which _dt_ = 1.

_Solution:_

```
series d = (t=="1984:2")
```
_Comment:_ The internal variable t is used to refer to observations in string form, so if you have
a cross-section sample you may just use d = (t=="123"). If the dataset has observation labels
you can use the corresponding label, in which case it’s more idiomatic to use obs rather than t.
For example, if you open the dataset mrw.gdt, supplied with gretl among the examples, a dummy
variable for Italy could be generated via

```
series DIta = (obs=="Italy")
```
Note that this method does not require scripting. You can use the GUI menu itrm “Add/Define new
variable” for the same purpose, with the same syntax.

Generating a discrete variable out of a set of dummies

_Problem:_ The dummify function (also available as a command) generates a set of mutually exclusive
dummies from a discrete variable. The reverse functionality, however, seems to be absent.

_Solution:_

```
series x = lincomb(D, seq(1, nelem(D)))
```
_Comment:_ Suppose you have a list D of mutually exclusive dummies, that is a full set of 0/1 vari-
ables coding for the value of some characteristic, such that the sum of the values of the elements
of D is 1 at each observation. This is, by the way, exactly what the dummify command produces.
The reverse job of dummify can be performed neatly by using the lincomb function.

The code above multiplies the first dummy variable in the list D by 1, the second one by 2, and so
on. Hence, the return value is a series whose value is _i_ if and only if the _i_ -th member of D has value
1.

If you want your coding to start from 0 instead of 1, you’ll have to modify the code snippet above
into

```
series x = lincomb(D, seq(0, nelem(D)-1))
```
Easter

_Problem:_ I have a 7-day daily dataset. How do I create an “Easter” dummy?

_Solution:_ We have the easterday() function, which returns the month and day of Easter (in the
form of a single scalar that must be unpacked) given the year. The following example script uses
this function and a few string magic tricks. It assumes a 7-day dataset that spans at least 2011 to
2016.

```
series Easter = 0
loop y=2011..2016
a = easterday(y)
```

Chapter 21. Cheat sheet 196

```
m = floor(a)
d = round(100*(a-m))
ed_str = sprintf("%04d-%02d-%02d", y, m, d)
Easter["@ed_str"] = 1
endloop
```
_Comment:_ The round() function is necessary for the “day” component because otherwise floating-
point problems may ensue. Try the year 2015, for example.

Recoding a variable

_Problem:_ You want to perform a 1-to-1 recode on a variable. For example, consider tennis points:
you may have a variable _x_ holding values 1 to 3 and you want to recode it to 15, 30, 40.

_Solution 1:_

```
series x = replace(x, 1, 15)
series x = replace(x, 2, 30)
series x = replace(x, 3, 40)
```
_Solution 2:_

```
matrix tennis = {15, 30, 40}
series x = replace(x, seq(1,3), tennis)
```
_Comment:_ There are many equivalent ways to achieve the same effect, but for simple cases such
as this, the replace function is simple and transparent. If you don’t mind using matrices, scripts
using replace can also be remarkably compact. Note that replace also performs _n_ -to-1 (“surjec-
tive”) replacements, such as

```
series x = replace{z, {2, 3, 5, 11, 22, 33}, 1)
```
which would turn all entries equal to 2, 3, 5, 11, 22 or 33 to 1 and leave the other ones unchanged.

Generating a “subset of values” dummy

_Problem:_ You have a dataset which contains a fine-grained coding for some qualitative variable
and you want to “collapse” this to a relatively small set of dummy variables. Examples: you have
place of work by US state and you want a small set of regional dummies; or you have detailed
occupational codes from a census dataset and you want a manageable number of occupational
category dummies.

Let’s call the source series src and one of the target dummies D1. And let’s say that the values of
src to be grouped under D1 are 2, 13, 14 and 25. We’ll consider three possible solutions:

_“Longhand” solution:_

```
series D1 = src==2 || src==13 || src==14 || src==25
```
_Comment:_ The above works fine if the number of distinct values in the source to be condensed into
each dummy variable is fairly small, but it becomes cumbersome if a single dummy must comprise
dozens of source values.

_Condensed solution:_

```
matrix sel = {2,13,14,25}
series D1 = contains(src, sel)
```

Chapter 21. Cheat sheet 197

_Comment:_ The subset of values to be grouped together can be written out as a matrix relatively
compactly.

Of course, whichever procedure you use, you have to repeat it for each of the dummy series you
want to create.

_Proper solution:_

The best solution, in terms of both computational efficiency and code clarity, would be using a
“conversion table” and the replace function, to produce a series on which the dummify command
can be used. For example, suppose we want to convert from a series called fips holding FIPS
codes^1 for the 50 US states plus the District of Columbia to a series holding codes for the four
standard US regions. We could create a 2× 51 matrix — call it srmap — with the 51 FIPS codes on
the first row and the corresponding region codes on the second, and then do

```
series region = replace(fips, srmap[1,], srmap[2,])
dummify region
```
_Comment:_ With this approach all the subset dummies are created in one go, using the naming
pattern Dregion_1 and so on. The minor price to pay is that the relatively large conversion table
srmap has to be constructed first.

Generating an ARMA(1,1)

_Problem:_ Generate _yt_ = 0_._ 9 _yt_ − 1 + _εt_ − 0_._ 5 _εt_ − 1 , with _εt_ ∼ _NIID(_ 0 _,_ 1 _)_.

_Recommended solution:_

```
alpha = 0.9
theta = -0.5
series y = filter(normal(), {1, theta}, alpha)
```
_“Bread and butter” solution:_

```
alpha = 0.9
theta = -0.5
series e = normal()
series y = 0
series y = alpha * y(-1) + e + theta * e(-1)
```
_Comment:_ The filter function is specifically designed for this purpose so in most cases you’ll
want to take advantage of its speed and flexibility. That said, in some cases you may want to
generate the series in a manner which is more transparent (maybe for teaching purposes).

In the second solution, the statement series y = 0 is necessary because the next statement eval-
uates y recursively, so y[1] must be set. Note that you must use the keyword series here instead
of writing genr y = 0 or simply y = 0, to ensure that y is a series and not a scalar.

Recoding a variable by classes

_Problem:_ You want to recode a variable by classes. For example, you have the age of a sample of
individuals ( _xi_ ) and you need to compute age classes ( _yi_ ) as

```
yi = 1 for xi< 18
yi = 2 for 18≤ xi< 65
yi = 3 for xi ≥ 65
```
_Solution:_

(^1) FIPS is the Federal Information Processing Standard: it assigns numeric codes from 1 to 56 to the US states and
outlying areas.


Chapter 21. Cheat sheet 198

```
series y = 1 + (x >= 18) + (x >= 65)
```
_Comment:_ True and false expressions are evaluated as 1 and 0 respectively, so they can be ma-
nipulated algebraically as any other number. The same result could also be achieved by using the
conditional assignment operator (see below), but in most cases it would probably lead to more
convoluted constructs.

Conditional assignment

_Problem:_ Generate _yt_ via the following rule:

```
yt =
```
#### (

```
xt for dt> a
zt for dt ≤ a
```
_Solution:_

```
series y = (d > a)? x : z
```
_Comment:_ There are several alternatives to the one presented above. One is a brute force solution
using loops. Another one, more efficient but still suboptimal, would be

```
series y = (d>a)*x + (d<=a)*z
```
However, the ternary conditional assignment operator is not only the most efficient way to accom-
plish what we want, it is also remarkably transparent to read when one gets used to it. Some readers
may find it helpful to note that the conditional assignment operator works exactly the same way as
the =IF() function in spreadsheets.

Generating a time index for panel datasets

_Comment:_ gretl has a $unit as well as a $time accessor. These special constructs as well as
variants such as genr time are aware of whether a dataset is a panel.

Sanitizing a list of regressors

_Problem:_ I noticed that built-in commands like ols automatically drop collinear variables and put
the constant first. How can I achieve the same result for an estimator I’m writing?

_Solution:_ No worry. The function below does just that

```
function list sanitize(list X)
list R = X - const
if nelem(R) < nelem(X)
R = const R
endif
return dropcoll(R)
end function
```
so for example the code below

```
nulldata 20
x = normal()
y = normal()
z = x + y # collinear
list A = x y const z
list B = sanitize(A)
```
```
list print A
list print B
```

Chapter 21. Cheat sheet 199

returns

```
? list print A
x y const z
? list print B
const x y
```
Aside: it has been brought to our attention that some mischievous programs out there put the
constant _last_ , instead of first, like God intended. We are not amused by this utter disrespect of
econometric tradition, but if you want to pursue the way of evil, it is rather simple to adapt the
script above to that effect.

Generating the “hat” values after an OLS regression

_Problem:_ I’ve just run an OLS regression, and now I need the so-called the leverage values (also
known as the “hat” values). I know you can access residuals and fitted values through “dollar”
accessors, but nothing like that seems to be available for “hat” values.

_Solution:_ “Hat” values are can be thought of as the diagonal of the projection matrix _PX_ , or more
explicitly as
_hi_ = x′ _i(X_ ′ _X)_ −^1 x _i_

where _X_ is the matrix of regressors and x′ _i_ is its _i_ -th row.

The reader is invited to study the code below, which offers four different solutions to the problem:

```
open data4-1.gdt --quiet
list X = const sqft bedrms baths
ols price X
```
```
# method 1
leverage --save --quiet
series h1 = lever
```
```
# these are necessary for what comes next
matrix mX = {X}
matrix iXX = invpd(mX’mX)
```
```
# method 2
series h2 = diag(qform(mX, iXX))
# method 3
series h3 = sumr(mX .* (mX*iXX))
# method 4
series h4 = NA
loop i=1..$nobs
matrix x = mX[i,]’
h4[i] = x’iXX*x
endloop
```
```
# verify
print h1 h2 h3 h4 --byobs
```
_Comment:_ Solution 1 is the preferable one: it relies on the built-in leverage command, which
computes the requested series quite efficiently, taking care of missing values, possible restrictions
to the sample, etc.

However, three more are shown for didactical purposes, mainly to show the user how to manipulate
matrices. Solution 2 first constructs the _PX_ matrix explicitly, via the qform function, and then takes
its diagonal; this is definitely _not_ recommended (despite its compactness), since you generate a


Chapter 21. Cheat sheet 200

much bigger matrix than you actually need and waste a lot of memory and CPU cycles in the
process. It doesn’t matter very much in the present case, since the sample size is very small, but
with a big dataset this could be a very bad idea.

Solution 3 is more clever, and relies on the fact that, if you define _Z_ = _X_ · _(X_ ′ _X)_ −^1 , then _hi_ could
also be written as

```
hi = x′ i z i =
```
```
X k
```
```
i = 1
```
```
xikzik
```
which is in turn equivalent to the sum of the elements of the _i_ -th row of _X_ ⊙ _Z_ , where ⊙ is the
element-by-element product. In this case, your clever usage of matrix algebra would produce a
solution computationally much superior to solution 2.

Solution 4 is the most old-fashioned one, and employs an indexed loop. While this wastes practi-
cally no memory and employs no more CPU cycles in algebraic operations than strictly necessary,
it imposes a much greater burden on the hansl interpreter, since handling a loop is conceptually
more complex than a single operation. In practice, you’ll find that for any realistically-sized prob-
lem, solution 4 is much slower that solution 3.

Moving functions for time series

_Problem:_ gretl provides native functions for moving averages, but I need a to compute a different
statistic on a sliding data window. Is there a way to do this without using loops?

_Solution:_ One of the nice things of the list data type is that, if you define a list, then several
functions that would normally apply “vertically” to elements of a series apply “horizontally” across
the list. So for example, the following piece of code

```
open bjg.gdt
order = 12
list L = lg || lags(order-1, lg)
smpl +order ;
series movmin = min(L)
series movmax = max(L)
series movmed = median(L)
smpl full
```
computes the moving minimum, maximum and median of the lg series. Plotting the four series
would produce something similar to figure 21.1.

Generating data with a prescribed correlation structure

_Problem:_ I’d like to generate a bunch of normal random variates whose covariance matrix is exactly
equal to a given matrix Σ. How can I do this in gretl?

_Solution:_ The Cholesky decomposition is your friend. If you want to generate data with a given
_population_ covariance matrix, then all you have to do is post-multiply your pseudo-random data by
the Cholesky factor (transposed) of the matrix you want. For example:

```
set seed 123
S = {2,1;1,1}
T = 1000
X = mnormal(T, rows(S))
X = X * cholesky(S)’
eval mcov(X)
```
should give you


Chapter 21. Cheat sheet 201

```
4.6
```
```
4.8
```
```
5
```
```
5.2
```
```
5.4
```
```
5.6
```
```
5.8
```
```
6
```
```
6.2
```
```
6.4
```
```
6.6
```
```
1950 1952 1954 1956 1958 1960
```
```
lg
movmin
movmed
movmax
```
```
Figure 21.1: “Moving” functions
```
```
? eval mcov(X)
2.0016 1.0157
1.0157 1.0306
```
If, instead, you want your simulated data to have a given _sample_ covariance matrix, you have to
apply the same technique twice: one for standardizing the data, another one for giving it the
covariance structure you want. Example:

```
S = {2,1;1,1}
T = 1000
X = mnormal(T, rows(S))
X = X * (cholesky(S)/cholesky(mcov(X)))’
eval mcov(X)
```
gives you

```
? eval mcov(X)
2 1
1 1
```
as required.

### 21.3 Neat tricks

Interaction dummies

_Problem:_ You want to estimate the model _yi_ = x _iβ_ 1 + z _iβ_ 2 + _diβ_ 3 + _(di_ · z _i)β_ 4 + _εt_ , where _di_ is a
dummy variable while x _i_ and z _i_ are vectors of explanatory variables.

_Solution:_ Gretl provides the ^ operator to make this operation easy, which essentially boils down
to creating a new list with d ^ z and adding that to the regressors. See section 15.1 for details
(especially Listing 15.1). This method avoids an explicit loop construct in which products of the
series would be formed.


Chapter 21. Cheat sheet 202

Realized volatility

_Problem:_ Given data by the minute, you want to compute the “realized volatility” for the hour as
_RVt_ = 601

#### P 60

```
τ = 1 y
```
```
2
t : τ. Imagine your sample starts at time 1:1.
```
_Solution:_

```
nulldata 720
setobs 60 1:1 --time-series # 60 minutes per hour
```
```
# artificial data by the minute
series x = normal()
```
```
# calculate variance using the 60 obs within each hour
matrix v = aggregate(x, $obsmajor, var) # $obsmajor means hour here
```
```
# go from minute data to lower hourly periodicity
dataset compact 1
series rv = v[,end] # final column of v holds the variance results
```
_Comment:_ Here we require that the dataset by the minute is explicitly defined with the special time-
series periodicity of 60, so that it can be compacted to hourly data by using the dataset compact
1 command. If needed, the dataset’s new periodicity can be re-set to 24 afterwards with the setobs
command, which is the usual property of hourly data.

Looping over two paired lists

_Problem:_ Suppose you have two lists with the same number of elements, and you want to apply
some command to corresponding elements over a loop. For example you want to regress each
element of one list on the corresponding element of the other.

_Solution:_

```
list Y = y1 y2 y3
list X = x1 x2 x3
loop i=1..nelem(Y)
ols Y[i] 0 X[i]
endloop
```
Convolution / polynomial multiplication

_Problem:_ How do I multiply polynomials? There’s no dedicated function to do that, and yet it’s a
fairly basic mathematical task.

_Solution:_ Never fear! We have the conv2d function, which is a tool for a more general problem, but
includes polynomial multiplication as a special case..

Suppose you want to multiply two finite-order polynomials _P(x)_ =

```
P m
i = 0 pix
i and Q(x) =P n
i = 0 qix
i.
```
What you want is the sequence of coefficients of the polynomial

```
R(x) = P(x) · Q(x) =
```
```
m X+ n
```
```
k = 0
```
```
rkxk
```
where

```
rk =
```
```
X k
```
```
i = 0
```
```
piqk − i
```
is the _convolution_ of the _pi_ and _qi_ coefficients. The same operation can be performed via the FFT,
but in most cases using conv2d is quicker and more natural.


Chapter 21. Cheat sheet 203

As an example, we’ll use the same one we used in Section 30.5: consider the multiplication of two
polynomials:

```
P(x) = 1 + 0. 5 x
Q(x) = 1 + 0. 3 x − 0. 8 x^2
R(x) = P(x) · Q(x) = 1 + 0. 8 x − 0. 65 x^2 − 0. 4 x^3
```
The following code snippet performs all the necessary calculations:

```
p = {1; 0.5}
q = {1; 0.3; -0.8}
r = conv2d(p, q)
print r
```
Runnning the above produces

```
r (4 x 1)
```
```
1
0.8
-0.65
-0.4
```
which is indeed the desired result. Note that the same computation could also be performed via
the filter function, at the price of slightly more elaborate syntax.

Comparing two lists

_Problem:_ How can I tell if two lists contain the same variables (not necessarily in the same order)?

_Solution:_ In many respects, lists are like sets, so it makes sense to use the so-called “symmetric
difference” operator, which is defined as

```
A △ B = (A \ B) ∪ (B \ A)
```
where in this context backslash represents the relative complement operator, which gives the ele-
ments of set _A_ than are not in set _B_ :

```
A \ B ={ x ∈ A : x ̸∈ B }
```
So we first check if there are any series in _A_ but not in _B_ , then we perform the reverse check. If the
union of the two results is an empty set, then the lists must contain the same variables. The hansl
syntax for this would be something like

```
scalar NotTheSame = nelem((A-B) || (B-A)) > 0
```
Reordering list elements

_Problem:_ Is there a way to reorder list elements?

_Solution:_ You can use the fact that a list can be cast into a vector of integers and then manipulated
via ordinary matrix syntax. So, for example, if you wanted to “flip” a list you may just use the
mreverse function. For example:

```
open AWM.gdt --quiet
list X = 3 6 9 12
matrix tmp = X
list revX = mreverse(tmp’)
```
```
list X print
list revX print
```

Chapter 21. Cheat sheet 204

will produce

```
? list X print
D1 D872 EEN_DIS GCD
? list revX print
GCD EEN_DIS D872 D1
```
Plotting an asymmetric confidence interval

_Problem:_ “I like the look of the --band option to the gnuplot and plot commands, but it’s set up
for plotting a symmetric interval and I want to show an asymmetric one.”

_Solution:_ Any interval is by construction symmetrical about its mean at each observation. So you
just need to perform a little tweak. Say you want to plot a series x along with a band defined by the
two series top and bot. Here we go:

```
# create series for mid-point and deviation
series mid = (top + bot)/2
series dev = top - mid
gnuplot x --band=mid,dev --time-series --with-lines --output=display
```
Cross-validation

_Problem:_ “I’d like to compute the so-called _leave-one-out cross-validation criterion_ for my regression.
Is there a command in gretl?”

If you have a sample with _n_ observations, the “leave-one-out” cross-validation criterion can be
mechanically computed by running _n_ regressions in which one observation at a time is omitted
and all the other ones are used to forecast its value. The sum of the _n_ squared forecast errors is
the statistic we want. Fortunately, there is no need to do so. It is possible to prove that the same
statistic can be computed as

```
CV =
```
```
X n
```
```
i = 1
```
```
[u ˆ i/( 1 − hi)]^2 ,
```
where _hi_ is the _i_ -th element of the “hat” matrix (see section 21.2) from a regression on the whole
sample.

This method is natively provided by gretl as a side benefit to the leverage command, that stores
the CV criterion into the $test accessor. The following script shows the equivalence of the two
approaches:

```
set verbose off
open data4-1.gdt
list X = const sqft bedrms baths
```
```
# compute the CV criterion the silly way
```
```
scalar CV = 0
matrix mX = {X}
loop i = 1 .. $nobs
xi = mX[i,]
yi = price[i]
smpl obs != i --restrict
ols price X --quiet
smpl full
scalar fe = yi - xi * $coeff
CV += fe^2
endloop
```

Chapter 21. Cheat sheet 205

```
printf "CV = %g\n", CV
```
```
# the smart way
```
```
ols price X --quiet
leverage --quiet
printf "CV = %g\n", $test
```
Is my matrix result broken?

_Problem:_ Most of the matrix manipulation functions available in gretl flag an error if something
goes wrong, but there’s no guarantee that every matrix computation will return an entirely finite
matrix, containing no infinities or NaNs. So how do I tell if I’ve got a fully valid matrix?

_Solution_ : The sum function applied to a matrix m returns the sum of all of its elements or NA if any
elements are non-finite. So “eval sum(m)” can be used as a check — or more explicitly,

```
if !ok(sum(m))
print "m is broken"
endif
```
Also note that the call “ok(m)” returns a matrix with the same dimensions as m, with elements 1
for finite values and 0 for infinities or NaNs.


## Part II

# Econometric methods

#### 206


## Chapter 22

Robust covariance matrix estimation

### 22.1 Introduction

Consider (once again) the linear regression model

```
y = Xβ + u (22.1)
```
where _y_ and _u_ are _T_ -vectors, _X_ is a _T_ × _k_ matrix of regressors, and _β_ is a _k_ -vector of parameters.
As is well known, the estimator of _β_ given by Ordinary Least Squares (OLS) is

```
β ˆ= (X ′ X) −^1 X ′ y (22.2)
```
If the condition _E(u_ | _X)_ = 0 is satisfied, this is an unbiased estimator; under somewhat weaker
conditions the estimator is biased but consistent. It is straightforward to show that when the OLS
estimator is unbiased (that is, when _E(β_ ˆ− _β)_ = 0), its variance is

```
Var (β) ˆ= E
```
#### 

```
(β ˆ− β)(β ˆ− β) ′
```
#### 

#### = (X ′ X) −^1 X ′Ω X(X ′ X) −^1 (22.3)

where Ω= _E(uu_ ′ _)_ is the covariance matrix of the error terms.

Under the assumption that the error terms are independently and identically distributed (iid) we
can write Ω= _σ_^2 _I_ , where _σ_^2 is the (common) variance of the errors (and the covariances are zero).
In that case (22.3) simplifies to the “classical” formula,

```
Var (β) ˆ= σ^2 (X ′ X) −^1 (22.4)
```
If the iid assumption is not satisfied, two things follow. First, it is possible in principle to construct
a more efficient estimator than OLS — for instance some sort of Feasible Generalized Least Squares
(FGLS). Second, the simple “classical” formula for the variance of the least squares estimator is no
longer correct, and hence the conventional OLS standard errors — which are just the square roots
of the diagonal elements of the matrix defined by (22.4) — do not provide valid means of statistical
inference.

In the recent history of econometrics there are broadly two approaches to the problem of non-
iid errors. The “traditional” approach is to use an FGLS estimator. For example, if the departure
from the iid condition takes the form of time-series dependence, and if one believes that this
could be modeled as a case of first-order autocorrelation, one might employ an AR(1) estimation
method such as Cochrane–Orcutt, Hildreth–Lu, or Prais–Winsten. If the problem is that the error
variance is non-constant across observations, one might estimate the variance as a function of the
independent variables and then perform weighted least squares, using as weights the reciprocals
of the estimated variances.

While these methods are still in use, an alternative approach has found increasing favor: that is,
use OLS but compute standard errors (or more generally, covariance matrices) that are robust with
respect to deviations from the iid assumption. This is typically combined with an emphasis on
using large datasets — large enough that the researcher can place some reliance on the (asymptotic)
consistency property of OLS. This approach has been enabled by the availability of cheap computing
power. The computation of robust standard errors and the handling of very large datasets were
daunting tasks at one time, but now they are unproblematic. The other point favoring the newer
methodology is that while FGLS offers an efficiency advantage in principle, it often involves making

#### 207


Chapter 22. Robust covariance matrix estimation 208

additional statistical assumptions which may or may not be justified, which may not be easy to test
rigorously, and which may threaten the consistency of the estimator — for example, the “common
factor restriction” that is implied by traditional FGLS “corrections” for autocorrelated errors.

James Stock and Mark Watson’s _Introduction to Econometrics_ illustrates this approach at the level of
undergraduate instruction: many of the datasets they use comprise thousands or tens of thousands
of observations; FGLS is downplayed; and robust standard errors are reported as a matter of course.
In fact, the discussion of the classical standard errors (labeled “homoskedasticity-only”) is confined
to an Appendix.

Against this background it may be useful to set out and discuss all the various options offered
by gretl in respect of robust covariance matrix estimation. The first point to notice is that gretl
produces “classical” standard errors by default (in all cases apart from GMM estimation). In script
mode you can get robust standard errors by appending the --robust flag to estimation commands.
In the GUI program the model specification dialog usually contains a “Robust standard errors”
check box, along with a “configure” button that is activated when the box is checked. The configure
button takes you to a configuration dialog (which can also be reached from the main menu bar:
Tools → Preferences → General → HCCME). There you can select from a set of possible robust
estimation variants, and can also choose to make robust estimation the default.

The specifics of the available options depend on the nature of the data under consideration —
cross-sectional, time series or panel — and also to some extent the choice of estimator. (Although
we introduced robust standard errors in the context of OLS above, they may be used in conjunction
with other estimators too.) The following three sections of this chapter deal with matters that are
specific to the three sorts of data just mentioned. Note that additional details regarding covariance
matrix estimation in the context of GMM are given in chapter 27.

We close this introduction with a brief statement of what “robust standard errors” can and cannot
achieve. They can provide for asymptotically valid statistical inference in models that are basically
correctly specified, but in which the errors are not iid. The “asymptotic” part means that they
may be of little use in small samples. The “correct specification” part means that they are not a
magic bullet: if the error term is correlated with the regressors, so that the parameter estimates
themselves are biased and inconsistent, robust standard errors will not save the day.

### 22.2 Cross-sectional data and the HCCME

With cross-sectional data, the most likely departure from iid errors is heteroskedasticity (non-
constant variance).^1 In some cases one may be able to arrive at a judgment regarding the likely
form of the heteroskedasticity, and hence to apply a specific correction. The more common case,
however, is where the heteroskedasticity is of unknown form. We seek an estimator of the covari-
ance matrix of the parameter estimates that retains its validity, at least asymptotically, in face of
unspecified heteroskedasticity. It is not obvious _a priori_ that this should be possible, but White
(1980) showed that
Vardh _(β)_ ˆ= _(X_ ′ _X)_ −^1 _X_ ′Ωˆ _X(X_ ′ _X)_ −^1 (22.5)

does the trick. (As usual in statistics we need to say “under certain conditions”, but the conditions
are not very restrictive.)Ωˆ is in this context a diagonal matrix, whose non-zero elements may be
estimated using squared OLS residuals. White referred to (22.5) as a heteroskedasticity-consistent
covariance matrix estimator (HCCME).

Davidson and MacKinnon (2004, chapter 5) offer a useful discussion of several variants on White’s
HCCME theme. They refer to the original variant of (22.5) — in which the diagonal elements ofΩˆ
are estimated directly by the squared OLS residuals, _u_ ˆ^2 _t_ — as HC 0. (The associated standard errors
are often called “White’s standard errors”.) The various refinements of White’s proposal share a
common point of departure, namely the idea that the squared OLS residuals are likely to be “too

(^1) In some specialized contexts spatial autocorrelation may be an issue. Gretl does not have any built-in methods to
handle this and we will not discuss it here.


Chapter 22. Robust covariance matrix estimation 209

small” on average. This point is quite intuitive. The OLS parameter estimates, _β_ ˆ, satisfy by design
the criterion that the sum of squared residuals,

```
X
u ˆ^2 t =
```
#### X

```
yt − Xtβ ˆ
```
####  2

is minimized for given _X_ and _y_. Suppose that _β_ ˆ≠ _β_. This is almost certain to be the case: even if
OLS is not biased it would be a miracle if the _β_ ˆ calculated from any finite sample were exactly equal
to _β_. But in that case the sum of squares of the true, unobserved _errors_ ,

#### P

```
u^2 t =
```
#### P

_(yt_ − _Xtβ)_^2 is
bound to be greater than

#### P

```
u ˆ^2 t. The elaborated variants on HC 0 take this point on board as follows:
```
- HC 1 : Applies a degrees-of-freedom correction, multiplying the HC 0 matrix by _T/(T_ − _k)_.
- HC 2 : Instead of using _u_ ˆ^2 _t_ for the diagonal elements ofΩˆ, uses _u_ ˆ^2 _t/(_ 1 − _ht)_ , where _ht_ =
    _Xt(X_ ′ _X)_ −^1 _Xt_ ′, the _t_ thdiagonal element of the projection matrix _PX_ , which has the property
    that _PX_ · _y_ = _y_ ˆ. The relevance of _ht_ is that if the variance of all the _ut_ is _σ_^2 , the expectation
    of _u_ ˆ^2 _t_ is _σ_^2 _(_ 1 − _ht)_ , or in other words, the ratio _u_ ˆ^2 _t/(_ 1 − _ht)_ has expectation _σ_^2. As Davidson
    and MacKinnon show, 0 ≤ _ht<_ 1 for all _t_ , so this adjustment cannot reduce the the diagonal
    elements ofΩˆ and in general revises them upward.
- HC 3 : Uses _u_ ˆ^2 _t/(_ 1 − _ht)_^2. The additional factor of _(_ 1 − _ht)_ in the denominator, relative to
    HC 2 , may be justified on the grounds that observations with large variances tend to exert a
    lot of influence on the OLS estimates, so that the corresponding residuals tend to be under-
    estimated. See Davidson and MacKinnon for a fuller explanation.
- HC 3 _a_ : Implements the jackknife approach from MacKinnon and White (1985). (HC 3 is a close
    approximation of this.)

The relative merits of these variants have been explored by means of both simulations and the-
oretical analysis. Unfortunately there is not a clear consensus on which is “best”. Davidson and
MacKinnon argue that the original HC 0 is likely to perform worse than the others and in gretl the
default is HC 1. If you want comparability with other software that reports “White’s standard errors”
you can choose HC 0.

If you wish to use a version other than HC 1 you can arrange for this in either of two ways. In script
or console mode you can do, for example,

```
set hc_version 2
```
and the version you specify will be applied in the current gretl session. In the GUI program you can
go to the HCCME configuration dialog, as noted above, and choose any of these variants to be the
default: a choice made in this way persists across gretl sessions.

### 22.3 Time series data and HAC covariance matrices

Heteroskedasticity may be an issue with time series data too but it is unlikely to be the only, or
even the primary, concern.

One form of heteroskedasticity is common in macroeconomic time series but is fairly easily dealt
with. That is, in the case of strongly trending series such as Gross Domestic Product, aggregate
consumption, aggregate investment, and so on, higher levels of the variable in question are likely
to be associated with higher variability in absolute terms. The obvious “fix”, employed in many
macroeconometric studies, is to use the logs of such series rather than the raw levels. Provided the
_proportional_ variability of such series remains roughly constant over time the log transformation
is effective.

Other forms of heteroskedasticity may resist the log transformation, but may demand a special
treatment distinct from the calculation of robust standard errors. We have in mind here _autore-
gressive conditional_ heteroskedasticity, for example in the behavior of asset prices, where large


Chapter 22. Robust covariance matrix estimation 210

disturbances to the market may usher in periods of increased volatility. Such phenomena call for
specific estimation strategies, such as GARCH (see chapter 31).

Despite the points made above, some residual degree of heteroskedasticity may be present in time
series data: the key point is that in most cases it is likely to be combined with serial correlation
(autocorrelation), hence demanding a special treatment. In White’s approach,Ωˆ, the estimated
covariance matrix of the _ut_ , remains conveniently diagonal: the variances, _E(u_^2 _t)_ , may differ by
_t_ but the covariances, _E(utus)_ for _s_ ≠ _t_ , are all zero. Autocorrelation in time series data means
that at least some of the the off-diagonal elements ofΩˆ should be non-zero. This introduces a
substantial complication and requires another piece of terminology: estimates of the covariance
matrix that are asymptotically valid in face of both heteroskedasticity and autocorrelation of the
error process are termed HAC (heteroskedasticity- and autocorrelation-consistent).

The issue of HAC estimation is treated in more technical terms in chapter 27. Here we try to
convey some of the intuition at a more basic level. We begin with a general comment: residual
autocorrelation is not so much a property of the data as a symptom of an inadequate model. Data
may be persistent though time, and if we fit a model that does not take this aspect into account
properly we end up with a model with autocorrelated disturbances. Conversely, it is often possible
to mitigate or even eliminate the problem of autocorrelation by including relevant lagged variables
in a time series model, or in other words, by specifying the dynamics of the model more fully. HAC
estimation should not be seen as the first resort in dealing with an autocorrelated error process.

That said, the “obvious” extension of White’s HCCME to the case of autocorrelated errors would
seem to be this: estimate the off-diagonal elements ofΩˆ (that is, the autocovariances, _E(utus)_ )
using, once again, the appropriate OLS residuals: _ω_ ˆ _ts_ = _u_ ˆ _tu_ ˆ _s_. This is basically right, but demands
an important amendment. We seek a _consistent_ estimator, one that converges towards the true Ω as
the sample size tends towards infinity. This can’t work if we allow unbounded serial dependence.
A larger sample will enable us to estimate more of the true _ωts_ elements (that is, for _t_ and _s_
more widely separated in time) but will not contribute ever-increasing information regarding the
maximally separated _ωts_ pairs since the maximal separation itself grows with the sample size.
To ensure consistency we have to confine our attention to processes exhibiting temporally limited
dependence. In other words we cut off the computation of the _ω_ ˆ _ts_ values at some maximum value
of _p_ = _t_ − _s_ , where _p_ is treated as an increasing function of the sample size, _T_ , although it cannot
increase in proportion to _T_.

The simplest variant of this idea is to truncate the computation at some finite lag order _p_ , where
_p_ grows as, say, _T_^1 _/_^4. The trouble with this is that the resultingΩˆ may not be a positive definite
matrix. In practical terms, we may end up with negative estimated variances. One solution to this
problem is offered by The Newey–West estimator (Newey and West, 1987), which assigns declining
weights to the sample autocovariances as the temporal separation increases.

To understand this point it is helpful to look more closely at the covariance matrix given in (22.5),
namely,
_(X_ ′ _X)_ −^1 _(X_ ′Ωˆ _X)(X_ ′ _X)_ −^1

This is known as a “sandwich” estimator. The bread, which appears on both sides, is _(X_ ′ _X)_ −^1. This
_k_ × _k_ matrix is also the key ingredient in the computation of the classical covariance matrix. The
filling in the sandwich is
Σˆ = _X_ ′ Ωˆ _X
(k_ × _k) (k_ × _T) (T_ × _T) (T_ × _k)_

It can be proven that under mild regularity conditions _T_ −^1 ˆΣ is a consistent estimator of the long-run
covariance matrix of the random _k_ -vector _xt_ · _ut_.

From a computational point of view it is neither necessary nor desirable to store the (potentially
very large) _T_ × _T_ matrixΩˆ as such. Rather, one computes the sandwich filling by summation as a
weighted sum:

```
ˆΣ=ˆΓ ( 0 ) +
```
```
X p
```
```
j = 1
```
```
wj
```
#### 

```
ˆΓ (j) +ˆΓ′ (j)
```
#### 


Chapter 22. Robust covariance matrix estimation 211

where _wj_ is the weight given to lag _j >_ 0 and the _k_ × _k_ matrixˆΓ _(j)_ , for _j_ ≥ 0, is given by

```
ˆΓ (j) =
```
#### X T

```
t = j + 1
```
```
u ˆ tu ˆ t − jXt ′ Xt − j ;
```
that is, the sample autocovariance matrix of _xt_ · _ut_ at lag _j_ , apart from a scaling factor _T_.

This leaves two questions. How exactly do we determine the maximum lag length or “bandwidth”,
_p_ , of the HAC estimator? And how exactly are the weights _wj_ to be determined? We will return to
the (difficult) question of the bandwidth shortly. As regards the weights, gretl offers three variants.
The default is the Bartlett kernel, as used by Newey and West. This sets

```
wj =
```
#### 

#### 

#### 

```
1 − pj + 1 j ≤ p
0 j > p
```
so the weights decline linearly as _j_ increases. The other two options are the Parzen kernel and the
Quadratic Spectral (QS) kernel. For the Parzen kernel,

```
wj =
```
#### 

#### 

#### 

```
1 − 6 a^2 j + 6 a^3 j 0 ≤ aj ≤ 0. 5
2 ( 1 − aj)^30. 5 < aj ≤ 1
0 aj> 1
```
where _aj_ = _j/(p_ + 1 _)_ , and for the QS kernel,

```
wj =
```
#### 25

```
12 π^2 d^2 j
```
```
sin mj
mj
```
```
− cos mj
```
#### !

where _dj_ = _j/p_ and _mj_ = 6 _πdj/_ 5.

Figure 22.1 shows the weights generated by these kernels, for _p_ = 4 and _j_ = 1 to 9.

```
Figure 22.1: Three HAC kernels
```
```
Bartlett Parzen QS
```
In gretl you select the kernel using the set command with the hac_kernel parameter:

```
set hac_kernel parzen
set hac_kernel qs
set hac_kernel bartlett
```
Selecting the HAC bandwidth

The asymptotic theory developed by Newey, West and others tells us in general terms how the
HAC bandwidth, _p_ , should grow with the sample size, _T_ — that is, _p_ should grow in proportion
to some fractional power of _T_. Unfortunately this is of little help to the applied econometrician,
working with a given dataset of fixed size. Various rules of thumb have been suggested and gretl
implements two such. The default is _p_ = 0_._ 75 _T_^1 _/_^3 , as recommended by Stock and Watson (2003).
An alternative is _p_ = 4 _(T/_ 100 _)_^2 _/_^9 , as in Wooldridge (2002b). In each case one takes the integer
part of the result. These variants are labeled nw1 and nw2 respectively, in the context of the set
command with the hac_lag parameter. That is, you can switch to the version given by Wooldridge
with


Chapter 22. Robust covariance matrix estimation 212

```
set hac_lag nw2
```
As shown in Table 22.1 the choice between nw1 and nw2 does not make a great deal of difference.

```
T p (nw1) p (nw2)
```
```
50 2 3
100 3 4
150 3 4
200 4 4
300 5 5
400 5 5
```
```
Table 22.1: HAC bandwidth: two rules of thumb
```
You also have the option of specifying a fixed numerical value for _p_ , as in

```
set hac_lag 6
```
In addition you can set a distinct bandwidth for use with the Quadratic Spectral kernel (since this
need not be an integer). For example,

```
set qs_bandwidth 3.5
```
Prewhitening and data-based bandwidth selection

An alternative approach is to deal with residual autocorrelation by attacking the problem from two
sides. The intuition behind the technique known as _VAR prewhitening_ (Andrews and Monahan,
1992) can be illustrated by a simple example. Let _xt_ be a sequence of first-order autocorrelated
random variables
_xt_ = _ρxt_ − 1 + _ut_

The long-run variance of _xt_ can be shown to be

```
VLR(xt) =
```
```
VLR(ut)
( 1 − ρ)^2
```
In most cases _ut_ is likely to be less autocorrelated than _xt_ , so a smaller bandwidth should suffice.
Estimation of _VLR(xt)_ can therefore proceed in three steps: (1) estimate _ρ_ ; (2) obtain a HAC estimate
of _u_ ˆ _t_ = _xt_ − _ρx_ ˆ _t_ − 1 ; and (3) divide the result by _(_ 1 − _ρ)_^2.

The application of the above concept to our problem implies estimating a finite-order Vector Au-
toregression (VAR) on the vector variables _ξt_ = _Xtu_ ˆ _t_. In general the VAR can be of any order, but
in most cases 1 is sufficient; the aim is not to build a watertight model for _ξt_ , but just to “mop up”
a substantial part of the autocorrelation. Hence, the following VAR is estimated

```
ξt = Aξt − 1 + εt
```
Then an estimate of the matrix _X_ ′Ω _X_ can be recovered via

```
(I − A) ˆ−^1 ˆΣ ε(I − A ˆ′ ) −^1
```
whereˆΣ _ε_ is any HAC estimator, applied to the VAR residuals.

You can ask for prewhitening in gretl using

```
set hac_prewhiten on
```

Chapter 22. Robust covariance matrix estimation 213

There is at present no mechanism for specifying an order other than 1 for the initial VAR.

A further refinement is available in this context, namely data-based bandwidth selection. It makes
intuitive sense that the HAC bandwidth should not simply be based on the size of the sample,
but should somehow take into account the time-series properties of the data (and also the kernel
chosen). A nonparametric method for doing this was proposed by Newey and West (1994); a good
concise account of the method is given in Hall (2005). This option can be invoked in gretl via

```
set hac_lag nw3
```
This option is the default when prewhitening is selected, but you can override it by giving a specific
numerical value for hac_lag.

Even the Newey–West data-based method does not fully pin down the bandwidth for any particular
sample. The first step involves calculating a series of residual covariances. The length of this series
is given as a function of the sample size, but only up to a scalar multiple — for example, it is given
as _O(T_^2 _/_^9 _)_ for the Bartlett kernel. Gretl uses an implied multiple of 1.

Newey–West with missing values

If the estimation sample for a time-series model includes incomplete observations — where the
value of the dependent variable or one more regressors is missing — the Newey–West procedure
must be either modified or abandoned, since some ingredients of theΣˆ matrix defined above will
be absent. Two modified methods have been discussed in the literature. Parzen (1963) proposed
what he called Amplitude Modulation (AM), which involves setting the values of the residual and
each of the regressors to zero for the incomplete observations (and then proceeding as usual).
Datta and Du (2012) propose the so-called Equal Spacing (ES) method: calculate as if the incomplete
observations did not exist, and the complete observations therefore form an equally-spaced series.
Somewhat suprisingly, it can be shown that both of these methods have appropriate asymptotic
properties; see Rho and Vogelsang (2018) for further elaboration.

In gretl you can select a preferred method via one or other of these commands:

```
set hac_missvals es # ES, Datta and Du
set hac_missvals am # AM, Parzen
set hac_missvals off
```
The ES method is the default. The off option means that gretl will refuse to produce HAC standard
errors when the sample includes incomplete observations: use this if you have qualms about the
modified methods.

VARs: a special case

A well-specified vector autoregression (VAR) will generally include enough lags of the dependent
variables to obviate the problem of residual autocorrelation, in which case HAC estimation is
redundant — although there may still be a need to correct for heteroskedasticity. For that rea-
son plain HCCME, and not HAC, is the default when the --robust flag is given in the context of the
var command. However, if for some reason you need HAC you can force the issue by giving the
option --robust-hac.

Long-run variance

Let us expand a little on the subject of the long-run variance that was mentioned above and the
associated tools offered by gretl for scripting. (You may also want to check out the reference for
the lrcovar function for the multivariate case.) As is well known, the variance of the average of _T_
random variables _x_ 1 _,x_ 2 _,...,xT_ with equal variance _σ_^2 equals _σ_^2 _/T_ if the data are uncorrelated. In
this case, the sample variance of _xt_ over the sample size provides a consistent estimator.


Chapter 22. Robust covariance matrix estimation 214

If, however, there is serial correlation among the _xt_ s, the variance of _X_ ̄ = _T_ −^1

#### P T

_t_ = 1 _xt_ must be
estimated differently. One of the most widely used statistics for this purpose is a nonparametric
kernel estimator with the Bartlett kernel defined as

```
ω ˆ^2 (k) = T −^1
```
```
T X− k
```
```
t = k
```
#### 

#### 

```
X k
```
```
i =− k
```
```
wi(xt − X)(x ̄ t − i − X) ̄
```
#### 

####  , (22.6)

where the integer _k_ is known as the window size and the _wi_ terms are the so-called _Bartlett weights_ ,
defined as _wi_ = 1 − _k_ |+ _i_ | 1. It can be shown that, for _k_ large enough, _ω_ ˆ^2 _(k)/T_ yields a consistent
estimator of the variance of _X_ ̄.

gretl implements this estimator by means of the function lrvar(). This function takes one re-
quired argument, namely the series whose long-run variance is to be estimated, followed by two
optional arguments. The first of these can be used to supply a value for _k_ ; if it is omitted or nega-
tive, the popular choice _T_^1 _/_^3 is used. The second allows specification of an assumed value for the
population mean of _X_ , which then replaces _X_ ̄ in the variance calculation. Usage is illustrated below.

```
# automatic window size; use xbar for mean
lrs2 = lrvar(x)
# set a window size of 12
lrs2 = lrvar(x, 12)
# set window size and impose assumed mean of zero
lrs2 = lrvar(x, 12, 0)
# impose mean zero, automatic window size
lrs2 = lrvar(x, -1, 0)
```
### 22.4 Special issues with panel data

Since panel data have both a time-series and a cross-sectional dimension one might expect that, in
general, robust estimation of the covariance matrix would require handling both heteroskedasticity
and autocorrelation (the HAC approach). In addition, some special features of panel data require
attention.

- The variance of the error term may differ across the cross-sectional units.
- The covariance of the errors across the units may be non-zero in each time period.
- If the “between” variation is not swept out, the errors may exhibit autocorrelation, not in the
    usual time-series sense but in the sense that the mean value of the error term may differ
    across units. This is relevant when estimation is by pooled OLS.

Gretl currently offers three panel-specific covariance matrix estimators in response to the --robust
option. These are available for models estimated via fixed effects, random effects, pooled OLS, and
pooled two-stage least squares. The default robust estimator is that suggested by Arellano (2003),
which is HAC provided the panel is of the “large _n_ , small _T_ ” variety (that is, many units are observed
in relatively few periods). The Arellano estimator involves clustering by the cross-sectional unit:

#### ˆΣA=

#### 

# Gretl Function Reference
See also the Gretl Command Reference

The following accessors and functions are documented below.


|$ahat     |$aic    |$allprobs|$bic     |$chisq   |$coeff   |$command |$compan  |
|----------|--------|---------|---------|---------|---------|---------|---------|
|$datatype |$depvar |$df      |$diagpval|$diagtest|$dotdir  |$dw      |$dwpval  |
|$ec       |$error  |$ess     |$evals   |$fcast   |$fcse    |$fevd    |$Fstat   |
|$gmmcrit  |$h      |$hausman |$hqc     |$huge    |$jalpha  |$jbeta   |$jvbeta  |
|$lang     |$llt    |$lnl     |$macheps |$mapfile |$mnlprobs|$model   |$mpirank |
|$mpisize  |$ncoeff |$nobs    |$now     |$nvars   |$obsdate |$obsmajor|$obsmicro|
|$obsminor |$panelpd|$parnames|$pd      |$pi      |$pkgdir  |$pvalue  |$qlrbreak|
|$result   |$rho    |$rsq     |$sample  |$sargan  |$seed    |$sigma   |$stderr  |
|$stopwatch|$sysA   |$sysB    |$sysGamma|$sysinfo |$system  |$T       |$t1      |
|$t2       |$test   |$time    |$tmax    |$trsq    |$uhat    |$unit    |$vcv     |
|$vecGamma |$version|$vma     |$windows |$workdir |$xlist   |$xtxinv  |$yhat    |
|$ylist    |        |         |         |         |         |         |         |





|abs      |acos      |acosh     |aggregate|argname  |array     |asin      |asinh    |
|---------|----------|----------|---------|---------|----------|----------|---------|
|asort    |assert    |atan      |atan2    |atanh    |atof      |bcheck    |bessel   |
|BFGSmax  |BFGSmin   |BFGScmax  |BFGScmin |bin2dec  |bincoeff  |binperms  |bkfilt   |
|bkw      |boxcox    |bread     |brename  |bwfilt   |bwrite    |carg      |cdemean  |
|cdf      |cdiv      |cdummify  |ceil     |cholesky |chowlin   |cmod      |cmult    |
|cnorm    |cnumber   |cnameget  |cnameset |cols     |commute   |complex   |conj     |
|contains |conv2d    |cquad     |corr     |corresp  |corrgm    |cos       |cosh     |
|cov      |critical  |cswitch   |ctrans   |cum      |curl      |dayspan   |dec2bin  |
|defarray |defbundle |deflist   |deseas   |det      |diag      |diagcat   |diff     |
|digamma  |distance  |dnorm     |dropcoll |dsort    |dummify   |easterday |ecdf     |
|eigen    |eigengen  |eigensym  |eigsolve |epochday |errmsg    |errorif   |exists   |
|exp      |fcstats   |fdjac     |feval    |fevalb   |fevd      |fft       |ffti     |
|filter   |firstobs  |fixname   |flatten  |floor    |fracdiff  |fzero     |gammafun |
|genseries|geoplot   |getenv    |getinfo  |getkeys  |getline   |ghk       |gini     |
|ginv     |GSSmax    |GSSmin    |halton   |hdprod   |hfdiff    |hfldiff   |hflags   |
|hflist   |hpfilt    |hyp2f1    |I        |Im       |imaxc     |imaxr     |imhof    |
|iminc    |iminr     |inbundle  |infnorm  |inlist   |instring  |instrings |int      |
|interpol |inv       |invcdf    |invmills |invpd    |irf       |irr       |iscomplex|
|isconst  |isdiscrete|isdummy   |isnan    |isoconv  |isocountry|isodate   |isoweek  |
|iwishart |jsonget   |jsongetb  |juldate  |kdensity |kdsmooth  |kfilter   |kmeier   |
|kpsscrit |ksetup    |ksimul    |ksmooth  |kurtosis |lags      |lastobs   |ldet     |
|ldiff    |lincomb   |linearize |ljungbox |lngamma  |loess     |log       |log10    |
|log2     |logistic  |lpsolve   |lower    |lrcovar  |lrvar     |Lsolve    |mat2list |
|max      |maxc      |maxr      |mcorr    |mcov     |mcovg     |mean      |meanc    |
|meanr    |median    |mexp      |mgradient|midasmult|min       |minc      |minr     |
|missing  |misszero  |mlag      |mlincomb |mlog     |mnormal   |mols      |monthlen |
|movavg   |mpiallred |mpibarrier|mpibcast |mpirecv  |mpireduce |mpiscatter|mpisend  |
|mpols    |mrandgen  |mread     |mreverse |mrls     |mshape    |msortby   |msplitby |
|muniform |mweights  |mwrite    |mxtab    |naalen   |nadarwat  |nelem     |ngetenv  |
|nlines   |NMmax     |NMmin     |nobs     |normal   |normtest  |npcorr    |npv      |
|NRmax    |NRmin     |nullspace |numhess  |obs      |obslabel  |obsnum    |ok       |
|onenorm  |ones      |orthdev   |pdf      |pergm    |pexpand   |pmax      |pmean    |
|pmin     |pnobs     |polroots  |polyfit  |princomp |prodc     |prodr     |psd      |
|psdroot  |pshrink   |psum      |pvalue   |pxnobs   |pxsum     |qform     |qlrpval  |
|qnorm    |qrdecomp  |quadtable |quantile |randgen  |randgen1  |randint   |randperm |
|randstr  |rank      |ranking   |rcond    |Re       |readfile  |regsub    |remove   |
|replace  |resample  |rgbmix    |round    |rnameget |rnameset  |rows      |schur    |
|sd       |sdc       |sdiff     |seasonals|selifc   |selifr    |seq       |setnote  |
|sgn      |simann    |sin       |sinh     |skewness |sleep     |smplspan  |sort     |
|sortby   |sphericorr|sprintf   |sqrt     |square   |sscanf    |sst       |stack    |
|stdize   |strfday   |strftime  |stringify|strlen   |strncmp   |strpday   |strptime |
|strsplit |strstr    |strstrip  |strsub   |strvals  |strvsort  |substr    |sum      |
|sumall   |sumc      |sumr      |svd      |svm      |tan       |tanh      |tdisagg  |
|toepsolv |tolower   |toupper   |tr       |transp   |trigamma  |trimr     |typename |
|typeof   |typestr   |uniform   |uniq     |unvech   |upper     |urcpval   |values   |
|var      |varname   |varnames  |varnum   |varsimul |vec       |vech      |vma      |
|weekday  |wmean     |wsd       |wvar     |xmlget   |zeromiss  |zeros     |         |


Accessors
---------

$ahat
-----

**Output:** series

Must follow the estimation of a fixed-effects or random-effects panel data model. Returns a series containing the estimates of the individual effects.

* * *

$aic
----

**Output:** scalar

Returns the Akaike Information Criterion for the last estimated model, if available. See chapter 28 of the Gretl User's Guide for details of the calculation.

* * *

$allprobs
---------

**Output:** matrix

Must follow estimation via ordered probit or logit, or multinomial logit. Returns an _n_ x _j_ matrix, where _n_ is the number of observations used and _j_ is the number of possible outcomes, holding the estimated probability of each outcome at each observation.

* * *

$bic
----

**Output:** scalar

Returns Schwarz's Bayesian Information Criterion for the last estimated model, if available. See chapter 28 of the Gretl User's Guide for details of the calculation.

* * *

$chisq
------

**Output:** scalar

Returns the overall chi-square statistic from the last estimated model, if available.

* * *

$coeff
------

**Output:** matrix or scalar



With no arguments, $coeff returns a column vector containing the estimated coefficients for the last model. With the optional string argument it returns a scalar, namely the estimated parameter named _s_. See also $stderr, $vcv.

Example:

```
	  open bjg
	  arima 0 1 1 ; 0 1 1 ; lg
	  b = $coeff               # gets a vector
	  macoef = $coeff(theta_1) # gets a scalar
```


If the "model" in question is actually a system, the result depends on the characteristics of the system: for VARs and VECMs the value returned is a matrix with one column per equation, otherwise it is a column vector containing the coefficients from the first equation followed by those from the second equation, and so on.

* * *

$command
--------

**Output:** string

Must follow the estimation of a model; returns the command word, for example ols or probit.

* * *

$compan
-------

**Output:** matrix

Must follow the estimation of a VAR or a VECM; returns the companion matrix.

* * *

$datatype
---------

**Output:** scalar

Returns an integer value representing the sort of dataset that is currently loaded: 0 = no data; 1 = cross-sectional (undated) data; 2 = time-series data; 3 = panel data.

* * *

$depvar
-------

**Output:** string

Must follow the estimation of a single-equation model; returns the name of the dependent variable.

* * *

$df
---

**Output:** scalar

Returns the degrees of freedom of the last estimated model. If the last model was in fact a system of equations, the value returned is the degrees of freedom per equation; if this differs across the equations then the value given is the number of observations minus the mean number of coefficients per equation (rounded up to the nearest integer).

* * *

$diagpval
---------

**Output:** scalar

Must follow estimation of a system of equations. Returns the _P_\-value associated with the $diagtest statistic.

* * *

$diagtest
---------

**Output:** scalar

Must follow estimation of a system of equations. Returns the test statistic for the null hypothesis that the cross-equation covariance matrix is diagonal. This is the Breusch–Pagan test except when the estimator is (unrestricted) iterated SUR, in which case it is a Likelihood Ratio test. See chapter 34 of the Gretl User's Guide for details; see also $diagpval.

* * *

$dotdir
-------

**Output:** string

This accessor returns the path where gretl stores temporary files, for example when using the mwrite function with a non-zero third argument.

* * *

$dw
---

**Output:** scalar

Returns the Durbin–Watson statistic for first-order serial correlation from the model last estimated (if available).

* * *

$dwpval
-------

**Output:** scalar

Returns the CDF of the Durbin–Watson distribution evaluated at the DW statistic for the model last estimated (if available), computed using the Imhof procedure. This is the p-value for a one-sided test with an alternative of positive first-order autocorrelation. If you want the p-value for a two-sided test, take 2_P_ if DW < 2 or 2(1 – _P_) if DW > 2, where _P_ is the value returned by the accessor.

Due to the limited precision of digital arithmetic, the Imhof integral can go negative when the Durbin–Watson statistic is close to its lower bound. In that case the accessor returns NA. Since any other failure mode results in an error being flagged it is probably safe to assume that an NA value means the true p-value is "very small", although we are unable to quantify it.

* * *

$ec
---

**Output:** matrix

Must follow the estimation of a VECM; returns a matrix containing the error correction terms. The number of rows equals the number of observations used and the number of columns equals the cointegration rank of the system.

* * *

$error
------

**Output:** scalar

Returns the program's internal error code, which will be non-zero in case an error has occurred but has been trapped using catch. Note that using this accessor causes the internal error code to be reset to zero. If you want to get the error message associated with a given $error you need to store the value in a temporary variable, as in

```
	  err = $error
	  if (err)
	      printf "Got error %d (%s)\n", err, errmsg(err)
	  endif
```


See also catch, errmsg.

* * *

$ess
----

**Output:** scalar

Returns the error sum of squares of the last estimated model, if available.

* * *

$evals
------

**Output:** matrix

Must follow the estimation of a VECM; returns a vector containing the eigenvalues that are used in computing the trace test for cointegration.

* * *

$fcast
------

**Output:** matrix

Must follow the fcast forecasting command; returns the forecast values as a matrix. If the model on which the forecast was based is a system of equations the returned matrix will have one column per equation, otherwise it is a column vector.

* * *

$fcse
-----

**Output:** matrix

Must follow the fcast forecasting command; returns the standard errors of the forecasts, if available, as a matrix. If the model on which the forecast was based is a system of equations the returned matrix will have one column per equation, otherwise it is a column vector.

* * *

$fevd
-----

**Output:** matrix

Must follow estimation of a VAR. Returns a matrix containing the forecast error variance decomposition (FEVD). This matrix has _h_ rows where _h_ is the forecast horizon, which can be chosen using set horizon or otherwise is set automatically based on the frequency of the data.

For a VAR with _p_ variables, the matrix has _p_2 columns: the first _p_ columns contain the FEVD for the first variable in the VAR; the second _p_ columns the FEVD for the second variable; and so on. The (decimal) fraction of the forecast error for variable _i_ attributable to innovation in variable _j_ is therefore found in column (_i_ – 1)_p_ + _j_.

For a more flexible variant of this functionality, see the fevd function.

* * *

$Fstat
------

**Output:** scalar

Returns the overall F-statistic from the last estimated model, if available.

* * *

$gmmcrit
--------

**Output:** scalar

Must follow a gmm block. Returns the value of the GMM objective function at its minimum.

* * *

$h
--

**Output:** series

Must follow a garch command. Returns the estimated conditional variance series.

* * *

$hausman
--------

**Output:** row vector

Must follow estimation of a model via either tsls or panel with the random effects option. Returns a 1 x 3 vector containing the value of the Hausman test statistic, the corresponding degrees of freedom and the p-value for the test, in that order.

* * *

$hqc
----

**Output:** scalar

Returns the Hannan-Quinn Information Criterion for the last estimated model, if available. See chapter 28 of the Gretl User's Guide for details of the calculation.

* * *

$huge
-----

**Output:** scalar

Returns a very large positive number. By default this is 1.0E100, but the value can be changed using the set command.

* * *

$jalpha
-------

**Output:** matrix

Must follow the estimation of a VECM, and returns the loadings matrix. It has as many rows as variables in the VECM and as many columns as the cointegration rank.

* * *

$jbeta
------

**Output:** matrix

Must follow the estimation of a VECM, and returns the cointegration matrix. It has as many rows as variables in the VECM (plus the number of exogenous variables that are restricted to the cointegration space, if any), and as many columns as the cointegration rank.

* * *

$jvbeta
-------

**Output:** square matrix

Must follow the estimation of a VECM, and returns the estimated covariance matrix for the elements of the cointegration vectors.

In the case of unrestricted estimation, this matrix has a number of rows equal to the unrestricted elements of the cointegration space after the Phillips normalization. If, however, a restricted system is estimated via the restrict command with the \--full option, a singular matrix with _(n+m)r_ rows will be returned (_n_ being the number of endogenous variables, _m_ the number of exogenous variables that are restricted to the cointegration space, and _r_ the cointegration rank).

Example: the code

```
	  open denmark.gdt
	  vecm 2 1 LRM LRY IBO IDE --rc --seasonals -q
	  s0 = $jvbeta

	  restrict --full
	    b[1,1] = 1
	    b[1,2] = -1
	    b[1,3] + b[1,4] = 0
	  end restrict
	  s1 = $jvbeta

	  print s0
	  print s1
```


produces the following output.

```
	  s0 (4 x 4)

          0.019751     0.029816  -0.00044837   -0.12227
          0.029816     0.31005   -0.45823      -0.18526
         -0.00044837  -0.45823    1.2169       -0.035437
         -0.12227     -0.18526   -0.035437      0.76062

	  s1 (5 x 5)

	  0.0000       0.0000       0.0000       0.0000       0.0000
	  0.0000       0.0000       0.0000       0.0000       0.0000
	  0.0000       0.0000      0.27398     -0.27398    -0.019059
	  0.0000       0.0000     -0.27398      0.27398     0.019059
	  0.0000       0.0000    -0.019059     0.019059    0.0014180
```


* * *

$lang
-----

**Output:** string

Returns a string representing the national language in force currently, if this can be determined. The string is composed of a two-letter ISO 639-1 language code (for example, en for English, jp for Japanese, el for Greek) followed by an underscore plus a two-letter ISO 3166-1 country code. Thus for example Portuguese in Portugal gives pt\_PT while Portuguese in Brazil gives pt\_BR.

If the national language cannot be determined, the string "unknown" is returned.

* * *

$llt
----

**Output:** series

For selected models estimated via Maximum Likelihood, returns the series of per-observation log-likelihood values. At present this is supported only for binary logit and probit, tobit and heckit.

* * *

$lnl
----

**Output:** scalar

Returns the log-likelihood for the last estimated model (where applicable).

* * *

$macheps
--------

**Output:** scalar

Returns the value of "machine epsilon", which gives an upper bound on the relative error due to rounding in double-precision floating point arithmetic.

* * *

$mapfile
--------

**Output:** string

If data from a GeoJSON file or ESRI shapefile have been loaded, returns the name of the file that should be opened to obtain the map polygons, otherwise returns an empty string. This is designed for use with the geoplot function.

* * *

$mnlprobs
---------

**Output:** matrix

Following estimation of a multinomial logit model (only), retrieves a matrix holding the estimated probabilities of each possible outcome at each observation in the model's sample range. Each row represents an observation and each column an outcome. As of gretl 2023a this accessor is deprecated: please use $allprobs instead.

* * *

$model
------

**Output:** bundle

Must follow estimation of a single-equation model; returns a bundle containing many items of data pertaining to the model. All the regular model accessors are included: these are referenced by keys that are the same as the regular accessor names, minus the leading dollar sign. So for example the residuals appear under the key uhat and the error sum of squares under ess.

Depending on the estimator, additional information may be available; the keys for such information should hopefully be fairly self-explanatory. To see what's available you can get a copy of the bundle and print its content, as in

```
	  ols y 0 x
	  bundle b = $model
	  print b
```


* * *

$mpirank
--------

**Output:** integer

If gretl is built with MPI support, and the program is running in MPI mode, returns the 0-based "rank" or ID number of the current process. Otherwise returns –1.

* * *

$mpisize
--------

**Output:** integer

If gretl is built with MPI support, and the program is running in MPI mode, returns the number of MPI processes currently running. Otherwise returns 0.

* * *

$ncoeff
-------

**Output:** integer

Returns the total number of coefficients estimated in the last model.

* * *

$nobs
-----

**Output:** integer

Returns the number of observations in the currently selected sample. Related: $tmax.

In the case of panel data the value returned is the number of pooled observations (number of units times number of observations per unit). If you want the time-series length of a panel use $pd, and the number of included units can be found as $nobs divided by $pd.

* * *

$now
----

**Output:** vector

Returns a 2-vector: its first element is the number of seconds elapsed since 1970-01-01 00:00:00 +0000 (UTC, or Coordinated Universal Time), which is widely used in the computing world to represent the current time, and the second is the current date in ISO 8601 "basic" format, YYYYMMDD. The strftime function may be used to process the first element, and epochday may be used to process the second.

* * *

$nvars
------

**Output:** integer

Returns the number of series in the dataset (including the constant). Since const is always present in any dataset a return value of 0 indicates that no dataset is in place. Note that if this accessor is used within a function, the number of series currently accessible may well fall short of that given by $nvars.

* * *

$obsdate
--------

**Output:** series

Applicable when the current dataset is time-series with annual, quarterly, monthly or decennial frequency, or is dated daily or weekly, or when the dataset is a panel with time-series information set appropriately (see the setobs command). The returned series holds 8-digit numbers on the pattern YYYYMMDD (ISO 8601 "basic" date format), which correspond to the day of the observation, or the first day of the observation period in case of a time-series frequency less than daily.

Such a series can be helpful when using the join command.

* * *

$obsmajor
---------

**Output:** series

Returns a series holding the "major" or low-frequency component of each observation. This means the year for annual, quarterly or monthly time series; the day for hourly data; or the individual in the case of panel data. If the data are cross-sectional the series returned is just a 1-based index of the observations.

See also $obsminor, $obsmicro.

* * *

$obsmicro
---------

**Output:** series

Applicable when the observations in the current dataset have a major:minor:micro structure, as in dated daily time series (year:month:day). Returns a series holding the micro or highest-frequency component of each observation (for example, the day).

See also $obsmajor, $obsminor.

* * *

$obsminor
---------

**Output:** series

Applicable when the observations in the current dataset have a major:minor structure, as in quarterly time series (year:quarter), monthly time series (year:month), hourly data (day:hour) and panel data (individual:period). Returns a series holding the minor or high-frequency component of each observation (for example, the month).

In the case of dated daily data, $obsminor gets the month of each observation.

See also $obsmajor, $obsmicro.

* * *

$panelpd
--------

**Output:** integer

Specific to panel data, returns the time-series periodicity (e.g. 4 for quarterly data). If the periodicity is not set in the active panel dataset, returns 1 in analogy to $pd for cross-sectional or undated data. If the dataset is not a panel NA is returned.

See also $pd, $datatype, setobs.

* * *

$parnames
---------

**Output:** array of strings

Following estimation of a single-equation model, returns an array of strings holding the names of the model's parameters. The number of names matches the number of elements in the $coeff vector.

For models specified via a list of regressors the result will be the same as that of

```
	  varnames($xlist)
```


(see varnames), but $parnames is more general; it also works for models with no regressor list (nls, mle, gmm).

* * *

$pd
---

**Output:** integer

Returns the frequency or periodicity of the data (e.g. 4 for quarterly data). In the case of panel data the value returned is the total time-series length.

See also $panelpd.

* * *

$pi
---

**Output:** scalar

Returns the value of π in double precision.

* * *

$pkgdir
-------

**Output:** string

A special facility for use by authors of function packages. Returns an empty string unless a packaged function is executing, in which case it returns the full (platform dependent) path under which the package is installed. For instance the return value might be

```
	  /usr/share/gretl/functions/foo
```


if that's the directory in which foo.gfn is located. This enables package writers to access resources such as matrix files that they have included in their package.

* * *

$pvalue
-------

**Output:** scalar or matrix

Returns the p-value of the test statistic that was generated by the last explicit hypothesis-testing command, if any (for example, chow). See chapter 10 of the Gretl User's Guide for details.

In most cases the return value is a scalar but sometimes it is a matrix (for example, the trace and lambda-max p-values from the Johansen cointegration test); in that case the values in the matrix are laid out in the same pattern as the printed results.

See also $test.

* * *

$qlrbreak
---------

**Output:** scalar

Must follow an invocation of the qlrtest command (the QLR test for a structural break at an unknown point). The value returned is the 1-based index of the observation at which the test statistic is maximized.

* * *

$result
-------

**Output:** matrix or bundle

Provides stored information following certain commands that do not have specific accessors. The commands in question include bds, bkw, corr, fractint, freq, hurst, leverage, summary, vif and xtab (in which cases the result is a matrix), plus pkg (which optionally stores a bundle result).

* * *

$rho
----

**Output:** scalar



Without arguments, returns the first-order autoregressive coefficient for the residuals of the last model. After estimating a model via the ar command, the syntax $rho(n) returns the corresponding estimate of ρ(_n_).

* * *

$rsq
----

**Output:** scalar

Returns the unadjusted _R_2 from the last estimated model, if available. Usually this will be the regular (centered) _R_2 but if the specification contains no constant (and no set of regressors that "add up to" a constant) it will be the uncentered version. In that case the centered version can be accessed as $model.centered\_R2.

* * *

$sample
-------

**Output:** series

Must follow estimation of a single-equation model. Returns a dummy series with value 1 for observations used in estimation, 0 for observations within the currently defined sample range but not used (presumably because of missing values), and NA for observations outside of the current range.

If you wish to compute statistics based on the sample that was used for a given model, you can do, for example:

```
	  ols y 0 xlist
	  series sdum = $sample
	  smpl sdum --dummy
```


* * *

$sargan
-------

**Output:** row vector

Must follow a tsls command. Returns a 1 x 3 vector, containing the value of the Sargan over-identification test statistic, the corresponding degrees of freedom and p-value, in that order. If the model is exactly identified, the statistic is unavailable, and trying to access it provokes an error.

* * *

$seed
-----

**Output:** scalar

Returns the value with which gretl's random number generator was seeded. If you set the seed yourself there's no need to use this accessor, but it may be of interest if the seed was set automatically (based on the time that execution of the program started).

* * *

$sigma
------

**Output:** scalar or matrix

Requires that a model has been estimated. If the last model was a single equation, returns the (scalar) Standard Error of the Regression (or in other words, the standard deviation of the residuals, with an appropriate degrees of freedom correction). If the last model was a system of equations, returns the cross-equation covariance matrix of the residuals.

* * *

$stderr
-------

**Output:** matrix or scalar



With no arguments, $stderr returns a column vector containing the standard error of the coefficients for the last model. With the optional string argument it returns a scalar, namely the standard error of the parameter named _s_.

If the "model" in question is actually a system, the result depends on the characteristics of the system: for VARs and VECMs the value returned is a matrix with one column per equation, otherwise it is a column vector containing the coefficients from the first equation followed by those from the second equation, and so on.

See also $coeff, $vcv.

* * *

$stopwatch
----------

**Output:** scalar

Must be preceded by set stopwatch, which activates the measurement of CPU time. The first use of this accessor yields the seconds of CPU time that have elapsed since the set stopwatch command. At each access the clock is reset, so subsequent uses of $stopwatch yield the seconds of CPU time since the previous access.

When a user-defined function is executing, the set stopwatch command and $stopwatch accessor are specific to that function—that is, timing within a function does not disrupt any "global" timing that may be going on in the main script.

* * *

$sysA
-----

**Output:** matrix

Must follow estimation of a simultaneous equations system. Returns the matrix of coefficients on the lagged endogenous variables, if any, in the structural form of the system. See the system command.

* * *

$sysB
-----

**Output:** matrix

Must follow estimation of a simultaneous equations system. Returns the matrix of coefficients on the exogenous variables in the structural form of the system. See the system command.

* * *

$sysGamma
---------

**Output:** matrix

Must follow estimation of a simultaneous equations system. Returns the matrix of coefficients on the contemporaneous endogenous variables in the structural form of the system. See the system command.

* * *

$sysinfo
--------

**Output:** bundle

Returns a bundle containing information on the capabilities of the gretl build and the system on which gretl is running. The members of the bundle are as follows:

*   gui\_mode: integer, equals 1 if libgretl is being called by the GUI program, otherwise 0.
    
*   mpi: integer, equals 1 if the system supports MPI (Message Passing Interface), otherwise 0.
    
*   omp: integer, equals 1 if gretl is built with support for Open MP, otherwise 0.
    
*   ncores: integer, the number of physical processor cores available.
    
*   nproc: integer, the number of processors available, which will be greater than ncores if hyper-threading is enabled.
    
*   mpimax: integer, the maximum number of MPI processes that can be run in parallel. This is zero if MPI is not supported, otherwise it equals the local nproc value unless an MPI hosts file has been specified, in which case it is the sum of the number of processors or "slots" across all the machines referenced in that file.
    
*   wordlen: integer, either 32 or 64 for 32- and 64-bit systems respectively.
    
*   os: string representing the operating system, either linux, macos, windows or other. Note that versions of gretl prior to 2021e gave the string osx for the Mac operating system; a version-independent test for Mac is therefore instring($sysinfo.os, "os")
    
*   hostname: the name of the host machine on which the current gretl process is running (with a fallback of localhost in case the name cannot be determined).
    
*   mem: a 2-vector holding total physical memory and free or available memory, expressed in MB. This information may not be available on all systems but should be on Windows, macOS and Linux.
    
*   blas: string identifying the supplier of the BLAS (Basic Linear Algebra Subprograms) library in use by gretl.
    
*   blas\_version: string identifying the version number of the blas library in use.
    
*   blascore: (if applicable) a string identifying the CPU type for which the current blas library is optimized.
    
*   compiler: a string identifying the compiler used when building libgretl.
    
*   cpuid: a string identifying the vendor and model of the CPU on which libgretl is running.
    
*   gnuplot: a string identifying the version of gnuplot available to gretl for plotting, in the form of three dot-separated numbers giving major version, minor version and patchlevel.
    
*   foreign: a sub-bundle containing 0/1 indicators for the presence on the host system of each of the "foreign" programs supported by gretl, under the keys julia, octave, ox, python, Rbin, Rlib and stata. The two keys pertaining to R represent the R executable and shared library, respectively.
    

Note that individual elements in the bundle can be accessed using "dot" notation without any need to copy the whole bundle under a user-specified name. For example,

```
	  if $sysinfo.os == "linux"
	      # do something linux-specific
	  endif
```


* * *

$system
-------

**Output:** bundle

Must follow estimation of a system of equations via one of the commands system, var or vecm; returns a bundle containing many items of data pertaining to the system. All the relevant regular system accessors are included: these are referenced by keys that are the same as the regular accessor names, minus the leading dollar sign. So for example the residuals appear under the key uhat and the coefficients under coeff. (Exceptions are the keys A, B, and Gamma, which correspond to the regular dollar accessors sysA, sysB, and sysGamma.) The keys for additional information should hopefully be fairly self-explanatory. To see what's available you can get a copy of the bundle and print its content, as in

```
	  var 4 y1 y2 y2
	  bundle b = $system
	  print b
```


A bundle obtained in this way can be passed as the final, optional argument to the functions fevd and irf.

* * *

$T
--

**Output:** integer

Returns the number of observations used in estimating the last model.

* * *

$t1
---

**Output:** integer

Returns the 1-based index of the first observation in the currently selected sample.

* * *

$t2
---

**Output:** integer

Returns the 1-based index of the last observation in the currently selected sample.

* * *

$test
-----

**Output:** scalar or matrix

Returns the value of the test statistic that was generated by the last explicit hypothesis-testing command, if any (e.g. chow). See chapter 10 of the Gretl User's Guide for details.

In most cases the return value is a scalar but sometimes it is a matrix (for example, the trace and lambda-max statistics from the Johansen cointegration test); in that case the values in the matrix are laid out in the same pattern as the printed results.

See also $pvalue.

* * *

$time
-----

**Output:** series

For time-series or panel data, creates a 1-based index of the time period. In the panel case the sequence of values repeats for each cross-sectional unit.

The command "genr time" is an alternative, with the difference that the genr variant automatically creates a series called time while the naming of the series is up to the caller when using $time, as in

```
	  series trend = $time
```


This accessor is not available for cross-sectional data.

* * *

$tmax
-----

**Output:** integer

Returns the maximum legal setting for the end of the sample range via the smpl command. In most cases this will equal the number of observations in the dataset but within a hansl function the $tmax value may be smaller, since in general data access within functions is limited to the sample range set by the caller.

Note that $tmax does not in general equal $nobs, which gives the number of observations in the current sample range.

* * *

$trsq
-----

**Output:** scalar

Returns _TR_2 (sample size times R-squared) from the last model, if available.

* * *

$uhat
-----

**Output:** series

Returns the residuals from the last model. This may have different meanings for different estimators. For example, after an ARMA estimation $uhat will contain the one-step-ahead forecast error; after a probit model, it will contain the generalized residuals.

If the "model" in question is actually a system (a VAR or VECM, or system of simultaneous equations), $uhat retrieves the matrix of residuals, one column per equation.

* * *

$unit
-----

**Output:** series

Valid for panel datasets only. Returns a series with value 1 for all observations on the first unit or group, 2 for observations on the second unit, and so on.

* * *

$vcv
----

**Output:** matrix or scalar


|Arguments:|s1 (name of coefficient, optional)|
|----------|----------------------------------|
|          |s2 (name of coefficient, optional)|


With no arguments, $vcv returns a square matrix containing the estimated covariance matrix for the coefficients of the last model. If the last model was a single equation, then you may supply the names of two parameters in parentheses to retrieve the estimated covariance between the parameters named _s1_ and _s2_. See also $coeff, $stderr.

This accessor is not available for VARs or VECMs; for models of that sort see $sigma and $xtxinv.

* * *

$vecGamma
---------

**Output:** matrix

Must follow the estimation of a VECM; returns a matrix in which the Gamma matrices (coefficients on the lagged differences of the cointegrated variables) are stacked side by side. Each row represents an equation; for a VECM of lag order _p_ there are _p_ – 1 sub-matrices.

* * *

$version
--------

**Output:** scalar

Returns an integer value that codes for the program version. The current gretl version string takes the form of a 4-digit year followed by a letter from a to j representing the sequence of releases within the year (for example, 2015d). The return value from this accessor is formed as 10 times the year plus the zero-based lexical order of the letter, so 2015d translates to 20153.

Prior to gretl 2015d, version identifiers took the form x.y.z (three integers separated by dots), and in that case the accessor value was calculated as 10000\*x + 100\*y + z, so that for example 1.10.2 (the last release under the old scheme) translates as 11002. Numerical order of $version values is therefore preserved across the change in versioning scheme.

* * *

$vma
----

**Output:** matrix

Must follow the estimation of a VAR or a VECM; returns a matrix containing the VMA representation up to the order specified via the set horizon command. See chapter 32 of the Gretl User's Guide for details.

* * *

$windows
--------

**Output:** integer

Returns 1 if gretl is running on MS Windows, otherwise 0. By conditioning on the value of this variable you can write shell calls that are portable across different operating systems.

Also see the shell command.

* * *

$workdir
--------

**Output:** string

This accessor returns the path which gretl reads from and writes to by default. A fuller discussion is provided in the Command Reference under workdir. Note that this string can be set by the user via the set command.

* * *

$xlist
------

**Output:** list

If the last model was a single equation, returns the list of regressors. If the last model was a system of equations, returns the "global" list of exogenous variables (in the same order in which they appear in $sysB). If the last model was a VAR, returns the list of exogenous regressors, if any, except for standard deterministic terms (constant, trend, seasonals).

* * *

$xtxinv
-------

**Output:** matrix

Following estimation of a VAR or VECM (only), returns _X'X_\-1, where _X_ is the common matrix of regressors used in each of the equations. While this accessor is available for a VECM estimated with a restriction imposed on α (the "loadings" matrix), it should be borne in mind that in that case not all coefficients of the regressors are freely varying.

* * *

$yhat
-----

**Output:** series

Returns the fitted values from the last regression.

* * *

$ylist
------

**Output:** list

If the last model estimated was a VAR, VECM or simultaneous system, returns the associated list of endogenous variables. If the last model was a single equation, this accessor gives a list with a single element, the dependent variable. In the special case of the biprobit model the list contains two elements.

Built-in strings
----------------

$dotdir
-------

**Output:** string

Yields the full path of the directory gretl uses for temporary files. To use it in string-substitution mode, prepend the at-sign (@dotdir).

* * *

$gnuplot
--------

**Output:** string

Yields the path to the gnuplot executable. To use it in string-substitution mode, prepend the at-sign (@gnuplot).

* * *

$gretldir
---------

**Output:** string

Yields the full path of the gretl installation directory. To use it in string-substitution mode, prepend the at-sign (@gretldir).

* * *

$tramo
------

**Output:** string

Yields the path to the tramo executable. To use it in string-substitution mode, prepend the at-sign (@tramo)

* * *

$tramodir
---------

**Output:** string

Yields the path string of the tramo data directory. To use it in string-substitution mode, prepend the at-sign (@tramodir).

* * *

$x12a
-----

**Output:** string

Yields the path to the x-12-arima executable. To use it in string-substitution mode, prepend the at-sign (@x12a).

* * *

$x12adir
--------

**Output:** string

Yields the path of the x-12-arima data directory. To use it in string-substitution mode, prepend the at-sign (@x12adir).

Functions proper
----------------

abs
---

**Output:** same type as input



Returns the absolute value of _x_.

* * *

acos
----

**Output:** same type as input



Returns the arc cosine of _x_, that is, the value whose cosine is _x_. The result is in radians; the input should be in the range –1 to 1.

* * *

acosh
-----

**Output:** same type as input



Returns the inverse hyperbolic cosine of _x_ (positive solution). _x_ should be greater than 1; otherwise, NA is returned. See also cosh.

* * *

aggregate
---------

**Output:** matrix


|Arguments:|x (series, list or matrix)    |
|----------|------------------------------|
|          |byvar (series, list or matrix)|
|          |funcname (string, optional)   |


Most of the following assumes that the first two arguments to this function take the form of series or lists, but see "Matrix input" below for alternative usage.

In the most minimal usage, _x_ is set to null, _byvar_ is a single series and the third argument is omitted, or set to null. In this case, the return value is a matrix with two columns holding, respectively, the distinct values of _byvar_, sorted in ascending order, and the count of observations at which _byvar_ takes on each of these values. For example,

```
	  open data4-1
	  eval aggregate(null, bedrms)
```


will show that the series bedrms has values 3 (with count 5) and 4 (with count 9).

More generally, if _byvar_ is a list with _n_ members, then the left-hand _n_ columns hold the combinations of the distinct values of each of the _n_ series and the count column holds the number of observations at which each combination is realized. Note that the count column can always be found at the position nelem(byvar) + 1.

### Specifying an aggregation function

If the third argument is given, then _x_ must not be null, and the rightmost _m_ columns hold the values of the statistic specified by _funcname_ for each of the variables in _x_. (Thus, _m_ is equal to 1 if _x_ is a single series and equal to nelem(x) if _x_ is a list.) The given statistic is calculated on the respective sub-samples defined by the combinations in _byvar_ (in ascending order); these combinations are shown in the first _n_ column(s) of the returned matrix.

So, in the special case where _x_ and _byvar_ are both individual series, the return value is a matrix with three columns holding, respectively, the distinct values of _byvar_, sorted in ascending order; the count of observations at which _byvar_ takes on each of these values; and the values of the statistic specified by _funcname_ calculated on series _x_, using only those observations at which _byvar_ takes on the value given in the first column.

The following values of _funcname_ are supported "natively": sum, sumall, mean, sd, var, sst, skewness, kurtosis, min, max, median, nobs, gini, isconst and isdummy. Each of these functions takes a series argument and returns a scalar value, and in that sense can be said to "aggregate" the series in some way. If none of these built-in functions does what you need, you can give the name of a user-defined function as the aggregator; like the built-ins, such a function must take a single series argument and return a scalar value.

Note that although a count of cases is provided automatically the nobs function is not redundant as an aggregator, since it gives the number of valid (non-missing) observations on _x_ at each _byvar_ combination.

For a simple example, suppose that region represents a coding of geographical region using integer values 1 to _n_, and income represents household income. Then the following would produce an _n_ x 3 matrix holding the region codes, the count of observations in each region, and mean household income for each of the regions:

```
	  matrix m = aggregate(income, region, mean)
```


For an example using lists, let gender be a male/female dummy variable, let race be a categorical variable with three values, and consider the following:

```
	  list BY = gender race
	  list X = income age
	  matrix m = aggregate(X, BY, sd)
```


The aggregate call here will produce a 6 x 5 matrix. The first two columns hold the 6 distinct combinations of gender and race values; the middle column holds the count for each of these combinations; and the rightmost two columns contain the sample standard deviations of income and age.

Note that if _byvar_ is a list, some combinations of the _byvar_ values may not be present in the data (giving a count of zero). In that case the value of the statistics for _x_ are recorded as NaN (not a number). If you want to ignore such cases you can use the selifr function to select only those rows that have a non-zero count. The column to test is one place to the right of the number of _byvar_ variables, so we can do:

```
	  matrix m = aggregate(X, BY, sd)
	  scalar c = nelem(BY)
	  m = selifr(m, m[,c+1])
```


### Matrix input

Instead of series or lists, _x_ and _byvar_ may be given in matrix form. However, if both arguments are provided they must match in type (you cannot give a series or list for one argument and a matrix for the other) and two matrix arguments must have the same number of rows. Also note that in this context matrix columns are treated as if they were series, so the aggregation function must follow the pattern described above, taking a series argument and returning a scalar.

* * *

argname
-------

**Output:** string


|Arguments:|s (string)                |
|----------|--------------------------|
|          |default (string, optional)|


For _s_ the name of a parameter to a user-defined function, returns the name of the corresponding argument, if the argument had a name at the caller level. If the argument was anonymous, an empty string is returned unless the optional _default_ argument is provided, in which case its value is used as a fallback.

* * *

array
-----

**Output:** see below

The basic "constructor" function for a new array variable. In using this function you must specify a type (in plural form) for the array: strings, matrices, bundles, lists or arrays. The return value is an array of the specified type with _n_ elements, each of which is initialized as "empty" (e.g. zero-length string, null matrix). Examples of usage:

```
	  strings S = array(5)
	  matrices M = array(3)
```


See also defarray.

* * *

asin
----

**Output:** same type as input



Returns the arc sine of _x_, that is, the value whose sine is _x_. The result is in radians; the input should be in the range –1 to 1.

* * *

asinh
-----

**Output:** same type as input



Returns the inverse hyperbolic sine of _x_. See also sinh.

* * *

asort
-----

**Output:** scalar


|Arguments:|a (array)     |
|----------|--------------|
|          |fname (string)|


Performs an in-place sort of the elements of _a_, using a comparator function specified by the caller under the control of the quicksort routine.

The argument _a_ can be of any of the types supported for a gretl array, namely strings, matrices, bundles, lists or arrays. The _fname_ argument must be the name of a function which takes two const arguments, whose type matches that of the elements of _a_. This function must return an integer value on the following pattern: 0 if the two arguments have the same sort order, negative if the first argument sorts before the second, or positive if the second sorts before the first. (The exact values do not matter.)

For example, suppose one wants to sort an array of bundles, each of which contains a scalar named crit, by increasing value of crit. Then the following function would be suitable for passing to asort:

```
	  function scalar my_bsort (const bundle b1, const bundle b2)
	     return sgn(b1.crit - b2.crit)
	  end function
```


If you want to preserve the unsorted array, make a copy of it before passing it to asort. The return value from this function is a nominal 0 on success.

See also sort for simple sorting of an array of strings.

* * *

assert
------

**Output:** scalar

This function is intended for testing or debugging of hansl code. The argument should be an expression which evaluates to a scalar. The return value is 1 if _expr_ evaluates to a non-zero value (boolean "true", or "success") or 0 if it evaluates to zero (boolean "false", or "failure").

By default there are no consequences of a call to assert failing other than the return value being zero. However, the set command can be used to make failure of an assertion more consequential. There are three levels:

```
	  # print a warning message but continue execution
	  set assert warn
	  # print an error message and stop script execution
	  set assert stop
	  # print a message to stderr and abort the program
	  set assert fatal
```


In most cases stop is sufficient to terminate a script but in certain special cases (such as within a function called from a command block such as mle) it may be necessary to use the fatal setting to get a clear indication of the failing assertion. Note, however, that in this case the message will go to standard error output.

The default behavior can be restored via

```
	  set assert off
```


By way of a simple example, if at a certain point in a hansl script a scalar x ought to be non-negative, the following will flag an error if that is not the case:

```
	  set assert stop
	  assert(x >= 0)
```


* * *

atan
----

**Output:** same type as input



Returns the arc tangent of _x_, that is, the value whose tangent is _x_. The result is in radians.

See also tan, atan2.

* * *

atan2
-----

**Output:** same type as input


|Arguments:|y (scalar, series or matrix)|
|----------|----------------------------|
|          |x (scalar, series or matrix)|


Returns the principal value of the arc tangent of _y_/_x_, using the signs of the two arguments to determine the quadrant of the result. The return value is in radians, in the range \[–π, π\].

If the two arguments differ in type, the type of the result is the "higher" of the two, where the ordering is matrix > series > scalar. For example, if _y_ is a scalar and _x_ an _n_\-vector (or vice versa) the result is an _n_\-vector. Note that matrix arguments must be vectors, and if neither argument is a scalar the two arguments must be of the same length.

See also tan, tanh.

* * *

atanh
-----

**Output:** same type as input



Returns the inverse hyperbolic tangent of _x_. See also tanh.

* * *

atof
----

**Output:** scalar

Closely related to the C library function of the same name. Returns the result of converting the string _s_ (or the leading portion thereof, after discarding any initial white space) to a floating-point number. Unlike atof in C, however, the decimal character is always assumed (for reasons of portability) to be ".". Any characters that follow the portion of _s_ that converts to a floating-point number under this assumption are ignored.

If none of _s_ (following any discarded white space) is convertible under the stated assumption, NA is returned.

```
	  # examples
	  x = atof("1.234") # gives x = 1.234
	  x = atof("1,234") # gives x = 1
	  x = atof("1.2y")  # gives x = 1.2
	  x = atof("y")     # gives x = NA
	  x = atof(",234")  # gives x = NA
```


See also sscanf for more flexible string to numeric conversion.

* * *

bcheck
------

**Output:** scalar


|Arguments:|target (reference to bundle)              |
|----------|------------------------------------------|
|          |input (bundle, optional)                  |
|          |required-keys (array of strings, optional)|


Primarily intended for use by writers of function packages. Here is the context in which bcheck may be useful: you have a function which accepts a bundle argument whereby the caller can make various choices. Some elements of the bundle may have default values—so the caller is not obliged to make an explicit choice—while other elements may be required. You want to determine whether the argument you get is valid. The main text below assumes that an _input_ bundle is supplied by the caller of your function, but see the section headed "No input bundle" for the contrary case.

To use bcheck you construct a template bundle containing all the supported keys, with values that exemplify the type associated with each key, and pass this in pointer form as _target_. For the second argument, _input_, pass the bundle you get from the caller. This function then checks the following:

*   Does _input_ contain any keys not present in _target_? If so, bcheck returns a non-zero value, indicating that _input_ is erroneous. (Most likely, the key in question is misspelled.)
    
*   Does _input_ contain under any given key an object whose type does not match that in _target_? If so, a non-zero value is returned.
    
*   If some elements in _target_ require input from the caller (so the value you supply is not a default value, just a placeholder to indicate the required type), you should supply a third argument to bcheck: an array of strings holding the keys for which input is not optional. Then the return value will be non-zero if any required elements are missing from _input_.
    

In addition to the above you may wish to impose lower and/or upper bounds on the value of one or more scalar members of the bundle argument. If so, add a bundle named bounds to your template bundle. Each member of this secondary bundle should have a _key_ that identifies a member of the template bundle; its _value_ should be a 2-vector holding lower and upper limits. Put NA in place of one of the limits if it is unbounded. So, for example, the following code will check that if x1 is given in the caller's input it is between 1 and 5, and if x2 is given it is non-negative:

```
	  template.bounds = _(x1={1,5}, x2={0,NA})
```


If no errors are detected on any of these points, values supplied in _input_ are copied to _target_ (defaults being replaced by valid selections on the caller's part). If errors are found a message will be printed indicating what is wrong with _input_.

To give a simple example, suppose your function's argument bundle supports a matrix X (required), a non-negative scalar z with default value 0, and a string s with default value "display". Then the following code fragment would be suitable for checking a bundle named uservals supplied by the caller:

```
	  bundle target = _(X={}, z=0, s="display")
	  target.bounds = _(z={0,NA})
	  strings req = defarray("X")
	  err = bcheck(&target, uservals, req)
	  if err
	     # react appropriately
	  else
	     # proceed, using the values in target
	  endif
```


### No input bundle

If the _input_ bundle is not supplied to bcheck, it behaves as follows. If the _required-keys_ argument is not given, it returns zero (since none of the error conditions mentioned above can occur), and _target_ is not modified. Otherwise it returns non-zero since it's clear that one or more specifications must be missing. This means that it's safe to pass a null _input_ to bcheck.

* * *

bessel
------

**Output:** same type as input


|Arguments:|type (character)            |
|----------|----------------------------|
|          |v (scalar)                  |
|          |x (scalar, series or matrix)|


Computes one of the Bessel function variants for order _v_ and argument _x_. The return value is of the same type as _x_. The specific function is selected by the first argument, which must be J, Y, I, or K. A good discussion of the Bessel functions can be found on Wikipedia; here we give a brief account.

case J: Bessel function of the first kind. Resembles a damped sine wave. Defined for real _v_ and _x_, but if _x_ is negative then _v_ must be an integer.

case Y: Bessel function of the second kind. Defined for real _v_ and _x_ but has a singularity at _x_ = 0.

case I: Modified Bessel function of the first kind. An exponentially growing function. Acceptable arguments are as for case J.

case K: Modified Bessel function of the second kind. An exponentially decaying function. Diverges at _x_ = 0 and is not defined for negative _x_. Symmetric around _v_ = 0.

* * *

BFGSmax
-------

**Output:** scalar


|Arguments:|&b (reference to matrix)   |
|----------|---------------------------|
|          |f (function call)          |
|          |g (function call, optional)|


Numerical maximization via the method of Broyden, Fletcher, Goldfarb and Shanno. On input the vector _b_ should hold the initial values of a set of parameters, and the argument _f_ should specify a call to a function that calculates the (scalar) criterion to be maximized, given the current parameter values and any other relevant data. If the object is in fact minimization, this function should return the negative of the criterion. On successful completion, BFGSmax returns the maximized value of the criterion, and _b_ holds the parameter values which produce the maximum.

The optional third argument provides a means of supplying analytical derivatives (otherwise the gradient is computed numerically). The gradient function call _g_ must have as its first argument a predefined matrix that is of the correct size to contain the gradient, given in pointer form. It also must take the parameter vector as an argument (in pointer form or otherwise). Other arguments are optional.

For more details and examples see chapter 37 of the Gretl User's Guide. See also BFGScmax, NRmax, fdjac, simann.

* * *

BFGSmin
-------

**Output:** scalar

An alias for BFGSmax; if called under this name the function acts as a minimizer.

* * *

BFGScmax
--------

**Output:** scalar


|Arguments:|&b (reference to matrix)   |
|----------|---------------------------|
|          |bounds (matrix)            |
|          |f (function call)          |
|          |g (function call, optional)|


Constrained numerical maximization using L-BFGS-B (limited memory BFGS, see Byrd, Lu, Nocedal and Zhu, 1995). On input the vector _b_ should hold the initial values of a set of parameters, _bounds_ should hold bounds on the parameter values (see below), and _f_ should specify a call to a function that calculates the (scalar) criterion to be maximized, given the current parameter values and any other relevant data. If the object is in fact minimization, this function should return the negative of the criterion. On successful completion, BFGScmax returns the maximized value of the criterion, subject to the constraints in _bounds_, and _b_ holds the parameter values which produce the maximum.

### Bounds on parameters

The _bounds_ matrix must have 3 columns and as many rows as there are constrained elements in the parameter vector. The first element on a given row is the (1-based) index of the constrained parameter; the second and third are the lower and upper bounds, respectively. The values \-$huge and $huge should be used to indicate that the parameter is unconstrained downward or upward, respectively. For example, the following is the way to specify that the second element of the parameter vector must be non-negative:

```
	  matrix bounds = {2, 0, $huge}
```


### Analytical derivatives

The optional fourth argument provides a means of supplying analytical derivatives (otherwise the gradient is computed numerically). The gradient function call _g_ must have as its first argument a predefined matrix that is of the correct size to contain the gradient, given in pointer form. It also must take the parameter vector as an argument (in pointer form or otherwise). Other arguments are optional.

For more details and examples see chapter 37 of the Gretl User's Guide. See also BFGSmax, NRmax, fdjac, simann.

* * *

BFGScmin
--------

**Output:** scalar

An alias for BFGScmax; if called under this name the function acts as a minimizer.

* * *

bin2dec
-------

**Output:** matrix

Given a matrix _B_ containing only zeros and ones, this function interprets each row as the binary representation of a 32-bit unsigned integer, and returns a column vector with the decimal representation of those integers. The argument cannot have more than 32 columns otherwise an error is flagged.

Note that the least significant bit comes in the first column. So column 1 corresponds to _2_0, column 2 to _2_1, and so on. For example, the expression

```
	  scalar x = bin2dec({1,0,1})
```


stores the value 5 into _x_.

The dec2bin function performs the inverse transformation.

* * *

bincoeff
--------

**Output:** same type as input


|Arguments:|n (scalar, series or matrix)|
|----------|----------------------------|
|          |k (scalar, series or matrix)|


Returns the binomial coefficient, that is the number of ways in which _k_ items can be chosen from _n_ items without repetition, irrespective of ordering. This is also equal to the coefficient of the (_k_+1)-th term in the polynomial expansion of the binomial power _(1+x)^n_.

For integer arguments the result is _n!/(k!(n-k)!)_ but the function also accepts noninteger arguments, and the formula above generalizes to Γ(_n_+1)/(Γ(_k_+1) × Γ(_n-k_+1)).

When _k_ > _n_ or _k_ < 0 no valid answer exists and an error is flagged.

If the two arguments differ in type, the type of the result is the "higher" of the two, where the ordering is matrix > series > scalar. For example, if _n_ is a scalar and _k_ an _r_\-vector (or vice versa) the result is an _r_\-vector. Note that matrix arguments must be vectors, and if neither argument is a scalar the two arguments must be of the same length.

See also gammafun and lngamma.

* * *

binperms
--------

**Output:** matrix


|Arguments:|n (integer)|
|----------|-----------|
|          |k (integer)|


Binary permutations: returns a _p_ x _n_ matrix, each of whose rows holds a distinct arrangement of _k_ ones and _n_ – _k_ zeros (in lexicographic order). The maximum supported value of _n_ is 64, _n_ and _k_ must be non-negative, and _k_ must be no greater than _n_; otherwise an error is flagged. In case _n_ = _k_ = 0 an empty matrix is returned.

For example, with _n_ = 4 and _k_ = 2, the result is

```
	  0   0   1   1 
	  0   1   0   1 
	  0   1   1   0 
	  1   0   0   1 
	  1   0   1   0 
	  1   1   0   0
```


_Warning:_ the number of permutations, _p_, is a steeply increasing function of _n_ and is greatest when _k_ is about half of _n_. You may want to check in advance the size of the matrix that binperms will attempt to allocate. The bincoeff function returns _p_, and the size of the resulting matrix in megabytes can be calculated as

```
	  MB = 8 * n * bincoeff(n, k) / 10^6
```


For _n_ = 30, this gives about 34 MB when _k_ = 25, 7211 MB if _k_ = 20, and 20758 MB if _k_ = 18.

* * *

bkfilt
------

**Output:** series


|Arguments:|y (series)            |
|----------|----------------------|
|          |f1 (integer, optional)|
|          |f2 (integer, optional)|
|          |k (integer, optional) |


Returns the result from application of the Baxter–King bandpass filter to the series _y_. The optional parameters _f1_ and _f2_ represent, respectively, the lower and upper bounds of the range of frequencies to extract, while _k_ is the approximation order to be used.

If these arguments are not supplied then the default values depend on the periodicity of the dataset. For yearly data the defaults for _f1_, _f2_ and _k_ are 2, 8 and 3, respectively; for quarterly data, 6, 32 and 12; for monthly data, 18, 96 and 36. These values are chosen to match the most common choice among practitioners, that is to use this filter for extracting the "business cycle" frequency component; this, in turn, is commonly defined as being between 18 months and 8 years. The filter, per default choice, spans 3 years of data.

If _f2_ is greater than or equal to the number of available observations, then the "low-pass" version of the filter will be run and the resulting series should be taken as an estimate of the trend component, rather than the cycle. See also bwfilt, hpfilt.

* * *

bkw
---

**Output:** matrix


|Arguments:|V (matrix)                           |
|----------|-------------------------------------|
|          |parnames (array of strings, optional)|
|          |verbose (boolean, optional)          |


Computes BKW collinearity diagnostics (see Belsley, Kuh and Welsch (1980)) given a covariance matrix of parameter estimates, _V_. The optional second argument, which can be an array of strings or a string containing comma-separated names, is used to label the columns showing the variance proportions; the number of names should match the dimension of _V_. After estimation of a model in gretl, suitable arguments can be obtained via the $vcv and $parnames accessors.

By default this function operates silently, just returning the BKW table as a matrix, but if a non-zero value is given for the third argument the table is printed along with some analysis.

There is also a command form of this facility, bkw, which automatically references the last model and requires no arguments.

* * *

boxcox
------

**Output:** same type as input


|Arguments:|y (series or matrix)|
|----------|--------------------|
|          |d (scalar)          |


Returns the Box–Cox transformation with parameter _d_ for the positive series _y_ (or the columns of matrix _y_).

The result is (_y_d - 1)/_d_ for _d_ not equal to zero, or log(_y_) for _d_ = 0.

* * *

bread
-----

**Output:** bundle


|Arguments:|fname (string)            |
|----------|--------------------------|
|          |import (boolean, optional)|


Reads a bundle from the file specified by the _fname_ argument. By default the bundle is assumed to be represented in XML, and to be gzip-compressed if _fname_ has extension .gz. But if the extension is .json or .geojson the content is assumed to be JSON.

In the XML case the file must contain a gretl-bundle element, which is used to store zero or more bundled-item elements. For example,

```
	  
	  
          moo
          3
	  
```


As you might expect, files suitable for reading via bread are generated by the companion function bwrite.

If the file name does not contain a full path specification, it will be looked for in several "likely" locations, beginning with the currently set workdir. However, if a non-zero value is given for the optional _import_ argument, the input file is taken to be in the user's "dot" directory. In that case _fname_ should be a plain file name, without any path component.

Should an error occur (such as the file being badly formatted or inaccessible), an error is returned via the $error accessor.

See also mread, bwrite.

* * *

brename
-------

**Output:** scalar


|Arguments:|B (bundle)     |
|----------|---------------|
|          |oldkey (string)|
|          |newkey (string)|


If the bundle _B_ contains a member under the key _oldkey_, its key is changed to _newkey_, otherwise an error is flagged. Returns 0 on successful renaming.

Changing the key of a bundle member is not a common task but it can arise in the context of functions that work with bundles, and brename is an efficient tool for the job. Example:

```
	  # set up a bundle holding a big matrix
	  bundle b
	  b.X = mnormal(1000, 1000)
	  if 0
	      # change the key manually
	      Xcopy = b.X
	      delete b.X
	      b.Y = Xcopy
	      delete Xcopy
	  else
	      # versus: change it efficiently
	      brename(b, "X", "Y")
	  endif
```


The first method requires that the big matrix be copied twice, out of the bundle then back into it under a different key; the efficient method changes the key directly.

* * *

bwfilt
------

**Output:** series


|Arguments:|y (series)    |
|----------|--------------|
|          |n (integer)   |
|          |omega (scalar)|


Returns the result from application of a low-pass Butterworth filter with order _n_ and frequency cutoff _omega_ to the series _y_. The cutoff is expressed in degrees and must be greater than 0 and less than 180. Smaller cutoff values restrict the pass-band to lower frequencies and hence produce a smoother trend. Higher values of _n_ produce a sharper cutoff, at the cost of possible numerical instability.

Inspecting the periodogram of the target series is a useful preliminary when you wish to apply this function. See chapter 30 of the Gretl User's Guide for details. See also bkfilt, hpfilt.

* * *

bwrite
------

**Output:** integer


|Arguments:|B (bundle)                |
|----------|--------------------------|
|          |fname (string)            |
|          |export (boolean, optional)|


Writes the bundle _B_ to file, serialized in XML or, if _fname_ has extension .json or .geojson, as JSON. See bread for a description of the format when XML is used. If _fname_ already exists, it will be overwritten. The nominal return value is 0 on successful completion; if writing fails an error is flagged.

The output file will be written in the currently set workdir, unless _fname_ contains a full path specification. However, if a non-zero value is given for the _export_ argument, the file will be written into the user's "dot" directory. In that case a plain file name, without any path component, should be given for the second argument.

In the case of XML output (only), the option of gzip compression is available; this is applied if _fname_ has the extension .gz.

See also bread, mwrite.

* * *

carg
----

**Output:** matrix



Returns an _m_ x _n_ real matrix holding the complex "argument" of each element of the _m_ x _n_ complex matrix _C_. The argument of the complex number _z_ = _x_ + _yi_ can also be computed as atan2(y, x).

See also abs, cmod, atan2.

* * *

cdemean
-------

**Output:** matrix


|Arguments:|X (matrix)                     |
|----------|-------------------------------|
|          |standardize (boolean, optional)|
|          |skip_na (boolean, optional)    |


Centers the columns of matrix _X_ around their means. If the optional second argument has a non-zero value then in addition the centered values are divided by the column standard deviations (which are calculated using _n_ – 1 as divisor, where _n_ is the number of rows of _X_).

If a non-zero value is supplied for _skip\_na_ missing values are ignored, otherwise if a column of _X_ contains any missing values the corresponding column in the output is all missing.

Note that stdize provides more flexible functionality.

* * *

cdf
---

**Output:** same type as input


|Arguments:|d (string)                  |
|----------|----------------------------|
|          |... (see below)             |
|          |x (scalar, series or matrix)|


**Examples:** p1 = cdf(N, -2.5) p2 = cdf(X, 3, 5.67) p3 = cdf(D, 0.25, -1, 1)

Cumulative distribution function calculator. Returns _P(X <= x)_, where the distribution of _X_ is determined by the string _d_. Between the arguments _d_ and _x_, zero or more additional scalar arguments are required to specify the parameters of the distribution, as follows (but note that the normal distribution has its own convenience function, cnorm).

*   Standard normal (d = z, n, or N): no extra arguments
    
*   Bivariate normal (D): correlation coefficient
    
*   Logistic (lgt or s): no extra arguments
    
*   Student's t (t): degrees of freedom
    
*   Chi square (c, x, or X): degrees of freedom
    
*   Snedecor's F (f or F): df (num.); df (den.)
    
*   Gamma (g or G): shape; scale
    
*   Beta (beta): 2 shape parameters
    
*   Binomial (b or B): probability; number of trials
    
*   Poisson (p or P): mean
    
*   Exponential (exp): scale
    
*   Weibull (w or W): shape; scale
    
*   Laplace (l or L): mean; scale
    
*   Generalized Error (E): shape
    
*   Non-central chi square (ncX): df, non-centrality parameter
    
*   Non-central F (ncF): df (num.), df (den.), non-centrality parameter
    
*   Non-central t (nct): df, non-centrality parameter
    

Note that most cases have aliases to help memorizing the codes. The bivariate normal case is special: the syntax is x = cdf(D, rho, z1, z2) where rho is the correlation between the variables z1 and z2.

See also pdf, critical, invcdf, pvalue.

* * *

cdiv
----

**Output:** matrix


|Arguments:|X (matrix)|
|----------|----------|
|          |Y (matrix)|


This is a legacy function, predating gretl's native support for complex matrices.

Complex division. The two arguments must have the same number of rows, _n_, and either one or two columns. The first column contains the real part and the second (if present) the imaginary part. The return value is an _n_ x 2 matrix or, if the result has no imaginary part, an _n_\-vector. See also cmult.

* * *

cdummify
--------

**Output:** list

This function returns a list in which each series in _L_ that has the "coded" attribute is replaced by a set of dummy variables representing each of its coded values, with the least value omitted. If _L_ contains no coded series the return value will be identical to _L_.

The generated dummy variables, if any, are named on the pattern D_varname_\__vi_ where _vi_ is the _i_th represented value of the coded variable. In case any values are negative, "m" is inserted before the (absolute) value of _vi_.

For example, suppose _L_ contains a coded series named C1 with values –9, –7, 0, 1 and 2. Then the generated dummies will be DC1\_m7 (coding for C1 = –7), DC1\_0 (coding for C1 = 0), and so on.

See also dummify, getinfo.

* * *

ceil
----

**Output:** same type as input



Ceiling function: returns the smallest integer greater than or equal to _x_. See also floor, int.

* * *

cholesky
--------

**Output:** square matrix



Performs a Cholesky decomposition of _A_. If _A_ is real it must be symmetric and positive definite; if so, the result is a lower-triangular matrix _L_ which satisfies _A = LL'_. If _A_ is complex it must be Hermitian and positive definite, and the result is a lower-triangular complex matrix such that _A = LL^H_. Otherwise, the function will return an error.

For the real case, see also psdroot and Lsolve.

* * *

chowlin
-------

**Output:** matrix


|Arguments:|Y (matrix)          |
|----------|--------------------|
|          |xfac (integer)      |
|          |X (matrix, optional)|


We no longer recommend use of this function; please use tdisagg instead.

Expands the input data, _Y_, to a higher frequency, using the method of Chow and Lin (1971). It is assumed that the columns of _Y_ represent data series; the returned matrix has as many columns as _Y_ and _xfac_ times as many rows. It is also assumed that each low-frequency value should be treated as the average of _xfac_ high-frequency values.

The _xfac_ value should be 3 for quarterly to monthly, 4 for annual to quarterly or 12 for annual to monthly. The optional third argument may be used to provide a matrix of covariates at the higher (target) frequency.

The regressors used by default are a constant and trend. If _X_ is provided, its columns are used as additional regressors; it is an error if the number of rows in _X_ does not equal _xfac_ times the number of rows in _Y_.

* * *

cmod
----

**Output:** matrix



Returns an _m_ x _n_ real matrix holding the complex modulus of each element of the _m_ x _n_ complex matrix _C_. The modulus of the complex number _z_ = _x_ + _yi_ equals the square root of _x_2 + _y_2.

See also abs, carg.

* * *

cmult
-----

**Output:** matrix


|Arguments:|X (matrix)|
|----------|----------|
|          |Y (matrix)|


This is a legacy function, predating gretl's native support for complex matrices.

Complex multiplication. The two arguments must have the same number of rows, _n_, and either one or two columns. The first column contains the real part and the second (if present) the imaginary part. The return value is an _n_ x 2 matrix, or, if the result has no imaginary part, an _n_\-vector. See also cdiv.

* * *

cnorm
-----

**Output:** same type as input



Returns the cumulative distribution function for a standard normal. See also dnorm, qnorm.

* * *

cnumber
-------

**Output:** scalar

Returns the condition number of the _n_ x _k_ matrix _X_, as defined in Belsley, Kuh and Welsch (1980). If the columns of _X_ are mutually orthogonal the condition number of _X_ is unity. Conversely, a large value of the condition number is an indicator of multicollinearity; "large" is often taken to mean 50 or greater (sometimes 30 or greater).

The steps in the calculation are: (1) form a matrix _Z_ whose columns are the columns of _X_ divided by their respective Euclidean norms; (2) form _Z'Z_ and obtain its eigenvalues; and (3) compute the square root of the ratio of the largest to the smallest eigenvalue.

See also rcond.

* * *

cnameget
--------

**Output:** string or array of strings


|Arguments:|M (matrix)             |
|----------|-----------------------|
|          |col (integer, optional)|


If the _col_ argument is given, retrieves the name for column _col_ of matrix _M_. If _M_ has no column names attached the value returned is an empty string; if _col_ is out of bounds for the given matrix an error is flagged.

If no second argument is given, retrieves an array of strings holding the column names from _M_, or an empty array if _M_ does not have column names attached.

Example:

```
	  matrix A = { 11, 23, 13 ; 54, 15, 46 }
	  cnameset(A, "Col_A Col_B Col_C")
	  string name = cnameget(A, 3)
	  print name
```


See also cnameset.

* * *

cnameset
--------

**Output:** scalar


|Arguments:|M (matrix)                  |
|----------|----------------------------|
|          |S (array of strings or list)|


Attaches names to the columns of the _T_ x _k_ matrix _M_. If _S_ is a named list, the names are taken from the names of the listed series; the list must have _k_ members. If _S_ is an array of strings, it should contain _k_ elements. A single string is also acceptable as the second argument; in that case it should contain _k_ space-separated substrings. As a special case, passing an empty string as the second argument has the effect of removing any existing column names.

The nominal return value is 0 on successful completion; in case of failure an error is flagged. See also rnameset.

Example:

```
	  matrix M = {1, 2; 2, 1; 4, 1}
	  strings S = array(2)
	  S[1] = "Col1"
	  S[2] = "Col2"
	  cnameset(M, S)
	  print M
```


* * *

cols
----

**Output:** integer

Returns the number of columns of _X_. See also mshape, rows, unvech, vec, vech.

* * *

commute
-------

**Output:** matrix


|Arguments:|A (matrix)                |
|----------|--------------------------|
|          |m (integer)               |
|          |n (integer, optional)     |
|          |post (integer, optional)  |
|          |add_id (integer, optional)|


Returns the matrix _A_ premultiplied by the commutation matrix _K_m,n (using an algorithm that is more efficient than explicit multiplication). Each column of _A_ is assumed to come from a vec operation on a _m x n_ matrix. In particular,

```
	  commute(vec(B), rows(B), cols(B))
```


gives vec(_B'_). In order to compute the commutation matrix proper, just apply the function to an appropriately sized identity matrix. For example:

```
	  K_32 = commute(I(6), 3, 2)
```


The optional argument _n_ defaults to _m_. If the optional argument _post_ is non-zero, then post-multiplication is performed instead of pre-multiplication; the optional Boolean switch _add\_id_ will premultiply _A_ by _I + K_m,n instead of _K_m,n.

* * *

complex
-------

**Output:** complex matrix


|Arguments:|A (scalar or matrix)          |
|----------|------------------------------|
|          |B (scalar or matrix, optional)|


Returns a complex matrix, where _A_ is taken to supply the real part and _B_ the imaginary part. If _A_ is _m_ x _n_ and _B_ is a scalar the result is _m_ x _n_ with a constant imaginary part—and similarly in the converse case but with a constant real part. If both arguments are matrices they must be of the same dimensions. If the second argument is omitted the imaginary part defaults to zero. See also cswitch.

* * *

conj
----

**Output:** complex matrix



Returns an _m_ x _n_ complex matrix holding the complex conjugate of each element of the _m_ x _n_ complex matrix _C_. The conjugate of the complex number _z_ = _x_ + _yi_ equals _x_ – _yi_.

See also carg, abs.

* * *

contains
--------

**Output:** same type as input


|Arguments:|x (scalar, series or matrix)|
|----------|----------------------------|
|          |S (matrix)                  |


Provides a means of determining whether the numerical object _x_ contains any of the elements of _S_, a matrix which plays the role of a set.

The return value is an object of the same size as _x_ containing 1s in positions where a value of _x_ matches any element of _S_ and zeros elsewhere. For example, the code

```
	  matrix A = mshape(seq(1,9), 3, 3)
	  matrix C = contains(A, {1, 5, 9})
```


gives

```
	  A (3 x 3)

	  1   4   7
	  2   5   8
	  3   6   9

	  C (3 x 3)

	  1   0   0
	  0   1   0
	  0   0   1
```


This function may be particularly useful when _x_ is a series that contains a fine-grained encoding for a qualitative characteristic, and you wish to reduce this to a smaller number of categories. You can pack into _S_ a set of values to be consolidated, and obtain a dummy variable with value 1 for observations matching this set, 0 otherwise.

Since _S_ serves as a set, for greatest efficiency it should be a vector with no repeated values, however an arbitrary matrix is accepted.

* * *

conv2d
------

**Output:** matrix


|Arguments:|A (matrix)|
|----------|----------|
|          |B (matrix)|


Computes the 2-dimensional convolution of the matrices _A_ and _B_. If _A_ is _r_ x _c_ and _B_ is _m_ x _n_ then the returned matrix will have _r+m-1_ rows and _c+n-1_ columns.

See also fft, filter.

* * *

cquad
-----

**Output:** matrix

Given an _m_ x _n_ complex matrix _Z_, returns an _m_ x _n_ real matrix holding the quadrance of the elements of _Z_. The quadrance of the complex number _z_ = _a_ + _bi_ is _a_2 + _b_2. It therefore equals the squared modulus of _z_ and also equals _z_ multiplied by its complex conjugate, but the direct calculation carried out by cquad is considerably faster than either of the alternative approaches.

* * *

corr
----

**Output:** scalar


|Arguments:|y1 (series or vector)|
|----------|---------------------|
|          |y2 (series or vector)|


Computes the correlation coefficient between _y1_ and _y2_. The arguments should be either two series, or two vectors of the same length. See also cov, mcov, mcorr, npcorr.

* * *

corresp
-------

**Output:** scalar


|Arguments:|a (series or vector)|
|----------|--------------------|
|          |b (series or vector)|


On the basis of a cross-tabulation of _a_ and _b_, returns an integer code indicating the sort of correspondence between the two variables, as follows.

*   Code = 2: there’s a 1-to-1 relationship.
    
*   Code = 1: there’s a 1-to-n relationship (_a_ "nests" _b_, can be interpreted as a function of _b_ in the mathematical sense).
    
*   Code = –1: there’s an n-to-1 relationship (_b_ "nests" _a_, can be interpreted as a function of _a_).
    
*   Code = 0: there’s no relationship.
    

Note that these codes are based solely on the sample values of the two arguments. In case _b_ is the square of _a_, for example, the result will differ depending on whether _a_ contains some pairs of values that differ only by sign (code = –1), or not (code = 2).

One possible use case is to check whether two discrete series encode the same information. For example, the following:

```
	  open grunfeld.gdt
	  c = corresp($unit, firm)
```


gives c = 2, indicating that the series firm is in fact a unique identifier for the cross-sectional units in this panel dataset.

See also mxtab.

* * *

corrgm
------

**Output:** matrix


|Arguments:|x (series, matrix or list)    |
|----------|------------------------------|
|          |p (integer)                   |
|          |y (series or vector, optional)|


If only the first two arguments are given, computes the correlogram for _x_ for lags 1 to _p_. Let _k_ represent the number of elements in _x_ (1 if _x_ is a series, the number of columns if _x_ is a matrix, or the number of list-members if _x_ is a list). The return value is a matrix with _p_ rows and 2_k_ columns, the first _k_ columns holding the respective autocorrelations and the remainder the respective partial autocorrelations.

If a third argument is given, this function computes the cross-correlogram for each of the _k_ elements in _x_ and _y_, from lead _p_ to lag _p_. The returned matrix has 2_p_ + 1 rows and _k_ columns. If _x_ is series or list and _y_ is a vector, the vector must have just as many rows as there are observations in the current sample range.

* * *

cos
---

**Output:** same type as input



Returns the cosine of _x_. See also sin, tan, atan.

* * *

cosh
----

**Output:** same type as input



Returns the hyperbolic cosine of _x_.

See also acosh, sinh, tanh.

* * *

cov
---

**Output:** scalar


|Arguments:|y1 (series or vector)|
|----------|---------------------|
|          |y2 (series or vector)|


Returns the covariance between _y1_ and _y2_. The arguments should be either two series, or two vectors of the same length. See also corr, mcov, mcorr.

* * *

critical
--------

**Output:** same type as input


|Arguments:|c (character)               |
|----------|----------------------------|
|          |... (see below)             |
|          |p (scalar, series or matrix)|


**Examples:** c1 = critical(t, 20, 0.025) c2 = critical(F, 4, 48, 0.05)

Critical value calculator. Returns _x_ such that _P(X > x) = p_, where the distribution _X_ is determined by the character _c_. Between the arguments _c_ and _p_, zero or more additional scalar arguments are required to specify the parameters of the distribution, as follows.

*   Standard normal (c = z, n, or N): no extra arguments
    
*   Student's t (t): degrees of freedom
    
*   Chi square (c, x, or X): degrees of freedom
    
*   Snedecor's F (f or F): df (num.); df (den.)
    
*   Binomial (b or B): probability; trials
    
*   Poisson (p or P): mean
    
*   Laplace (l or L): mean; scale
    
*   Standardized GED (E): shape
    

See also cdf, invcdf, pvalue.

* * *

cswitch
-------

**Output:** matrix


|Arguments:|A (matrix)   |
|----------|-------------|
|          |mode (scalar)|


Reinterprets a real matrix as holding complex values or vice versa. The precise action depends on _mode_ (which must have value 1, 2, 3 or 4) as follows:

mode 1: _A_ must be a real matrix with an even number of columns. Returns a complex matrix with half as many columns, the odd-numbered columns of _A_ supplying the real parts and the even-numbered columns the imaginary parts.

mode 2: Performs the inverse operation of mode 1. _A_ must be a complex matrix and the return value is a real matrix with twice as many columns as _A_.

mode 3: _A_ must be a real matrix with an even number of rows. Returns a complex matrix with half as many rows, the odd-numbered rows of _A_ supplying the real parts and the even-numbered rows the imaginary parts.

mode 4: Performs the inverse operation of mode 3. _A_ must be a complex matrix and the return value is a real matrix with twice as many rows as _A_.

See also complex.

* * *

ctrans
------

**Output:** complex matrix



Returns an _n_ x _m_ complex matrix holding the conjugate transpose of the _m_ x _n_ complex matrix _C_. The ' (prime) operator also performs conjugate transposition for complex matrices. The transp function can be used on complex matrices but it performs "straight" transposition (not conjugated).

* * *

cum
---

**Output:** same type as input



Cumulates _x_ (that is, creates a running sum). When _x_ is a series, produces a series _y_ each of whose elements is the sum of the values of _x_ to date; the starting point of the summation is the first non-missing observation in the currently selected sample. If any missing values are encountered in _x_, subsequent values of _y_ will be set to missing. When _x_ is a matrix, its elements are cumulated by columns.

In the case of panel data cumulation is in the time dimension, starting anew for each panel unit.

If you want cumulation to ignore missing values (that is, to treat them as if they were zeros), you can apply misszero to the argument, as in

```
	  series cx = cum(misszero(x))
```


See also diff.

* * *

curl
----

**Output:** integer



Provides a somewhat flexible means of obtaining a text buffer containing data from an internet server, using libcurl. On input the bundle _b_ must contain a string named URL which gives the full address of the resource on the target host. Other optional elements are as follows.

*   "header": a string specifying an HTTP header to be sent to the host.
    
*   "postdata": a string holding data to be sent to the host.
    

The header and postdata fields are intended for use with an HTTP POST request; if postdata is present the POST method is implicit, otherwise the GET method is implicit. (But note that for straightforward GET requests readfile offers a simpler interface.)

One other optional bundle element is recognized: if a scalar named include is present and has a non-zero value, this is taken as a request to include the header received from the host with the output body.

On completion of the request, the text received from the server is added to the bundle under the key "output".

If an error occurs in formulating the request (for example there's no URL on input) the function fails, otherwise it returns 0 if the request succeeds or non-zero if it fails, in which case the error message from the curl library is added to the bundle under the key "errmsg". Note, however, that "success" in this sense does not necessarily mean you got the data you wanted; all it means is that some response was received from the server. You must check the content of the output buffer (which may in fact be a message such as "Page not found").

Here is an example of use: downloading some data from the US Bureau of Labor Statistics site, which requires sending a JSON query. Note the use of sprintf to embed double-quotes in the POST data.

```
	  bundle req
	  req.URL = "http://api.bls.gov/publicAPI/v1/timeseries/data/"
	  req.include = 1
	  req.header = "Content-Type: application/json"
	  string s = sprintf("{\"seriesid\":[\"LEU0254555900\"]}")
	  req.postdata = s
	  err = curl(&req)
	  if err == 0
	      s = req.output
	      string line
	      loop while getline(s, &line)
	          printf "%s\n", line
	      endloop
	  endif
```


See also the functions jsonget and xmlget for means of processing JSON and XML data received, respectively.

* * *

dayspan
-------

**Output:** integer


|Arguments:|ed1 (integer)    |
|----------|-----------------|
|          |ed2 (integer)    |
|          |weeklen (integer)|


Returns the number of (relevant) days between the epoch days _ed1_ and _ed2_, inclusive. The _weeklen_, which must equal 5, 6 or 7, gives the number of days in the week that should be counted (a value of 6 omits Sundays, and a value of 5 omits both Saturdays and Sundays).

To obtain epoch days from the more familiar form of dates, see epochday. Related: see smplspan.

* * *

dec2bin
-------

**Output:** matrix

This function returns the binary representation of the numbers contained in the column vector _x_, by storing each binary digit into a column of the returned matrix, which always has 32 columns. Each element of _x_ must be an integer between 0 and _2_32_\-1_. Otherwise, an error is flagged.

Note that the least significant bit comes in the first column. So column 1 corresponds to _2_0, column 2 to _2_1, and so on. For example, the expression

```
	  matrix B = dec2bin(5)
```


produces a row vector full of zeros except for positions 1 and 3.

The bin2dec function performs the inverse transformation.

* * *

defarray
--------

**Output:** see below



Enables the definition of an array variable _in extenso_, by providing one or more elements. In using this function you must specify a type (in plural form) for the array: strings, matrices, bundles or lists. Each of the arguments must evaluate to an object of the specified type. On successful completion, the return value is an array of _n_ elements, where _n_ is the number of arguments.

```
	  strings S = defarray("foo", "bar", "baz")
	  matrices M = defarray(I(3), X'X, A*B, P[1:])
```


See also array.

* * *

defbundle
---------

**Output:** bundle



Enables the initialization of a bundle variable _in extenso_, by providing zero or more pairs of the form _key_, _member_. If we count the arguments from 1, every odd-numbered argument must evaluate to a string (key) and every even-numbered argument must evaluate to an object of a type that can be included in a bundle.

A couple of simple examples:

```
	  bundle b1 = defbundle("s", "Sample string", "m", I(3))
	  bundle b2 = defbundle("yn", normal(), "x", 5)
```


The first example creates a bundle with members a string and a matrix; the second, a bundle with a series member and a scalar member. Note that you cannot specify a type for each argument when using this function, so you must accept the "natural" type of the argument in question. If you wanted to add a series with constant value 5 to a bundle named b1 it would be necessary to do something like the following (after declaring b1):

```
	  series b1.s5 = 5
```


If no arguments are given to this function it is equivalent to creating an empty bundle (or to emptying an existing bundle of its content), as could also be done via

```
	  bundle b = null
```


### Variant syntax

Two alternative forms of syntax are available for defining bundles. In each case the keyword defbundle is replaced by a single underscore. In the first variant the comma-separated arguments take the form key=value, where the key is taken to be a literal string and does not require quotation. Here is an example:

```
	  bundle b = _(x=5, strval="some string", m=I(3))
```


This form is particularly convenient for constructing an anonymous bundle on the fly as a function argument, as in

```
	  b = regls(ys, LX, _(lfrac=0.35, stdize=0))
```


where the regls function takes an optional bundle argument holding various parameters.

The second variant is designed for the case where you wish to pack several pre-existing named objects into a bundle: you just give their names, unquoted:

```
	  bundle b = _(x, y, z)
```


Here the object x is copied into the bundle under the key "x", and similarly for y and z.

These alternative forms involve less typing than the full defbundle() version and are likely to be more convenient in many cases, but note that they are less flexible. Only the full version can handle keys given as string variables rather than literal strings.

* * *

deflist
-------

**Output:** list



Defines a list (of named series), given one or more suitable arguments. Each argument must be a named series (given by name or integer ID number), an existing named list, or an expression which evaluates to a list (including a vector which can be interpreted as a set of series ID numbers).

One point to note: this function simply concatenates its arguments to produce the list that it returns. If the intent is that the return value does not contain duplicates (does not reference any given series more than once), it is up to the caller to ensure that requirement is satisfied.

* * *

deseas
------

**Output:** series


|Arguments:|x (series)             |
|----------|-----------------------|
|          |opts (bundle, optional)|


The primary purpose of this function is to produce a deseasonalized version of the (quarterly or monthly) input series _x_, using X-13ARIMA-SEATS; it is available only if X-13ARIMA-SEATS is installed. If the second, optional argument is omitted, seasonal adjustment is carried out with all X-13ARIMA options at their default values (fully automatic procedure). When _opts_ is supplied, it may contain any of the following option specifications.

*   verbose: what to print? 0 = nothing (the default); 1 = confirmation of the options selected; 2 = confirmation of options plus the output from X-13ARIMA.
    
*   seats: 1 to use the SEATS algorithm in place of the default X11 algorithm for seasonal adjustment, or 0.
    
*   airline: 1 to use the "airline" ARIMA model specification (0,1,1)(0,1,1) in place of the default automatic model selection, or 0.
    
*   arima: can be used to impose a chosen ARIMA specification, in the form of a 6-vector holding small non-negative integers. These are given the (p,d,q,P,D,Q) interpretation, in traditional time-series notation: the first three terms represent the non-seasonal AR, Integration and MA orders, and the last three the seasonal counterparts. If both airline and arima are given, arima takes precedence.
    
*   outliers: enable detection and correction for outliers (choices 1 through 7), or 0 (the default) to omit this feature. The three available outlier types with their numerical codes are: 1 = additive outlier (ao), 2 = level shift (ls), 4 = temporary change (tc). To combine options you add the codes, for example 1 + 2 + 4 = 7 to activate all three. Note that the choice 3 = 1 + 2 (ao and ls) is the default within X-13ARIMA-SEATS, and is selected via the outlier tickbox in gretl's dialog window for seasonal adjustment via X13.
    
*   critical: a positive scalar, the critical value for defining outliers, the default being automatic, dependent on the sample size. Relevant only when outliers is specified.
    
*   logtrans: should the input series be put in log form? 0 = no, 1 = yes, 2 = automatically selected (the default). Note that it is not recommended to pass the input series in log form; if you want the log to be used, pass the "raw" level but specify logtrans=1.
    
*   trading\_days: should trading-day effects be included? 0 = no, 1 = yes, 2 = automatic (the default).
    
*   working\_days: a simpler version of trading\_days with a single distinction between weekdays and weekends rather than individual day effects. 0 = no (the default), 1 = yes, 2 = automatic. Use only one of trading\_days and working\_days.
    
*   easter: 1 to allow for an easter effect, as a supplement to either trading\_days or working\_days, or 0 (the default).
    
*   output: a string to select the type of the output series, "sa" for deseasonalized (the default), "trend" for the estimated trend, or "irreg" for the irregular component.
    
*   save\_spc: boolean flag, default 0; see below.
    

### Augmented results

In some cases one may wish to obtain all three of the results available from X-13ARIMA via a single call to deseas. This is supported as follows. Pass the _opts_ bundle in pointer form, and give the string "all" under the output key. The direct return value is then the seasonally adjusted series, but on successful completion _opts_ will contain a matrix named results with three columns: seasonally adjusted, trend and irregular. Here's an illustration (where the direct return value is discarded).

```
	  bundle b = _(output="all")
	  deseas(y, &b)
	  series y_dseas = b.results[,1]
	  series y_trend = b.results[,2]
	  series y_irreg = b.results[,3]
```


### Saving the X-13ARIMA specification

The save\_spc flag can be used to save the content of the X-13ARIMA input file written by gretl. The options bundle should be passed in pointer form and the specification (as a string) can be found under the key x13a\_spc. The following code illustrates saving this to file under the name myspec.spc in the user's working directory. (Note that the .spc extension is required by X-13ARIMA.)

```
	  bundle b = _(save_spc=1)
	  deseas(y, &b)
	  outfile myspec.spc
	     print b.x13a_spc
	  end outfile
```


* * *

det
---

**Output:** scalar



Returns the determinant of _A_, computed via the LU factorization. If what you actually want is the log determinant you should call ldet instead. See also rcond, cnumber.

* * *

diag
----

**Output:** matrix

Returns the principal diagonal of _X_ in a column vector. Note: if _X_ is an _m_ x _n_ matrix, the number of elements of the output vector is min(_m_, _n_). See also tr.

* * *

diagcat
-------

**Output:** matrix


|Arguments:|A (matrix)|
|----------|----------|
|          |B (matrix)|


Returns the direct sum of _A_ and _B_, that is a matrix holding _A_ in its north-west corner and _B_ in its south-east corner. If both _A_ and _B_ are square, the resulting matrix is block-diagonal.

* * *

diff
----

**Output:** same type as input



Computes first differences. If _y_ is a series, or a list of series, starting values are set to NA. If _y_ is a matrix, differencing is done by columns and starting values are set to 0.

When a list is returned, the individual variables are automatically named according to the template d\_ _varname_ where _varname_ is the name of the original series. The name is truncated if necessary, and may be adjusted in case of non-uniqueness in the set of names thus constructed.

See also cum, ldiff, sdiff.

* * *

digamma
-------

**Output:** same type as input



Returns the digamma (or Psi) function of _x_, that is the derivative of the log of the Gamma function.

See also lngamma, trigamma.

* * *

distance
--------

**Output:** matrix


|Arguments:|X (matrix)               |
|----------|-------------------------|
|          |metric (string, optional)|
|          |Y (matrix, optional)     |


Computes distances between points on a metric that can be euclidean (the default), manhattan, hamming, chebyshev, cosine or mahalanobis. The string identifying the metric can be given as an unambiguous truncation. The additional metrics correlation, standardized Euclidean are supported via simple transformations of the inputs; see below.

Each row of the _m_ x _n_ matrix _X_ is treated as a point in an _n_\-dimensional space; in an econometric context this is likely to represent a single observation comprising the values of _n_ variables.

### Standard cases

This section applies to all metrics except the Mahalanobis distance, for which the syntax is slightly different (see below).

If _Y_ is not given, the return value is a column vector of length _m_(_m_ – 1)/2 comprising the non-redundant subset of all pairwise distances between the _m_ points (rows of _X_). Given such a vector named d, the full symmetric matrix of inter-point distances (with zeros on the principal diagonal) can be constructed via

```
	  D = unvech(d, 0)
```


since d is akin to the vech of D, with diagonal elements omitted. The optional second argument to unvech says that the diagonal should be filled with zeros.

If _Y_ is given, it must be a _p_ x _n_ matrix, each row of which is again treated as a point in _n_\-space. In this case the return value is an _m_ x _p_ matrix whose _i,j_ element holds the distance between row _i_ of _X_ and row _j_ of _Y_.

To obtain the distances from a given reference point (for example, the centroid) to each of _n_ data-points, give _Y_ as a single row.

### Definitions of the supported metrics

*   euclidean: the square root of the sum of squared deviations in each of the dimensions.
    
*   manhattan: the sum of the absolute deviations in each of the dimensions.
    
*   hamming: the proportion of the dimensions in which the deviation is non-zero (so bounded by 0 and 1).
    
*   chebyshev: the greatest absolute deviation in any dimension.
    
*   cosine: 1 minus the cosine of the angle between the "points", considered as vectors.
    

### Mahalanobis distance

Mahalanobis distances are defined as the Euclidean distances between the points in question (rows of _X_) and a given centroid, scaled by the inverse of a covariance matrix. In the simplest case the centroid is constituted by the sample means of the variables (columns of _X_) and the covariance matrix is their sample covariance.

These can be obtained by supplying as second argument the string "mahalanobis" or any unambiguous abbreviation, as in

```
	  dmahal = distance(X, "mahal")
```


In this case the third argument _Y_ is not supported, and the return value is a column vector of length _m_ with the Mahalanobis distances from the centroid of _X_ (that is, its sample mean). In practice, the output matrix in this case is the same you get by executing the mahal command on a list of series corresponding to the columns of _X_.

To obtain Mahalanobis distances using a different centroid, mu, and/or inverse covariance matrix, ICV, the following syntax can be used:

```
	  dmahal = distance(X*cholesky(ICV), "euc", mu)
```


### Other metrics

Standardized Euclidean distances and correlation distances can be obtained as follows:

```
	  # standardized euclidean
	  dseu = distance(stdize(X), "eu")
	  # correlation (based on cosine)
	  dcor = distance(stdize(X', -1)', "cos")
```


* * *

dnorm
-----

**Output:** same type as input



Returns the density of the standard normal distribution at _x_. To get the density for a non-standard normal distribution at _x_, pass the _z_\-score of _x_ to the dnorm function and multiply the result by the Jacobian of the _z_ transformation, namely 1 over σ, as illustrated below:

```
	  mu = 100
	  sigma = 5
	  x = 109
	  fx = (1/sigma) * dnorm((x-mu)/sigma)
```


See also cnorm, qnorm.

* * *

dropcoll
--------

**Output:** list


|Arguments:|X (list)                  |
|----------|--------------------------|
|          |epsilon (scalar, optional)|


Returns a list with the same elements as _X_, but for the collinear series. Therefore, if all the series in _X_ are linearly independent, the output list is just a copy of _X_.

The algorithm uses the QR decomposition (Householder transformation), so it is subject to finite precision error. In order to gauge the sensitivity of the algorithm, a second optional parameter _epsilon_ may be specified to make the collinearity test more or less strict, as desired. The default value for _epsilon_ is 1.0e-8. Setting _epsilon_ to a larger value increases the probability of a series to be dropped.

Example:

```
	  nulldata 20
	  set seed 9876
	  series foo = normal()
	  series bar = normal()
	  series foobar = foo + bar
	  list X = foo bar foobar
	  list Y = dropcoll(X)
	  list print X
	  list print Y
	  # set epsilon to a ridiculously small value
	  list Y = dropcoll(X, 1.0e-30)
	  list print Y
```


produces

```
	  ? list print X
	  foo bar foobar
	  ? list print Y
	  foo bar
	  ? list Y = dropcoll(X, 1.0e-30)
	  Replaced list Y
	  ? list print Y
	  foo bar foobar
```


* * *

dsort
-----

**Output:** same type as input



Sorts _x_ in descending order, skipping observations with missing values when _x_ is a series. See also sort, values.

* * *

dummify
-------

**Output:** list


|Arguments:|x (series)                |
|----------|--------------------------|
|          |omitval (scalar, optional)|


The argument _x_ should be a discrete series. This function creates a set of dummy variables coding for the distinct values in the series. By default the smallest value is taken as the omitted category and is not explicitly represented.

The optional second argument represents the value of _x_ which should be treated as the omitted category. The effect when a single argument is given is equivalent to dummify(x, min(x)). To produce a full set of dummies, with no omitted category, use dummify(x, NA).

The generated variables are automatically named according to the template D_varname_\__i_ where _varname_ is the name of the original series and _i_ is a 1-based index. The original portion of the name is truncated if necessary, and may be adjusted in case of non-uniqueness in the set of names thus constructed.

* * *

easterday
---------

**Output:** same type as input



Given the year in argument _y_, returns the date of Easter on the Gregorian calendar as _month + day/100_. For example, in 2014 the date of Easter was April 20, which is represented under this convention as 4.2. (Note that April 2 would be returned as 4.02.) The following code shows how month and day can be extracted from the return value.

```
	  scalar e = easterday(2014)
	  scalar m = floor(e)
	  scalar d = round(100*(e-m))
```


* * *

ecdf
----

**Output:** matrix



Calculates the empirical CDF of _y_. This is returned in a matrix with two columns: the first holds the sorted unique values of _y_ and the second holds the cumulative relative frequency, that is the count of observations whose value is less than or equal to the value in the first column, divided by the total number of observations.

* * *

eigen
-----

**Output:** matrix


|Arguments:|A (square matrix)                |
|----------|---------------------------------|
|          |&V (reference to matrix, or null)|
|          |&W (reference to matrix, or null)|


Computes the eigenvalues, and optionally the right and/or left eigenvectors, of the _n_ x _n_ matrix _A_, which may be real or complex. The eigenvalues are returned in a complex column vector. To obtain the norm of the eigenvalues, you can use the abs function, which accepts complex arguments.

If you wish to retrieve the right eigenvectors (as an _n_ x _n_ complex matrix), supply the name of an existing matrix, preceded by & to indicate the "address" of the matrix in question, as the second argument. Otherwise this argument can be omitted.

To retrieve the left eigenvectors (again, as a complex matrix), supply a matrix-address as the third argument. Note that if you want the left eigenvectors but not the right ones, you should use the keyword null as a placeholder for the second argument.

See also eigensym, eigsolve, svd.

* * *

eigengen
--------

**Output:** matrix


|Arguments:|A (square matrix)                |
|----------|---------------------------------|
|          |&U (reference to matrix, or null)|


_This is a legacy function, predating gretl's native support for complex matrices. It should not be used in newly written hansl scripts. Use_ eigen _instead._

Computes the eigenvalues, and optionally the right eigenvectors, of the _n_ x _n_ matrix _A_. If all the eigenvalues are real an _n_ x 1 matrix is returned; otherwise the result is an _n_ x 2 matrix, the first column holding the real components and the second column the imaginary components. The eigenvalues are not guaranteed to be sorted in any particular order.

The second argument must be either the name of an existing matrix preceded by & (to indicate the "address" of the matrix in question), in which case an auxiliary result is written to that matrix, or the keyword null, in which case the auxiliary result is not produced.

If a non-null second argument is given, the specified matrix will be over-written with the auxiliary result. (It is not required that the existing matrix be of the right dimensions to receive the result.) The output is organized as follows:

*   If the _i_\-th eigenvalue is real, the _i_\-th column of _U_ will contain the corresponding eigenvector;
    
*   If the _i_\-th eigenvalue is complex, the _i_\-th column of _U_ will contain the real part of the corresponding eigenvector and the next column the imaginary part. The eigenvector for the conjugate eigenvalue is the conjugate of the eigenvector.
    

In other words, the eigenvectors are stored in the same order as the eigenvalues, but the real eigenvectors occupy one column, whereas complex eigenvectors take two (the real part comes first); the total number of columns is still _n_, because the conjugate eigenvector is skipped.

See also eigensym, eigsolve, qrdecomp, svd.

* * *

eigensym
--------

**Output:** matrix


|Arguments:|A (symmetric matrix)             |
|----------|---------------------------------|
|          |&U (reference to matrix, or null)|


Works mostly as eigen except that the argument _A_ must be symmetric (in which case less calculation is required), and the eigenvalues are returned in ascending order. If you want to get the eigenvalues in descending order (and have the eigenvectors reordered correspondingly) you can do the following:

```
	  matrix U
	  e = eigensym(A, &U)
	  Tmp = msortby((-e' | U)',1)'
	  e = -Tmp[1,]'
	  U = Tmp[2:,]
	  # now largest to smallest eigenvalues
	  print e U
```


Note: if you're interested in the eigen-decomposition of a matrix of the form _X'X_ it's preferable to compute the argument via the prime operator X'X rather than using the more general syntax X'\*X. The former expression uses a specialized algorithm which offers greater computational efficiency as well as ensuring that the result is exactly symmetric.

* * *

eigsolve
--------

**Output:** matrix


|Arguments:|A (symmetric matrix)             |
|----------|---------------------------------|
|          |B (symmetric matrix)             |
|          |&U (reference to matrix, or null)|


Solves the generalized eigenvalue problem |_A_ – λ_B_| = 0, where both _A_ and _B_ are symmetric and _B_ is positive definite. The eigenvalues are returned directly, arranged in ascending order. If the optional third argument is given it should be the name of an existing matrix preceded by &; in that case the generalized eigenvectors are written to the named matrix.

* * *

epochday
--------

**Output:** scalar or series


|Arguments:|year (scalar or series) |
|----------|------------------------|
|          |month (scalar or series)|
|          |day (scalar or series)  |


Returns the number of the day in the current epoch specified by year, month and day. The epoch day equals 1 for the first of January in the year 1 AD on the proleptic Gregorian calendar; it stood at 733786 on 2010-01-01. If any of the arguments are given as series the value returned is a series, otherwise it is a scalar.

By default the _year_, _month_ and _day_ values are assumed to be given relative to the Gregorian calendar, but if the year is a negative value the interpretation switches to the Julian calendar.

An alternative call is also supported: if a single argument is given, it is taken to be a date (or series of dates) in ISO 8601 "basic" numeric format, YYYYMMDD. So the following two calls produce the same result, namely 700115.

```
	  eval epochday(1917, 11, 7)
	  eval epochday(19171107)
```


For the inverse function, see isodate and also (for the Julian calendar) juldate. For another means of converting dates to epoch days see strpday.

* * *

errmsg
------

**Output:** string



Retrieves the gretl error message associated with _errno_. See also $error.

* * *

errorif
-------

**Output:** scalar


|Arguments:|condition (boolean)|
|----------|-------------------|
|          |msg (string)       |


Applicable only in the context of a user-defined function, or within an mpi block. If _condition_ evaluates as non-zero, it causes execution of the current function to terminate with an error condition flagged; the _msg_ argument is then printed as part of the message shown to the caller of the function in question.

The return value from this function (1) is purely nominal.

* * *

exists
------

**Output:** integer

Returns non-zero if _name_, which should be valid as a gretl identifier, names a currently defined object, be it a scalar, a series, a matrix, list, string, bundle or array; otherwise returns 0.

Intended usage is for the case where a user-defined function has an optional parameter with a null default. The function writer can use exists(), passing the parameter name, to check whether or not the caller supplied an argument. But please note, lists are an exception in this respect: if a list parameter has a null default and the caller doesn't supply an argument, the function gets an empty list rather than no list; therefore exists will always return non-zero. To check for emptiness of a list argument, use nelem.

For related checks, see typeof and inbundle.

* * *

exp
---

**Output:** same type as input



Returns _e_x. Note that in case of matrix input the function acts element by element. For the matrix exponential function, see mexp.

* * *

fcstats
-------

**Output:** matrix


|Arguments:|y (series or vector)      |
|----------|--------------------------|
|          |f (series, list or matrix)|
|          |U2 (boolean, optional)    |


Produces a matrix holding several statistics which serve to evaluate _f_ as a forecast of the observed data _y_.

If _f_ is a series or vector the output is a column vector; if _f_ is a list with _k_ members or a _T_ x _k_ matrix the output has _k_ columns, each of which holds statistics for the corresponding element (series or column) of the input as a forecast of _y_.

In all cases the "vertical" dimension of the input (for a series or list the length of the current sample range, for a matrix the number of rows) must match across the two arguments.

The rows of the returned matrix are as follows:

```
	  1  Mean Error (ME)
	  2  Root Mean Squared Error (RMSE)
	  3  Mean Absolute Error (MAE)
	  4  Mean Percentage Error (MPE)
	  5  Mean Absolute Percentage Error (MAPE)
	  6  Theil's U (U1 or U2)
	  7  Bias proportion, UM
	  8  Regression proportion, UR
	  9  Disturbance proportion, UD
```


The variant of Theil's U shown by default depends on the nature of the data: if they are known to be time series then U2 is shown, otherwise U1 is produced. But this choice can be forced via the optional trailing argument: give a non-zero value to force U2, or zero to force U1.

For details on the calculation of these statistics, and the interpretation of the _U_ values, please see chapter 35 of the Gretl User's Guide.

* * *

fdjac
-----

**Output:** matrix


|Arguments:|b (column vector)    |
|----------|---------------------|
|          |fcall (function call)|
|          |h (scalar, optional) |


Calculates a numerical approximation to the Jacobian associated with the _n_\-vector _b_ and the transformation function specified by the argument _fcall_. The function call should take _b_ as its first argument (either straight or in pointer form), followed by any additional arguments that may be needed, and it should return an _m_ x 1 matrix. On successful completion fdjac returns an _m_ x _n_ matrix holding the Jacobian.

The optional third argument can be used to set the step size _h_ used in the approximation mechanism (see below); if this argument is omitted the step size is determined automatically.

Here is an example of usage:

```
	  matrix J = fdjac(theta, myfunc(&theta, X))
```


The function can use three different methods: simple forward-difference, bilateral difference or 4-nodes Richardson extrapolation. Respectively:

_J_0 = _(f(x+h) - f(x))/h_

_J_1 = _(f(x+h) - f(x-h))/2h_

_J_2 = _\[8(f(x+h) - f(x-h)) - (f(x+2h) - f(x-2h))\] /12h_

The three alternatives above provide, generally, a trade-off between accuracy and speed. You can choose among methods via the set command: specify a value of 0, 1 or 2 for the fdjac\_quality variable. The default is 0.

For more details and examples chapter 37 of the Gretl User's Guide.

See also BFGSmax, numhess, set.

* * *

feval
-----

**Output:** see below


|Arguments:|funcname (string)|
|----------|-----------------|
|          |... (see below)  |


Primarily useful for writers of functions. The first argument should be the name of a function; the remaining arguments will be passed to the specified function. This permits treating the function identified by _funcname_ as itself a variable. The return value is whatever the named function returns given the specified arguments.

The example below illustrates some possible uses.

```
	  function scalar utility (scalar c, scalar sigma)
	      return (c^(1-sigma)-1)/(1-sigma)
	  end function

	  strings S = defarray("log", "utility")

	  # call a 1-argument built-in function
	  x = feval(S[1], 2.5)
	  # call a user-defined function
	  x = feval(S[2], 5, 0.5)
	  # a 2-argument built-in function
	  func = "zeros"
	  m = feval(func, 5-2, sqrt(4))
	  print m
	  # a 3-argument built-in
	  x = feval("monthlen", 12, 1980, 5)
```


There's a weak analogy between feval and genseries: both functions render variable a syntactic element that is usually fixed at the time a script is composed.

See also fevalb.

* * *

fevalb
------

**Output:** see below


|Arguments:|funcname (string)|
|----------|-----------------|
|          |b (bundle)       |


This is a variant of feval which meets a case that may be encountered by function writers, where the number and types of the arguments to be passed to the named function are not known in advance. Instead of the arguments being passed individually, they are passed as members of the bundle argument _b_.

Since the order of the members in a gretl bundle is indeterminate, some mechanism is required to ensure that they are passed to the function in question in the right order. This is automatically ensured if the lexicographic order of the keys in the bundle gives the argument order. For examples, the keys could be arg1, arg2 and so on (or arg01, arg02 and so on in the unlikely event that the function takes more than nine arguments). Alternatively, the bundle may contain an array of strings under the reserved key arglist. This array must hold exactly the keys in _b_, except for arglist itself, in the desired order.

The examples below illustrate both approaches, as applied to the monthlen function.

```
	  # using lexicographic order
	  bundle b = _(arg1=12, arg2=1980, arg3=5)
	  n = feval("monthlen", b)

	  # using arglist
	  bundle b = _(month=12, year=1980, wkdays=5)
	  b.arglist = defarray("month", "year", "wkdays")
	  n = feval("monthlen", b)
```


See also feval.

* * *

fevd
----

**Output:** matrix


|Arguments:|target (integer)      |
|----------|----------------------|
|          |shock (integer)       |
|          |sys (bundle, optional)|


This function provides a more flexible alternative to the accessor $fevd for obtaining a forecast error variance decomposition (FEVD) matrix following estimation of a VAR or VECM. Without the final optional argument, it is available only when the last model estimated was a VAR or VECM. Alternatively, information on such a system can be stored in a bundle via the $system accessor and subsequently passed to fevd.

The _target_ and _shock_ arguments take the form of 1-based indices of the endogenous variables in the system, with 0 taken to mean "all". The following code fragment illustrates usage. In the first example the matrix fe1 holds the shares of the FEVD for y1 due to each of y1, y2 and y3 (the rows therefore summing to 1). In the second, fe2 holds the contribution of y2 to the forecast error variance of all three variables (so the rows do not sum to 1). In the third case the return value is a column vector showing the "own share" of the FEVD for y1.

```
	  var 4 y1 y2 y3
	  bundle vb = $system
	  matrix fe1 = fevd(1, 0, vb)
	  matrix fe2 = fevd(0, 2, vb)
	  matrix fe3 = fevd(1, 1, vb)
```


The number of periods (rows) over which the decomposition is traced is determined automatically based on the frequency of the data, but this can be overridden via the horizon argument to the set command, as in set horizon 10.

See also irf.

* * *

fft
---

**Output:** matrix

Discrete Fourier transform. The input matrix _X_ may be real or complex. The output is a complex matrix of the same dimensions as _X_.

Should it be necessary to compute the Fourier transform on several vectors with the same number of elements, it is more efficient to group them into a matrix rather than invoking fft for each vector separately. See also ffti.

* * *

ffti
----

**Output:** matrix

Inverse discrete Fourier transform. It is assumed that _X_ contains _n_ complex column vectors. A matrix with _n_ columns is returned.

Should it be necessary to compute the inverse Fourier transform on several vectors with the same number of elements, it is more efficient to group them into a matrix rather than invoking ffti for each vector separately. See also fft.

* * *

filter
------

**Output:** see below


|Arguments:|x (series or matrix)           |
|----------|-------------------------------|
|          |a (scalar or vector, optional) |
|          |b (scalar or vector, optional) |
|          |y0 (scalar, optional)          |
|          |x0 (scalar or vector, optional)|


Computes an ARMA-like filtering of the argument _x_. The transformation can be written as

_y_t = _a_0 _x_t + _a_1 _x_t-1 + ... _a_q _x_t-q + _b_1 _y_t-1 + ... _b_p_y_t-p

If argument _x_ is a series, the result will be itself a series. Otherwise, if _x_ is a matrix with _T_ rows and _k_ columns, the result will be a matrix of the same size, in which the filtering is performed column by column.

The two arguments _a_ and _b_ are optional. They may be scalars, vectors or the keyword null.

If _a_ is a scalar, this is used as _a_0 and implies _q=0_; if it is a vector of _q+1_ elements, they contain the coefficients from _a_0 to _a_q. If _a_ is null or omitted, this is equivalent to setting _a_0 _\=1_ and _q=0_.

If _b_ is a scalar, this is used as _b_1 and implies _p=1_; if it is a vector of _p_ elements, they contain the coefficients from _b_1 to _b_p. If _b_ is null or omitted, this is equivalent to setting _B(L)=1_.

The optional scalar argument _y0_ is taken to represent all values of _y_ prior to the beginning of sample (used only when _p > 0_). If omitted, it is understood to be 0. Similarly, the optional argument _x0_ may be used to specify one or more pre-sample values of _x_, information that is relevant only when _q > 0_. Otherwise pre-sample values of _x_ are assumed to be zero.

See also bkfilt, bwfilt, fracdiff, hpfilt, movavg, varsimul.

Example:

```
	  nulldata 5
	  y = filter(index, 0.5, -0.9, 1)
	  print index y --byobs
	  x = seq(1,5)' ~ (1 | zeros(4,1))
	  w = filter(x, 0.5, -0.9, 1)
	  print x w
```


produces

```
          index            y

          1            1     -0.40000
          2            2      1.36000
          3            3      0.27600
          4            4      1.75160
          5            5      0.92356

          x (5 x 2)

          1   1
          2   0
          3   0
          4   0
          5   0

          w (5 x 2)

          -0.40000     -0.40000
           1.3600       0.36000
           0.27600     -0.32400
           1.7516       0.29160
           0.92356     -0.26244
```


* * *

firstobs
--------

**Output:** integer


|Arguments:|y (series)                  |
|----------|----------------------------|
|          |insample (boolean, optional)|


Returns the 1-based index of the first non-missing observation for the series _y_. By default the whole data range is examined, so if subsampling is in effect the value returned may be smaller than the accessor $t1. But if a non-zero value is given for _insample_ only the current sample range is considered. See also lastobs.

* * *

fixname
-------

**Output:** string


|Arguments:|rawname (string)              |
|----------|------------------------------|
|          |underscore (boolean, optional)|


Primarily intended for use in connection with the join command. Returns the result of converting _rawname_ to a valid gretl identifier, which must start with a letter, contain nothing but (ASCII) letters, digits and the underscore character, and must not exceed 31 characters. The rules used in conversion are:

1\. Skip any leading non-letters.

2\. Until the 31-character limit is reached or the input is exhausted: transcribe "legal" characters; skip "illegal" characters apart from spaces; and replace one or more consecutive spaces with an underscore, unless the previous character transcribed is an underscore in which case space is skipped.

If you are confident that the input is not too long (and hence subject to truncation), you may wish to have sequences of one or more illegal characters replaced with an underscore rather than just being deleted; this may produce a more readable identifier. To get this effect, supply a nonzero value for the optional second argument. But this is not advisable in the context of the join command, since the automatically "fixed" name will not use underscores in this way.

* * *

flatten
-------

**Output:** see below


|Arguments:|A (array of matrices or strings) |
|----------|---------------------------------|
|          |alt (integer or string, optional)|


"Flattens" either an array of matrices into a single matrix or an array of strings into a single string.

### Matrices

In the matrix case, the way the matrices in _A_ are joined together depends on the the _alt_ argument, which should have value 0 (horizontal), 1 (vertical) or 2 ("vec-wise"). The best way to explain the difference between the three alternatives is by example: the code

```
	  X = {1,3,5; 2,4,6}
	  A = defarray(X, X+6)
	  U = flatten(A,0) # = A[1] ~ A[2]
	  V = flatten(A,1) # = A[1] | A[2]
	  W = flatten(A,2) # = vec(A[1]) ~ vec(A[2])
```


produces the following three matrices:

```
	  U (2 x 6)

	  1    3    5    7    9   11 
	  2    4    6    8   10   12 

	  V (4 x 3)

	  1    3    5 
	  2    4    6 
	  7    9   11 
	  8   10   12 

	  W (6 x 2)

	  1    7 
	  2    8 
	  3    9 
	  4   10 
	  5   11 
	  6   12 
```


An error is flagged if the matrices in the array are not conformable for the operation. See msplitby for the inverse operation.

### Strings

In the string case the result holds the strings in _A_, arranged one per line by default. If a non-zero numerical value is given for _alt_ the strings are separated by spaces rather than newlines, but an alternative usage of _alt_ is supported: you may give a specific string to use as the separator. The inverse function for the string case is strsplit.

* * *

floor
-----

**Output:** same type as input



Returns the greatest integer less than or equal to _x_. Note: int and floor differ in their effect for negative arguments: int(-3.5) gives –3, while floor(-3.5) gives –4.

* * *

fracdiff
--------

**Output:** series


|Arguments:|y (series)|
|----------|----------|
|          |d (scalar)|


Returns the fractional difference of order _d_ for the series _y_.

Note that in theory fractional differentiation is an infinitely long filter. In practice, presample values of _y_t are assumed to be zero.

A negative value of _d_ can be given, in which case fractional integration is performed.

* * *

fzero
-----

**Output:** scalar


|Arguments:|fcall (function call)            |
|----------|---------------------------------|
|          |init (scalar or vector, optional)|
|          |toler (scalar, optional)         |


Attempts to find a single root of a continuous (typically nonlinear) function _f_—that is, a value of the scalar variable _x_ such that _f_(_x_) = 0. The _fcall_ argument should provide a call to the function in question; _fcall_ may include an arbitrary number of arguments but the first one must be the scalar playing the role of _x_. On successful completion the value of the root is returned.

The method used is that of Ridders (1979). This requires an initial bracket {_x_0, _x_1} such that both _x_ values lie in the domain of the function and the respective function values are of opposite sign. Best results are likely to be obtained if the user can supply, via the second argument, a 2-vector holding suitable end-points for the bracket. Failing that, one can supply a single scalar value and fzero will try to find a counterpart. If the second argument is omitted, _x_0 is initialized to a small positive value and we search for a suitable _x_1.

The optional _toler_ argument can be used to adjust the maximum acceptable absolute difference of _f_(_x_) from zero, the default being 1.0e–14.

By default this function operates silently, but the progress of the iterative method can be exposed by executing the command "set max\_verbose on" before calling fzero.

Some simple examples follow.

```
	  # Approximate pi by finding a zero for sin() in the
	  # bracket 2.8 to 3.2
	  x = fzero(sin(x), {2.8, 3.2})
	  printf "\nx = %.12f vs pi = %.12f\n\n", x, $pi

	  # Approximate the 'Omega constant' starting from x = 0.5
	  function scalar f(scalar x)
	      return log(x) + x
	  end function
	  x = fzero(f(x), 0.5)
	  printf "x = %.12f f(x) = %.15f\n", x, f(x)
```


* * *

gammafun
--------

**Output:** same type as input



Returns the gamma function of _x_.

See also bincoeff and lngamma.

* * *

genseries
---------

**Output:** scalar


|Arguments:|varname (string)|
|----------|----------------|
|          |rhs (series)    |


Provides the script writer with a convenient means of generating series whose names are not known in advance, and/or creating a series and appending it to a list in a single operation.

The first argument gives the name of the series to create (or modify); this can be a string literal, a string variable, or an expression that evaluates to a string. The second argument, _rhs_ ("right-hand side"), defines the source series: this can be the name of an existing series or an expression that evaluates to a series, as would appear to the right of the equals sign when defining a series in the usual way.

The return value from this function is the ID number of the series in the dataset, a value suitable for inclusion in a list (or –1 on failure).

For example, suppose you want to add _n_ random normal series to the dataset and put them all into a named list. The following will do the job:

```
	  nulldata 10
	  list Normals = null
	  scalar n = 3
	  loop i = 1 .. n
	      Normals += genseries(sprintf("norm%d", i), normal())
	  endloop
```


On completion Normals will contain the series norm1, norm2 and norm3 .

Those who find genseries useful may also like to explore feval.

* * *

geoplot
-------

**Output:** none


|Arguments:|mapfile (string)          |
|----------|--------------------------|
|          |payload (series, optional)|
|          |options (bundle, optional)|


Calls for production of a map, when suitable geographical data are present. In most cases the _mapfile_ argument should be given as $mapfile, an accessor that retrieves the name of the relevant GeoJSON file or ESRI shapefile. The optional _payload_ argument is used to give the name of a series with which to colorize the regions of the map. And the final bundle argument enables you to set numerous options.

See the geoplot documentation, geoplot.pdf, for full details and examples. This explains all the settings configurable via the _options_ argument.

* * *

getenv
------

**Output:** string

If an environment variable by the name of _s_ is defined, returns the string value of that variable, otherwise returns an empty string. See also ngetenv.

* * *

getinfo
-------

**Output:** bundle

Returns information on the specified series, which may be given by name or ID number. The returned bundle contains all the attributes which can be set via the setinfo command. It also contains additional information relevant for series that have been created as transformations of primary data (lags, logs, etc.): this includes the gretl command word for the transformation under the key "transform" and the name of the associated primary series under "parent". For lagged series, the specific lag number can be found under the key "lag".

Here is an example of usage:

```
	  open data9-7
	  lags QNC
	  bundle b = getinfo(QNC_2)
	  print b
```


On executing the above we see:

```
	  has_string_table = 0
	  lag = 2
	  parent = QNC
	  name = QNC_2
	  graph_name =
	  coded = 0
	  discrete = 0
	  transform = lags
	  description = = QNC(t - 2)
```


To test whether series 5 in a dataset is a lagged term one can do this sort of thing:

```
	  if getinfo(5).lag != 0
	     printf "series 5 is a lag of %s\n", getinfo(5).parent
	  endif
```


Note that the dot notation to access bundle members can be used even when the bundle is "anonymous" (not saved under its own name).

* * *

getkeys
-------

**Output:** array of strings

Returns an array of strings holding the keys identifying the contents of _b_. If the bundle is empty an empty array is returned.

* * *

getline
-------

**Output:** scalar


|Arguments:|source (string)              |
|----------|-----------------------------|
|          |&target (reference to string)|


This function is used to read successive lines from _source_, which should be a named string variable. On each call a line from the source is written to _target_ (which must also be a named string variable, given in pointer form), with the newline character stripped off. The valued returned is 1 if there was anything to be read (including blank lines), 0 if the source has been exhausted.

Here is an example in which the content of a text file is broken into lines:

```
	  string s = readfile("data.txt")
	  string line
	  scalar i = 1
	  loop while getline(s, &line)
	      printf "line %d = '%s'\n", i++, line
	  endloop
```


In this example we can be sure that the source is exhausted when the loop terminates. If the source might not be exhausted you should follow your regular call(s) to getline with a "clean up" call, in which _target_ is replaced by null (or omitted altogether) as in

```
	  getline(s, &line) # get a single line
	  getline(s, null) # clean up
```


Note that although the reading position advances at each call to getline, _source_ is not modified by this function, only _target_.

* * *

ghk
---

**Output:** matrix


|Arguments:|C (matrix)                        |
|----------|----------------------------------|
|          |A (matrix)                        |
|          |B (matrix)                        |
|          |U (matrix)                        |
|          |&dP (reference to matrix, or null)|


Computes the GHK (Geweke, Hajivassiliou, Keane) approximation to the multivariate normal distribution function; see for example Geweke (1991). The value returned is an _n_ x 1 vector of probabilities.

The argument _C_ (_m_ x _m_) should give the Cholesky factor (lower triangular) of the covariance matrix of _m_ normal variates. The arguments _A_ and _B_ should both be _n_ x _m_, giving respectively the lower and upper bounds applying to the variates at each of _n_ observations. Where variates are unbounded, this should be indicated using the built-in constant $huge or its negative.

The matrix _U_ should be _m_ x _r_, with _r_ the number of pseudo-random draws from the uniform distribution; suitable functions for creating _U_ are muniform and halton.

We illustrate below with a relatively simple case where the multivariate probabilities can be calculated analytically. The series P and Q should be numerically very similar to one another, P being the "true" probability and Q its GHK approximation:

```
	  nulldata 20
	  series inf1 = -2*uniform()
	  series sup1 = 2*uniform()
	  series inf2 = -2*uniform()
	  series sup2 = 2*uniform()

	  scalar rho = 0.25
	  matrix V = {1, rho; rho, 1}

	  series P = cdf(D, rho, inf1, inf2) - cdf(D, rho, sup1, inf2) \
	  - cdf(D, rho, inf1, sup2) + cdf(D, rho, sup1, sup2)

	  C = cholesky(V)
	  U = halton(2, 100)

	  series Q = ghk(C, {inf1, inf2}, {sup1, sup2}, U)
```


The optional _dP_ argument can be used to retrieve the _n_ x _k_ matrix of analytical derivatives of the probabilities, where _k_ equals 2_m_ + _m_(_m_ + 1)/2. The first _m_ columns hold the derivatives with respect to the lower bounds, the next _m_ those with respect to the upper bounds, and the remainder the derivatives with respect to the unique elements of the _C_ matrix in "vech" order.

* * *

gini
----

**Output:** scalar



Returns Gini's inequality index for the (non-negative) series or vector _y_. A Gini value of zero indicates perfect equality. The maximum Gini value for a series with _n_ members is (_n_ – 1)/_n_, occurring when only one member has a positive value; a Gini of 1.0 is therefore the limit approached by a large series with maximal inequality.

* * *

ginv
----

**Output:** matrix


|Arguments:|A (matrix)            |
|----------|----------------------|
|          |tol (scalar, optional)|


Returns _A_+, the Moore–Penrose or generalized inverse of the _r_ x _c_ matrix _A_, computed via the singular value decomposition.

The result of this operation depends on the number of singular values of _A_ that are found to be numerically 0. The _tol_ optional parameter can be used for tweaking this aspect. Singular values are considered to be 0 if they are less than _m × tol × s_, where _m_ is the greater of _r_ and _c_ and _s_ is the largest singular value. If the second argument is omitted _tol_ is set to machine epsilon (see $macheps). In some cases, you may want to set _tol_ to a larger value (eg 1.0e-9) in order to avoid overestimating the rank of _A_, which may lead to numerically unstable results.

This matrix has the properties _A_ _A_+ _A_ = _A_ and _A_+ _A_ _A_+ = _A_+. Moreover, the products _A_ _A_+ and _A_+ _A_ are symmetric by construction.

See also inv, svd.

* * *

GSSmax
------

**Output:** scalar


|Arguments:|&b (reference to matrix)|
|----------|------------------------|
|          |f (function call)       |
|          |toler (scalar, optional)|


One-dimensional maximization via the Golden Section Search method. The matrix _b_ should be a 3-vector. On input the first element is ignored while the second and third elements set the lower and upper bounds on the search. The _fncall_ argument should specify a call to a function that returns the value of the maximand; element 1 of _b_, which will hold the current value of the adjustable parameter when the function is called, should be given as its first argument; any other required arguments may then follow. The function in question should be unimodal (should have no local maxima other than the global maximum) over the stipulated range, or GSS is not sure to find the maximum.

On successful completion GSSmax returns the optimum value of the maximand, while _b_ holds the optimal parameter value along with the limits of its bracket.

The optional third argument may be used to set the tolerance for convergence, that is, the maximum acceptable width of the final bracket for the parameter. If this argument is not given a value of 0.0001 is used.

If the object is in fact minimization, either the function call should return the negative of the criterion or alternatively GSSmax may be called under the alias GSSmin.

Here is a simple example of usage:

```
	  function scalar trigfunc (scalar theta)
	      return 4 * sin(theta) * (1 + cos(theta))
	  end function

	  matrix m = {0, 0, $pi/2}
	  eval GSSmax(&m, trigfunc(m[1]))
	  printf "\n%10.7f", m
```


* * *

GSSmin
------

**Output:** scalar

An alias for GSSmax; if called under this name the function acts as a minimizer.

* * *

halton
------

**Output:** matrix


|Arguments:|m (integer)               |
|----------|--------------------------|
|          |r (integer)               |
|          |offset (integer, optional)|


Returns an _m_ x _r_ matrix containing _m_ Halton sequences of length _r_. The sequences are constructed using the first _m_ primes. By default the first 10 elements of each sequence are discarded, but this figure can be adjusted via the optional _offset_ argument, which should be a non-negative integer. See Halton and Smith (1964).

* * *

hdprod
------

**Output:** matrix


|Arguments:|X (matrix)          |
|----------|--------------------|
|          |Y (matrix, optional)|


Horizontal direct product. The two arguments must have the same number of rows, _r_. The return value is a matrix with _r_ rows, in which the _i_\-th row is the Kronecker product of the corresponding rows of _X_ and _Y_. If _Y_ is omitted, the "shorthand" syntax applies (see below).

If _X_ is an _r x k_ matrix and _Y_ is an _r x m_ matrix, the result will be a matrix with _r_ rows and _km_ columns.

This operation is called "horizontal direct product" in conformity to its implementation in the GAUSS programming language. Its equivalent in standard matrix algebra would be called the row-wise Khatri-Rao product, or "face-splitting" product in the signal processing literature.

Example: the code

```
	  A = {1,2,3; 4,5,6}
	  B = {0,1; -1,1}
	  C = hdprod(A, B)
```


produces the following matrix:

```
          0    1    0    2    0    3
         -4    4   -5    5   -6    6
```


### Shorthand syntax

If _X_ and _Y_ are the same matrix, then each row of the result is the vectorization of a symmetric matrix. In these cases, the second argument may be omitted; however, the returned matrix will only contain the non-redundant columns, and will therefore have _k(k+1)/2_ columns. For example,

```
	  A = {1,2,3; 4,5,6}
	  C = hdprod(A)
```


produces

```
	  1    2    3    4    6    9
	  16   20   24   25   30   36
```


Note that the _i_\-th row of _C_ is _vech(a_i _a_i_')_, where _a_i is the _i_\-th row of _A_.

When using the shorthand syntax with complex matrices, the implicit second argument will be the _conjugate_ of the first one, so as to make each row of the result the symmetric vectorization of a Hermitian matrix.

* * *

hfdiff
------

**Output:** list


|Arguments:|hfvars (list)      |
|----------|-------------------|
|          |multiplier (scalar)|


Given a MIDAS list, produces a list of the same length holding high-frequency first differences. The second argument is optional and defaults to unity: it can be used to multiply the differences by some constant.

* * *

hfldiff
-------

**Output:** list


|Arguments:|hfvars (list)      |
|----------|-------------------|
|          |multiplier (scalar)|


Given a MIDAS list, produces a list of the same length holding high-frequency log-differences. The second argument is optional and defaults to unity: it can be used to multiply the differences by some constant, for example one might give a value of 100 to produce (approximate) percentage changes.

* * *

hflags
------

**Output:** list


|Arguments:|minlag (integer)|
|----------|----------------|
|          |maxlag (integer)|
|          |hfvars (list)   |


Given a MIDAS list, _hfvars_, produces a list holding high-frequency lags _minlag_ to _maxlag_. Use positive values for actual lags, negative for leads. For example, if _minlag_ is –3 and _maxlag_ is 5 then the returned list will hold 9 series: 3 leads, the contemporary value, and 5 lags.

Note that high-frequency lag 0 corresponds to the first high frequency period within a low frequency period, for example the first month of a quarter or the first day of a month.

* * *

hflist
------

**Output:** list


|Arguments:|x (vector)     |
|----------|---------------|
|          |m (integer)    |
|          |prefix (string)|


Produces from the vector _x_ a MIDAS list of _m_ series, where _m_ is the ratio of the frequency of observation for the variable in _x_ to the base frequency of the current dataset. The value of _m_ must be at least 3 and the length of _x_ must be _m_ times the length of the current sample range.

The names of the series in the returned list are constructed from the given _prefix_ (which must be an ASCII string of 24 characters or less, and valid as a gretl identifier), plus one or more digits representing the sub-period of the observation. An error is flagged if any of these names duplicate names of existing objects.

* * *

hpfilt
------

**Output:** series


|Arguments:|y (series)                   |
|----------|-----------------------------|
|          |lambda (scalar, optional)    |
|          |one-sided (boolean, optional)|


Returns the cycle component from application of the Hodrick–Prescott filter to series _y_. If the smoothing parameter, _lambda_, is not supplied then a data-based default is used, namely 100 times the square of the periodicity (100 for annual data, 1600 for quarterly data, and so on).

By default the filter is the usual two-sided version, but if the optional third argument is given with a non-zero value a one-sided variant (with no look-ahead) is computed in the manner of Stock and Watson (1999).

The most common use of the HP filter is detrending, but if it's the trend you are interested in that is easily obtained by subtraction, as in

```
	  series hptrend = y - hpfilt(y)
```


See also bkfilt, bwfilt.

* * *

hyp2f1
------

**Output:** scalar or matrix


|Arguments:|a (scalar)          |
|----------|--------------------|
|          |b (scalar)          |
|          |c (scalar)          |
|          |x (scalar or matrix)|


Returns the Gauss hypergeometric function for real argument _x_.

If _x_ is a scalar, the return value will be scalar; otherwise, it will be a matrix the same size as _x_.

* * *

I
-

**Output:** matrix


|Arguments:|n (integer)          |
|----------|---------------------|
|          |m (integer, optional)|


If _m_ is omitted, returns an identity matrix of order _n_. Otherwise returns an _n_ x _m_ matrix with ones on the main diagonal and zeros elsewhere.

* * *

Im
--

**Output:** matrix



Returns a real matrix of the same dimensions as _C_, holding the imaginary part of the input matrix. See also Re.

* * *

imaxc
-----

**Output:** row vector


|Arguments:|X (matrix)                 |
|----------|---------------------------|
|          |skip_na (boolean, optional)|


Returns the row indices of the maxima of the columns of _X_. For columns containing NAs the result is also set to NA, unless the optional argument _skip\_na_ is nonzero, in which case the index for the maximum valid entry will be returned.

See also imaxr, iminc, maxc.

* * *

imaxr
-----

**Output:** column vector


|Arguments:|X (matrix)                 |
|----------|---------------------------|
|          |skip_na (boolean, optional)|


Returns the column indices of the maxima of the columns of _X_. For rows containing NAs the result is also set to NA, unless the optional argument _skip\_na_ is nonzero, in which case the index for the maximum valid entry will be returned.

See also imaxc, iminr, maxr.

* * *

imhof
-----

**Output:** scalar


|Arguments:|M (matrix)|
|----------|----------|
|          |x (scalar)|


Computes Prob(_u'Au_ < _x_) for a quadratic form in standard normal variates, _u_, using the procedure developed by Imhof (1961).

If the first argument, _M_, is a square matrix it is taken to specify _A_, otherwise if it's a column vector it is taken to be the precomputed eigenvalues of _A_, otherwise an error is flagged.

See also pvalue.

* * *

iminc
-----

**Output:** row vector


|Arguments:|X (matrix)                 |
|----------|---------------------------|
|          |skip_na (boolean, optional)|


Returns the row indices of the minima of the columns of _X_. For columns containing NAs the result is also set to NA, unless the optional argument _skip\_na_ is nonzero, in which case the index for the minimum valid entry will be returned.

See also iminr, imaxc, minc.

* * *

iminr
-----

**Output:** column vector


|Arguments:|X (matrix)                 |
|----------|---------------------------|
|          |skip_na (boolean, optional)|


Returns the column indices of the minima of the rows of _X_. For rows containing NAs the result is also set to NA, unless the optional argument _skip\_na_ is nonzero, in which case the index for the minimum valid entry will be returned.

See also iminc, imaxr, minr.

* * *

inbundle
--------

**Output:** integer


|Arguments:|b (bundle)  |
|----------|------------|
|          |key (string)|


Checks whether bundle _b_ contains a data-item with name _key_. The value returned is an integer code for the type of the item: 0 for no match, 1 for scalar, 2 for series, 3 for matrix, 4 for string, 5 for bundle, 6 for array and 7 for list. The function typestr may be used to get the string corresponding to this code.

* * *

infnorm
-------

**Output:** scalar

Returns the infinity-norm of _X_, that is, the maximum across the rows of _X_ of the sum of absolute values of the row elements.

See also onenorm.

* * *

inlist
------

**Output:** integer


|Arguments:|L (list)  |
|----------|----------|
|          |y (series)|


Returns the (1-based) position of _y_ in list _L_, or 0 if _y_ is not present in _L_.

The second argument may be given as the name of a series or alternatively as an integer ID number. If you know that a series of a certain name (say foo) exists, then you can call this function as, for example,

```
	  pos = inlist(L, foo)
```


Here you are, in effect, asking "Give me the position of series foo in list L (or 0 if it is not included in L)." However, if you are unsure whether a series of the given name exists, you should place the name in quotes:

```
	  pos = inlist(L, "foo")
```


In this case you are asking, "If there's a series named foo in L give me its position, otherwise return 0."

* * *

instring
--------

**Output:** integer


|Arguments:|s1 (string)                 |
|----------|----------------------------|
|          |s2 (string)                 |
|          |ign_case (boolean, optional)|


This is a boolean relative of strstr: it returns 1 if _s1_ contains _s2_, 0 otherwise. So the conditional expression

```
	  if instring("cattle", "cat")
```


is logically equivalent to, but more efficient than,

```
	  if strlen(strstr("cattle", "cat")) > 0
```


If the optional argument _ign\_case_ is nonzero, the search is case-insensitive. For example,

```
	  instring("Cattle", "cat")
```


returns 0, but

```
	  instring("Cattle", "cat", 1)
```


returns 1.

* * *

instrings
---------

**Output:** see below


|Arguments:|S (array of strings)      |
|----------|--------------------------|
|          |test (string)             |
|          |simple (boolean, optional)|


Checks the elements of the strings array _S_ for equality with _test_. By default, returns a column vector of length equal to the number of matches, holding the positions of the matches within the array—or an empty matrix in case of no matches.

Example:

```
	  strings S = defarray("A", "B", "C", "B")
	  eval instrings(S, "B")
	  2
	  4
```


If a non-zero value is given for the optional _simple_ argument, the return value is a scalar: 1 if _test_ is found in _S_, 0 otherwise. In this case the implementation is able to take a shortcut, so it's more efficient if you just want a boolean answer.

* * *

int
---

**Output:** same type as input



Returns the integer part of _x_, truncating the fractional part, or NA if the result cannot be represented as a 32-bit signed integer (does not lie in the interval \[–2147483648, 2147483647\]).

Note: int and floor differ in their effect for negative arguments: int(-3.5) gives –3, while floor(-3.5) gives –4. See also ceil, floor, round.

* * *

interpol
--------

**Output:** series

Returns a series in which missing values in _x_ are imputed via linear interpolation, for time series data or in the time dimension of a panel dataset. Extrapolation is not performed; missing values are replaced only if they are both preceded and followed by valid observations.

* * *

inv
---

**Output:** matrix



Returns the inverse of _A_. If _A_ is singular or not square, an error message is produced and nothing is returned. Note that gretl checks automatically the structure of _A_ and uses the most efficient numerical procedure to perform the inversion.

The matrix types gretl checks for are: identity; diagonal; symmetric and positive definite; symmetric but not positive definite; and triangular.

Note: it makes sense to use this function only if you plan to use the inverse of _A_ more than once. If you just need to compute an expression of the form _A_\-1_B_, you'll be much better off using the "division" operators \\ and /. See chapter 17 of the Gretl User's Guide for details.

See also ginv, invpd.

* * *

invcdf
------

**Output:** same type as input


|Arguments:|d (string)                  |
|----------|----------------------------|
|          |... (see below)             |
|          |u (scalar, series or matrix)|


Inverse cumulative distribution function calculator. For a continuous distribution, returns _x_ such that _P(X <= x) = u_, for _u_ in the interval 0 to 1. For a discrete distribution (Binomial or Poisson), returns the smallest _x_ such that _P(X <= x) ≥ u_.

The distribution of _X_ is determined by the string _d_. Between the arguments _d_ and _u_, zero or more additional scalar arguments are required to specify the parameters of the distribution, as follows.

*   Standard normal (c = z, n, or N): no extra arguments
    
*   Gamma (g or G): shape; scale
    
*   Student's t (t): degrees of freedom
    
*   Chi square (c, x, or X): degrees of freedom
    
*   Snedecor's F (f or F): df (num.); df (den.)
    
*   Binomial (b or B): probability; trials
    
*   Poisson (p or P): mean
    
*   Laplace (l or L): mean; scale
    
*   Standardized GED (E): shape
    
*   Non-central chi square (ncX): df, non-centrality parameter
    
*   Non-central F (ncF): df (num.), df (den.), non-centrality parameter
    
*   Non-central t (nct): df, non-centrality parameter
    

See also cdf, critical, pvalue.

* * *

invmills
--------

**Output:** same type as input



Returns the inverse Mills ratio at _x_, that is the ratio between the standard normal density and the complement to the standard normal distribution function, both evaluated at _x_.

This function uses a dedicated algorithm which yields greater accuracy compared to calculation using dnorm and cnorm, but the difference between the two methods is appreciable only for very large negative values of _x_.

See also cdf, cnorm, dnorm.

* * *

invpd
-----

**Output:** square matrix


|Arguments:|A (positive definite matrix)           |
|----------|---------------------------------------|
|          |&logdet (reference to scalar, optional)|


Returns the inverse of the symmetric, positive definite matrix _A_. This function is slightly faster than inv for large matrices, since no check for symmetry is performed; for that reason it should be used with care.

If the optional argument _&logdet_ is present, the corresponding scalar will contain on successful exit the log determinant of _A_. This may be convenient to have in some cases, for example in the context of the evaluation of a Gaussian log-likelihood, because the log determinant is a by-product of the inversion algorithm and retrieving it via the _&logdet_ argument avoids extra computations.

Note: if you're interested in the inversion of a matrix of the form _X'X_, where _X_ is a large matrix, it is preferable to compute it via the prime operator X'X rather than using the more general syntax X'\*X. The former expression uses a specialized algorithm which has the double advantage of being more efficient computationally and of ensuring that the result will be free by construction of machine precision artifacts that may render it numerically non-symmetric.

* * *

irf
---

**Output:** matrix


|Arguments:|target (integer)                        |
|----------|----------------------------------------|
|          |shock (integer)                         |
|          |alpha (scalar between 0 and 1, optional)|
|          |sys (bundle, optional)                  |


Provides estimated impulse response functions pertaining to a VAR or VECM, traced out over a certain forecast horizon. Without the final optional argument, this function works only when the last model estimated was a VAR or VECM. Alternatively, information on such a system can be saved as a bundle via the $system accessor and subsequently passed to irf.

The _target_ and _shock_ arguments take the form of 1-based indices of the endogenous variables in the system, with 0 taken to mean "all". The responses (expressed in the units of the _target_ variable) are to an innovation of one standard deviation in the _shock_ variable. If _alpha_ is given a suitable positive value the estimates include a 1 – α confidence interval (so, for example, give 0.1 for a 90 percent interval).

The following code fragment illustrates usage. In the first example the matrix ir1 holds the responses of y1 to innovations in each of y1, y2 and y3 (point estimates only since _alpha_ is omitted). In the second, ir2 holds the responses of all targets to an innovation in y2, with 90 percent confidence intervals. In this case the returned matrix will have 9 columns: each response path occupies 3 adjacent columns giving point estimate, lower bound and upper bound. The last example produces a matrix with 27 columns: 3 per response for each target times each shock.

```
	  var 4 y1 y2 y3
	  matrix ir1 = irf(1, 0)
	  matrix ir2 = irf(0, 2, 0.1)
	  matrix ir3 = irf(0, 0, 0.1)
```


The number of periods (rows) over which the response is traced is determined automatically based on the frequency of the data, but this can be overridden via the set command, as in set horizon 10.

When confidence intervals are produced they are derived via bootstrapping, with resampling of the original residuals. It is assumed that the lag order of the VAR or VECM is sufficient to eliminate serial correlation of the residuals. By default the number of bootstrap replications is 1999, but that can be adjusted via set, as in

```
	  set boot_iters 2999
```


See also fevd, vma.

* * *

irr
---

**Output:** scalar



Returns the Internal Rate of Return for _x_, considered as a sequence of payments (negative) and receipts (positive). See also npv.

* * *

iscomplex
---------

**Output:** scalar

Tests whether _name_ is the identifier for a complex matrix. The return value is one of the following:

NA: _name_ does not identify a matrix.

0: _name_ identifies a real matrix, composed entirely of regular floating-point numbers ("doubles", in C parlance).

1: _name_ identifies a "nominally" complex matrix, composed of numbers with both a real and an imaginary part, but in which all imaginary parts are zero.

2: the matrix in question holds at least one "genuinely" complex value, with a non-zero imaginary part.

* * *

isconst
-------

**Output:** integer


|Arguments:|y (series or vector)          |
|----------|------------------------------|
|          |panel-code (integer, optional)|


Without the optional second argument, returns 1 if _y_ has a constant value over the current sample range (or over its entire length if _y_ is a vector), otherwise 0.

The second argument is accepted only if the current dataset is a panel and _y_ is a series. In that case a _panel-code_ value of 0 calls for a check for time-invariance, while a value of 1 means check for cross-sectional invariance (that is, in each time period the value of _y_ is the same for all groups).

If _y_ is a series, missing values are ignored in checking for constancy.

* * *

isdiscrete
----------

**Output:** integer

If _name_ is the identifier for a currently defined series, returns 1 if the series is marked as discrete-valued, otherwise 0. If _name_ does not identify a series, returns NA.

* * *

isdummy
-------

**Output:** integer



If all the values contained in _x_ are 0 or 1 (or missing), returns the number of ones, otherwise 0.

* * *

isnan
-----

**Output:** same type as input



Given a scalar argument, returns 1 if _x_ is "Not a Number" (NaN), otherwise 0. Given a matrix argument, returns a matrix of the same dimensions with 1s in positions where the corresponding element of the input is NaN and 0s elsewhere.

* * *

isoconv
-------

**Output:** integer


|Arguments:|date (series)                       |
|----------|------------------------------------|
|          |&year (reference to series)         |
|          |&month (reference to series)        |
|          |&day (reference to series, optional)|


Given a series _date_ holding dates in ISO 8601 "basic" format (YYYYMMDD), this function writes the year, month and (optionally) day components into the series named by the second and subsequent arguments. An example call, assuming the series dates contains suitable 8-digit values:

```
	  series y, m, d
	  isoconv(dates, &y, &m, &d)
```


The nominal return value is 0 on successful completion; in case of failure an error is flagged.

* * *

isocountry
----------

**Output:** same type as input


|Arguments:|source (string or array of strings)|
|----------|-----------------------------------|
|          |output (integer, optional)         |


This function maps between the four designations for countries present in ISO 3166, namely

1.  Country name
    
2.  Alpha-2 code (two uppercase letters)
    
3.  Alpha-3 code (three uppercase letters)
    
4.  Numeric code (3 digits)
    

Given a country's designation in one form, the return value is its designation in the form (1 to 4) selected by the optional _output_ argument or, if this argument is omitted, a default conversion as follows: when _source_ is a country name the return value is the country's 2-letter code; otherwise the return value is the country name. Various valid calls are illustrated below in interactive form.

```
	  ? eval isocountry("Bolivia")
	  BO
	  ? eval isocountry("Bolivia", 3)
	  BOL
	  ? eval isocountry("GB")
	  United Kingdom of Great Britain and Northern Ireland
	  ? eval isocountry("GB", 3)
	  GBR
	  ? strings S = defarray("ES", "DE", "SD")
	  ? strings C = isocountry(S)
	  ? print C
	  Array of strings, length 3
	  [1] "Spain"
	  [2] "Germany"
	  [3] "Sudan"
	  ? matrix m = {4, 840}
	  ? C = isocountry(m)
	  ? print C
	  Array of strings, length 2
	  [1] "Afghanistan"
	  [2] "United States of America"
```


When _source_ is in form 4 (numeric code) this can be given as a string or array of strings (for example, "032" for Argentina) or in numeric form. In the latter case _source_ may be given as a series or vector, though an error will be flagged if any of the numbers are out of the range 0 to 999.

In all cases (even when output form 4 is selected) a string, or array of strings, is returned; if numeric values are required these may be obtained using atof. If _source_ is not matched by any entry in the ISO 3166 table the return value is an empty string, in which case a warning is printed.

* * *

isodate
-------

**Output:** see below


|Arguments:|ed (scalar, series or matrix)|
|----------|-----------------------------|
|          |as-string (boolean, optional)|


The argument _ed_ is interpreted as an epoch day, which equals 1 for the first of January in the year 1 AD on the proleptic Gregorian calendar. The default return value (of the same type as _ed_) is an 8-digit number, or a series of such numbers, on the pattern YYYYMMDD (ISO 8601 "basic" format), giving the Gregorian calendar date corresponding to the epoch day.

If the optional second argument _as-string_ is non-zero, the return value is not numeric but rather a string on the pattern YYYY-MM-DD (ISO 8601 "extended" format), or a string-valued series if _ed_ is a series, or an array of strings if _ed_ is a vector. For a more flexible means of obtaining string representations of epoch days, see strfday.

For the inverse function, see epochday; also see juldate.

* * *

isoweek
-------

**Output:** see below


|Arguments:|year (scalar or series) |
|----------|------------------------|
|          |month (scalar or series)|
|          |day (scalar or series)  |


Returns the ISO 8601 week number corresponding to the date(s) specified by the three arguments, or NA if the date is invalid. Note that all three arguments must be of the same type, either scalars (integers) or series.

ISO weeks are numbered from 01 to 53; most years have 52 weeks but on average 71 out of 400 years have 53 weeks. The ISO 8601 definition for week 01 is the week containing the year's first Thursday on the Gregorian calendar. For a full account see https://en.wikipedia.org/wiki/ISO\_week\_date.

An alternative call is also supported: if a single argument is given, it is taken to be a date (or series of dates) in ISO 8601 "basic" numeric format, YYYYMMDD. So the following two calls produce the same result, namely 13.

```
	  eval isoweek(2022, 4, 1)
	  eval isoweek(20220401)
```


* * *

iwishart
--------

**Output:** matrix


|Arguments:|S (symmetric matrix)|
|----------|--------------------|
|          |v (integer)         |


Given _S_ (a positive definite _p_ x _p_ scale matrix), returns a drawing from the Inverse Wishart distribution with _v_ degrees of freedom, where _v_ must not be smaller than _p_. The returned matrix is also _p_ x _p_. The algorithm of Odell and Feiveson (1966) is used.

* * *

jsonget
-------

**Output:** string


|Arguments:|buf (string)                          |
|----------|--------------------------------------|
|          |path (string)                         |
|          |&nread (reference to scalar, optional)|


The argument _buf_ should be a JSON buffer, as may be retrieved from a suitable website via the curl function, and the _path_ argument should be a JsonPath specification.

This function returns a string representing the data found in the buffer at the specified path. Data types of double (floating-point), int (integer) and string are supported. In the case of doubles or ints, their string representation is returned (using the "C" locale for doubles). If the object to which _path_ refers is an array, the members are printed one per line in the returned string.

By default an error is flagged if _path_ is not matched in the JSON buffer, but this behavior is modified if you pass the third, optional argument: in that case the argument retrieves a count of the matches and an empty string is returned if there are none. Example call:

```
	  ngot = 0
	  ret = jsonget(jbuf, "$.some.thing", &ngot)
```


However, an error is still flagged in case of a malformed query.

An accurate account of JsonPath syntax can be found at http://goessner.net/articles/JsonPath/. However, please note that the back-end for jsonget is provided by json-glib, which does not necessarily support all elements of JsonPath. Moreover, the exact functionality of json-glib may differ depending on the version you have on your system. See https://wiki.gnome.org/Projects/JsonGlib if you need details.

That said, the following operators should be available to jsonget:

*   root node, via the $ character
    
*   recursive descent operator: ..
    
*   wildcard operator: \*
    
*   subscript operator: \[\]
    
*   set notation operator, for example \[i,j\]
    
*   slice operator: \[start:end:step\]
    

* * *

jsongetb
--------

**Output:** bundle


|Arguments:|buf (string)           |
|----------|-----------------------|
|          |path (string, optional)|


The argument _buf_ should be a JSON buffer, as may be retrieved from a suitable website via the curl function. The specification and effect of the optional _path_ argument are described below.

The return value is a bundle whose structure basically mirrors that of the input: JSON objects become gretl bundles and JSON arrays become gretl arrays, each of which can hold strings, bundles or arrays. JSON "value" nodes become either members of bundles or elements of arrays; in the latter case numerical values are converted to strings using sprintf. Note that although the JSON specification allows arrays of mixed type these cannot be handled by jsongetb since gretl arrays must be of a single type.

The _path_ argument can be used to limit the JSON elements included in the returned bundle. This is not a "JsonPath" as described in the help for jsonget; it is a simple construct subject to the following specification.

*   _path_ is a slash-separated array of elements where slash ("/") indicates moving to one level "deeper" in the JSON tree represented by _buf_. A leading slash is allowed but not required; implicitly the path always starts at the root. No extraneous white-space characters should be included.
    
*   Each slash-separated element must take one of the following forms: (a) a single name, in which case only a JSON element whose name matches at the given structural level will be included; or (b) "\*" (asterisk), in which case all elements at the given level are included; or (c) an array of comma-separated names, enclosed in braces ("{" and "}"), in which case only JSON elements whose names match one of the given names will be included.
    

See also the string-oriented jsonget; depending on your purpose one of these functions may be more helpful than the other.

* * *

juldate
-------

**Output:** see below


|Arguments:|ed (scalar, series or matrix)|
|----------|-----------------------------|
|          |as-string (boolean, optional)|


This function works just like isodate except that on output the dates are relative to the Julian calendar rather than the Gregorian.

* * *

kdensity
--------

**Output:** matrix


|Arguments:|x (series, list or matrix) |
|----------|---------------------------|
|          |scale (scalar, optional)   |
|          |control (boolean, optional)|


Computes a kernel density estimate (or set of estimates) for the argument _x_, which may be a single series or vector or a list or matrix with more than column. The returned matrix has _k_ + 1 columns, where _k_ is the number of elements (series or columns) in _x_. The first column holds a set of evenly spaced abscissae and the rest hold the estimated density or densities at each of these points.

The formula used to compute the estimated density at each reference point, _x_, is

!missing image

where _n_ denotes the number of data points, _h_ is a "bandwidth" parameter, and _k_() is the kernel function. The larger the value of the bandwidth parameter, the smoother the estimated density.

The optional _scale_ parameter can be used to adjust the bandwidth relative to the default of 1.0, which corresponds to the rule of thumb proposed by Silverman (1986), namely

!missing image

where _s_ denotes the standard deviation of the data and IQR is the inter-quartile range. The _control_ parameter acts as a boolean: 0 (the default) means that the Gaussian kernel is used; a non-zero value switches to the Epanechnikov kernel.

A plot of the results may be obtained using the gnuplot command, as illustrated below. Note that the column containing the abscissae should come last for plotting.

```
	  matrix d = kdensity(x)
	  # if x has a single element
	  gnuplot 2 1 --matrix=d --with-lines --fit=none
	  # if x has two elements
	  gnuplot 2 3 1 --matrix=d --with-lines --fit=none
```


* * *

kdsmooth
--------

**Output:** integer


|Arguments:|&kb (reference to bundle)|
|----------|-------------------------|
|          |MSE (boolean, optional)  |


Performs disturbance smoothing for a Kalman bundle previously set up by means of ksetup and returns 0 on successful completion or non-zero if numerical problems are encountered. The return value should be checked before making using of results.

On successful completion, the smoothed disturbances will be available as kb.smdist.

The optional _MSE_ argument determines the contents of the kb.smdisterr key. If 0 or omitted, this matrix will contain the unconditional standard errors of the smoothed disturbances, which are normally used to compute the so-called _auxiliary residuals_. Otherwise, kb.smdisterr will contain the estimated root mean square deviations of the auxiliary residuals from their true value.

For more details see chapter 36 of the Gretl User's Guide.

See also ksetup, kfilter, ksmooth, ksimul.

* * *

kfilter
-------

**Output:** scalar



Performs a forward, filtering pass on a Kalman bundle previously set up by means of ksetup and returns 0 on successful completion or 1 if numerical problems are encountered.

On successful completion, the one-step-ahead prediction errors will be available as kb.prederr and the sequence of their covariance matrices as kb.pevar. Moreover, the key kb.llt gives access to a _T_\-vector containing the log-likelihood by observation.

For more details see chapter 36 of the Gretl User's Guide.

See also kdsmooth, ksetup, ksmooth, ksimul.

* * *

kmeier
------

**Output:** matrix


|Arguments:|d (series or vector)             |
|----------|---------------------------------|
|          |cens (series or vector, optional)|


Given a sample of duration data, _d_, possibly accompanied by a record of censoring status, _cens_, computes the Kaplan–Meier nonparametric estimator of the survival function (Kaplan and Meier, 1958). The returned matrix has three columns holding, respectively, the sorted unique values in _d_, the estimated survival function corresponding to the duration value in column 1 and the (large sample) standard error of the estimator, calculated via the method of Greenwood (1926).

If the _cens_ series is given, the value 0 is taken to indicate an uncensored observation while a value of 1 indicates a right-censored observation (that is, the period of observation of the individual in question has ended before the duration or spell has been recorded as terminated). If _cens_ is not given, it is assumed that all observations are uncensored. (Note: the semantics of _cens_ may be extended at some point to cover other types of censoring.)

See also naalen.

* * *

kpsscrit
--------

**Output:** matrix


|Arguments:|T (scalar)     |
|----------|---------------|
|          |trend (boolean)|


Returns a row vector containing critical values at the 10, 5 and 1 percent levels for the KPSS test for stationarity of a time series. _T_ should give the number of observations and _trend_ should be 1 if the test includes a trend, 0 otherwise.

The critical values given are based on response surfaces estimated in the manner set out by Sephton (Economics Letters, 1995). See also the kpss command.

* * *

ksetup
------

**Output:** bundle


|Arguments:|Y (series, matrix or list)|
|----------|--------------------------|
|          |Z (scalar or matrix)      |
|          |T (scalar or matrix)      |
|          |Q (scalar or matrix)      |
|          |R (matrix, optional)      |


Sets up a Kalman bundle, that is an object which contains all the information needed to define a linear state space model of the form

!missing image

where Var_(u) = R_, and state transition equation

!missing image

where Var_(v) = Q_.

Objects created via this function can be later used via the dedicated functions kfilter for filtering, ksmooth and kdsmooth for smoothing and ksimul for performing simulations.

The class of models that gretl can handle is in fact much wider than the one implied by the representation above: it is possible to have time-varying models, models with diffuse priors and exogenous variable in the measurement equation and models with cross-correlated innovations. For further details, see chapter 36 of the Gretl User's Guide.

See also kdsmooth, kfilter, ksmooth, ksimul.

* * *

ksimul
------

**Output:** matrix


|Arguments:|&kb (reference to bundle)|
|----------|-------------------------|
|          |U (matrix)               |
|          |extra (boolean, optional)|


Uses a Kalman bundle previously set up by means of ksetup to perform simulation, the disturbances being taken from the matrix _U_. By default the returned matrix (which will have as many rows as _U_) contains simulated values of the observable(s), but if a non-zero value is given for _extra_ the simulated state is also included. In the latter case each row holds the state first, then the observable(s).

For details see chapter 36 of the Gretl User's Guide.

See also ksetup, kfilter, ksmooth.

* * *

ksmooth
-------

**Output:** integer



Performs a fixed-point smoothing (backward) pass on a Kalman bundle previously set up by means of ksetup and returns 0 on successful completion or non-zero if numerical problems are encountered. The return value should be checked before making using of results.

On successful completion, the smoothed states will be available as kb.state and the sequence of their covariance matrices as kb.stvar. For more details see chapter 36 of the Gretl User's Guide.

See also ksetup, kdsmooth, kfilter, ksimul.

* * *

kurtosis
--------

**Output:** scalar

Returns the excess kurtosis of the series _x_, skipping any missing observations.

* * *

lags
----

**Output:** list or matrix


|Arguments:|p (scalar or vector)      |
|----------|--------------------------|
|          |y (series, list or matrix)|
|          |bylag (boolean, optional) |


If the first argument is a scalar, generates lags 1 to _p_ of the series _y_, or if _y_ is a list, of all series in the list, or if _y_ is a matrix, of all columns in the matrix. If _p_ = 0 and _y_ is a series or list, the maximum lag defaults to the periodicity of the data; otherwise _p_ must be positive.

If a vector is given as the first argument, the lags generated are those specified in the vector. Common usage in this case would be to give _p_ as, for example, seq(3,7), hence omitting the first and second lags. However, it is OK to give a vector with gaps, as in {3,5,7}, although the lags should always be given in ascending order.

In the case of list output, the generated variables are automatically named according to the template _varname_ \_ _i_ where _varname_ is the name of the original series and _i_ is the specific lag. The original portion of the name is truncated if necessary, and may be adjusted in case of non-uniqueness in the set of names thus constructed.

When _y_ is a list, or a matrix with more than one column, and the lag order is greater than 1, the default ordering of the terms in the return value is by variable: all lags of the first input series or column followed by all lags of the second, and so on. The optional third argument can be used to change this: if _bylag_ is non-zero then the terms are ordered by lag: lag 1 of all the input series or columns, then lag 2 of all the series or columns, and so on.

See also mlag for use with matrices.

* * *

lastobs
-------

**Output:** integer


|Arguments:|y (series)                  |
|----------|----------------------------|
|          |insample (boolean, optional)|


Returns the 1-based index of the last non-missing observation for the series _y_. By default the whole data range is examined, so if subsampling is in effect the value returned may be larger than the accessor $t2. But if a non-zero value is given for _insample_ only the current sample range is considered. See also firstobs.

* * *

ldet
----

**Output:** scalar



Returns the natural log of the determinant of _A_, computed via the LU factorization. Note that this is more efficient than calling det and taking the log of the result. Moreover, in some cases ldet is able to return a valid result even if the determinant of _A_ is numerically "infinite" (exceeds the C library's maximum double-precision number). See also rcond, cnumber.

* * *

ldiff
-----

**Output:** same type as input



Computes log differences; starting values are set to NA.

When a list is returned, the individual variables are automatically named according to the template ld\__varname_ where _varname_ is the name of the original series. The name is truncated if necessary, and may be adjusted in case of non-uniqueness in the set of names thus constructed.

See also diff, sdiff.

* * *

lincomb
-------

**Output:** series


|Arguments:|L (list)  |
|----------|----------|
|          |b (vector)|


Computes a new series as a linear combination of the series in the list _L_. The coefficients are given by the vector _b_, which must have length equal to the number of series in _L_.

See also wmean.

* * *

linearize
---------

**Output:** series

Depends on having TRAMO installed. Returns a "linearized" version of the input series; that is, a series in which any missing values are replaced by interpolated values and outliers are adjusted. TRAMO's fully automatic mechanism is used; consult the TRAMO documentation for details.

Note that if the input series has no missing values and no values that TRAMO regards as outliers, this function will return a copy of the original series.

* * *

ljungbox
--------

**Output:** scalar


|Arguments:|y (series) |
|----------|-----------|
|          |p (integer)|


Computes the Ljung–Box Q' statistic for the series _y_ using lag order _p_, over the currently defined sample range. The lag order must be greater than or equal to 1 and less than the number of available observations.

This statistic may be referred to the chi-square distribution with _p_ degrees of freedom as a test of the null hypothesis that the series _y_ is not serially correlated. See also pvalue.

* * *

lngamma
-------

**Output:** same type as input



Returns the log of the gamma function of _x_.

See also bincoeff and gammafun.

* * *

loess
-----

**Output:** series


|Arguments:|y (series)                |
|----------|--------------------------|
|          |x (series)                |
|          |d (integer, optional)     |
|          |q (scalar, optional)      |
|          |robust (boolean, optional)|


Performs locally-weighted polynomial regression and returns a series holding predicted values of _y_ for each non-missing value of _x_. The method is as described by William Cleveland (1979).

The optional arguments _d_ and _q_ specify the order of the polynomial in _x_ and the proportion of the data points to be used in local estimation, respectively. The default values are _d_ = 1 and _q_ = 0.5. The other acceptable values for _d_ are 0 and 2. Setting _d_ = 0 reduces the local regression to a form of moving average. The value of _q_ must be greater than 0 and cannot exceed 1; larger values produce a smoother outcome.

If a non-zero value is given for the _robust_ argument the local regressions are iterated twice, with the weights being modified based on the residuals from the previous iteration so as to give less influence to outliers.

See also nadarwat, and in addition see chapter 40 of the Gretl User's Guide for details on nonparametric methods.

* * *

log
---

**Output:** same type as input



Returns the natural logarithm of _x_; produces NA for non-positive values. Note: ln is an acceptable alias for log.

When a list is returned, the individual variables are automatically named according to the template l\__varname_ where _varname_ is the name of the original series. The name is truncated if necessary, and may be adjusted in case of non-uniqueness in the set of names thus constructed.

Note that in case of matrix input the function acts element by element. For the matrix logarithm function, see mlog.

* * *

log10
-----

**Output:** same type as input



Returns the base-10 logarithm of _x_; produces NA for non-positive values.

* * *

log2
----

**Output:** same type as input



Returns the base-2 logarithm of _x_; produces NA for non-positive values.

* * *

logistic
--------

**Output:** same type as input



Returns the logistic CDF of the argument _x_, that is, 1/(1 + _e_–x). If _x_ is a matrix, the function is applied element by element.

* * *

lpsolve
-------

**Output:** bundle

Solves a linear programming problem using the lpsolve library. See gretl-lpsolve.pdf for details and examples of usage.

* * *

lower
-----

**Output:** square matrix

Returns an _n_ x _n_ lower triangular matrix: the elements on and below the diagonal are equal to the corresponding elements of _A_; the remaining elements are zero.

See also upper.

* * *

lrcovar
-------

**Output:** matrix


|Arguments:|A (matrix)                |
|----------|--------------------------|
|          |demean (boolean, optional)|


Returns the long-run variance-covariance matrix of the columns of _A_. The data are first demeaned unless the second (optional) argument is set to zero. The kernel type and lag truncation parameter (window size) can be chosen before calling this function with the HAC-related options that the set command offers, such as hac\_kernel, hac\_lag, hac\_prewhiten. See also the section on Time series data and HAC covariance matrices in chapter 22 of the Gretl User's Guide.

See also lrvar.

* * *

lrvar
-----

**Output:** scalar


|Arguments:|y (series or vector) |
|----------|---------------------|
|          |k (integer, optional)|
|          |mu (scalar, optional)|


Returns the long-run variance of _y_, calculated using a Bartlett kernel with window size _k_. If the second argument is omitted, or given a negative value, the window size defaults to the integer part of the cube root of the sample size.

For the variance calculation, the series _y_ is centered around the optional parameter _mu_; if this is omitted or NA, the sample mean is used.

For a multivariate counterpart, see lrcovar.

* * *

Lsolve
------

**Output:** matrix


|Arguments:|L (matrix)|
|----------|----------|
|          |B (matrix)|


Solves for _x_ in _AX = B_, where _L_ is the lower triangular Cholesky factor of the positive definite matrix _A_, satisfying _LL' = A_. Suitable _L_ can be obtained using the cholesky function with _A_ as argument.

The following two calculations should produce the same result (up to machine precision), but the first variant allows for reuse of a precomputed Cholesky factor and so should be substantially faster if you are solving repeatedly for given _A_ and several values of _B_. The speed-up will be greater, the greater the dimension of _A_.

```
	  # variant 1
	  matrix L = cholesky(A)
	  matrix X = Lsolve(L, B)
	  # variant 2
	  matrix X = A \ B
```


* * *

mat2list
--------

**Output:** list


|Arguments:|X (matrix)               |
|----------|-------------------------|
|          |prefix (string, optional)|


A convenience function for making a list of series using the columns of a suitable matrix as input. The row dimension of _X_ must equal either the length of the current dataset or the number of observations in the current sample range.

The naming of the series in the returned list proceeds as follows. First, if the optional _prefix_ argument is supplied, the series created from column _i_ of _X_ is named by appending _i_ to the given string, as in myprefix1, myprefix2 and so on. Otherwise, if _X_ has column names set (see cnameset) these names are used. Finally, if neither of the above conditions is satisfied, the names are column1, column2 and so on. Note that this policy may result in overwriting existing series; if you don't want that to happen, take charge of naming the columns explicitly via cnameset, or supply _prefix_.

Here is an illustrative example of usage:

```
	  matrix X = mnormal($nobs, 8)
	  list L = mat2list(X, "xnorm")
	  # or alternatively, if you don't need X as such
	  list L = mat2list(mnormal($nobs, 8), "xnorm")
```


This will add to the dataset eight full-length series named xnorm1, xnorm2 and so on.

* * *

max
---

**Output:** depends on input


|Arguments:|x (scalar, series or matrix)          |
|----------|--------------------------------------|
|          |y (scalar, series or matrix, optional)|


This function has two primary modes plus a special case.

The first mode is activated if a single argument of type scalar, series or matrix is given: the return value is a scalar, the maximum valid value "within" the argument: if _x_ is a series, its maximum value within the current sample range, or if _x_ is a matrix, its greatest element, missing values being ignored. The case of a scalar argument is supported for the sake of completeness; you just get its value back.

The second mode is activated if two arguments are given. The arguments _x_ and _y_ must be of the same type, and must be scalars, series or matrices (and if they are matrices, they must be of the same dimensions). The return value is an object of the same type as the arguments, holding the "between" or "cross" maximum or maxima. If the arguments are scalars you get the greater of the two; if they're series you get a series holding the greater of the values of the two series at each observation in the current sample range; if they're matrices you get a matrix holding the greater of their elements in each row and column. For each of the pairwise comparisons if either term is missing the result is also a missing value.

### The special case

This arises if a single list argument is given. The return value is a series, containing at each observation in the current sample range the greatest of the values of the series in the list at that observation.

See also min.

* * *

maxc
----

**Output:** row vector


|Arguments:|X (matrix)                 |
|----------|---------------------------|
|          |skip_na (boolean, optional)|


Returns a row vector containing the maxima of the columns of _X_. For columns containing NAs the result is also set to NA, unless the optional argument _skip\_na_ is nonzero, in which case the maximum valid entry will be returned.

See also imaxc, maxr, minc.

* * *

maxr
----

**Output:** column vector


|Arguments:|X (matrix)                 |
|----------|---------------------------|
|          |skip_na (boolean, optional)|


Returns a column vector containing the maxima of the rows of _X_. For rows containing NAs the result is also set to NA, unless the optional argument _skip\_na_ is nonzero, in which case the maximum valid entry will be returned.

See also imaxr, maxc, minr.

* * *

mcorr
-----

**Output:** matrix

Computes a (Pearson) correlation matrix treating each column of _X_ as a variable. See also corr, cov, mcov.

* * *

mcov
----

**Output:** matrix


|Arguments:|X (matrix)                |
|----------|--------------------------|
|          |dfcorr (integer, optional)|


Computes a covariance matrix treating each column of _X_ as a variable. The divisor is _n_ – 1, where _n_ is the number of rows of _X_, unless the optional second argument is supplied, in which case _n_ – _dfcorr_ is used.

See also corr, cov, mcorr.

* * *

mcovg
-----

**Output:** matrix


|Arguments:|X (matrix)          |
|----------|--------------------|
|          |u (vector, optional)|
|          |w (vector, optional)|
|          |p (integer)         |


Returns the matrix covariogram for a _T_ x _k_ matrix _X_ (typically containing regressors), an (optional) _T_ \-vector _u_ (typically containing residuals), an (optional) (_p_+1)-vector of weights _w_, and a lag order _p_, which must be greater than or equal to 0.

The returned matrix is the sum for _j_ from _\-p_ to _p_ of _w(|j|) \* X(t)X(t-j)' \* u(t)u(t-j)_, where _X(t)'_ is the _t_\-th row of _X_.

If _u_ is given as null the _u_ terms are omitted, and if _w_ is given as null all the weights are taken to be 1.0.

For example, the following piece of code

```
	  set seed 123
	  X = mnormal(6,2)
	  Lag = mlag(X,1)
	  Lead = mlag(X,-1)
	  print X Lag Lead
	  eval X'X
	  eval mcovg(X, , , 0)
	  eval X'(X + Lag + Lead)
	  eval mcovg(X, , , 1)
```


produces this output:

```
	  ? print X Lag Lead
	  X (6 x 2)

	    -0.76587      -1.0600
	    -0.43188      0.30687
	    -0.82656      0.40681
	     0.39246      0.75479
	     0.36875       2.5498
	     0.28855     -0.55251

	  Lag (6 x 2)

	      0.0000       0.0000
	    -0.76587      -1.0600
	    -0.43188      0.30687
	    -0.82656      0.40681
	     0.39246      0.75479
	     0.36875       2.5498

	  Lead (6 x 2)

	    -0.43188      0.30687
	    -0.82656      0.40681
	     0.39246      0.75479
	     0.36875       2.5498
	     0.28855     -0.55251
	      0.0000       0.0000

	  ? eval X'X
	      1.8295       1.4201
	      1.4201       8.7596

	  ? eval mcovg(X,,, 0)
	      1.8295       1.4201
	      1.4201       8.7596

	  ? eval X'(X + Lag + Lead)
	      3.0585       2.5603
	      2.5603       10.004

	  ? eval mcovg(X,,, 1)
	      3.0585       2.5603
	      2.5603       10.004
```


* * *

mean
----

**Output:** scalar or series


|Arguments:|x (series or list)         |
|----------|---------------------------|
|          |partial (boolean, optional)|


If _x_ is a series, returns the (scalar) sample mean, skipping any missing observations.

If _x_ is a list, returns a series _y_ such that _y_t is the mean of the values of the variables in the list at observation _t_. By default the mean is recorded as NA if there are any missing values at _t_, but if you pass a non-zero value for _partial_ any non-missing values will be used to form the statistic.

The following example illustrates the working of the function

```
		open denmark.gdt
		eval mean(LRM)
		list L = dataset
		eval mean(L)
```


The first call will return the scalar mean value (scalar) of the series LRM, and the second one returns a series.

See also median, sum, max, min, sd, var.

* * *

meanc
-----

**Output:** row vector


|Arguments:|X (matrix)                 |
|----------|---------------------------|
|          |skip_na (boolean, optional)|


Returns the means of the columns of _X_. If a non-zero value is given for the optional second argument missing values are ignored, otherwise the result is NA for any columns that contain missing values.

For example, the following piece of code

```
		matrix m = mnormal(5, 2)
		m[1,2] = NA
		print m
		eval meanc(m)
```


produces this output:

```
		? print m
		m (5 x 2)

	   -0.098299          nan
	      1.1829      -1.2817
	     0.46037     -0.92947
	      1.4896     -0.91970
	     0.91918      0.47748

		? eval meanc(m)
	     0.79075          nan
```


See also meanr, sumc, maxc, minc, sdc, prodc.

* * *

meanr
-----

**Output:** column vector


|Arguments:|X (matrix)                 |
|----------|---------------------------|
|          |skip_na (boolean, optional)|


Returns the means of the rows of _X_. If a non-zero value is given for the optional second argument missing values are ignored, otherwise the result is NA for any rows that contain missing values. See also meanc, sumr.

* * *

median
------

**Output:** scalar or series



If _x_ is a series, returns the (scalar) sample median, skipping any missing observations.

If _x_ is a list, returns a series _y_ such that _y_t is the median of the values of the variables in the list at observation _t_, or NA if there are any missing values at _t_.

The following example illustrates the working of the function

```
	  set verbose off
	  open denmark.gdt
	  eval median(LRM)
	  list L = dataset
	  series m = median(L)
```


The first call will return the scalar median value (scalar) of the series LRM, and the second one returns a series.

See also mean, sum, max, min, sd, var.

* * *

mexp
----

**Output:** square matrix



Computes the matrix exponential of _A_. If _A_ is a real matrix, algorithm 11.3.1 from Golub and Van Loan (1996) is used. If _A_ is complex the algorithm uses eigendecomposition and _A_ must be diagonalizable.

See also mlog.

* * *

mgradient
---------

**Output:** matrix


|Arguments:|p (integer)             |
|----------|------------------------|
|          |theta (vector)          |
|          |type (integer or string)|


Analytical derivatives for MIDAS weights. Let _k_ denote the number of elements in the vector of hyper-parameters, _theta_. This function returns a _p_ x _k_ matrix holding the gradient of the vector of weights (as calculated by mweights) with respect to the elements of _theta_. The first argument represents the desired lag order and the last argument specifies the type of parameterization. See mweights for an account of the acceptable _type_ values.

See also midasmult, mlincomb, mweights.

* * *

midasmult
---------

**Output:** matrix


|Arguments:|mod (bundle)      |
|----------|------------------|
|          |cumulate (boolean)|
|          |v (integer)       |


Computes MIDAS multipliers. The _mod_ argument must be a bundle containing a MIDAS model, as the one produced by the midasreg command and accessible via the $model keyword. The function returns a matrix with the implicit MIDAS multipliers for variable _v_ in its first column and the corresponding standard errors in the second one. If the _cumulate_ argument is nonzero, the multipliers are cumulated.

Note that the returned matrix is automatically endowed with appropriate row labels, so it is suitable to be used as the first argument to the modprint command. For example, the code

```
	  open gdp_midas.gdt
	  list dIP = ld_indpro*
	  smpl 1985:1 ;
	  midasreg ld_qgdp 0 ; mds(dIP, 0, 6, 2)
	  matrix ip_m = midasmult($model, 0, 1)
	  modprint ip_m
```


produces the following output:

```
             coefficient   std. error      z       p-value
  ---------------------------------------------------------
  dIP_0      0.343146      0.0957752     3.583     0.0003   ***
  dIP_1      0.402547      0.0834904     4.821     1.43e-06 ***
  dIP_2      0.176437      0.0673776     2.619     0.0088   ***
  dIP_3      0.0601876     0.0621927     0.9678    0.3332
  dIP_4      0.0131263     0.0259137     0.5065    0.6125
  dIP_5      0.000965260   0.00346703    0.2784    0.7807
  dIP_6      0.00000       0.00000      NA        NA
```


See also mgradient, mweights, mlincomb.

* * *

min
---

**Output:** depends on input


|Arguments:|x (scalar, series or matrix)|
|----------|----------------------------|
|          |y (scalar, series or matrix)|


Please see the help for max; this function works in exactly the same way except that it returns a minimum or minima.

* * *

minc
----

**Output:** row vector


|Arguments:|X (matrix)                 |
|----------|---------------------------|
|          |skip_na (boolean, optional)|


Returns the minima of the columns of _X_. For columns containing NAs the result is also set to NA, unless the optional argument _skip\_na_ is nonzero, in which case the minimum valid entry will be returned.

See also iminc, maxc, minr.

* * *

minr
----

**Output:** column vector


|Arguments:|X (matrix)                 |
|----------|---------------------------|
|          |skip_na (boolean, optional)|


Returns the minima of the rows of _X_. For rows containing NAs the result is also set to NA, unless the optional argument _skip\_na_ is nonzero, in which case the minimum valid entry will be returned.

See also iminr, maxr, minc.

* * *

missing
-------

**Output:** same type as input



Returns a binary variable holding 1 if _x_ is NA. If _x_ is a series, the comparison is done element by element; if _x_ is a list of series, the output is a series with 1 at observations for which at least one series in the list has a missing value, and 0 otherwise. For example, the following code

```
		nulldata 3
		series x = normal()
		x[2] = NA
		series x_ismiss = missing(x)
		print x x_ismiss --byobs
```


sets a missing value at the second observation of _x_, and creates a new boolean series _x\_ismiss_ which identifies the missing observation

```
		             y     y_ismiss

		1    -1.551247            0
		2                         1
		3    -2.244616            0
```


See also misszero, ok, zeromiss.

* * *

misszero
--------

**Output:** same type as input



Converts NAs to zeros. If _x_ is a series or matrix, the conversion is done element by element. For example, the following code

```
		nulldata 3
		series x = normal()
		x[2] = NA
		y = misszero(x)
		print x y --byobs
```


sets a missing value at the second observation of _x_, and creates a new series _y_ for which the missing observation is replaced by zero:

```
	             x            y

		1    0.7355250    0.7355250
		2                     0.000
		3   -0.2465936   -0.2465936
```


See also missing, ok, zeromiss.

* * *

mlag
----

**Output:** matrix


|Arguments:|X (matrix)          |
|----------|--------------------|
|          |p (scalar or vector)|
|          |m (scalar, optional)|


Shifts up or down the rows of _X_. If _p_ is a positive scalar, returns a matrix in which the columns of _X_ are shifted down by _p_ rows and the first _p_ rows are filled with the value _m_. If _p_ is a negative number, _X_ is shifted up and the last rows are filled with the value _m_. If _m_ is omitted, it is understood to be zero.

If _p_ is a vector the operation described above is carried out for each element in _p_ and the resulting matrices are joined horizontally. The following code illustrates this usage, for input _X_ with two columns and input _p_ calling for lags 1 and 2. Missing values are set to NA as opposed to the default of 0.

```
	matrix X = mnormal(5, 2)
	print X
	eval mlag(X, {1, 2}, NA)
```


```
	m (5 x 2)

      1.5953    -0.070740
    -0.52713     -0.47669
     -2.2056     -0.28112
     0.97753       1.4280
     0.49654      0.18532

         nan          nan          nan          nan
      1.5953    -0.070740          nan          nan
    -0.52713     -0.47669       1.5953    -0.070740
     -2.2056     -0.28112     -0.52713     -0.47669
     0.97753       1.4280      -2.2056     -0.28112
```


See also lags.

* * *

mlincomb
--------

**Output:** series


|Arguments:|hfvars (list)           |
|----------|------------------------|
|          |theta (vector)          |
|          |type (integer or string)|


A convenience MIDAS function which combines lincomb with mweights. Given a list _hfvars_, it constructs a series which is a weighted sum of the elements of the list, the weights based on the vector of hyper-parameters _theta_ and the type of parameterization: see mweights for details. Note that hflags is generally the best way to create a list suitable as the first argument to this function.

To be explicit, the call

```
	  series s = mlincomb(hfvars, theta, 2)
```


is equivalent to

```
	  matrix w = mweights(nelem(hfvars), theta, 2)
	  series s = lincomb(hfvars, w)
```


but use of mlincomb saves on some typing and also some CPU cycles.

* * *

mlog
----

**Output:** square matrix



Computes the matrix logarithm of _A_. The algorithm employed relies on eigendecomposition, which requires that _A_ be diagonalizable. See also mexp.

* * *

mnormal
-------

**Output:** matrix


|Arguments:|r (integer)          |
|----------|---------------------|
|          |c (integer, optional)|


Returns a matrix with _r_ rows and _c_ columns, filled with standard normal pseudo-random variates. If omitted, the number of columns defaults to 1 (column vector). See also normal, muniform.

* * *

mols
----

**Output:** matrix


|Arguments:|Y (matrix)                       |
|----------|---------------------------------|
|          |X (matrix)                       |
|          |&U (reference to matrix, or null)|
|          |&V (reference to matrix, or null)|


Returns a _k_ x _n_ matrix of parameter estimates obtained by OLS regression of the _T_ x _n_ matrix _Y_ on the _T_ x _k_ matrix _X_.

If the third argument is not null, the _T_ x _n_ matrix _U_ will contain the residuals. If the final argument is given and is not null then the _k_ x _k_ matrix _V_ will contain (a) the covariance matrix of the parameter estimates, if _Y_ has just one column, or (b) _X'X_\-1 if _Y_ has multiple columns.

By default, estimates are obtained via Cholesky decomposition, with a fallback to QR decomposition if the columns of _X_ are highly collinear. The use of SVD can be forced via the command set svd on.

See also mpols, mrls.

* * *

monthlen
--------

**Output:** same type as input


|Arguments:|month (scalar or series)|
|----------|------------------------|
|          |year (scalar or series) |
|          |weeklen (integer)       |


Returns the number of (relevant) days in the specified month in the specified year, on the proleptic Gregorian calendar. The _weeklen_ argument, which must equal 5, 6 or 7, gives the number of days in the week that should be counted (a value of 6 omits Sundays, and a value of 5 omits both Saturdays and Sundays).

The return value is a scalar if both _month_ and _year_ are scalars, otherwise a series.

For example, if you have a monthly dataset open, the call

```
	  series wd = monthlen($obsminor, $obsmajor, 5)
```


will return a series containing the number of working days for each month in the sample.

* * *

movavg
------

**Output:** series


|Arguments:|x (series)                 |
|----------|---------------------------|
|          |p (scalar)                 |
|          |control (integer, optional)|
|          |y0 (scalar, optional)      |


Depending on the value of the parameter _p_, returns either a simple or an exponentially weighted moving average of the input series _x_.

If _p_ > 1, a simple _p_\-term moving average is computed, that is, the arithmetic mean of _x_ from period _t_ to _t-p+1_. If a non-zero value is supplied for the optional _control_ parameter the MA is centered, otherwise it is "trailing". The optional _y0_ argument is ignored.

If _p_ is a positive fraction, an exponential moving average is computed:

_y(t) = p\*x(t) + (1-p)\*y(t-1)_

By default the output series, _y_, is initialized using the first value of _x_, but the _control_ parameter may be used to specify the number of initial observations that should be averaged to produce _y(0)_. A zero value for _control_ indicates that all the observations should be used. Alternatively, an initializer may be specified using the optional _y0_ argument; in that case the _control_ argument is ignored.

* * *

mpiallred
---------

**Output:** integer


|Arguments:|&object (reference to object)|
|----------|-----------------------------|
|          |op (string)                  |


Available only when gretl is in MPI mode (see gretl + MPI). Must be called by all processes. This function works like mpireduce except that all processes, not just the root process, get a copy of the "reduced" object in place of the original. It is therefore equivalent to mpireduce followed by a call to mpibcast, but more efficient.

* * *

mpibarrier
----------

**Output:** integer

Available only when gretl is in MPI mode (see gretl + MPI). Takes no arguments. Enforces synchronization of MPI processes: no process can continue beyond the barrier until it has been reached by all.

```
	  # nobody gets past until everyone gets here
	  mpibarrier()
```


* * *

mpibcast
--------

**Output:** integer


|Arguments:|&object (reference to object)|
|----------|-----------------------------|
|          |root (integer, optional)     |


Available only when gretl is in MPI mode (see gretl + MPI). Must be called by all processes. Broadcasts the _object_ argument, which must be given in pointer form, to all processes. The object in question (a matrix, bundle, scalar, array, string or list) must be declared in all processes prior to the broadcast. No process can continue beyond a call to mpibcast until all processes have successfully executed it.

By default "root", the source of the broadcast, is the MPI process with rank 0, but this can be adjusted via the optional second argument, which must be an integer from 0 to the number of MPI processes minus 1.

A simple example follows. On successful completion every process will have a copy of the matrix X defined at rank 0.

```
	  matrix X
	  if $mpirank == 0
	      X = mnormal(T, k)
	  endif
	  mpibcast(&X)
```


* * *

mpirecv
-------

**Output:** object

Available only when gretl is in MPI mode (see gretl + MPI). See mpisend, with which mpirecv must always be paired, for an explanation. The _src_ argument specifies the rank of the process from which the object is to be received, in the range 0 to the number of MPI processes minus 1.

* * *

mpireduce
---------

**Output:** integer


|Arguments:|&object (reference to object)|
|----------|-----------------------------|
|          |op (string)                  |
|          |root (integer, optional)     |


Available only when gretl is in MPI mode (see gretl + MPI). Must be called by all processes. This function gathers objects (scalars, matrices or arrays) of a specified name, given in pointer form, from all processes and "reduces" them to a single object at the root node.

The op argument specifies the reduction operation or method. The methods supported for scalars are sum, prod (product), max and min. For matrices the methods are sum, prod (Hadamard product), hcat (horizontal concatenation) and vcat (vertical concatenation). For arrays only acat (concatenation) is supported.

By default "root", the target of the reduction, is the MPI process with rank 0, but this can be adjusted via the optional third argument, which must be an integer from 0 to the number of MPI processes minus 1.

An example follows. On successful completion of the above, the root process will have a matrix X which is the sum of the matrices X at all processes.

```
	  matrix X
	  X = mnormal(T, k)
	  mpireduce(&X, sum)
```


* * *

mpiscatter
----------

**Output:** integer


|Arguments:|&M (reference to matrix)|
|----------|------------------------|
|          |op (string)             |
|          |root (integer, optional)|


Available only when gretl is in MPI mode (see gretl + MPI). Must be called by all processes. This function distributes chunks of a matrix in the root process to all processes. The matrix must be declared in all processes prior to the call to mpiscatter, and must be given in pointer form.

The op argument must be either byrows or bycols. Let _q_ denote the quotient of the number of rows in the matrix to be scattered and the number of processes. In the byrows case root sends the first _q_ rows to process 0, the next _q_ to process 1, and so on. If there is a remainder from the division of rows it is added to the last allotment. The bycols case is exactly analogous but splitting of the matrix is by columns.

An example follows. If there are 4 processes, each one (including root) will each get a 2500 x 10 share of the original X as it existed in the root process. If you want to preserve the full matrix in the root process, it is necessary to make a copy of it before calling mpiscatter.

```
	  matrix X
	  if $mpirank == 0
	      X = mnormal(10000, 10)
	  endif
	  mpiscatter(&X, byrows)
```


* * *

mpisend
-------

**Output:** integer


|Arguments:|object (object)|
|----------|---------------|
|          |dest (integer) |


Available only when gretl is in MPI mode (see gretl + MPI). Sends the named object (a matrix, bundle, array, scalar, string or list) from the current process to the one identified by the integer _dest_ (from 0 to the number of MPI processes minus 1).

A call to this function must always be paired with a call to mpirecv in the _dest_ process, as in the following example which sends a matrix from rank 2 to rank 3.

```
	  if $mpirank == 2
	      matrix C = cholesky(A)
	      mpisend(C, 3)
	  elif $mpirank == 3
	      matrix C = mpirecv(2)
	  endif
```


* * *

mpols
-----

**Output:** matrix


|Arguments:|Y (matrix)                       |
|----------|---------------------------------|
|          |X (matrix)                       |
|          |&U (reference to matrix, or null)|


Works exactly as mols, except that the calculations are done in multiple precision using the GMP library.

By default GMP uses 256 bits for each floating point number, but you can adjust this using the environment variable GRETL\_MP\_BITS, e.g. GRETL\_MP\_BITS=1024.

* * *

mrandgen
--------

**Output:** matrix


|Arguments:|d (string)                        |
|----------|----------------------------------|
|          |p1 (scalar or matrix)             |
|          |p2 (scalar or matrix, conditional)|
|          |p3 (scalar, conditional)          |
|          |rows (integer)                    |
|          |cols (integer)                    |


**Examples:** matrix mx = mrandgen(u, 0, 100, 50, 1) matrix mt14 = mrandgen(t, 14, 20, 20) matrix D = mrandgen(dir, {0.5,1,2,4}, 30)

With one exception (see below), this function works like randgen except that the return value is a matrix rather than a series. The initial arguments to this function (the number of which depends on the selected distribution) are as described for randgen, but they must be followed by two integers to specify the row and column dimensions of the desired random matrix. If _p1_ or _p2_ are given in matrix form they must have a number of elements equal to the product of _rows_ and _cols_.

The exceptional case is the Dirichlet distribution. This is a multivariate distribution, and invoking mrandgen with "dir" as first parameter triggers special syntax: the second argument must be a _k_\-element positive vector _a_, and the third a scalar _r_. The function will return an _r_ x _k_ matrix where each row is an independent draw from a Dirichlet distribution with parameter _a_.

The first example above calls for a column vector of length 50 holding draws from a continuous uniform distribution on \[0,100\]. The second example specifies a 20 x 20 random matrix with draws from the _t_ distribution with 14 degrees of freedom; and the third returns a 30 x 4 matrix holding 30 draws from a specified Dirichlet distribution.

See also mnormal, muniform.

* * *

mread
-----

**Output:** matrix


|Arguments:|fname (string)            |
|----------|--------------------------|
|          |import (boolean, optional)|


Reads a matrix from a file named _fname_. If the file name does not contain a full path specification, it will be looked for in several "likely" locations, beginning with the currently set workdir. However, if a non-zero value is given for the optional _import_ argument, the input file is looked for in the user's "dot" directory. This is intended for use with the matrix-exporting functions offered in the context of the foreign command. In this case the _fname_ argument should be a plain filename, without any path component.

Currently, the function recognizes four file formats:

### Native text format

These files are identified by the extension ".mat", and are fully compatible with the Ox matrix file format. If the filename has the suffix ".gz" it is assumed that gzip compression has been applied in writing the data. The file is assumed to be plain text, conforming to the following specification:

*   It starts with zero or more comments, defined as lines that start with the hash mark, #; such lines are ignored.
    
*   The first non-comment line contains two integers, separated by a tab character, indicating the number of rows and columns, respectively.
    
*   The columns are separated by tabs.
    
*   The decimal separator is the dot character, ".".
    

### Binary files

Files with the suffix ".bin" are assumed to be in binary format. The ".gz" suffix, for gzip compression, is also recognized. The first 19 bytes contain the characters gretl\_binary\_matrix, the next 8 bytes contain two 32-bit integers giving the number of rows and columns, and the remainder of the file contains the matrix elements as little-endian "doubles", in column-major order. If gretl is run on a big-endian system, the binary values are converted to little endian on writing, and converted to big endian on reading.

### Delimited text files

If the name of the file to be read has extension ".csv" the rules governing the format of the file are different, and more relaxed. In this case the actual data should _not_ be preceded by a line giving the number of rows and columns. Gretl will try to figure out the delimiter (comma, semicolon or space) and do its best to import the matrix, allowing for use of comma as decimal separator if need be. Note that the delimiter should not be the tab character, on pain of confusing such files with those in gretl's "native" matrix format.

### Gretl dataset files

Files with extension ".gdt" or ".gdtb" are treated as gretl native data files, as created by the store command. In this case, the matrix returned contains the numerical values of the series of the dataset, arranged by column. Note that string-valued series are not read as such; the matrix will just contain their numeric encodings.

See also bread, mwrite.

* * *

mreverse
--------

**Output:** matrix


|Arguments:|X (matrix)               |
|----------|-------------------------|
|          |bycol (boolean, optional)|


Returns a matrix containing the rows of _X_ in reverse order, or the columns in reverse order if the optional second argument has a non-zero value.

* * *

mrls
----

**Output:** matrix


|Arguments:|Y (matrix)                       |
|----------|---------------------------------|
|          |X (matrix)                       |
|          |R (matrix)                       |
|          |q (column vector)                |
|          |&U (reference to matrix, or null)|
|          |&V (reference to matrix, or null)|


Restricted least squares: returns a _k_ x _n_ matrix of parameter estimates obtained by least-squares regression of the _T_ x _n_ matrix _Y_ on the _T_ x _k_ matrix _X_ subject to the linear restriction _RB_ = _q_, where _B_ denotes the stacked coefficient vector. _R_ must have _kn_ columns; each row of this matrix represents a linear restriction. The number of rows in _q_ must match the number of rows in _R_.

If the fifth argument is not null, the _T_ x _n_ matrix _U_ will contain the residuals. If the final argument is given and is not null then the _k_ x _k_ matrix _V_ will hold the restricted counterpart to the matrix _X'X_\-1. The variance matrix of the estimates for equation _i_ can be constructed by multiplying the appropriate sub-matrix of _V_ by an estimate of the error variance for that equation.

* * *

mshape
------

**Output:** matrix


|Arguments:|X (matrix)           |
|----------|---------------------|
|          |r (integer)          |
|          |c (integer, optional)|


Rearranges the elements of _X_ into a matrix with _r_ rows and _c_ columns. Elements are read from _X_ and written to the target in column-major order. If _X_ contains fewer than _k_ = _rc_ elements, the elements are repeated cyclically; otherwise, if _X_ has more elements, only the first _k_ are used.

If the third argument is omitted, _c_ defaults to 1 if _X_ is 1 x 1 otherwise to _N_/_r_ where _N_ is the total number of elements in _X_. However, if _N_ is not an integer multiple of _r_ an error is flagged.

See also cols, rows, unvech, vec, vech.

* * *

msortby
-------

**Output:** matrix


|Arguments:|X (matrix) |
|----------|-----------|
|          |j (integer)|


Returns a matrix in which the rows of _X_ are reordered by increasing value of the elements in column _j_. This is a stable sort: rows that share the same value in column _j_ will not be interchanged.

* * *

msplitby
--------

**Output:** array of matrices


|Arguments:|X (matrix)          |
|----------|--------------------|
|          |v (scalar or matrix)|
|          |bycol (boolean)     |


Returns an array of matrices, the result of splitting _X_ horizontally or vertically under the control of the arguments _v_ and _bycol_. If _bycol_ is nonzero, the matrix will be split by columns; otherwise, as per default, by rows.

The argument _v_ can be either a vector or a scalar.

*   vector: must be of length equal to the relevant (row or column) dimension of _X_, and must contain positive integers. The greatest integer sets the length of the array that is returned. Each element of _v_ indicates the array index of the matrix to which the corresponding row of _X_ should be assigned.
    
*   scalar: the relevant dimension of _X_ (row or column, as dictated by _bycol_) must be an exact multiple of the scalar value. _X_ will be split in chunks with _v_ rows or columns each.
    

In the following example we split a 4 x 3 matrix into three matrices: the first two rows are assigned to the first matrix; the second matrix is left empty; the third and fourth matrices gets row 3 and 4 of _X_, respectively

```
	  matrix X = {1,2,3; 4,5,6; 7,8,9; 10,11,12}
	  matrices M = msplitby(X, {1,1,3,4})
	  print M
```


The print statement gives

```
	  Array of matrices, length 4
	  [1] 2 x 3
	  [2] null
	  [3] 1 x 3
	  [4] 1 x 3
```


The next example splits _X_ evenly:

```
	  matrix X = {1,2,3; 4,5,6; 7,8,9; 10,11,12}
	  matrices MM = msplitby(X, 2)
	  print MM[1]
	  print MM[2]
```


which gives

```
	  ? print MM[1]
	  1   2   3
	  4   5   6

	  ? print MM[2]
	  7    8    9
	  10   11   12
```


See flatten for the inverse operation.

* * *

muniform
--------

**Output:** matrix


|Arguments:|r (integer)          |
|----------|---------------------|
|          |c (integer, optional)|


Returns a matrix with _r_ rows and _c_ columns, filled with uniform (0,1) pseudo-random variates. If omitted, the number of columns defaults to 1 (column vector). Note: the preferred method for generating a scalar uniform r.v. is to use the randgen1 function.

See also mnormal, uniform.

* * *

mweights
--------

**Output:** matrix


|Arguments:|p (integer)             |
|----------|------------------------|
|          |theta (vector)          |
|          |type (integer or string)|


Returns a _p_\-vector of MIDAS weights to be applied to _p_ lags of a high-frequency series, based on the vector _theta_ of hyper-parameters.

The _type_ argument identifies the type of parameterization, which governs the required number of elements, _k_, in _theta_: 1 = normalized exponential Almon (_k_ at least 1, typically 2); 2 = normalized beta with zero last (_k_ = 2); 3 = normalized beta with non-zero last lag (_k_ = 3); and 4 = Almon polynomial (_k_ at least 1). Note that in the normalized beta case the first two elements of _theta_ must be positive.

The _type_ may be given as an integer code, as shown above, or by one of the following strings (respectively): nealmon, beta0, betan, almonp. If a string is used, it should be placed in double quotes. For example, the following two statements are equivalent:

```
	  W = mweights(8, theta, 2)
	  W = mweights(8, theta, "beta0")
```


See also mgradient, midasmult, mlincomb.

* * *

mwrite
------

**Output:** integer


|Arguments:|X (matrix)                |
|----------|--------------------------|
|          |fname (string)            |
|          |export (boolean, optional)|


Writes the matrix _X_ to a file named _fname_. By default this file will be plain text; the first line will hold two integers, separated by a tab character, representing the number of rows and columns; on the following lines the matrix elements appear, in scientific notation, separated by tabs (one line per row). To avoid confusion on reading, files to be written in this format should be named with the suffix ".mat". See below for alternative formats.

If a file _fname_ already exists, it will be overwritten. The nominal return value is 0 on successful completion; if writing fails an error is flagged.

The output file will be written in the currently set workdir, unless the _filename_ string contains a full path specification. However, if a non-zero value is given for the _export_ argument, the output file will be written into the user's "dot" directory, where it is accessible by default via the matrix-loading functions offered in the context of the foreign command. In this case a plain filename, without any path component, should be given for the second argument.

Matrices stored via the mwrite function in its default form can be easily read by other programs; see chapter 17 of the Gretl User's Guide for details.

Three mutually exclusive inflections of this function are available, as follows:

*   If _fname_ has the suffix ".gz" then the file is written in the format described above but with gzip compression.
    
*   If _fname_ has the suffix ".bin" then the matrix is written in binary format. In this case the first 19 bytes contain the characters gretl\_binary\_matrix, the next 8 bytes contain two 32-bit integers giving the number of rows and columns, and the remainder of the file contains the matrix elements as little-endian "doubles", in column-major order. If gretl is run on a big-endian system, the binary values are converted to little endian on writing, and converted to big endian on reading.
    
*   If _fname_ has the suffix ".csv" then the matrix is written in comma-separated format, without a header line indicating the number of rows and columns to follow. This may be easier for third-party programs to handle, but it is not recommended if the matrix file is intended for reading by gretl.
    

Note that if the matrix file is to be read by a third-party program it is not advisable to use the gzip or binary options. But if the file is intended for reading by gretl the alternative formats save space, and the binary format allows for much faster reading of large matrices. The gzip format is not recommended for very large matrices, since decompression can be quite slow.

See also mread. And for writing a matrix to file as a dataset, see store.

* * *

mxtab
-----

**Output:** matrix


|Arguments:|x (series or vector)|
|----------|--------------------|
|          |y (series or vector)|


Returns a matrix holding the cross tabulation of the values contained in _x_ (by row) and _y_ (by column). The two arguments should be of the same type (both series or both column vectors). It is generally expected (though not required) that the arguments will be discrete-valued, with fewer distinct values than observations. Otherwise the cross-tabulation may be very large and not very informative.

See also values, corresp.

* * *

naalen
------

**Output:** matrix


|Arguments:|d (series or vector)             |
|----------|---------------------------------|
|          |cens (series or vector, optional)|


Given a sample of duration data, _d_, possibly accompanied by a record of censoring status, _cens_, computes the Nelson–Aalen nonparametric estimator of the hazard function (Nelson, 1972; Aalen, 1978). The returned matrix has three columns holding, respectively, the sorted unique values in _d_, the estimated cumulated hazard function corresponding to the duration value in column 1, and the standard error of the estimator.

If the _cens_ series is given, the value 0 is taken to indicate an uncensored observation while a value of 1 indicates a right-censored observation (that is, the period of observation of the individual in question has ended before the duration or spell has been recorded as terminated). If _cens_ is not given, it is assumed that all observations are uncensored. (Note: the semantics of _cens_ may be extended at some point to cover other types of censoring.)

See also kmeier.

* * *

nadarwat
--------

**Output:** series


|Arguments:|y (series)             |
|----------|-----------------------|
|          |x (series)             |
|          |h (scalar, optional)   |
|          |LOO (boolean, optional)|
|          |trim (scalar, optional)|


Computes the Nadaraya–Watson nonparametric estimator of the conditional mean of _y_ given _x_. The return value is a series holding _m(x_i_)_, the estimate of _E(y_i_|x_i_)_ for each non-missing element of the series _x_.

The kernel function employed by this estimator is given by _K = exp(-x_2 _/ 2h)_ for _|x| < T_, and zero otherwise. (_T_ = trimming parameter.)

The three optional arguments inflect the behavior of the estimator as described below.

### Bandwidth

The argument _h_ can be used to control the bandwidth, a positive real number. This is usually small; larger values of _h_ make _m(x)_ smoother. A popular choice is to make _h_ proportional to _n_\-0.2. If _h_ is omitted or set to zero, the bandwidth defaults to a data-determined value using the proportionality just mentioned but incorporating the dispersion of the _x_ data as measured by the inter-quartile range or standard deviation; see chapter 40 of the Gretl User's Guide for more details.

### Leave-one-out

"Leave-one-out" is a variant of the algorithm which omits the _i_\-th observation when evaluating _m(x_i_)_. This makes the Nadaraya–Watson estimator more robust numerically and is generally advised when the estimator is computed for inference purposes. This variant is not enabled by default, but is activated if a non-zero value is given for the _LOO_ argument.

### Trimming

The _trim_ argument can be used to control the degree of "trimming", which is imposed to prevent numerical problems when the kernel function is evaluated too far away from zero. This parameter is expressed as a multiple of _h_, the default value being 4. In some cases a value greater than 4 may be preferable. Again see chapter 40 of the Gretl User's Guide for details.

See also loess.

* * *

nelem
-----

**Output:** integer



Returns the number of elements in the argument, which may be a list, a matrix, a bundle, an array or a string, but not a series. In the case of a string argument the number of bytes (which may not be equal to the number of characters in the string) is returned; see also strlen.

* * *

ngetenv
-------

**Output:** scalar

If an environment variable by the name of _s_ is defined and has a numerical value, returns that value; otherwise returns NA. See also getenv.

* * *

nlines
------

**Output:** scalar

Returns a count of the complete lines (that is, lines that end with the newline character) in _buf_.

Example:

```
        string web_page = readfile("http://gretl.sourceforge.net/")
        scalar number = nlines(web_page)
        print number
```


* * *

NMmax
-----

**Output:** scalar


|Arguments:|&b (reference to matrix)    |
|----------|----------------------------|
|          |f (function call)           |
|          |maxfeval (integer, optional)|


Numerical maximization via the Nelder–Mead derivative-free simplex method. On input the vector _b_ should hold the initial values of a set of parameters, and the argument _f_ should specify a call to a function that calculates the (scalar) criterion to be maximized, given the current parameter values and any other relevant data. On successful completion, NMmax returns the maximized value of the criterion, and _b_ holds the parameter values which produce the maximum.

The optional third argument may be used to set the maximum number of function evaluations; if it is omitted or set to zero the maximum defaults to 2000. As a special signal to this function the _maxfeval_ value may be set to a negative number. In this case the absolute value is taken, and NMmax flags an error if the best value found for the objective function at the maximum number of function evaluations is not a local optimum. Otherwise non-convergence in this sense is not treated as an error.

If the object is in fact minimization, either the function call should return the negative of the criterion or alternatively NMmax may be called under the alias NMmin.

For more details and examples chapter 37 of the Gretl User's Guide. See also simann.

* * *

NMmin
-----

**Output:** scalar

An alias for NMmax; if called under this name the function acts as a minimizer.

* * *

nobs
----

**Output:** scalar or series



If _x_ is a series, returns the number of non-missing observations for this series in the currently selected sample.

If _x_ is a list, returns a series _y_ such that _y_t is the count of the series in the list that have a non-missing value at observation _t_.

See also pnobs, pxnobs.

* * *

normal
------

**Output:** series


|Arguments:|μ (scalar)|
|----------|----------|
|          |σ (scalar)|


Generates a series of Gaussian pseudo-random variates with mean μ and standard deviation σ. If no arguments are supplied, standard normal variates _N_(0,1) are produced. The values are produced using the Ziggurat method (Marsaglia and Tsang, 2000).

See also randgen, mnormal, muniform.

* * *

normtest
--------

**Output:** matrix


|Arguments:|y (series or vector)     |
|----------|-------------------------|
|          |method (string, optional)|


Carries out one or more tests for normality of _y_. By default the Doornik–Hansen test is performed but the optional _method_ argument can be used to select an alternative: use swilk to get the Shapiro–Wilk test, jbera for Jarque–Bera test, or lillie for the Lilliefors test. Or give all for the _method_ argument to carry out all four tests.

The second argument may be given in either quoted or unquoted form. In the latter case, however, if the argument is the name of a string variable the value of the variable is substituted.

The returned matrix is 1 x 2 for a single test, or 4 x 2 if all tests are performed. Test statistics are found in the first column and p-values in the second. The test statistic does not follow the same distribution is all cases. For Doornik–Hansen and Jarque–Bera it is chi-square(2); for the other methods it is an idiosyncratic statistic whose p-value requires special calculation.

See also the normtest command.

* * *

npcorr
------

**Output:** matrix


|Arguments:|x (series or vector)     |
|----------|-------------------------|
|          |y (series or vector)     |
|          |method (string, optional)|


Calculates a measure of correlation between _x_ and _y_ using a nonparametric method. If given, the third argument should be either kendall (for Kendall's tau, version b, the default method) or spearman (for Spearman's rho).

The return value is a 3-vector holding the correlation measure plus a test statistic and p-value for the null hypothesis of no correlation. Note that if the sample size is too small the test statistic and/or p-value may be NaN (not a number, or missing).

See also corr for Pearson correlation.

* * *

npv
---

**Output:** scalar


|Arguments:|x (series or vector)|
|----------|--------------------|
|          |r (scalar)          |


Returns the Net Present Value of _x_, considered as a sequence of payments (negative) and receipts (positive), evaluated at annual discount rate _r_, which must be expressed as a decimal fraction, not a percentage (0.05 rather than 5%). The first value is taken as dated "now" and is not discounted. To emulate an NPV function in which the first value is discounted, prepend zero to the input sequence.

Supported data frequencies are annual, quarterly, monthly, and undated (undated data are treated as if annual).

See also irr.

* * *

NRmax
-----

**Output:** scalar


|Arguments:|&b (reference to matrix)   |
|----------|---------------------------|
|          |f (function call)          |
|          |g (function call, optional)|
|          |h (function call, optional)|


Numerical maximization via the Newton–Raphson method. On input the vector _b_ should hold the initial values of a set of parameters, and the argument _f_ should specify a call to a function that calculates the (scalar) criterion to be maximized, given the current parameter values and any other relevant data. If the object is in fact minimization, this function should return the negative of the criterion. On successful completion, NRmax returns the maximized value of the criterion, and _b_ holds the parameter values which produce the maximum.

The optional third and fourth arguments provide means of supplying analytical derivatives and an analytical (negative) Hessian, respectively. The functions referenced by _g_ and _h_ must take as their first argument a predefined matrix that is of the correct size to contain the gradient or Hessian, respectively, given in pointer form. They also must take the parameter vector as an argument (in pointer form or otherwise). Other arguments are optional. If either or both of the optional arguments are omitted, a numerical approximation is used.

For more details and examples see chapter 37 of the Gretl User's Guide. See also BFGSmax, fdjac.

* * *

NRmin
-----

**Output:** scalar

An alias for NRmax; if called under this name the function acts as a minimizer.

* * *

nullspace
---------

**Output:** matrix

Computes the right nullspace of _A_, via the singular value decomposition: the result is a matrix _B_ such that the product _AB_ is a zero matrix, except when _A_ has full column rank, in which case an empty matrix is returned. Otherwise, if _A_ is _m_ x _n_, _B_ will be _n_ by (_n_ – _r_), where _r_ is the rank of _A_.

If _A_ is not of full column rank, then the vertical concatenation of _A_ and the transpose of _B_ produces a full rank matrix.

Example:

```
      A = mshape(seq(1,6),2,3)
      B = nullspace(A)
      C = A | B'

      print A B C

      eval A*B
      eval rank(C)
```


Produces

```
      ? print A B C
      A (2 x 3)

      1   3   5
      2   4   6

      B (3 x 1)

      -0.5
         1
      -0.5

      C (3 x 3)

         1      3      5
         2      4      6
      -0.5      1   -0.5

      ? eval A*B
      -4.4409e-16
      -4.4409e-16

      ? eval rank(C)
      3
```


See also rank, svd.

* * *

numhess
-------

**Output:** matrix


|Arguments:|b (column vector)    |
|----------|---------------------|
|          |fcall (function call)|
|          |d (scalar, optional) |


Calculates a numerical approximation to the Hessian associated with the _n_\-vector _b_ and the objective function specified by the argument _fcall_. The function call should take _b_ as its first argument (either straight or in pointer form), followed by any additional arguments that may be needed, and it should return a scalar result. On successful completion numhess returns an _n_ x _n_ matrix holding the Hessian, which is exactly symmetric by construction.

The method used is Richardson extrapolation, with four steps. The optional third argument can be used to set the fraction _d_ of the parameter value used in setting the initial step size; if this argument is omitted the default is _d_ = 0.01.

Here is an example of usage:

```
	  matrix H = numhess(theta, myfunc(&theta, X))
```


See also BFGSmax, fdjac.

* * *

obs
---

**Output:** series

Returns a series of consecutive integers, setting 1 at the start of the dataset. Note that the result is invariant to subsampling. This function is especially useful with time-series datasets. Note: you can write t instead of obs with the same effect.

See also obsnum.

* * *

obslabel
--------

**Output:** string or array of strings



If _t_ is a scalar, returns a single string, the observation label for observation _t_. The inverse function is provided by obsnum.

If _t_ is a vector, returns an array of strings, the observation labels for the observations given by the elements of _t_.

In either case the _t_ values must be integers, valid as 1-based indices of observations in the current dataset, otherwise an error is flagged.

* * *

obsnum
------

**Output:** integer

Returns an integer corresponding to the observation specified by the string _s_. Note that the result is invariant to subsampling. This function is especially useful with time-series datasets. For example, the following code

```
	  open denmark
	  k = obsnum(1980:1)
```


yields k = 25, indicating that the first quarter of 1980 is the 25th observation in the denmark dataset.

See also obs, obslabel.

* * *

ok
--

**Output:** see below



If _x_ is a scalar, returns 1 if _x_ is not NA, otherwise 0. If _x_ is a series, returns a series with value 1 at observations with non-missing values and zeros elsewhere. If _x_ is a list, the output is a series with 0 at observations for which at least one series in the list has a missing value, and 1 otherwise.

If _x_ is a matrix the function returns a matrix of the same dimensions as _x_, with 1s in positions corresponding to finite elements of _x_ and 0s in positions where the elements are non-finite (either infinities or not-a-number, as per the IEEE 754 standard).

See also missing, misszero, zeromiss. But note that these functions are not applicable to matrices.

* * *

onenorm
-------

**Output:** scalar

Returns the 1-norm of the matrix _X_, that is, the maximum across the columns of _X_ of the sum of absolute values of the column elements.

See also infnorm, rcond.

* * *

ones
----

**Output:** matrix


|Arguments:|r (integer)          |
|----------|---------------------|
|          |c (integer, optional)|


Outputs a matrix with _r_ rows and _c_ columns, filled with ones. If omitted, the number of columns defaults to 1 (column vector).

See also seq, zeros.

* * *

orthdev
-------

**Output:** series

Only applicable if the currently open dataset has a panel structure. Computes the forward orthogonal deviations for variable _y_.

This transformation is sometimes used instead of differencing to remove individual effects from panel data. For compatibility with first differences, the deviations are stored one step ahead of their true temporal location (that is, the value at observation _t_ is the deviation that, strictly speaking, belongs at _t_ – 1). That way one loses the first observation in each time series, not the last.

See also diff.

* * *

pdf
---

**Output:** same type as input


|Arguments:|d (string)                  |
|----------|----------------------------|
|          |... (see below)             |
|          |x (scalar, series or matrix)|


**Examples:** f1 = pdf(N, -2.5) f2 = pdf(X, 3, y) f3 = pdf(W, shape, scale, y)

Probability density function calculator. Returns the density at _x_ of the distribution identified by the code _d_. See cdf for details of the required (scalar) arguments. The distributions supported by the pdf function are the normal, Student's _t_, chi-square, _F_, Gamma, Beta, Exponential, Weibull, Laplace, Generalized Error, Binomial and Poisson. Note that for the Binomial and the Poisson what's calculated is in fact the probability mass at the specified point. For Student's _t_, chi-square, _F_ the noncentral variants are supported too.

For the normal distribution, see also dnorm.

* * *

pergm
-----

**Output:** matrix


|Arguments:|x (series or vector)        |
|----------|----------------------------|
|          |bandwidth (scalar, optional)|


If only the first argument is given, computes the sample periodogram for the given series or vector. If the second argument is given, computes an estimate of the spectrum of _x_ using a Bartlett lag window of the given bandwidth, up to a maximum of half the number of observations (_T_/2).

Returns a matrix with two columns and _T_/2 rows: the first column holds the frequency, ω, from 2π/_T_ to π, and the second the corresponding spectral density.

* * *

pexpand
-------

**Output:** series


|Arguments:|v (vector)                       |
|----------|---------------------------------|
|          |by_individual (boolean, optional)|


Only applicable if the currently open dataset has a panel structure. By default, performs the inverse operation of pshrink. That is, given a vector of length equal to the number of individuals in the current panel sample, it returns a series in which each value is repeated _T_ times, for _T_ the time-series length of the panel. The resulting series is therefore non-time varying.

If a non-zero value is given for _by\_individual_, the length of _v_ should equal _T_ and repetition is across the individuals in the panel.

* * *

pmax
----

**Output:** series


|Arguments:|y (series)             |
|----------|-----------------------|
|          |mask (series, optional)|


Only applicable if the current dataset has a panel structure. Returns a series holding the maxima of variable _y_ for each cross-sectional unit (repeated for each time period).

If the optional second argument is provided then observations for which the value of _mask_ is zero are ignored.

See also pmin, pmean, pnobs, psd, pxsum, pshrink, psum.

* * *

pmean
-----

**Output:** series


|Arguments:|y (series)             |
|----------|-----------------------|
|          |mask (series, optional)|


Only applicable if the current dataset has a panel structure. Returns a series holding the time-mean of variable _y_ for each cross-sectional unit, the values being repeated for each period. Missing observations are skipped in calculating the means.

If the optional second argument is provided then observations for which the value of _mask_ is zero are ignored.

See also pmax, pmin, pnobs, psd, pxsum, pshrink, psum.

* * *

pmin
----

**Output:** series


|Arguments:|y (series)             |
|----------|-----------------------|
|          |mask (series, optional)|


Only applicable if the current dataset has a panel structure. Returns a series holding the minima of variable _y_ for each cross-sectional unit (repeated for each time period).

If the optional second argument is provided then observations for which the value of _mask_ is zero are ignored.

See also pmax, pmean, pnobs, psd, pshrink, psum.

* * *

pnobs
-----

**Output:** series


|Arguments:|y (series)             |
|----------|-----------------------|
|          |mask (series, optional)|


Only applicable if the current dataset has a panel structure. Returns a series holding the number of valid observations of variable _y_ for each cross-sectional unit (repeated for each time period).

If the optional second argument is provided then observations for which the value of _mask_ is zero are ignored.

See also pmax, pmin, pmean, psd, pshrink, psum.

* * *

polroots
--------

**Output:** matrix

Finds the roots of a polynomial. If the polynomial is of degree _p_, the vector _a_ should contain _p_ + 1 coefficients in ascending order, i.e. starting with the constant and ending with the coefficient on _x_p.

The return value is a complex column vector of length _p_.

* * *

polyfit
-------

**Output:** series


|Arguments:|y (series) |
|----------|-----------|
|          |q (integer)|


Fits a polynomial trend of order _q_ to the input series _y_ using the method of orthogonal polynomials. The series returned holds the fitted values.

* * *

princomp
--------

**Output:** matrix


|Arguments:|X (matrix)                |
|----------|--------------------------|
|          |p (integer)               |
|          |covmat (boolean, optional)|


Let the matrix _X_ be _T_ x _k_, containing _T_ observations on _k_ variables. The argument _p_ must be a positive integer less than or equal to _k_. This function returns a _T_ x _p_ matrix, _P_, holding the first _p_ principal components of _X_.

The optional third argument acts as a boolean switch: if it is non-zero the principal components are computed on the basis of the covariance matrix of the columns of _X_ (the default is to use the correlation matrix).

The elements of _P_ are computed as the sum from _i_ to _k_ of _Z_ti times _v_ji, where _Z_ti is the standardized value (or just the centered value, if the covariance matrix is used) of variable _i_ at observation _t_ and _v_ji is the _j_th eigenvector of the correlation (or covariance) matrix of the _X_is, with the eigenvectors ordered by decreasing value of the corresponding eigenvalues.

See also eigensym.

* * *

prodc
-----

**Output:** row vector


|Arguments:|X (matrix)                 |
|----------|---------------------------|
|          |skip_na (boolean, optional)|


Returns the product of the elements of _X_, by column. If a non-zero value is given for the optional second argument missing values are ignored, otherwise the result is NA for any columns that contain missing values. Note that specifying _skip\_na_ is equivalent to treating missing values as if they were 1s.

See also prodr, meanc, sdc, sumc.

* * *

prodr
-----

**Output:** column vector


|Arguments:|X (matrix)                 |
|----------|---------------------------|
|          |skip_na (boolean, optional)|


Returns the product of the elements of _X_, by row. If a non-zero value is given for the optional second argument missing values are ignored, otherwise the result is NA for any rows that contain missing values. Note that specifying _skip\_na_ is equivalent to treating missing values as if they were 1s.

See also prodc, meanr, sumr.

* * *

psd
---

**Output:** series


|Arguments:|y (series)             |
|----------|-----------------------|
|          |mask (series, optional)|


Only applicable if the current dataset has a panel structure. Returns a series holding the sample standard deviation of variable _y_ for each cross-sectional unit (with the values repeated for each time period). The denominator used is the sample size for each unit minus 1, unless the number of valid observations for the given unit is 1 (in which case 0 is returned) or 0 (in which case NA is returned).

If the optional second argument is provided then observations for which the value of _mask_ is zero are ignored.

Note: this function makes it possible to check whether a given variable (say, X) is time-invariant via the condition max(psd(X)) == 0.

See also pmax, pmin, pmean, pnobs, pshrink, psum.

* * *

psdroot
-------

**Output:** square matrix


|Arguments:|A (symmetric matrix)        |
|----------|----------------------------|
|          |psdcheck (boolean, optional)|


Performs a generalized variant of the Cholesky decomposition of the matrix _A_, which must be positive semidefinite (but may be singular). If the input matrix is not square an error is flagged, but symmetry is assumed and not tested; only the lower triangle of _A_ is read. The result is a lower-triangular matrix _L_ which satisfies _A = LL'_. Indeterminate elements in the solution are set to zero.

To force a check on the positive semidefiniteness of _A_, give a non-zero value for the optional second argument. In that case an error is flagged if the maximum absolute value of _A – LL'_ exceeds 1.0e-8. Such a check can also be performed manually:

```
	  L = psdroot(A)
	  chk = maxc(maxr(abs(A - L*L')))
```


For the case where _A_ is positive definite, see cholesky.

* * *

pshrink
-------

**Output:** matrix

Only applicable if the current dataset has a panel structure. Returns a column vector holding the first valid observation for the series _y_ for each cross-sectional unit in the panel, over the current sample range. If a unit has no valid observations for the input series it is skipped.

This function provides a means of compacting the series returned by functions such as pmax and pmean, in which a value pertaining to each cross-sectional unit is repeated for each time period.

See pexpand for the inverse operation.

* * *

psum
----

**Output:** series


|Arguments:|y (series)             |
|----------|-----------------------|
|          |mask (series, optional)|


This function is applicable only if the current dataset has a panel structure. It returns a series holding the sum over time of variable _y_ for each cross-sectional unit, the values being repeated for each period. Missing observations are skipped in calculating the sums.

If the optional second argument is provided then observations for which the value of _mask_ is zero are ignored.

See also pmax, pmean, pmin, pnobs, psd, pxsum, pshrink.

* * *

pvalue
------

**Output:** same type as input


|Arguments:|c (character)               |
|----------|----------------------------|
|          |... (see below)             |
|          |x (scalar, series or matrix)|


**Examples:** p1 = pvalue(z, 2.2) p2 = pvalue(X, 3, 5.67) p2 = pvalue(F, 3, 30, 5.67)

_P_\-value calculator. Returns _P(X > x)_, where the distribution of _X_ is determined by the character _c_. Between the arguments _c_ and _x_, zero or more additional arguments are required to specify the parameters of the distribution; see cdf for details. The distributions supported by the pvalue function are the standard normal, _t_, Chi square, _F_, gamma, binomial, Poisson, Exponential, Weibull, Laplace and Generalized Error.

See also critical, invcdf, urcpval, imhof.

* * *

pxnobs
------

**Output:** series


|Arguments:|y (series)             |
|----------|-----------------------|
|          |mask (series, optional)|


Only applicable if the current dataset has a panel structure. Returns a series holding the number of valid observations of _y_ in each time period (this count being repeated for each unit).

If the optional second argument is provided then observations for which the value of _mask_ is zero are ignored.

Note that this function works in a different dimension from the pnobs function.

* * *

pxsum
-----

**Output:** series


|Arguments:|y (series)             |
|----------|-----------------------|
|          |mask (series, optional)|


Only applicable if the current dataset has a panel structure. Returns a series holding the sum of the values of _y_ for each cross-sectional unit in each period (the values being repeated for each unit).

If the optional second argument is provided then observations for which the value of _mask_ is zero are ignored.

Note that this function works in a different dimension from the psum function.

* * *

qform
-----

**Output:** matrix


|Arguments:|x (matrix)          |
|----------|--------------------|
|          |A (symmetric matrix)|


Computes the quadratic form _Y = xAx'_. Using this function instead of ordinary matrix multiplication guarantees more speed and better accuracy, when _A_ is a generic symmetric matrix. However, in the special case when _A_ is the identity matrix, the simple expression x'x performs much better than qform(x',I(rows(x)).

In the special case when _A_ is a diagonal matrix, the second argument can be given as a vector of the appropriate size, which is understood to contain the main diagonal of _A_. In this case, a more efficient algorithm is used.

If _x_ and _A_ are not conformable, or _A_ is not symmetric, an error is returned.

* * *

qlrpval
-------

**Output:** scalar


|Arguments:|X2 (scalar) |
|----------|------------|
|          |df (integer)|
|          |p1 (scalar) |
|          |p2 (scalar) |


_P_\-values for the test statistic from the QLR sup-Wald test for a structural break at an unknown point (see qlrtest), as per Bruce Hansen (1997).

The first argument, _X2_, denotes the (chi-square form of) the maximum Wald test statistic and _df_ denotes its degrees of freedom. The third and fourth arguments represent, as decimal fractions of the overall estimation range, the starting and ending points of the central range of observations over which the successive Wald tests are calculated. For example if the standard approach of 15 percent trimming is adopted, you would set _p1_ to 0.15 and _p2_ to 0.85.

See also pvalue, urcpval.

* * *

qnorm
-----

**Output:** same type as input



Returns quantiles for the standard normal distribution. If _x_ is not between 0 and 1, NA is returned. See also cnorm, dnorm.

* * *

qrdecomp
--------

**Output:** matrix


|Arguments:|X (matrix)                       |
|----------|---------------------------------|
|          |&R (reference to matrix, or null)|
|          |&P (reference to matrix, or null)|


Computes the "thin" QR decomposition of an _m_ x _n_ matrix _X_ with _m_ ≥ _n_, such that _X = QR_ where _Q_ is an _m_ x _n_ orthogonal matrix and _R_ is an _n_ x _n_ upper triangular matrix. The matrix _Q_ is returned directly, while _R_ can be retrieved via the optional second argument.

If the optional third argument is supplied the decomposition employs column pivoting, and on successful completion _P_ holds the final ordering of the columns in the form of a row vector. If the columns are not in fact reordered _P_ will compare equal to seq(1, n).

See also eigengen, eigensym, svd.

* * *

quadtable
---------

**Output:** matrix


|Arguments:|n (integer)             |
|----------|------------------------|
|          |type (integer, optional)|
|          |a (scalar, optional)    |
|          |b (scalar, optional)    |


Returns an _n_ x 2 matrix for use with Gaussian quadrature (numerical integration). The first column holds the nodes or abscissae, the second the weights.

The first argument specifies the number of points (rows) to compute. The second argument codes for the type of quadrature: use 1 for Gauss–Hermite (the default); 2 for Gauss–Legendre; or 3 for Gauss–Laguerre. The significance of the optional parameters _a_ and _b_ depends on the selected _type_, as explained below.

Gaussian quadrature is a method of approximating numerically the definite integral of some function of interest. Let the function be represented as the product _f(x)W(x)_. The types of quadrature differ in the specification of the component _W(x)_: in the Hermite case this is exp(–_x_2); in the Laguerre case, exp(–_x_); and in the Legendre case simply _W(x)_ = 1.

For each specification of _W_, one can compute a set of nodes, _x_i, and weights, _w_i, such that the sum from _i_\=1 to _n_ of _w_i _f_(_x_i) approximates the desired integral. The method of Golub and Welsch (1969) is used.

When the Gauss–Legendre type is selected, the optional arguments _a_ and _b_ can be used to control the lower and upper limits of integration, the default values being –1 and 1. (In Hermite quadrature the limits are fixed at minus and plus infinity, while in the Laguerre case they are fixed at 0 and infinity.)

In the Hermite case _a_ and _b_ play a different role: they can be used to replace the default form of _W_(_x_) with the (closely related) normal distribution with mean _a_ and standard deviation _b_. Supplying values of 0 and 1 for these parameters, for example, has the effect of making _W_(_x_) into the standard normal pdf, which is equivalent to multiplying the default nodes by the square root of two and dividing the weights by the square root of π.

* * *

quantile
--------

**Output:** scalar or matrix


|Arguments:|y (series or matrix)|
|----------|--------------------|
|          |p (scalar or vector)|


If _y_ is a series, returns the _p_\-quantile for the series. For example, when _p_ = 0.5, the median is returned.

If _y_ is a matrix, returns a row vector containing the _p_\-quantiles for the columns of _y_; that is, each column is treated as a series.

In addition, for matrix _y_ an alternate form of the second argument is supported: _p_ may be given as a vector. In that case the return value is an _m_ x _n_ matrix, where _m_ is the number of elements in _p_ and _n_ is the number of columns in _y_.

Hyndman and Fan (1996) describe nine variant methods for calculating sample quantiles. The default method in gretl is the one they call _Q_6 (which is also the default in Python). Method _Q_7 (the default in R) or _Q_8 (the one recommended by Hyndman and Fan) can be selected instead via the set command, as in

```
	  set quantile_type Q7 # or Q8
```


For example, the code

```
	  set verbose off
	  matrix x = seq(1,7)'
	  set quantile_type Q6
	  printf "Q6: %g\n", quantile(x, 0.45)
	  set quantile_type Q7
	  printf "Q7: %g\n", quantile(x, 0.45)
	  set quantile_type Q8
	  printf "Q8: %g\n", quantile(x, 0.45)
```


produces the following output:

```
	  Q6: 3.6
	  Q7: 3.7
	  Q8: 3.63333
```


* * *

randgen
-------

**Output:** series


|Arguments:|d (string)                        |
|----------|----------------------------------|
|          |p1 (see below)                    |
|          |p2 (scalar or series, conditional)|
|          |p3 (scalar, conditional)          |


**Examples:** series x = randgen(u, 0, 100) series t14 = randgen(t, 14) series y = randgen(B, 0.6, 30) series g = randgen(G, 1, 1) series P = randgen(P, mu)

All-purpose random number generator. The argument _d_ is a string (in most cases just a single character) which specifies the distribution from which the pseudo-random numbers should be drawn. The arguments _p1_ to _p3_ specify the parameters of the selected distribution; the number of such parameters (and, in some cases, their nature) depends on the distribution.

For distributions other than the beta-binomial and the generic discrete, the parameters _p1_ and (if applicable) _p2_ may be given as either scalars or series: if they are given as scalars the output series is identically distributed, while if a series is given for _p1_ or _p2_ the distribution is conditional on the parameter value at each observation.

The two special cases have the following requirements:

*   beta-binomial: all three parameters must be scalar.
    
*   generic discrete: a single parameter is wanted, namely a _k_\-vector whose elements represent the probabilities for an integer-valued random variable with support from 1 to _k_.
    

Specifics are given below: the string code for each distribution is shown in parentheses, followed by the interpretation of the arguments _p1_ and, where applicable, _p2_ and _p3_.

*   Uniform (continuous) (u or U): minimum, maximum
    
*   Uniform (discrete) (i): minimum, maximum
    
*   Normal (z, n, or N): mean, standard deviation
    
*   Student's t (t): degrees of freedom
    
*   Chi square (c, x, or X): degrees of freedom
    
*   Snedecor's F (f or F): df (num.), df (den.)
    
*   Gamma (g or G): shape, scale
    
*   Binomial (b or B): probability, number of trials
    
*   Poisson (p or P): mean
    
*   Exponential (exp): scale
    
*   Logistic (lgt or s): location, scale
    
*   Weibull (w or W): shape, scale
    
*   Laplace (l or L): mean, scale
    
*   Generalized Error (E): shape
    
*   Beta (beta): shape1, shape2
    
*   Beta-Binomial (bb): trials, shape1, shape2
    
*   Generic discrete (disc): probabilities
    

See also normal, uniform, mrandgen, randgen1.

* * *

randgen1
--------

**Output:** scalar


|Arguments:|d (character)           |
|----------|------------------------|
|          |p1 (scalar)             |
|          |p2 (scalar, conditional)|


**Examples:** scalar x = randgen1(z, 0, 1) scalar g = randgen1(g, 3, 2.5)

Works like randgen except that the return value is a scalar rather than a series.

The first example above calls for a value from the standard normal distribution, while the second specifies a drawing from the Gamma distribution with shape 3 and scale 2.5.

See also mrandgen.

* * *

randint
-------

**Output:** integer


|Arguments:|min (integer)|
|----------|-------------|
|          |max (integer)|


Returns a pseudo-random integer in the closed interval \[_min_, _max_\]. See also randgen.

* * *

randperm
--------

**Output:** vector


|Arguments:|n (integer)          |
|----------|---------------------|
|          |k (integer, optional)|


If only the first argument is given, returns a row vector containing a random permutation of the integers from 1 to _n_, without repetition of elements. If the second argument is given it must be a positive integer in the range 1 to _n_; in this case the function returns a row vector containing _k_ integers selected randomly from 1 to _n_ without replacement.

If you wish to sample _k_ rows from a matrix X with _n_ rows (without replacement), that can be accomplished as shown below:

```
	  matrix S = X[randperm(n, k),]
```


And if you wish to preserve the original order of the rows in the sample:

```
	  matrix S = X[sort(randperm(n, k)),]
```


See also resample for resampling with replacement.

* * *

randstr
-------

**Output:** string

Returns a random string of length _n_ bytes. The string includes the numerals 0 to 9 and the lower-case letters a to f with equal probability, and is interpretable as a hexadecimal integer. Intended usage is as a unique identifier. For example, with _n_ = 16 the string will one of over 1019 possibilities and so unique with probability close to 1.

* * *

rank
----

**Output:** integer


|Arguments:|X (matrix)            |
|----------|----------------------|
|          |tol (scalar, optional)|


Returns the rank of the _r_ x _c_ matrix _X_, numerically computed via the singular value decomposition.

The result of this operation is the number of singular values of _X_ that are found to be numerically greater than 0. The _tol_ optional parameter can be used for tweaking this aspect. Singular values are considered to be non-zero if they are greater than _m × tol × s_, where _m_ is the greater of _r_ and _c_ and _s_ is the largest singular value. If the second argument is omitted _tol_ is set to machine epsilon (see $macheps). In some cases, you may want to set _tol_ to a larger value (eg 1.0e-9) in order to avoid overestimating the rank of _X_, which may lead to numerically unstable results.

See also svd.

* * *

ranking
-------

**Output:** same type as input



Returns a series or vector with the ranks of _y_. The rank for observation _i_ is the number of elements that are less than _y_i plus one half the number of elements that are equal to _y_i. (Intuitively, you may think of chess points, where victory gives you one point and a draw gives you half a point.) One is added so the lowest rank is 1 instead of 0.

See also sort, sortby.

* * *

rcond
-----

**Output:** scalar



Returns the reciprocal condition number for _A_ with respect to the 1-norm. In many circumstances, this is a better measure of the sensitivity of _A_ to numerical operations such as inversion than the determinant.

The value is computed as the reciprocal of the product, 1-norm of _A_ times 1-norm of _A_\-inverse.

See also det, ldet, onenorm.

* * *

Re
--

**Output:** matrix



Returns a real matrix of the same dimensions as _C_, holding the real part of the input matrix. See also Im.

* * *

readfile
--------

**Output:** string


|Arguments:|fname (string)            |
|----------|--------------------------|
|          |codeset (string, optional)|


If a file by the name of _fname_ exists and is readable, returns a string containing the content of this file, otherwise flags an error. If _fname_ does not contain a full path specification, it will be looked for in several "likely" locations, beginning with the currently set workdir. If the file in question is gzip-compressed, this is handled transparently.

If _fname_ starts with the identifier of a supported internet protocol (http://, ftp:// or https://), libcurl is invoked to download the resource. See also curl for more elaborate downloading operations.

If the text to be read is not encoded in UTF-8, gretl will try recoding it from the current locale codeset if that is not UTF-8, or from ISO-8859-15 otherwise. If this simple default does not meet your needs you can use the optional second argument to specify a codeset. For example, if you want to read text in Microsoft codepage 1251 and that is not your locale codeset, you should give a second argument of "cp1251".

Examples:

```
        string web_page = readfile("http://gretl.sourceforge.net/")
        print web_page

        string current_settings = readfile("@dotdir/.gretl2rc")
        print current_settings
```


Also see the sscanf and getline functions.

* * *

regsub
------

**Output:** same type as input


|Arguments:|s (string, strings array or string-valued series)|
|----------|-------------------------------------------------|
|          |match (string)                                   |
|          |repl (string)                                    |


If _s_ is a single string, returns a copy of _s_ in which all occurrences of the pattern _match_ are replaced using _repl_. The arguments _match_ and _repl_ are interpreted as Perl-style regular expressions. If _s_ is an array of strings or string-valued series this operation is performed on each string in the array or series.

See also strsub for simple substitution of literal strings.

* * *

remove
------

**Output:** integer

If a file by the name of _fname_ exists and is writable by the user, this function removes (deletes) the file and returns 0. If there is no such file or for some reason the file cannot be deleted, a non-zero error code is returned.

If _fname_ does not specify a full path, it is taken to be relative to the current workdir.

* * *

replace
-------

**Output:** same type as input


|Arguments:|x (series or matrix)    |
|----------|------------------------|
|          |find (scalar or vector) |
|          |subst (scalar or vector)|


Replaces each element of _x_ equal to the _i_\-th element of _find_ with the corresponding element of _subst_.

If _find_ is a scalar, _subst_ must also be a scalar. If _find_ and _subst_ are both vectors, they must have the same number of elements. But if _find_ is a vector and _subst_ a scalar, then all matches will be replaced by _subst_.

Example:

```
	  a = {1,2,3;3,4,5}
	  find = {1,3,4}
	  subst = {-1,-8, 0}
	  b = replace(a, find, subst)
	  print a b
```


produces

```
          a (2 x 3)

          1   2   3
          3   4   5

          b (2 x 3)

          -1    2   -8
          -8    0    5
```


* * *

resample
--------

**Output:** same type as input


|Arguments:|x (series or matrix)         |
|----------|-----------------------------|
|          |blocksize (integer, optional)|
|          |draws (integer, optional)    |


The initial description of this function pertains to cross-sectional or time-series data; see below for the case of panel data.

Resamples from _x_ with replacement. In the case of a series argument, each value of the returned series, _y_t, is drawn from among all the values of _x_t with equal probability. When a matrix argument is given, each row of the returned matrix is drawn from the rows of _x_ with equal probability. See also randperm for sampling rows from a matrix without replacement.

The optional argument _blocksize_ represents the block size for resampling by moving blocks. If this argument is given it should be a positive integer greater than or equal to 2. The effect is that the output is composed by random selection with replacement from among all the possible contiguous sequences of length _blocksize_ in the input. (In the case of matrix input, this means contiguous rows.) If the length of the data is not an integer multiple of the block size, the last selected block is truncated to fit.

### Number of draws

By default the number of resampled observations in the output is equal to that in the input—if _x_ is a series, the length of the current sample range; if _x_ is a matrix, its number of rows. In the matrix case _only_ this can be adjusted via the optional third argument, which must be a positive integer. Note that if _blocksize_ is greater than 1, _draws_ refers to the number of individual observations, not the number of blocks.

### Panel data

If the argument _x_ is a series and the dataset takes the form of a panel, resampling by moving blocks is not supported. The basic form of resampling is supported, but has this specific interpretation: the data are resampled "by individual". Suppose you have a panel in which 100 individuals are observed over 5 periods. Then the returned series will again be composed of 100 blocks of 5 observations: each block will be drawn with equal probability from the 100 individual time series, with the time-series order preserved.

* * *

rgbmix
------

**Output:** array of strings


|Arguments:|color1 (string)         |
|----------|------------------------|
|          |color2 (string)         |
|          |f (matrix)              |
|          |plot (boolean, optional)|


Given two colors and a vector _f_ of length _n_ containing values in \[0,1\], this function returns an array of _n_ strings, element _i_ of which holds the hexadecimal RGB code for a mixture of the form (1-_f_i) × color1 + _f_i × color2. The weighted average is taken over the Red, Green and Blue channels of the input colors.

The color arguments can be specified by names known to gnuplot, or as hexadecimal values in the form 0xrrggbb or #rrggbb. Hex values in the first of these forms may be given numerically, otherwise strings are needed. If a non-zero value is given for the _plot_ argument, a plot that shows the color mixtures is produced.

This function offers a means of generating a set of related colors for plotting purposes, the primary use case being specification of multiple bands in a plot (for example, to indicate confidence intervals at more than one level). Three examples follow: the first produces successive lightenings of an initial blue; the second progressive darkenings of a pink shade; and the third a transition from red to yellow.

```
	  f = {0, 0.5, 0.75, 0.875, 0.9375}
	  mixes = rgbmix(0x1b43dc, "white", f, 1)
	  print mixes
	  f = {0, 0.1, 0.2, 0.3, 0.4}
	  rgbmix(0xefd0d3, "black", f, 1)
	  f = {0, 0.2, 0.4, 0.6, 0.8, 1}
	  rgbmix("red", "yellow", f, 1)
```


The output from the print command in the first example is

```
	  [1] "0x1b43dc"
	  [2] "0x8da1ee"
	  [3] "0xc6d0f6"
	  [4] "0xe2e8fb"
	  [5] "0xf1f3fd"
```


* * *

round
-----

**Output:** same type as input



Rounds to the nearest integer. Note that when _x_ lies halfway between two integers, rounding is done "away from zero", so for example 2.5 rounds to 3, but round(-3.5) gives –4. This is a common convention in spreadsheet programs, but other software may yield different results. See also ceil, floor, int.

* * *

rnameget
--------

**Output:** string or array of strings


|Arguments:|M (matrix)           |
|----------|---------------------|
|          |r (integer, optional)|


If the _r_ argument is given, retrieves the name for row _r_ of matrix _M_. If _M_ has no row names attached the value returned is an empty string; if _r_ is out of bounds for the given matrix an error is flagged.

If no second argument is given, retrieves an array of strings holding the row names from _M_, or an empty array if the matrix does not have row names attached.

Example:

```
	  matrix A = { 11, 23, 13 ; 54, 15, 46 }
	  rnameset(A, "First Second")
	  string name = rnameget(A, 2)
	  print name
```


See also rnameset.

* * *

rnameset
--------

**Output:** integer


|Arguments:|M (matrix)                  |
|----------|----------------------------|
|          |S (array of strings or list)|


Attaches names to the rows of the _m_ x _n_ matrix _M_. If _S_ is a named list, the names are taken from the names of the listed series; the list must have _m_ members. If _S_ is an array of strings, it should contain _m_ elements. A single string is also acceptable as the second argument; in that case it should contain _m_ space-separated substrings.

The nominal return value is 0 on successful completion; in case of failure an error is flagged. See also cnameset.

Example:

```
	  matrix M = {1, 2; 2, 1; 4, 1}
	  strings S = array(3)
	  S[1] = "Row1"
	  S[2] = "Row2"
	  S[3] = "Row3"
	  rnameset(M, S)
	  print M
```


* * *

rows
----

**Output:** integer

Returns the number of rows of the matrix _X_. See also cols, mshape, unvech, vec, vech.

* * *

schur
-----

**Output:** complex matrix


|Arguments:|A (complex matrix)               |
|----------|---------------------------------|
|          |&Z (reference to matrix, or null)|
|          |&w (reference to matrix, or null)|


Performs the Schur decomposition of the complex matrix _A_, returning a complex upper triangular matrix _T_. If the second argument is given and is not null it retrieves a complex matrix _Z_ holding the Schur vectors associated with _A_ and _T_, such that _A_ = _ZTZ_H. If the third argument is given it retrieves the eigenvalues of _A_ in a complex column vector.

* * *

sd
--

**Output:** scalar or series


|Arguments:|x (series or list)         |
|----------|---------------------------|
|          |partial (boolean, optional)|


If _x_ is a series, returns the (scalar) sample standard deviation, skipping any missing observations.

If _x_ is a list, returns a series _y_ such that _y_t is the sample standard deviation of the values of the series in the list at observation _t_. By default the standard deviation is recorded as NA if there are any missing values at _t_, but if you pass a non-zero value for _partial_ any non-missing values will be used to form the statistic.

See also var.

* * *

sdc
---

**Output:** row vector


|Arguments:|X (matrix)                 |
|----------|---------------------------|
|          |df (scalar, optional)      |
|          |skip_na (boolean, optional)|


Returns the standard deviations of the columns of _X_. If _df_ is positive it is used as the divisor for the column variances, otherwise the divisor is the number of rows in _X_ (that is, no degrees of freedom correction is applied). If a non-zero value is given for the optional third argument missing values are ignored, otherwise the result is NA for any columns that contain missing values. See also meanc, sumc.

* * *

sdiff
-----

**Output:** same type as input



Computes seasonal differences: _y(t) - y(t-k)_, where _k_ is the periodicity of the current dataset (see $pd or $panelpd). Starting values are set to NA.

When a list is returned, the individual variables are automatically named according to the template sd\__varname_ where _varname_ is the name of the original series. The name is truncated if necessary, and may be adjusted in case of non-uniqueness in the set of names thus constructed.

See also diff, ldiff.

* * *

seasonals
---------

**Output:** list


|Arguments:|baseline (integer, optional)|
|----------|----------------------------|
|          |center (boolean, optional)  |


Applicable only if the dataset has a time-series structure with periodicity greater than 1. Returns a list of dummy variables coding for the period or season, named S1, S2 and so on.

The optional _baseline_ argument can be used to exclude one period from the set of dummies. For example, if you give a baseline value of 1 with quarterly data the returned list will hold dummies for quarters 2, 3 and 4 only. If this argument is omitted or set to zero a full set of dummies is generated; if non-zero, it must be an integer from 1 to the periodicity of the data.

The _center_ argument, if non-zero, calls for the dummies to be centered; that is, to have their population mean subtracted. For example, with quarterly data centered seasonals will have values –0.25 and 0.75 rather than 0 and 1.

With weekly data the precise effect depends on whether the data are dated or not. If they are dated, up to 53 seasonals are created, based on the ISO 8601 week number (see isoweek); if not, the maximum number of series is 52 (and over a long time span the "seasonals" will drift out of phase with the calendar year). In the dated weekly case, if you wish to create monthly seasonals this can be done as follows:

```
	  series month = $obsminor
	  list months = dummify(month)
```


See dummify for details.

* * *

selifc
------

**Output:** matrix


|Arguments:|A (matrix)    |
|----------|--------------|
|          |b (row vector)|


Selects from _A_ only the columns for which the corresponding element of _b_ is non-zero. _b_ must be a row vector with the same number of columns as _A_.

See also selifr.

* * *

selifr
------

**Output:** matrix


|Arguments:|A (matrix)       |
|----------|-----------------|
|          |b (column vector)|


Selects from _A_ only the rows for which the corresponding element of _b_ is non-zero. _b_ must be a column vector with the same number of rows as _A_.

See also selifc, trimr.

* * *

seq
---

**Output:** row vector


|Arguments:|a (scalar)          |
|----------|--------------------|
|          |b (scalar)          |
|          |k (scalar, optional)|


Given only two arguments, returns a row vector filled with values from _a_ to _b_ with an increment of 1, or a decrement of 1 if _a_ is greater than _b_.

If the third argument is given, returns a row vector containing a sequence of values starting with _a_ and incremented (or decremented, if _a_ is greater than _b_) by _k_ at each step. The final value is the largest member of the sequence that is less than or equal to _b_ (or mutatis mutandis for _a_ greater than _b_). The argument _k_ must be positive.

See also ones, zeros.

* * *

setnote
-------

**Output:** integer


|Arguments:|b (bundle)   |
|----------|-------------|
|          |key (string) |
|          |note (string)|


Sets a descriptive note for the object identified by _key_ in the bundle _b_. This note will be shown when the print command is used on the bundle. This function returns 0 on success or non-zero on failure (for example, if there is no object in _b_ under the given _key_).

* * *

sgn
---

**Output:** same type as input



Returns the sign function of _x_; that is, 0 if _x_ is zero, 1 if _x_ is positive, –1 if _x_ is negative, or NA if _x_ is Not a Number.

* * *

simann
------

**Output:** scalar


|Arguments:|&b (reference to matrix) |
|----------|-------------------------|
|          |f (function call)        |
|          |maxit (integer, optional)|


Implements simulated annealing, which may be helpful in improving the initialization for a numerical optimization problem.

On input the first argument holds the initial value of a parameter vector and the second argument specifies a function call which returns the (scalar) value of the maximand. The optional third argument specifies the maximum number of iterations (which defaults to 1024). On successful completion, simann returns the final value of the maximand and _b_ holds the associated parameter vector.

For more details and an example see chapter 37 of the Gretl User's Guide. See also BFGSmax, NRmax.

* * *

sin
---

**Output:** same type as input



Returns the sine of _x_. See also cos, tan, atan.

* * *

sinh
----

**Output:** same type as input



Returns the hyperbolic sine of _x_.

See also asinh, cosh, tanh.

* * *

skewness
--------

**Output:** scalar

Returns the skewness value for the series _x_, skipping any missing observations.

* * *

sleep
-----

**Output:** scalar

Not of any direct use for econometrics, but can be useful for testing parallelization methods. This function simply causes the current thread to "sleep"—that is, do nothing—for _ns_ seconds. The argument must be non-negative. On wake-up, the function returns 0.

* * *

smplspan
--------

**Output:** scalar


|Arguments:|startobs (string)|
|----------|-----------------|
|          |endobs (string)  |
|          |pd (integer)     |


Returns the number of observations from _startobs_ to _endobs_ (inclusive) for time-series data with frequency _pd_.

The first two arguments should be given in the form preferred by gretl for annual, quarterly or monthly data—for example, 1970, 1970:1 or 1970:01 for each of these frequencies, respectively—or as ISO 8601 dates, YYYY-MM-DD.

The _pd_ argument must be 1, 4 or 12 (annual, quarterly, monthly); one of the daily frequencies (5, 6, 7); or 52 (weekly). If _pd_ equals 1, 4 or 12, then ISO 8601 dates are acceptable for the first two arguments if they indicate the start of the period in question. For example, 2015-04-01 is acceptable in place of 2015:2 to represent the second quarter of 2015.

If you already have a dataset of frequency _pd_ in place, with a sufficient range of observations, then the result of this function could easily be emulated using obsnum. The advantange of smplspan is that you can calculate the number of observations without having a suitable dataset (or any dataset) in place. An example follows:

```
	  scalar T = smplspan("2010-01-01", "2015-12-31", 5)
	  nulldata T
	  setobs 5 2010-01-01
```


This produces:

```
	  ? scalar T = smplspan("2010-01-01", "2015-12-31", 5)
	  Generated scalar T = 1565
	  ? nulldata T
	  periodicity: 1, maxobs: 1565
	  observations range: 1 to 1565
	  ? setobs 5 2010-01-01
	  Full data range: 2010-01-01 - 2015-12-31 (n = 1565)
```


After the above, you can be confident that the last observation in the dataset created via nulldata will be 2015-12-31. Note that the number 1565 would have been rather tricky to compute otherwise.

* * *

sort
----

**Output:** same type as input



Sorts _x_ in ascending order. Observations with missing values are skipped if _x_ is a series, but sorted to the end if _x_ is a vector. See also dsort, values. For matrices specifically, see msortby.

* * *

sortby
------

**Output:** series


|Arguments:|y1 (series)|
|----------|-----------|
|          |y2 (series)|


Returns a series containing the elements of _y2_ sorted by increasing value of the first argument, _y1_. See also sort, ranking.

* * *

sphericorr
----------

**Output:** matrix


|Arguments:|X (matrix)                       |
|----------|---------------------------------|
|          |mode (integer)                   |
|          |&J (reference to matrix, or null)|


Calculates the spherical coordinates representation of a correlation matrix, or its inverse, depending on the value of the _mode_ parameter.

When _mode_ is 0 or omitted, _X_ is assumed to be an _n_ x _n_ correlation matrix. The returned value will be a vector with _n(n-1)/2_ elements between 0 and π. In this mode the reference to _J_ is ignored.

When _mode_ is 1 or 2 the inverse transformation is performed, so _X_ must be a vector with _n(n-1)/2_ elements between 0 and π. The return value is the correlation matrix _R_ if _mode_ equals 1, or its Cholesky factor _K_ if _mode_ equals 2. The optional pointer to matrix _J_, if present, retrieves the Jacobian of vech(_R_) or vech(_K_) with respect to _X_.

Note that the spherical coordinates representation makes it very easy to compute the log-determinant of the correlation matrix _R_:

```
	 omega = sphericorr(X)
	 log_det = 2 * sum(log(sin(omega)))
```


* * *

sprintf
-------

**Output:** string


|Arguments:|format (string)|
|----------|---------------|
|          |... (see below)|


The returned string is constructed by printing the values of the trailing arguments, indicated by the dots above, under the control of _format_. It is meant to give you great flexibility in creating strings. The _format_ is used to specify the precise way in which you want the arguments to be printed.

In general, _format_ must be an expression that evaluates to a string, but in most cases will just be a string literal (an alphanumeric sequence surrounded by double quotes). Some character sequences in the format have a special meaning: those beginning with the percent character (%) are interpreted as "placeholders" for the items contained in the argument list; moreover, special characters such as the newline character are represented via a combination beginning with a backslash.

For example, the code below

```
	  scalar x = sqrt(5)
	  string claim = sprintf("sqrt(%d) is (roughly) %6.4f.\n", 5, x)
	  print claim
```


will output

```
	  sqrt(5) is (roughly) 2.2361.
```


The expression %d in the format string indicates that we want an integer at that place in the output; since it is the leftmost "percent" expression, it is matched to the first argument, that is 5. The second special sequence is %6.4f, which stands for a decimal value at least 6 digits wide with 4 digits after the decimal separator. The number of such sequences must match the number of arguments following the format string.

See the help page for the printf command for more details about the syntax you can use in format strings.

* * *

sqrt
----

**Output:** same type as input



Returns the positive square root of _x_; produces NA for negative values.

Note that if the argument is a matrix the operation is performed element by element. For the "matrix square root" see cholesky.

* * *

square
------

**Output:** list


|Arguments:|L (list)                          |
|----------|----------------------------------|
|          |cross-products (boolean, optional)|


Returns a list that references the squares of the variables in the list _L_, named on the pattern sq\__varname_. If the optional second argument is present and has a non-zero value, the returned list also includes the cross-products of the elements of _L_; these are named on the pattern _var1_\__var2_. In these patterns the input variable names are truncated if need be, and the output names may be adjusted in case of duplication of names in the returned list.

Note that dummy variables will be skipped when computing squares to avoid producing an identical series, but their product (aka "interaction") with other series in the input list _L_ will be computed.

* * *

sscanf
------

**Output:** integer


|Arguments:|src (string or array of strings)|
|----------|--------------------------------|
|          |format (string)                 |
|          |... (see below)                 |


Reads values from _src_ under the control of _format_ and assigns these values to one or more trailing arguments, indicated by the dots above. Returns the number of values assigned. This is a simplified version of the sscanf function in the C programming language, with an extension to the scanning of an entire matrix; this extension is described under the leading "Scanning a matrix" below. Note that giving an array of strings as _src_ is acceptable only in the case of matrix scanning.

_src_ may be either a literal string, enclosed in double quotes, or the name of a predefined string variable. _format_ is defined similarly to the format string in printf (more on this below). _args_ should be a comma-separated list containing the names of predefined variables: these are the targets of conversion from _src_. (For those used to C: one can prefix the names of numerical variables with & but this is not required.)

Literal text in _format_ is matched against _src_. Conversion specifiers start with %, and recognized conversions include %f, %g or %lf for floating-point numbers; %d for integers; %s for strings. You may insert a positive integer after the percent sign: this sets the maximum number of characters to read for the given conversion. Alternatively, you can insert a literal \* after the percent to suppress the conversion (thereby skipping any characters that would otherwise have been converted for the given type). For example, %3d converts the next 3 characters in _src_ to an integer, if possible; %\*g skips as many characters in _src_ as could be converted to a single floating-point number.

In addition to %s conversion for strings, a simplified version of the C format %_N_\[_chars_\] is available. In this format _N_ is the maximum number of characters to read and _chars_ is a set of acceptable characters, enclosed in square brackets: reading stops if _N_ is reached or if a character not in _chars_ is encountered. The function of _chars_ can be reversed by giving a circumflex, ^, as the first character; in that case reading stops if a character in the given set is found. (Unlike C, the hyphen does not play a special role in the _chars_ set.)

If the source string does not (fully) match the format, the number of conversions may fall short of the number of arguments given. This is not in itself an error so far as gretl is concerned. However, you may wish to check the number of conversions performed; this is given by the return value. Some simple examples follow:

```
	  # scanning scalar values
	  scalar x
	  scalar y
	  sscanf("123456", "%3d%3d", x, y)
	  # scanning string values
	  string s = "one two"
	  string s1
	  string s2
	  sscanf(s, "%s %s", s1, s2)
	  print s1 s2
```


### Scanning a matrix

Matrix scanning must be signaled by the special conversion specification "%m". The maximum number of rows to be read can be specified by inserting an integer between the "%" sign and the "m" for matrix. Two variants are supported: _src_ a single string representing a matrix, and _src_ an array of strings. We describe these options in turn.

If _src_ is a single string argument the scanner reads a line of input and counts the (space- or tab-separated) number of numeric fields. This defines the number of columns in the matrix. By default, reading then proceeds for as many lines (rows) as contain the same number of numeric columns, but the maximum number of rows can be limited via the optional integer value mentioned above.

If _src_ is an array of strings the output is necessarily a column vector, each element of which is the numerical conversion of the corresponding string, or NA if the string is not numeric. Here are some simple examples.

```
	  # scanning a single string
	  string s = sprintf("1 2 3 4\n5 6 7 8")
	  print s
	  matrix m
	  sscanf(s, "%m", m)
	  print m
	  # scanning an array of strings
	  strings S = defarray("1.1", "2.2", "3.3", "4.4", "5.5")
	  sscanf(S, "%4m", m)
	  print m
```


* * *

sst
---

**Output:** scalar



Returns the sum of squared deviations from the mean for the non-missing observations in the series or vector _y_. See also var.

* * *

stack
-----

**Output:** series


|Arguments:|L (list)                  |
|----------|--------------------------|
|          |n (integer)               |
|          |offset (integer, optional)|


Designed for manipulation of data into the stacked time series format required by gretl for panel data. The return value is a series obtained by stacking "vertically" _n_ observations from each series in the list _L_. By default the first _n_ observations are used (corresponding to _offset_ = 0) but the starting point can be shifted by supplying a positive value for _offset_. If the resulting series is longer than the existing dataset, observations are added as needed.

This function can handle the case where a data file holds side-by-side time series for a number of cross-sectional units, as well as the case where time runs horizontally and each row represents a cross-sectional unit.

See the section titled "Panel data specifics" in chapter 4 of the Gretl User's Guide for details and examples of usage.

* * *

stdize
------

**Output:** same type as input


|Arguments:|X (series, list or matrix) |
|----------|---------------------------|
|          |v (integer, optional)      |
|          |skip_na (boolean, optional)|


By default, returns a standardized version of the series, list or matrix: the input is centered and divided by its sample standard deviation (with a degrees of freedom correction of 1). Results are computed by column in the case of matrix input.

The optional second argument can be used to inflect the result. A non-negative value of _v_ sets the degrees of freedom correction used in the standard deviation, so _v_ = 0 gives the maximum likelihood estimator. As a special case, if _v_ equals –1 only centering is performed.

By default missing values are automatically skipped in the case of series or list input but not for matrix input. To have missing values ignored in the matrix case, supply a non-zero value for _skip\_na_.

* * *

strfday
-------

**Output:** depends on input


|Arguments:|epoch_day (scalar, series or matrix)|
|----------|------------------------------------|
|          |format (string, optional)           |


This function works like strftime, converting from a numeric value to a string governed by _format_, except that the input is an "epoch day", for the definition of which see epochday. Since the resolution is daily, only date-related formats are handled; time-related formats give undefined results.

If the second argument is omitted the format defaults to ISO 8601 extended, YYYY-MM-DD.

* * *

strftime
--------

**Output:** depends on input


|Arguments:|tm (scalar, series or matrix)|
|----------|-----------------------------|
|          |format (string, optional)    |
|          |offset (scalar, optional)    |


The argument _tm_ is taken to give "Unix time", the number of seconds since the start of the year 1970 according to UTC, and the return value is a string giving the corresponding date and/or time—either in a format specified via the optional second argument or, by default, the "preferred date and time representation for the current locale" as determined by the system C library. See below for more on the format specification.

The optional _offset_ argument can be used to specify an offset in seconds relative to UTC, thus selecting a time zone other than the default, which is always local time. For example an offset of 3600 selects Central European Time, while 0 selects GMT. The absolute value of _offset_ should not exceed 86400 (24 hours).

The specific type returned depends on that of _tm_: if _tm_ is a scalar, vector, or series the output is, respectively, a single string, an array of strings, or a string-valued series.

Values of _tm_ suitable for use with this function may be obtained via the $now accessor or the strptime function.

Note that while _tm_ is taken as relative to UTC the output of this function is by default "local", relative to the time-zone setting on the host computer. A given _tm_ will therefore show a different time, and perhaps a different date, in different time zones. But if you want a string representing UTC rather than local time, gretl can do that; see below.

### Format options

The standard formatting options may be found by consulting the strftime manual page, on systems which have such pages, or via one of the many websites which present relevant information, such as https://devhints.io/strftime. In addition to the standard formats gretl recognizes a special option: if _format_ is just "8601", date and time are shown in ISO 8601 format.

* * *

stringify
---------

**Output:** integer


|Arguments:|y (series)          |
|----------|--------------------|
|          |S (array of strings)|


Provides a means of defining string values for the series _y_. Two conditions must be satisfied for this to work: the target series must have nothing but integer values, none of them less than 1, and the array _S_ must have at least _n_ elements where _n_ is the largest value in _y_. In addition each element of _S_ must be valid UTF-8. If any of these conditions is not met, an error is flagged. The nominal return value is 0 on successful completion.

An alternative to stringify that may be useful in some contexts is direct assignment from an array of strings to a series: this creates a series whose values are taken from the array in sequence; the number of elements in the array must equal either the full length of the dataset or the length of the current sample range, and values may be repeated as required.

See also strvals, strvsort.

* * *

strlen
------

**Output:** integer



If _s_ is a single string, returns the number of UTF-8 characters it contains. Note that this will be less than the number of bytes if the string contains any multi-byte (non-ASCII) characters. If you want the number of bytes you can use the nelem function. For example:

```
	  string s = "¡Olé!"
	  printf "strlen(s) = %d, nelem(s) = %d\n", strlen(s), nelem(s)
```


should return

```
	  strlen(s) = 5, nelem(s) = 7
```


If the argument is an array of strings the return value is a column vector holding the number of characters in each string. A string-valued series is also an acceptable argument: in this case the return value is a series holding the length of the string values over the current sample range.

* * *

strncmp
-------

**Output:** integer


|Arguments:|s1 (string)          |
|----------|---------------------|
|          |s2 (string)          |
|          |n (integer, optional)|


Compares the two string arguments and returns an integer less than, equal to, or greater than zero if _s1_ is found, respectively, to be less than, to match, or be greater than _s2_, up to the first _n_ characters. If _n_ is omitted the comparison proceeds as far as possible.

Note that if you just want to compare two strings for equality, that can be done without using a function, as in if (s1 == s2) ...

* * *

strpday
-------

**Output:** depends on input


|Arguments:|s (string, strings array or string-valued series)|
|----------|-------------------------------------------------|
|          |format (string, optional)                        |


This function works just like strptime, except that the return value is an "epoch day" value, for the definition of which see epochday. Since the resolution is daily, any time-of-day information in _s_ is ignored.

* * *

strptime
--------

**Output:** depends on input


|Arguments:|s (string, strings array or string-valued series)|
|----------|-------------------------------------------------|
|          |format (string, optional)                        |


This function is the converse of strftime; it parses one or more date/time strings using the specified _format_ and returns the number of seconds since the start of 1970 according to Coordinated Universal Time (UTC). The specific type of the return value depends on that of _s_: if _s_ is a string, strings array, or string-valued series the output is, respectively, a scalar, a column vector, or a numeric series.

If _format_ is omitted, it defaults to ISO 8601 "extended", YYYY-MM-DD (which translates to "%Y-%m-%d" as a strptime format).

As a special case, the first argument may be given as an 8-digit integer conforming to the ISO 8601 "basic" date format, YYYYMMDD (or a vector or series containing such values). In that case _format_ should be omitted.

Note that the first argument to this function is taken as relative to the time-zone setting on the host computer. So for example, the call

```
	  strptime("13/02/2009 23:31.30", "%d/%m/%Y %H:%M.%S")
```


will produce 1234567890 on output if your system time is set to UTC but if you're in the Central European time zone (UTC+01:00) the output will be 1234564290.

The _format_ options may be found by consulting the strptime manual page, on systems which have such pages, or via one of the many websites which present relevant information, such as http://man7.org/linux/man-pages/man3/strptime.3.html.

The example below shows how one can convert date information from one format to another.

```
	  scalar tm = strptime("Thursday 02/07/19", "%A %m/%d/%y")
	  eval strftime(tm) # default output
	  eval strftime(tm, "%B %d, %Y")
```


On the East Coast of the USA the result is

```
	  Thu 07 Feb 2019 12:00:00 AM EST
	  February 07, 2019
```


* * *

strsplit
--------

**Output:** string or array of strings


|Arguments:|s (string)            |
|----------|----------------------|
|          |sep (string, optional)|
|          |i (integer, optional) |


In basic usage, with a single argument, returns the array of strings that results from the splitting of _s_ on white space (that is on any combination of the space, tab and/or newline characters).

The optional second argument can be used to specify the separator used for splitting _s_. For example

```
	  string basket = "banana,apple,jackfruit,orange"
	  strings S = strsplit(basket, ",")
```


will split the input into an array of four strings using comma as separator.

The backslash-escape sequences "\\n", "\\r" and "\\t" are taken to represent newline, carriage return and tab, respectively, in the optional _sep_ argument. If you wish to include a literal backslash as a separator character you should double it, as in "\\\\". Example:

```
	  string s = "c:\fiddle\sticks"
	  strings S = strsplit(s, "\\")
```


Regardless of the separator, the members of the returned array are trimmed of any leading or trailing white space. Correspondingly, if _sep_ contains non-whitespace characters then it is stripped of any leading or trailing space.

If an integer value greater than zero is given as the third argument the return value is a single string, namely the (1-based) element _i_ of the array that would otherwise be produced. If _i_ is less than 1 that provokes an error, but if _i_ is greater than the implied number of elements an empty string is returned.

* * *

strstr
------

**Output:** string


|Arguments:|s1 (string)                 |
|----------|----------------------------|
|          |s2 (string)                 |
|          |ign_case (boolean, optional)|


Searches _s1_ for an occurrence of the string _s2_. If a match is found, returns a copy of the portion of _s1_ that starts with _s2_, otherwise returns an empty string.

Example:

```
          string s1 = "Gretl is an econometrics package"
          string s2 = strstr(s1, "an")
          print s2
```


If the optional argument _ign\_case_ is nonzero, the search is case-insensitive. For example,

```
	  strstr("Chicago", "c")
```


returns "cago", but

```
	  strstr("Chicago", "c", 1)
```


returns "Chicago".

If you just wish to find out if _s1_ contains _s2_ (boolean test), see instring.

* * *

strstrip
--------

**Output:** string

Returns a copy of the argument _s_ from which leading and trailing white space have been removed.

Example:

```
          string s1 = "    A lot of white space.  "
          string s2 = strstrip(s1)
          print s1 s2
```


* * *

strsub
------

**Output:** same type as input


|Arguments:|s (string, strings array or string-valued series)|
|----------|-------------------------------------------------|
|          |find (string)                                    |
|          |subst (string)                                   |


If _s_ is a single string, returns a copy of _s_ in which all occurrences of _find_ are replaced by _subst_. If _s_ is an array of strings or string-valued series this operation is performed on each string in the array or series. See also regsub for more complex string replacement via regular expressions.

Example:

```
          string s1 = "Hello, Gretl!"
          string s2 = strsub(s1, "Gretl", "Hansl")
          print s2
```


* * *

strvals
-------

**Output:** array of strings


|Arguments:|y (series)                   |
|----------|-----------------------------|
|          |subsample (boolean, optional)|


If the series _y_ is string-valued, returns by default an array containing all its distinct values (irrespective of the current setting of the sample range), ordered by the associated numerical values starting at 1. If the dataset is currently subsampled you can give a non-zero value for the optional second argument to obtain an array holding just the string values present in the subsample.

If _y_ is not string-valued an empty strings array is returned. See also stringify.

An alternative to strvals that may be useful in some contexts is direct assignment of a string-valued series to an array of strings: this provides not just the distinct values, but all values of the series in the current sample range.

* * *

strvsort
--------

**Output:** integer


|Arguments:|y (series)                    |
|----------|------------------------------|
|          |S (array of strings, optional)|


Carries out one or other of two sorts of rearrangment of the series _y_, which must be string-valued. The nominal return value is 0 on successful completion.

Method 1: If the second argument is not given, the effect is to sort _y_ in this sense: the distinct string values are alphabetized and then the series is recoded such that 1 is assigned for the first of the ordered strings, 2 for the second, and so on. This can be useful, among other reasons, for ensuring a uniform encoding for multiple series that share the same set of string values.

Method 2: If the second argument is given, it must be an array which contains exactly the distinct string values of _y_ (which can be found via strvals), but put into a preferred order. Then the effect is to recode the series such that value 1 is assigned for the first string in _S_, value 2 for the second, and so on. This can be useful for ensuring that the numeric codes "make sense" when string values can be thought of as naturally ordered.

The primary use case for these methods is the handling of string-valued series imported from third-party sources such as comma-separated files. For such data, gretl assigns numeric codes based simply on the order of occurrence of the strings across the rows of the file. So in a series with values low, middle and high, high will be assigned code 1 if it happens to occur first, rather than 3, which would clearly be more "natural". This can be fixed using Method 2. Moreover, if two or more series share the same string values, they will be encoded differently unless their distinct values happen to appear in the same order in the data file. This could be fixed by either method.

See also stringify, strvals.

* * *

substr
------

**Output:** same type as input


|Arguments:|s (string, strings array or string-valued series)|
|----------|-------------------------------------------------|
|          |start (integer)                                  |
|          |end (integer)                                    |


If _s_ is a single string, returns the substring of _s_ from the character with (1-based) index _start_ to that with index _end_, inclusive, or from _start_ to the end of _s_ if _end_ is –1. If the argument is an array of strings or string-valued series, this operation is performed on each string in the array or series.

For example, the code below

```
          string s1 = "Hello, Gretl!"
          string s2 = substr(s1, 8, 12)
          print s2
```


gives:

```
	  ? print s2
	  Gretl
```


It should be noted that in some cases you may be willing to trade clarity for conciseness, and use slicing and increment operators, as in

```
          string s1 = "Hello, Gretl!"
          string s2 = s1[8:12]
          string s3 = s1 + 7
          print s2
          print s3
```


which would give you

```
	  ? print s2
	  Gretl
	  ? print s3
	  Gretl!
```


* * *

sum
---

**Output:** scalar or series


|Arguments:|x (series, matrix or list) |
|----------|---------------------------|
|          |partial (boolean, optional)|


If _x_ is a series, returns the (scalar) sum of the non-missing observations in _x_. See also sumall.

If _x_ is a matrix, returns the sum of the elements of the matrix.

If _x_ is a list, returns a series _y_ such that _y_t is the sum of the values of the variables in the list at observation _t_. By default the sum is recorded as NA if there are any missing values at _t_, but if you pass a non-zero value for _partial_ any non-missing values will be used to form the sum.

* * *

sumall
------

**Output:** scalar

Returns the sum of the observations of _x_ over the current sample range, or NA if there are any missing values. Use sum if you want missing values to be skipped.

* * *

sumc
----

**Output:** row vector


|Arguments:|X (matrix)                 |
|----------|---------------------------|
|          |skip_na (boolean, optional)|


Returns the sums of the columns of _X_. If a non-zero value is given for the optional second argument missing values are ignored, otherwise the result is NA for any columns that contain missing values. See also meanc, sumr.

* * *

sumr
----

**Output:** column vector


|Arguments:|X (matrix)                 |
|----------|---------------------------|
|          |skip_na (boolean, optional)|


Returns the sums of the rows of _X_. If a non-zero value is given for the optional second argument missing values are ignored, otherwise the result is NA for any rows that contain missing values. See also meanr, sumc.

* * *

svd
---

**Output:** row vector


|Arguments:|X (matrix)                       |
|----------|---------------------------------|
|          |&U (reference to matrix, or null)|
|          |&V (reference to matrix, or null)|


Performs the singular values decomposition of the matrix _X_.

The singular values are returned in a row vector. The left and/or right singular vectors _U_ and _V_ may be obtained by supplying non-null values for arguments 2 and 3, respectively. For any matrix A, the code

```
	  s = svd(A, &U, &V)
	  B = (U .* s) * V
```


should yield B identical to A (apart from machine precision).

See also eigengen, eigensym, qrdecomp.

* * *

svm
---

**Output:** series


|Arguments:|L (list)                             |
|----------|-------------------------------------|
|          |bparms (bundle)                      |
|          |bmod (reference to bundle, optional) |
|          |bprob (reference to bundle, optional)|


This function enables the training of, and prediction based on, an SVM (a Support Vector Machine), using LIBSVM as back-end. The list argument _L_ should include the dependent variable followed by the independent variables and the _bparms_ bundle is used to pass options to the SVM mechanism. The return value is a series holding the SVM's predictions. The two optional bundle-pointer argument can be used to retrieve additional information after training and/or prediction.

For details, please see the PDF documentation for gretl + SVM.

* * *

tan
---

**Output:** same type as input



Returns the tangent of _x_. See also atan, cos, sin.

* * *

tanh
----

**Output:** same type as input



Returns the hyperbolic tangent of _x_.

See also atanh, cosh, sinh.

* * *

tdisagg
-------

**Output:** matrix


|Arguments:|Y (series or matrix)                |
|----------|------------------------------------|
|          |X (series, list or matrix, optional)|
|          |s (scalar)                          |
|          |opts (bundle, optional)             |
|          |results (bundle, optional)          |


Performs temporal disaggregation (conversion to higher frequency) of the time-series data in _Y_. The argument _s_ gives the expansion factor (for example, 3 for quarterly to monthly). The argument _X_ may contain one or more covariates at the higher frequency to aid in the disaggregation. Several options may be passed in _opts_, and details of the disaggregation may be retrieved via _results_.

See chapter 9 of the Gretl User's Guide for details.

* * *

toepsolv
--------

**Output:** column vector


|Arguments:|c (vector)                          |
|----------|------------------------------------|
|          |r (vector)                          |
|          |b (vector)                          |
|          |&det (reference to scalar, optional)|


Solves a Toeplitz system of linear equations, that is _Tx = b_ where _T_ is a square matrix whose element _T_i,j equals _c_i-j for _i>=j_ and _r_j-i for _i<=j_. Note that the first elements of _c_ and _r_ must be equal, otherwise an error is returned. Upon successful completion, the function returns the vector _x_.

The algorithm used here takes advantage of the special structure of the matrix _T_, which makes it much more efficient than other unspecialized algorithms, especially for large problems. Warning: in certain cases, the function may spuriously issue a singularity error when in fact the matrix _T_ is nonsingular; this problem, however, cannot arise when _T_ is positive definite.

If the optional argument _det_ is supplied (in pointer form), it will contain on exit the determinant of _T_. For example, the code:

```
	  A = unvech({3;2;1;3;2;3})    # Build a 3x3 Toeplitz matrix
	  x = ones(3,1)                # and a 3x1 vector
	  print A x
	  eval A\x                     # solution via generic inversion
	  eval det(A)                  # print the determinant
	  a = A[1,]
	  d = 0
	  eval toepsolv(a, a, x, &d)   # use the dedicated function
	  print d
```


produces

```
A (3 x 3)

  3   2   1
  2   3   2
  1   2   3

x (3 x 1)

  1
  1
  1

     0.25000
 -3.3307e-17
     0.25000

8
     0.25000
  2.7756e-17
     0.25000


d =  8.0000000
```


* * *

tolower
-------

**Output:** same type as input



If _s_ is a single string, returns a copy of _s_ in which any upper-case characters are converted to lower case. If _s_ is an array of strings or string-valued series this operation is performed on each string in the array or series.

Example:

```
          string s1 = "Hello, Gretl!"
          string s2 = tolower(s1)
          print s2
```


* * *

toupper
-------

**Output:** same type as input



If _s_ is a single string, returns a copy of _s_ in which any lower-case characters are converted to upper case. If _s_ is an array of strings or string-valued series this operation is performed on each string in the array or series.

Examples:

```
          string s1 = "Hello, Gretl!"
          string s2 = toupper(s1)
          print s2
```


* * *

tr
--

**Output:** scalar



Returns the trace of the square matrix _A_, that is, the sum of its diagonal elements. See also diag.

* * *

transp
------

**Output:** matrix

Returns the transpose of _X_. Note: this is rarely used; in order to get the transpose of a matrix, in most cases you can just use the prime operator: X'.

* * *

trigamma
--------

**Output:** same type as input



Returns the trigamma function of _x_, that is the second derivative of the log of the Gamma function.

See also lngamma, digamma.

* * *

trimr
-----

**Output:** matrix


|Arguments:|X (matrix)    |
|----------|--------------|
|          |ttop (integer)|
|          |tbot (integer)|


Returns a matrix that is a copy of _X_ with _ttop_ rows trimmed at the top and _tbot_ rows trimmed at the bottom. The latter two arguments must be non-negative, and must sum to less than the total rows of _X_.

See also selifr.

* * *

typename
--------

**Output:** string

A convenience function which combines typeof and typestr, with a little value added. Basically, the following two statements are equivalent

```
	  eval typestr(typeof(x))
	  eval typename(x)
```


except that if _expr_ names an array, typename returns the specific type of the array, as in

```
	  strings S = defarray("foo", "bar", "baz")
	  eval typestr(typeof(S))  # gives "array"
	  eval typename(S)         # gives "strings"
```


* * *

typeof
------

**Output:** integer

Returns a numeric code indicating the type of _expr_, if it names a currently defined variable, specifies a sub-object such as a bundle member or array element, or is a valid expression that could stand as the right-hand side of an assignment statement. The codes are 1 for scalar, 2 for series, 3 for matrix, 4 for string, 5 for bundle, 6 for array and 7 for list. A return value of 0 indicates that _expr_ names no existing object, or more generally that an assignment with _expr_ on the right-hand side would fail.

A few examples follow:

```
	  strings S = defarray("foo", "bar")
	  eval typeof(S)            # gives 6 (array)
	  eval typeof(S[1])         # gives 4 (string)
	  eval typeof(S[7])         # gives 0 (out of bounds)
	  eval typeof(S[x])         # gives 0 (invalid index)
	  eval typeof(1+1)          # gives 1 (scalar)
	  eval typeof(sqrt("foo"))  # gives 0 (invalid)
```


The function typestr may be used to get the string corresponding to the return value from typeof, though if you just want the string result typename may be a more convenient alternative.

* * *

typestr
-------

**Output:** string



Given a gretl type code (for example, obtained via typeof or inbundle), returns a string giving the name of the type. The mapping from codes to strings is: 1 = "scalar", 2 = "series", 3 = "matrix", 4 = "string", 5 = "bundle", 6 = "array", 7 = "list", and 0 = "null".

See also typename for an alternative.

* * *

uniform
-------

**Output:** series


|Arguments:|a (scalar)|
|----------|----------|
|          |b (scalar)|


Generates a series of uniform pseudo-random variates in the interval (_a_, _b_), or, if no arguments are supplied, in the interval (0,1). The algorithm used by default is the SIMD-oriented Fast Mersenne Twister developed by Saito and Matsumoto (2008).

See also randgen, normal, mnormal, muniform.

* * *

uniq
----

**Output:** column vector



Returns a vector containing the distinct non-missing elements of _x_, not sorted but in their order of appearance. See values for a variant that sorts the elements.

* * *

unvech
------

**Output:** square matrix


|Arguments:|v (vector)          |
|----------|--------------------|
|          |d (scalar, optional)|


If the second argument is omitted, returns an _n_ x _n_ symmetric matrix obtained by rearranging the elements of _v_. The number of elements in _v_ must be a triangular integer—i.e., a number _k_ such that an integer _n_ exists with the property _k = n(n+1)/2_. This is the inverse of the function vech.

If the argument _d_ is given, the function returns an _(n+1)_ x _(n+1)_ matrix with the extra-diagonal entries filled with the elements of _v_ as above. All the elements of the diagonal are set to _d_ instead.

Example:

```
        v = {1;2;3}
        matrix one = unvech(v)
        matrix two = unvech(v, 99)
        print one two
```


returns

```
      one (2 x 2)

      1   2
      2   3

      two (3 x 3)

      99     1     2
       1    99     3
       2     3    99
```


See also mshape, vech.

* * *

upper
-----

**Output:** square matrix



Returns an _n_ x _n_ upper triangular matrix: the elements on and above the diagonal are equal to the corresponding elements of _A_; the remaining elements are zero.

See also lower.

* * *

urcpval
-------

**Output:** scalar


|Arguments:|tau (scalar) |
|----------|-------------|
|          |n (integer)  |
|          |niv (integer)|
|          |itv (integer)|


_P_\-values for the test statistic from the Dickey–Fuller unit-root test and the Engle–Granger cointegration test, as per James MacKinnon (1996).

The arguments are as follows: _tau_ denotes the test statistic; _n_ is the number of observations (or 0 for an asymptotic result); _niv_ is the number of potentially cointegrated variables when testing for cointegration (or 1 for a univariate unit-root test); and _itv_ is a code for the model specification: 1 for no constant, 2 for constant included, 3 for constant and linear trend, 4 for constant and quadratic trend.

Note that if the test regression is "augmented" with lags of the dependent variable, then you should give an _n_ value of 0 to get an asymptotic result.

See also pvalue, qlrpval.

* * *

values
------

**Output:** column vector



Returns a vector containing the distinct elements of _x_ sorted in ascending order, ignoring any missing values. If you wish to truncate the values to integers before applying this function, use the expression values(int(x)).

See also uniq, dsort, sort.

* * *

var
---

**Output:** scalar or series


|Arguments:|x (series or list)         |
|----------|---------------------------|
|          |partial (boolean, optional)|


If _x_ is a series, returns the (scalar) sample variance, skipping any missing observations.

If _x_ is a list, returns a series _y_ such that _y_t is the sample variance of the values of the variables in the list at observation _t_. By default the variance is recorded as NA if there are any missing values at _t_, but if you pass a non-zero value for _partial_ any non-missing values will be used to form the statistic.

In each case the sum of squared deviations from the mean is divided by (_n_ – 1) for _n_ > 1. Otherwise the variance is given as zero if _n_ = 1, or as NA if _n_ = 0.

See also sd.

* * *

varname
-------

**Output:** string



If given an integer argument, returns the name of the variable with ID number _v_, or generates an error if there is no such variable.

If given a list argument, returns a string containing the names of the variables in the list, separated by commas. If the supplied list is empty, so is the returned string. To get an array of strings as return value, use varnames instead.

Example:

```
        open broiler.gdt
        string s = varname(7)
        print s
```


* * *

varnames
--------

**Output:** array of strings

Returns an array of strings containing the names of the variables in the list _L_. If the supplied list is empty, so is the returned array.

Example:

```
        open keane.gdt
        list L = year wage status
        strings S = varnames(L)
        eval S[1]
        eval S[2]
        eval S[3]
```


* * *

varnum
------

**Output:** integer



Returns the ID number of the variable called _varname_, or NA is there is no such variable.

* * *

varsimul
--------

**Output:** matrix


|Arguments:|A (matrix) |
|----------|-----------|
|          |U (matrix) |
|          |y0 (matrix)|


Simulates a _p_\-order _n_\-variable VAR, that is _y(t) = A1 y(t-1) + ... + Ap y(t-p) + u(t)._ The coefficient matrix _A_ is composed by stacking the _A_i matrices horizontally; it is _n_ x _np_, with one row per equation. This corresponds to the first _n_ rows of the matrix $compan provided by the var and vecm commands.

The _u\_t_ vectors are contained (as rows) in _U_ (_T_ x _n_). Initial values are in _y0_ (_p_ x _n_).

If the VAR contains deterministic terms and/or exogenous regressors, these can be handled by folding them into the _U_ matrix: each row of _U_ then becomes _u(t) = B'x(t) + e(t)._

The output matrix has _T_ + _p_ rows and _n_ columns; it holds the initial _p_ values of the endogenous variables plus _T_ simulated values.

See also $compan, var, vecm.

* * *

vec
---

**Output:** column vector

Stacks the columns of _X_ as a column vector. See also mshape, unvech, vech.

* * *

vech
----

**Output:** column vector


|Arguments:|A (square matrix)            |
|----------|-----------------------------|
|          |omit-diag (boolean, optional)|


This function rearranges the the elements of _A_ on and above the diagonal into a column vector, unless the _omit-diag_ is given a non-zero value, in which case only the entries above the diagonal are considered.

Typically, this function is used on symmetric matrices, in which case it can be undone by the function unvech. If the input matrix is not symmetric and it's the lower triangle that contains the "right" values, vech(A') will give the desired answer (its elements may have to be re-ordered, however). See also vec.

* * *

vma
---

**Output:** matrix


|Arguments:|A (matrix)                 |
|----------|---------------------------|
|          |K (matrix, optional)       |
|          |horizon (integer, optional)|


This function yields the VMA representation for a VAR system. If _y(t) = A1 y(t-1) + ... + Ap y(t-p) + u(t)_, where _u_t are the one-step-ahead prediction errors, the corresponding VMA representation is _y(t) = C0 e(t) + C1 e(t-1) + ..._. The relationship between the forecast errors _u_t and the structural shocks _e_t is given by _u(t) = K e(t)_. (Note that _C_0 = _K_.)

The coefficient matrix _A_ is composed by stacking the _A_i matrices horizontally; it is _n_ x _np_, with one row per equation. This corresponds to the first _n_ rows of the matrix $compan provided by gretl's var and vecm commands. The _K_ matrix is optional, and defaults to the identity matrix if omitted.

The returned matrix will have _horizon_ rows and _n_2 columns: its _i_\-th row contains _C_i-1 in vectorized form. The _horizon_ value defaults to 24 if omitted.

See also irf.

* * *

weekday
-------

**Output:** same type as input


|Arguments:|year (scalar or series) |
|----------|------------------------|
|          |month (scalar or series)|
|          |day (scalar or series)  |


Returns the day of the week (from Sunday = 0 to Saturday = 6) for the date(s) specified by the three arguments, or NA if the date is invalid. Note that all three arguments must be of the same type, either scalars (integers) or series.

An alternative call is also supported: if a single argument is given, it is taken to be a date (or series of dates) in ISO 8601 "basic" numeric format, YYYYMMDD. So the following two calls produce the same result, namely 2 (Tuesday).

```
	  eval weekday(1990, 5, 1)
	  eval weekday(19900501)
```


A common alternative numbering for days of the week runs from Monday = 1 to Sunday = 7. If you have a series named wd obtained via weekday and you want to convert to the alternative you can do

```
	  altwd = wd == 0 ? 7 : wd
```


Note that if you simply add 1 to wd you get a numbering that's valid but non-standard, namely Sunday = 1 to Saturday = 7.

* * *

wmean
-----

**Output:** series


|Arguments:|Y (list)                   |
|----------|---------------------------|
|          |W (list)                   |
|          |partial (boolean, optional)|


Returns a series _y_ such that _y_t is the weighted mean of the values of the variables in list _Y_ at observation _t_, the respective weights given by the values of the variables in list _W_ at _t_. The weights can therefore be time-varying. The lists _Y_ and _W_ must be of the same length and the weights must be non-negative.

By default the result is NA if any values are missing at observation _t_, but if you pass a non-zero value for _partial_ any non-missing values will be used.

See also wsd, wvar.

* * *

wsd
---

**Output:** series


|Arguments:|Y (list)                   |
|----------|---------------------------|
|          |W (list)                   |
|          |partial (boolean, optional)|


Returns a series _y_ such that _y_t is the weighted sample standard deviation of the values of the variables in list _Y_ at observation _t_, the respective weights given by the values of the variables in list _W_ at _t_. The weights can therefore be time-varying. The lists _Y_ and _W_ must be of the same length and the weights must be non-negative.

By default the result is NA if any values are missing at observation _t_, but if you pass a non-zero value for _partial_ any non-missing values will be used.

See also wmean, wvar.

* * *

wvar
----

**Output:** series


|Arguments:|X (list)                   |
|----------|---------------------------|
|          |W (list)                   |
|          |partial (boolean, optional)|


Returns a series _y_ such that _y_t is the weighted sample variance of the values of the variables in list _X_ at observation _t_, the respective weights given by the values of the variables in list _W_ at _t_. The weights can therefore be time-varying. The lists _Y_ and _W_ must be of the same length and the weights must be non-negative.

By default the result is NA if any values are missing at observation _t_, but if you pass a non-zero value for _partial_ any non-missing values will be used.

See also wmean, wsd.

* * *

xmlget
------

**Output:** string


|Arguments:|buf (string)                            |
|----------|----------------------------------------|
|          |path (string or array of strings)       |
|          |&matches (reference to scalar, optional)|


The argument _buf_ should be an XML buffer, as may be retrieved from a suitable website via the curl function (or read from file via readfile), and the _path_ argument should be either a single XPath specification or an array of such.

This function returns a string representing the data found in the XML buffer at the specified path. If multiple nodes match the path expression the items of data are printed one per line in the returned string. If an array of paths is given as the second argument the returned string takes the form of a comma-separated buffer, with column _i_ holding the matches from path _i_. In this case if a string obtained from the XML buffer contains any spaces or commas it is wrapped in double quotes.

By default an error is flagged if _path_ is not matched in the XML buffer, but this behavior is modified if you pass the third, optional argument: in that case the argument retrieves a count of the matches and an empty string is returned if there are none. Example call:

```
	  ngot = 0
	  ret = xmlget(xbuf, "//some/thing", &ngot)
```


However, an error is still flagged in case of a malformed query.

A good introduction to XPath usage and syntax can be found at https://www.w3schools.com/xml/xml\_xpath.asp. The back-end for xmlget is provided by the xpath module of libxml2, which supports XPath 1.0 but not XPath 2.0.

See also jsonget, readfile.

* * *

zeromiss
--------

**Output:** same type as input



Converts zeros to NAs. If _x_ is a series or matrix, the conversion is done element by element. See also missing, misszero, ok.

* * *

zeros
-----

**Output:** matrix


|Arguments:|r (integer)          |
|----------|---------------------|
|          |c (integer, optional)|


Outputs a zero matrix with _r_ rows and _c_ columns. If omitted, the number of columns defaults to 1 (column vector). See also ones, seq.

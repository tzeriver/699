Interim Presentation
========================================================
author: Dylan Sun & Zijiang Yang
date: 
autosize: true

Objectives
========================================================

- Determining the erectile function rates following SBRT
- Determining predictors of erectile function preservation after SBRT

Hypotheses
========================================================
Negatively Associated:
- Age, Gleason Score, T-stage, PSA, ADT, BMI

Positively Associated:
- HRQOL, Erectile Function at Baseline

We expect HRQOL and Erectile Function at Baseline to be highly correlated, because erectile function is included in the questionnaire. 

Questions and Concerns
========================================================
- BMI Outlier

![plot of chunk unnamed-chunk-1](Presentation-figure/unnamed-chunk-1-1.png)

***
Subject 67 has a BMI of 112. 
This is theoretically possible.


========================================================
![plot of chunk unnamed-chunk-2](Presentation-figure/unnamed-chunk-2-1.png)


Tables
========================================================

| never_functional| gain_function| loss_function| retain_function|
|----------------:|-------------:|-------------:|---------------:|
|              153|            14|            70|              88|

Model
========================================================
$logit(EF2) = \beta_{intercept} + \beta_{age} Age + \beta_{Gleason} Gleason + \beta_{Tstage} TStage + \beta_{PSA} PSA \\
+ \beta_{HRQOL} HRQOL + \beta_{ADT} ADT + \beta_{BMI} BMI + \beta_{EFbase} EFBase$

Results
========================================================

|term                            |   estimate| std.error|  statistic|   p.value|
|:-------------------------------|----------:|---------:|----------:|---------:|
|(Intercept)                     |  0.6215224| 0.3389228|  1.8338172| 0.0676215|
|Age                             | -0.0094434| 0.0034752| -2.7173835| 0.0069428|
|`Gleason Score`                 |  0.0078768| 0.0372337|  0.2115504| 0.8325942|
|`T-Stage Group`                 | -0.0511802| 0.0628191| -0.8147237| 0.4158440|
|PSA                             |  0.0099910| 0.0047340|  2.1104646| 0.0356039|
|HRQOL                           |  0.0029451| 0.0010672|  2.7596882| 0.0061232|
|ADT                             | -0.0909474| 0.0772114| -1.1779012| 0.2397223|
|BMI                             | -0.0024765| 0.0033832| -0.7319945| 0.4647145|
|`Erectile Function at Baseline` |  0.2867081| 0.0659157|  4.3496193| 0.0000184|

Results
========================================================
Error rate = $\dfrac{\sum |predicted-actual|}{total}$

```
[1] 0.2123077
```

Future Plan
========================================================

Intro to ROC Curves
================
Bindoff, A. D.
2022-08-22

*Receiver operating characteristic* (ROC) curves are a graphical method
of determining the diagnostic accuracy of a test over a full range of
thresholds or cut-off values. One way to compare two tests is by
calculating the *area under the curve* (AUC) for each ROC curve. The
diagnostic test with the curve that encompasses the most area (highest
AUC) usually has the best trade-off between sensitivity (ability to pick
up positive cases) and specificity (ability to discriminate between
positive and negative cases).

In this example we will compare the diagnostic accuracy of 3 imaginary
biomarkers (imaginatively named m1, m2, and m3) in detecting Alzheimer’s
Disease (AD) pathology. These data are simulated, but at the Wicking
Centre the diagnostic accuracy of protein concentrations in blood,
performance on motor-cognitive tasks and other tests is an active area
of research as we try to diagnose AD earlier, before symptoms become
readily apparent (a stage known as ‘pre-clinical AD’).

We will begin by looking at the diagnostic properties of *m1*, so that
we can understand what the ROC curve is telling us.

![](Intro-to-ROC-curves_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

The plot on the left is called a *beeswarm plot*. It shows the
distribution of biomarker concentrations in Control and pre-clinical AD
participants. The plot on the right is the ROC curve. The curve shows
thresholds for the biomarker plotted against the fraction of true and
false positives (y-axis and x-axis respectively). The true positive
fraction is the proportion of people with pre-clinical AD (in this
example) who would test positive for pre-clinical AD above a given
threshold. The false positive fraction is the proportion of people who
do not have pre-clinical AD but would test positive for pre-clinical AD
above a given threshold. In this example, lower thresholds correspond to
higher true positive fractions (higher sensitivity - good!) but with the
trade-off of higher false positive fractions (lower specificity - bad!)

Question 1: The labelled points on the curve (in blue) are the
thresholds. What is the “true positive fraction” and the “false positive
fraction” for threshold = 0.5? Find 0.5 on the y-axis of the beeswarm
plot, do these fractions look right to you?

Question 2: Imagine we have a promising treatment that slows the
progression of AD if given early enough. Unfortunately, it also carries
the risk of serious side effects. You wish to test the treatment on
participants with pre-clinical AD, so you screen participants using
biomarker m1. Which part of the curve would you choose your threshold
from?

Question 3: You develop a keyboard tapping test that has poor diagnostic
accuracy, but anyone can take the test at home for free. You don’t want
to unnecessarily concern people who take the test and get a score which
indicates a higher risk of pre-clinical AD, but you also don’t want
those people not to go to their doctor for more costly/invasive
diagnostic testing so that they can get appropriate care. Which cut-off
would you choose, and what are the advantages and disadvantages of
choosing a different cut-off?

We will now compare biomarkers m1, m2, and m3. The plotted boxes show
the median, 25th and 75th percentiles of biomarker concentrations.
Notice that the difference in medians between AD and healthy controls is
the same for m1 and m3, but the difference for m2 is roughly twice as
big.

![](Intro-to-ROC-curves_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

Now consider the variability (how much the points are spread out, which
is conveniently summarised by the 25th and 75th percentiles plotted
here). Biomarker m3 clearly has less variability. Because the data are
simulated, I know that m1 and m2 have the same variability (compare the
controls), and less obviously, m3 has half the variability of m1 and m2.

Before we look at the ROC curves, which biomarker do you think will have
the smallest AUC (worst diagnostic accuracy)? Do any stand out as having
the highest AUC?

![](Intro-to-ROC-curves_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

Question 4: Assuming we can obtain any of the three biomarkers for the
same cost and inconvenience to the patient, are there any biomarkers you
would not bother to obtain? Are there any that stand out as having the
best diagnostic accuracy?

Extra credit question: The year is 2020, a highly infectious and
dangerous new virus is circulating with similar symptoms to many other
viruses. People with any symptoms are encouraged to get tested so that
they don’t spread the new and dangerous virus if positive.

The laboratory analysing the swabs has a choice between running the test
for fewer cycles and missing true positive cases, or running the test
for more cycles and diagnosing more false positives. You are a
biostatistician, so they ask you which course of action they should
take - what advice do you give them? What are the consequences of not
following your advice? Is there a downside to following your excellent
advice?

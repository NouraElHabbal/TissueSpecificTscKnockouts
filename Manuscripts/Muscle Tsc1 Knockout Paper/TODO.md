
# First Submission ToDo List

Comments from MCM, DS, ARS, QT

No Comments from MP, KF

No Response from BL, JCH, JRR

## General Comments About Article

ARS: Very interesting study, but I think there are a lot of things missing that the reviewers will ding you on no matter where you send the paper.  I mentioned a few of these in the text.  I didn’t really do a serious rewrite of the paper since I think these missing experiments really need attention.  I think the biggest question is why there is such a big decrease in fat mass, with such a small effect on energy expenditure.  I get that there is a lot of muscle, but still…..  There are lots of missing things- same measurements in ND and HFD, incomplete reporting on metabolic cage studies, serum levels of insulin, glucose, ffas, leptin, cytokines, etc. It just needs a lot more.  I don’t think AJP is taking papers like this that aren’t really complete.  Also what about insulin sensitivity in muscle?  I think you also need measurements of fat and glucose oxidation- not that hard to do.  Sorry to sound so negative.  I think reviewers will be much harsher.

QT: I think Figure 4 and the text related to this figure need a bit of work.

## Comments to Think About

* **Both short term overfeeding and chronic obesity result in increased energy expenditure.**  - very controversial, I don’t agree.  Yes to short term, no to long term (ARS)
* **This is consistent with the hypothesis that the adiposity is inversely related to insulin sensitivity and that these mice are not lipodystrophic, but the mice with muscle Tsc1 knockout are protected from adipose tissue expansion via changes in energy balance.** Was this on normal or HFD?  Looks like ND.  How do you explain that?  You’d think that the muscle would be insulin resistant. (ARS).  Related to this maybe we should include the ITT and glucose clamp data showing no changes in insulin sensitivity on NCD (DB).
* For Mixed linear models.  I don’t think we should use Chi-square test here because they are continuous variables. I will check the R codes and let you know. (QT).
* I think the biggest question is why there is such a big decrease in fat mass, with such a small effect on energy expenditure. (ARS).  We could calculate out what the expected change in energy balance would be based on our measured intake/increases in energy expenditure and see if that comes close to matching.  It would be tricky because it wouldnt account for an adaptation, but for example if there was a 7% increase in EE how much less fat mass would be expected.  Ill think about this (DB)
* incomplete reporting on metabolic cage studies, serum levels of insulin, glucose, ffas, leptin, cytokines, etc. It just needs a lot more. (ARS).  Not sure what is missing about metabolic cage stuff.  Im not sure if we have insulin/FFAs/leptin/cytokines but i can look into what 70d old blood we have available.  
* I think you also need measurements of fat and glucose oxidation- not that hard to do (ARS).  

## Things to Change

* Can we stick with the same color scheme used in Figure 1, i.e. knockout is in cyan (greenish color) and wild-type/control is in pink/orange. We have these 2 colors switched in Figure 2. (QT).
* Same here. Can we use color for the bar plot just like the one in Figure 1? It is easier if we use the same color scheme throughout so when we look at the figures, we know cyan is knockout and red/pink/oranges (pick one) is control.  If not, then everything should be in dark gray or light gray with labels (like in the figure 3C). Too many colors are used here. (QT)
* Add Body weight to Figure 3.
* Add insulin sensitivity to Figure 2, including an exlanation of why they are **not** insulin resistant.
* Rewrite section describing Figure 4 or the figure, so that panels are described in the same order that they appear (see QT comments).
---
layout: entry
title: Documentation for Disease-Lifestyle Relations Annotation
---

## Annotation scope

The scope of this annotation is to detect lifestyle factors which affect the risk of disease onset and development. Below are some general examples of the guidelines that will be used in the annotation.

## General guidelines

* Annotations should be made according to the annotator’s best understanding of the __author’s intended meaning in context__. 
* Annotators should treat named entities as being __masked__, i.e. they shouldn't annotate relationships between entities just based on their names, when they would be unable to make the same annotations for two other entities.
* Annotators can assign multiple relationships between entities when applicable.

### What to annotate:

1. Causal relationship: _LSF causes disease_ / _disease causes LSF_.
Examples:
    * A __LSF__ causes a __disease__.
    * A __LSF__  contributes to the development of a __disease__.  
    * A __LSF__  developed a __disease__.
    * A __LSF__ is a recognized/reversible/know/common cause of a __disease__
    * __LSF__-induced __disease__
    * A __LSF__ may induce a __disease__.
    * A __LSF__ increases a __disease__ mortality.
    * A __disease__ is a result/side-effect of a __LSF__.
    * A __disease__ is attributed to / transmitted by / determined by a __LSF__.
    * The consequences of a __LSF__ is a __disease__.

2. Statistically associated relationship: _LSF is statistically associated with disease_. 
Examples:
    * A __LSF__ is associated with a __disease__.
    * A __LSF__ is associated with the development of __disease__.
    * A __LSF__ is associated with the risk of a __disease__.
    * A __LSF__ is associated with __disease__ treatment and control.
    * A __LSF__ has a role in/effect on a __disease__.

    2.1 Positive statistical association:
      * A __LSF__ increases the risk of a __disease__.
      * A __LSF__ is the risk factor a __disease__.
      * A __LSF__ carries a risk of a __disease__.
      * A __LSF__ is a predictor of a __disease__.
      * A __disease__ is characterized by a __LSF__.
      * __disease__ patients were more likely to practice __LSF__ than controls.
      * A __LSF__ increases incidence of a __disease__.
      * A __LSF__ increases the risk of developing a __disease__.
      * A __LSF__ increases prevalence of a __disease__.
      * A __LSF__ contributes to the burden of a __disease__.
      * A __LSF__ is linked/connected to a __disease__. &rarr; (implies positive direction and is always used as such)
      * A __LSF__ should be considered during risk stratification for a __disease__.
      * The prevalence of __LSF__ was higher in __disease__ patients than in controls. &rarr; (such a **comparative** mention in abstracts implies significance in the majority of cases even when significance is omitted. Comparative prevalence numbers (x % vs x'%) can also work).



    2.2 Negative statistical association:
      * A __LSF__ decreases the risk of a __disease__.
      * A __LSF__ decreases incidence of a __disease__.
      * A __LSF__ decreases prevalence of a __disease__.
      * A __LSF__ could be critical in the current fight against __disease__.
      * A __LSF__ is inversely associated with a __disease__.
      * The prevalence of __LSF__ was lower in __disease__ patients than in controls.
      
3. Controls: _LSF controls disease_. Examples:
    * A __LSF__ play a regulatory role in __disease__.
    * A __LSF__ has beneficial effect for the control of __disease__.
    * A __LSF__ improves survival outcomes in __disease__.
    * A __LSF__ decreases/reduces/attenuates __disease__ &rarr; (not the prevalence of __disease__).

    3.1 Prevents relationship: _LSF prevents disease_ / _disease prevents LSF_. Examples:
     * A __LSF__ is therefore imperative for preventing a __disease__ morbidity and mortality.
     * A __LSF__ is chemopreventive in a __disease__.
     * A __LSF__ is protected against a __disease__.
     * A __LSF__ reduce a __disease__ mortality.

    3.2 Therapeutic relationship: _LSF treats disease_.
    Examples:
     * The treatment of a __disease__ includes a __LSF__.
     * A __LSF__ is essential for treating a __disease__.
     * A __LSF__ is used for the therapy of a __disease__.
     * The efficacy of a __LSF__  in a __disease__.
     * A __LSF__ is the relief of a __disease__.
     * A __LSF__ is was effective in a __disease__.
     * A __disease__ were eliminated by a __LSF__.
     * A __disease__ were improved after (using) a __LSF__.

4. No statistical association: _LSF is not associated with disease_. Examples:
    * A __LSF__ is **not** associated with a __disease__.
    * There is no association between __LSF__ and __disease__.

### What **NOT** to annotate:
1. Hypothetical statements: 

    “Here we study the link between LSF and disease”.<br />
    "It is possible to suspect a relationship between ESRD and insecticides or pesticides".<br />
    "LSF might be involved in Dis". → Take context into consideration in case this is no more than a hypothesis.
    
2. Tendency but no statistical significance : 

    “We **did not** find the relationship between LSF and disease to be statistically significant” / "There is an association between __LSF__ and __disease__, but **no significance**".

3. No statistical test implied/ no control group comparison:
    
    “A majority percentage of HIV-positive MSM engage in unprotected sexual behavior”. → other individuals without HIV could have the same behavior.\
    “A total of 45% of children receiving __LSF__ had no symptom recurrence of __disease__”.<br />
    “In our study, __disease__ was very common in __LSF__ practitioners”.<br />
    “In our study, 54% of cancer patients suffer from poor sleep and 34% of low energy”. → What is problematic is not the lack of a significance report but the **absence of a control group** implication in all above cases. We cannot make an assumption that a statistical test was actually performed.

    _or_
    
    Observation:

    “Cannabis is the most widely used illicit substance in the United States with especially high prevalence of use among those with psychiatric disorders.”
    

5. LSF that is a part of a bigger Named entity: sleep in multiple sleep latency test (MSLT)
6. Do NOT annotate "... in/among LSF/DIS":

    __Dairy farmers__ is not part of relation: Among __dairy farmers__, moreover, __lung cancer__ SMRs showed a significant downward trend across the quartiles of increasing __length of work__.

7. Statistical associations should not be annotated if p-value is greater than 0.05.
8. Statistical associations should not be annotated if CI encompasses 1.0.
9. Inconsistent/Debatable evidence → do not annotate.
   


### Special rules for relationships:
1. Across sentence boundaries should be annotated.<br />In cases of co-reference ("this","it" etc.), annotate only the previous entity mention in the relation.<br />Annotate taking into account the wider context, not just the present sentence.<br />
2. “Is believed” should be annotated.

    “Air pollutants are believed to induce or exacerbate a range of inflammatory diseases (atopic dermatitis...)”.
   
3. In cases where "Limited/Weak/Poor/Little evidence" is mentioned → Judge the author’s intention: If the author implies that the evidence is inadequate, do not annotate. In the opposite case, annotate. 

    “Results provide limited evidence for an association of early-life mobile source air pollution with childhood asthma incidence ...”.
4. Animal experiments should be annotated, as they are supposed to be a model for a human disease.

5. Be careful with an occupation + a clause with LSFs. 

    In the following examples, farmers __should not__ be linked with acute lymphatic or chronic lymphatic leukemia.<br />

    “Farmers from major corn-producing, hog- and chicken-raising, and pesticide- and fertilizer-using counties tended to be at higher risk of acute lymphatic”.<br />

    “Farmers from counties with large cattle inventories and significant dairy activity were at higher risk of chronic lymphatic leukemia”.<br />

6. Annotate what the sentence says, even if there are contradictory statement. Example:
    
    Previous study shows A causes B… : annotate A Cause B.

    In contrast to the previous study, A causes C, or C causes B or no relation… : annotate either A causes C, C causes B or nothing

7. Mentions of “the X-Y association” between an LSF X and a disease Y should be annotated as statistically associated relationships.<br />
8. Ambiguous/Hedging expressions (sentences such as “LSF MAY/MIGHT affect the development of Dis”):<br />
     Annotate as affirmative statements only if the context provided by the rest of the sentence indicates significant findings produced in the study. For example, in sentence: “Our data suggest that LSF and/or other related sources MAY reduce the risk of Dis” → “our data suggest” suggests that a study was performed prior to this statement instead of it being a hypothesis to be tested.<br />
   

9. Indirect relations:\
   a) Both direct and indirect associations should be annotated, for example in sentence 1: “LSF1 is associated with Dis, but the association seems to be mainly mediated by LSF2”. → annotate both LSF1 and LSF2 as statistically associated with Dis.\
      However, in cases such as sentence 2: “__LSF__ was not independently associated with __disease__” , do not annotate unless it specifically mentions that the LSF was dependently associated.\
   b) Do not annotate indirect relations that stem from deductive reasoning, for example in sentence 3: “LSF contributes to the inflammatory response. Inflammation can lead to various diseases such as Dis1, Dis2, Dis3”. → do not relate LSF with Dis1, Dis2, Dis3.\
      Consistently, do not annotate cases such as sentence 4: “Anthocyanins, commonly found in fruits and vegetables, help delay Dis in mouse models/cell cultures”. → only relate anthocyanins with Dis, not fruits and vegetables with Dis.\
   
10. Relationships like the following: 

    __LSF1__ and __LSF2__ when present together cause disease __disease__, but when __LSF1__ is present alone it **does not** cause __disease__.
    
    Annotate as _LSF1 causes disease_, _LSF2 causes disease_ (for the first sentence) and no annotations between LSF1 and disease in the second sentence.

11. Compared/comparison:
 a) if the comparison is between LSF/not having LSF or Dis/not having Dis then annotate only LSF to Dis with the appropriate relationship (not the not-LSF or not-Dis).

   “The seizure rate was significantly higher in cocaine users (37 [26%] of 142 patients) than in non-cocaine users (151 [15.2%] of 992 patients, p = 0.001)”. → Annotate Positive SA between cocaine and seizure.
 b) if the comparison is between separate things (eg one type of cancer to another) then annotate based on the direction you would assume could be applied if the comparison were cancer/healthy controls or **do not annotate at all** if assuming is not possible.\

   “The proportion of patients working in professions with exposures to known carcinogens was 33.5% for lung cancer, and 17.1% for large bowel cancer (p=0.000)”. → carcinogens cause cancer, so since lung cancer patients were more likely to work in carcinogen exposed professions than LB cancer patients then it is safe to say that lung cancer is positively associated with carcinogens (no annotation for LB cancer)”.

12. Annotate relationships even when they are not independent.
13. Also consider numbers in ORs, HRs, RRs for the direction of the association, even if not specifically written in words as “positive” or “negative” (eg OR>1 means positive association and OR<1 means negative association).

   
   “__SO2__ was also significantly associated with __birth defects__ in the second month before the pregnancy (aOR = 1.31; 95% CI: 1.20 ~ 3.22)”.

14. A __LSF__ used as defense for a __disease__. → annotate either as treats or prevents according to context.
      
15. Annotate LSF and **Disease mortality** associations as LSF and **Disease**.
    

## Annotation process
* The annotation process started by creating an initial set of annotation guidelines, which we improved in the second round. 
* Initial annotation guideline was formed and updated during a first round of Inter-Annotator Agreement (IAA) after three annotators individually annotated 30 abstracts and discussed their inconsistencies.
* A second round of IAA was performed with a fourth annotator by annotating a new set of 30 abstracts to further update and solidify the final guidelines.
* The annotators were not allowed to be in contact and discuss any cases before metric calculation for each IAA round, so as not to affect the measurements and negatively affect the process.
* A meeting was held after each round to discuss disagreements, update the guidelines, and clarify any ambiguities or gaps in the rules that caused the disagreements between the annotators.
* Evaluating the quality of the manual annotations in terms of inter-annotator agreement gave an F1-score of 82.1%.
* We subsequently annotated the entire LSD600 according to the final guidelines


   



### Detailed guidelines

For information on Annodoc, see <http://spyysalo.github.io/annodoc/>.

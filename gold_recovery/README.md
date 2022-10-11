# Recovery of gold from ore
The customer is a company that develops solutions for the efficient operation of industrial enterprises.

## Task
Prepare a prototype machine model. The model must predict the gold recovery rate from gold ore using data with mining and refining parameters.
The model will help optimize production so as not to launch an enterprise with unprofitable characteristics.
You need to predict two quantities at once:  
- efficiency of rough concentrate enrichment;  
- efficiency of enrichment of the final concentrate.  

**Technological process**  

When the mined ore undergoes primary processing, a crushed mixture is obtained. It is sent for flotation (enrichment) and two-stage purification:

Flotation  
1. A mixture of gold ore is fed into the flotation plant. After enrichment, a rough concentrate and “dump tails” are obtained, that is, product residues with a low concentration of valuable metals.  
The stability of this process is affected by the unstable and non-optimal physical and chemical state of the flotation pulp (a mixture of solid particles and liquid).
2. Cleaning  
The crude concentrate goes through two purifications. The output is the final concentrate and new final tailings.  

## Data

**Data Description**  

*Technological process:*  
- Rougher feed - feedstock  
- Rougher additions (or reagent additions) - flotation reagents: Xanthate, Sulphate, Depressant  
    - Xanthate - xanthate (promoter, or flotation activator);  
    - Sulphate - sulfate (in this production, sodium sulfide);  
    - Depressant - depressant (sodium silicate).  
- Rougher process (English "rough process") - flotation  
- Rougher tails  
- Float banks - flotation unit  
- Cleaner process - cleaning  
- Rougher Au - rough gold concentrate  
- Final Au - final gold concentrate  

*Stage parameters:*  
- air amount — air volume  
- fluid levels - fluid level  
- feed size - feed granule size  
- feed rate - feed rate  

*Name of features:*  

The name of the features should be:  
`[stage].[parameter_type].[parameter_name]`  
Example: `rougher.input.feed_ag`  

Possible values for the `[stage]` block:  
- rougher - flotation  
- primary_cleaner - primary cleaning  
- secondary_cleaner - secondary cleaning  
- final - final characteristics  
Possible values for the `[parameter_type]` block:  
- input — raw material parameters  
- output — product parameters  
- state — parameters characterizing the current state of the stage  
- calculation - calculated characteristics  

**Efficiency calculation**  

It is necessary to simulate the process of recovering gold from gold ore.  
Enrichment efficiency is calculated by the formula  

$Recovery = \frac{C\times{}(F - T)}{F\times{}(C - T)}\times{} 100$%  

where:
- C is the proportion of gold in the concentrate after flotation/refining;  
- F is the proportion of gold in the raw material/concentrate before flotation/refining;  
- T is the proportion of gold in tailings after flotation/cleaning.  

To predict the ratio, you need to find the proportion of gold in concentrates and tailings. Moreover, not only the final product is important, but also the rough concentrate.  

**Quality metric**

To solve the problem, a new quality metric is introduced - sMAPE (Symmetric Mean Absolute Percentage Error).

$sMAPE = \frac{1}{N} \displaystyle\sum_{i=1}^{N} \frac{|y_i - \hat{y_i}|}{(|y_i| + |\hat{y_i}| )/2} \times{} 100$%

where:  
- $y_i$ - the value of the target feature for the object with serial number i in the sample on which the quality is measured;  
- $\hat{y_i}$ - prediction value for the object with serial number i, for example, in the test sample;  
- N - the number of objects in the sample;  

You need to predict two quantities at once:  
- rough concentrate enrichment efficiency rougher.output.recovery;  
- efficiency of final concentrate final.output.recovery enrichment.  

The final metric consists of two values:  

$final sMAPE = 25$% $\times{} sMAPE(rougher) + 75$% $\times{} sMAPE(final)$

## Libraries used  
numpy, pandas, missingno, matplotlib, seaborn, sklearn

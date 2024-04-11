#### Oservations

 | Loss Type | Step | Training Loss | Validation Loss | Rewards/chosen | Rewards/rejected | Rewards/accuracies | Rewards/margins | Logps/rejected | Logps/chosen | Logits/rejected | Logits/chosen | Training Time |
|-----------|------|---------------|-----------------|----------------|------------------|---------------------|-----------------|----------------|--------------|-----------------|---------------|---------------|
| sigmoid   | 700  | 1.046600      | 0.818465        | -6.640719      | -9.874228        | 0.746366            | 3.233507        | -422.851959    | -426.357910  | -2.316090       | -2.453040     | 4h 24min 16s  |
| sigmoid   | 1400 | 0.703900      | 0.705096        | -6.530509      | -12.535101       | 0.808503            | 6.004593        | -449.460724    | -425.255829  | -2.141517       | -2.255401     | 4h 24min 16s  |
| sigmoid   | 2100 | 0.951900      | 0.602490        | -7.816830      | -14.538786       | 0.831032            | 6.721958        | -469.497559    | -438.118958  | -2.191130       | -2.306392     | 4h 24min 16s  |
| kto pair  | 700  | 0.226100      | 0.269065        | 3.838436       | 0.520103         | 0.695131             | 3.318334        | -302.432556    | -312.774078  | -2.400373       | -2.510294     | 4h 23min 11s  |
| kto pair  | 1400 | 0.193400      | 0.219717        | 3.091814       | -2.054316        | 0.780160             | 5.146130        | -328.176758    | -320.240265  | -2.314026       | -2.431551     | 4h 23min 11s  |
| kto pair  | 2100 | 0.216300      | 0.202358        | 3.923744       | -1.219949        | 0.787064             | 5.143694        | -319.833069    | -311.920959  | -2.282722       | -2.413529     | 4h 23min 11s  |
| ipo       | 700  | 17.787100     | 16.408241       | -0.224279      | -0.370638        | 0.790334             | 0.146359        | -5.773531      | -3.824460    | -1.842325       | -1.883672     | 4h 26min 28s  |
| ipo       | 1400 | 13.421200     | 14.549047       | -0.492412      | -0.738297        | 0.809230             | 0.245885        | -9.450124      | -6.505787    | -0.917404       | -0.950979     | 4h 26min 28s  |
| ipo       | 2100 | 13.266500     | 13.640387       | -0.469297      | -0.702615        | 0.823401             | 0.233318        | -9.093308      | -6.274642    | -0.821429       | -0.842232     | 4h 26min 28s  |
| hinge     | 700  | 0.920500      | 0.733086        | -4.056917      | -6.304759        | 0.748910             | 2.247841        | -377.882416    | -394.461884  | -2.574166       | -2.650745     | 4:01:02       |
| hinge     | 1400 | 0.649300      | 0.653185        | -4.023954      | -7.192891        | 0.788881             | 3.168936        | -386.763702    | -394.132172  | -2.456152       | -2.546264     | 4:01:02       |
| hinge     | 2100 | 0.663000      | 0.590392        | -3.597967      | -6.356043        | 0.795422             | 2.758075        | -378.395294    | -389.872375  | -2.420573       | -2.499924     | 4:01:02       |


 #### Conclusion

 1. The kto pair loss type shows the lowest training and validation losses consistently across all steps. This suggests it's learning more effectively and generalizing better than the others.
 2. The kto pair loss type again stands out with generally positive rewards for chosen actions and improving accuracies and margins over steps, indicating a balance between exploration and exploitation and an increasing ability to differentiate between actions over time.
 3. The hinge loss type has the shortest training time, but its performance metrics do not match those of the kto pair loss type.
 
 #### References
 1. https://towardsdatascience.com/fine-tune-a-mistral-7b-model-with-direct-preference-optimization-708042745aac
 2. https://colab.research.google.com/drive/15iFBr1xWgztXvhrj5I9fBv20c7CFOPBE?usp=sharing
 

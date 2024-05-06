# Coral Shield Project

## Overview
Coral Shield is a synthetic biology project aimed at protecting coral reefs from the harmful effects of oxybenzone, 
a common ingredient in sunscreen that contributes to coral bleaching. This repository contains the biological 
circuit designs and the SimBiology model files used to simulate and validate the efficacy of the oxybenzone 
detection and degradation system.

## Repository Structure
## Biological Circuit
In the first biological circuit, ADH1 is used as a constitutive promoter that enables the continual transcription of GEM protein. Once GEM protein is expressed, the biomarker, oxybenzone, if present in the surroundings, can bind to the estrogen receptor component of GEM protein as an agonist. This complex of GEM protein bound to an estrogenic compound like oxybenzone can then move into the nucleus. The DNA binding domain and activator component of the GEM protein then act as an inducer to activate GAL1, a regulatory promoter. GAL1 involves a positive inducible system where activation of GAL1 initiates transcription of the second biological circuit.

The second circuit begins with the activated GEM protein and oxybenzone complex binding to the GAL4 binding sites on the operator which induces the activity of the coupled GAL1 promoter. This circuit contains two DNA coding sequences for the enzyme laccase and the chromoprotein eforRed. In the presence of the mediator ABTS, laccase can recognize and break down oxybenzone by catalyzing the reaction with molecular oxygen, creating a species that cannot be converted into the conjugate phototoxic glucoside. This mediator is required as laccase alone is unable to bind to or recognize oxybenzone. Several mediators are suitable for this reaction, however, all of them are either synthetic, or their biosynthesis pathway is not completely understood. Since the mediator cannot be produced intracellularly, the solution uses a synthetic mediator which is affordable and less likely to interact with other chemicals within the system. During laboratory investigation, ABTS will be introduced into the test by the experimenter. This is intended to be a temporary solution and act as a proof of concept, with a final solution producing its own mediator once the necessary pathways have been further studied. This is where the chromoprotein comes in as it will be important to notify the experimenter when ABTS may be required.

## SimBiology Model
The SimBiology model simulates the interactions within the biological circuit in response to oxybenzone presence in a marine environment. 
It uses detailed reaction kinetics and has been parameterized based on laboratory and literature data. To run the simulations, 
navigate to the `/SimBiologyModel` directory.



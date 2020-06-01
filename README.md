# MoF3D
Modelling Forests in 3 Dimensions

This is the repository with the codes and executables for a mechanistic model for simulating realistic functional-structural forests in 3D (DFG project ModVE, number SA-21331).

To run the code, it is necessary to install GroIMP (https://sourceforge.net/projects/groimp/), a 3D modelling plattform written in Java. Hence, it is also necessary to have Java installed. After downloading GroIMP, open the program from the desktop shortcut icon, then open the code and modify the path of the code and input files as well as the path in which output files should be saved in (one for the raw data, one for pictures):
/**Set model folder*/  
static String folderMain = "C:\\Users\\Yourpath"; //name of the folder with the java code
static String namePictureFile = "My_Experiment"; //name of experiment
static String folderParam = folderMain + "\\Model"; //folder in which the main model script and the pass/global files are located
static String folderReport = folderMain + "\\Results"; //folder in which the model results are saved to file
static String folderPictures = folderMain + "\\Pictures\\"; //folder in which images are saved to file

Save the modified code and on the left field of the programm hit the button 'run' to run each time step by consequent clicking, or hit the buttun 'run run' to simulate the entire simulation experiment.

The model recognizes two types of input files for running a simulation, which is found in a folder that here is called 'Model':
1) The first type of file is called "Forest_param_global" and there should be only one of this type of file in the folder, in which global parameters for the simulation experiment can be specified:

Timesteps	80 (Number of time steps in years)

Replicates	1 (Number of replicate runs, each requires a pass file?)

MaxX	50 (Extent in grid cells at the X dimension)

MaxY	50 (Extent in grid cells at the Y dimension)

MaxZ	80 (Extent in grid cells at the Z dimension, height above ground)

WidthCorridor	20 (Extent in grid cells of a buffer zone for edge effects?)

VoxelSize	1 (3D grain in grid cells or meter)

ReportForest	1 (if 1: save forest outputs to file; if 0: no output saved to file at the forest level)

ReportLight	1 (if 1: save distribution of light conditions to file; if 0: no output saved to file)

ReportMortality	1 (if 1: save mortality tallies to file; if 0: no output saved to file)

ReportShoots	1 (if 1: save shoot outputs to file; if 0: no output saved to file at the shoot level)

ReportTrees	1 (if 1: save forest outputs to file; if 0: no output saved to file at the tree level)

ReportVoxel	1 (if 1: save forest outputs to file; if 0: no output saved to file at the voxel level)

SimulateForest	0 (if 1: simulate entire forest; if 0: simulate single tree ?)

ThreadCount	2 (?)

VisualizationMethod	2 (?)

VisualizationShader	1 (?)

    
 2) The second type of file is called "Forest_param_pass" pasted with a number (Replicate -1) that refers to the replicate. There should be as many pass files as there should be replicates. These pass files contain the parameters of the environment and tree species:

LightC	1

ALMax	15000

ALProdMax_Min	65000

ALProdMax_Max	65000

LDTreeDev_Min	-0.8

LDTreeDev_Max	0.8

BetaD_Min	0.1

BetaD_Max	0.3

LightThreshApical_Min	30

LightThreshApical_Max	100

BetaS	3

CarbonOverheadCosts	1.45

CBLratio	0.5

CBWratio	0.5

MortalityDisturbanceRate	0

MortalityDisturbanceFrequency	0

AngleFirstOrderSideView_Min	0

AngleFirstOrderSideView_Max	40

PhyllotaxisFirstOrder_Min	3

PhyllotaxisFirstOrder_Max	5

AngleSecondOrderTopView_Min	20

AngleSecondOrderTopView_Max	60

Imax	900

InitialDiamter	5e-04

InternodeLengthBranchMin_Min	0.3

InternodeLengthBranchMin_Max	0.4

InternodeLengthBranchMax_Min	0.4

InternodeLengthBranchMax_Max	0.6

InternodeLengthTrunkMin_Min	0.3

InternodeLengthTrunkMin_Max	0.5

InternodeLengthTrunkMax_Min	0.5

InternodeLengthTrunkMax_Max	0.7

KInt_Min	0.01

KInt_Max	0.02

LightExtinctionCoeff	0.6

LDBranch	3

LPratio	40000

DistanceVoxelLightCal	4

MinLeafBiomass	30

MortalityBiomassRate	0.032

MortalityBiomassScalingExponent	0.13

MortalityNeighMinDiameter	0.15

MortalityNeighRate	0.05

RespirationRateWood	5e-04

NumberSeedlingPerHa_Min	500

NumberSeedlingPerHa_Max	500

ShorteningFactor_Min	0.7

ShorteningFactor_Max	0.9

SiteIndex	0.9

SLA_Min	50

SLA_Max	200

NumberSpecies	1000

Stochasticity	1

StochasticityTwisting_Min	2

StochasticityTwisting_Max	7

StochasticityAngleSecondOrderTopView_Min	0

StochasticityAngleSecondOrderTopView_Max	10

StochasticityTropismStrength_Min	0

StochasticityTropismStrength_Max	0.02

StochasticityAngleFirstOrderSideView_Min	5

StochasticityAngleFirstOrderSideView_Max	10

StochasticityAngleFirstOrderTopView_Min	0

StochasticityAngleFirstOrderTopView_Max	20

StopCriterionBasalArea	80

TropismStrength_Min	-0.02

TropismStrength_Max	0.02

WoodDensity_Min	0.5

WoodDensity_Max	0.7

PipeReuseFactor_Min	0.6

PipeReuseFactor_Max	0.6

Tyear	270

Hsun	8

TreeCompetionNum	0

TreeCompetionDist	6

BranchMortMethod	0

BranchMortRandomRate	0.2

BranchMortMassRate	0.02

BranchMortMassScalingExponent	0.2

TreeMortNeigh	1

TreeMortBiomass	1

TreeMortCarbon	1

TreeMortDist	0

PipeLengthMethod	1

FormFactorWood	0.55

SafetyFactorTrunk	0.3

EdgeC	0

BrCollide	1

MethodBranchGrowth	1

ALProdMaxMethod	0

BranchLossMinBiomass	100





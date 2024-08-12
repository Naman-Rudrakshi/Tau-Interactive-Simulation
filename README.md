This is the code for my group's research project at the Research in Science and Engineering Summer Program at Boston University in the summer of 2024. This project was a collaborative effort among five students. 

Backend: Python, handles simulation
Frontend: HTML/CSS/JS: displays interactive results of simulation in 3D

Below is the research project proposal for our simulation:


Modeling the Spread of Tau Proteins in Small Brain Regions

Our project is aimed towards modeling the spread of tau protein aggregation throughout regions of the brain. Tau protein is heavily associated with the stability of microtubules, a structure found in the cytoplasm of cells, essential for cell integrity. However, tau proteins can undergo hyperphosphorylation, a process that inhibits the binding of tau proteins to microtubules, compromising its stabilization and axonal transport. During hyperphosphorylation, tau proteins detach from the microtubules and become free floating, sticking to other tau proteins and forming tangles within the intracellular space–tangles that inhibit proper neuron function and are associated with neurodegenerative diseases. Patients with neurodegenerative diseases have been found to have over three times the amount of tau proteins in the brain as compared to healthy individuals. 

	Our aim is to create a basic three dimensional model of how tangles of tau proteins form and spread throughout a homogeneous region of the brain, potentially later applying our model to specific heterogeneous regions of the brain (Note: “brain region” in this context refers to a cube of brain matter composed of several smaller cubes–brain packets. Each packet connects directly to the packet surrounding it with connective strengths that we will specify. “Homogeneous” refers to a region where all constituent packets have equal connective strength and are equally spaced, while “heterogeneous” refers to a region with variance in these factors). We will create our own programmatic, discrete Laplacian function to model our three dimensional space of heterogeneous brain matter, similar to the continuous mathematical Laplacian function used to represent the proximity and connectivity gradients in a realistic 3D portion of the brain in Bertsch et. al 2023. We will also use the three equations they derived to model the production, aggregation, and diffusion of six lengths of tau protein in a given region of neurons. We intend to use Python to program this model, and later JavaScript to visualize the results of our model in three dimensions. 


Given that these equations were created to model the progression of tau proteins specifically in individuals with Alzheimers, they have components specific to the A𝛽 protein, another protein associated with ND diseases that we are not interested in. We will be removing these components and adapting their equations accordingly, using constants if needed. Additionally, the graph space that the paper defines for the proximity and connectivity of brain regions is not cited, and likely also covers the entire brain. We will redefine our graph space to be a small homogenous space at first, and will later experiment with more realistic and complex graph spaces to represent specific brain regions. Finally, while Bertsch et. al 2023 accounts for spatial factors in its equations, its outputs focus only the concentration of tau in a given region, not its location. So, we will be adapting an equation from the Fisher-Kolmogorov model to apply the results of the previous equations to 3D space, allowing us to model the spread of tau proteins over time in our space (Schafer et. al 2021). 


Our first steps as a group will be understanding each component of the equation to its fullest extent, in order to build on our understanding and alter the equation as needed. 
We first hope to construct a basic model full of a homogenous brain region. This will attempt to model at its most simplistic level the spread of tangles of misfolded tau proteins through a cube of 8 brain packets starting from one corner. Once we have achieved this basic level of construction, we will increase the size of our homogeneous model space and add multiple source points for the spread of tau tangles to see how they interact upon collision. This procedure is meant to model the interaction and aggregation of tau spread in individuals with repeated head injuries, which can cause degenerative diseases like CTE.
Eventually, we will attempt to model different regions of the brain–for example, by creating layers with low connectivity amongst each other to model the visual cortex. We will then observe the dynamics of tau spread in these various regions.
The end goal of our project is to observe firstly how multiple brain injuries and their resulting tau protein spreads interact with and amplify one another, and secondly how the types of brain matter that tau proteins spread through affect their movement. 

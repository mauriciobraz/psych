## The physics of brain network structure, function, and control 

 Christopher W. Lynn^1 & Danielle S. Bassett^1 ,^2 ,^3 ,^4 ,^5 ,∗ 

(^1) Department of Physics & Astronomy, College of Arts & Sciences, University of Pennsylvania, Philadelphia, PA 19104, USA (^2) Department of Bioengineering, School of Engineering & Applied Science, University of Pennsylvania, Philadelphia, PA 19104, USA (^3) Department of Electrical & Systems Engineering, School of Engineering & Applied Science, University of Pennsylvania, Philadelphia, PA 19104, USA (^4) Department of Neurology, Perelman School of Medicine, University of Pennsylvania, Philadelphia, PA 19104, USA (^5) Department of Psychiatry, Perelman School of Medicine, University of Pennsylvania, Philadelphia, PA 19104, USA 

# arXiv:1809.06441v3 [q-bio.NC] 7 Jan 2019 


The brain is a complex organ characterized by heterogeneous patterns of structural connections supporting unparalleled feats of cognition and a wide range of behaviors. New noninvasive imaging techniques now allow these patterns to be carefully and comprehensively mapped in individual humans and animals. Yet, it remains a fundamental challenge to understand how the brain’s structural wiring supports cognitive processes, with major implications for the personalized treatment of mental health disorders. Here, we review recent efforts to meet this challenge that draw on intuitions, models, and theories from physics, spanning the domains of statistical mechanics, information theory, and dynamical systems and control. We begin by considering the organizing principles of brain network architecture instantiated in structural wiring under constraints of symmetry, spatial embedding, and energy minimization. We next consider models of brain network function that stipulate how neural activity propagates along these structural connections, producing the long-range interactions and collective dynamics that support a rich repertoire of system functions. Finally, we consider perturbative experiments and models for brain network control, which leverage the physics of signal transmission along structural wires to infer intrinsic control processes that support goal-directed behavior and to inform stimulation-based therapies for neurological disease and psychiatric disorders. Throughout, we highlight several open questions in the physics of brain network structure, function, and control that will require creative efforts from physicists willing to brave the complexities of living matter. 


It is our good fortune as physicists to seek to understand the nature of the observable world around us. In this inquiry, we need not reach to contemporary science to appreciate the fact that our perception of the world around us is inextricably linked to the world within us: the mind. Indeed, even Aristotle c. 350 B.C. noted that it is by mapping the structure of the world that the human comes to understand their own mind 1. “Mind thinks itself because it shares the nature of the object of thought; for it becomes an object of thought in coming into contact with and thinking its objects, so that mind and object of thought are the same” 2. Over the ensuing 2000-plus years, it has not completely escaped notice that the mappers of the world have unique contributions to offer the mapping of the mind (from Thales of Miletus, c. 624–546 B.C., to Leonardo Da Vinci, 1452–1519). More recently, it is notable that nearly all famous physicists of the early 20th^ century 

- Albert Einstein, Niels Bohr, Erwin Schroedinger, Werner Heisenberg, Max Born – considered the philosophical implications of their observations and theories 3. In the post-war era, philo- sophical musings turned to particularly conspicuous empirical contributions at the intersection of neuroscience and artificial intelligence, spanning polymath John von Neumann’s work enhancing our understanding of computational architectures 4 and physicist John Hopfield’s invention of the associative neural network, which revolutionized our understanding of collective computation 5. 

In the contemporary study of the mind and its fundamental organ – the brain – nearly all of the domains of physics, perhaps with the exception of relativity, are not only relevant but truly essential, motivating the early coinage of the term neurophysics some four decades ago 6. The fundamentals of electricity and magnetism prove critical for building theoretical models of neurons and the transmission of action potentials 7. These theories are being increasingly informed by mechanics to understand how force-generating and load-bearing proteins bend, curl, kink, buckle, constrict, and stretch to mediate neuronal signaling and plasticity 8. Principles from thermodynamics come into play when predicting how the brain samples the environment (action) or shifts the distribution of information that it encodes (perception) 9. Collectively, theories of brain function are either buttressed or dismantled by imaging, with common tools including magnetic resonance imaging 10 and magnetoencephalography 11 , the latter being built on superconducting quantum interference devices and next-generation quantum sensors that can be embedded into a system that 


can be worn like a helmet, revolutionizing our ability to measure brain function while allowing free and natural movement 12. Moreover, recent developments in nanoscale analysis tools and in the design and synthesis of nanomaterials have generated optical, electrical, and chemical methods to explore brain function by enabling simultaneous measurement and manipulation of the activity of thousands or even millions of neurons 13. Beyond its relevance for continued imaging advancements 14 , optics has come to the fore of neuroscience over the last decade with the development of optogenetics, an approach that uses light to alter neural processing at the level of single spikes and synaptic events, offering reliable, millisecond-timescale control of excitatory and inhibitory synaptic transmission 15. 

Such astounding advances, enabled by the intersection of physics and neuroscience, have motivated the construction of a National Brain Observatory at the Argonne National Laboratory (Director: Peter Littlewood, previously of Cavendish Laboratories) funded by the National Science Foundation, as well as frequent media coverage including titles in the APS News such as “Physicists, the Brain is Calling You.”^16 And as physicists answer the call, our understanding of the brain deepens and our ability to mark and measure its component parts expands. Yet alongside this growing systematization and archivation, we have begun to face an increasing realization that it is the interactions between hundreds or thousands of neurons that generate the mind’s functional states 13. Indeed, from interactions among neural components emerge computation 17 , communication 18 , and information propagation 19. We can confidently state of neuroscience what Henri Poincare, the French mathematician, theoretical physicist, and philosopher of science, states of science generally: “The aim of science is not things themselves, as the dogmatists in their simplicity imagine, but the relations among things; outside these relations there is no reality knowable.”^20 The overarching goal of mapping these interactions in neural systems has motivated multibillion-dollar investments across the United States (the Brain Initiative generally, and the Human Connectome Project specifically 21 ), the European Union (the Blue Brain Project 22 ), China (the China Brain Project 23 ), and Japan (Japan’s Brain/MINDS project 24 ). 

 While it is clear that interactions are paramount, exactly how the functions of the mind arise 


from these interactions remains one of the fundamental open questions of brain science 25. To the physicist, such a question appears to exist naturally within the purview of statistical mechanics 26 , with one major caveat: the interaction patterns observed in the brain are far from regular, such as those observed in crystalline structures, and are also far from random, such as those observed in fully disordered systems 27. Indeed, the observed heterogeneity of interaction patterns in neural systems – across a range of spatial and temporal scales – generally limits the utility of basic continuum models or mean-field theories, which would otherwise comprise our natural first approaches. Fortunately, similar observations of interaction heterogeneity have been made in other technological, social, and biological systems, leading to concerted efforts to develop a statistical mechanics of complex networks 28. The resultant area of inquiry includes criteria for building a network model of a complex system 29 , statistics to quantify the architecture of that network 30 , models to stipulate the dynamics that can occur both in and on a network 31–33, and theories of network function and control 34, 35. 

Here, we provide a brief review for the curious physicist, spanning the network-based approaches, statistics, models, and theories that have recently been used to understand the brain. Importantly, the interpretations that can be rationally drawn from all such efforts depend upon the nature of the network representation 29 , including its descriptive, explanatory, and predictive validity – topics that are treated with some philosophical rigor elsewhere 36. Following a simple primer on the nature of network models, we discuss the physics of brain network structure, beginning with an exposition regarding measurement before turning to an exposition regarding modeling. In a parallel line of discourse, we then discuss the physics of brain network function, followed by a description of perturbation experiments and brain network control. In each section we separate our remarks into the known and the unknown, the past and the future, the fact and the speculation. Our goal is to provide an accessible introduction to the field, and to inspire the younger generation of physicists to courageously tackle some of the most pressing open questions surrounding the inner workings of the mind. 


The physics of brain network structure 

We begin with a discussion of the architecture, or structural wiring, of networks in the brain, focusing on the measurement and modeling of their key organizational features (see Box 1 for a simple primer on networks). Each edge in a structural brain network represents a physical connection between two elements. For example, synapses support the propagation of information between neurons 37 and white matter tracts define physical pathways of communication between brain regions 38. In physics, it has long been recognized that the organization of such structural connections can determine the qualitative large-scale features of a system 28. In the Ising model, for instance, a one-dimensional lattice remains paramagnetic across all temperatures 39 , while in two dimensions or more, the system spontaneously breaks symmetry, yielding the type of bulk magnetization exhibited by magnets on a refrigerator 40, 41. Similarly, the organization of structural wiring in the brain largely determines the types of mental processes and cognitive functions that can be supported 42–46, from memory 47–49^ to learning 50, 51, and from vision 52 to motion 53. However, unlike many physics applications, which assume simple lattice or random network architectures, the wiring of the brain is highly heterogeneous, often making symmetry arguments and mean-field descriptions far from applicable 27. While this heterogeneity presents a unique set of challenges, in what follows we review some powerful experimental and theoretical tools that allow us to distill the brain’s structural complexity to a number of fundamental organizing principles. 

 [Box 1 here] 

Measuring brain network structure. Some of the earliest empirical measurements of the brain’s structural connectivity can be traced to Camillo Golgi, who in 1873 soaked blocks of brain tissue in silver-nitrate solution to provide among the first glimpses of the intricate branching of nerve cells 54. Soon after, Santiago Ram ́on y Cajal combined Golgi’s method with light microscopy to achieve stunning pictures establishing that neurons do not exist in solitude; they instead combine to form intricate networks of physical connections 55. This notion that the brain comprises a com


plex web of distinct components, known as the neuron doctrine 56 , established the foundation upon which modern network neuroscience has flourished. The introduction of the electron microscope in the 1930s provided even more detailed measurements of the physical connections between neurons. Perhaps the most impressive application remains the complete mapping of interconnections between the 302 neurons in the nematode C. elegans 57. Since this achievement, reconstructions of the synaptic connectivity in other animals have evolved rapidly, from a mapping of the optic medulla in the visual system of the fruit fly Drosophila to the enumeration of connections between 950 distinct neurons in the mouse retina 52, 58. Efforts continue to press forward toward the ultimate goal of reconstructing the neuronal wiring diagram of an entire human brain 59. 

Concurrently with these achievements using electron microscopy, complimentary efforts in tract tracing have revealed the mesoscale structure of the macaque 60, 61, cat 62 , mouse 63 , and fly 64. Particularly important for our understanding of human cognition are recent advances in noninvasive imaging that have allowed unprecedented views of the mesoscale structure of the brain in vivo. Introduced in the 1970s, computerized axial tomography (CAT) provided among the most detailed anatomic images of the human brain to date 65. Soon after, the development of magnetic resonance imagining (MRI) sparked an explosion of refinements, a notable example being diffusion tensor imaging (DTI) 66. While standard CAT and MRI techniques capture crosssectional images of the brain, DTI traces the diffusion of water molecules through white matter tracts to reconstruct the large-scale neural pathways connecting distinct brain regions 67, 68. Given measurements of the anatomical wiring connecting a set of neural elements, such as synapses linking neurons or white matter tracts connecting brain regions, researchers can build a structural brain network by forming edges between elements that share a physical connection (Fig. 1a). Ongoing experimental efforts to acquire these measurements continue to provide rich network datasets detailing the brain’s structural organization. 

Modeling brain network structure. A first glance at the brain’s wiring reveals that it is far from homogeneous – a fact that is not surprising considering the array of physical, energetic, and cognitive constraints that it is required to balance 69. To handle this heterogeneity, researchers have 


 Community structure 

 Stochastic block 

 (efficient communication)^ Small-world 

 Watts—Strogatz 

 (heavy-tailed deg. dist.)^ Hub structure 

 Barabási—Albert 

 a Measurement 

Example: White matter tracts (via DTI) (^) Adjacency matrix Structural brain network Network type **b Modeling** Generative model (no structure)^ Random Erdös—Rényi Spatially embedded Spatial model Figure 1 | **Measuring and modeling brain network structure. a** | The measurement of brain network structure begins with experimental data specifying the physical interconnections between neurons or brain regions. As an example, we consider a dataset of white matter tracts measured via DTI. First, the data is discretized into non-overlapping gray matter volumes representing distinct nodes. Then, one constructs an adjacency matrix A, where Aij represents the connection strength between nodes i and j. This adjacency matrix, in turn, defines a structural brain network constructed from our original measurements of physical connectivity. **b** | To capture an architectural feature of structural brain networks, we utilize generative network models. The simplest generative network model is the Erd ̈os–R ́enyi model, which has no discernible non-random structure. Networks with modular structure, divided into communities with dense connectivity, are constructed using the stochastic block model. Small-world networks, which balance efficient communication and high clustering, are generated using the Watts–Strogatz model. Networks with hub structure, characterized by a heavy-tailed degree distribution, are typically constructed using a preferential attachment model such as the Barab ́asi–Albert model. Spatially embedded networks, whose connectivity is constrained to exist within a physical volume, are generated through the use of spatial network models. | 


increasingly turned to the field of network science for mathematical tools and intuitions 70, 71. The primary goal of this interdisciplinary effort has been to distill the explosion of experimental data, spanning structural brain networks in C. elegans 72 , the mouse 73 , cat 74 , macaque 75, 76, and human 

(^77) , down to a number of cogent organizing principles. Here we review some important properties that are thought to characterize structural brain networks and introduce several generative network models that help to explain how these properties arise from underlying biological mechanisms (Fig. 1b). Random structure. While healthy members of a species exhibit anatomical similarities in brain structure, the specific instantiation of physical connections in each individual is far from deterministic. Indeed, in vivo imaging techniques in humans, such as DTI described above, have revealed not only stark differences in brain structure between individuals 78 , but also within the same individual over time 79, 80. Importantly, these structural differences have been linked to variability in a wide range of behaviors 81 , including empathy 82 , introspection 83 , fear acquisition 84 , and even political orientation 85. To study the mathematical properties of random networks, and to understand the types of biological mechanisms that can give rise to qualitative structural properties, it is useful to consider generative network models 70. The simplest and most common model for generating random networks is the Erd ̈os–R ́enyi (ER) model 86 , wherein each pair of nodes is connected independently with a fixed probability P. While the ER model has a number of interesting mathematical properties, such as a binomial degree distribution, it has no discernible structure and does not reflect the mechanisms by which most networks grow in the brain. Accordingly, if we wish to understand some of the principles underlying naturally occurring brain networks, we must consider generative models that yield networks with realistic properties. Community structure. Perhaps the brain’s most well-studied structural property is its division into distinct anatomical regions, which are widely thought to be responsible for specialized cognitive functions 87. Interestingly, by studying the large-scale structure of brain networks in several mammalian species, researchers have shown that the organization of connections tends to partition the networks into densely-connected communities separated by sparse inter-community connectivity 


88–91. Moreover, these clusters of high connectivity closely resemble postulated anatomical subdi

visions 89. It has therefore been argued that the so-called community structure of brain networks segregates the brain into subnetworks with specific cognitive functions 92–96. Practically speaking, in order to extract the community structure of a real-world network, one must employ algorithms for community detection – a vibrant branch of research that is now applied throughout network neuroscience 97, 98. From a complimentary perspective, to generate networks with a defined community structure, researchers predominantly use the stochastic block (SB) model, wherein nodes are assigned to distinct communities and an edge is placed between each pair of nodes with a probability that depends on the nodes’ community assignments 99, 100. Such SB networks are often used as null models to distinguish between properties of brain networks that are implied simply by their community structure and those that require additional biological mechanisms 70, 100. 

Small-world structure. Seemingly in contradiction to their striking community structure, largescale brain networks also exhibit average path lengths between all nodes that are much shorter than a typical random network 69, 101, 102. This competition between high clustering and short average paths is thought to facilitate the simultaneous segregation and integration of information in the brain 103 , possibly minimizing the total number of computational steps needed to process external stimuli 104, 105. Seeking an explanation for similar “small-world” topologies exhibited by other realworld systems (most notably social networks 106 ), Duncan Watts and Steven Strogatz developed a model for generating random networks with both high clustering and short average path lengths 107. Generally, the Watts-Strogatz (WS) model supposes that small-world networks are an interpolation between two extreme configurations: a ring lattice, wherein nodes are arranged along a circle and connected to their k nearest neighbors on either side, and an ER random network. Notably, the presence of small-world structure in the brain suggests that efficient communication emerges from a finely-tuned balance of lattice-like organization and structural disorder. 

Hub structure. In addition to their modular and small-world structure, many large-scale brain networks also feature high-degree “hubs”, which form a densely interconnected structural core 108. Acting as bridges between structurally distinct communities, these specialized hub regions are 


thought to help minimize overall path lengths across the network 90 and facilitate the integration of information 103. Supporting the notion of a centralized core, many studies have identified hubs within the parietal and prefrontal regions, areas that are often active during a wide range of cognitive functions 108, 109. Such core-periphery architecture is characterized by a heavy-tailed degree distribution, such as that observed in scale-free networks, in some cases arising through preferential attachment mechanisms 110. In the Barab`asi–Albert (BA) model 111 , for instance, nodes are added to a network in sequential order, and each new node i forms an edge with each existing node j with a probability proportional to the degree of node j. In this way, new nodes preferentially attach to existing nodes of high degree, creating a “rich club” of centralized hubs that link otherwise distant regions of the network. 

Spatial structure. Thus far, we have focused exclusively on the topological properties of brain networks, which are thought to be driven primarily by the simultaneous functional pressures of information segregation and integration 103. However, brain networks are also physically constrained to exist within a tight three-dimensional volume and their structural connections are metabolically driven to minimize total wiring distance 69, 92, 105. Such physical and metabolic constraints are captured by spatial (or geometric) network models, which embed networks into three-dimensional Euclidean space and penalize the formation of long-distance connections 70. The simplest such model assumes that the probability of two nodes i and j forming an edge is proportional to d−ijα , where dij is the physical distance between i and j, and α ≥ 0 tunes the metabolic cost associated with constructing connections of a given length 112. If we keep the number of nodes and edges fixed, one can see that, much like the WS model, this spatial model interpolates between a latticelike structure, in which nodes only connect to their nearest neighbors (α → ∞), and an ER random network (α = 0). 

Competition between structural properties. As the brain grows and adapts to changing cognitive demands, it is widely thought that the underlying network evolves to balance the trade-off between topological value and metabolic wiring cost 69. Thus, while the modular, small-world, heavytailed, and inherently physical properties of brain networks provide simple organizing principles, 


in reality the brain is constantly and dynamically weighing these pressures against one another. Accordingly, an accurate generative model should aim to explain multiple real-world properties at once 70. With this goal in mind, recent work has shown that an impressive range of topological properties can be understood as arising from a competition between two competing factors: a metabolic penalty for the formation of long-distance connections and a topological incentive to connect regions with similar inputs 113. Notably, investigations of the human, C. elegans, and mouse connectomes have revealed that the total wiring distance is consistently greater than minimal, supporting the notion that brain networks weigh the costs of long-distance connections against the functional benefits of an integrated network topology 92, 114. Together, these efforts toward a comprehensive generative model are vital for our understanding of healthy brain network structure, with important clinical implications for the diagnosis, prognosis, prevention, and treatment of disorders of mental health 115, 116. 

The future of brain network structure. Current advances in neuroimaging techniques and network science continue to expand our ability to measure and model the architecture of structural connections in the brain. As experimental measurements become increasingly detailed, an important direction is the bridging of brain network structure at different spatiotemporal scales 117–119. Such cross-scale approaches could link protein interaction networks within neurons to the wiring of synaptic connectivity between neurons to mesoscale networks connecting brain regions and all the way to social networks linking distinct organisms (Box 2). The goal of such cross-scale integration is to understand how the architecture of connectivity at each of these scales emerges from the scale below. Practically, researchers have begun to address this goal by employing hierarchical network models 120 , which treat each node at the macroscale as an entire subnetwork at the microscale 121. 

 [Box 2 here] 

Perhaps the most ambitious future goal is the reconstruction of the entire human connectome at the scale of individual neurons, pressing the current boundaries of 3D electron microscopy 


and statistical image reconstruction 59. Extensive mapping efforts in other species have revealed notable and quantifiable neuronal diversity 122, 123, suggesting the importance of extending network models to include non-identical units. At the mesoscale, advances in noninvasive imaging have allowed researchers to begin tracking changes in structural connectivity over time 72, 124–126. To analyze these temporally ordered measurements, network scientists have extended standard static graph theoretic tools to study networks with dynamically evolving connections 98. Notably, these so-called temporal networks 127 were recently shown to be easier to control, requiring less energy to attain a desired pattern of neural activity, than their static counterparts 128. 

Properly modeling the dynamics of brain networks requires also understanding the functional dynamics occurring on brain networks. For instance, dating to Donald Hebb’s 1949 book The Organization of Behavior, it has been posited that the strength of a synaptic connection increases with the persistent synchronized firing of its preand postsynaptic neurons 129. Such Hebbian plasticity has been observed in vitro 130 and is thought to explain many aspects of brain network structure 131, 132. More generally, Hebb’s postulate highlights the fact that a complete understanding of the brain cannot simply include a description of its structural wiring; it must also stipulate the types of dynamics supported by this physical circuitry. 

The physics of brain network function 

While structural brain networks represent the physical wiring between neural elements (e.g., between individual neurons or brain regions), knowledge of this circuitry alone is not sufficient to understand how the brain works. For this reason, we turn our attention to models of brain network function that stipulate how neural activity propagates along structural connections. Just as the neuron doctrine postulates that the brain’s structure is divided into a network of distinct nerve cells, it is also widely expected that the brain’s array of cognitive functions emerges from the collective activity of individual neurons 13, 18, 25, 133, 134. To understand how the firing of simple nerve cells can give rise to the brain’s rich repertoire of cognitive functions 135 , analogies are often drawn with notions of emergence in statistical mechanics 25, 133, 136. Developed concurrently with the neu


ron doctrine in the late 19th^ century, statistical mechanics established (among other achievements) that the thermodynamic laws governing the macroscopic behavior of gas molecules can be derived from the microscopic dynamics of the molecules themselves 137. Similarly, growing evidence suggests that the dynamics of individual neurons and brain regions, when embedded in networks of structural connections, can produce the types of long-range correlations and collective patterns of activity that we observe in the brain 133, 138–143. Here we traverse what is known about brain network function in relatively broad strokes, from the dynamics of distinct neurons to the networked activity of the entire brain. 

Measuring brain network function. The first measurements of the brain’s functional organization date to 1815, when Marie-Jean-Pierre Flourens pioneered the use of localized lesions in the brains of living animals to observe their effects on behavior. Through his experiments, Flourens discovered that the cerebellum regulates motor control, the cerebral cortex supports higher cognition, and the brain stem controls vital functions 144. The remainder of the 19th^ century brought increasingly detailed measurements of the brain’s functional organization, from the demonstration that the occipital lobe regulates vision 145 to the discovery that the left frontal lobe is essential for speech 146. These discoveries, combined with the early images of neural circuits captured by Ram ́on y Cajal 55 , culminated in Thomas Scott Sherrington’s book The Integrative Action of the Nervous System, which proposed the idea that neurons behave in functional groups 87. 

Meanwhile, in 1849 the physicist Hermann von Helmholtz achieved the first electrical measurements of a nerve impulse 147 , sparking a wave of experiments investigating the electrical properties of the nervous system. Through invasive measurements in animals using newly-developed electroencephalography (EEG) techniques 148 , it quickly became clear that individual neurons communicate with one another via electrical signals 149–151, thus providing a clear mechanism explaining how information is propagated and manipulated in the brain. Today, scientists possess a rich menu of experimental techniques for measuring brain dynamics across a range of scales. At the neuronal level, the development of invasive methods in animals, such as electrophysiological recordings of brain slice preparations in vitro 152, 153^ and calcium imaging of neuronal activity in 


vivo 154, 155, have vastly expanded our understanding of synaptic communication. At the regional level, complimentary minimally-invasive imaging techniques have identified fundamental properties of information processing in humans 156. Interestingly, these advances in mesoscale functional imaging can largely be traced to the efforts of physicists. MEG methods, for instance, use superconducting quantum interference devices (SQUIDS) to directly measure the magnetic fields generated by electrical currents in the brain 12, 157; and PET techniques measure the positron emission of radioisotopes produced in cyclotrons to reconstruct the metabolic activity of neural tissue 158. Over the last twenty years, measurements of brain dynamics have been increasingly dominated by functional MRI (fMRI) 159 , which estimates neural activity by calculating contrasts in blood oxygen levels, without relying on the invasive injections and radiation that limit the applicability of other imaging techniques 160. This modern progress in functional brain imaging has galvanized the field of network neuroscience by making detailed datasets of large-scale neural activity widely accessible. 

One particularly important application of functional brain imaging has been the study of so-called functional brain networks 161 , which have allowed researchers to investigate the organization of neural activity using tools from network science. In functional brain networks, as in their structural counterparts, nodes represent physical neural elements, ranging in size from individual neurons to distinct brain regions 162. However, whereas structural brain networks define the connectivity between elements based on physical measures of neural wiring (e.g., synapses between neurons or white matter tracts between brain regions), functional brain networks define connectivity based on the similarity between two elements’ dynamics 162. To see how this works, we briefly consider the common example of a large-scale functional brain network calculated from fMRI measurements of regional activity 161 (Fig. 2a). First, blood oxygen levels indirectly reflecting neural activity are measured within three-dimensional non-overlapping voxels, spatially contiguous collections of which each represent a distinct brain region. After preprocessing the signal to correct for sources of systematic noise such as fluctuations in heart rate, the activity of each brain region is discretized in time, yielding a vector (or time series) of neural activity. Finally, to quantify functional connectivity, one computes the similarity between each pair of brain 


regions, for example using the quite simple Pearson correlation between the two regions’ activity time series 138, 163. The end result, even for different types of functional data and different choices for the preprocessing steps and similarity metric, is a functional brain network representing the organization of neural activity. 

After constructing a functional brain network, researchers can utilize techniques from network science to study its key organizing features. Such efforts have demonstrated that large-scale functional brain networks, much like structural networks, exhibit signs of modular, small-world, heavy-tailed, and metabolically constrained organization 161, 164–167. The existence of strong functional community structure, for instance, further supports the hypothesis that brain networks segregate into subnetworks with specialized cognitive functions 168, 169. Moreover, the presence of high clustering and short average path lengths, combined with the existence of high-degree hub regions, highlights the competing functional pressures of information segregation and integration in the brain 166, 170. Metabolic constraints on the brain’s structural wiring are also evident in its functional connectivity 171 , with spatially localized brain regions generally supporting more strongly correlated activity than distant regions 69. In light of the similarities between the brain’s functional and structural organization, it is tempting to suspect that functional brain networks closely resemble the physical wiring upon which they exist 172, 173. However, the relationship between brain function and structure is highly nonlinear 174 , and understanding how a functional brain network arises from its underlying structural connectivity remains a subject of intense academic focus 119, 175. 

Modeling brain network function. To understand how the web of physical connections in the brain gives rise to its functional properties, statistical mechanical intuition dictates that we should begin by studying the dynamics of individual elements. Once we have settled on accurate models of the interactions between individual neurons and brain regions, we can link these elements together in a network to predict macroscopic features of the brain’s function from its underlying structure 36, 71. Interestingly, the history of modeling in neuroscience has followed precisely this path, beginning with models of neuronal dynamics 17, 176, 177, then increasing in scale to mean-field neural mass models of distinct brain regions 178, 179, and eventually achieving models of entire 


 b Modeling 

 Similarity matrix Functional brain network 

 a Measurement 

 Example: Blood oxygen level (via fMRI) 

 Activity 

 Biophysical dynamics 

 e.g. Wilson—Cowan 

 Fine-scale 

 e.g. Hodgkin—Huxley, FitzHugh—Nagumo 

 Mesoscale inputs 

 e.g. McCulloch—Pitts “dog” e.g. image classifier 

 Artificial neural net 

 output 

 inputs 

 threshold 

 Artificial neuron 

 Artificial dynamics 

 output 

 Large-scale 

 neuron 

 neuronal network 

neural mass (^) regional network Figure 2 | **Measuring and modeling brain network function. a** | The measurement of brain network function begins with experimental data specifying the activity of neurons or brain regions. As an example, we consider variations in blood oxygen level in different parts of the brain measured via fMRI. Calculating the similarity (e.g., correlation or synchronization) between pairs of activity time series, one arrives at a similarity matrix. This matrix, in turn, defines a functional brain network constructed from our original measurements of neural activity. **b** | We divide models of neural activity into two classes: abstract models with artificial dynamics (left) and biophysical models with realistic dynamics (right). Models of artificial neurons, such as the MP neuron, typically take in a weighted combination of inputs and pass the inputs through a nonlinear threshold function to generate an output. Networks of artificial neurons, from deep neural networks to Hopfield networks, have been shown to reproduce key aspects of human information processing, such as learning from examples and storing memories. By contrast, biophysical models of individual neurons, such as the Hodgkin–Huxley or FitHugh– Nagumo models, capture realistic functional features such as the propagation of the nerve impulse. When interconnected with artificial synapses, researchers are able to simulate entire neuronal networks. Complimentary mesoscale approaches, including neural mass models such as the Wilson–Cowan model, average over all neurons in a population to derive a mean firing rate. To simulate the large-scale activity of an entire brain, researchers use neural mass models to represent brain regions and embed them into a network with connectivity derived from measurements of neural tracts (e.g., as measured via DTI). | 


networks of neurons and brain regions 5, 141, 180. Here we review important developments in the modeling of neural dynamics, dividing the modeling techniques into two complimentary classes: those with artificial dynamics and those with biophysically realistic dynamics (Fig. 2b). As we will see, models from each of these two classes are able to reproduce important aspects of neural activity and system function that have been observed in a range of physiological and behavioral experiments. 

Artificial models. One of the earliest mathematical models of neural activity whatsoever was proposed in the mid-1940s by Warren McCulloch and Walter Pitts to describe the logical functioning of an individual neuron 17. Known as the MP neuron, their model accepted binary inputs, combined these inputs using linear weights, and produced a binary output reflecting whether or not the weighted sum of inputs exceeded a given threshold (Fig. 2b). Albeit a simple caricature of neuronal dynamics, this model has been shown to reproduce some important qualitative features of neuronal activity, including the linear summation of excitatory inputs 181 and the “all-or-none” response to the resulting integrated signal 182. Moreover, by connecting the inputs and outputs of multiple MP neurons, researchers have achieved deep insights about how brain networks perform basic cognitive functions. For example, soon after the introduction of the MP model, researchers demonstrated that networks of artificial neurons could be used to represent any Boolean function (i.e., any function mapping a list of binary variables to a binary output), thereby establishing the basic capability of neural networks to perform logical computations 6. 

While their ability to perform basic computations was quickly realized, it was not clear at the outset whether artificial neural networks could reproduce other cognitive functions, such as the ability to learn or store memories. The former was established by Frank Rosenblatt in 1957, when he showed that the weights on the inputs to an MP neuron could be tuned such that the output defines a binary classifier. Known as the perceptron, this algorithm enabled a single MP neuron to segregate incoming data into one of two classes by learning from past examples. This remarkable result directly inspired more advanced learning algorithms, including support vector machines 183 and artificial neural networks 184 , effectively setting in motion the study of machine 


learning. Today, deep neural networks, consisting of multiple layers of artificial neurons feeding in one direction from the input layer to the output layer (Fig. 2b), are able to learn a wide range of impressive cognitive functions that we have come to expect from the brain 185. While the list of applications is ever-expanding, deep neural networks have been used to process and identify images of objects, scenes, and people 186 ; recognize, interpret, and respond to spoken language 187 ; and formulate strategies and make decisions in adversarial settings 188. 

In addition to performing computations and learning from examples, the physicist John Hopfield showed in 1982 that neural networks can also store and recall memories. Specifically, Hopfield demonstrated that the synaptic weights connecting a set of MP neurons could be adjusted in a Hebbian fashion such that the network is able to “memorize” a number of desired activity states 5 (i.e., configurations of the network in which each neuron is either active or inactive). Notably, the number of memorized states grows linearly with the number of neurons in the network 

(^189) , and errors in recall often yield states that are semantically similar to the target state, a phenomenon commonly observed in humans 190. Interestingly, the memorized activity states can be interpreted as local minima of an associated energy function, making each Hopfield network equivalent to an Ising model at zero temperature 41. More recently, Ising-like models have also been used to explain the critical or avalanche-like behavior of activity in neural ensembles 191 , which is thought to support adaptation to environmental changes 192 , information storage 193 , optimal information transmission 194 , maximal dynamic range 195, 196, and computational power 197. Further building upon this connection to statistical mechanics, scientists have recently used maximum entropy techniques to construct data-based models of neuronal dynamics. These maximum entropy models, which are equivalent to networks of Ising spins with specially-chosen external fields and interaction strengths, have been shown to predict the observed long-range correlations within naturally occurring networks of neurons and brain regions 141, 198. Together, artificial models of neural dynamics, from simple MP neurons to artificial neural networks and data-driven maximum entropy models, continue to inform our understanding of brain networks as information processing systems. 


Biophysical models. While artificial models continue to generate insights about the nature of neural computation, they only vaguely resemble the complex biophysical mechanisms that guide observable neural activity. Among the first biophysically realistic models of the electrical behavior of an individual neuron was achieved nearly a decade after the introduction of the MP neuron by physiologists Alan Lloyd Hodgkin and Andrew Fielding Huxley 176. Beginning from a principled description of the initiation and propagation of action potentials in living neurons, the Hodgkin– Huxley (HH) model explains important qualitative aspects of neuronal behavior 6 , including the spontaneous emergence of limit cycles or oscillations in activity 199 and the presence of a Hopf bifurcation in the neuronal firing rate, which is thought to underlie the all-or-none principle 176 (Fig. 2c). Subsequent extensions of the HH model expand biophysical realism by incorporating multiple ion channel populations 200 , the complex geometries of dendrites and axons 201 , and more realistic stochastic dynamics yielding thermodynamic and hybrid HH models 202, 203. Concurrent with these descriptive improvements, several simplified neuronal models were also developed, including the notable FitzHugh–Nagumo model 177, 204, facilitating efficient large-scale simulations of groups of neurons. 

Simplifications in neuronal modeling, paired with fine-scale measurements of the synaptic wiring in several animals, have spurred large-scale simulations of real neuronal circuits (Fig. 2b). For example, on the heels of mapping the entire C. elegans connectome 57 , researchers began simulating the 302-neuron network at the cellular level 205 , eventually even including the nematode’s entire muscular system and representations of its physical environment 206. Despite these and other efforts simulating the Drosophila brain 207 and the rat’s neocortical column 208 , it remains unclear how networks of neurons combine to generate the complex range of behaviors observed even in these relatively simple organisms. This contrast between the simplicity of neuronal dynamics and the apparent complexity of large-scale neural behavior hints at the crucial role of emergence. To understand how macroscopic behaviors emerge within groups of neurons, researchers began developing mean-field descriptions of large neuronal populations. Known as neural mass models, these efforts culminated in the foundational Wilson–Cowan (WC) model of population dynamics 179. Whereas previous neural mass models only considered excitatory interactions between neurons, 


Wilson and Cowan also included inhibitory interactions, thereby enabling the WS model to predict the collective neural oscillations observed in experiments as well as the emergence of other key properties of neural behavior, including the existence of multiple stable states and hysteresis in the neural response to stimuli 179. This progress was further extended to include spatial fluctuations in activity, yielding neural field models that exhibit other behaviors typically observed in the brain, including regions of localized activity 209 and traveling waves 210. 

In much the same way that neuronal circuits have been modeled using observable synaptic wiring in animals, one could imagine simulating a network of neural mass models whose connections are drawn based on non-invasive measures of regional connectivity in humans. By doing so, researchers are now able to simulate whole sections of the human brain (Fig. 2c), opening the door for comparisons with experimental measurements of regional activity. Precisely this approach has driven a deeper understanding of the structure-function relationship, including the demonstration that the broad spectrum of MEG/EEG recordings of electrical activity can be reproduced by networked models of neural masses 211 and that the functional connectivity within such recordings depends critically on the coupling strength between neural masses 212. To facilitate large-scale simulations of the entire human brain, researchers have frequently turned to the Kuramoto model of oscillatory dynamics as a simplified neural mass model 180, 213. These efforts have provided insights about the spontaneous synchronization of neural oscillations 214 , a phenomenon which is thought to play a critical role in neural communication 215 , information processing 216 , and motor coordination 217. Moreover, by embedding Kuramoto oscillators into a realistic map of the human connectome, researchers have shown that even this simple model is able to reproduce the patterned fluctuations in activity and long-range correlations observed in fMRI data 218. Detailed biophysical models of neural dynamics, from descriptions of the electrical activity of individual neurons to networked neural mass models simulating the entire brain, continue to inform our understanding of how collective neural behavior and high-level cognitive functions arise from the brain’s underlying physical circuitry. 

The future of brain network function. Over the last two centuries, our understanding of the 


brain’s functional organization and information processing capabilities has progressed immensely. Despite this progress, the modern neuroscientist remains fundamentally limited by the experimental and theoretical tools at their disposal 219, 220. Invasive techniques such as intracranial electrocorticography, and even minimally invasive techniques such as stereotactic electroencephalography (sEEG) 221–223, provide immense precision in mapping human brain dynamics, but remain constrained to patients with medically refractory epilepsy. Other noninvasive imaging techniques all suffer from trade-offs between spatial and temporal resolution 224 ; methods that directly measure electromagnetic signals (e.g., EEG and MEG) have high temporal resolution but low spatial resolution, while measurements of blood flow and metabolic activity (e.g., via fMRI or PET) have relatively high spatial accuracy but poor resolution in time. Even fMRI – widely considered the standard for high spatial resolution in humans – integrates signals over hundreds of thousands of neurons and several seconds 225. Consequently, any changes in neural activity that occur over tens of thousands of neurons or even over the span of a second are imperceivable on a standard fMRI scan. 

To improve the precision of functional neuroimaging (fMRI in particular), recent efforts have leveraged modern advances in image processing to strengthen the signal and reduce background noise. For example, to minimize the inevitable effects of head movements and fluctuations in blood flow during scanning, fMRI signals are increasingly corrected using techniques similar to image stabilization in video cameras 226. Additionally, in order to draw general conclusions from neuroimaging results across a group of subjects, impressive strides have been made to correct for inter-subject heterogeneities in brain structure 227. Together, advances in image processing have begun to push neuroimaging from a tool exclusively used for academic research to one that can aid in the diagnosis and treatment of psychiatric disorders such as schizophrenia and Alzheimer’s disease. 

Beyond data collection, data analysis and models in network neuroscience have historically been limited to dyadic relationships between neural elements, such as synapses connecting pairs of neurons or Pearson correlations between pairs of brain regions 36, 71. While these dyadic notions 


of connectivity have provided important insights about the brain’s circuitry, mounting evidence suggests that higher-order interactions between three or more elements are also crucial for understanding the large-scale behavior of entire brain networks 198, 228, 229. In order to study these higherorder connections, recent efforts have focused on generalizing traditional definitions and intuitions from network science, primarily by adopting methods from algebraic topology 230. One notable approach, known as persistent homology, has allowed researchers to extrapolate conclusions about neural activity across scales, escape the problem of selecting appropriate thresholds for functional edge strengths 231 , and extract principled mesoscale features of network organization 229, 232. 

Efforts have also been made to expand traditional metrics of functional connectivity, which are typically based on correlation, to include more sophisticated notions of causality 167. Since causality reflects the flow of information in a network from one element to another, efforts which aim to uncover causal relationships between neurons and brain regions have naturally drawn inspiration from concepts in information theory (see Box 3) 233. From mutual information to transfer entropy, information theoretic notions of functional connectivity are increasingly being used to quantify the flow of information in the brain 216, 234, 235. These measures of causality, in turn, have real-world implications for controlling brain networks and intervening to treat neurological disease and psychiatric disorders. 

 [Box 3 here] 

Perturbation experiments and the physics of brain network control 

Thus far, we have examined what is known about the structural circuitry connecting neural components in the brain as well as the dynamical laws governing the interactions between these components. An ultimate test of our understanding, however, lies in our ability to intervene and shift the brain’s dynamics to facilitate desirable behaviors. An important implication of the brain’s networked structure is that localized perturbations (e.g., targeted lesions or stimulation) do not just 


yield localized effects – they also induce indirect effects that propagate along neural pathways 236, 237. In this way, the task of controlling brain dynamics requires knowledge of how signals 

transmit along the brain’s structural wires, making the problem inherently one of network control 

(^238). Building upon targeted lesioning experiments in animals and clinical interventions in humans, efforts toward a theory of network control in the brain have recently taken shape, inspiring several fundamental questions 239. Are brain networks designed to facilitate control 240? What are the principles that allow brain networks to control themselves toward desired activity states 241, 242? Can we leverage these principles to inform stimulation-based therapies for neurological diseases and psychiatric disorders 243–246? To address these questions, here we review the current frontiers in the physics of brain network control. Targeted perturbations and clinical interventions. The first attempts to systematically control brain dynamics date to the early 19th^ century, when Marie-Jean-Pierre Flourens noticed that targeted lesions to the brain in living rabbits and pigeons yielded specific changes in the animals’ perception, motor coordination, and behavior 144. These efforts, in conjunction with other targeted lesioning experiments in animals 145, 146, supported the notion of functional localization – the theory that specific cognitive functions are supported by specific parts of the brain. In humans, evidence for functional localization has typically relied on patients with localized brain damage (e.g., due to a stroke or head trauma). Historical studies of this kind have revealed, for instance, that damage to one half of the occipital lobe often induces blindness in the opposite field of vision (^247) and that lesions in the frontal lobe can result in memory loss and an increase in impulsivity and risk taking 248. More recently, advances in non-invasive stimulation techniques such as transcranial magnetic stimulation (TMS) 249 , which induces “transient” lesions by disrupting the brain’s normal electrical activity, have opened the door for the control of localized brain functions, including perception 250 , learning 251 , language processing 252 , and attention 253. These non-invasive transcranial techniques have been supplemented by more invasive deep brain stimulation (DBS) methods to provide targeted therapies for a number of psychiatric and neurological disorders 249, 254. By focusing electromagnetic stimulation on the brain regions associated with specific disorders, both TMS and DBS have been used to treat Parkinson’s disease, epilepsy, depression, and schizophre


nia, among other disorders that are resistant to traditional therapies 255, 256^ (Fig. 3a). Despite these therapeutic benefits, it remains unclear exactly how and why TMS and DBS are so effective 236, 254; however, recent evidence suggests that the answers may rely on a deeper understanding of the indirect effects of stimulation that are mediated by the brain’s physical circuitry 257, 258. 

With the recent development of whole-brain neuroimaging methods such as fMRI, evidence continues to mount that brain regions are heavily interdependent on one another, often working in unison to process information and formulate responses 103, 161. In a particularly clear demonstration of the brain’s functional integration, Anthony Randall McIntosh and colleagues trained human subjects to associate an auditory stimulus with a visual event. Later, when the auditory stimulus was presented alone, the investigators observed increased activity in the occipital lobe, more traditionally thought of as being reserved for visual processing 259. Experiments such as these reveal how activity or stimulation in one part of the brain can propagate along neural pathways to induce activity in other distant parts. To understand the system-wide impacts of targeted stimulation, researchers have increasingly drawn upon network models of brain dynamics 257, 258. These efforts have resulted in the identification of neural circuits, rather than isolated regions, that are critical for reducing the symptoms of Parkinson’s disease 258, 260. Similar network-based approaches are also being used to suppress epileptic seizures using DBS 261 , non-invasively treat depression using TMS 262 , and modulate consciousness during surgery using anesthesia 263. Moreover, by stimulating and recording neural activity in several brain regions simultaneously, researchers have achieved closed-loop strategies for dynamically updating targeted treatments 264, 265^ (Fig. 3a). Meanwhile, clinical applications are increasingly being informed by detailed computational simulations of perturbations to specific brain regions, typically employing networked biophysical models such as those discussed in the previous section 266, 267. Together, these real-world and computational studies of targeted stimulation have opened the door for sophisticated strategies that aim to shift neural activity with the ultimate goal of guiding healthy cognitive function. 

Network control in the brain. To inform strategies for targeted stimulation and brain network control, it helps to draw upon existing tools from control theory in mathematics and intuitions from 


**a Targeted stimulation b Cognitive control** 

 e.g. deep brain stimulation 

 electrode 

 e.g. targeted treatment for Parkinson’s disease Default mode Frontoparietal Cingulo-opercular^ Ventral attention 

 Auditory Dorsal attention Somatosensory VisualOther 

 1% 3%2% 11% 

 30% 18% 

 4% 

 19% 

 12% 16% 3% 17% 18% 1% 15% 

 12% 

 7% 

controllability^ Average (^) controllabilityModal 11% closed-loop control Figure 3 | **Targeted perturbations and brain network control. a** | Methods for targeted control are used in the study, design, and optimization of external control processes, such as transcranial magnetic stimulation and deep brain stimulation. These targeted perturbations of neural activity are being utilized in clinical settings to treat major depression, epilepsy, and Parkinson’s disease. By simultaneously stimulating and measuring neural activity, researchers can now perform closed-loop control, continuously updating stimulation strategies in real time. **b** | Controllability metrics provide summary statistics regarding the ease with which a given node can enact influence on the network. Two common metrics are the average controllability, which assesses the ease of moving the system to all nearby states, and the modal controllability, which assesses the ability to move the system to distant states (see Box 4). Notions of controllability have proven useful in the study of the brain’s internal control processes, such as homeostatic regulation and cognitive control. For example, the human brain displays marked levels of both average and modal controllability, and the proportion of average and modal controllers differs across cognitive systems, suggesting the capacity for a diverse repertoire of dynamics 241. | 


cognitive control in psychology. Given a mathematical model of a system, control theory seeks to understand how the system can be influenced such that it moves toward a desired state 238, 268^ (see Box 4). Cognitive control, on the other hand, encompasses a broad class of processes by which the brain enacts control over itself, typically to achieve an abstract goal or desired response 269. For example, dating to the early 1970s neurophysiological studies revealed that the act of holding an object in working memory induces a sustained neural response in the prefrontal cortex 270, 271. In fact, the prefrontal cortex is now believed to play a key role in many cognitive control processes, from the representation of complex goal-directed behaviors 272 to the support of flexible responses to changes in the environment 273. But how do these notions of cognitive control (as defined by psychologists and cognitive neuroscientists) compare to theories of network control (as defined by physicists and engineers)? Furthermore, how can knowledge of the brain’s intrinsic control processes inform targeted therapies for mental illness? 

 [Box 4 here] 

To address these questions, we begin by comparing cognitive notions of intrinsic control with theoretical measures of control and controllability in brain networks (see Box 4). It is interesting, for example, to ask which brain regions are most capable of inducing desired neural responses in other brain regions that are responsible for common functions such as vision, audition, and motor coordination. Toward this end, Gu et al. used methods from control theory to demonstrate that the strongest driver nodes corresponded to brain regions with high communicability – or many topological paths through the brain network – to the target brain regions 274. In a related study, Betzel et al. used the structural wiring of the brain to simulate transitions between commonly observed activity states 275. They found that optimal control nodes tended to have high degree in the network, and that when this rich-club of hub regions was destroyed by simulated lesioning, the ability of the brain to make common transitions was significantly reduced. 

In addition to studying the roles of specific control trajectories, complementary approaches have considered trajectory-independent metrics such as the average and modal controllabilities 


discussed in Box 4 276. By comparing control theoretic measures of node controllability with the cognitive functions associated with each brain region, researchers have observed that different types of controllers are located in distinct areas of the brain (Fig. 3b) 241. For example, brain regions with strong average controllability are disproportionately located in the default mode system, which is associated with baseline neural activity; meanwhile, strong modal controllers are primarily located in cognitive control systems. These observations are particularly interesting because they suggest that regions associated with the default mode are optimally positioned to push the system into many easily reachable states, while regions associated with cognitive control are optimally positioned to steer the system toward distant states. 

As a final layer of abstraction, rather than studying the controllabilities of specific brain regions, one could envision averaging over all regions to quantify the mean controllability of an entire brain network. Interestingly, by taking precisely this approach, Tang et al. established that brain networks as a whole are finely tuned to maximize both average and modal controllability, thereby supporting a diverse range of possible control strategies 277. Furthermore, by comparing subjects in different stages of adolescence, the researchers found that brain network controllability increases with age, suggesting that neural circuitry evolves over time to support increasingly complex dynamics. In related studies, metrics of network controllability were found to differ by sex 

(^278) and to be altered in individuals with high genetic risk for bipolar disorder 242. Taken together, these results demonstrate that network measures of optimal control and controllability correspond closely to existing notions of intrinsic and cognitive control in neuroscience. This close correspondence, in turn, suggests that network control theory, by taking into account the complex wiring of the brain, has the promise to enrich our understanding of the brain’s control principles 279. The future of brain network control. Throughout this section, we have focused primarily on targeted therapies that rely on the coarse-grained stimulation of entire brain regions and simple control strategies that assume idealized linear dynamics. Emerging efforts in neuroscience and control theory, however, are opening the door for a number of significant improvements, including: (i) techniques for fine-scale control of neural activity 280–283, even down to the level of in


dividual neurons 284, 285, (ii) systems identification approaches that allow for the incorporation of effective connectivity measurements to inform control, superseding solely structural explanations 

(^286) , and (iii) generalizations of linear control theory that include more realistic nonlinear dynamics 287, 288. Among recent advances in the manipulation of fine-scale neural activity, arguably the most promising tool is optogenetics, which offers millisecond-scale optical control of specific cell types within the brains of conscious animals 280, 281. Its striking precision 282 , in some cases even down to single-cell resolution 284, 285, has enabled researchers to investigate the nature of causal signals between neurons and to study how these signals give rise to qualitative changes in animal behavior (^283). While linear control theory continues to provide critical insights about how signals propagate along the brain’s structural wiring 240, 241, 274, 275, interactions between neural components, from individual neurons to entire brain regions, are highly nonlinear (Fig. 2b) 119. Initial efforts to develop a theory of nonlinear control, dating as early as the 1970s 289–291, quickly converged on the conclusion that results as strong and general as those derived for linear dynamics could not be obtained for a general nonlinear system 238. Fortunately, concerted theoretic efforts have led to weaker notions of nonlinear controllability 292 , notable among which are techniques for linearizing nonlinear systems around stable equilibrium states 287, 288^ and methods for leveraging the symmetries of a system 293 such as repeated network motifs to simplify control strategies 294. Additional efforts have utilized advances in computing power to simulate the effects of external perturbations across a range of model systems, including networks of FitzHugh–Nagumo neurons 293 , Wilson–Cowan neural masses 243 , and Kuramoto oscillators 295 as well as artificial neural networks such as the Ising model 296, 297. Together, recent advances in high-precision neural stimulation like optogenetics and our emerging understanding of the principles governing nonlinear control are pushing the boundaries of what is considered possible in the investigation of neural activity. Targeted control of the brain’s complex behavior – once considered a topic of science fiction – now has the promise to shape targeted therapies for a range of psychiatric and neurological disorders. 


Conclusions and future directions in the neurophysics of brain networks 

The intricate inner workings of the brain remains one of the greatest mysteries defying resolution by contemporary scientific inquiry. On the heels of decades of effort investigating the functions of the brain’s individual components 298 , from neurons to neuronal ensembles and large-scale brain regions, conclusive evidence points to the need for maps and models of the interactions between these components in order to fundamentally understand the brain’s ensemble dynamics, circuit function, and emergent behavior 36, 299. Here we reviewed recent advances toward meeting this challenge with an eclectic array of curios from the physicist’s cabinet: statistical mechanics of complex networks, thermodynamics, information theory, dynamical systems theory, and control theory. In the course of our exposition, we considered the principles of small-worldness 27 , interconnected high-degree hubs 300 , modularity 91 , and spatial embedding 301 that provide useful explanations for the architecture of structural brain networks. We then saw these same principles reflected in the organization of long-range functional connectivity supporting information dissemination, and the computations that can result therefrom 38, 216. As with any physical system, a natural next step is to probe the validity of our descriptive and explanatory models using perturbative approaches both in theory and experiment. Thus, we next summarized the utility of network control theory in offering insights into internal control processes such as homeostatic regulation and cognitive control, as well as external control processes such as neurostimulation, which are currently being used to treat multiple disorders of mental health 279. 

Throughout the exposition, we described current frontiers in the investigation of brain network structure, function, and control. Although we will not reiterate those points here, we do wish to offer the sentiment that, while the empirical advances laying the foundation of the field have spanned several decades, the network physics of the brain is an incredibly young area, rich with opportunities for discovery. And perhaps – with a bit of courage – we may even begin to provide an empirical constitution to the deeper philosophical questions that humans have wrestled with for millennia: What makes us unique and different from non-human animals 240, 302? How do we represent abstract concepts such as value to ourselves 303 and others 304? How are representations 


transmitted throughout the brain or reconfigured based on new knowledge 305? What makes a mind from a brain? Physicists, the brain is calling you. 


Box 1 | A simple primer on networks. Here, we define what we mean by a network and describe tools for summarizing its architecture. Importantly, a network is agnostic to the system that it represents 36 , whether it be a brain, a granular material 306 , or a quantum lattice 307. By far the simplest network model is represented by a binary undirected graph in which identical nodes represent system components and identical edges indicate relations or connections between pairs of nodes (see the figure). Such a network can be encoded in an adjacency matrix A, where each element Aij indicates the strength of connectivity between nodes i and j. When all edge strengths are unity, the network is said to be binary. When edges have a range of weights, the network represented by the adjacency matrix is said to be weighted. When A = Aᵀ, the network is undirected; otherwise, the network is directed. 

 One can extend this simple encoding to study multilayer, multislice, and multiplex networks 

(^308) ; dynamic or temporal networks 127, 309; annotated networks 310 ; hypergraphs 311 ; and simplicial complexes 230. One can also calculate various statistics to quantify the architecture of a network and to infer the function thereof (see figure). Intuitively, these statistics range from measures of the local structure in the network, which depend solely on the links directly emanating from a given node (e.g., degree and clustering), to measures of the network’s global structure, which depend on the complex pattern of interconnections between all nodes (e.g., path lengths and centrality) (^30). Intermediate statistics exist to study network organization at the mesoscale, such as cavity structure and community structure, the latter of which describes the presence of communities of densely connected nodes 312–314. As we will see, the encoding of a system as a network and the quantitative assessment of its architecture can provide important insights into its function 34, 107. 


 Degree 

 Clustering 

 Path length 

 Centrality 

Communities 

 Cavities 

 Node Edge 


Box 2 | Bridging spatiotemporal scales. In the context of complex systems generally and neural systems specifically, the cutting edge work relates to extending our tools, theories, and intuitions from a single network to so-called multiscale, multilayer, and multiplex networks 308, 315. Perhaps the most obvious context in which to make this extension is from regional networks to cellular-scale neuronal networks 121. Large-scale brain activity provides a coarse-grained encoding of neural processes, and the map from cellular dynamics to regional dynamics reflects rules of system function. By combining these two layers we can address questions like, “How do cellular processes shape circuit behavior?” The next logical extension is to move even further down the natural hierarchy of scales to understand how molecular networks – including gene coexpression networks 123, 316–318 

- shape the behavior of cells 319. Understanding how molecular mechanisms affect large-scale brain network function is critical for the development of effective pharmacological interventions 116, 320, 321. By extending the network model from regions to cells to molecular drivers, we can ask 

questions like, “How do genetic codes and epigenetic drivers shape circuit behavior across spatial scales?” And in a final extension, it is time to move up in the natural hierarchy of scales to combine information from the connectivity within a single human brain to the connectivity between human brains in large-scale social networks 304, 322–324. While brain activity and structure offer biological mechanisms for human behaviors, social networks offer external inducers or modulators of those behaviors 325. By extending the network model to this larger scale, we can start to ask – and potentially answer – questions like, “How do brains shape social networks? And how do social ties shape the brain?” This extension will be important in understanding human behavior within the broader contexts of culture and society. 

 Molecular network Neuronal network Regional network Social network 


Box 3 | Information theory and network neuroscience. At its core the brain is an information processing system, having evolved over millions of years to encode and manipulate a continuous stream of sensory signals 326. As such, information theory – the science of how signals are encoded and processed – provides a compelling lens through which to study the brain’s function 327. Information theory began with the 1948 paper “A Mathematical Theory of Communication,” wherein Claude Shannon proposed the entropy of a signal as the natural measure of its information content and derived fundamental limits on the information capacity of a communication channel 328. Soon after, MacKay and McCulloch adapted the concept of channel capacity to obtain limits on the rate at which one neuron can transmit information to another 329 , sparking the study of information flow in the brain. Subsequent work by Attneave and Barlow proposed the idea that neural activity is optimized for the transmission of sensory information 330, 331, providing the foundation for future investigations of neural coding 135, 326. 

Despite these initial efforts bridging information theory and neuroscience, progress slowed primarily due to difficulties obtaining unbiased information estimates from neural systems. Improvements in experimental techniques, however, eventually sparked renewed interest 332 , spurring the introduction of robust methods for estimating information theoretic quantities 333–335. On the basis of these advancements, information theory has once again become a powerful tool for the network neuroscientist. Recent attempts, for instance, to uncover causal relationships between neural elements have successfully adapted notions of information flow, such as mutual information and transfer entropy 336, 337. At the same time, efforts to understand large-scale correlations within neuronal populations have utilized the principle of maximum entropy 338 , resulting in Ising-like models of collective neural behavior 141, 198. As information theory becomes increasingly integrated into the fabric of neuroscience, physicists are uniquely positioned to pioneer exciting new techniques for investigating the nature of information processing in the brain. 


Box 4 | Linear control and network controllability. To investigate the principles of control in the brain, it is useful to understand the theory of network control generally. In network control, the system in question typically comprises a complex web of interacting components, and the goal is to drive this networked system toward a desired state by influencing a select number of input nodes 238. The starting point for most control theoretic problems is the linear time-invariant control system x(t + 1) = Ax(t) + u(t), where x(t) defines the state of the system (e.g., the BOLD signal measured by fMRI), A is the interaction matrix (e.g., white matter tracts estimated using DTI), and u(t) defines the input signal (e.g., electromagnetic stimulation using TMS or DBS) 339. Such a system is said to be controllable if it can be driven to any desired state. Often, however, many naturally occurring networks that are theoretically controllable cannot be steered to certain states due to limitations on control resources 340, 341, motivating the introduction of control strategies u∗(t) that minimize the so-called control energy E(u) = ∑∞ t=0 |u(t)|^22. 

By limiting the control input to a single node, we can quantify the ability of that node to steer the dynamics of the entire system. For example, the average controllability of a node represents its capacity to drive the network to many nearby states 241 , while a node’s modal controllability quantifies its ability to push the network toward distant hard-to-reach states 276 (see figure). Averaging these metrics over all nodes in a system, one can estimate the inherent controllability of an entire network itself. Control theoretic efforts such as these have only recently been applied to understand the locomotion of the nematode 342 and the networked behavior of the brain more broadly 237, 239, 279, promising new strategies for stimulation-based therapies and fresh insights about the 

brain’s capacity for intrinsic control. 

 Linear control Controllability metrics Linear dynamics signal ui 

 network Aij 

 state xi 

 Initial state 

 x 1 x 3 

 x 2 

 Uncontrolled trajectory^ Controlled trajectory Average Nearby controllability: states 

 Control energy Modal Distant controllability: states 

 x (t+1) = Ax (t) + u (t) x 1 Initial^ state 


References 

1. Lear, J. Aristotle: The Desire to Understand (Cambridge University Press, 1988). 

2. Aristotle. Metaphysics, vol. VII.7. 

3. Stenger, V. J., Lindsay, J. A. & Boghossian, P. Physicists are philosophers, too. Scientific     American (2015). 

4. von Neumann, J. The Computer and the Brain (1958). 

5. Hopfield, J. J. Neural networks and physical systems with emergent collective computational     abilities. Proc. Nat. Acad. Sci. (USA) 79 , 2554–2558 (1982). 

6. Scott, A. Neurophysics (Wiley, 1977). 

7. Koch, C. & Poggio, T. A theoretical analysis of electrical properties of spines. Proc R Soc     Lond B Biol Sci 218 , 455–477 (1983). 

8. Tyler, W. J. The mechanobiology of brain function. Nature Reviews Neuroscience 13 , 867–     878 (2012). 

9. Friston, K., Kilner, J. & Harrison, L. A free energy principle for the brain. J Physiol Paris     100 , 70–87 (2006). 

10. Plewes, D. B. & Kucharczyk, W. Physics of MRI: a primer. J Magn Reson Imaging 35 ,     1038–1054 (2012). 

11. Hari, R. & Salmelin, R. Magnetoencephalography: From SQUIDs to neuroscience. Neu-     roimage 20th anniversary special edition. Neuroimage 61 , 386–396 (2012). 

12. Boto, E. et al. Moving magnetoencephalography towards real-world applications with a     wearable system. Nature 555 , 657–661 (2018). 

13. Alivisatos, A. P. et al. Nanotools for neuroscience and brain activity mapping. ACS Nano 7 ,     1850–1866 (2013). 


14. Piazza, S., Bianchini, P., Sheppard, C., Diaspro, A. & Duocastella, M. Enhanced volumetric     imaging in 2-photon microscopy via acoustic lens beam shaping. J Biophotonics 11 (2018). 

15. Boyden, E. S., Zhang, F., Bamberg, E., Nagel, G. & Deisseroth, K. Millisecond-timescale,     genetically targeted optical control of neural activity. Nat Neurosci 8 , 1263–1268 (2005). 

16. Popkin, G. Physicists, the brain is calling you (2016). 

17. McCulloch, W. S. & Pitts, W. A logical calculus of the ideas immanent in nervous activity.     Bull Math Biol 5 , 115–133 (1943). 

18. Fries, P. Rhythms for cognition: Communication through coherence. Neuron 88 , 220–235     (2015). 

19. Betzel, R. F. & Bassett, D. S. Specificity and robustness of long-distance connections in     weighted, interareal connectomes. Proc Natl Acad Sci U S A 115 , E4880–E4889 (2018). 

20. Poincare, H. Science and Hypothesis (London: Walter Scott Publishing, 1905). 

21. Van Essen, D. C. et al. The WU-Minn Human Connectome Project: an overview. Neuroim-     age 80 , 62–79 (2013). 

22. Markram, H. et al. Reconstruction and simulation of neocortical microcircuitry. Cell 163 ,     456–492 (2015). 

23. Poo, M. M. et al. China Brain Project: Basic Neuroscience, Brain Diseases, and Brain-     Inspired Computing. Neuron 92 , 591–596 (2016). 

24. Okano, H., Miyawaki, A. & Kasai, K. Brain/MINDS: brain-mapping project in Japan. Philos     Trans R Soc Lond B Biol Sci 370 , 20140310 (2015). 

25. Bassett, D. S. & Gazzaniga, M. S. Understanding complexity in the human brain. Trends     Cogn Sci 15 , 200–209 (2011). 

26. Sethna, J. P. Statistical Mechanics: Entropy, Order Parameters and Complexity (Oxford     University Press, 2006). 


27. Bassett, D. S. & Bullmore, E. T. Small-world brain networks revisited. Neuroscientist Sep     21 , 1073858416667720 (2016). 

28. Albert, E. & Barabasi, A.-L. Statistical mechanics of complex networks. Rev. Mod. Phys. 74     (2002). 

29. Butts, C. T. Revisiting the foundations of network analysis. Science 325 , 414–416 (2009). 

30. Costa, L. d. F., Rodrigues, F. A., Travieso, G. & Villas Boas, P. R. Characterization of     complex networks: A survey of measurements. Advances In Physics 56 , 167–242 (2006). 

31. Gross, T. & Blasius, B. Adaptive coevolutionary networks: a review. J R Soc Interface 5 ,     259–271 (2008). 

32. Zhang, X., Moore, C. & Newman, M. E. J. Random graph models for dynamic networks.     Eur. Phys. J. B 90 , 200 (2017). 

33. Hackett, A., Melnik, s. & Gleeson, J. P. Cascades on a class of clustered random networks.     Phys. Rev. E 83 , 056107 (2011). 

34. The structure and function of complex networks. SIAM REVIEW 45 , 167–256 (2003). 

35. Motter, A. E. Networkcontrology. Chaos 25 , 097621 (2015). 

36. Bassett, D. S., Zurn, P. & Gold, J. I. On the nature and use of models in network neuroscience.     Nat Rev Neurosci Epub ahead of print (2018). 

37. Pereda, A. E. Electrical synapses and their functional interactions with chemical synapses.     Nat Rev Neurosci 15 , 250–263 (2014). 

38. Avena-Koenigsberger, A., Misic, B. & Sporns, O. Communication dynamics in complex     brain networks. Nat Rev Neurosci 19 , 17–33 (2017). 

39. Ising, E. Beitrag zur theorie des ferromagnetismus. Zeitschrift f ̈ur Physik 31 , 253–258     (1925). 


40. Onsager, L. Crystal statistics. i. a two-dimensional model with an order-disorder transition.     Phys. Rev. 65 , 117 (1944). 

41. Brush, S. G. History of the lenz-ising model. Rev. Mod. Phys. 39 , 883 (1967). 

42. Sporns, O., Chialvo, D. R., Kaiser, M. & Hilgetag, C. C. Organization, development and     function of complex brain networks. Trends Cogn Sci 8 , 418–425 (2004). 

43. Medaglia, J. D., Lynall, M. E. & Bassett, D. S. Cognitive network neuroscience. J Cogn     Neurosci 27 , 1471–1491 (2015). 

44. Sporns, O. Contributions and challenges for network models in cognitive neuroscience. Nat     Neurosci 17 , 652–660 (2014). 

45. Petersen, S. E. & Sporns, O. Brain networks and cognitive architectures. Neuron 88 , 207–219     (2015). 

46. Misic, B. & Sporns, O. From regions to connections and networks: new bridges between     brain and behavior. Curr Opin Neurobiol 40 , 1–7 (2016). 

47. Wallace, E., Maei, H. R. & Latham, P. E. Randomly connected networks have short temporal     memory. Neural Comput 25 , 1408–1439 (2013). 

48. Rajan, K., Harvey, C. D. & Tank, D. W. Recurrent network models of sequence generation     and memory. Neuron 90 , 128–142 (2016). 

49. Chaudhuri, R. & Fiete, I. Computational principles of memory. Nat Neurosci 19 , 394–403     (2016). 

50. Hermundstad, A. M., Brown, K. S., Bassett, D. S. & Carlson, J. M. Learning, memory, and     the role of neural network architecture. PLoS Comput Biol 7 , e1002063 (2011). 

51. Teileanu, T., Olveczky, B. & Balasubramanian, V. Rules and mechanisms for efficient two-     stage learning in neural circuits. Elife 6 , e20944 (2017). 


52. Takemura, S. Y. et al. A visual motion detection circuit suggested by drosophila connec-     tomics. Nature 500 , 175–181 (2013). 

53. Zhen, M. & Samuel, A. D. C. elegans locomotion: small circuits, complex functions. Curr     Opin Neurobiol 33 , 117–126 (2015). 

54. Golgi, C. Sulla fina anatomia degli organi centrali del sistema nervoso (S. Calderini, 1885). 

55. y Cajal, S. R. Estructura de los centros nerviosos de las aves (1888). 

56. Shepherd, G. M. Foundations of the neuron doctrine (Oxford University Press, 2015). 

57. White, J. G., Southgate, E., Thomson, J. N. & Brenner, S. The structure of the nervous     system of the nematode Caenorhabditis elegans. Phil. Trans. R. Soc. Lond. B 314 , 1–340     (1986). 

58. Helmstaedter, M. et al. Connectomic reconstruction of the inner plexiform layer in the mouse     retina. Nature 500 , 168–174 (2013). 

59. Sporns, O., Tononi, G. & K ̈otter, R. The human connectome: a structural description of the     human brain. PLoS Comput Biol 1 , e42 (2005). 

60. Stephan, K. E. et al. Advanced database methodology for the collation of connectivity data     on the Macaque brain (CoCoMac). Philos Trans R Soc Lond B Biol Sci 356 , 1159–1186     (2001). 

61. Markov, N. T. et al. A weighted and directed interareal connectivity matrix for macaque     cerebral cortex. Cereb Cortex 24 , 17–36 (2014). 

62. Young, M. P., Scannell, J. W., Burns, G. A. & Blakemore, C. Analysis of connectivity: neural     systems in the cerebral cortex. Rev Neurosci 5 , 227–250 (1994). 

63. Oh, S. W. et al. A mesoscale connectome of the mouse brain. Nature 508 , 207–214 (2014). 

64. Shih, C. T. et al. Connectomics-based analysis of information flow in the Drosophila brain.     Curr Biol 25 , 1249–1258 (2015). 


65. Hsieh, J. et al. Computed tomography: principles, design, artifacts, and recent advances     (SPIE Bellingham, WA, 2009). 

66. Pierpaoli, C., Jezzard, P., Basser, P. J., Barnett, A. & Di Chiro, G. Diffusion tensor MR     imaging of the human brain. Radiology 201 , 637–648 (1996). 

67. Basser, P. J., Pajevic, S., Pierpaoli, C., Duda, J. & Aldroubi, A. In vivo fiber tractography     using DT-MRI data. Magn Reson Med 44 , 625–632 (2000). 

68. Behrens, T. E. & Johansen-Berg, H. Relating connectional architecture to grey matter func-     tion using diffusion imaging. Philos Trans R Soc Lond B Biol Sci 360 , 903–911 (2005). 

69. Bullmore, E. & Sporns, O. The economy of brain network organization. Nat. Rev. Neurosci.     13 , 336–349 (2012). 

70. Betzel, R. F. & Bassett, D. S. Generative models for network neuroscience: prospects and     promise. J R Soc Interface 14 , 20170623 (2017). 

71. Bassett, D. S. & Sporns, O. Network neuroscience. Nat Neurosci 20 , 353–364 (2017). 

72. Nicosia, V., V ́ertes, P. E., Schafer, W. R., Latora, V. & Bullmore, E. T. Phase transition in     the economically modeled growth of a cellular nervous system. Proceedings of the National     Academy of Sciences USA 110 , 7880–7885 (2013). 

73. Henriksen, S., Pang, R. & Wronkiewicz, M. A simple generative model of the mouse     mesoscale connectome. Elife 5 , e12366 (2016). 

74. Beul, S. F., Grant, S. & Hilgetag, C. C. A predictive model of the cat cortical connectome     based on cytoarchitecture and distance. Brain Struct Funct 220 , 3167–3184 (2015). 

75. Ercsey-Ravasz, M. et al. A predictive network model of cerebral cortical connectivity based     on a distance rule. Neuron 80 , 184–197 (2013). 

76. Beul, S. F., Barbas, H. & Hilgetag, C. C. A predictive structural model of the primate con-     nectome. Sci Rep 7 , 43176 (2017). 


77. Betzel, R. F. et al. Generative models of the human connectome. Neuroimage 124 , 1054–     1064 (2016). 

78. Thompson, P. M. et al. Genetic influences on brain structure. Nat. Neurosci. 4 , 1253 (2001). 

79. Raz, N. et al. Regional brain changes in aging healthy adults: general trends, individual     differences and modifiers. Cereb. Cortex 15 , 1676–1689 (2005). 

80. Gong, G. et al. Age-and gender-related differences in the cortical anatomical network. J.     Neurosci. 29 , 15684–15693 (2009). 

81. Kanai, R. & Rees, G. The structural basis of inter-individual differences in human behaviour     and cognition. Nat. Rev. Neurosci. 12 , 231 (2011). 

82. Banissy, M. J., Kanai, R., Walsh, V. & Rees, G. Inter-individual differences in empathy are     reflected in human brain structure. Neuroimage 62 , 2034–2039 (2012). 

83. Fleming, S. M., Weil, R. S., Nagy, Z., Dolan, R. J. & Rees, G. Relating introspective accuracy     to individual differences in brain structure. Science 329 , 1541–1543 (2010). 

84. Hartley, C. A., Fischl, B. & Phelps, E. A. Brain structure correlates of individual differences     in the acquisition and inhibition of conditioned fear. Cereb. Cortex 21 , 1954–1962 (2011). 

85. Kanai, R., Feilden, T., Firth, C. & Rees, G. Political orientations are correlated with brain     structure in young adults. Curr. Biol. 21 , 677–680 (2011). 

86. Erd ̈os, P. & R ́enyi, A. On the evolution of random graphs. Publ. Math. Inst. Hung. Acad. Sci     5 , 17–60 (1960). 

87. Sherrington, C. S. The Integrative Action of the Nervous System (Yale University Press,     1906). 

88. Sporns, O., Tononi, G. & Edelman, G. M. Theoretical neuroanatomy: relating anatomical     and functional connectivity in graphs and cortical connection matrices. Cereb. cortex 10 ,     127–141 (2000). 


89. Hilgetag, C.-C., Burns, G. A., O’Neill, M. A., Scannell, J. W. & Young, M. P. Anatomical     connectivity defines the organization of clusters of cortical areas in the macaque and the cat.     Phil. Trans. R. Soc. Lon. B 355 , 91–110 (2000). 

90. Sporns, O. & Zwi, J. D. The small world of the cerebral cortex. Neuroinformatics 2 , 145–162     (2004). 

91. Sporns, O. & Betzel, R. F. Modular brain networks. Annu Rev Psychol 67 , 613–640 (2016). 

92. Bassett, D. S. et al. Efficient physical embedding of topologically complex information pro-     cessing networks in brains and computer circuits. PLoS Comput. Biol. 6 , e1000748 (2010). 

93. Taylor, P. N., Wang, Y. & Kaiser, M. Within brain area tractography suggests local modularity     using high resolution connectomics. Sci Rep 7 , 39859 (2017). 

94. Lesicko, A. M., Hristova, T. S., Maigler, K. C. & Llano, D. A. Connectional modularity     of top-down and bottom-up multimodal inputs to the lateral cortex of the mouse inferior     colliculus. J Neurosci 36 , 11037–11050 (2016). 

95. Sohn, Y., Choi, M. K., Ahn, Y. Y., Lee, J. & Jeong, J. Topological cluster analysis reveals     the systemic organization of the Caenorhabditis elegans connectome. PLoS Comput Biol 7 ,     e1001139 (2011). 

96. Azulay, A., Itskovits, E. & Zaslaver, A. The C. elegans connectome consists of homogenous     circuits with defined functional roles. PLoS Comput Biol 12 , e1005021 (2016). 

97. Betzel, R. F. & Bassett, D. S. Multi-scale brain networks. Neuroimage 160 , 73–83 (2017). 

98. Khambhati, A. N., Sizemore, A. E., Betzel, R. F. & Bassett, D. S. Modeling and interpreting     mesoscale network dynamics. Neuroimage S1053-8119, 30500–1 (2017). 

99. Aicher, C., Jacobs, A. Z. & Clauset, A. Learning latent block structure in weighted networks.     Journal of Complex Networks 3 , 221–248 (2015). 


100. Betzel, R. F., Medaglia, J. D. & Bassett, D. S. Diversity of meso-scale architecture in human     and non-human connectomes. Nature Communications 9 , 346 (2018). 

101. van den Heuvel, M. P. & Sporns, O. Network hubs in the human brain. Trends Cogn. Sci. 17 ,     683–696 (2013). 

102. Liao, X., Vasilakos, A. V. & He, Y. Small-world human brain networks: Perspectives and     challenges. Neurosci Biobehav Rev 77 , 286–300 (2017). 

103. Deco, G., Tononi, G., Boly, M. & Kringelbach, M. L. Rethinking segregation and integration:     contributions of whole-brain modelling. Nat. Rev. Neurosci. 16 , 430 (2015). 

104. Latora, V. & Marchiori, M. Efficient behavior of small-world networks. Phys. Rev. Lett. 87 ,     198701 (2001). 

105. Kaiser, M. & Hilgetag, C. C. Nonoptimal component placement, but short processing paths,     due to long-distance projections in neural systems. PLOS Comput. Biol. 2 , e95 (2006). 

106. Travers, J. & Milgram, S. The small world problem. Phychology Today 1 , 61–67 (1967). 

107. Watts, D. J. & Strogatz, S. H. Collective dynamics of ’small-world’ networks. Nature 393 ,     440–442 (1998). 

108. Gong, G. et al. Mapping anatomical connectivity patterns of human cerebral cortex using in     vivo diffusion tensor imaging tractography. Cereb. cortex 19 , 524–536 (2008). 

109. Wedeen, V. J., Hagmann, P., Tseng, W.-Y. I., Reese, T. G. & Weisskoff, R. M. Mapping     complex tissue architecture with diffusion spectrum magnetic resonance imaging. Magn.     Reson. Med. 54 , 1377–1386 (2005). 

110. de Solla Price, D. J. Networks of scientific papers. Science 149 , 510–515 (1965). 

111. Barabasi, A. L. & Albert, R. Emergence of scaling in random networks. Science 286 , 509–     512 (1999). 


112. Dall, J. & Christensen, M. Random geometric graphs. Physical Review E 66 , 016121 (2002). 

113. Vertes, P. E. et al. Simple models of human brain functional networks. Proc Natl Acad Sci     U S A 109 , 5868–5873 (2012). 

114. Rubinov, M., Ypma, R., Watson, C. & Bullmore, E. Wiring cost and topological participation     of the mouse brain connectome. Proceedings of the National Academy of Sciences of the USA     doi/10.1073/pnas.1420315112 (2015). 

115. Kaiser, M. Mechanisms of connectome development. Trends Cogn Sci 21 , 703–717 (2017). 

116. Stam, C. J. Modern network science of neurological disorders. Nat Rev Neurosci 15 , 683–695     (2014). 

117. Scholtens, L. H., Schmidt, R., de Reus, M. A. & van den Heuvel, M. P. Linking macroscale     graph analytical organization to microscale neuroarchitectonics in the macaque connectome.     J Neurosci 34 , 12192–12205 (2014). 

118. Chaudhuri, R., Knoblauch, K., Gariel, M. A., Kennedy, H. & Wang, X. J. A large-scale     circuit mechanism for hierarchical dynamical processing in the primate cortex. Neuron 88 ,     419–431 (2015). 

119. Breakspear, M. Dynamic models of large-scale brain activity. Nat Neurosci 20 , 340–352     (2017). 

120. Bentley, B. et al. The multilayer connectome of Caenorhabditis elegans. PLoS Comput Biol     12 , e1005283 (2016). 

121. Mejias, J. F., Murray, J. D., Kennedy, H. & Wang, X. J. Feedforward and feedback frequency-     dependent interactions in a large-scale laminar network of the primate cortex. Sci Adv. 2 ,     e1601335 (2016). 

122. Seung, H. S. & Sumbul, U. Neuronal cell types and connectivity: lessons from the retina.     Neuron 83 , 1262–1272 (2014). 


123. Arnatkeviciute, A., Fulcher, B. D., Pocock, R. & Fornito, A. Hub connectivity, neuronal     diversity, and gene expression in the Caenorhabditis elegans connectome. PLoS Comput Biol     14 , e1005989 (2018). 

124. Scholz, J., Klein, M. C., Behrens, T. E. & Johansen-Berg, H. Training induces changes in     white-matter architecture. Nat Neurosci 12 , 1370–1371 (2009). 

125. Baum, G. L. et al. Modular segregation of structural brain networks supports the development     of executive function in youth. Curr Biol 27 , 1561–1572.e8 (2017). 

126. Zuo, X. N. et al. Human connectomics across the life span. Trends Cogn Sci 21 , 32–45     (2017). 

127. Holme, P. & Saramaki, J. Temporal networks. Phys. Rep. 519 , 97–125 (2012). 

128. Li, A., Cornelius, S. P., Liu, Y.-Y., Wang, L. & Barab ́asi, A.-L. The fundamental advantages     of temporal networks. Science 358 , 1042–1046 (2017). 

129. Hebb, D. The Organization of Behavior (Wiley, 1949). 

130. Magee, J. C. & Johnston, D. A synaptically controlled, associative signal for hebbian plas-     ticity in hippocampal neurons. Science 275 , 209–213 (1997). 

131. Montague, P. R., Dayan, P. & Sejnowski, T. J. A framework for mesencephalic dopamine     systems based on predictive hebbian learning. J. Neurosci. 16 , 1936–1947 (1996). 

132. Song, S., Miller, K. D. & Abbott, L. F. Competitive hebbian learning through spike-timing-     dependent synaptic plasticity. Nat. Neurosci. 3 , 919 (2000). 

133. Chialvo, D. R. Emergent complex neural dynamics. Nat. Phys. 6 , 744 (2010). 

134. Tononi, G., Boly, M., Massimini, M. & Koch, C. Integrated information theory: from con-     sciousness to its physical substrate. Nat Rev Neurosci 17 , 450–461 (2016). 

135. Abbott, L. F. & Dayan, P. Theoretical Neuroscience (MIT Press, 2001). 


136. Dechery, J. B. & MacLean, J. N. Emergent cortical circuit dynamics contain dense, interwo-     ven ensembles of spike sequences. J Neurophysiol 118 , 1914–1925 (2017). 

137. Reif, F. Fundamentals of statistical and thermal physics (Waveland Press, 2009). 

138. Brody, C. D. Correlations without synchrony. Neural Comput 11 , 1537–1551 (1999). 

139. Brody, C. D. Disambiguating different covariation types. Neural Comput 11 , 1527–1535     (1999). 

140. Sporns, O., Tononi, G. & Edelman, G. M. Connectivity and complexity: the relationship     between neuroanatomy and brain dynamics. Neural Netw 13 , 909–922 (2000). 

141. Schneidman, E., Berry II, M. J., Segev, R. & Bialek, W. Weak pairwise correlations imply     strongly correlated network states in a neural population. Nature 440 , 1007 (2006). 

142. Levina, A., Herrmann, J. M. & Geisel, T. Dynamical synapses causing self-organized criti-     cality in neural networks. Nat. Phys. 3 , 857 (2007). 

143. Vuksanovic, V. & Hovel, P. Functional connectivity of distant cortical regions: role of remote     synchronization and symmetry in interactions. Neuroimage 97 , 1–8 (2014). 

144. Flourens, P. Recherches exp ́erimentales sur les propri ́et ́es et les fonctions du syst`eme nerveux     dans les animaux vert ́ebr ́es (Balli`ere, 1842). 

145. Panizza, B. Osservazioni sul nervo ottico (Bernardoni, 1855). 

146. Broca, P. Remarques sur le si`ege de la facult ́e du langage articul ́e, suivies dune observation     daph ́emie (perte de la parole). Bulletin et Memoires de la Societe anatomique de Paris 6 ,     330–357 (1861). 

147. von Helmholtz, H. Vorl ̈aufiger bericht ̈uber die fortpflanzungs-geschwindigkeit der nerven-     reizung. Archiv f ̈ur Anatomie, Physiologie und wissenschaftliche Medicin 71–73 (1850). 

148. Haas, L. F. Hans berger (1873–1941), richard caton (1842–1926), and electroencephalogra-     phy. J. Neurol. Neurosurg. Psychiatry 74 , 9–9 (2003). 


149. Caton, R. Electrical currents of the brain. J. Nerv. Ment. Dis. 2 , 610 (1875). 

150. Beck, A. Die str ̈ome der nervencentren. Centralbl Physiol 4 , 572–573 (1890). 

151. Lorente de N ́o, R. Studies on the structure of the cerebral cortex. ii. continuation of the study     of the ammonic system. Journal f ̈ur Psychologie und Neurologie (1934). 

152. Green, D. J. & Gillette, R. Circadian rhythm of firing rate recorded from single cells in the     rat suprachiasmatic brain slice. Brain Res. 245 , 198–200 (1982). 

153. Edwards, F. A., Konnerth, A., Sakmann, B. & Takahashi, T. A thin slice preparation for patch     clamp recordings from neurones of the mammalian central nervous system. Pfl ̈ugers Archiv     414 , 600–612 (1989). 

154. Stosiek, C., Garaschuk, O., Holthoff, K. & Konnerth, A. In vivo two-photon calcium imaging     of neuronal networks. Proc Natl Acad Sci U S A 100 , 7319–7324 (2003). 

155. Grewe, B. F., Langer, D., Kasper, H., Kampa, B. M. & Helmchen, F. High-speed in vivo     calcium imaging reveals neuronal network activity with near-millisecond precision. Nat.     Methods 7 , 399 (2010). 

156. Penny, W. D., Friston, K. J., Ashburner, J. T., Kiebel, S. J. & Nichols, T. E. Statistical     parametric mapping: the analysis of functional brain images (Elsevier, 2011). 

157. H ̈am ̈al ̈ainen, M., Hari, R., Ilmoniemi, R. J., Knuutila, J. & Lounasmaa, O. V. Magnetoen-     cephalographytheory, instrumentation, and applications to noninvasive studies of the working     human brain. Rev. Mod. Phys. 65 , 413 (1993). 

158. Bailey, D. L., Maisey, M. N., Townsend, D. W. & Valk, P. E. Positron emission tomography     (Springer, 2005). 

159. Raichle, M. E. Behind the scenes of functional brain imaging: a historical and physiological     perspective. Proc Natl Acad Sci U S A 95 , 765–772 (1998). 


160. Zarahn, E., Aguirre, G. K. & D’Esposito, M. Empirical analyses of bold fmri statistics.     Neuroimage 5 , 179–197 (1997). 

161. Van Den Heuvel, M. P. & Pol, H. E. H. Exploring the brain network: a review on resting-state     fmri functional connectivity. Eur Neuropsychopharmacol 20 , 519–534 (2010). 

162. Bullmore, E. & Sporns, O. Complex brain networks: graph theoretical analysis of structural     and functional systems. Nat Rev Neurosci 10 , 186–198 (2009). 

163. Zalesky, A., Fornito, A. & Bullmore, E. On the use of correlation as a measure of network     connectivity. Neuroimage 60 , 2096–2106 (2012). 

164. He, Y. et al. Uncovering intrinsic modular organization of spontaneous brain activity in     humans. PloS one 4 , e5226 (2009). 

165. Salvador, R. et al. Neurophysiological architecture of functional magnetic resonance images     of human brain. Cerebral cortex 15 , 1332–1342 (2005). 

166. Achard, S., Salvador, R., Whitcher, B., Suckling, J. & Bullmore, E. A resilient, low-     frequency, small-world human brain functional network with highly connected association     cortical hubs. J Neurosci 26 , 63–72 (2006). 

167. Bettencourt, L. M., Stephens, G. J., Ham, M. I. & Gross, G. W. Functional structure of     cortical neuronal networks grown in vitro. Phys Rev E 75 , 021915 (2007). 

168. Sadovsky, A. J. & MacLean, J. N. Scaling of topologically similar functional modules defines     mouse primary auditory and somatosensory microcircuitry. J Neurosci 33 , 14048–14060     (2013). 

169. Yue, Q. et al. Brain modularity mediates the relation between task complexity and perfor-     mance. J Cogn Neurosci 29 , 1532–1546 (2017). 

170. Bassett, D. S. & Bullmore, E. Small-world brain networks. Neuroscientist 12 , 512–523     (2006). 


171. Rosenbaum, R., Smith, M. A., Kohn, A., Rubin, J. E. & Doiron, B. The spatial structure of     correlated neuronal variability. Nat Neurosci 20 , 107–114 (2017). 

172. Go ̃ni, J. et al. Resting-brain functional connectivity predicted by analytic measures of net-     work communication. Proceedings of the National Academy of Sciences 111 , 833–838     (2014). 

173. Honey, C. et al. Predicting human resting-state functional connectivity from structural con-     nectivity. Proceedings of the National Academy of Sciences 106 , 2035–2040 (2009). 

174. Medaglia, J. D. et al. Functional alignment with anatomical networks is associated with     cognitive flexibility. Nature Human Behaviour 2 , 156–164 (2018). 

175. Park, H.-J. & Friston, K. Structural and functional brain networks: from connections to     cognition. Science 342 , 1238411 (2013). 

176. Hodgkin, A. L. & Huxley, A. F. A quantitative description of membrane current and its     application to conduction and excitation in nerve. J. Physiol. 117 , 500–544 (1952). 

177. FitzHugh, R. Impulses and physiological states in theoretical models of nerve membrane.     Biophys. J. 1 , 445–466 (1961). 

178. Beurle, R. L. Properties of a mass of cells capable of regenerating pulses. Phil. Trans. R.     Soc. Lond. B 240 , 55–94 (1956). 

179. Wilson, H. R. & Cowan, J. D. Excitatory and inhibitory interactions in localized populations     of model neurons. Biophys. J. 12 , 1–24 (1972). 

180. Kuramoto, Y. Chemical oscillations, waves, and turbulence, vol. 19 (Springer Science &     Business Media, 2012). 

181. Cash, S. & Yuste, R. Linear summation of excitatory inputs by ca1 pyramidal neurons.     Neuron 22 , 383–394 (1999). 


182. Ferrell, J. E. & Machleder, E. M. The biochemical basis of an all-or-none cell fate switch in     xenopus oocytes. Science 280 , 895–898 (1998). 

183. Hearst, M. A., Dumais, S. T., Osuna, E., Platt, J. & Scholkopf, B. Support vector machines.     IEEE Intell. Syst. 13 , 18–28 (1998). 

184. Kleene, S. C. Representation of events in nerve nets and finite automata. Tech. Rep., RAND     PROJECT AIR FORCE SANTA MONICA CA (1951). 

185. Schmidhuber, J. Deep learning in neural networks: An overview. Neural Netw. 61 , 85–117     (2015). 

186. Egmont-Petersen, M., de Ridder, D. & Handels, H. Image processing with neural networksa     review. Pattern Recognit. 35 , 2279–2301 (2002). 

187. Hinton, G. et al. Deep neural networks for acoustic modeling in speech recognition: The     shared views of four research groups. IEEE Signal Process. Mag. 29 , 82–97 (2012). 

188. Silver, D. et al. Mastering the game of go with deep neural networks and tree search. Nature     529 , 484 (2016). 

189. Newman, C. M. Memory capacity in neural network models: Rigorous lower bounds. Neural     Netw. 1 , 223–238 (1988). 

190. Hertz, J., Krogh, A. & Palmer, R. G. Introduction to the theory of neural computation.     (Addison-Wesley/Addison Wesley Longman, 1991). 

191. Moosavi, S. A. & Montakhab, A. Structural versus dynamical origins of mean-field behavior     in a self-organized critical model of neuronal avalanches. Phys Rev E Stat Nonlin Soft Matter     Phys 92 , 052804 (2015). 

192. Woodrow, W. L. et al. Adaptation to sensory input tunes visual cortex to criticality. Nature     Physics 11 , 659–663 (2015). 


193. Haldeman, C. & Beggs, J. M. Critical branching captures activity in living neural networks     and maximizes the number of metastable states. Phys. Rev. Lett. 94 , 058101 (2005). URL     https://link.aps.org/doi/10.1103/PhysRevLett.94.058101. 

194. Beggs, J. M. & Plenz, D. Neuronal avalanches in neocortical circuits. Jour-     nal of Neuroscience 23 , 11167–11177 (2003). URL [http://www.jneurosci.](http://www.jneurosci.)     org/content/23/35/11167. [http://www.jneurosci.org/content/23/](http://www.jneurosci.org/content/23/)     35/11167.full.pdf. 

195. Kinouchi, O. & Copelli, M. Optimal dynamical range of excitable networks at criticality.     Nature Physics 2 , 348 EP – (2006). URL [http://dx.doi.org/10.1038/nphys289.](http://dx.doi.org/10.1038/nphys289.) 

196. Shew, W. L., Yang, H., Petermann, T., Roy, R. & Plenz, D. Neuronal avalanches im-     ply maximum dynamic range in cortical networks at criticality. Journal of Neuroscience     29 , 15595–15600 (2009). URL [http://www.jneurosci.org/content/29/49/](http://www.jneurosci.org/content/29/49/)     15595. [http://www.jneurosci.org/content/29/49/15595.full.pdf.](http://www.jneurosci.org/content/29/49/15595.full.pdf.) 

197. Bertschinger, N. & Natschl ̈ager, T. Real-time computation at the edge of chaos in re-     current neural networks. Neural Computation 16 , 1413–1436 (2004). URL https:     //doi.org/10.1162/089976604323057443. https://doi.org/10.1162/     089976604323057443. 

198. Ganmor, E., Segev, R. & Schneidman, E. Sparse low-order interaction network underlies     a highly correlated and learnable neural population code. Proc Natl Acad Sci U S A 108 ,     9679–9684 (2011). 

199. Lee, S.-G., Neiman, A. & Kim, S. Coherence resonance in a hodgkin-huxley neuron. Phys.     Rev. E 57 , 3292 (1998). 

200. Hille, B. et al. Ion channels of excitable membranes, vol. 507 (Sinauer Sunderland, MA,     2001). 

201. Plant, R. & Kim, M. Mathematical description of a bursting pacemaker neuron by a modifi-     cation of the hodgkin-huxley equations. Biophys. J. 16 , 227–244 (1976). 


202. Andersen, S. S., Jackson, A. D. & Heimburg, T. Towards a thermodynamic theory of nerve     pulse propagation. Prog. Neurobiol. 88 , 104–113 (2009). 

203. Pakdaman, K., Thieullen, M. & Wainrib, G. Fluid limit theorems for stochastic hybrid sys-     tems with application to neuron models. Adv. Appl. Probab. 42 , 761–794 (2010). 

204. Nagumo, J., Arimoto, S. & Yoshizawa, S. An active pulse transmission line simulating nerve     axon. Proc. IRE 50 , 2061–2070 (1962). 

205. Niebur, E. & Erd ̈os, P. Theory of the locomotion of nematodes: control of the somatic motor     neurons by interneurons. Math. Biosci. 118 , 51–82 (1993). 

206. Bryden, J. & Cohen, N. A simulation model of the locomotion controllers for the nematode     caenorhabditis elegans. In From Animals to Animats 8: Proceedings of the Eighth Interna-     tional Conference on the Simulation of Adaptive Behavior, 183–192 (MIT Press, 2004). 

207. Arena, P., Patan ́e, L. & Termini, P. S. An insect brain computational model inspired by     drosophila melanogaster: simulation results. In Neural Networks (IJCNN), The 2010 Inter-     national Joint Conference on, 1–8 (IEEE, 2010). 

208. Markram, H. The blue brain project. Nat. Rev. Neurosci. 7 , 153 (2006). 

209. Kishimoto, K. & Amari, S.-i. Existence and stability of local excitations in homogeneous     neural fields. J. Math. Biol. 7 , 303–318 (1979). 

210. Pinto, D. J. & Ermentrout, G. B. Spatially structured activity in synaptically coupled neuronal     networks: I. traveling fronts and pulses. SIAM J Appl Math 62 , 206–225 (2001). 

211. David, O. & Friston, K. J. A neural mass model for meg/eeg:: coupling and neuronal dynam-     ics. NeuroImage 20 , 1743–1755 (2003). 

212. David, O., Cosmelli, D. & Friston, K. J. Evaluation of different measures of functional     connectivity using a neural mass model. Neuroimage 21 , 659–673 (2004). 


213. Kuramoto, Y. & Araki, H. Lecture notes in physics, international symposium on mathemati-     cal problems in theoretical physics (1975). 

214. Ward, L. M. Synchronous neural oscillations and cognitive processes. Trends Cogn. Sci. 7 ,     553–559 (2003). 

215. Fries, P. A mechanism for cognitive dynamics: neuronal communication through neuronal     coherence. Trends Cogn. Sci. 9 , 474–480 (2005). 

216. Palmigiano, A., Geisel, T., Wolf, F. & Battaglia, D. Flexible information routing by transient     synchrony. Nat Neurosci 20 , 1014–1022 (2017). 

217. Schnitzler, A. & Gross, J. Normal and pathological oscillatory communication in the brain.     Nat. Rev. Neurosci. 6 , 285 (2005). 

218. Cabral, J., Hugues, E., Sporns, O. & Deco, G. Role of local network oscillations in resting-     state functional connectivity. Neuroimage 57 , 130–139 (2011). 

219. Petersson, K. M., Nichols, T. E., Poline, J.-B. & Holmes, A. P. Statistical limitations in     functional neuroimaging. i. non-inferential methods and statistical models. Philos. Trans. R.     Soc. Lond., B, Biol. Sci. 354 , 1239–1260 (1999). 

220. Petersson, K. M., Nichols, T. E., Poline, J.-B. & Holmes, A. P. Statistical limitations in     functional neuroimaging ii. signal detection and statistical inference. Philos. Trans. R. Soc.     Lond., B, Biol. Sci. 354 , 1261–1281 (1999). 

221. Bancaud, J. & Talairach, J. Methodology of stereo eeg exploration and surgical intervention     in epilepsy. Rev. Otoneuroophtalmol. 45 , 315–328 (1973). 

222. Chauvel, P., Vignal, J., Biraben, A., Badier, J. & Scarabin, J. Stereoelectroencephalography,     80–108 (Springer Verlag, 1996). 

223. Todaro, C., Marzetti, L., Valdes Sosa, P. A., Valdes-Hernandez, P. A. & Pizzella, V. Map-     ping brain activity with electrocorticography: Resolution properties and robustness of inverse     solutions. Brain Topogr Epub Ahead of Print (2018). 


224. Menon, R. S. & Kim, S.-G. Spatial and temporal limits in cognitive neuroimaging with fmri.     Trends Cogn. Sci. 3 , 207–216 (1999). 

225. Aguirre, G. K. Functional neuroimaging: technical, logical, and social perspectives. Hastings     Cent. Rep. 44 , S8–S18 (2014). 

226. Ciric, R. et al. Benchmarking of participant-level confound regression strategies for the     control of motion artifact in studies of functional connectivity. Neuroimage 154 , 174–187     (2017). 

227. Avants, B. B. et al. A reproducible evaluation of ANTs similarity metric performance in     brain image registration. Neuroimage 54 , 2033–2044 (2011). 

228. Amari, S.-i., Nakahara, H., Wu, S. & Sakai, Y. Synchronous firing and higher-order interac-     tions in neuron pool. Neural Comput. 15 , 127–142 (2003). 

229. Sizemore, A. E. et al. Cliques and cavities in the human connectome. J Comput Neurosci     Epub Ahead of Print (2017). 

230. Giusti, C., Ghrist, R. & Bassett, D. S. Two’s company, three (or more) is a simplex:     Algebraic-topological tools for understanding higher-order structure in neural data. J Comput     Neurosci 41 , 1–14 (2016). 

231. Giusti, C., Pastalkova, E., Curto, C. & Itskov, V. Clique topology reveals intrinsic geometric     structure in neural correlations. Proc Natl Acad Sci U S A 112 , 13455–13460 (2015). 

232. Reimann, M. W. et al. Cliques of neurons bound into cavities provide a missing link between     structure and function. Front Comput Neurosci 11 , 48 (2017). 

233. Battaglia, D., Witt, A., Wolf, F. & Geisel, T. Dynamic effective connectivity of inter-areal     brain circuits. PLoS Comput Biol 8 , e1002438 (2012). 

234. Zylberberg, J., Pouget, A., Latham, P. E. & Shea-Brown, E. Robust information propagation     through noisy neural circuits. PLoS Comput Biol 13 , e1005497 (2017). 


235. Kirst, C., Timme, M. & Battaglia, D. Dynamic information routing in complex networks.     Nat Commun 7 , 11061 (2016). 

236. McIntyre, C. C., Savasta, M., Kerkerian-Le Goff, L. & Vitek, J. L. Uncovering the mecha-     nism (s) of action of deep brain stimulation: activation, inhibition, or both. Clin. Neurophys-     iol. 115 , 1239–1248 (2004). 

237. Lozano, A. M. & Lipsman, N. Probing and regulating dysfunctional circuits using deep brain     stimulation. Neuron 77 , 406–424 (2013). 

238. Liu, Y.-Y. & Barab ́asi, A.-L. Control principles of complex systems. Rev. Mod. Phys. 88 ,     035006 (2016). 

239. Schiff, S. J. Neural control engineering: the emerging intersection between control theory     and neuroscience (MIT Press, 2012). 

240. Kim, J. Z. et al. Role of graph architecture in controlling dynamical networks with applica-     tions to neural systems. Nature Physics Epub Ahead of Print (2018). 

241. Gu, S. et al. Controllability of structural brain networks. Nat Commun 6 , 8414 (2015). 

242. Jeganathan, J. et al. Fronto-limbic dysconnectivity leads to impaired brain network control-     lability in young people with bipolar disorder and those at high genetic risk. Neuroimage     Clin 19 , 71–81 (2018). 

243. Muldoon, S. F. et al. Stimulation-based control of dynamic brain networks. PLoS Comput     Biol 12 , e1005076 (2016). 

244. Taylor, P. N. et al. Optimal control based seizure abatement using patient derived connectiv-     ity. Front Neurosci 9 , 202 (2015). 

245. Medaglia, J. D. et al. Network controllability in the inferior frontal gyrus relates to controlled     language variability and susceptibility to TMS. J Neurosci 38 , 6399–6410 (2018). 


246. Holt, A. B., Wilson, D., Shinn, M., Moehlis, J. & Netoff, T. I. Phasic burst stimulation: A     closed-loop approach to tuning deep brain stimulation parameters for Parkinson’s disease.     PLoS Comput Biol 12 , e1005011 (2016). 

247. Holmes, G. Disturbances of vision by cerebral lesions. The British journal of ophthalmology     2 , 353 (1918). 

248. Owen, A. M., Downes, J. J., Sahakian, B. J., Polkey, C. E. & Robbins, T. W. Planning     and spatial working memory following frontal lobe lesions in man. Neuropsychologia 28 ,     1021–1034 (1990). 

249. Walsh, V. & Cowey, A. Transcranial magnetic stimulation and cognitive neuroscience. Nat.     Rev. Neurosci. 1 , 73 (2000). 

250. Amassian, V. E. et al. Measurement of information processing delays in human visual cortex     with repetitive magnetic coil stimulation. Brain Res. 605 , 317–321 (1993). 

251. Pascual-Leone, A., Grafman, J. & Hallett, M. Modulation of cortical motor output maps     during development of implicit and explicit knowledge. Science 263 , 1287–1289 (1994). 

252. Pascual-Leone, A., Gates, J. R. & Dhuna, A. Induction of speech arrest and counting errors     with rapid-rate transcranial magnetic stimulation. Neurology 41 , 697–702 (1991). 

253. Walsh, V., Ellison, A., Battelli, L. & Cowey, A. Task–specific impairments and enhancements     induced by magnetic stimulation of human visual area v5. Proc. R. Soc. Lond., B, Biol. Sci.     265 , 537–543 (1998). 

254. Kringelbach, M. L., Jenkinson, N., Owen, S. L. & Aziz, T. Z. Translational principles of     deep brain stimulation. Nat. Rev. Neurosci. 8 , 623 (2007). 

255. George, M. S., Lisanby, S. H. & Sackeim, H. A. Transcranial magnetic stimulation: applica-     tions in neuropsychiatry. Archives of General Psychiatry 56 , 300–311 (1999). 

256. Perlmutter, J. S. & Mink, J. W. Deep brain stimulation. Annu. Rev. Neurosci. 29 , 229–257     (2006). 


257. Tass, P. et al. Detection of n: m phase locking from noisy data: Application to magnetoen-     cephalography. Phys. Rev. Lett. 81 , 3291 (1998). 

258. Santaniello, S. et al. Therapeutic mechanisms of high-frequency stimulation in parkinsons     disease and neural restoration via loop-based reinforcement. Proceedings of the National     Academy of Sciences 112 , E586–E595 (2015). 

259. Zeki, S. A vision of the brain (Blackwell Scientific Publ., 1993). 

260. Chiken, S. & Nambu, A. Disrupting neuronal transmission: mechanism of dbs? Front. Syst.     Neurosci. 8 , 33 (2014). 

261. Ber ́enyi, A., Belluscio, M., Mao, D. & Buzs ́aki, G. Closed-loop control of epilepsy by     transcranial electrical stimulation. Science 337 , 735–737 (2012). 

262. Kedzior, K. K., Gierke, L., Gellersen, H. M. & Berlim, M. T. Cognitive functioning and deep     transcranial magnetic stimulation (dtms) in major psychiatric disorders: a systematic review.     J. Psychiatr. Res. 75 , 107–115 (2016). 

263. Ching, S. et al. Real-time closed-loop control in a rodent model of medically induced coma     using burst suppression. Anesthesiology 119 , 848–860 (2013). 

264. Holt, A. B. & Netoff, T. I. Origins and suppression of oscillations in a computational model     of parkinsons disease. J. Comput. Neurosci. 37 , 505–521 (2014). 

265. Heck, C. N. et al. Two-year seizure reduction in adults with medically intractable partial     onset epilepsy treated with responsive neurostimulation: final results of the RNS System     Pivotal trial. Epilepsia 55 , 432–441 (2014). 

266. Crinion, J. et al. Spatial normalization of lesioned brains: performance evaluation and impact     on fmri analyses. Neuroimage 37 , 866–875 (2007). 

267. Santaniello, S., Fiengo, G., Glielmo, L. & Grill, W. M. Closed-loop control of deep brain     stimulation: a simulation study. IEEE Trans. Neural. Syst. Rehabil. Eng. 19 , 15–24 (2011). 


268. Iudice, F. L., Garofalo, F. & Sorrentino, F. Structural permeability of complex networks to     control signals. Nat. Commun. 6 , 8349 (2015). 

269. Posner, M. I., Snyder, C. R. & Solso, R. Attention and cognitive control. Cogn. Psychol. 205     (2004). 

270. Fuster, J. M. & Alexander, G. E. Neuron activity related to short-term memory. Science 173 ,     652–654 (1971). 

271. Goldman, P. S. & Rosvold, H. E. Localization of function within the dorsolateral prefrontal     cortex of the rhesus monkey. Exp. Neurol. 27 , 291–304 (1970). 

272. Bechara, A., Damasio, A. R., Damasio, H. & Anderson, S. W. Insensitivity to future conse-     quences following damage to human prefrontal cortex. Cognition 50 , 7–15 (1994). 

273. Dias, R., Robbins, T. & Roberts, A. Dissociation in prefrontal cortex of affective and atten-     tional shifts. Nature 380 , 69 (1996). 

274. Gu, S. et al. Optimal trajectories of brain state transitions. Neuroimage 148 , 305–317 (2017). 

275. Betzel, R. F., Gu, S., Medaglia, J. D., Pasqualetti, F. & Bassett, D. S. Optimally controlling     the human connectome: the role of network topology. Sci. Rep. 6 , 30770 (2016). 

276. Pasqualetti, F., Zampieri, S. & Bullo, F. Controllability metrics, limitations and algorithms     for complex networks. IEEE Trans. Control Network Syst. 1 , 40–52 (2014). 

277. Tang, E. et al. Developmental increases in white matter network controllability support a     growing diversity of brain dynamics. Nat. Commun. 8 , 1252 (2017). 

278. Cornblath, E. J. et al. Sex differences in network controllability as a predictor of executive     function in youth. arXiv 1801 , 04623. 

279. Tang, E. & Bassett, D. S. Control of dynamics in brain networks. Reviews of Modern Physics     In Press (2018). 


280. Adamantidis, A. R., Zhang, F., Aravanis, A. M., Deisseroth, K. & De Lecea, L. Neural     substrates of awakening probed with optogenetic control of hypocretin neurons. Nature 450 ,     420 (2007). 

281. Deisseroth, K. Optogenetics. Nat. Methods 8 , 26 (2011). 

282. Gunaydin, L. A. et al. Ultrafast optogenetic control. Nature neuroscience 13 , 387 (2010). 

283. Grosenick, L., Marshel, J. H. & Deisseroth, K. Closed-loop and activity-guided optogenetic     control. Neuron 86 , 106–139 (2015). 

284. Prakash, R. et al. Two-photon optogenetic toolbox for fast inhibition, excitation and bistable     modulation. Nat. Methods 9 , 1171 (2012). 

285. Rickgauer, J. P., Deisseroth, K. & Tank, D. W. Simultaneous cellular-resolution optical     perturbation and imaging of place cell firing fields. Nat. Neurosci. 17 , 1816 (2014). 

286. Becker, C. O., Bassett, D. & Preciado, V. M. Large-scale dynamic modeling of task-fMRI     signals via subspace system identification. J Neural Eng Epub Ahead of print (2018). 

287. Coron, J.-M. Control and nonlinearity. 136 (American Mathematical Soc., 2007). 

288. Klickstein, I., Shirin, A. & Sorrentino, F. Locally optimal control of complex networks. Phys.     Rev. Let. 119 , 268301 (2017). 

289. Haynes, G. & Hermes, H. Nonlinear controllability via lie theory. SIAM J. Control 8 , 450–     460 (1970). 

290. Sussmann, H. J. & Jurdjevic, V. Controllability of nonlinear systems. Differ. Equ. 12 , 95–116     (1972). 

291. Hermann, R. & Krener, A. Nonlinear controllability and observability. IEEE Trans. Automat.     Contr. 22 , 728–740 (1977). 

292. Cornelius, S. P., Kath, W. L. & Motter, A. E. Realistic control of network dynamics. Nat.     Commun. 4 , 1942 (2013). 


293. Whalen, A. J., Brennan, S. N., Sauer, T. D. & Schiff, S. J. Observability and controllability     of nonlinear networks: The role of symmetry. Phys. Rev. X 5 , 011005 (2015). 

294. Isidori, A. Nonlinear control systems (Springer Science & Business Media, 2013). 

295. Chopra, N. & Spong, M. W. On exponential synchronization of kuramoto oscillators. IEEE     Trans. Automat. Contr. 54 , 353–357 (2009). 

296. Lynn, C. W. & Lee, D. D. Statistical mechanics of influence maximization with thermal     noise. EPL 117 , 66001 (2017). 

297. Lynn, C. W. & Lee, D. D. Maximizing activity in ising networks via the tap approximation.     In Association for the Advancement of Artificial Intelligence, 679–686 (2018). 

298. Amunts, K. & Zilles, K. Architectonic mapping of the human brain beyond Brodmann.     Neuron 88 , 1086–1107 (2015). 

299. Cohen, M. R. & Kohn, A. Measuring and interpreting neuronal correlations. Nat Neurosci     14 , 811–819 (2011). 

300. van den Heuvel, M. P. & Sporns, O. Rich-club organization of the human connectome. J     Neurosci 31 , 15775–15786 (2011). 

301. Stiso, J. & Bassett, D. S. Spatial embedding imposes constraints on the network architectures     of neural systems. arXiv 1807 , 04691 (2018). 

302. van den Heuvel, M. P., Bullmore, E. T. & Sporns, O. Comparative connectomics. Trends     Cogn Sci 20 , 345–361 (2016). 

303. Persichetti, A. S., Aguirre, G. K. & Thompson-Schill, S. L. Value is in the eye of the be-     holder: early visual cortex codes monetary value of objects during a diverted attention task.     J Cogn Neurosci 27 , 893–901 (2015). 

304. Dore, B. P. et al. Brain activity tracks population information sharing by capturing consensus     judgments of value. Cereb Cortex Aug 28 (2018). 


305. Constantinescu, A. O., O’Reilly, J. X. & Behrens, T. E. J. Organizing conceptual knowledge     in humans with a gridlike code. Science 352 , 1464–1468 (2016). 

306. Papadopoulos, L., Porter, M. A., Daniels, K. E. & Bassett, D. S. Network analysis of particles     and grains. Journal of Complex Networks 6 , 485–565 (2018). 

307. Bianconi, G., Rahmede, C. & Wu, Z. Complex quantum network geometries: Evolution and     phase transitions. Phys Rev E Stat Nonlin Soft Matter Phys 92 , 022815 (2015). 

308. Kivel, M. et al. Multilayer networks. J. Complex Netw. 2 , 203–271 (2014). 

309. De Domenico, M., Granell, C., Porter, M. A. & Arenas, A. The physics of spreading pro-     cesses in multilayer networks 12 , 901–906 (2016). 

310. Newman, M. E. J. & Clauset, A. Structure and inference in annotated networks. Nature     Communications 7 , 11863 (2016). 

311. Bassett, D. S., Wymbs, N. F., Porter, M. A., Mucha, P. J. & Grafton, S. T. Cross-linked     structure of network evolution. Chaos 24 , 013112 (2014). 

312. Porter, M. A., Onnela, J.-P. & Mucha, P. J. Communities in networks. Notices of the AMS     56 , 1082–1097 (2009). 

313. Fortunato, S. Community detection in graphs. Physics reports 486 , 75–174 (2010). 

314. Fortunato, S. & Hric, D. Community detection in networks: A user guide. Physics Reports     659 , 1–44 (2016). 

315. Gosak, M. et al. Network science of biological systems at different scales: A review. Phys     Life Rev 24 , 118–135 (2018). 

316. Richiardi, J. et al. Correlated gene expression supports synchronous activity in brain net-     works. Science 348 , 1241–1244 (2015). 

317. Romero-Garcia, R. et al. Structural covariance networks are coupled to expression of genes     enriched in supragranular layers of the human cortex. Neuroimage 171 , 256–267 (2018). 


318. Whitaker, K. J. et al. Adolescence is associated with genomically patterned consolidation of     the hubs of the human brain connectome. Proc Natl Acad Sci U S A 113 , 9105–9110 (2016). 

319. Hardingham, G. E., Pruunsild, P., Greenberg, M. E. & Bading, H. Lineage divergence of     activity-driven transcription and evolution of cognitive ability. Nat Rev Neurosci 19 , 9–15     (2018). 

320. Luke, D. A. & Harris, J. K. Network analysis in public health: history, methods, and appli-     cations. Annu Rev Public Health 28 , 69–93 (2007). 

321. Braun, U. et al. From maps to multi-dimensional network mechanisms of mental disorders.     Neuron 97 , 14–31 (2018). 

322. Schmalzle, R. et al. Brain connectivity dynamics during social interaction reflect social     network structure. Proc Natl Acad Sci U S A 114 , 5153–5158 (2017). 

323. Parkinson, C., Kleinbaum, A. M. & Wheatley, T. Similar neural responses predict friendship.     Nat Commun 9 , 332 (2018). 

324. Parkinson, C., Liu, S. & Wheatley, T. A common cortical metric for spatial, temporal, and     social distance. J Neurosci 34 , 1979–1987 (2014). 

325. Falk, E. B. & Bassett, D. S. Brain and social networks: Fundamental building blocks of     human experience. Trends Cogn Sci 21 , 674–690 (2017). 

326. Rieke, F., Warland, D., de Ruyter van Steveninck, R. & Bialek, W. Spikes: exploring the     neural code (MIT Press, 1997). 

327. Cover, T. M. & Thomas, J. A. Elements of information theory (John Wiley & Sons, 2012). 

328. Shannon, C. E. A mathematical theory of communication. Bell Syst. Tech. J. 27 (1948). 

329. MacKay, D. M. & McCulloch, W. S. The limiting information capacity of a neuronal link.     Bull. Math. Biophys. 14 , 127–135 (1952). 


330. Attneave, F. Some informational aspects of visual perception. Psychol. Rev. 61 , 183 (1954). 

331. Barlow, H. B. Possible principles underlying the transformations of sensory messages (1961). 

332. van Steveninck, R. d. R. & Bialek, W. Real-time performance of a movement-sensitive neu-     ron in the blowfly visual system: coding and information transfer in short spike sequences.     Proc. R. Soc. Lond. B 234 , 379–414 (1988). 

333. Strong, S. P., Koberle, R., van Steveninck, R. R. d. R. & Bialek, W. Entropy and information     in neural spike trains. Phys. Rev. Lett. 80 , 197 (1998). 

334. Paninski, L. Estimation of entropy and mutual information. Neural Comput. 15 , 1191–1253     (2003). 

335. Nemenman, I., Bialek, W. & van Steveninck, R. d. R. Entropy and information in neural     spike trains: Progress on the sampling problem. Phys. Rev. E 69 , 056111 (2004). 

336. Schreiber, T. Measuring information transfer. Phys. Rev. Lett. 85 , 461 (2000). 

337. Vicente, R., Wibral, M., Lindner, M. & Pipa, G. Transfer entropy—a model-free measure of     effective connectivity for the neurosciences. J. Comput. Neurosci. 30 , 45–67 (2011). 

338. Jaynes, E. T. Information theory and statistical mechanics. Phys. Rev. 106 , 620 (1957). 

339. Kailath, T. Linear Systems (Prentice-Hall, Inc., 1980). 

340. Liu, Y.-Y., Slotine, J.-J. & Barab ́asi, A.-L. Controllability of complex networks. Nature 473 ,     167–173 (2011). 

341. Klickstein, I., Shirin, A. & Sorrentino, F. Energy scaling of targeted optimal control of     complex networks. Nat. Commun. 8 , 15145 (2017). 

342. Yan, G. et al. Network control principles predict neuron function in the Caenorhabditis     elegans connectome. Nature 550 , 519–523 (2017). 


Acknowledgements We are grateful to Lia Papadopoulos, Jason Z. Kim, and Vivek Buch for helpful comments on an earlier version of this manuscript. We also thank Ann E. Sizemore for artistic inspiration. D.S.B. and C.W.L. acknowledge support from the John D. and Catherine T. MacArthur Foundation, the Alfred P. Sloan Foundation, the ISI Foundation, the Paul Allen Foundation, the Army Research Laboratory (W911NF-10-2-0022), the Army Research Office (Bassett-W911NF-14-1-0679, Grafton-W911NF-16-10474, DCISTW911NF-17-2-0181), the Office of Naval Research, the National Institute of Mental Health (2-R01-DC-009209-11, R01-MH112847, R01-MH107235, R21-M MH-106799), the National Institute of Child Health and Human Development (1R01HD086888-01), National Institute of Neurological Disorders and Stroke (R01 NS099348), and the National Science Foundation (BCS-1441502, BCS-1430087, NSF PHY-1554488 and BCS-1631550). We also thank Vecteezy for supplying vector art. 

Competing interests The authors declare no competing interests. 

Corresponding author Correspondence and requests for materials should be addressed to D.S.B. (dsb@seas.upenn.edu). 



# Theoretical Neuroscience
### [Theoretical Neuroscience](https://boulderschool.yale.edu/sites/default/files/files/DayanAbbott.pdf)
#### Contents

1. Neural Encoding I: Firing Rates and Spike Statistics 
2. Neural Encoding II: Reverse Correlation and Visual Receptive Field
3. Neural Decoding
4. Information Theory
5. Model Neurons I: Neuroelectronics
6. Model Neurons II: Conductances and Morphology
7. Network Models
8. Plasticity and Learning
9. Classical Conditioning and Reinforcement Learning
10. Representational Learning
#### Preface
- Theoretical analysis and computational modeling are important tools for characterizing what nervous systems do, determinging how they function, and understanding why they operate in particular ways. Neuroscinece encompasses approaches ranging from molecular and cellular studies to human psychophysics and psychology. Theoretical neuroscience encourages crosstalk among these subdisciplines by constructing compact represenations of what has been learned, building bridges between different levels of description, and identifying unifying concepts and principles. In this book, we present the basic methods used for these purposes and discuss examples in which theoretical approaches have yielded insight into nervous system function.   

---

- Neurons are remarkable among the cells of the body in their ability to propagate signals  rapidly over large sdistances. They do this by generating characteristic electrical pulses (action potentials) or more simply spikes that can travel down nerve fibers. Neurons represent and transmit information by firing sequences of spikes in various temporal patterns. The study of neural coding involves measuring and characterizing how stimulus attributes such as light or sound intensity, or motor actions, such as direction of an arm movement, are represented by action potentials. The link between stimulus and response can be studied from two opposite points of view. Neural encoding refers to the map from stimulus to response. Neural decoding refers to the reverse map, from response to stimulus, and the challenge is to reconstruct a stimulus, or certain aspects of that stimulus, from the spike sequences it evokes. 

---

### Properties of Neurons

- Neurons are highly specialized for generating electrical signals in response to chemical and other inputs, and transmitting them to other cells. Some important morphological specializations are the dendrites that receive inputs from other neurons and the axon that carries the neuronal output to other cells. The elaborate branching structure of the dendritic tree allows a neuron to receive inputs from many other neurons through synaptic connections. The cortical pyramidal neuron and the cortical interneuron each receiive thousands of synaptic inputs, and for the cerebellar Purkinje cell the number is over 100,000. Axons from single neurons can traverse large fractions of teh brain or, in some cases, of the entier body.

- Along with these morphological features, neurons have physiological specializations. Most prominent among these are a wide variety of membrane-spanning ion channels that allow ions, predominantly sodium (Na+), potassium (K+), calcium (Ca2+), and chloride (Cl-), to move into and out of the cell. Ion channels control the flow of ions across the cell membrane by opening and closing in response to voltage changes and to both internal and external signals.

- The electrical signal of relevance to the nervous system is the differnce in electrical potential between the interior of a neuron and the surrounding extracellular medium. Under resting conditions, the potental inside the cell membrane of a neuron is about -70mV relative to that of the surrouding bath (which is conventionally defined to be 0mV), and the cell is said to be polerized. Ion pumps located in the cell membrane maintain concentration gradients that support his membrane potential difference. For example, Na+ is much more concentrated outside a neruon than inside it, and the concetration of K+ is significantly higher inside the neuron than in the extracellular medium. Ions thus flow into and out of a cell due to both voltage and concentration gradiesnt. Current in the form of positively charge ions flowing out of the cell (or negatively charged ions flowing into the cell) through open channels makes the membran potential more negative, a process called hyperpolarization. Current flowing into the cell changes the membrane potential to less negative or even positive values. This is called depolarization.

- If a neuron is depolarized sufficiently to raise the membrane potential above a threshold level, a positive feedback process is initiated, and the neuron generates an action potential. An action potential is roughly 100mV fluctuation in the electrical potential across the cell membrane that lasts for about 1ms. Action potental generation also depends on the recent history of cell firing. For a few milliseconds just after an action potential has been fired, it may be virtually impossible to initiate another spike. This is called the absolute refractory period. For a longer interval know as the relative refractory period, lasting up to tes of milliseconds after a spike, it is more difficult to evoke an action potential.

- Action potentials are of great importance because they are the only form of membrane potential fluctuations that can propagate over large distances. Subthreshold potential fluctuations are severly attenuated over distances of 1 mm or less. Action potentials are on the other hand are regenerated actively along axon processes and can travel rapidly over large distances without attenuation.
- Axons terminate at synapese where the voltage transient of the action potential opens ion channels, producting an influx of Ca2+ that leads to the release of a neurotransmitter. The neurotransmitter binds to receptors at the signal-receiving or postsynaptic side of the synapse, causing ion-conducting channels to open. Depending on the nature of the ion flow, the synapses can have either an excitatory, depolarizing, or an inhibitory, typically hyperpolarizing, effect on the postsynaptic neuron.

### Recording Neural Responses

- Membrane potentials are measured intracellularly by connecting a hollow glass electrode filled with a conducting electrolyte to a neuron, and comparing the potential it records with that of a reference electrode placed in the extracellular medium. Intracellular recordings are made either with sharp electrodes inserted through the membrane into the cell, or patch electrodes that have broader tips and are sealed tightly to the surface of the membrane. After the patch electrode selals, the membrane beneath its tip is either broken or perforated, providing electrical contact witht he interior of the cell. The recording show rapid spikes riding on top of a more slowly varying subthreshold potential. The bottom trace is a schematic of an intracelluar recording makde some distance out on the axon of the neuron. These traces are drawings, not real recordings; such intracellular axon recordings, although possible in some types of cells, are difficult and rare. Intracellular recordings from the soma are the norm, but intracellular dendritic recordings are increasingly being made as well. The subthreshold membrane potential waveform, apparent in the soma recording, is completely absent on the axon due to attenuation, but the action potential sequence in the two recordings is the same. This illustrates the important point that spikes, but not subthreshold potentials, propagate regeneratively down axons.

---

### From Stimulus to Response

#### - Characterizing the relationship between stimulus and response is difficult because neuronal responses are complex and variable. Neruons typically respond by producing complex spike sequences that reflect both the intrinsic dynamics of the neuron and the temporal characteristics of the stimulus. Isolating features of the response that encode changes in the stimulus can be difficult, especially if the time scale for these changes is of the same order as teh average interval between spikes. Neural responses can vary from trial to trial even when the same stimulus is presented repeatedly. There are many potential sources of this variability, including variable levels of arousal and attention, randomness associated with various biophysical processes that affect neuronal firing, and the effects of other cognitive processes taking place during a trial. The complexity and trial-to-trial variability of action potential sequences make it unlikely that we can describe and predict the timing of each spike deterministically. Instead, we seek a model that can account for the probabilities that different spike sequences are evoked by a specific stimulus.

-Typically, many neurons respond to a given stimulus, and stimulus features are therefore encoded by the activites of large neural populations. In studying population coding, we must examine not only the firing patterns of individual neurons but also the relationships of these firing patterns to each other across the populations of responding cells.

---
### Spike Trains and Firing Rates

- Action potentials convey information throught their timing. Although action potentials can vary somewhat in duration, amplitude, and shape, they are typically treated as identical stereotyped events in neural encoding studies. If we ignore the brief duration of an action potential (about 1 ms), an action potential sequence can be characterized simply by a list of the time when spikes occurred. For *n* spikes, we denote these times by *ti* with times when spikes occurred. For *n* spikes, we denote these times *ti* with *i*=1,2,...*n*. The trial during which the spikes are recorded is taken to start at time 1 and end at time T, so 0<_*ti*<-T for all *i*. The spike sequence can also be represented as a sum of infinitesimally narrow, idealized spikes in the form of Dirac $\delta, functions. 


























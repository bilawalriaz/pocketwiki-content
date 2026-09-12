# Brain–computer interface

A brain–computer interface (BCI) is a direct communication link between the brain's electrical activity and an external device, such as a computer cursor, robotic limb, or speech synthesizer. BCIs bypass the body's normal output channels (nerves and muscles), reading neural signals and translating them into commands. Because the brain can rewire itself through cortical plasticity, users can learn to treat a prosthesis as if it were a natural limb.

## How signals are acquired

BCIs differ mainly in how close the electrodes sit to brain tissue:

- **Non-invasive:** EEG (electroencephalography, electrical signals through the scalp), MEG (magnetoencephalography, magnetic fields from neural activity), and fMRI (functional MRI, measuring blood-flow changes). No surgery; signals are noisier.
- **Partially invasive:** ECoG (electrocorticography, a thin pad of electrodes on the brain's surface under the skull) and endovascular arrays (stent-mounted electrodes placed inside blood vessels near the cortex). Better signal quality than EEG, lower risk than penetrating the brain.
- **Invasive:** Microelectrode arrays inserted into the grey matter record action potentials (the brief electrical spikes neurons use to communicate) from individual or small groups of neurons. Best signal quality, but scar-tissue build-up and electrode rejection degrade recordings over time.

## Functional classes

By purpose, BCIs split into three:

- **Active:** the user deliberately modulates neural activity (e.g. motor imagery, imagined movement, or focused attention) to issue commands such as moving a cursor or a robotic arm.
- **Passive:** the system continuously reads brain state (workload, fatigue, attention) and adapts without conscious user effort.
- **Reactive:** the system decodes automatic brain responses to external stimuli, such as event-related potentials (brief, time-locked EEG deflections triggered by a specific event), falling between active and passive.

## A short history

Hans Berger recorded the first human EEG in 1924, identifying alpha waves (rhythmic 8–13 Hz oscillations over the resting brain). Jacques Vidal coined the term "brain–computer interface" in a 1973 paper and demonstrated EEG-based cursor control in 1977. In 1988, researchers first moved a physical robot using EEG. The mid-1990s saw the first implanted neuroprosthetics in humans, and the field grew quickly after 2010 as non-invasive recording improved. Thorsten Zander formalised the passive BCI concept in 2011.

## Key milestones in humans and animals

- 1969: Eberhard Fetz showed monkeys could learn to control a biofeedback arm by modulating neural firing rates, the first operant conditioning of cortical neurons (rewarding the animal for producing a target pattern of activity).
- 1998: Johnny Ray, who had locked-in syndrome (complete paralysis with intact awareness) after a brainstem stroke, received the first implant that restored neural output from a paralysed patient and learned to move a cursor.
- 2005: Matt Nagle, tetraplegic (paralysed in all four limbs), controlled a robotic hand with a 96-electrode BrainGate array, the first long-term human trial.
- 2011: A rhesus monkey controlled a virtual arm while receiving sensory feedback through cortical stimulation.
- 2021: A paralysed man with anarthria (inability to speak despite intact language comprehension) decoded speech at roughly 15 words per minute; a separate Stanford system decoded imagined handwriting at about 18 words per minute, or 86 characters per minute.
- 2023: Two studies reached 62 and 78 words per minute using recurrent neural networks (networks with feedback loops, well suited to sequential data like speech) to decode speech.
- 2020–2023: The Stentrode, a stent-mounted electrode array threaded into a vein next to the motor cortex, allowed paralysed patients to text, email, and shop wirelessly without open brain surgery; a one-year trial reported no serious adverse events in four patients.

## Technical challenges

The central problem is signal stability. Chronic (long-term implanted) microelectrodes provoke glial scarring (accumulation of immune cells that wall off the electrode, degrading the signal), blood-brain barrier leakage, and gradual signal loss. Recordings that begin at hundreds of microvolts often fade as the body encapsulates the foreign material. Research focuses on flexible electrode materials, wireless "neural dust" sensors, and improved coatings to extend recording lifespans. Optogenetic interfaces (using light-gated ion channels, proteins that open or close in response to light, to control specific neurons) have shown promise in animal research.

## Applications

- **Communication:** spelling, speech synthesis, and handwriting decoding for people with ALS (amyotrophic lateral sclerosis, a progressive neurodegenerative disease causing total paralysis) or locked-in syndrome.
- **Motor restoration:** cursor and robotic-arm control, and EEG-based systems that promote motor recovery after stroke by reinforcing correct movement imagery.
- **Sensory restoration:** cochlear implants (over 736,900 recipients worldwide) and experimental retinal and visual-cortex implants that produce phosphenes (small points of perceived light) to restore a crude sense of sight.
- **Rehabilitation and assessment:** BCI for stroke recovery, disorder-of-consciousness diagnosis, and functional brain mapping during neurosurgery.
- **Consumer and gaming:** low-cost EEG headsets from NeuroSky, Emotiv, and open-source boards have brought BCI into entertainment, though motor-imagery control remains slow and requires extensive training.

Ethical debates focus on informed consent for users who cannot easily communicate, long-term safety, neural-data privacy, potential coercion or "brain hacking," and the line between therapy and cognitive enhancement.

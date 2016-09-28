P1
===

Good afternoon everyone. I am Han. I am very honored to be here at the 10 year anniversary of JMN, giving a presentation about my little interesting master project. The role of hippocampal neuron degeneration, dendritic atrophy, and neurogenesis in depression onset and rescue. And I did a numeric study on this topic.

Also I want to express my gratitude to my supervisor Prof. Stefan Rotter and tutor Ms. Julia Gallinaro in Bernstein Center Freiburg.

P2
===

Depression is among top 5 disease burden, and is potentially fatal. So it attracts mounting public attention and academic interest.

Among all studies concerning risk factors and brain mechanisms, the plasticity hypothesis stands out as the possible converging mechanism.

P3
===

It is reported in animal models of depression and post-mortem brain slices of depressive patients, that stressors could influence neuroplasticity in the hippocampus and lead to depression. On the other hand, treatments like antidepressants and electroconvulsive therapy could restore hippocampal neuroplasticity and rescue depressive symptoms.

P4
===

And to specify a bit, hippocampal neuroplasticity includes: hippocampal volume, synaptic changes like long term potenciation and depression, dendritic morphological change like shrinkage of dendritic tree, or neuron population size.

P5
===

For example, stressors trigger depression by causing dendritic atrophy in CA3 pyramidal cells, inhibiting neurogenesis in the dentate gyrus and causing neuron degeneration. Treatments rescue depression by inducing neurogenesis in the dentate gyrus.

P6
===

It is really intriguing. From the view of computational neuroscience, adding new items or eliminating existing items from a network, changing input strength and connection strength between neurons could definitely change the network dynamics and plasticity. So how about looking at depression from the view of network dynamics?


P7
===

Let's first look at the anatomic structure in the hippocampus.
CA3 is a recurrent network, with connections between inhibitory neurons and excitatory neurons. It receives inputs from entorhinal cortex and granule cells in the dentate gyrus.

P8
===

We hypothesize that dendritic atrophy in CA3 and neuron degeneration in the dentate gyrus will influences network dynamics and plasticity in CA3. Neurogenesis in the dentate gyrus will rescue CA3 dynamics and plasticity.

P9
===

The next step is to build numeric models. I used NEST to run large scale neuron network simulation, and I used leaky integrate and fire neuron model, Brunel network model and both static and STDP synapse model.

P10
===

This graph illustrates my experiment design, entorhinal cortex sends spike trains to the dentate gyrus and CA3, CA3 is sparsely connected, granule cells in the dentate gyrus also send connections to excitatory neurons in the CA3.

P11
===

When neuron degeneration happens, the granule cell number decreases 60 neurons per 6 seconds. When dendritic atrophy happens, the synaptic weight from dentate gyrus to CA3 excitatory neurons decreases to 90% per 6 seconds.


P12
===

When neurogenesis happens, granule cell number increases 100 neurons per 6 seconds, and new granule cells are more excitable, so they form stronger connections.

P13
===

This is my simulation timeline. I simulated the initial network for 120s, then I started neuron degeneration and dendritic atrophy for 180s. This part is onset. Later I simulated the current network for 120s, followed by 180s neurogenesis. And this is called rescue.

P14
===

To analyze the CA3 network dynamics, I used this graph. The upper part is raster plot. The x axis is time, y axis is neuron ID. This figure plots which neuron fires at which time point. The lower panel is PSTH. The x axis is again time, y axis is neuron number. This figure plots how many neuron fire in each time window. And to quantify the network dynamics, I calculated firing rate and correlation coefficient. Correlation coefficient is the index of synchronicity.

To analyze plasticity, I calculated the mean synaptic weights of excitatory neurons in CA3. The synaptic weight is the amplitude of post synaptic current.

P15
===

Soon I am going to show you an animation about how neuron degeneration influences network activities. Please note when you see a red arrow, it means neuron degeneration happens.

It is clear that neuron degeneration makes the network fire less intensively and less synchronously.

P16
===

When we quantify the firing activity, it also shows decrease in firing rate and correlation coefficient when neuron degeneration or dendritic atrophy happens.

P17
===

The same decrease is also observed in mean synaptic weights. So network dynamics and plasticity are both influenced by dendritic atrophy and neuron degeneration.

And now I am going to show you another animation, how neurogenesis rescues the network dynamics from neuron degeneration. When you see the red arrow, it means neurogenesis starts.

P18
===

At the beginning, the network is not very active. With neurogenesis happens, the network is firing more intensively and correlated.

P19
===

Again I quantified the network activity, and increase in firing rate and correlation is observed.

P20
===

The same increase is also observed in mean synaptic weights. So network dynamics and plasticity are rescued by neurogenesis.

P21
===

To summarize a bit, no matter it is dendritic atrophy, neuron degeneration, or neurogenesis, they influence the input strength from the dentate gyrus to the CA3. And we confirmed that it will change the dynamics and plasticity in CA3 from different directions.

This is also partially supported by empirical studies in depressive cases. Decreased activity is observed in hippocampus in depressive patients. And when increasing activation of the dentate gyrus, stress-related symptoms could be alleviated.

But our current simulation is over simplified, I didn't include back-projections from CA3 to the dentate gyrus, and from CA2 to CA3, and I didn't simulate maturation process of the newly generated granule cells. In fact immature dentate gyrus endophynotype has dramatic impact on psychiatric disorder.

so we are expecting to make a more elaborate network in the future and use other models like structural plasticity to cross-validate the results.

P22
===

So that is my presentation for today. I want to thank you for your attention and thank JMN for providing me the opportunity to present here and also for providing me, a psychologist, the opportunity to study real neuroscience.

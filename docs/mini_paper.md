## Abstract
Spiking neuron models vary in their trade-offs between biological realism and
computational efficiency. In this work, three widely used neuron models—the
Leaky Integrate-and-Fire (LIF), Izhikevich, and Hodgkin–Huxley models—are
implemented and compared under identical stimulation conditions. The models
are evaluated based on their ability to reproduce biologically meaningful
spiking behavior and their computational cost. The results demonstrate that
the Izhikevich model provides an effective balance between realism and efficiency,
supporting the arguments presented by Izhikevich (2004).

## Introduction
Computational models of spiking neurons play a central role in understanding
neural dynamics and large-scale brain simulations. Simple models such as the
Leaky Integrate-and-Fire neuron are computationally efficient but biologically
limited, while detailed biophysical models like Hodgkin–Huxley provide accurate
action potential dynamics at the cost of high computational complexity.

Izhikevich (2004) proposed a neuron model that captures diverse cortical firing
patterns while remaining computationally inexpensive. This project aims to
empirically evaluate these trade-offs by implementing and comparing LIF,
Izhikevich, and Hodgkin–Huxley neuron models using consistent input conditions.

## Methods
Three neuron models were implemented using Python and simulated using numerical
integration.

The LIF model was implemented as a first-order differential equation describing
membrane potential dynamics with a fixed firing threshold.

The Izhikevich model was implemented using two coupled differential equations
representing membrane potential and recovery variables, with parameters chosen
to reproduce regular spiking behavior.

The Hodgkin–Huxley model was implemented using four differential equations
describing membrane potential and voltage-gated ion channel dynamics. Due to
its biophysical detail, a significantly smaller time step was required.

All models were driven using comparable external current stimulation to allow
qualitative and computational comparison.

## Results
The LIF model produced regular spiking behavior but lacked spike shape diversity
and adaptation. The Hodgkin–Huxley model generated biologically realistic action
potentials with detailed depolarization and repolarization phases but required
high computational resources.

The Izhikevich model successfully reproduced biologically meaningful spiking
patterns while maintaining computational efficiency close to that of the LIF
model. Runtime measurements showed that the Hodgkin–Huxley model was
significantly slower than both LIF and Izhikevich models.

## Discussion and Conclusion
This comparative study demonstrates the fundamental trade-off between biological
realism and computational efficiency in spiking neuron models. While the
Hodgkin–Huxley model provides detailed biophysical accuracy, its computational
cost limits its scalability. The LIF model, though efficient, fails to capture
rich neuronal dynamics.

The Izhikevich model emerges as a practical compromise, offering biologically
relevant behavior with minimal computational complexity. These findings align
closely with the conclusions of Izhikevich (2004) and highlight the importance
of model selection in computational neuroscience research.

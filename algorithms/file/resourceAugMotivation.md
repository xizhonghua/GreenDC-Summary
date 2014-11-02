## Motivation of Resource Augmentation

### Motivation
- If some algorithms have bad worst-case performance, but they seem to perform reasonably well over a wide range of inputs, then resource augmentation may explain this phenomenon.
- It is common for systems to posses the following informally defined **threshold property**
  - The input or input distributions are parameterized by a load &lambda;, and the server is parameterized by a capacity &mu;. The QoS provided by the server is reasonable if the load &lambda; is at most 90% of the server capacity &mu;, and the QoS is horrible if &lambda; is more than 110% of &mu;.

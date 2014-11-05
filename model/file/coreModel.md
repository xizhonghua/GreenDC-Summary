## Power Model of Processor


### Model
- Ref: [[Haque-2013]](../../papers/Haque13_energy-aware-task-replication.md)
- The power model is considered in previous reliability-aware power management research [[Sridharan-2010]](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=5523628&tag=1). The power consumption of each core consists of static and dynamic powr components.
  - the static power P<sub>s</sub>: 
    - is determined mainly by the leakage current of the system;
  - the dynamic power P<sub>d</sub> includes:
    - a frequency-dependent power component (determined by voltage and frequency levels); and
    - a frequency-independent power component P<sub>ind</sub>, driven by the modules such as memory and I/O subsystem in the active state.
- In DVS technique, the supply voltage is scaled in almost linear fashion with the processing frequency. Consequently, the power consumption of a core can be approximated by
  - P<sub>active</sub> = P<sub>s</sub> + P<sub>ind</sub> + C<sub>e</sub>f^3
  - where C<sub>e</sub> is a system-dependent constant, reflecting the effective switching capacitance.
- When a core is not executing any task (idle state), its power consumption is primarily determined by the static power. We assume that the static power consumption can only be eliminated by the complete power-down of the core.

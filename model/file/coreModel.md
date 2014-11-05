## Power Model of Processor

- Ref: [[Haque-2013]](../../papers/Haque13_energy-aware-task-replication.md)

### Model
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


### Observation
- Existing research indicates that arbitrary slowing down a task is not always energy-efficient [[Fan-2005]](http://link.springer.com/chapter/10.1007%2F978-3-540-28641-7_12) [[Jejurikar-2004]](http://dl.acm.org/citation.cfm?id=996650) [[Zhu-2004]](http://dl.acm.org/citation.cfm?id=1112252), due to the frequency-independent power components. In other words, there is a processing frequency below which the total consumption increases. 
  - This frequency is called *energy efficient frequency* and denoted by f<sub>ee</sub>
  - f<sub>ee</sub> can be computed analytically through the well-known techniques [[Jejurikar-2004]](http://dl.acm.org/citation.cfm?id=996650), [[Zhu-2004]](http://dl.acm.org/citation.cfm?id=1112252).

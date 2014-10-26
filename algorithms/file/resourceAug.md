## Resource Augmentation

### Definition
- (1+&epsilon;)-speed augmentation
  - it means if a processor can run at power P and speed s, then the online algorithm can run the processor at power p and speed (1+&epsilon;)s.

### Procedure
My summary from paper [[Pruhs-2010]](../../papers/PruhsS10_schedule-energy.md)
- First, create an lower bound instance.
- Then, refecting on this lower bound instance, once notices that if the processors used by the online algorithm were only slightly more energy efficient, then the online algorithm could be competitive on this instances.
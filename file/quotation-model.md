## Quotation Model

- Ref: [[Keskinocak-2001]](http://www2.tepper.cmu.edu/andrew/ravi/ms01.pdf)

### Terms
- SLTQ: scheduling and reliable lead-time quotation

### Model
- Quotation (Q-SLTQ)
  - the decision about accepting/rejecting an order must be made and a lead time must be quoted *immediately* when the order arrives
- Delayed Quotation (D-SLTQ)
  - the decisions about accepting/rejecting an order and lead-time quotation have to ba made within *q* time units afte the order arrives, when *q* is smaller than the maximum acceptable lead time.
  
### Algorithms
- O-HRR: Online Highest Remaining Revenue first
- O-HUR: Online Hihgest Unit Revenue first
- Q-FRAC: Quotation FRACtional revenue
  - only schedule the jobs that have revenue exceed &alpha; l
- O-HYBRID: a combine of O-1HRR and O-HRR
- O-GAP: leaving the machine free for at least &beta; fraction of the time

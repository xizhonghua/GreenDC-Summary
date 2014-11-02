## Wegithed Response

### Definition
- Each job J<sub>i</sub> has an associated positive weight w<sub>i</sub> that is revealed to the clairvoyant scheduler at the release time r<sub>i</sub>. 
- The objective is function is \sum w<sub>i</sub> F<sub>i</sub> where F<sub>i</sub> is the response time.

### Characteristic
- [[Buccgetti-2001]](http://link.springer.com/chapter/10.1007%2F3-540-44666-4_8#page-1) showed that besides being a sufficient condition, local c-competitive is a necessary condition for an online algorithm to be c-competitive. 
  - The idea is that if an online algorithm was ever worse than locally c-competitive at some time, then the adversary could then bring a stream of dense short jobs that contribute little to the weighted response if they are processed as they arrive, but will increase the weighted response tremendously if they are delayed at all. 
- There is no O(1)-competitive algorithm for weighted response.

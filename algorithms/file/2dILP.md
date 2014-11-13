## 2D Bin Packing ILP

- Ref [[Beasley-1985]](http://www.jstor.org/stable/170866)


### Problem Model
- A large stock rectangle A<sub>0</sub> = (L<sub>0</sub>, W<sub>0</sub>) of length L<sub>0</sub> and width W<sub>0</sub> is to be cut into m smaller rectangular pieces; piece i has size (L<sub>i</sub>, W<sub>i</sub>) and value v<sub>i</sub>
  - Let P<sub>i</sub> and Q<sub>i</sub> be the minimum number of pieces of type i that cna be cut from A<sub>0</sub>.

### Define
- x<ipq> = 1 if a piece of type i is cut with its bottom left-hand corner at (p,q) where 0 &le; p &le; L<sub>0</sub>- L<sub>i</sub> and 0 &le; q &le; W<sub>0</sub>- W<sub>i</sub>

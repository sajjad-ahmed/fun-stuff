## finding softmax in python using numpy array
The softmax function equation goes like this:
![](http://latex.codecogs.com/gif.latex?S%28yi%29%3D%5Cfrac%7Be%5E%7Byi%7D%7D%7B%5Csum_%7Bj%7De%5E%7Byj%7D%7D)

If we define a funtion which takes a  np array `x` and returns the softmax of that array, then the code for that softmax function would look like this
```python
def softmax(x):
    _exp = np.exp(x)
    _sum=np.sum(np.exp(x),axis=0)
    ans = _exp / _sum
    return ans
```
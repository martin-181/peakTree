# peakTree.py

Small python script that finds multiple peaks in a given array. Subpeaks are stored in a tree structure.
Originally intended for atmospheric research cloud radar Doppler spectra, but also useful for other application.

### Usage

```python
import peakTree
peaks, pt, threslist = peakTree.detect_peak_recursive(data_array, threshold, lambda thres: thres*1.5)
```

Internally following steps are employed:
```python
pt.insert(peak, thres)
pt.concat()
pt.extendedges()
print(pt)
```



### License
Copyright 2017, Martin Radenz
[MIT License](http://www.opensource.org/licenses/mit-license.php)
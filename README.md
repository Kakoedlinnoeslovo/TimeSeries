# TimeSeries

We provide own pytorch wrap

base: 
  - network      # BaseNet : provide get_trainable and get_restorable methods
  - layers       # Layer   : provide get_trainable and get_restorable methods
  - reader       # Reader  : wrap for pytorch dataset, need to use file configuration
  - transform    # provide a numpy and putorch version of non parametric, non trainable transformation
  - writer       # adapter to tensorboard
  - installer    # use it when you want download and parse your specific dataset  

contrib:
  - utils
  - shape_utils
train            # lr save_num num epoch optimizer config  
test             # num config  
config           # all configuration  

You have to build your model inheriting from a BaseNet, after that you must describe your model in __init__ method,   
also you must create your own reader inheriting Reader and create your own Dataset class inheriting from Dataset  
  
Then you can launch training and testing by   
  - python3.6 train.py <parameters>  
  - python3.6 test.py <parameters>  
  
Our wiki:  
https://github.com/DELTA37/TimeSeries/wiki/Articles  

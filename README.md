# CNTK-faster-rcnn
This project aims to help getting started with running the Faster RCNN CNTK
examples since the base CNTK images require additional setup.

# Using the images
To use the CPU or GPU image just go into the `cpu` or `gpu` directory and type:

```
docker build .
docker run --rm -it -v `pwd`:`pwd` -w `pwd` hashfrombuild bash
```

or (for GPU):

```
nvidia-docker build .
nvidia-docker run --rm -it -v `pwd`:`pwd` -w `pwd` hashfrombuild bash
```

# Running the examples
If you want to run the examples that come with CNTK, you'll need to make sure
the dataset is downloaded first:

```
cd /cntk/Examples/Image/Detection/FastRCNN
python install_data_and_model.py
```

Then you can run the example(s):

```
cd /cntk/Examples/Image/Detection/FastRCNN
python run_fast_rcnn.py
```

or

```
cd /cntk/Examples/Image/Detection/FasterRCNN
python run_faster_rcnn.py
```


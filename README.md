# orbslam2_with_dense_map
This is a modified ORB_SLAM2 (from https://github.com/raulmur/ORB_SLAM2) with a online point cloud map module running in RGB-D mode. You can visualize your point cloud map during the SLAM process. 

# How to Install
First compile the modified g2o:

```
  cd g2o_with_orbslam2
  mkdir build
  cd build
  cmake ..
  make 
```

Following the instructions from the original g2o library: [https://github.com/RainerKuemmerle/g2o] if you have dependency problems. I just add the extra vertecies and edges provided in ORB_SLAM2 into g2o. 

Then compile the ORB_SLAM2. You need firstly to compile the DBoW2 in ORB_SLAM2_modified/Thirdpary, and then the Pangolin module (https://github.com/stevenlovegrove/Pangolin). Finally, build ORB_SLAM2:
there should be a file in ORB_SLAM2_modified/Vcabulory named "ORBvoc.txt"  but it too big to upload so just download it from original ORB-SLAM2 https://github.com/raulmur/ORB_SLAM2.
```
cd ORB_SLAM2_modified
mkdir build
cd build
cmake ..
make
```



# Run examples
Prepare a RGBD camera or dataset, give the correct parameters and you can get a ORB SLAM with point cloud maps

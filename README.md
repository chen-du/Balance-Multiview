# Balance-Multiview
 
This dataset contains 6,348,768 synchronized 2D body landmark frames and corresponding center of pressure measurements for balance-related movement captured from four different camera views.

This dataset includes data from 20 healthy adults. During the collection phase, each subject stood on the force plate with no shoes using 1) feet side-by-side and 2) feet-in-tandem (i.e., heel-to-toe) postures. We instructed subjects to perform random movements, e.g., from rigid standing to body swaying, involving the trunk, arms, hands, or bending knees. The only specified requirement was not to move the feet; we provided no specific instructions about the action patterns.

The video was collected by four RGB cameras using a resolution of 640 x 480 pixels at 30 fps, while the center of pressure was recorded at 60 Hz using a force plate. Please refer to the following publication for more details.

## File format
2D_Bodylandmark contains the 2D body landmarks; the shape of data is N (frames) * 17 (joints) * 2 (dimensions). The body landmark was estimated by Detectron2 (https://github.com/facebookresearch/detectron2). The Cam 001 - 004 correspond to the Cam A - D in the following publication.

CenterOfPressure contains the corresponding center of pressure measurements (x, y) in centimeters (cm) for each frame; the shape of the data is N (frames) * 2 (dimensions).

CAM_01_04_stereoParams.mat contains the stereoParams between Cam_001 (Cam-A) and Cam_004 (Cam-D) estimated by MATLAB Stereo Camera Calibrator (https://www.mathworks.com/help/vision/ref/stereocameracalibrator-app.html) using a checkerboard calibration pattern.

*The dataset was processed using pickle 4.0

## Citation

If you make use of the dataset, please consider citing the following references in any publications:

Chen Du, Sarah Graham, Colin Depp, and Truong Nguyen. "View-invariant Center-of-pressure Metrics Estimation with Monocular RGB Camera." IEEE Transactions on Multimedia (2022).


## Contact
If you have any questions, please contact c9du@ucsd.edu

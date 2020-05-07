# Image Stitching 

Installing Dependencies:

The code is written in python and tested on version 3.6
To install the dependencies
```
pip install -r requirements.txt

```

To run the code
```
python imageStitching.py left_image_path right_image_path
```

More detailed running instructions:
```
usage: python imageStitching.py [-h]
                                [--harris_neighbourhood_size HARRIS_NEIGHBOURHOOD_SIZE]
                                [--harris_keypoint_threshold HARRIS_KEYPOINT_THRESHOLD]
                                [--descriptor DESCRIPTOR] [--patch_size PATCH_SIZE]
                                [--n_matches N_MATCHES]
                                [--matching_method MATCHING_METHOD]
                                [--RANSAC_iterations RANSAC_ITERATIONS]
                                [--RANSAC_init_points RANSAC_INIT_POINTS]
                                [--RANSAC_inlier_threshold RANSAC_INLIER_THRESHOLD]
                                [--no_gui NO_GUI] [--wandb WANDB]
                                [--results_file RESULTS_FILE]
                                left_image_path right_image_path

positional arguments:
  left_image_path       Path to first image in the pair
  right_image_path      Path to second image in the pair

optional arguments:
  -h, --help            show this help message and exit
  --harris_neighbourhood_size HARRIS_NEIGHBOURHOOD_SIZE
                        Number of pixels in the harris neighbourhood
  --harris_keypoint_threshold HARRIS_KEYPOINT_THRESHOLD
                        Harris keypoint selection threshold
  --descriptor DESCRIPTOR
                        Type of descriptor to choose: sift |
                        pixel_neighbourhood
  --patch_size PATCH_SIZE
                        Patch size, ignore for sift since it does it by
                        default
  --n_matches N_MATCHES
                        Number of top matches to choose for RANSAC
  --matching_method MATCHING_METHOD
                        Method to use for matching between the keypoints
  --RANSAC_iterations RANSAC_ITERATIONS
                        Number of iterations to run for RANSAC
  --RANSAC_init_points RANSAC_INIT_POINTS
                        Number of starting points to choose for RANSAC
  --RANSAC_inlier_threshold RANSAC_INLIER_THRESHOLD
                        Threshold to choose inliers for RANSAC
  --no_gui NO_GUI       Set to false for no display
  --wandb WANDB         Weights and Biases integration for experiment tracking
  --results_file RESULTS_FILE
                        Path to sensitivity analysis results
```

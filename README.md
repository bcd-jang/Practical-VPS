# Practical-VPS
This repository provides datasets for visual localization, specifically created for an indoor visual positioning system with multi-view queries. These datasets are intended to support the development of visual localization algorithms.
You can download our datasets here.

## Dataset Description
There are two datasets, labeled 'ENG' and 'Church,' respectively. Each dataset contains two folders: 'Database' and 'Query.' The structure of the datasets is as follows:

### Database folder
  - alignments: The transformation matrix of the front-facing frame that captured the scanning trajectory. It is represented as a 1 by 16 array, where each set of four values corresponds to a column in a 4 by 4 matrix.
  - cutouts: The database contains images and depth data, organized by frame in folders named [frame.surface.-]. Each frame consists of three surfaces, labeled as follows: 0 for right, 1 for left, and 4 for front.
  - pcd: 3D point cloud data for the specified location 

### Query folder
  - multiple-image: The multi-view query images are each named in the format [frame.surface.jpg]. Each frame consists of four surfaces, labeled as follows: 0 for right, 1 for left, 4 for front, and 5 for rear.
  - ground_truth.txt: This file contains the 6-DoF ground truth poses for each query image. Each entry is formatted as [query name, position (x, y, z), quaternion (w, x, y, z)], where position (x, y, z) represents the translation vector (in meters) from the world coordinate system to the camera coordinate system, and quaternion (w, x, y, z) specifies the camera’s orientation relative to the world coordinate system as a unit quaternion.

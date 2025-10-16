import os
import cv2

# Dataset base path
base_path = r"D:\data_set"

# Subfolder paths
resource_path = os.path.join(base_path, "resource")
segmentation_path = os.path.join(base_path, "segmentation")
annotation_path = os.path.join(base_path, "annotation")
lit_path = os.path.join(base_path, "lit")

# Check if folders exist
print("Resource exists:", os.path.exists(resource_path))
print("Segmentation exists:", os.path.exists(segmentation_path))

# Load one image for testing
for img_file in os.listdir(resource_path):
    if img_file.endswith(('.jpg', '.png', '.jpeg')):
        img = cv2.imread(os.path.join(resource_path, img_file))
        cv2.imshow("Sample Eye Image", img)
        cv2.waitKey(0)
        cv2.destroyAllWindows()
        break

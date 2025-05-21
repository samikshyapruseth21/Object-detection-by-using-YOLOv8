# Self-Driving Car Object Detection using OpenCV and Python

This project demonstrates object detection for self-driving car systems using classical computer vision techniques with Python and OpenCV. It utilizes a labeled dataset of driving scenes to visualize bounding boxes around detected objects.

## 📁 Dataset Source

The dataset used is publicly available on Kaggle:  
👉 [Self-Driving Cars - Dataset on Kaggle](https://www.kaggle.com/datasets/alincijov/self-driving-cars)

## 🧪 What This Notebook Does

The notebook walks through:
- Loading and visualizing the dataset.
- Drawing bounding boxes for various objects detected in traffic scenes.
- A step-by-step demonstration using OpenCV and `matplotlib`.

---

## 📦 Requirements

Before running the notebook, install the required packages:

```bash
pip install opencv-python matplotlib pandas scikit-learn
```

---

## 🗂️ File Structure

- `oBJECT_detection.ipynb`: Jupyter notebook with full implementation.
- `labels_train.csv`: Contains bounding box coordinates and class labels.
- `README.md`: Project overview and usage instructions.
- `/img/your_image.jpg`: Example image for testing (replace with your own).

---

## ▶️ How to Run

1. **Clone the Repository or Download Files**
   ```bash
   git clone <your-repo-url>
   cd your-repo-folder
   ```

2. **Prepare Your Image**
   Place an image in your project directory (e.g., `img/sample.jpg`).

3. **Modify the Notebook**
   In the notebook, update the source code like this:

   ```python
   img = cv2.imread("img/sample.jpg")
   results[i][0] = "img/sample.jpg"
   ```

4. **Plot the Image with Bounding Boxes**
   After assigning the image path, the notebook will visualize it using:

   ```python
   fig, ax = plt.subplots(1, 1, figsize=(15, 8))
   ax.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))

   for row in results[i][1:]:
       x, y, w, h = int(row[1]), int(row[2]), int(row[3]), int(row[4])
       ax.add_patch(Rectangle((x, y), w, h, linewidth=2, edgecolor='r', facecolor='none'))
   ```

---

## 🧠 Object Detection Logic

- Each image has multiple annotations representing objects like vehicles, pedestrians, and road signs.
- Coordinates from the CSV file are used to draw bounding boxes.
- The script uses `matplotlib.patches.Rectangle` for drawing.

---

## 📷 Example Visualization

![Sample Result](img/sample_result.jpg)  
*Example of a driving scene with annotated bounding boxes*

---

## 📌 Notes

- Make sure to shuffle the dataset before plotting.
- All coordinates are based on the top-left origin convention.
- The images and annotations must match by filename.

---

## 💡 Inspiration

Inspired by the practical needs of autonomous vehicle perception systems, this project showcases how basic vision tools can simulate complex object detection pipelines.

## AUTHOR
- Samikshya Pruseth 

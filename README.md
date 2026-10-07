# 2d-game-transformation-engine
# 🎮 2D Game Transformation Engine (F3)

## 📌 Project Overview

The **2D Game Transformation Engine** is a mathematical visualization project that demonstrates how **matrix multiplication and transformation composition** are used in 2D games.

A triangle representing a game sprite is transformed using three operations:

1. **Scaling** – changes the size of the object.
2. **Rotation** – rotates the object by a given angle.
3. **Translation** – moves the object to a new position.

The transformations are performed step by step and also combined into a single transformation matrix.

---

## 🎯 Problem Statement

In a 2D game, a sprite may need to be resized, rotated, and moved on the screen.

This project demonstrates how these operations can be represented using matrices and composed into one transformation:

$$
\boxed{Total = T \times R \times S}
$$

where:

* **S** = Scaling Matrix
* **R** = Rotation Matrix
* **T** = Translation Matrix

The final transformation is applied to a triangle using homogeneous coordinates.

---

## 🧮 Mathematical Concepts Used

### 1. Homogeneous Coordinates

Each 2D point is represented as:

$$
P =
\begin{bmatrix}
x\\
y\\
1
\end{bmatrix}
$$

The additional `1` allows translation to be represented using matrix multiplication.

### 2. Scaling

The scaling matrix is:

$$
S =
\begin{bmatrix}
s & 0 & 0\\
0 & s & 0\\
0 & 0 & 1
\end{bmatrix}
$$

For this project:

$$
s = 2
$$

### 3. Rotation

The rotation matrix is:

$$
R =
\begin{bmatrix}
\cos\theta & -\sin\theta & 0\\
\sin\theta & \cos\theta & 0\\
0 & 0 & 1
\end{bmatrix}
$$

For this project:

$$
\theta = 45^\circ
$$

### 4. Translation

The translation matrix is:

$$
T =
\begin{bmatrix}
1 & 0 & t_x\\
0 & 1 & t_y\\
0 & 0 & 1
\end{bmatrix}
$$

For this project:

$$
t_x = 3,\qquad t_y = 2
$$

---

## 🔄 Transformation Process

The original triangle is:

* A = `(0, 0)`
* B = `(2, 0)`
* C = `(1, 2)`

The transformation sequence is:

```text
Original Triangle
       ↓
    Scaling
       ↓
    Rotation
       ↓
   Translation
       ↓
  Final Triangle
```

Mathematically:

$$
P' = T(R(SP))
$$

Therefore:

$$
\boxed{P' = (T \times R \times S)P}
$$

---

## 📊 Project Parameters

| Parameter        |    Value |
| ---------------- | -------: |
| Scale            |      2.0 |
| Rotation Angle   |      45° |
| Translation X    |      3.0 |
| Translation Y    |      2.0 |
| Shape            | Triangle |
| Number of Points |        3 |

---

## 💻 Technologies Used

* **Python**
* **NumPy**
* **Matplotlib**
* Matrix multiplication
* Homogeneous coordinates

---

## 📦 Required Libraries

Install the required libraries using:

```bash
pip install numpy matplotlib
```

If you are using **Google Colab**, these libraries are generally already available.

---

## ▶️ How to Run

### Option 1: Google Colab

1. Open Google Colab.
2. Create a new notebook.
3. Copy the Python code into a code cell.
4. Run the cell.
5. View the matrices, coordinates, and graphs.

### Option 2: Python

Save the program as:

```text
game_transformation.py
```

Then run:

```bash
python game_transformation.py
```

---

## 📈 Visualization

The program produces four visualizations:

### 1. Original Triangle

Shows the triangle before any transformation.

### 2. Scaled Triangle

Shows the triangle after scaling by a factor of **2**.

### 3. Rotated Triangle

Shows the scaled triangle after a **45° rotation**.

### 4. Final Triangle

Shows the triangle after scaling, rotation, and translation.

The final transformation is:

```text
T × R × S
```

---

## 🔍 Verification

The project performs an important verification.

It calculates the result in two ways:

### Method 1 — Step by Step

```text
Scaling → Rotation → Translation
```

### Method 2 — Combined Matrix

```text
T × R × S
```

The program compares both results.

If they are equal, it displays:

```text
✓ Step-by-step result = Combined matrix result
✓ Transformation composition is correct!
```

This confirms that the matrix composition has been implemented correctly.

---

## 🌍 Real-World Application

Matrix transformations are widely used in:

* 🎮 2D games
* 🖥️ Computer graphics
* 🎬 Animation
* 🤖 Robotics
* 📱 User-interface graphics
* 🗺️ Coordinate transformations
* 🎨 Image processing

For example, when a game character moves, rotates, or changes size, transformation matrices can be used to calculate its new position and orientation.

---

## ⭐ Why This Project Is Useful

This project connects a mathematical concept from linear algebra with a practical application in game development.

It demonstrates that:

> **Matrix multiplication can be used to perform and combine graphical transformations efficiently.**

---

## 🧠 Learning Outcomes

After completing this project, we can understand:

* What a transformation matrix is.
* How homogeneous coordinates work.
* How scaling is represented using matrices.
* How rotation is represented using matrices.
* How translation is represented using matrices.
* How matrix multiplication combines transformations.
* Why the order of transformations matters.
* How mathematics is applied in 2D game development.

---

## 📁 Project Structure

```text
2D-Game-Transformation-Engine/
│
├── game_transformation.py
├── README.md
└── output/
    └── transformation_visualization.png
```

---

## 🏆 Conclusion

The **2D Game Transformation Engine** successfully demonstrates the use of **matrix multiplication and transformation composition** in a real-world game-development scenario.

A simple triangle is:

$$
\boxed{\text{Scaled} \rightarrow \text{Rotated} \rightarrow \text{Translated}}
$$

and the same result is obtained using:

$$
\boxed{Total = T \times R \times S}
$$

The verification step confirms that both approaches produce the same final coordinates.

### 🎮 Project Theme

**Mathematics + Matrices + Computer Graphics + Game Development**

---

## 👥 Team

**Project:** 2D Game Transformation Engine
**Project Code:** F3
**Subject:** Mathematics
**Topic:** Matrix Multiplication & Transformation Composition

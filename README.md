# Wildfire_Boundary_Detection
Design and Analysis of algorithm project on Wildfire boundary detection using Convex Hull - Divide &amp; Conquer method by Yashika Vashist

##  **Project Overview**

This project demonstrates **Wildfire Boundary Detection** using the **Divide and Conquer Convex Hull Algorithm** — a classic computational geometry problem applied to a real-world disaster analysis scenario.

The algorithm identifies the **outermost boundary** (convex hull) that encloses all detected wildfire hotspots. This helps in **predicting fire spread regions**, **resource allocation**, and **visualizing disaster impact areas**.

##  **Concept Used — Convex Hull (Divide & Conquer Approach)**

The **Convex Hull** of a set of points is the smallest convex polygon that contains all the points.  
In this project:
- Each hotspot represents a fire-detected location.
- The Convex Hull forms the **fire boundary**, enclosing all hotspots.

### **Divide & Conquer Steps**
1. **Divide** — Split all hotspot points into left and right halves (based on longitude).  
2. **Conquer** — Compute convex hulls for each half separately.  
3. **Merge** — Combine both hulls to form the final outer wildfire boundary.

This approach improves efficiency from **O(n³)** (brute force) to **O(n log n)**.



## **Algorithm **

1. **Generate Random Hotspots:**  
   Random (x, y) coordinates simulate wildfire detection points.

2. **Sort Points:**  
   Sort by X-axis to divide the region into Western and Eastern halves.

3. **Compute Convex Hulls:**  
   - Left Hull → Western Fire Boundary  
   - Right Hull → Eastern Fire Boundary  
   - Merged Hull → Overall Wildfire Spread

4. **Visualize Data:**  
   - Plot points, hulls, and merged boundaries with Matplotlib.  
   - Add glowing hotspots and gradient hull effects for clarity.

5. **Display Statistics:**  
   - Total hotspots  
   - Region-wise division  
   - Hull vertices  
   - Final merged boundary



## **Algorithm Complexity**
| Operation | Time Complexity |
|------------|-----------------|
| Sorting (by x-coordinate) | O(n log n) |
| Convex Hull (per half) | O(m log m) |
| Merge Hulls | O(n) |
| **Overall** | **O(n log n)** |


## **Tech Stack**
- **Language:** Python  
- **Libraries:**  
  - `numpy` — numerical computation  
  - `matplotlib` — data visualization  
  - `scipy.spatial.ConvexHull` — convex hull algorithm
  - 'random'-to generate random hotspots


```bash

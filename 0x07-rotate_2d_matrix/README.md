To perform a 2D rotation in Python, you can use trigonometric functions like `cos` and `sin` to calculate the new coordinates after rotation. The rotation formula for a point `(x, y)` around the origin `(0, 0)` by an angle `theta` in a counter-clockwise direction is:

```
x' = x * cos(theta) - y * sin(theta)
y' = x * sin(theta) + y * cos(theta)
```

Here's a Python code example demonstrating how to perform a 2D rotation using this formula:

```python
import math

def rotate_point(point, angle):
    x, y = point
    angle_rad = math.radians(angle)
    new_x = x * math.cos(angle_rad) - y * math.sin(angle_rad)
    new_y = x * math.sin(angle_rad) + y * math.cos(angle_rad)
    return new_x, new_y

# Example usage
original_point = (2, 3)
rotation_angle_deg = 45

new_point = rotate_point(original_point, rotation_angle_deg)
print(f"Original Point: {original_point}")
print(f"Rotated Point: {new_point}")
```

In this example, the `rotate_point` function takes a point `(x, y)` and an angle in degrees, and returns the new rotated point `(new_x, new_y)`.

Keep in mind that this rotation is around the origin `(0, 0)`. If you need to rotate around a different point `(cx, cy)`, you would first translate the point to be rotated by subtracting `(cx, cy)`, then perform the rotation, and finally translate the point back by adding `(cx, cy)` to the rotated point.

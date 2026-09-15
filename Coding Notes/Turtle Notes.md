# Python Turtle Graphics: Complete Learning Guide

This GitHub-ready Markdown guide provides a structured breakdown of Python's `turtle` graphics library for study and quick reference.

---

## 1. Core Overview & Mental Model
* **Turtle graphics** is an implementation of geometric drawing tools originally introduced in **Logo** in 1967 by Wally Feurzeig, Seymour Papert, and Cynthia Solomon [1].
* In Python, turtle graphics models a physical **robotic turtle** with a pen that moves across a 2D **x-y plane**, starting at coordinates `(0, 0)` facing East [2-4].
* It provides **immediate visual feedback**, making it an effective educational tool for introducing core programming concepts [3, 5].
* It also allows programmers to produce graphical output without introducing complex external libraries [3].

---

## 2. Setup & Execution Modes

### System Requirements & Imports
* The module requires the **Tk interface package (`tkinter`)** to be installed on your system [4, 6].
* **Procedural Approach:** Functions are imported directly into the global namespace via `from turtle import *` [4, 5, 7].
* **Standard Namespace Import:** To avoid name collisions in larger scripts, use `import turtle as t` [7, 8].
* **Object-Oriented Approach:** Instantiate `Turtle` and `Screen` objects directly for full control and multiple turtles [9-11].

### Script Execution & Mainloop
* Standalone scripts must include `mainloop()` (or `done()`) at the end so the graphic window stays open until dismissed [8, 9, 12].

```python
# Procedural Quick Start
from turtle import *

forward(100)
left(120)
forward(100)
mainloop()
```

```python
# Standard Scripting Approach (Recommended)
import turtle as t

t.forward(100)
t.left(120)
t.forward(100)
t.mainloop()
```

```python
# Object-Oriented Approach
from turtle import Screen, Turtle

screen = Screen()
pen = Turtle()

pen.forward(100)
pen.left(120)
pen.forward(100)

screen.mainloop()
```

---

## 3. Motion & Positioning Reference

### Movement & Rotation
* **`forward(distance)` / `fd(distance)`**: Moves forward by `distance` pixels [13, 14].
* **`backward(distance)` / `bk(distance)` / `back(distance)`**: Moves backward by `distance` pixels [13-15].
* **`right(angle)` / `rt(angle)`**: Rotates clockwise by `angle` degrees [13, 15].
* **`left(angle)` / `lt(angle)`**: Rotates counter-clockwise by `angle` degrees [13, 16].

### Absolute Coordinates & Orientations
* **`goto(x, y)` / `setpos(x, y)` / `setposition(x, y)`**: Moves directly to coordinates `(x, y)`, drawing a line if pen is down [13, 16, 17].
* **`teleport(x, y)`**: Moves turtle to `(x, y)` **without drawing a line**, introduced in Python 3.12 [13, 17-19].
* **`setx(x)` / `sety(y)`**: Updates x or y coordinate independently [13, 19].
* **`setheading(to_angle)` / `seth(to_angle)`**: Sets orientation heading [13, 19, 20].
  * **Standard Mode (Default):** 0° = East, 90° = North, 180° = West, 270° = South [20, 21].
  * **Logo Mode:** 0° = North, 90° = East, 180° = South, 270° = West [20, 21].
* **`home()`**: Moves turtle to origin `(0, 0)` and resets heading [13, 20].

### Shapes & Curves
* **`circle(radius, extent=None, steps=None)`**: Draws a circle or arc [13, 20, 22].
  * `radius`: Positive draws counter-clockwise; negative draws clockwise [22].
  * `extent`: Angle arc to draw (e.g., `180` for semicircle) [22, 23].
  * `steps`: Number of steps for regular inscribed polygon approximation [22, 23].
* **`dot(size=None, color=None)`**: Draws a filled circular dot [13, 23, 24].

### State Queries
* **`pos()` / `position()`**: Returns current location tuple `(x, y)` [13, 25].
* **`xcor()` / `ycor()`**: Returns current x or y coordinate [13, 26, 27].
* **`heading()`**: Returns current angle heading [13, 27].
* **`distance(x, y)`**: Returns distance to specified point or another turtle [13, 28].

---

## 4. Pen & Color Control

### Pen State
* **`penup()` / `pu()` / `up()`**: Lifts pen up so moving draws no line [13, 29, 30].
* **`pendown()` / `pd()` / `down()`**: Lowers pen down to resume drawing [13, 29, 30].
* **`pensize(width)` / `width(width)`**: Sets line thickness [13, 29, 30].
* **`isdown()`**: Returns `True` if pen is down, `False` if up [13, 31].

### Color Control
* **`pencolor(color)`**: Sets pen line color [13, 32].
* **`fillcolor(color)`**: Sets shape fill color [13, 33].
* **`color(pencolor, fillcolor)`**: Sets both pencolor and fillcolor simultaneously [13, 34, 35].
* **`colormode(cmode)`**: Sets color mode to `1.0` (floats between 0.0-1.0) or `255` (integers between 0-255) [21, 33, 36].

Acceptable color formats include strings (e.g., `"red"`), hex codes (e.g., `"#33cc8c"`), or RGB tuples [32, 33].

### Shape Filling Methods

#### Standard Method (`begin_fill` / `end_fill`)
```python
import turtle as t

t.color("black", "red")
t.begin_fill()
t.circle(80)
t.end_fill()
```
* **`begin_fill()`**: Called immediately before drawing a closed shape [13, 37, 38].
* **`end_fill()`**: Fills the enclosed area drawn since `begin_fill()` was called [5, 13, 37, 38].

#### Context Manager Method (Python 3.14+)
```python
import turtle as t

t.color("black", "red")
with t.fill():
    t.circle(80)
```
* **`fill()`**: Context manager introduced in **Python 3.14** that automatically handles starting and ending shape fills [6, 7, 38, 39].

---

## 5. Window, Canvas & Animation Control

### Screen Management
* **`bgcolor(color)`**: Sets screen background color [40-42].
* **`bgpic(picname)`**: Sets background image (`.png`, `.gif`, `.pgm`, `.ppm`) [40, 43].
* **`clearscreen()` / `screen.clear()`**: Erases drawings and removes turtles [40, 44, 45].
* **`resetscreen()` / `screen.reset()`**: Resets all turtles on screen to default state [40, 46].
* **`setup(width, height, startx, starty)`**: Sets window dimensions and position [40, 47, 48].
* **`title(titlestring)`**: Sets window title text [40, 49].
* **`save(filename, overwrite=False)`**: Saves canvas output as PostScript file (**Python 3.14+**) [40, 47].

### Animation Speed & Updates
* **`speed(speed)`**: Sets animation speed from `1` (slowest) to `10` (fastest) [13, 25, 50].
  * **`speed(0)`**: Turns off animation completely for instant jumping/turning [25].
* **`tracer(n, delay)`**: Disables or sets screen update intervals to speed up rendering [40, 51].
* **`update()`**: Manually updates screen when `tracer` animation updates are suppressed [40, 52].
* **`no_animation()`**: Context manager introduced in **Python 3.14** to temporarily disable turtle animations inside a code block [51, 53].

```python
# Instant rendering pattern (Python 3.14+)
with screen.no_animation():
    for dist in range(2, 400, 2):
        pen.fd(dist)
        pen.rt(90)
```

---

## 6. Event Handling & Interactivity

### Mouse Events
* **`onclick(fun)`**: Binds function to mouse clicks on a turtle or screen [13, 40, 54, 55].
* **`onrelease(fun)`**: Binds function to mouse button release events [13, 56, 57].
* **`ondrag(fun)`**: Binds function to mouse drag events on a turtle [13, 57, 58].

### Keyboard Events
* **`listen()`**: Sets focus on screen to collect key events [40, 52].
* **`onkey(fun, key)` / `onkeyrelease(fun, key)`**: Binds function to key release [40, 52, 59, 60].
* **`onkeypress(fun, key)`**: Binds function to key press [40, 55, 59, 60].

### GUI Input Dialogs
* **`textinput(title, prompt)`**: Pops up dialog requesting string input [40, 61].
* **`numinput(title, prompt, default, minval, maxval)`**: Pops up dialog requesting numerical input [40, 61, 62].

```python
# Interactive Keyboard Example
from turtle import Turtle, Screen

screen = Screen()
pen = Turtle()

def move_forward():
    pen.forward(50)

screen.onkey(move_forward, "Up")
screen.listen()
screen.mainloop()
```

---

## 7. Custom Shapes & Appearance

### Built-in Shapes
* Initial built-in shapes: `"arrow"`, `"turtle"`, `"circle"`, `"square"`, `"triangle"`, `"classic"` [63].
* Set shape using `shape(name)` [13, 63].

### Custom Shape Registration
* **Image Shapes:** `register_shape("filename.png")` registers image shapes (PNG, GIF, PGM, PPM supported in Python 3.14) [40, 64-66]. *Note: Image shapes do not rotate with turtle heading [65].*
* **Polygon Shapes:** `register_shape("shape_name", polygon_tuple)` registers coordinate tuples [40, 65, 66].
* **Compound Shapes:** Constructed using `Shape("compound")` and `addcomponent()` [13, 67-69].

---

## 8. Demo Scripts
Python includes built-in demo scripts demonstrating turtle capabilities [70, 71]. Run the demo viewer from your terminal:

```bash
python -m turtledemo
```

---

*Would you like me to create flashcards, a quiz, or a tailored report to help you study and test your knowledge on Python Turtle graphics?*

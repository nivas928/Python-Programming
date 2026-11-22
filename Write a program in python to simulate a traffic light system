import turtle
import time

# Screen Setup
wn = turtle.Screen()
wn.title("Traffic Light with Timer")
wn.bgcolor("black")
wn.tracer(0) # Updates screen faster

# Draw the Frame
frame = turtle.Turtle()
frame.color("white")
frame.width(3)
frame.hideturtle()
frame.penup()
frame.goto(-50, 180)
frame.pendown()
for _ in range(2):
    frame.forward(100)
    frame.right(90)
    frame.forward(300)
    frame.right(90)

# Create Lights
def make_light(y, color):
    light = turtle.Turtle()
    light.shape("circle")
    light.shapesize(3)
    light.color("gray")
    light.penup()
    light.goto(0, y)
    return light

red_light = make_light(120, "red")
yellow_light = make_light(30, "yellow")
green_light = make_light(-60, "green")

# Timer Display
timer_pen = turtle.Turtle()
timer_pen.hideturtle()
timer_pen.color("white")
timer_pen.penup()
timer_pen.goto(70, 0) # Timer position next to lights

def run_timer(seconds, active_light, light_color):
    active_light.color(light_color)
    for i in range(seconds, 0, -1):
        timer_pen.clear()
        timer_pen.write(f"  {i}s", font=("Arial", 24, "bold"))
        wn.update()
        time.sleep(1)
    active_light.color("gray")

# Main Loop
try:
    while True:
        run_timer(5, red_light, "red")       # Red for 5s
        run_timer(5, green_light, "green")   # Green for 5s
        run_timer(2, yellow_light, "yellow") # Yellow for 2s
except:
    print("Simulation closed.")

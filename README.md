import math
from turtle import *
def heart_x(k):
return 15 * math.sin(k)**3
def heart_y(k):
return 12*math.cos(k) - 5*math.cos(2*k) - 2*math.cos(3*k) - math.cos(4*k)
# Drawing speed (medium)
speed(5)
# Background and pen settings
bgcolor('black')
color("#F55AA2")
penup()
# Draw heart curve
for i in range(6000):
x = heart_x(i/50) * 20
y = heart_y(i/50) * 20
goto(x, y)
pendown()
# Return to center
penup()
goto(0, 0)
# Write "B" on left side
goto(-120, 20)
color("white")
write("B", align="center", font=("Arial", 36, "bold"))
# Write "N" on right side
goto(120, 20)
write("N", align="center", font=("Arial", 36, "bold"))
hideturtle()
done()

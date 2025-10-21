# 五星红旗
import turtle
screen = turtle.Screen()
screen.setup(900, 600)
screen.bgcolor("white")
t = turtle.Turtle()
t.speed(0)
t.penup()
t.goto(-300, 200)
t.pendown()
t.color("red")
t.begin_fill()
for _ in range(2):
    t.forward(600)
    t.right(90)
    t.forward(400)
    t.right(90)
t.end_fill()
t.penup()
t.goto(-250, 150)
t.pendown()
t.color("yellow")
for _ in range(5):
    t.forward(60)
    t.right(144)
small_stars = [(-180, 180, 20, 30), (-160, 150, 20, 0), (-160, 110, 20, 330), (-180, 80, 20, 300)]
for x, y, size, angle in small_stars:
    t.penup()
    t.goto(x, y)
    t.pendown()
    t.setheading(angle)
    t.color("yellow")
    for _ in range(5):
        t.forward(size)
        t.right(144)
t.hideturtle()
turtle.mainloop()

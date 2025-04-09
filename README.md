from turtle import *

# إعداد شاشة الرسم
screen = Screen()
screen.title("علم فلسطين")
screen.bgcolor("white")

def draw_rectangle(color_name, x, y, width, height):
    penup()
    goto(x, y)
    pendown()
    color(color_name)
    begin_fill()
    for _ in range(2):
        forward(width)
        right(90)
        forward(height)
        right(90)
    end_fill()

def draw_triangle(color_name, points):
    penup()
    goto(points[0])  # النقطة الأولى
    pendown()
    color(color_name)
    begin_fill()
    goto(points[1])  # النقطة الثانية
    goto(points[2])  # النقطة الثالثة
    goto(points[0])  # العودة إلى النقطة الأولى لإغلاق المثلث
    end_fill()


# رسم المستطيل الأسود
draw_rectangle("black", -150, 100, 300, 67)

# رسم المستطيل الأبيض
draw_rectangle("white", -150, 33, 300, 67)

# رسم المستطيل الأخضر
draw_rectangle("green", -150, -33, 300, 67)
# رسم المثلث الأحمر
draw_triangle("red", [(-150, 100), (-150, -100), (-50, 0)])

# كتابة نص الدعم
penup()
goto(-80, -150)
pendown()
color("red")
write("#Save_Palestine", font=('Verdana', 15, 'bold'))

# إنهاء الرسم
hideturtle()
done()

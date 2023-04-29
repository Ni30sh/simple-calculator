from tkinter import *


def press(item):
    global statement
    statement = statement + str(item)
    input.set(statement)


def clean():
    global statement
    statement = ""
    input.set("")


def equal():
    global statement
    result = str(eval(statement))
    input.set(result)
    statement = ""


statement = ""

win = Tk()
win.title("Calculater")
win.config(bg="black")
win.iconbitmap(r"F:\Calculator-icon.ico")
win.geometry("380x470")

input = StringVar()
e = Entry(win, font=("Time in romana", 25, "bold"), textvariable=input, justify="right")
e.place(x=5, y=5, height=100, width=365)

l2 = Button(win, text="c", font=("Time in romana", 25, "bold"), bg="sky blue", command=lambda: clean())
l2.place(x=10, y=120, height=50, width=70)

l3 = Button(win, text="/", font=("Time in romana", 25, "bold"), bg="#c5ccd3", command=lambda: press("/"))
l3.place(x=100, y=120, height=50, width=70)

l4 = Button(win, text="*", font=("Time in romana", 25, "bold"), bg="#c5ccd3", command=lambda: press("*"))
l4.place(x=190, y=120, height=50, width=70)
#
l5 = Button(win, text="-", font=("Time in romana", 25, "bold"), bg="#c5ccd3", command=lambda: press("-"))
l5.place(x=280, y=120, height=50, width=90)

l5a = Button(win, text="+", font=("Time in romana", 25, "bold"), bg="#c5ccd3", command=lambda: press("+"))
l5a.place(x=280, y=190, height=120, width=90)

l5b = Button(win, text="=", font=("Time in romana", 25, "bold"), bg="#ffa500", command=lambda: equal())
l5b.place(x=280, y=330, height=120, width=90)

l6 = Button(win, text="7", font=("Time in romana", 25, "bold"), bg="#c5ccd3", command=lambda: press("7"))
l6.place(x=10, y=190, height=50, width=70)

l6a = Button(win, text="4", font=("Time in romana", 25, "bold"), bg="#c5ccd3", command=lambda: press("4"))
l6a.place(x=10, y=260, height=50, width=70)

l6b = Button(win, text="1", font=("Time in romana", 25, "bold"), bg="#c5ccd3", command=lambda: press("1"))
l6b.place(x=10, y=330, height=50, width=70)

l6b = Button(win, text="0", font=("Time in romana", 25, "bold"), bg="#c5ccd3", command=lambda: press("0"))
l6b.place(x=10, y=400, height=50, width=160)
#
l7 = Button(win, text="8", font=("Time in romana", 25, "bold"), bg="#c5ccd3", command=lambda: press("8"))
l7.place(x=100, y=190, height=50, width=70)

l7a = Button(win, text="5", font=("Time in romana", 25, "bold"), bg="#c5ccd3", command=lambda: press("5"))
l7a.place(x=100, y=260, height=50, width=70)

l7b = Button(win, text="2", font=("Time in romana", 25, "bold"), bg="#c5ccd3", command=lambda: press("2"))
l7b.place(x=100, y=330, height=50, width=70)
#
l8 = Button(win, text="9", font=("Time in romana", 25, "bold"), bg="#c5ccd3", command=lambda: press("9"))
l8.place(x=190, y=190, height=50, width=70)

l8a = Button(win, text="6", font=("Time in romana", 25, "bold"), bg="#c5ccd3", command=lambda: press("6"))
l8a.place(x=190, y=260, height=50, width=70)

l8b = Button(win, text="3", font=("Time in romana", 25, "bold"), bg="#c5ccd3", command=lambda: press("3"))
l8b.place(x=190, y=330, height=50, width=70)

l8 = Button(win, text=".", font=("Time in romana", 25, "bold"), bg="#c5ccd3", command=lambda: press("."))
l8.place(x=190, y=400, height=50, width=70)

win.mainloop()

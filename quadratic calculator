import math
from tkinter import *

window = Tk()
window.title("Quadratic Equations Calculator")

# button function/ Clear
def clear():
    insert1.delete(0, END)
    insert2.delete(0, END)
    insert3.delete(0, END)
    insert4.delete(0, END)

# button function/ Calculate/ quadratic equation calculator
def cal():
    try:
        a = int(insert1.get())
        b = int(insert2.get())
        c = int(insert3.get())
        # checking if b^2 - 4ac is less than, equal or more than 0
        try:
            b_square = b * b
            Four_A_C = 4 * (a * c)
            A = (math.sqrt(b_square - Four_A_C))
            if A > 0:
                B = (b * (-1))
                C = (a * 2)
                B_minus_sqroot = B - A
                B_plus_sqroot = B + A
                ans_1 = str(B_plus_sqroot / C)
                ans_2 = str(B_minus_sqroot / C)
                insert4.insert(0, str("x = ") + str(ans_1) + str(" or x = ") + str(ans_2))
            if A == 0:
                B = (b * (-1))
                C = (a * 2)
                B_minus_sqroot = B - A
                B_plus_sqroot = B + A
                ans_1 = str(B_plus_sqroot / C)
                ans_2 = str(B_minus_sqroot / C)
                insert4.insert(0, str("x = ") + str(ans_1))
        except ValueError:
            insert4.insert(0, "no real solutions, this can be explained as b^2 - 4ac is less than zero ")
    except ValueError:
        insert4.insert(0, "you have to type in a number")

# Labels for prompts
Label(window, text="coefficient of x^2").grid(row=0, column=0)
Label(window, text="coefficient of x").grid(row=1, column=0)
Label(window, text="the last number").grid(row=2, column=0)

# Box for prompts
insert1 = Entry(window, width=15)
insert2 = Entry(window, width=15)
insert3 = Entry(window, width=15)
insert4 = Entry(window, width=75)
button_cal = Button(window, text="Calulate", width=7, padx=10, pady=5, borderwidth=5, background="light green", command=cal)
button_clear = Button(window, text="Clear", width=7, padx=10, pady=5, borderwidth=5, background="orange", foreground="black", command=clear)

# Button function
button_cal.grid(row=3, column=2)
button_clear.grid(row=3, column=3)
insert1.grid(row=0, column=1, columnspan=1, padx=10, pady=10)
insert2.grid(row=1, column=1, columnspan=1, padx=10, pady=10)
insert3.grid(row=2, column=1, columnspan=1, padx=10, pady=10)
insert4.grid(row=4, column=0, columnspan=3, padx=20, pady=20)

window.mainloop()

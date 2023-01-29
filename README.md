# draw.py
draw the picture of information
import matplotlib.pyplot as plt
import numpy as np

def main():        
    plt.plot([1, 2, 3], [list_grade1[0], list_grade1[1], list_grade1[2]], 'b-')
    plt.plot([1, 2, 3], [list_grade2[0], list_grade2[1], list_grade2[2]], 'r--')
    plt.axis([0, 4, 0, 100])
    plt.xlabel(xlabel)
    plt.ylabel(ylabel)
    plt.savefig('figure.png')

list_grade1 = []
list_grade2 =[]
xlabel = input('請輸入X座標標示：')
ylabel = input('請輸入Y座標標示：')
for i in range(3):
    grade1 = int(input('請輸入第一筆資料：'))
    if grade1 > 100:
        print('輸入值超出範圍')
        break
        sol()
    grade2 = int(input('請輸入第二筆資料：'))
    if grade2 > 100:
        print('輸入值超出範圍')
        break
    else:
        list_grade1.append(grade1)
        list_grade2.append(grade2)
        if i == 2:
            main()

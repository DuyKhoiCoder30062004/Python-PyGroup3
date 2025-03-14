# Python-PyGroup3
Đồ Án về Python có sử dụng AI



# * Lưu ý, ghi chú về cách chuyển đổi cửa sổ để mà chuyển đổi từ UI này sang UI mới để thao tác mới 

import tkinter as tk


def open_second_window():
    # Hide the first window
    root.withdraw()

    # Create a new window
    second_window = tk.Toplevel(root) # TK()  thứ 2
    second_window.title("Second Window")

    # Add some content to the second window
    label = tk.Label(second_window, text="Welcome to the second window!")
    label.pack()

    # Add a button to close the second window and go back to the first window
    def close_second_window():
        second_window.destroy()
        root.deiconify()  # Show the first window again

    close_button = tk.Button(second_window, text="Close", command=close_second_window)
    close_button.pack()


# Create the main window
root = tk.Tk()
root.title("Main Window")

# Add a button to open the second window
open_button = tk.Button(root, text="Open Second Window", command=open_second_window)
open_button.pack()

# Run the application
root.mainloop()



#Convolution Kernel 
# import tkinter as tk
#
#
# def open_second_window():
#     # Hide the first window
#     root.withdraw()
#
#     # Create a new window
#     second_window = tk.Toplevel(root) # TK()  thứ 2
#     second_window.title("Second Window")
#
#     # Add some content to the second window
#     label = tk.Label(second_window, text="Welcome to the second window!")
#     label.pack()
#
#     # Add a button to close the second window and go back to the first window
#     def close_second_window():
#         second_window.destroy()
#         root.deiconify()  # Show the first window again
#
#     close_button = tk.Button(second_window, text="Close", command=close_second_window)
#     close_button.pack()
#
#
# # Create the main window
# root = tk.Tk()
# root.title("Main Window")
#
# # Add a button to open the second window
# open_button = tk.Button(root, text="Open Second Window", command=open_second_window)
# open_button.pack()
#
# # Run the application
# root.mainloop()


import numpy as np
print(np.convolve((1,2,3),(4,5,6))) #padding kernel

# (1,2,3) x (6,5,4)

# [1,2,3]
# [4,5]
#
#   [1,2,3]
# [4,5]





#CÁCH XỬ LÝ ẢNH KHI ÁP DỤNG REGION OF INTEREST (CÓ THAO TÁC KERNEL)

# # Write Python3 code here
#
# import cv2
# import numpy as np
#
# image = cv2.imread(r'C:\Users\HELLO\Pictures\Saved Pictures\Sonic3.PNG')
#
# # making filter of 3 by 3 filled with 1 divide
# # by 9 for normalization
# blur_filter1 = np.ones((3, 3), np.float64)/(9.0)
#
# # making filter of 5 by 5 filled with 1 divide
# # by 25 for normalization
# blur_filter2 = np.ones((5, 5), np.float64)/(25.0)
#
# # making filter of 7 by 7 filled with 1 divide
# # by 49 for normalization
# blur_filter3 = np.ones((7, 7), np.float64)/(49.0)
#
# image_blur1 = cv2.filter2D(image, -1, blur_filter1)
# image_blur2 = cv2.filter2D(image, -1, blur_filter2)
# image_blur3 = cv2.filter2D(image, -1, blur_filter3)
#
# cv2.imshow('geek', image)
# cv2.imshow('geek_blur1', image_blur1)
# cv2.imshow('geek_blur2', image_blur2)
# cv2.imshow('geek_blur3', image_blur3)
#
# cv2.waitKey(0)
# cv2.destroyAllWindows()
#
#
# #convolution -> reverse array -> kernel (contains positive and negative)

import cv2
import numpy as np
import matplotlib.pyplot as plt
#DJango (not sure if enough time to grasp?!) (combine : python + html/css also)
img = cv2.imread(r'C:\Users\HELLO\Pictures\Saved Pictures\Sonic3.PNG')
img = cv2.resize(img, (200, 200))
img_xam = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
print(img.shape)
print(img_xam.shape)


#thiết kế Convolution
class Conv2d:
    def __init__(self, input, kernelSize):
        self.input = input
        self.chieu_cao, self.chieu_rong = input.shape
        self.kernel = np.random.randn(kernelSize, kernelSize)
    # print(kernel)

        self.results = np.zeros((self.chieu_cao - kernelSize + 1, self.chieu_rong - kernelSize + 1))

    def getRoi(self):
        for row in range(0, self.chieu_cao - self.kernel.shape[0] + 1):
            for col in range(0, self.chieu_rong - self.kernel.shape[1] + 1):
                roi = self.input[row: row + self.kernel.shape[0], col:col + self.kernel.shape[1]]
                yield row,col,roi
    def operating(self):
        for row, col, roi in self.getRoi():
            self.results[row, col] = np.sum(roi * self.kernel)
        # print(results, results.shape)
    # roi : region of interest
        return self.results

conv2d = Conv2d(img_xam, 5)
img_gray_con2d = conv2d.operating()
plt.imshow(img_gray_con2d, cmap='gray')

plt.show()









#Kỹ thuật sử dụng Notification sử dụng MessageBox
import tkinter as tk
from tkinter import messagebox

def show_notification():
    messagebox.showinfo("Notification", "This is your notification message!")

# Create the main window
root = tk.Tk()
root.title("Tkinter Notification Example")

# Set up the button to trigger the notification
notify_button = tk.Button(root, text="Show Notification", command=show_notification)
notify_button.pack(pady=20)

# Start the Tkinter event loop
root.mainloop()


#Neural Network , Squiggle, Hidđen layers

#Dosage example
#curved, bent lines, sigmoid function, ReLU Function
#softplus function f(x) = log(1+e^x) (ln log e cofficient)
#sigmoid curve : f(x) = e^x / ((e^x) +1 )
#ReLU: f(x) = max(0,x)
#blue curve are y - axis value
#objective: get x axis and y axis
#weight, bias
#https://www.youtube.com/watch?v=CqOfi41LfDw&list=PLblh5JKOoLUIxGDQs4LFFD--41Vzf-ME1&index=2


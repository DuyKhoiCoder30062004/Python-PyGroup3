# Python-PyGroup3
Đồ Án về Python có sử dụng AI



<!------------- Lưu ý, ghi chú về cách chuyển đổi cửa sổ để mà chuyển đổi từ UI này sang UI mới để thao tác mới --->>>

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

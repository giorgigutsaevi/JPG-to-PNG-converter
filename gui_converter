import tkinter as tk
from tkinter import filedialog
from tkinter import messagebox
from PIL import Image


root = tk.Tk()

canvas1 = tk.Canvas(root, width=300, height=250, bg='green', relief='raised')
canvas1.pack()

label1 = tk.Label(root, text='File Conversion Tool', bg='green')
label1.config(font=('calibri', 20))
canvas1.create_window(150, 60, window=label1)


def get_jpg():
    global my_image

    import_file_path = filedialog.askopenfilename()
    my_image = Image.open(import_file_path)


browseButton_JPG = tk.Button(text="      Import JPG File     ", command=get_jpg, bg='beige',
                             font=('calibri', 12, 'bold'))
canvas1.create_window(150, 130, window=browseButton_JPG)


def convert_to_png():
    global my_image

    export_file_path = filedialog.asksaveasfilename(defaultextension='.png')
    my_image.save(export_file_path)

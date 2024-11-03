# Text-to-Speech
This Python project converts written text into natural-sounding speech using the pytts3x library. Users can input any text, select the language, and listen to the generated audio output. Ideal for applications in accessibility, language learning, and multimedia content creation.

import tkinter as tk
from tkinter import *
import pyttsx3

engine=pyttsx3.init()

def speaknow():
    engine.say(textv.get())
    engine.runAndWait()
    engine.stop()
    
root= Tk()

textv=StringVar()

obj = LabelFrame (root,text="Text to Speech",font= 20,bd=1)
obj.pack(fill="both",expand="yes",padx=10,pady=10)

lbl=Label(obj,text="Text",font=30)
lbl.pack(side=tk.LEFT,padx=5)

text=Entry(obj,textvariable=textv,font=30,width=25,bd=5)
text.pack(side=tk.LEFT,padx=10)

btn=Button(obj,text="Speak",font=20,bg="Black",fg="White",command=speaknow)
btn.pack(side=tk.LEFT,padx=10)

root.title("Text to Speech")
root.geometry("400x200")
root.resizable(False,False)
root.mainloop()

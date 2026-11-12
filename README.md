# k-n
APP_USER=admin
APP_USER=1234

import os
import tkinter as tk
fron dotenv import load_dotenv

load_dotenv()
APP_USER= os.getenv("APP_USER")
APP_PASSWORD= 
os.getenv("APP_PASSWORD")

def capturar_credenciales():usuario= entry_usuario .get().strip()
contrasena= entry_contrasena.get().strip()
return usuario, contrasena

def validar_credenciaes(usuario, contrasena):
return usuario==APP_USER and contrasena == APP_PASSWORD

def mostrarr_mensaje (es_correcto): if es_correcto:
    label_mensaje.config(text="Acceso correcto", fg="green")
elese:
     label_mensaje.config(text="usuario o contraseña incorrectos", fg="red")

  def verificar(): 
    usuario, contrasena = capturar_credenciales()
    es_correcto = validar_credenciaes(usuario,contrasena)
    mostrarr_mensaje(es_correcto)

ventana=tk.tk ()
ventana.title("vañidacion de credenciales")
ventana.geometry("350x220")
ventana.resizable(flase,flase)

tk.lebel(ventana, text="usuario:").pack(pady=(20,0))
entry_usuario=tk Entry(ventana,width=30)
entry_usuario.pack()


tk.lebel(ventana,text="contraseña:").pack(pady=(10,0))
entry_contrasena.pack()

tk.button(ventana,text="ingresar", command=verificar).pack(pasy=15)

label_mensaje=tk.lebel(ventana,text="",font=("Arial", 11."bold")
label_mensaje.pack()
ventana.mainloop()



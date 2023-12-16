# Calculadora-IMC
Linha de código simples em Python 
import tkinter as tk

def calculo():
  num1=float(entrada1.get())
  num2=float(entrada2.get())
  if num2 != 0:
    resultado= num1/num2**2
    resultado_label.config(text = f'Resultado: {resultado}')
  else:
       resultado_label.config(text = '#Erro divisão por zero')


root= tk.Tk()

root.geometry('500x500')
root.title('#Calculadora de IMC!')

label = tk.Label(root,bg='grey', fg= 'white',text = 'Digite seu peso:')
label.pack()
entrada1= tk.Entry (root)
entrada1.pack()
label2 = tk.Label(root, bg='grey', fg= 'white', text= 'Digite sua altura(M):')
label2.pack()
entrada2= tk.Entry (root)
entrada2.pack()

bt = tk.Button(root,bg='grey', fg= 'white', text = 'IMC=',command=calculo)
bt.pack()

resultado_label =tk.Button(root,bg='grey', fg= 'white',text= '=')
resultado_label.pack()
root.mainloop()

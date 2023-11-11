#підключення бібліотек
from PyQt5.QtCore import Qt #підключення бібліотек
from PyQt5.QtWidgets import QApplication, QWidget, QLabel, QVBoxLayout, QRadioButton,QHBoxLayout #імпортуємо все для створення програми
#створення додатка і головного вікна
app = QApplication([])#створення додатку
win = QWidget() #створення вікна
win.setWindowTitle("Тест") #створення назви гри
win.resize(600, 400)#розмір вікна
win.move(550, 250)#розсташування вікна
#створення елементів інтерфейсу
text1 = QLabel("Хто легенда афганістану")#створення текту питання 
rb_1 = QRadioButton("Дацків") #створення перемикачів1 :)
rb_2 = QRadioButton("Ільницька") #створення перемикачів2 :)
rb_3 = QRadioButton("Гошовський") #створення перемикачів3 :) 
rb_4 = QRadioButton("Лебідка") #створення перемикачів4 :)
#створення віджетів головного вікна
line1 = QHBoxLayout()#створення горизонтальної лінії
line2 = QHBoxLayout()#створення горизонтальної лінії
line3 = QHBoxLayout()#створення горизонтальної лінії
line_q = QVBoxLayout()#створення вертикальної лінії
#розташування віджетів по лейаутам
line3.addWidget(text1, alignment = Qt.AlignCenter)#прикріплення до лінії "хто легенда афганістану"
line1.addWidget(rb_1, alignment = Qt.AlignCenter)#прикріплення до горизонтальеої ліінії 1 перемикач
line1.addWidget(rb_2, alignment = Qt.AlignCenter)#прикріплення до горизонтальеої ліінії 2 перемикач
line2.addWidget(rb_3, alignment = Qt.AlignCenter)#прикріплення до горизонтальеої ліінії 3 перемикач
line2.addWidget(rb_4, alignment = Qt.AlignCenter)#прикріплення до горизонтальеої ліінії 4 перемикач
line_q.addLayout(line3)#створення ліній до якої прикріплений текст
line_q.addLayout(line1)#створення лінії 1 до якої прикріплені відповіді
line_q.addLayout(line2)#створення лінії 2 до якої прикріплені відповіді
win.setLayout(line_q)#ліній до якої приєднуються інші ліній на яких розташовані відповіді а також відповідає за текст

#фуххх зробив :) 



#обробка натискань на перемикачі
 
#відображення вікна додатка 







win.show() #показування вікна
app.exec_() #функція для того що моментально не закривало вікно

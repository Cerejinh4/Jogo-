import kivy
from kivy.app import App
from kivy.uix.label import Label
from kivy.uix.button import Button
from kivy.uix.textinput import TextInput
from kivy.uix.image import Image
from kivy.uix.gridlayout import GridLayout
from kivy.uix.scrollview import ScrollView

# Carregar Imagens
roupa1 = Image(source="roupas/roupa1.png")
roupa2 = Image(source="roupas/roupa2.png")
roupa3 = Image(source="roupas/roupa3.png")

# Definir Layout
layout = GridLayout(cols=3, spacing=10, padding=10)
layout.add_widget(roupa1)
layout.add_widget(roupa2)
layout.add_widget(roupa3)

# Criar ScrollView
scroll = ScrollView(size_hint=(1, None))
scroll.add_widget(layout)

# Definir Interface
class TelaApp(App):
    def build(self):
        return scroll

# Executar App
if __name__ == "__main__":
    TelaApp().run()
    

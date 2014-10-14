from kivy.app import App
from kivy.lang import Builder
from kivy.uix.screenmanager import ScreenManager, Screen
from kivy.core.window import Window
Window.clearcolor = (0, 0.8, .152, 1)

# Create both screens. Please note the root.manager.current: this is how
# you can control the ScreenManager from kv. Each screen has by default a
# property manager that gives you the instance of the ScreenManager used.
Builder.load_string("""
<HomeScreen>:
    GridLayout:
        padding: 20
        spacing: 20
        cols: 1
        Label:
            font_size: '62sp'
            text: "[color=000000][sub][GamePlan][/sub][/color]"
            markup: True
            size_hint_y: .5
        Button:
            text: '[b]Host[/b]'
			font_size: '24sp'
			markup: True
            on_press: root.manager.current = 'hostscreen'
        Button:
            text: '[b]Join[/b]'
			font_size: '24sp'
			markup: True
            on_press: root.manager.current = 'joinscreen'
        Button:
            text: "[b]What's Around Me?[/b]"
			font_size: '24sp'
			markup: True
            on_press: root.manager.current = 'around'
		Button:
			text: '[b]My GamePlan[/b]'
			font_size: '24sp'
			markup: True
			on_press: root.manager.current = 'mygameplan'

<HostScreen>:
    GridLayout:
        padding: 20
        spacing: 20
        cols: 1
        Label:
            font_size: '62sp'
            text: "[color=000000][sub][Host][/sub][/color]"
            markup: True
            size_hint_y: .5
			
		GridLayout:
			cols: 2
			Button:
				text: "[b]Cancel[/b]"
				font_size: '20sp'
				markup: True
				padding: -10, -10
				halign: 'center'
				valign: 'middle'
				text_size: self.size
				on_press: root.manager.current = 'home'
			Button:
				text: "[b]Host Event[/b]"
				font_size: '20sp'
				markup: True
				padding: -10, -10
				halign: 'center'
				valign: 'middle'
				text_size: self.size

<JoinScreen>:
    GridLayout:
        padding: 20
        spacing: 20
        cols: 1
        Label:
            font_size: '62sp'
            text: "[color=000000][sub][Join][/sub][/color]"
            markup: True
            size_hint_y: .5
			
		GridLayout:
			cols: 2
			Button:
				text: "[b]Back[/b]"
				font_size: '20sp'
				markup: True
				padding: -10, -10
				halign: 'center'
				valign: 'middle'
				text_size: self.size
				on_press: root.manager.current = 'home'
			Button:
				text: "[b]Next[/b]"
				font_size: '20sp'
				markup: True
				padding: -10, -10
				halign: 'center'
				valign: 'middle'
				text_size: self.size


<AroundScreen>:
    GridLayout:
        padding: 20
        spacing: 20
        cols: 1
        Label:
            font_size: '62sp'
            text: "[color=000000][sub][Around Me][/sub][/color]"
            markup: True
            size_hint_y: .5			
        Button:
            text: '[b]Back[/b]'
			font_size: '20sp'
			markup: True
            on_press: root.manager.current = 'home'
			
<My_GamePlan>:
	GridLayout:
		padding: 20
		spacing: 20
		cols: 1
		Label:
			font_size: '62sp'
			text: "[color=000000][sub][My GamePlan][/sub][/color]"
            markup: True
            size_hint_y: .5
        Button:
            text: '[b]Back[/b]'
			font_size: '20sp'
			markup: True
            on_press: root.manager.current = 'home'
""")

# Declare both screens
class HomeScreen(Screen):
    pass

class HostScreen(Screen):
    pass

class JoinScreen(Screen):
    pass

class AroundScreen(Screen):
    pass
	
class My_GamePlan (Screen):
	pass

# Create the screen manager
sm = ScreenManager()
sm.add_widget(HomeScreen(name='home'))
sm.add_widget(HostScreen(name='hostscreen'))
sm.add_widget(JoinScreen(name='joinscreen'))
sm.add_widget(AroundScreen(name='around'))
sm.add_widget(My_GamePlan(name='mygameplan'))

class TestApp(App):

    def build(self):
        return sm

if __name__ == '__main__':
    TestApp().run()

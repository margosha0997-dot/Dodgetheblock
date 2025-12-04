from kivy.app import App
from kivy.uix.widget import Widget
from kivy.clock import Clock
from kivy.graphics import Color, Rectangle
from kivy.core.window import Window
from kivy.uix.label import Label
from random import randint

PLAYERSIZE = 50
ENEMYSIZE = 50
ENEMYSPEED = 5
MOVESPEED = 10

Window.clearcolor = (0.12, 0.12, 0.12, 1)

class GameWidget(Widget):
    def __init__(self, kwargs):
        super().__init__(kwargs)
        self.score = 0
        self.playerx = (Window.width - PLAYERSIZE) / 2
        self.playery = 10
        self.enemies = []
        self.touchdir = 0
        self.gameover = False

        self.scorelabel = Label(text="Score: 0", sizehint=(None, None))
        self.addwidget(self.scorelabel)
        Clock.scheduleinterval(self.update, 1.0 / 60.0)
        Window.bind(onresize=self.onresize)
        self.onresize()

    def onresize(self, args):
        self.scorelabel.pos = (10, Window.height - 40)

    def ontouchdown(self, touch):
        if self.gameover:
            self.resetgame()
            return True
        if touch.x < Window.width / 2:
            self.touch_dir = -1
        else:
            self.touch_dir = 1
        return True

    def on_touch_up(self, touch):
        self.touch_dir = 0
        return True

    def spawn_enemy(self):
        x = randint(0, int(Window.width - ENEMY_SIZE))
        y = Window.height
        self.enemies.append([x, y])

    def update(self, dt):
        if self.game_over:
            return

        self.player_x += self.touch_dir  MOVE_SPEED
        if self.pl......

# Kpick

Python module for creating menus.

## Установка

Для установки используйте следующую команду:

```bash
pip install Kpick
```

### Basic Example
```Python
from Kpick import create_menu

menu_options = ['Option 1', 'Option 2', 'Option 3']
selection = create_menu(menu_options)

print(f'Вы выбрали: {selection_index}')
```

### Advanced Example
```Python
import Kpick  

class Menu():
    def __init__(self) -> None:
        self.options = ["WireLessAttacl", "Wifi", "Hacking"]
        self.selected_index = None

    def main_menu(self):
        self.selected_index = Kpick.run_menu(self.options)

        if self.selected_index == 0:
            self.first()
        elif self.selected_index == 1:
            self.second()
        elif self.selected_index == 2:
            print("You selected Option 3.")

    def first(self):
        opt2 = ["Jammer", "Flood", "WPA PIN HACK","exit"]
        slt = Kpick.run_menu(opt2)
        
        if slt == 0:
            return(self.first())
        elif slt == 1:
            return(self.first())
        elif slt == 2:
            return(self.first())
        elif slt == 3:
            return(self.main_menu())

    def second(self):
        opt3 = ["Monitoring Mode", "Scan Networks", "exit"]
        slt2 = Kpick.run_menu(opt3)

        if slt2 == 0:
            return(self.second())
        elif slt2 == 1:
            return(self.second())
        elif slt2 == 2:
            return(self.main_menu())

menu = Menu()
menu.main_menu()

# RenPy-Map

## script.rpy

```python
label start:
    show screen gameUI
    "Test"
    return

label serre_pressed:
    "Tu entre dans la serre"
```

## map.rpy

```python
screen gameUI:
    imagebutton:
        xalign 1.0
        yalign 0.0
        xoffset -30
        yoffset 30
        auto "UI/mapbutton_%s.png"
        action ShowMenu("MapUI")

screen MapUI():
    tag mapUI
    add "map/background.jpg"

    imagebutton:
        xpos 593
        ypos 335
        idle "map/serre_idle.png"
        hover "map/serre_hover.png"
        action Jump("serre_pressed")
```
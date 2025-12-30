# Code Snippets & Templates

## FlipComponent Example
```gdscript
extends Node2D
class_name FlipComponent

signal flipped(direction: int)

@export var can_auto_flip: bool = true

func flip(direction: int):
    scale.x = abs(scale.x) * direction
    emit_signal("flipped", direction)
```

## Shockwave Example
```gdscript
func cast_shockwave():
    for enemy in get_tree().get_nodes_in_group("enemies"):
        var dist = global_position.distance_to(enemy.global_position)
        var dmg = clamp(100 - dist, 0, 100)
        enemy.apply_damage(dmg)

    blackout_lights()
```

## Shield Timer Example
```gdscript
var shield_active = false
var shield_timer = 0.0

func activate_shield(duration: float):
    shield_active = true
    shield_timer = duration

func _process(delta):
    if shield_active:
        shield_timer -= delta
        if shield_timer <= 0:
            shield_active = false
```

# Common Mistakes & Pitfalls

- ❌ Forgetting to check `is_instance_valid(node)` before using a reference.
- ❌ Calling tweens/animations before the scene is ready.
- ❌ Using hardcoded node paths instead of exports or groups.
- ❌ Mixing `_ready()`, `_process()` without understanding execution order.
- ❌ Energy/Shield not clamped → leading to negative values.
- ❌ Forgetting to reset states when reloading scene.

# Rules to Remember for `Align`

---

### Rule 1 — Tight Constraint → Align fills it, factor ignored
> Parent gives exact size (e.g. `Container(width: 400)`) → Align becomes that size. **Factor does nothing.**

---

### Rule 2 — Loose Constraint + Factor set → Factor wins
> Parent gives max size but not forced (e.g. `ConstrainedBox(maxWidth: 400)`) → Align becomes **child × factor**

---

### Rule 3 — Loose Constraint + No Factor → Align fills max
> Parent gives max size, no factor set → Align **stretches to fill** that max size

---

### Rule 4 — Unconstrained + Factor set → Factor wins
> No size from parent, factor is set → Align becomes **child × factor**

---

### Rule 5 — Unconstrained + No Factor → Align wraps child
> No size from parent, no factor → Align **shrinks to child's size**

---

### One Line to Remember All:

> **Tight → parent wins 🔒 | Loose/Unconstrained → factor wins ✅ | No factor → fills or wraps**

---

### Quick Cheat Sheet:

| Constraint | Factor | Align Size |
|---|---|---|
| Tight (exact) | any | Parent size 🔒 |
| Loose (max only) | set | child × factor |
| Loose (max only) | null | fills max |
| Unconstrained | set | child × factor |
| Unconstrained | null | child size |

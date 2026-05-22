# Rules to Remember for `Padding`

---

### Rule 1 — Padding steals space from constraints first
> Parent gives `300px` → you set `20px` each side → child only gets `260px`. **Child never sees the original 300px.**

---

### Rule 2 — Child is always smaller than Padding's available space
> Whatever space parent gives → child always gets **less** by the amount of padding you set.

---

### Rule 3 — Padding sizes itself by child + padding
> Padding does NOT keep full parent size. It wraps child then **adds padding back** on top.
> `Padding size = child size + padding on all sides`

---

### Rule 4 — Padding just creates empty space around child
> That extra space is just **blank**. Nothing lives there. Child sits inside surrounded by emptiness.

---

### One Line to Remember All:

> **Padding shrinks space for child → child lays out smaller → Padding wraps child and adds space back → empty space around child**

---

### Quick Cheat Sheet:

| Step | What Happens |
|---|---|
| Parent gives space | `300px` available |
| Padding subtracts | `300 - 20 - 20 = 260px` given to child |
| Child lays out | Child is `260px` |
| Padding wraps child | `260 + 20 + 20 = 300px` final size |
| Visual result | Empty space surrounding child |

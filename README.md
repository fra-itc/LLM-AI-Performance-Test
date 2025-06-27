# 🏢 TRAPDOOR ELEVATOR LOGIC TEST v3.0
## (50-Floor Extended Cut)

---

## 📌 **OBJECTIVE**
- Start from **floor 0** and reach **EXACTLY floor 50**
- Use the **MINIMUM number of button presses**
- Maintain **≥5 ⚡️Energy Pack** and **≥2 🗝 Code-Cards** at the end
- **Avoid all Trap Floors and Random Traps**

---

## 🎮 **AVAILABLE BUTTONS**

| Button | Effect | Cost |
|--------|--------|------|
| **A** | +10 floors | 2⚡️ |
| **B** | +5 floors | 1⚡️ |
| **C** | +1 floor | Variable cost → if floor is multiple of 7, bounces −2 |
| **D** | −1 floor | Regenerates 1⚡️ (never below 0) |
| **E** | Emergency-Escape | Works ONLY on trap floors; +1 floor, resets flag |
| **F** | Mirror-Mode toggle | If active, inverts ↑↓ for 3 moves (costs 0⚡️) |
| **G** | Night-Shift toggle | If active, halves all ⚡️ costs for 5 moves |
| **H** | Teleport to 49 | Available ONLY after touching floor 42; consumes all remaining ⚡️ and requires Green 🗝 Code-Card |

---

## 🔥 **TRAP FLOORS**

| Floor | Effect |
|-------|--------|
| **13** | Stuck until you press E (anything else → return to floor 0) |
| **29** | Command inversion for next 3 moves (A↓10, D↑1, B nix, C +7) |
| **36** | Memory-Reset → "forget" last 2 button presses (must recalculate) |
| **47** | Random-Trap → 50% chance of losing 1🗝 Code-Card |

---

## 🎲 **RANDOM TRAPS**
Every time you land on a **prime floor >40**, roll a d6:
- **1-2:** lose 2⚡️
- **3-4:** lose 1🗝 Code-Card  
- **5-6:** nothing

**Prime floors >40:** 41, 43, 47

---

## 🗝 **CODE-CARDS**

| Card | How to Obtain |
|------|---------------|
| **Blue Card** | Obtained at floor 17 (autopick; no cost) |
| **Red Card** | Obtained at floor 33 by pressing B exactly |
| **Green Card** | Obtained at floor 8 by pressing C→A in sequence |

**Requirements:**
- Need at least **2 different cards** at the end
- Button H requires the **Green Card** to survive

---

## ⚡️ **ENERGY PACK**
- Start with **10⚡️**
- **Never go below zero** or you fail

---

## 💥 **SUMMARY RULES**

1. You can press buttons in **any order**, but apply **ALL contextual effects**
2. If you **run out of energy** or **break a constraint**, **GAME OVER**
3. You must reach **floor 50 exactly**: neither 51, nor 49 → **50**
4. Provide **step-by-step reasoning**, then **final sequence** (e.g. "AABF…")
5. Include **verification table** (floor, energy, cards, flags) for each move

---

## 🏆 **BONUS** (optional but appreciated)
- Prove the **OPTIMALITY** of your sequence (BFS, A*, or algorithm of choice)
- List any **alternative paths** ≤ same length

---

## 📋 **EXPECTED RESPONSE FORMAT**

1. **Detailed reasoning**
2. **Final sequence** (string)
3. **State-by-state table**
4. **Constraint verification + conclusion**
5. **(Bonus)** Proof of optimality / alternatives


---

## 📜 LICENSE

This game logic is open-sourced under the **MIT License** (see `LICENSE` file).  
Original concept by **Francesco Trani**
---

## 📎 METADATA

```json
{
  "name": "Trapdoor Elevator Logic Test v3.0",
  "author": "Francesco Trani",
  "version": "3.0",
  "type": "Logic Puzzle / Interactive Game",
  "min_floor": 0,
  "max_floor": 50,
  "requires_code_cards": true,
  "traps": true,
  "energy_constraint": true,
  "license": "MIT"
}
```

---

## 🌐 LINKS

- [GitHub Repo](https://github.com/fra-itc/LLM-AI-Performance-Test)



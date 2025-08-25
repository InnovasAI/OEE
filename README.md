# OEE Calculator — Mobile‑first (Hours)

A single‑file **web app** that calculates Overall Equipment Effectiveness (OEE) with a friendly, mobile‑first UI. All time inputs are in **hours**, and the ideal speed is in **parts per hour**.

---

## ✨ Features

* **Live OEE math** with Availability, Performance, Quality, and overall **OEE%**
* **Mobile‑first** layout with large touch targets and unit chips (h, parts/h)
* **Run Log** saved to `localStorage` (no server required)
* **CSV export** of the log
* **Traffic‑light status pill** (Great / Fair / Needs Attention)
* Single file: just `index.html` (HTML + CSS + JS)

---

## 🧩 File Structure

```
./
└── index.html   # The entire app (no build step)
```

---

## 🚀 Getting Started

1. **Download** `index.html` (from the canvas) and save it in a folder.
2. **Open** it in a modern browser (Chrome, Edge, Firefox, Safari). That’s it.

> Optional: serve locally for better file‑URL behavior:

```bash
# Python 3
python -m http.server 8080
# Then open http://localhost:8080
```

---

## 🧮 Inputs & Units

* **Planned production time (hours)** — total scheduled time.
* **Unplanned downtime (hours)** — breakdowns, jams, waiting, etc.
* **Ideal rate (parts/hour)** — best *repeatable* speed.
* **Total pieces** — good + scrap.
* **Good pieces** — saleable output.

---

## 📐 Formulas

Let:

* `Planned` = planned time (h)
* `Downtime` = unplanned downtime (h)
* `Rate` = ideal rate (parts/h)
* `Total` = total pieces (good + scrap)
* `Good` = good pieces

Then:

* **Run time (h)** = `Planned − Downtime`
* **Availability** = `Run / Planned`
* **Performance** = `Total ÷ (Run × Rate)`  *(capped at 100%)*
* **Quality** = `Good ÷ Total`
* **OEE** = `Availability × Performance × Quality`

### Example

```
Planned = 8.0 h
Downtime = 1.0 h
Rate = 120 parts/h
T
```

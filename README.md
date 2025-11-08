# resume
import tkinter as tk
from tkinter import ttk

# Root window
root = tk.Tk()
root.title("Harshit — Jetpack Mission Log")
root.configure(bg="#031018")
root.geometry("1000x700")

# Styles
style = ttk.Style()
style.configure("Card.TFrame", background="#0b2734", padding=18, relief="raised")
style.configure("Title.TLabel", foreground="#9fd6e6", font=("Arial", 9, "bold"))
style.configure("Section.TLabel", foreground="#e6f7ff", font=("Arial", 10))
style.configure("Muted.TLabel", foreground="#9fd6e6", font=("Arial", 9))
style.configure("Badge.TLabel", background="#083b46", foreground="#9feaff", padding=4, font=("Arial", 9), relief="ridge")

# Header
header = tk.Frame(root, bg="#031018")
header.pack(pady=10, anchor="w")

avatar = tk.Label(header, text="H", bg="#ffd44d", fg="#07202a", font=("Arial", 20, "bold"), width=4, height=2)
avatar.pack(side="left", padx=10)

info = tk.Frame(header, bg="#031018")
info.pack(side="left")

tk.Label(info, text="Harshit — Jetpack Mission Log", font=("Arial", 18), fg="#e6f7ff", bg="#031018").pack(anchor="w")
tk.Label(info, text="Reliability-focused Engineer • Project Lead • M.Sc. Informatics (pursuing)", fg="#9fd6e6", bg="#031018").pack(anchor="w")
tk.Label(info, text="Contact: rharshit1111@gmail.com • github.com/Harshit-Ace • New Delhi", fg="#9fd6e6", bg="#031018").pack(anchor="w", pady=4)

# Main content
main = tk.Frame(root, bg="#031018")
main.pack(padx=20, pady=10, fill="both", expand=True)

# Left column
left = ttk.Frame(main, style="Card.TFrame")
left.grid(row=0, column=0, sticky="nsew", padx=10, pady=10)

# Run Summary
ttk.Label(left, text="Run Summary", style="Title.TLabel").pack(anchor="w")
ttk.Label(left, text="Open to roles that value systems thinking, telemetry-first development, and reliable delivery.", style="Section.TLabel", wraplength=500).pack(anchor="w", pady=5)

# Jetpack Stats
ttk.Label(left, text="Jetpack Stats", style="Title.TLabel").pack(anchor="w", pady=(10, 0))
stats = tk.Frame(left, bg="#083443")
stats.pack(anchor="w", pady=5)
for label, value in [("Level", "6"), ("XP", "2,800 / 5,000"), ("Distance", "Hospital Management System MVP")]:
    stat = tk.Frame(stats, bg="#083443", padx=10, pady=5)
    stat.pack(side="left", padx=5)
    tk.Label(stat, text=label, fg="#e6f7ff", bg="#083443", font=("Arial", 10, "bold")).pack()
    tk.Label(stat, text=value, fg="#e6f7ff", bg="#083443").pack()

# Skills
ttk.Label(left, text="Gadgets & Upgrades", style="Title.TLabel").pack(anchor="w", pady=(10, 0))
skills = [("Python", "Intermediate"), ("SQL", "Intermediate"), ("C / C++", "Intermediate"),
          ("Java", "Beginner"), ("HTML / CSS", "Beginner"), ("Power BI", "Beginner")]
for skill, level in skills:
    row = tk.Frame(left, bg="#0b2734")
    row.pack(anchor="w", fill="x")
    tk.Label(row, text=skill, fg="#e6f7ff", bg="#0b2734").pack(side="left")
    tk.Label(row, text=level, fg="#e6f7ff", bg="#0b2734").pack(side="right")

# Run Logs
ttk.Label(left, text="Run Logs", style="Title.TLabel").pack(anchor="w", pady=(10, 0))
log = tk.Frame(left, bg="#0b2734", padx=10, pady=5)
log.pack(anchor="w", fill="x")
tk.Label(log, text="Hospital Management System — Lead Developer", fg="#ffd44d", bg="#0b2734", font=("Arial", 10, "bold")).pack(anchor="w")
tk.Label(log, text="Solo project", fg="#9fd6e6", bg="#0b2734").pack(anchor="w")
tk.Label(log, text="Built a system to manage patient records, staff, doctors, and appointments. Implemented backend flows and Power BI reports.", fg="#e6f7ff", bg="#0b2734", wraplength=500).pack(anchor="w")

# Achievements
achievements = ttk.Frame(left, style="Card.TFrame")
achievements.pack(anchor="w", pady=10, fill="x")
ttk.Label(achievements, text="Medals & Achievements", style="Title.TLabel").pack(anchor="w")
for badge in ["Delivered MVP", "Strong Communicator", "Project Management"]:
    ttk.Label(achievements, text=badge, style="Badge.TLabel").pack(side="left", padx=4)

# Power-up Paths
ttk.Label(achievements, text="Power-up Paths", style="Title.TLabel").pack(anchor="w", pady=(10, 0))
ttk.Label(achievements, text="Plans to upskill in CI/CD, containers, databases, and full-stack development.", style="Section.TLabel", wraplength=500).pack(anchor="w")

# Right column (Sidebar)
right = ttk.Frame(main, style="Card.TFrame")
right.grid(row=0, column=1, sticky="nsew", padx=10, pady=10)

# Education
ttk.Label(right, text="Education", style="Title.TLabel").pack(anchor="w")
for edu in ["G.L.T Saraswati Bal Mandir, Nehru Nagar", "BSc (H) Electronics", "MSc Informatics — pursuing"]:
    ttk.Label(right, text=edu, style="Section.TLabel").pack(anchor="w")

# Loadout
ttk.Label(right, text="Loadout", style="Title.TLabel").pack(anchor="w", pady=(10, 0))
ttk.Label(right, text="Python · SQL · C/C++ · Java · HTML/CSS · Power BI", style="Section.TLabel").pack(anchor="w")

# Traits
ttk.Label(right, text="Player Traits", style="Title.TLabel").pack(anchor="w", pady=(10, 0))
ttk.Label(right, text="Good communicator • Project management skills • Rapid learner", style="Muted.TLabel").pack(anchor="w")

# Next Mission
ttk.Label(right, text="Next Mission", style="Title.TLabel").pack(anchor="w", pady=(10, 0))
tk.Button(right, text="Request Tailored Dossier / PDF", bg="#ffd44d", fg="#07202a", font=("Arial", 10, "bold")).pack(fill="x", pady=5)

# Contact
contact = ttk.Frame(right, style="Card.TFrame")
contact.pack(anchor="w", pady=10, fill="x")
ttk.Label(contact, text="Contact", style="Title.TLabel").pack(anchor="w")
ttk.Label(contact, text="rharshit1111@gmail.com", style="Section.TLabel").pack(anchor="w")
ttk.Label(contact, text="github.com/Harshit-Ace • New Delhi", style="Muted.TLabel").pack(anchor="w")

# Footer
tk.Label(root, text="Replace or add links (portfolio, repo, phone) and I will regenerate a tailored PDF.", fg="#9fd6e6", bg="#031018", font=("Arial", 9)).pack(pady=10)

root.mainloop()


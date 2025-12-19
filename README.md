#!/usr/bin/env python3
"""
Daily Note Generator
- Creates or appends a daily note with timestamp
- Saves notes into daily_notes.txt
"""

import datetime

def main():
    now = datetime.datetime.now().strftime("%Y-%m-%d %H:%M:%S")
    note = f"{now} - Daily activity logged.\n"

    with open("daily_notes.txt", "a", encoding="utf-8") as f:
        f.write(note)

    print("Daily note added:")
    print(note.strip())

if __name__ == "__main__":
    main()

def main():
    print("📝 Simple Notepad")
    print("Type your notes below. Enter 'SAVE' to save and quit.\n")

    notes = []
    while True:
        line = input("> ")
        if line.strip().upper() == "SAVE":
            break
        notes.append(line)

    with open("notes.txt", "w", encoding="utf-8") as f:
        f.write("\n".join(notes))

    print("✅ Notes saved in 'notes.txt'")

if __name__ == "__main__":
    main()

# dz-
import os

def show_contents(path):
    if not os.path.isdir(path):
        print("Такої директорії не існує!")
        return

    print(f"\nВміст директорії: {path}\n")

    for root, dirs, files in os.walk(path):
        print(f"📂 Директорія: {root}")

        for d in dirs:
            print("  [DIR] ", d)

        for f in files:
            print("  [FILE]", f)

        print("-" * 40)


path = input("Введіть шлях до папки: ")
show_contents(path)

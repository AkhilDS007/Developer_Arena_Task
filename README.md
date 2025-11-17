# Developer_Arena_Task

def personal_introduction():
    name = input("What's your name? ").strip()
    while not name:
        name = input("Please enter your name: ").strip()
        
    age = input("How old are you? ").strip()
    while True:
        try:
            age_int = int(age)
            if age_int < 0:
                raise ValueError("Negative age")
            break
        except ValueError:
            age = input("Please enter a valid non-negative integer for age: ").strip()

    hobby = input("What's your favorite hobby? ").strip()
    if not hobby:
        hobby = "no hobby specified"

    print(f"\nWelcome, {name}! 🎉")
    print(f"You are {age_int} years old and enjoy {hobby}.")
    print("Nice to meet you!")

personal_introduction()

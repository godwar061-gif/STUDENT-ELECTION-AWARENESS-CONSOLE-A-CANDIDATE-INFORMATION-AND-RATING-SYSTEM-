users = {}

# PART 1: LOGIN
print(
    "Welcome to the Student Election Awareness Console!\n"
    "This program is developed to help PHINMA Cagayan de Oro College students\n"
    "become more informed and engaged during campus elections.\n"
    "Here, you can explore candidate information and rate them based on\n"
    "leadership, credibility, and popularity.\n"
)

while True:
    print("\nLOGIN MENU\n1. Sign Up\n2. Login\n0. Exit")
    login_choice = input("Enter your choice: ")

    if login_choice == "1":
        print("\n-- SIGN UP --")
        student_id = input("Enter your Student ID: ")
        password = input("Enter your new password: ")
        users[student_id] = password
        print("\nAccount created successfully! You can now log in.\n")

    elif login_choice == "2":
        print("\n-- LOGIN --")
        student_id = input("Enter your Student ID: ")
        password = input("Enter your password: ")

        if student_id in users and users[student_id] == password:
            print(
                f"\nLogin successful! Welcome Student {student_id}!\n"
                "You can now explore candidates, rate them, and view the Rating Overview."
            )
            input("\nPress Enter to continue...")
            break
        else:
            print("\nInvalid Student ID or password. Please try again.")

    elif login_choice == "0":
        print("\nThank you for using the Student Election Awareness Console. Goodbye!")
        exit()

    else:
        print("\nInvalid input. Please enter 1, 2, or 0.")

#RATING STORAGE PER CANDIDATE
ratings = {
    "Ken Torre": {"total": 0, "count": 0},
    "Micah Reyes": {"total": 0, "count": 0},
    "Janah Abonitalla": {"total": 0, "count": 0},
    "Carl Mendoza": {"total": 0, "count": 0},
    "Shem Borromeo": {"total": 0, "count": 0},
    "Alex Tanso": {"total": 0, "count": 0},
    "Benhassan Casir": {"total": 0, "count": 0},
    "Marie Dizon": {"total": 0, "count": 0},
}

# PART 2: MAIN MENU
while True:
    print(
        f"\nSTUDENT ELECTION AWARENESS CONSOLE\n"
        f"Welcome Student {student_id}!\n"
        "1. View CSG Branches and Candidates\n"
        "2. Rate Candidates\n"
        "3. View Rating Overview\n"
        "0. Exit"
    )
    choice = input("Enter your choice: ")

    # VIEW BRANCHES
    if choice == "1":
        while True:
            print(
                "\nCENTRAL STUDENT GOVERNMENT (CSG)\n"
                "1. Executive Branch\n"
                "2. Legislative Branch\n"
                "3. Judiciary Branch\n"
                "0. Back to Main Menu"
            )
            branch_choice = input("Enter your choice: ")

            # EXECUTIVE BRANCH
            if branch_choice == "1":
                while True:
                    print(
                        "\nEXECUTIVE BRANCH\n"
                        "1. View President Candidate - Ken Torre\n"
                        "2. View President Candidate - Micah Reyes\n"
                        "3. View Vice President Candidate - Janah Abonitalla\n"
                        "4. View Vice President Candidate - Carl Mendoza\n"
                        "0. Back"
                    )
                    exec_choice = input("Enter your choice: ")

                    if exec_choice == "1":
                        print(
                            "\nCANDIDATE PROFILE\n"
                            "Name: Ken Torre\n"
                            "Position: PRESIDENT\n"
                            "Age: 19\n"
                            "Course: BSIT 1st Year\n"
                            "Platform: 'U.O.I – Uplifting Students Through Art'\n"
                            "Slogan: 'Pag may tsaga, may nilaga.'\n"
                        )
                        input("\nPress Enter to return...")

                    elif exec_choice == "2":
                        print(
                            "\nCANDIDATE PROFILE\n"
                            "Name: Micah Reyes\n"
                            "Position: PRESIDENT\n"
                            "Age: 20\n"
                            "Course: BSIT 2nd Year\n"
                            "Platform: 'UNITY – Empowering Students through Collaboration'\n"
                            "Slogan: 'Together we rise!'\n"
                        )
                        input("\nPress Enter to return...")

                    elif exec_choice == "3":
                        print(
                            "\nCANDIDATE PROFILE\n"
                            "Name: Janah Abonitalla\n"
                            "Position: VICE PRESIDENT\n"
                            "Age: 18\n"
                            "Course: BSIT 1st Year\n"
                            "Platform: 'LEAD – Leadership, Equality, Action, Development'\n"
                            "Slogan: 'Lead with purpose.'\n"
                        )
                        input("\nPress Enter to return...")

                    elif exec_choice == "4":
                        print(
                            "\nCANDIDATE PROFILE\n"
                            "Name: Carl Mendoza\n"
                            "Position: VICE PRESIDENT\n"
                            "Age: 19\n"
                            "Course: BSIT 2nd Year\n"
                            "Platform: 'SERVE – Student Empowerment and Resourceful Vision for Everyone'\n"
                            "Slogan: 'Service above self.'\n"
                        )
                        input("\nPress Enter to return...")

                    elif exec_choice == "0":
                        break
                    else:
                        print("\nInvalid input. Try again.")

            # LEGISLATIVE BRANCH
            elif branch_choice == "2":
                while True:
                    print(
                        "\nLEGISLATIVE BRANCH\n"
                        "1. Senator - Shem Borromeo\n"
                        "2. Senator - Alex Tanso\n"
                        "0. Back"
                    )
                    leg_choice = input("Enter your choice: ")

                    if leg_choice == "1":
                        print(
                            "\nCANDIDATE PROFILE\n"
                            "Name: Shem Borromeo\n"
                            "Position: Senator\n"
                            "Course: BSIT 1st Year\n"
                            "Platform: 'Digital literacy and student inclusion'\n"
                            "Slogan: 'Learn, Code, Lead.'\n"
                        )
                        input("\nPress Enter to return...")
                    elif leg_choice == "2":
                        print(
                            "\nCANDIDATE PROFILE\n"
                            "Name: Alex Tanso\n"
                            "Position: Senator\n"
                            "Course: BSHM 2nd Year\n"
                            "Platform: 'Green Campus Initiatives'\n"
                            "Slogan: 'Go Green!'\n"
                        )
                        input("\nPress Enter to return...")
                    elif leg_choice == "0":
                        break
                    else:
                        print("\nInvalid input. Try again.")

            # JUDICIARY BRANCH
            elif branch_choice == "3":
                while True:
                    print(
                        "\nJUDICIARY BRANCH\n"
                        "1. Judge - Benhassan Casir\n"
                        "2. Judge - Marie Dizon\n"
                        "0. Back"
                    )
                    jud_choice = input("Enter your choice: ")

                    if jud_choice == "1":
                        print(
                            "\nCANDIDATE PROFILE\n"
                            "Name: Benhassan Casir\n"
                            "Position: Judge\n"
                            "Course: BSCrim 2nd Year\n"
                            "Slogan: 'Justice for All.'\n"
                        )
                        input("\nPress Enter to return...")
                    elif jud_choice == "2":
                        print(
                            "\nCANDIDATE PROFILE\n"
                            "Name: Marie Dizon\n"
                            "Position: Judge\n"
                            "Course: BSCrim 2nd Year\n"
                            "Slogan: 'Ethics and Equality Above All.'\n"
                        )
                        input("\nPress Enter to return...")
                    elif jud_choice == "0":
                        break
                    else:
                        print("\nInvalid input. Try again.")

            elif branch_choice == "0":
                break
            else:
                print("\nInvalid input. Try again.")

    # RATE CANDIDATES
    elif choice == "2":
        while True:
            print(
                "\nRATE CANDIDATES\n"
                "1. President Ken Torre\n"
                "2. President Micah Reyes\n"
                "3. Vice President Janah Abonitalla\n"
                "4. Vice President Carl Mendoza\n"
                "5. Senator Shem Borromeo\n"
                "6. Senator  Alex Tanso\n"
                "7. Judge Benhassan Casir\n"
                "8. Judge Marie Dizon\n"
                "0. Back"
            )
            rate_choice = input("Enter your choice: ")

            if rate_choice == "0":
                break

            candidates = [
                "Ken Torre",
                "Micah Reyes",
                "Janah Abonitalla",
                "Carl Mendoza",
                "Shem Borromeo",
                "Alex Tanso",
                "Benhassan Casir",
                "Marie Dizon",
            ]

            if rate_choice not in [str(i) for i in range(1, 9)]:
                print("\nInvalid option.")
                continue

            name = candidates[int(rate_choice) - 1]
            print(f"\nYou selected {name}.\nPlease enter your ratings below:")
            leadership = int(input("Leadership (1–5): "))
            credibility = int(input("Credibility (1–5): "))
            popularity = int(input("Popularity (1–5): "))
            avg = round((leadership + credibility + popularity) / 3, 2)

            ratings[name]["total"] += avg
            ratings[name]["count"] += 1

            print(f"\nYou rated {name} with an average of {avg} ★")
            input("\nThank you for your feedback! Press Enter to return to the Rating Menu...")

    # RATING OVERVIEW
    elif choice == "3":
        print("\nRATING OVERVIEW\n")
        for name, data in ratings.items():
            if data["count"] > 0:
                avg = round(data["total"] / data["count"], 2)
                print(f"{name}: {avg} ★  (based on {data['count']} ratings)")
            else:
                print(f"{name}: No ratings yet.")
        input("\nPress Enter to return to Main Menu...")

    elif choice == "0":
        print(
            "\nThank you for using the Student Election Awareness Console!\n"
            "Stay informed. Lead with integrity. Vote wisely.\nGoodbye!"
        )
        break

    else:
        print("\nInvalid input. Try again.")

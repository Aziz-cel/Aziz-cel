- 👋 Hi, I’m @Aziz-cel
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Aziz-cel/Aziz-cel is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
 
def print_cubes(cubes):
    print("Current cubes: ", cubes)

def move_cube(cubes, direction):
    if direction == 'up' and len(cubes) > 0:
        cubes.insert(0, cubes.pop())
    elif direction == 'down' and len(cubes) > 0:
        cubes.append(cubes.pop(0))
    else:
        print("Invalid direction or empty cubes list.")
    return cubes

def main():
    target_number = 15  # Example target number
    cubes = [5, 3, 7, 2, 8]  # Example cubes
    print("Target number: ", target_number)
    print_cubes(cubes)
    
    while True:
        direction = input("Enter direction to move cube (up/down): ").strip().lower()
        cubes = move_cube(cubes, direction)
        print_cubes(cubes)
        current_sum = sum(cubes)
        print("Current sum: ", current_sum)
        
        if current_sum == target_number:
            print("Congratulations! You've matched the target number.")
            break
        else:
            print("Keep trying to match the target number.")

if __name__ == "__main__":
    main()